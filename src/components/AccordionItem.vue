<template>
  <div class="accordion-item">
    <div class="accordion-item__header" @click="active = !active">
      <img class="accordion-item__icon" :src="require(`@/assets/img/icons/${itemData.icon}.svg`)" />
      <h3 class="accordion-item__title">{{ itemData.title }}</h3>
      <icon-base
        :class="['accordion-item__arrow', { 'is-active': active }]"
        class="input-block__icon"
        width="10"
        height="6"
      >
        <icon-arrow />
      </icon-base>
    </div>
    <p class="accordion-item__content" v-if="active">{{ itemData.content }}</p>
  </div>
</template>
<script>
import IconBase from "../components/IconBase.vue";
import IconArrow from "../components/icons/IconArrow.vue";
export default {
  components: {
    IconBase,
    IconArrow
  },
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
    margin-bottom: 16px;
    cursor: pointer;
    @media (max-width: $bk768) {
      min-height: 48px;
    }
  }
  &__icon {
    width: 20px;
    height: 20px;
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
    &.is-active {
      transform: rotate(180deg);
    }
    @media (max-width: $bk992) {
      display: none;
    }
  }
  &__content {
    @include rubik-reg;
    color: #fff;
    line-height: 24px;
  }
}
</style>
