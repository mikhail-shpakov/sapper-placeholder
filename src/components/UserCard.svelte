<script>
  import UserCardInfo from "./UserCardInfo.svelte";

  export let user;
</script>

<style lang="scss">
  .uc {
    padding: 32px;
    background: $background-color;
    border-radius: $border-radius;
    margin-bottom: 24px;

    @media (min-width: $desktop) {
      margin-bottom: 0;
    }

    &__name {
      margin-bottom: 28px;
    }

    &__link {
      display: inline-flex;
      margin-top: 28px;
    }
  }
</style>

<div class="uc">
  <p class="uc__name body1 medium">{user.name}</p>

  <UserCardInfo icon="city" info={user.address.city}/>
  <UserCardInfo icon="site" info={user.website}/>
  <UserCardInfo icon="email" info={user.email}/>

  <a
      class="uc__link"
      href="/user/{user.id}">
    Смотреть посты пользователя
  </a>
</div>
