<template>
  <div class="sidebar">
    <img class="sidebar__logo" src="@/assets/img/logo.svg" />
    <h1 class="sidebar__title">Premium</h1>
    <div class="sidebar__accordion">
      <Accordion :accordion-data="accordion" />
    </div>
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
  height: 100%;
  background: linear-gradient(
      0deg,
      rgba(1, 14, 40, 0) 0%,
      rgba(1, 14, 40, 0.8) 55.44%
    ),
    url("../assets/img/shutterstock.png");
  background-blend-mode: normal, lighten;
  background-position: bottom;
  background-size: cover;
  @media (max-width: $bk992) {
    border-radius: $border-radius $border-radius 0 0;
    padding: 48px 24px 24px 24px;
  }
  @media (max-width: $bk576) {
    padding: 40px 16px 24px 16px;
  }
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
    @media (max-width: $bk576) {
      margin-bottom: 0;
    }
  }
  &__accordion {
    @media (max-width: $bk576) {
      display: none;
    }
  }
}
</style>
