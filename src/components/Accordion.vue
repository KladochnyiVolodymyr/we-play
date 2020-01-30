<template>
  <div class="accordion">
    <AccordionItem
      v-for="item in accordionData"
      :key="item.id"
      :item-data="item"
    />
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
