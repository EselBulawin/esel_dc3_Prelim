<template>
  <div class="item-list">
    <h2>Item List</h2>
    <div class="item-container">
      <ItemList
        v-for="product in products"
        :key="product.id"
        :product="product"
        @add-to-cart="handleAddToCart"
      />
       <h3>{{ product.name }}</h3>
    <p class="product-price">Price: P{{ product.price }}</p>
    <button @click="addToCart" :aria-label="`Add ${product.name} to cart`">Add to Cart</button>
    </div>
  </div>
</template>

<script>
import Item from './Item.vue'

export default {
  name: 'ItemList',
  components: {
    ItemList
  },
  props: {
    products: {
      type: Array,
      required: true
    }
  },
  methods: {
    handleAddToCart(product) {
      console.log(`Adding product to cart: ${product.name}`)
      console.log('Product Details:', product)
    }
  }
}
</script>