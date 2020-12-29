<script>
  export let post;
</script>

<style lang="scss">
  .up {
    padding: 32px;
    margin-bottom: 24px;
    background-color: $background-color;
    border-radius: $border-radius;

    &__body {
      color: $text-secondary;
      margin-top: 20px;
    }
  }
</style>

<div class="up">
  <p class="up__title body1 medium">{post.title}</p>
  <p class="up__body body2">{post.body}</p>
</div>
