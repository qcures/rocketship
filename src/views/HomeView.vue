<script setup>
import CardContainer from "../components/CardContainer.vue";
import AboutView from "./AboutView.vue";
</script>

<template>
  <div class="home">
    <AboutView />
    <div class="cards">
      <CardContainer />
    </div>
  </div>
</template>

<style scoped>
.home {
  display: flex;
}

.cards {
  flex: auto;
}
</style>
