<template>
<body>
<!-- Header Starts -->
<div class="header">
    <div class="container">
        <div class="navbar">
            <div class="logo">
                <img src="Images/logo-without-bg.png">
            </div>
        <nav>
            <ul>
                <li><a href="">Home</a></li>
                <li><a href="">Products</a></li>
                <li><a href="">About Us</a></li>
                <!-- <li><a href="">  </a></li> -->
                <!-- <li><a href="">Account</a></li> -->
            </ul>
        </nav>
        <img src="Images/Cart.png" class="cart">
        <div style="margin-top: 50px; font-weight: bold;  background-color: #ba0e44;">  <h3 style=" background-color: #ba0e44;"> (0) </h3>  </div>
    </div>
    </div>
</div>
<!-- Header Ends -->

<!-- Checkout Starts -->
<div class="min-h-screen bg-gray-300">
  <div class="container mx-auto p-10 max-w-screen-lg">
    <div class="bg-white rounded shadow p-8">
      <!-- Order Summary  -->
      <div>
        <h3 class="text-xl mt-4 font-bold">Order Summary</h3>
        <!--     BOX     -->
        <div class="border w-full rounded mt-5 flex p-4 justify-between items-center flex-wrap">
          <img src="Images/Horn-Rakhi-Gift-Hamper/Black.jpg   " class="w-12">
          <div class="w-2/3">
            <h3 class="text-lg font-medium">Black Jacket XL</h3>
            <p class="text-gray-600 text-xs">Sold by <b>Aashir Khan</b></p>
            <h4 class="text-red-700 text-xs font-bold mt-1">Only 2 left in stock</h4>
          </div>
          <div>
            <h4 class="text-3xl font-medium"><sup class="text-lg text-purple-800">$</sup> 89</h4>
            <h5 class="text-sm font-bold text-purple-800">60% OFF</h5>
          </div>
          <div class="w-full flex justify-between mt-4">
            <button class="text-red-700 hover:bg-red-100 px-2">DELETE</button>
            <label class="block uppercase tracking-wide text-gray-700" for="grid-first-name">
              QTY
              <select class="ml-3 text-sm bg-purple-700 border border-purple-200 text-white p-2 rounded leading-tight" id="grid-state">
                <option>1</option>
                <option>2</option>
              </select>
            </label>
          </div>
        </div>
        <div class="border w-full rounded mt-5 flex p-4 justify-between items-center flex-wrap">
          <img src="Images/Horn-Rakhi-Gift-Hamper/Black.jpg   " class="w-12">
          <div class="w-2/3">
            <h3 class="text-lg font-medium">Black Hat</h3>
            <p class="text-gray-600 text-xs">Sold by <b>Taha Dildar</b></p>
            <h4 class="text-red-700 text-xs font-bold mt-1">Only 1 left in stock</h4>
          </div>
          <div>
            <h4 class="text-3xl font-medium"><sup class="text-lg text-purple-800">$</sup> 20</h4>
            <h5 class="text-sm font-bold text-purple-800">40% OFF</h5>
          </div>
          <div class="w-full flex justify-between mt-4">
            <button class="text-red-700 hover:bg-red-100 px-2">DELETE</button>
            <label class="block uppercase tracking-wide text-gray-700" for="grid-first-name">
              QTY
              <select class="ml-3 text-sm bg-purple-700 border border-purple-200 text-white p-2 rounded leading-tight" id="grid-state">
                <option>1</option>
                <option>2</option>
              </select>
            </label>
          </div>
        </div>
      </div>
      <button class="px-4 py-4 bg-purple-700 text-white w-full mt-3 rounded shadow font-bold hover:bg-purple-900">PROCEED TO CHECKOUT SCREEN</button>
    </div>
    <div class="flex justify-between mt-8 flex-wrap lg:justify-center">
      <div class="bg-white rounded shadow p-2 w-full lg:w-2/4">
        <div class="w-full bg-orange-200 px-8 py-6">
          <h3 class="text-2xl mt-4 font-bold">Price Breakdown</h3>
          <div class="flex justify-between mt-3">
            <div class="text-xl text-orange-900 font-bold">Amount</div>
            <div class='text-xl text-right font-bold '>$102</div>
          </div>
          <div class="flex justify-between mt-3">
            <div class="text-xl text-orange-900 font-bold">VAT (15%)</div>
            <div class='text-xl text-right font-bold'>$12</div>
          </div>
          <div class="bg-orange-300 h-1 w-full mt-3"></div>
          <div class="flex justify-between mt-3">
            <div class="text-xl text-orange-900 font-bold">Total Amount</div>
            <div class="text-2xl text-orange-900 font-bold">$114</div>
          </div>
          <button class="px-4 py-4 bg-purple-700 text-white w-full mt-3 rounded shadow font-bold hover:bg-purple- 900"> CHECKOUT</button>
        </div>
      </div>
      <div class="bg-white rounded shadow px-10 py-6 w-full mt-4 flex flex-wrap justify-center lg:w-2/4 lg:ml-3">
        <div class="pr-8">
        <h3 class="text-2xl mt-4 font-bold text-purple-900">Thank You!</h3>
        <h4 class="text-sm text-gray-600 font-bold">ORDER #1234</h4>
        </div>
        <img src="https://image.flaticon.com/icons/svg/1611/1611768.svg" alt="" class="w-24">
      </div>
    </div>
  </div>
</div>
<!-- Checkout Ends -->

<!-- Footer Starts -->
<div class="footer">
<div class="container2">
    <div class="footer_child footer_child_1">
        <img src="Images/logo-without-bg.png" width="300px" height="100px">
        <br />
        <!-- <h1>Wallet Town</h1> -->
    </div>
    <div class="footer_child">
        <ul>
            <li class="first">Quick Links</li>
            <li>Home</li>
            <li>Products</li>
            <li>About Us</li>
            <li>Cart</li>
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

<!-- Footer Ends -->
</body>

</template>

<script>
const imgs = document.querySelectorAll(".img-select a");
const imgBtns = [...imgs];
let imgId = 1;

imgBtns.forEach((imgItem) => {
  imgItem.addEventListener("click", (event) => {
    event.preventDefault();
    imgId = imgItem.dataset.id;
    slideImage();
  });
});

function slideImage() {
  const displayWidth = document.querySelector(
    ".img-showcase img:first-child"
  ).clientWidth;

  document.querySelector(".img-showcase").style.transform = `translateX(${
    -(imgId - 1) * displayWidth
  }px)`;
}

window.addEventListener("resize", slideImage);
</script>


<style>
.card-wrapper{
    max-width: 1100px;
    margin: 0 auto;
}
img{
    width: 100%;
    display: block;
}
.img-display{
    overflow: hidden;
}
.img-showcase{
    display: flex;
    width: 100%;
    transition: all 0.5s ease;
}
.img-showcase img{
    min-width: 100%;
}
.img-select{
    display: flex;
}
.img-item{
    margin: 0.3rem;
}
.img-item:nth-child(1),
.img-item:nth-child(2),
.img-item:nth-child(3){
    margin-right: 0;
}
.img-item:hover{
    opacity: 0.8;
}
.product-content{
    padding: 2rem 1rem;
}
.product-title{
    font-size: 3rem;
    text-transform: capitalize;
    font-weight: 700;
    position: relative;
    color: #12263a;
    margin: 1rem 0;
}
.product-title::after{
    content: "";
    position: absolute;
    left: 0;
    bottom: 0;
    height: 4px;
    width: 80px;
    background: #12263a;
}
.product-link{
    text-decoration: none;
    text-transform: uppercase;
    font-weight: 400;
    font-size: 0.9rem;
    display: inline-block;
    margin-bottom: 0.5rem;
    background: #256eff;
    color: #fff;
    padding: 0 0.3rem;
    transition: all 0.5s ease;
}
.product-link:hover{
    opacity: 0.9;
}
.product-rating{
    color: #ffc107;
}
.product-rating span{
    font-weight: 600;
    color: #252525;
}
.product-price{
    margin: 1rem 0;
    font-size: 1rem;
    font-weight: 700;
}
.product-price span{
    font-weight: 400;
}
.last-price span{
    color: #f64749;
    text-decoration: line-through;
}
.new-price span{
    color: #256eff;
}
.product-detail h2{
    text-transform: capitalize;
    color: #12263a;
    padding-bottom: 0.6rem;
}
.product-detail p{
    font-size: 0.9rem;
    padding: 0.3rem;
    opacity: 0.8;
}
.product-detail ul{
    margin: 1rem 0;
    font-size: 0.9rem;
}
.product-detail ul li{
    margin: 0;
    list-style: none;
    background: url(https://fadzrinmadu.github.io/hosted-assets/product-detail-page-design-with-image-slider-html-css-and-javascript/checked.png) left center no-repeat;
    background-size: 18px;
    padding-left: 1.7rem;
    margin: 0.4rem 0;
    font-weight: 600;
    opacity: 0.9;
}
.product-detail ul li span{
    font-weight: 400;
}
.purchase-info{
    margin: 1.5rem 0;
}
.purchase-info input,
.purchase-info .btn{
    border: 1.5px solid #ddd;
    border-radius: 25px;
    text-align: center;
    padding: 0.45rem 0.8rem;
    outline: 0;
    margin-right: 0.2rem;
    margin-bottom: 1rem;
}
.purchase-info input{
    width: 60px;
}
.purchase-info .btn{
    cursor: pointer;
    color: #fff;
}
.purchase-info .btn:first-of-type{
    background: #256eff;
}
.purchase-info .btn:last-of-type{
    background: #f64749;
}
.purchase-info .btn:hover{
    opacity: 0.9;
}
.social-links{
    display: flex;
    align-items: center;
}
.social-links a{
    display: flex;
    align-items: center;
    justify-content: center;
    width: 32px;
    height: 32px;
    color: #000;
    border: 1px solid #000;
    margin: 0 0.2rem;
    border-radius: 50%;
    text-decoration: none;
    font-size: 0.8rem;
    transition: all 0.5s ease;
}
.social-links a:hover{
    background: #000;
    border-color: transparent;
    color: #fff;
}

@media screen and (min-width: 992px){
    .card{
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-gap: 1.5rem;
    }
    .card-wrapper{
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .product-imgs{
        display: flex;
        flex-direction: column;
        justify-content: center;
    }
    .product-content{
        padding-top: 0;
    }
}
</style>
