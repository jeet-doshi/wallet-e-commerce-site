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
<div class="row">
    <div class="col-75">
        <div class="container">
            <form id="validate" action="/action_page.php">
                <div class="row">
                    <div class="col-50">
                        <h3>Billing Address</h3>
                        <label for="fname"><i class="fa fa-user"></i> Full Name</label>
                        <input type="text" id="fname" name="fullname" placeholder="name surname" required>
                        <label for="email"><i class="fa fa-envelope"></i> Email</label>
                        <input type="text" id="email" name="email" placeholder="name.surname@gmail.com" required>
                        <label for="adr"><i class="fa fa-address-card-o"></i> Address</label>
                        <input type="text" id="adr" name="address" placeholder="address" required>
                        <label for="city"><i class="fa fa-institution"></i> City</label>
                        <input type="text" id="city" name="city" placeholder="city" required>

                        <div class="row">
                            <div class="col-50">
                                <label for="state">State</label>
                                <input type="text" id="state" name="state" placeholder="state" required>
                            </div>
                            <div class="col-50">
                                <label for="zip">Zip</label>
                                <input type="text" id="zip" name="zip" placeholder="123456" required>
                            </div>
                        </div>
                    </div>

                    <div class="col-50">
                        <h3>Payment</h3>
                        <label for="fname">Accepted Cards</label>
                        <div class="icon-container">
                            <i class="fa fa-cc-visa" style="color:navy;"></i>
                            <i class="fa fa-cc-amex" style="color:blue;"></i>
                            <i class="fa fa-cc-mastercard" style="color:red;"></i>
                            <i class="fa fa-cc-discover" style="color:orange;"></i>
                        </div>

                        <label for="cname">Name on Card</label>
                        <input type="text" id="cname" name="cardname" placeholder="name surname" required>
                        <label for="ccnum">Credit card number</label>
                        <input type="text" id="ccnum" name="cardnumber" placeholder="1111-2222-3333-4444" required>
                        <label for="expmonth">Exp Month</label>
                        <input type="text" id="expmonth" name="expmonth" placeholder="month" required>
                        <div class="row">
                            <div class="col-50">
                                <label for="expyear">Exp Year</label>
                                <input type="text" id="expyear" name="expyear" placeholder="year" required>
                            </div>
                            <div class="col-50">
                                <label for="cvv">CVV</label>
                                <input type="text" id="cvv" name="cvv" placeholder="cvv" required>
                            </div>
                        </div>
                    </div>
                </div>
                <label>
                <input type="checkbox" checked="checked" name="sameadr"> Shipping address same as billing
                </label>
                <input type="submit" value="Continue to checkout" class="btn">
            </form>
        </div>
    </div>
    <div class="col-25">
        <div class="container">
            <h4>Cart <span class="price" style="color:black"><i class="fa fa-shopping-cart"></i> <b>4</b></span></h4>
            <p><a href="#">Hornbull</a> <span class="price">2500</span></p>
            <p><a href="#">Benial Men's wallet</a> <span class="price">3500</span></p>
            <p><a href="#">Billy Men's wallet with pen and keychain</a> <span class="price">4400</span></p>
            <p><a href="#">Buttler Men's wallet with pen and keychain/a> <span class="price">5200</span></p>
            <hr>
            <p>Total <span class="price" style="color:black"><b>15600</b></span></p>
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

<style>
.error {
    color: red;
    border-color: red;
}

.row {
    display: -ms-flexbox; /* IE10 */
    display: flex;
    -ms-flex-wrap: wrap; /* IE10 */
    flex-wrap: wrap;
    margin: 0 -10px;
}

.col-25 {
    -ms-flex: 25%; /* IE10 */
    flex: 25%;
}

.col-50 {
    -ms-flex: 50%; /* IE10 */
    flex: 50%;
}

.col-75 {
    -ms-flex: 75%; /* IE10 */
    flex: 75%;
}

.col-25,.col-50,.col-75 {
    padding: 0 16px;
}

.container {
    background-color: #FFFFFF;
    padding: 3px 18px 13px 18px;
    border: 1px solid lightgrey;
    border-radius: 3px;
    box-shadow: 0 0 2rem 0 rgba(168, 180, 194, 0.37);
}


input[type=text] {
    width: 100%;
    margin-bottom: 20px;
    padding: 12px;
    border: 1px solid rgb(130, 26, 26);
    border-radius: 1px;
}

label {
    margin-bottom: 10px;
    display: block;
}

.icon-container {
    margin-bottom: 20px;
    padding: 7px 0;
    font-size: 24px;
}

.btn {
    background-color: #01BAEF;
    color: white;
    padding: 12px;
    margin: 10px 0;
    border: none;
    width: 100%;
    border-radius: 3px;
    cursor: pointer;
    font-size: 17px;
    box-shadow: 0 0 1rem 0 rgba(99, 123, 150, 0.329);

}

.btn:hover {
    background-color: #0CBABA;
}

a {
    color: #2196F3;
}

hr {
    border: 1px solid lightgrey;
}

span.price {
    float: right;
    color: grey;
}

/* Responsive layout - when the screen is less than 800px wide, make the two columns 
    stack on top of each other instead of next to each other (also change the direction 
    - make the "cart" column go on top) 
*/
@media (max-width: 800px) {
    .row {
        flex-direction: column-reverse;
    }
    .col-25 {
        margin-bottom: 20px;
    }
}
</style>