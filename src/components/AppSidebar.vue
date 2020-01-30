<template>
  <div class="sidebar">
    <img class="sidebar__logo" src="@/assets/img/svg/logo.svg" />
    <h1 class="sidebar__title">Premium</h1>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.sidebar {
  padding: 48px 24px 0 24px;
  border-radius: $border-radius 0px 0px $border-radius;
  background: $general-black;
  &__logo {
    margin-bottom: 13px;
  }
  &__title {
    font-size: 48px;
    color: $gold-color;
    @include rubik-bold;
  }
}
</style>
