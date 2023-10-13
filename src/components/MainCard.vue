<script setup>
const props = defineProps({
  product: { type: Object },
});
</script>
<template>
  <div class="card" :class="`${product.available ? '' : 'agotado'}`">
    <h1>{{ product.product }}</h1>
    <div class="card_img">
      <img :src="product.image_url" alt="" />
    </div>
    <h2>{{ product.description }}</h2>
    <div class="price_stock_row">
      <h3 class="prices">{{ product.price }}</h3>
      <div class="disponible">AGOTADO</div>
    </div>
  </div>
</template>

<style scoped>
body {
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
}

.agotado .prices {
  text-decoration: line-through;
}

.agotado .card_img {
  filter: grayscale(100%);
}

.disponible {
  display: none;
}

.agotado .disponible {
  display: initial;
  color: red;
}

.card {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  width: 244px;
  height: 307px;
  border-radius: 23px;
  background: #d9d9d9;
  padding: 20px;
  white-space: nowrap;
  overflow: initial;
}

.heading-container {
  display: flex;
  align-items: flex-start;
  flex-direction: column;
}

.card h1 {
  font-size: 24px;
  color: #333333;
  margin: 0;
}

.card_img {
  background: #8d8d8d;
  width: 200px;
  height: 139px;
}

.card_img > img {
  object-fit: cover;
  width: 100%;
  height: 100%;
}

.card h2 {
  font-size: 20px;
  color: #333333;
  margin-top: 10px;
}

.price_stock_row {
  display: flex;
  justify-content: space-between;
  width: 100%;
  margin-top: auto;
}

.price_stock_row h3 {
  font-size: 16px;
  color: #666666;
  margin-left: 10px;
}

.price_stock_row h4 {
  font-size: 16px;
  color: #666666;
  margin-right: 10px;
}
</style>
