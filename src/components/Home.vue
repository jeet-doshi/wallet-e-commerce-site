<template>
<div class="header">
    <div class="container">
    <div class="navbar">
        <div class="logo">
            <!-- <img src="" width="125px">   -->
        </div>
        <nav>
            <ul>
                <li><a href="">Home</a></li>
                <li><a href="">Products</a></li>
                <li><a href="">About</a></li>
                <li><a href="">Contact</a></li>
                <li><a href="">Account</a></li>
            </ul>
        </nav>
        <!-- <img src="/Images/Hornbull-Benial/Black" width="40px" height="40px"> -->
    </div>
    <div class="row">
        <div class="col-2">
            <h1>Shoe Wonder</h1>
            <p>Give your workout a new style</p>
            <a href="" class="btn">Explore Now </a>
        </div>
        <div class="col-2">
            <!-- <img src="IMAGES/Images1/shoe.jpg"> -->
        </div>
    </div>
    </div>
</div>

</template>

<style scoped>
*
{
    margin: 0px;
    padding: 0px;
    box-sizing: border-box;
}
body{
    font-family: 'Libre Baskerville', serif;
}
.navbar{
    display: flex;
    align-items: center;
    padding: 20px;
}
nav{
    flex: 1;
    text-align: right;
}
nav ul{
    display: inline-block;
    list-style-type: none;
}
nav ul li{
    display: inline-block;
    margin-right: 20px;
}
a{
    text-decoration: none;
    color: #555;
    font-size: large;
}
p{
    color: #555;
}
.container{
    max-width: 1300px;
    margin: auto;
    padding-left: 25px;
    padding-right: 25px;
}
.row{
    display: flex;
    align-items: center;
    flex-wrap: wrap;
    justify-content: space-around;
}
.col-2{
    flex-basis: 50%;
    min-width: 300px;
}
.col-2 img{
    max-width: 100%;
    padding: 50px 0;
}
.col-2 h1{
    font-size: 40px;
    line-height: 60px;
    margin: 25px 0;
}
.col-2 img{
    max-width: 100%;
    padding: 20pxpx;
}
.btn{
    display: inline-block;
    background: #FF523B;
    color: #fff;
    padding: 8px 30px;
    margin: 30px 0;
    border-radius: 30px;
    transition: background 0.5s;
}
.btn:hover{
    background: #563434;
}
.header{
    background: radial-gradient(#fff,#FFD6D6);
}
.header .row{
    margin-top: 115px;
}

</style>
