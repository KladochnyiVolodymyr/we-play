<template>
  <div class="accordion">
    <AccordionItem v-for="item in accordionData" :key="item.id" :item-data="item" />
  </div>
</template>
<script>
import AccordionItem from "../components/AccordionItem.vue";
export default {
  components: {
    AccordionItem
  },
  props: {
    accordionData: {
      type: Array
    }
  }
};
</script>
<style lang="scss" scoped>
.accordion {
  @media (max-width: $bk992) {
    display: grid;
    grid-template-columns: 250px 250px;
    grid-column-gap: 25px;
  }
  @media (max-width: $bk768) {
    grid-template-columns: 220px 220px;
  }
}
</style>
