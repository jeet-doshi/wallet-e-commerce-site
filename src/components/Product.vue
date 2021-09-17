<template>
<div>
  <div class="product-box">
    <div class="product-image">
      <img :src="currentProduct.image" alt="" width="300px" height="300px">
      <stars :rate="rated(currentProduct.stars)" :totalReviews="currentProduct.totalReviews"/>
    </div>
    <div class="product-info">
      <h2 class="product-title">{{ currentProduct.name }}</h2>
      <span class="product-price">Rs {{ currentProduct.price }}</span>
      <span class="product-orgprice">Rs <strike>{{ currentProduct.orgprice }}</strike></span>
      <btn btnColor="btn btn-large btn-sucess" :cartIcon="true"
      @click.native="addProductToCart(currentProduct)">
        Buy Now
      </btn>
      <btn btnColor="btn btn-large btn-info"
          @click.native="openModal()">
        More Info
      </btn>
    </div>
    <modal>{{ currentProduct.details }}</modal>
  </div>

  <ul class="listOfProducts">
    <li v-for="(product, index) in suggestedproducts" :key="index" class="product">
      <img :src="product.image" alt="" height="300px" width="300px">
      <router-link to="/product-details">
        <h2 class="product-name"
            @click="addCurrentProduct(product)">
          {{ product.name }}
        </h2>
      </router-link>
      <div class="product-price">
        <span>Rs {{ product.price }}</span>
        <span>Rs <strike>{{ product.orgprice }}</strike></span>
      </div>
      <btn btnColor="btn btn-large btn-sucess"
          :cartIcon="true"
          @click.native="addProductToCart(product)">
        Add to cart
      </btn>
    </li>
  </ul>
</div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex';
import btn from './Btn';
import modal from './Modal';

export default {
  props: ['suggestedproducts'],
  components: {
    btn,
    modal,
  },

  computed: {
    ...mapGetters({
      currentProduct: 'getCurrentProduct',
    }),
  },

  methods: {
    ...mapActions([
      'addProduct',
      'showOrHiddenModal',
    ]),
    addProductToCart(product) {
      this.addProduct(product);
    },
    rated(rate) {
      return `${rate * 20}%`;
    },
    openModal() {
      this.showOrHiddenModal();
    },
  },

};
</script>

<style scoped>
  .product-box {
    width: 800px;
    height: 400px;
    margin: 50px auto;
    box-sizing: border-box;
    padding: 1.5em;
    background-color: #fff;
    border-radius: 7px;
    display: flex;
    justify-content: space-around;
    align-items: center;
  }

  .product-image {
    width: 300px;
  }

  .product-info {
    width: 400px;
    align-self: flex-start;
  }

  .product-title {
    font-weight: normal;
  }

  .product-price {
    font-size: 2em;
    font-weight: bolder;
  }

  .product-orgprice {
    font-size: 1.5em;
    margin-left: 4em;
  }

  .product-box button {
    width: 300px;
    margin: .3em 0;
  }
   .listOfProducts {
    width: 100%;
    max-width: 1000px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    padding: 0;
  }
</style>
