<template>
  <div class="home">
    <div class="splash-container">
      <div class="splash">
        <h1>Splendid Food</h1>
      </div>
    </div>

    <main class="wrapper">

      <h2>Recommended</h2>

      <div class="recommended">

        <ProductCard v-for="(item, index) in inventory.slice(0, 3)"
          v-bind:item="item"
          v-bind:index="index"
          v-bind:addToCart="addToCart"
          class="card"
        />

      </div>

    </main>
  </div>
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
