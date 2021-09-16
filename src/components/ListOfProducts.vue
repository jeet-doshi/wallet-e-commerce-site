<template>
  <ul class="listOfProducts">
    <li v-for="(product, index) in products" :key="index" class="product">
      <img :src="product.image" alt="" height="300px" width="300px">
      <router-link to="/product-details">
        <h2 class="product-name"
            @click="addCurrentProduct(product)">
          {{ product.name }}
        </h2>
      </router-link>
      <div class="product-price">
        <span style="color: red;">New Price: <strong> Rs {{ product.price }} </strong> </span>
        <span>Rs <strike>{{ product.orgprice }}</strike></span>
      </div>

      <btn btnColor="btn btn-large btn-sucess"
          :cartIcon="true"
          @click.native="addProductToCart(product)">
        Add to cart
      </btn>
    </li>
  </ul>
</template>

<script>
import { mapActions } from 'vuex';
import btn from './Btn';

export default {
  props: ['products'],

  components: {
    btn,
  },
  methods: {
    ...mapActions([
      'addProduct',
      'currentProduct',
    ]),

    addProductToCart(product) {
      this.addProduct(product);
    },
    addCurrentProduct(product) {
      this.currentProduct(product);
    },
  },
};
</script>

<style scoped>
  .listOfProducts {
    width: 100%;
    max-width: 1000px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    padding: 0;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
  }

  .product {
    width: 310px;
    background-color: #fff;
    list-style: none;
    box-sizing: border-box;
    padding: 1em;
    margin: 1em 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    border-radius: 7px;
    border:solid black;
    margin-top: 30px;
  }

  .product:hover{
  border-radius: 5% 5% 5% 5% / 5% 5% 5% 5% ;
  box-shadow: 10px 10px rgba(0,0,0,.25);
  box-shadow: 23px 23px rgba(0,0,0,.15);
  transition: all .4s ease;
  }

  .product-name {
    font-size: 1.2em;
    font-weight: normal;
  }

  .product-name:hover {
    cursor: pointer;
    text-decoration: underline;
  }

  .product-price {
    width: 100%;
    align-self: flex-start;
    display: flex;
    justify-content: space-between;
    margin-bottom: .5em;
  }


</style>

