<template>
  <div class="credit-card">
    <div class="credit-card__header">
      <div class="credit-card__logos">
        <img src="@/assets/img/mastercard-logo.svg" />
        <img src="@/assets/img/visa-logo.svg" />
        <img src="@/assets/img/amex-logo.svg" />
      </div>
      <div class="credit-card__security">
        <img src="@/assets/img/icons/lock.svg" />
        <p>Платежная информация защищена</p>
      </div>
    </div>
    <div class="credit-card__form">
      <div class="input-row">
        <InputBlock label="Card number" placeholder="5167 9855 6160 0974" input-type="number" />
      </div>
      <div class="input-row input-row_double">
        <InputBlock label="Valid thru" placeholder="MM/YY" input-type="number" input-size="small" />
        <InputBlock
          label="Security code"
          placeholder="••••"
          input-type="password"
          input-size="small"
        />
      </div>
    </div>
  </div>
</template>
<script>
import InputBlock from "../components/InputBlock.vue";
export default {
  components: {
    InputBlock
  }
};
</script>
<style lang="scss" scoped>
.credit-card {
  &__header {
    display: flex;
    justify-content: space-between;
    margin-bottom: 16px;
    @media (max-width: $bk576) {
      display: block;
      margin-bottom: 28px;
    }
  }
  &__logos {
    display: flex;
    align-items: center;
    img {
      margin-right: 24px;
    }
    @media (max-width: $bk576) {
      margin-bottom: 24px;
    }
  }
  &__security {
    display: flex;
    align-items: center;
    color: $blue-color;
    font-size: 12px;
    @include rubik-reg;
    img {
      margin-right: 12px;
    }
  }
}
.input-row {
  margin-bottom: 31px;
  &_double {
    display: flex;
    @media (max-width: $bk992) {
      margin-bottom: 24px;
    }
  }
}
</style>