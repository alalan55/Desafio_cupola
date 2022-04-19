<template>
  <div class="home-template">
    <div class="content-home">
      <Card
        class="card"
        v-for="item in informations"
        :cardData="item"
        :key="item.id"
      />
    </div>
  </div>
</template>

<script>
import Card from "@/components/organisms/CardComponent.vue";
export default {
  components: {
    Card,
  },
  props: {
    informations: { type: Array, required: true, default: undefined },
  },
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/colors.scss";

.home-template {
  background: $grey-1;
  height: 100vh;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  .content-home {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    gap: 2.5rem;

    .card {
      margin: 1rem 0;
    }
  }
}
</style>