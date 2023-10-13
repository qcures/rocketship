<script setup>
import { products } from "./../database/card_database";
import MainCard from "./MainCard.vue";
</script>
<template>
  <section>
    <div class="card-container">
      <MainCard v-for="p in products" :product="p" />
    </div>
  </section>
</template>

<style scoped>
.card-container {
  margin-top: 50px;
  margin-bottom: 50px;
  justify-items: center;
  justify-content: center;
  display: grid;
  grid-template-columns: repeat(3, 244px);
  gap: 20px;
}
</style>
