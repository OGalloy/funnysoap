<template>
  <div>
    <CatalogProduct v-for="product in products" :key="product.title" :img="product.img" :price="product.price"
      :title="product.title" />
  </div>
</template>

<script lang="ts" setup>
const products = [
  {
    img: '',
    price: '',
    title: ''
  }
]
</script>

<style></style>