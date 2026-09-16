```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>The Local Shop | Fresh Finds, Best Prices</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, Helvetica, sans-serif;
    scroll-behavior:smooth;
}

body{
    background:#f7f8fa;
    color:#222;
}

/* ================= HEADER ================= */

header{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    z-index:1000;
    background:rgba(255,255,255,.94);
    backdrop-filter:blur(12px);
    box-shadow:0 2px 15px rgba(0,0,0,.08);
}

.navbar{
    max-width:1200px;
    margin:auto;
    padding:15px 20px;
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.logo{
    font-size:22px;
    font-weight:800;
    color:#111;
}

.logo span{
    color:#ff6b35;
}

nav a{
    text-decoration:none;
    color:#333;
    margin-left:20px;
    font-weight:600;
}

nav a:hover{
    color:#ff6b35;
}

@media(max-width:700px){
    nav a{
        display:none;
    }
}

/* ================= HERO ================= */

.hero{
    min-height:100vh;
    position:relative;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;

    background:
        linear-gradient(rgba(0,0,0,.48),rgba(0,0,0,.48)),
        url("https://i.ibb.co/Xr1vdhgf/golu.jpg");

    background-size:cover;
    background-position:center;
}

.hero-content{
    color:white;
    padding:30px;
    max-width:800px;
}

.hero-content small{
    font-size:17px;
    letter-spacing:2px;
    text-transform:uppercase;
}

.hero h1{
    font-size:clamp(42px,8vw,78px);
    margin:15px 0;
    font-weight:900;
}

.hero p{
    font-size:20px;
    margin-bottom:30px;
}

.btn{
    display:inline-block;
    padding:14px 28px;
    border:none;
    border-radius:30px;
    background:#ff6b35;
    color:white;
    font-size:16px;
    font-weight:bold;
    cursor:pointer;
    text-decoration:none;
    transition:.3s;
}

.btn:hover{
    transform:translateY(-3px);
    background:#ff5420;
    box-shadow:0 10px 25px rgba(255,107,53,.35);
}

/* ================= SECTIONS ================= */

section{
    padding:80px 20px;
}

.container{
    max-width:1200px;
    margin:auto;
}

.section-title{
    text-align:center;
    margin-bottom:35px;
}

.section-title h2{
    font-size:36px;
    margin-bottom:8px;
}

.section-title p{
    color:#777;
}

/* ================= PRODUCTS ================= */

.product-carousel{
    display:flex;
    gap:20px;
    overflow-x:auto;
    padding:10px 5px 25px;
    scroll-snap-type:x mandatory;
}

.product-carousel::-webkit-scrollbar{
    height:7px;
}

.product-carousel::-webkit-scrollbar-thumb{
    background:#ff6b35;
    border-radius:20px;
}

.product{
    min-width:250px;
    background:white;
    border-radius:18px;
    overflow:hidden;
    box-shadow:0 8px 25px rgba(0,0,0,.08);
    scroll-snap-align:start;
    transition:.3s;
}

.product:hover{
    transform:translateY(-7px);
}

.product img{
    width:100%;
    height:190px;
    object-fit:cover;
}

.product-info{
    padding:18px;
}

.product-info h3{
    margin-bottom:8px;
}

.product-info p{
    color:#777;
    font-size:14px;
    margin-bottom:12px;
}

.price{
    font-size:20px;
    font-weight:800;
    color:#ff6b35;
    margin-bottom:15px;
}

.add-btn{
    width:100%;
    padding:11px;
    border:none;
    border-radius:10px;
    background:#111;
    color:white;
    cursor:pointer;
    font-weight:bold;
}

.add-btn:hover{
    background:#ff6b35;
}

/* ================= CART ================= */

.cart-box{
    background:white;
    max-width:850px;
    margin:auto;
    border-radius:20px;
    padding:25px;
    box-shadow:0 8px 30px rgba(0,0,0,.08);
}

.cart-items{
    margin-bottom:20px;
}

.cart-item{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:14px 0;
    border-bottom:1px solid #eee;
    gap:15px;
}

.cart-item-name{
    font-weight:bold;
}

.quantity{
    display:flex;
    align-items:center;
    gap:8px;
}

.quantity button{
    width:28px;
    height:28px;
    border:none;
    border-radius:50%;
    cursor:pointer;
    background:#eee;
}

.remove{
    color:#e53935;
    cursor:pointer;
    border:none;
    background:none;
}

.total{
    text-align:right;
    font-size:22px;
    font-weight:800;
    margin:20px 0;
}

/* ================= FORM ================= */

.order-form{
    display:grid;
    gap:15px;
    margin-top:25px;
}

.order-form input,
.order-form textarea{
    width:100%;
    padding:14px;
    border:1px solid #ddd;
    border-radius:10px;
    outline:none;
    font-size:15px;
}

.order-form input:focus,
.order-form textarea:focus{
    border-color:#ff6b35;
}

textarea{
    min-height:100px;
    resize:vertical;
}

.empty{
    text-align:center;
    color:#888;
    padding:20px;
}

/* ================= SHOP INFO ================= */

.shop-info{
    background:#111;
    color:white;
}

.info-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:25px;
    text-align:center;
}

.info-card{
    padding:25px;
}

.info-card .icon{
    font-size:35px;
    margin-bottom:10px;
}

.info-card p{
    color:#ccc;
    margin-top:7px;
}

@media(max-width:700px){
    .info-grid{
        grid-template-columns:1fr;
    }

    section{
        padding:65px 15px;
    }

    .cart-item{
        flex-wrap:wrap;
    }
}

/* ================= WHATSAPP ================= */

.whatsapp{
    position:fixed;
    right:20px;
    bottom:20px;
    width:58px;
    height:58px;
    background:#25D366;
    color:white;
    border-radius:50%;
    display:flex;
    align-items:center;
    justify-content:center;
    text-decoration:none;
    font-size:29px;
    box-shadow:0 7px 25px rgba(0,0,0,.25);
    z-index:999;
    transition:.3s;
}

.whatsapp:hover{
    transform:scale(1.1);
}

/* ================= FOOTER ================= */

footer{
    background:#080808;
    color:#aaa;
    text-align:center;
    padding:25px;
    font-size:14px;
}
</style>
</head>

<body>

<!-- ================= HEADER ================= -->

<header>
    <div class="navbar">
        <div class="logo">
            The <span>Local Shop</span>
        </div>

        <nav>
            <a href="#home">Home</a>
            <a href="#products">Products</a>
            <a href="#cart">Cart</a>
            <a href="#contact">Contact</a>
        </nav>
    </div>
</header>


<!-- ================= HERO ================= -->

<section class="hero" id="home">

    <div class="hero-content">

        <small>Welcome to</small>

        <h1>The Local Shop</h1>

        <p>
            Fresh Finds, Best Prices
        </p>

        <a href="#products" class="btn">
            Shop Now →
        </a>

    </div>

</section>


<!-- ================= PRODUCTS ================= -->

<section id="products">

    <div class="container">

        <div class="section-title">
            <h2>Our Products</h2>
            <p>Fresh products at local-shop prices</p>
        </div>

        <div class="product-carousel">

            <!-- Product 1 -->

            <div class="product">

                <img src="https://images.unsplash.com/photo-1542838132-92c53300491e?auto=format&fit=crop&w=600&q=80">

                <div class="product-info">

                    <h3>Fresh Vegetables</h3>

                    <p>Fresh and locally sourced vegetables.</p>

                    <div class="price">₹80</div>

                    <button class="add-btn"
                    onclick="addToCart('Fresh Vegetables',80)">
                    Add to Cart
                    </button>

                </div>

            </div>


            <!-- Product 2 -->

            <div class="product">

                <img src="https://images.unsplash.com/photo-1574226516831-e1dff420e37f?auto=format&fit=crop&w=600&q=80">

                <div class="product-info">

                    <h3>Fresh Fruits</h3>

                    <p>Healthy and delicious seasonal fruits.</p>

                    <div class="price">₹120</div>

                    <button class="add-btn"
                    onclick="addToCart('Fresh Fruits',120)">
                    Add to Cart
                    </button>

                </div>

            </div>


            <!-- Product 3 -->

            <div class="product">

                <img src="https://images.unsplash.com/photo-1608198093002-ad4e005484ec?auto=format&fit=crop&w=600&q=80">

                <div class="product-info">

                    <h3>Fresh Bread</h3>

                    <p>Soft and freshly baked bread.</p>

                    <div class="price">₹50</div>

                    <button class="add-btn"
                    onclick="addToCart('Fresh Bread',50)">
                    Add to Cart
                    </button>

                </div>

            </div>


            <!-- Product 4 -->

            <div class="product">

                <img src="https://images.unsplash.com/photo-1547592180-85f173990554?auto=format&fit=crop&w=600&q=80">

                <div class="product-info">

                    <h3>Grocery Pack</h3>

                    <p>Daily-use grocery essentials.</p>

                    <div class="price">₹250</div>

                    <button class="add-btn"
                    onclick="addToCart('Grocery Pack',250)">
                    Add to Cart
                    </button>

                </div>

            </div>


            <!-- Product 5 -->

            <div class="product">

                <img src="https://images.unsplash.com/photo-1550583724-b2692b85b150?auto=format&fit=crop&w=600&q=80">

                <div class="product-info">

                    <h3>Milk</h3>

                    <p>Fresh everyday milk.</p>

                    <div class="price">₹60</div>

                    <button class="add-btn"
                    onclick="addToCart('Milk',60)">
                    Add to Cart
                    </button>

                </div>

            </div>

        </div>

    </div>

</section>


<!-- ================= CART ================= -->

<section id="cart">

    <div class="container">

        <div class="section-title">
            <h2>Your Cart</h2>
            <p>Review your items before placing your order</p>
        </div>

        <div class="cart-box">

            <div id="cartItems" class="cart-items">

                <div class="empty">
                    Your cart is empty.
                </div>

            </div>

            <div class="total">
                Total: ₹<span id="total">0</span>
            </div>


            <!-- ORDER FORM -->

            <h3>Customer Details</h3>

            <form class="order-form" id="orderForm">

                <input
                    type="text"
                    id="customerName"
                    placeholder="Your Full Name"
                    required
                >

                <input
                    type="tel"
                    id="phone"
                    placeholder="Phone Number"
                    required
                >

                <input
                    type="email"
                    id="email"
                    placeholder="Your Email (optional)"
                >

                <textarea
                    id="address"
                    placeholder="Delivery Address / Additional Note"
                ></textarea>

                <button type="submit" class="btn">
                    Place Order via Email
                </button>

            </form>

        </div>

    </div>

</section>


<!-- ================= SHOP INFORMATION ================= -->

<section class="shop-info" id="contact">

    <div class="container">

        <div class="section-title">

            <h2 style="color:white;">
                Visit The Local Shop
            </h2>

            <p>
                Fresh Finds • Best Prices • Local Service
            </p>

        </div>


        <div class="info-grid">

            <div class="info-card">

                <div class="icon">🏪</div>

                <h3>The Local Shop</h3>

                <p>
                    Your trusted local store
                </p>

            </div>


            <div class="info-card">

                <div class="icon">📧</div>

                <h3>Email</h3>

                <p>
                    divyansh9279496343@gmail.com
                </p>

            </div>


            <div class="info-card">

                <div class="icon">📱</div>

                <h3>WhatsApp</h3>

                <p>
                    9279496243
                </p>

            </div>

        </div>

    </div>

</section>


<!-- ================= FOOTER ================= -->

<footer>

    © 2026 The Local Shop.
    All Rights Reserved.

</footer>


<!-- ================= WHATSAPP ================= -->

<a
    class="whatsapp"
    href="https://wa.me/919279496243"
    target="_blank"
    aria-label="Chat on WhatsApp"
>
    ☎
</a>


<script>

/* ==========================================
   SHOP CART
========================================== */

let cart = [];


/* ADD PRODUCT */

function addToCart(name, price){

    const existing = cart.find(item => item.name === name);

    if(existing){

        existing.quantity++;

    }else{

        cart.push({
            name:name,
            price:price,
            quantity:1
        });

    }

    updateCart();

    document
        .getElementById("cart")
        .scrollIntoView({
            behavior:"smooth"
        });
}


/* UPDATE CART */

function updateCart(){

    const cartItems =
        document.getElementById("cartItems");

    const totalElement =
        document.getElementById("total");

    if(cart.length === 0){

        cartItems.innerHTML =
        `<div class="empty">
            Your cart is empty.
        </div>`;

        totalElement.innerText = "0";

        return;
    }


    let total = 0;

    cartItems.innerHTML = "";


    cart.forEach((item,index)=>{

        total += item.price * item.quantity;


        const div =
        document.createElement("div");

        div.className = "cart-item";


        div.innerHTML = `

            <div>

                <div class="cart-item-name">
                    ${item.name}
                </div>

                <small>
                    ₹${item.price} each
                </small>

            </div>


            <div class="quantity">

                <button
                onclick="changeQuantity(${index},-1)">
                −
                </button>

                <strong>
                    ${item.quantity}
                </strong>

                <button
                onclick="changeQuantity(${index},1)">
                +
                </button>

            </div>


            <strong>
                ₹${item.price * item.quantity}
            </strong>


            <button
            class="remove"
            onclick="removeItem(${index})">
                Remove
            </button>

        `;


        cartItems.appendChild(div);

    });


    totalElement.innerText = total;

}


/* CHANGE QUANTITY */

function changeQuantity(index, amount){

    cart[index].quantity += amount;


    if(cart[index].quantity <= 0){

        cart.splice(index,1);

    }


    updateCart();

}


/* REMOVE ITEM */

function removeItem(index){

    cart.splice(index,1);

    updateCart();

}


/* ==========================================
   PLACE ORDER
========================================== */

document
.getElementById("orderForm")
.addEventListener("submit",function(event){

    event.preventDefault();


    if(cart.length === 0){

        alert("Please add at least one product to your cart.");

        return;

    }


    const customerName =
        document.getElementById("customerName").value.trim();


    const phone =
        document.getElementById("phone").value.trim();


    const email =
        document.getElementById("email").value.trim();


    const address =
        document.getElementById("address").value.trim();


    let itemList = "";

    let total = 0;


    cart.forEach(item => {

        const itemTotal =
            item.price * item.quantity;

        total += itemTotal;


        itemList +=
        `${item.name} x ${item.quantity} = ₹${itemTotal}\n`;

    });


    const subject =
        `New Order - The Local Shop - ${customerName}`;


    const body =

`Hello The Local Shop,

I would like to place an order.

CUSTOMER DETAILS
----------------
Name: ${customerName}
Phone: ${phone}
Email: ${email || "Not provided"}

ORDER ITEMS
-----------
${itemList}

TOTAL: ₹${total}

DELIVERY ADDRESS / NOTE
-----------------------
${address || "Not provided"}

Thank you.
`;


    const mailto =
        `mailto:divyansh9279496343@gmail.com`
        + `?subject=${encodeURIComponent(subject)}`
        + `&body=${encodeURIComponent(body)}`;


    window.location.href = mailto;

});


/* ==========================================
   AUTO-SCROLL PRODUCT CAROUSEL
========================================== */

const carousel =
    document.querySelector(".product-carousel");


let autoScroll;


function startAutoScroll(){

    autoScroll =
    setInterval(()=>{

        if(
            carousel.scrollLeft +
            carousel.clientWidth >=
            carousel.scrollWidth - 10
        ){

            carousel.scrollTo({
                left:0,
                behavior:"smooth"
            });

        }else{

            carousel.scrollBy({
                left:270,
                behavior:"smooth"
            });

        }

    },3000);

}


function stopAutoScroll(){

    clearInterval(autoScroll);

}


carousel.addEventListener(
    "mouseenter",
    stopAutoScroll
);

carousel.addEventListener(
    "mouseleave",
    startAutoScroll
);


carousel.addEventListener(
    "touchstart",
    stopAutoScroll
);


carousel.addEventListener(
    "touchend",
    startAutoScroll
);


startAutoScroll();

</script>

</body>
</html>
```
