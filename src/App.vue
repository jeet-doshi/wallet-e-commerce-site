<template>
  <div id="app">
    <Home></Home>
  </div>
</template>

<script>
import Home from './components/Home.vue'
import Product from './components/Product.vue'
import Checkout from './components/Checkout.vue'

export default {
  name: 'App',
  components:{ 
    Home,
    Product,
    Checkout
  }
}
</script>





