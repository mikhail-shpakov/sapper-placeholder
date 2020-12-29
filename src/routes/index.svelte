<script>
  import {onMount} from 'svelte'
  import PageHeader from "../components/PageHeader.svelte";
  import UserCard from "../components/UserCard.svelte";

  let users = []

  onMount(async () => {
    try {
      const res = await fetch(`https://jsonplaceholder.typicode.com/users`);
      users = await res.json();
    } catch (e) {
      alert(`Произошла ошибка при загрузке пользователей: ${e}`)
    }
  })

</script>

<style lang="scss">
  .users {
    @media (min-width: $desktop) {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      grid-gap: 24px;
    }
  }
</style>

<svelte:head>
  <title>Первое приложение на Sapper.js</title>
</svelte:head>

<PageHeader
    title="Sapper.js"
    subtitle="Создаём своё первое приложение с помощью
      <a href='https://jsonplaceholder.typicode.com/' target='_blank' rel='noopener noreferrer'>
        JSON Placeholder
      </a>"
/>

<div class="users">
  {#each users as user}
    <UserCard user={user}/>
  {/each}
</div>
