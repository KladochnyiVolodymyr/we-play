<template>
  <div class="app">
    <div class="app__sidebar">
      <AppSidebar />
    </div>
    <div class="app__payment">
      <AppPayment />
    </div>
  </div>
</template>

<script>
import AppSidebar from "./components/AppSidebar.vue";
import AppPayment from "./components/AppPayment.vue";

export default {
  name: "app",
  components: { AppSidebar, AppPayment }
};
</script>

<style lang="scss" scoped>
.app {
  width: 848px;
  margin: 0 auto;
  margin-top: 85px;
  border: 1px solid $gold-color;
  border-radius: $border-radius;
  display: flex;
  &__sidebar {
    width: 324px;
  }
  &__payment {
    width: 524px;
  }
}
</style>
