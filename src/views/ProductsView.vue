<template>
  <main class="wrapper">
    <h1>Products</h1>

    <div class="card-container">
      <ProductCard v-for="(item, index) in inventory"
          v-bind:item="item"
          v-bind:index="index"
          v-bind:addToCart="addToCart"
          class="card"
        />
    </div>
  </main>
</template>

<script>
import ProductCard from '@/components/ProductCard.vue';

export default {
  props: ['inventory', 'addToCart'],
  components: {
    ProductCard
  }
}
</script>