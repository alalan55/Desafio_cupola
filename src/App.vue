<script setup>
import Home from "@/components/templates/HomeTemplate.vue";
import { informations } from "@/mock";

const informationsData = informations;
</script>

<template>
  <main>
    <Home :informations="informationsData" />
  </main>
</template>
