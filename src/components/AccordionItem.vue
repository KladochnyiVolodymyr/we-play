<template>
  <div class="accordion-item">
    <div class="accordion-item__header" @click="active = !active">
      <img
        class="accordion-item__icon"
        :src="require(`@/assets/img/svg/${itemData.icon}.svg`)"
      />
      <h3 class="accordion-item__title">{{ itemData.title }}</h3>
      <img
        :class="[
          'accordion-item__arrow',
          { 'accordion-item__arrow_active': active }
        ]"
        src="@/assets/img/svg/arrow.svg"
      />
    </div>
    <p class="accordion-item__content" v-if="active">
      {{ itemData.content }}
    </p>
  </div>
</template>
<script>
export default {
  props: {
    itemData: {
      type: Object
    }
  },
  data() {
    return {
      active: false
    };
  }
};
</script>
<style lang="scss" scoped>
.accordion-item {
  margin-bottom: 24px;
  &__header {
    display: flex;
    position: relative;
    align-self: center;
    margin-bottom: 16px;
    cursor: pointer;
  }
  &__title {
    @include rubik-med;
    font-size: 16px;
    line-height: 24px;
    color: #fff;
    margin-left: 10px;
  }
  &__arrow {
    position: absolute;
    right: 8px;
    top: 8px;
    &_active {
      transform: rotate(180deg);
    }
  }
  &__content {
    @include rubik-reg;
    color: #fff;
    line-height: 24px;
  }
}
</style>
