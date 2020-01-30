<template>
  <div class="sidebar">
    <img class="sidebar__logo" src="@/assets/img/logo.svg" />
    <h1 class="sidebar__title">Premium</h1>
    <Accordion :accordion-data="accordion" />
  </div>
</template>
<script>
import Accordion from "../components/Accordion.vue";
export default {
  components: {
    Accordion
  },
  data() {
    return {
      accordion: [
        {
          id: 1,
          title: "Закрытые турниры",
          content:
            "Участвуй в закрытых турнирах, с возможностью выиграть высокие призовые и эксклюзивные призы.",
          icon: "tournament"
        },
        {
          id: 2,
          title: "Приоритетная поддержка",
          content:
            "Участвуй в закрытых турнирах, с возможностью выиграть высокие призовые и эксклюзивные призы.",
          icon: "support"
        },
        {
          id: 3,
          title: "Премиум бейдж",
          content:
            "Участвуй в закрытых турнирах, с возможностью выиграть высокие призовые и эксклюзивные призы.",
          icon: "premium"
        },
        {
          id: 4,
          title: "Расширенная статистика",
          content:
            "Участвуй в закрытых турнирах, с возможностью выиграть высокие призовые и эксклюзивные призы.",
          icon: "rating"
        }
      ]
    };
  }
};
</script>
<style lang="scss" scoped>
.sidebar {
  padding: 48px 24px 100px 24px;
  border-radius: $border-radius 0px 0px $border-radius;
  background: $general-black;
  height: 100%;
  &__logo {
    margin-bottom: 13px;
  }
  &__title {
    font-size: 48px;
    @include rubik-bold;
    background: -webkit-linear-gradient(360deg, #c59639 0%, #e9c467 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 25px;
  }
}
</style>
