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
  padding: 10px 16px;
  font-size: 14px;
  @include rubik-med;
  border-radius: 20px;
  box-sizing: border-box;
  cursor: pointer;
  transition: 0.3s;
  &:hover {
    opacity: 0.8;
  }
  &_secondary {
    color: $blue-color;
    border: 1px solid $blue-color;
  }
  &_success {
    background: linear-gradient(90deg, #c59639 0%, #e9c467 100%);
    color: #fff;
    padding: 12px 16px 9px;
  }
  &_primary {
    background-color: $blue-color;
    border-radius: 4px;
    color: #fff;
  }
}
</style>