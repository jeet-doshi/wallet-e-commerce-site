<template>
<div>
<div>
  <div class="product-box">
    <div class="product-image">
      <img :src="currentProduct.image" alt="" width="300px" height="300px">
    </div>
    <div class="product-info">
      <h2 class="product-title">{{ currentProduct.name }}</h2>
      <span class="product-price">Rs {{ currentProduct.price }}</span>
      <span class="product-orgprice">Rs <strike>{{ currentProduct.orgprice }}</strike></span>
      <div style="margin-top: 10px;"> Available Colors: </div>
      <div class="color-options">
        <!-- <div> Colors: </div> -->
        <div class="figure black"></div>
        <div class="figure blue"></div>
        <div class="figure green"></div>
        <div class="figure brown"></div>
      </div>

      <btn btnColor="btn btn-large btn-info"
          @click.native="openModal()">
        More Info
      </btn>
      <btn btnColor="btn btn-large btn-sucess" :cartIcon="true"
      @click.native="addProductToCart(currentProduct)">
        Buy Now
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
<div class="footer">
<div class="container2">
    <div class="footer_child footer_child_1">
        <img src="https://i.imgur.com/ruPamPO.png" width="300px" height="100px">
        <br />
        <!-- <h1>Wallet Town</h1> -->
    </div>
    <div class="footer_child">
        <ul>
            <li class="first">Quick Links</li>
            <li class="linker">
              <router-link to="/" style="color:white">Products</router-link>
            </li>
            <li class="linker">
              <router-link to="/checkout" style="color:white">Cart</router-link>
            </li>
        </ul>
    </div>
    <div class="footer_child">
        <ul>
            <li class="first">Contact Us</li>
            <li>
                29th Street, plot 304,
                Washington, 410206 USA.
            </li>
            <li>+91-9087645364</li>
            <li>enquiry@wallettown.com</li>
        </ul>
    </div>
</div>
</div>
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

.color-options {
  height: 50px;
  /* background-color: red; */
  display: flex;
}

.figure {
  background-color: green;
  border-radius: 50px;
  width: 40px;
  height: 40px;
  margin-right: 15px;
  margin-top: 10px;
}

.black {
  background-color: black;
}

.blue {
  background-color: ROYALBLUE;
}

.green {
  background-color: olivedrab;
}

.brown {
  background-color: brown ;
}

/* CSS for footer */
   .container2{
    display: flex;
    width:100%;
    background-color: DIMGREY;
    margin-top: 5px;
}
.footer{
    width: 100%;
    height: 225px;
    /* margin-top: 750px; */
    background-color: DIMGREY;
    display: flex;
    flex-direction: row;
    justify-content: center;
}
.footer_child{
    height: 200px;
    width: 25%;
    margin-left: 20px;
    font-family: segoe UI;
    display: flex;
    justify-content: center;
    background-color: DIMGREY;
}
.footer_child_1{
    align-items: center;
    color: white;
    font-size: 30px;
    background-color: DIMGREY;
    flex-direction: column;
}

.footer_child_4{
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: DIMGREY;
}

.first{
    font-size: 22px;
}

.footer_child ul {
    margin-top: 40px;
    background-color: DIMGREY;
}

.footer_child li {
    list-style-type: none;
    margin-bottom: 10px;
    color: white;
    background-color:DIMGREY;
}

.linker:hover{
    color: orange;
    cursor: pointer;

}

</style>
