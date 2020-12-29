<script context="module">
  export async function preload({params}) {
    try {
      const res = await this.fetch(`https://jsonplaceholder.typicode.com/posts?userId=${params.id}`);
      const posts = await res.json();
      return {posts}
    } catch (e) {
      this.error(e);
    }
  }
</script>

<script>
  import UserPost from "../../components/UserPost.svelte";
  import PageHeader from "../../components/PageHeader.svelte";

  export let posts;
</script>

<svelte:head>
  <title>Первое приложение на Sapper.js</title>
</svelte:head>

<PageHeader
    title="Все посты"
    subtitle="<a href='/'>Вернуться на главную</a>"/>

<div class="posts">
  {#each posts as post}
    <UserPost post={post}/>
  {/each}
</div>
