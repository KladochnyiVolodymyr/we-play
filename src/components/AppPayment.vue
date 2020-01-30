<template>
  <div class="payment">
    <ul class="payment-switch">
      <li class="payment-switch__item is-active">Credit card</li>
      <li class="payment-switch__item">PayPal</li>
    </ul>
    <div class="payment-content">
      <div class="payment-content__tab">
        <CreditCardTab />
      </div>
    </div>
  </div>
</template>
<script>
import CreditCardTab from "../components/CreditCardTab.vue";
export default { components: { CreditCardTab } };
</script>
<style lang="scss" scoped>
.payment {
  padding: 48px 24px 24px;
  &-switch {
    display: flex;
    margin-bottom: 24px;
    &__item {
      color: $grey-color;
      @include rubik-med;
      font-size: 16px;
      line-height: 24px;
      cursor: pointer;
      padding: 0 18px 7px;
      &.is-active {
        color: $general-black;
        border-bottom: 2px solid $blue-color;
      }
    }
  }
}
</style>
