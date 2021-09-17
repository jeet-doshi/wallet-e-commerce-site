<template>
<div>
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
  <!-- Footer -->
  <!-- <div class="footer">
<div class="container2">
    <div class="footer_child footer_child_1">
        <img src="https://i.imgur.com/ruPamPO.png" width="300px" height="100px">
        <br />
        <h1>Wallet Town</h1>
    </div>
    <div class="footer_child">
        <ul>
            <li class="first">Quick Links</li>
            <li class="linker">
              <router-link to="/" style="color:white">Products</router-link>
            </li>
            <li class="link">
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
</div> -->
</div>
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

/* CSS for footer */
   .container2{
    display: flex;
    width:100%;
    background-color: DIMGREY;
    margin-top: 5px;
    margin-left: 350px;
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

.linker{
  color: white;
}
.linker:hover{
    color: orange;
    cursor: pointer;

}
</style>

