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
    <div class="payment-footer">
      <div class="payment-footer__total">
        <span>Всего:</span>
        <span>$4</span>
      </div>
      <div class="payment-footer__btns">
        <Button type-btn="secondary" btn-text="Назад" />
        <Button type-btn="success" btn-text="Оплатить" />
      </div>
    </div>
    <div class="payment__agree">
      <p>
        By proceeding payment I agree to WePlay!
        <a href="#">& Conditions and Privacy Policy</a>
      </p>
    </div>
  </div>
</template>
<script>
import CreditCardTab from "../components/CreditCardTab.vue";
import Button from "../components/Button.vue";
export default { components: { CreditCardTab, Button } };
</script>
<style lang="scss" scoped>
.payment {
  padding: 48px 24px 24px;
  border-left: 1px solid $border-color-light;
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
  &-footer {
    border-top: 1px solid $border-color-light;
    border-bottom: 1px solid $border-color-light;
    padding-top: 28px;
    margin-bottom: 18px;
    &__total {
      display: flex;
      justify-content: space-between;
      margin-bottom: 53px;
      span {
        color: $general-black;
        @include rubik-med;
      }
    }
    &__btns {
      display: flex;
      justify-content: space-between;
      margin-bottom: 16px;
    }
  }
  &__agree {
    color: $grey-color;
    @include rubik-reg;
    font-size: 12px;
    a {
      color: $blue-color;
    }
  }
}
</style>
