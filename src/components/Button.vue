<template>
  <div :class="['button',`button_${typeBtn}`]">{{btnText}}</div>
</template>
<script>
export default {
  props: {
    typeBtn: {
      type: String,
      default: "primary"
    },
    btnText: {
      type: String
    }
  }
};
</script>
<style lang="scss" scoped>
.button {
  padding: 11px 16px;
  font-size: 14px;
  @include rubik-med;
  border-radius: 20px;
  box-sizing: border-box;
  cursor: pointer;
  &_secondary {
    color: $blue-color;
    border: 1px solid $blue-color;
  }
  &_success {
    background: linear-gradient(90deg, #c59639 0%, #e9c467 100%);
    color: #fff;
  }
  &_primary {
  }
}
</style>