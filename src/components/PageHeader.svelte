<script>
  export let title;
  export let subtitle;
</script>

<style lang="scss">
  .ph {
    margin-bottom: 64px;

    &__title {
      margin: 0 0 20px;
    }

    &__subtitle {
      color: $text-secondary;
    }
  }
</style>

<div class="ph">
  <h1 class="h1 ph__title">{@html title}</h1>
  <p class="body2 ph__subtitle">{@html subtitle}</p>
</div>
