<script>
  import PageFooter from "../components/PageFooter.svelte";
</script>

<style lang="scss" global> // TODO
  main {
    position: relative;
    max-width: $max-content;
    margin: 40px auto;
    padding: 0 24px;

    @media (min-width: $tablet) {
      margin: 80px auto;
    }

    p {
      margin: 0;
    }
  }
</style>

<main>
  <slot/>
  <PageFooter/>
</main>
