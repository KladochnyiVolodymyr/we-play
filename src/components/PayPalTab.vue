<template>
  <div class="pay-pal">
    <p class="pay-pal__text">Подпишись на WePlay! Premium используя PayPal account</p>
    <div class="pay-pal__btn">
      <Button type-btn="primary" btn-text="Перейти на PayPal" />
    </div>
  </div>
</template>
<script>
import Button from "../components/Button.vue";
export default {
  components: {
    Button
  }
};
</script>
<style lang="scss" scoped>
.pay-pal {
  &__text {
    @include rubik-reg;
    font-size: 16px;
    color: $grey-color;
    margin-bottom: 24px;
    line-height: 24px;
  }
  &__btn {
    width: 161px;
    margin: 0 auto;
  }
}
</style>