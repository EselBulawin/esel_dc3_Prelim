<template>
  <div class="container">
    <p v-if="item" key="item" Products:products="products" />
  </div>
</template>

<script>
import ProductList from './components/ItemList.vue'

export default {
  name: 'Item',
  components: {
    ProductList
  },
  data() {
    return {
      products: [
        {name: 'Coke', price: 100.00 },
        {name: 'Sprite', price: 20.16 },
        {name: 'Royal', price: 50.67 }
      ]
    }
  }
}
</script>
