<template>
  <div class="home-template">
    <div class="content-home">
      <Card class="card" />
      <Card class="card" />
      <Card class="card" />
    </div>
  </div>
</template>

<script setup>
import Card from "@/components/organisms/CardComponent.vue";
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