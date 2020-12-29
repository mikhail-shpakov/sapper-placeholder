<script>
  export let icon;
  export let info;

  let iconPath = `icons/${icon}.svg`
</script>

<style lang="scss">
  .uci {
    color: $text-secondary;
    display: flex;
    margin: 16px 0;

    &__info {
      margin-left: 16px;
      text-overflow: ellipsis;
      white-space: nowrap;
      overflow: hidden;
    }
  }
</style>

<div class="uci">
  <img
      src={iconPath}
      alt={icon}
      loading="lazy">
  <p class="uci__info">{info}</p>
</div>
