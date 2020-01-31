<template>
  <div :class="['input-block', `input-block_${inputSize}`]">
    <label class="input-block__label">{{ label }}</label>
    <the-mask
      class="input-block__input"
      :mask="mask"
      :placeholder="placeholder"
    />
    <icon-base class="input-block__icon" width="16" height="20">
      <icon-lock fill="#63708a" />
    </icon-base>
  </div>
</template>
<script>
import IconBase from "../components/IconBase.vue";
import IconLock from "../components/icons/IconLock.vue";
import { TheMask } from "vue-the-mask";

export default {
  components: {
    IconBase,
    IconLock,
    TheMask
  },
  props: {
    label: {
      type: String
    },
    placeholder: {
      type: String
    },
    inputSize: {
      type: String,
      default: "full"
    },
    mask: {
      type: String
    }
  }
};
</script>
<style lang="scss" scoped>
.input-block {
  position: relative;
  &:not(:last-child) {
    margin-right: 24px;
  }
  &_full {
    width: 100%;
  }
  &_small {
    width: 142px;
  }
  &__label {
    @include rubik-bold;
    font-size: 12px;
    display: block;
    margin-bottom: 10px;
  }
  &__input {
    border: 1px solid $grey-light;
    border-radius: 4px;
    padding: 10px 44px 10px 16px;
    box-sizing: border-box;
    width: 100%;
    font-size: 16px;
    line-height: 16px;
    @include rubik-reg;
    color: $general-black;
    &::placeholder {
      color: $grey-light;
    }
    &::-webkit-outer-spin-button,
    &::-webkit-inner-spin-button {
      -webkit-appearance: none;
      margin: 0;
    }
    &[type="number"] {
      -moz-appearance: textfield;
    }
  }
  &__icon {
    position: absolute;
    right: 19px;
    bottom: 11px;
  }
}
</style>
