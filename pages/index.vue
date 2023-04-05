<template>
  <h1>Index</h1>
  <template v-for="dd in products">
      <p>
          <div>{{ dd.title }}</div>
          <NuxtLink :to="`/products/${dd.id}`">Detail...</NuxtLink>
      </p>
  </template>
</template>
<script setup>
const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>