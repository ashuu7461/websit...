

    

    <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>ABJ Local Shop</title>

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <!-- Font Awesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css"/>

  <style>

    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family:'Poppins',sans-serif;
    }

    body{
      background:#f7f7f7;
      color:#222;
      overflow-x:hidden;
    }

    html{
      scroll-behavior:smooth;
    }

    /* HERO */

    .hero{
      width:100%;
      height:100vh;
      background:url('https://share.google/UI4sCuwIv6VU8nU3K') center/cover no-repeat;
      position:relative;
      display:flex;
      align-items:center;
      justify-content:center;
      text-align:center;
      padding:20px;
    }

    .hero::before{
      content:'';
      position:absolute;
      inset:0;
      background:rgba(0,0,0,0.55);
    }

    .hero-content{
      position:relative;
      z-index:2;
      color:#fff;
      max-width:700px;
    }

    .hero-content h1{
      font-size:60px;
      margin-bottom:15px;
      font-weight:700;
    }

    .hero-content p{
      font-size:20px;
      margin-bottom:30px;
    }

    .hero-btn{
      display:inline-block;
      padding:15px 35px;
      background:#ff9800;
      color:#fff;
      border-radius:50px;
      text-decoration:none;
      font-weight:600;
      transition:0.3s;
    }

    .hero-btn:hover{
      background:#ff7b00;
      transform:translateY(-3px);
    }

    /* SECTION */

    section{
      padding:70px 20px;
    }

    .section-title{
      text-align:center;
      font-size:38px;
      margin-bottom:40px;
      font-weight:700;
    }

    /* PRODUCT CAROUSEL */

    .carousel-container{
      overflow:hidden;
      position:relative;
    }

    .carousel{
      display:flex;
      gap:20px;
      overflow-x:auto;
      scroll-behavior:smooth;
      padding-bottom:10px;
    }

    .carousel::-webkit-scrollbar{
      display:none;
    }

    .product-card{
      min-width:300px;
      background:#fff;
      border-radius:20px;
      overflow:hidden;
      box-shadow:0 5px 20px rgba(0,0,0,0.08);
      transition:0.3s;
      flex-shrink:0;
    }

    .product-card:hover{
      transform:translateY(-5px);
    }

    .product-card img{
      width:100%;
      height:240px;
      object-fit:cover;
    }

    .product-content{
      padding:20px;
    }

    .product-content h3{
      font-size:22px;
      margin-bottom:10px;
    }

    .product-content p{
      font-size:15px;
      color:#666;
      margin-bottom:20px;
      line-height:1.6;
    }

    .product-content button{
      width:100%;
      padding:14px;
      border:none;
      background:#111;
      color:#fff;
      border-radius:12px;
      font-size:16px;
      font-weight:600;
      cursor:pointer;
      transition:0.3s;
    }

    .product-content button:hover{
      background:#ff9800;
    }

    /* ORDER FORM */

    .order-wrapper{
      max-width:700px;
      margin:auto;
      background:#fff;
      padding:35px;
      border-radius:20px;
      box-shadow:0 5px 20px rgba(0,0,0,0.08);
    }

    .form-group{
      margin-bottom:20px;
    }

    .form-group label{
      display:block;
      margin-bottom:8px;
      font-weight:600;
    }

    .form-group input,
    .form-group textarea{
      width:100%;
      padding:14px;
      border:1px solid #ddd;
      border-radius:12px;
      font-size:15px;
      outline:none;
    }

    .cart-box{
      background:#f3f3f3;
      padding:20px;
      border-radius:15px;
      margin-bottom:20px;
    }

    .cart-box h4{
      margin-bottom:10px;
    }

    #cartItems li{
      margin-bottom:8px;
    }

    .submit-btn{
      width:100%;
      padding:16px;
      border:none;
      background:#ff9800;
      color:#fff;
      font-size:17px;
      border-radius:12px;
      cursor:pointer;
      font-weight:600;
      transition:0.3s;
    }

    .submit-btn:hover{
      background:#ff7b00;
    }

    /* FOOTER */

    footer{
      background:#111;
      color:#fff;
      text-align:center;
      padding:25px;
      margin-top:40px;
    }

    /* WHATSAPP BUTTON */

    .whatsapp-btn{
      position:fixed;
      right:20px;
      bottom:20px;
      width:60px;
      height:60px;
      background:#25D366;
      color:#fff;
      border-radius:50%;
      display:flex;
      align-items:center;
      justify-content:center;
      font-size:28px;
      text-decoration:none;
      box-shadow:0 5px 15px rgba(0,0,0,0.3);
      z-index:999;
    }

    @media(max-width:768px){

      .hero-content h1{
        font-size:42px;
      }

      .hero-content p{
        font-size:17px;
      }

      .section-title{
        font-size:30px;
      }

      .product-card{
        min-width:85%;
      }

    }

  </style>
</head>

<body>

  <!-- HERO SECTION -->

  <section class="hero">

    <div class="hero-content">

      <h1>ABJ Local Shop</h1>

      <p>Fresh Finds, Best Prices</p>

      <a href="#products" class="hero-btn">
        Shop Now
      </a>

    </div>

  </section>

  <!-- PRODUCTS -->

  <section id="products">

    <h2 class="section-title">
      Our Products
    </h2>

    <div class="carousel-container">

      <div class="carousel" id="carousel">

        <!-- PRODUCT 1 -->

        <div class="product-card">

          <img src="https://i.ibb.co/VWFmZDtc/IMG-20260508-WA0018.jpg" alt="Product">

          <div class="product-content">

            <h3>Fresh Grocery Pack</h3>

            <p>
              Premium quality grocery items with best pricing and trusted freshness.
            </p>

            <button onclick="addToCart('Fresh Grocery Pack')">
              Add To Cart
            </button>

          </div>

        </div>

        <!-- PRODUCT 2 -->

        <div class="product-card">

          <img src="https://i.ibb.co/VWFmZDtc/IMG-20260508-WA0018.jpg" alt="Product">

          <div class="product-content">

            <h3>Daily Essentials</h3>

            <p>
              Everyday local shop products available at affordable rates.
            </p>

            <button onclick="addToCart('Daily Essentials')">
              Add To Cart
            </button>

          </div>

        </div>

        <!-- PRODUCT 3 -->

        <div class="product-card">

          <img src="https://i.ibb.co/VWFmZDtc/IMG-20260508-WA0018.jpg" alt="Product">

          <div class="product-content">

            <h3>Special Combo</h3>

            <p>
              High-quality combo products carefully selected for customers.
            </p>

            <button onclick="addToCart('Special Combo')">
              Add To Cart
            </button>

          </div>

        </div>

      </div>

    </div>

  </section>

  <!-- ORDER FORM -->

  <section>

    <h2 class="section-title">
      Place Your Order
    </h2>

    <div class="order-wrapper">

      <form id="orderForm">

        <div class="form-group">

          <label>Customer Name</label>

          <input 
            type="text"
            id="customerName"
            placeholder="Enter your name"
            required
          >

        </div>

        <div class="form-group">

          <label>Phone Number</label>

          <input 
            type="tel"
            id="customerPhone"
            placeholder="Enter your phone number"
            required
          >

        </div>

        <div class="cart-box">

          <h4>Cart Items</h4>

          <ul id="cartItems">

            <li>No items added</li>

          </ul>

        </div>

        <button type="submit" class="submit-btn">
          Send Order
        </button>

      </form>

    </div>

  </section>

  <!-- FOOTER -->

  <footer>

    <p>
      © 2026 ABJ Local Shop | All Rights Reserved
    </p>

  </footer>

  <!-- WHATSAPP -->

  <a 
    href="https://wa.me/918969242471"
    class="whatsapp-btn"
    target="_blank"
  >
    <i class="fa-brands fa-whatsapp"></i>
  </a>

  <!-- EMAILJS -->

  <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>

  <script>

    // EMAILJS INIT
    // Replace with your EmailJS Public Key

    emailjs.init("YOUR_PUBLIC_KEY");

    // CART

    let cart = [];

    function addToCart(product){

      cart.push(product);

      updateCart();

      alert(product + " added to cart!");

    }

    function updateCart(){

      const cartItems = document.getElementById("cartItems");

      cartItems.innerHTML = "";

      if(cart.length === 0){

        cartItems.innerHTML = "<li>No items added</li>";

        return;

      }

      cart.forEach(item => {

        let li = document.createElement("li");

        li.textContent = item;

        cartItems.appendChild(li);

      });

    }

    // AUTO SLIDE

    const carousel = document.getElementById("carousel");

    let scrollAmount = 0;

    setInterval(() => {

      if(scrollAmount >= carousel.scrollWidth - carousel.clientWidth){

        scrollAmount = 0;

      } else {

        scrollAmount += 320;

      }

      carousel.scrollTo({
        left: scrollAmount,
        behavior: "smooth"
      });

    }, 3000);

    // SEND ORDER

    document
      .getElementById("orderForm")
      .addEventListener("submit", function(e){

      e.preventDefault();

      const customerName =
        document.getElementById("customerName").value;

      const customerPhone =
        document.getElementById("customerPhone").value;

      if(cart.length === 0){

        alert("Please add products to cart!");

        return;

      }

      const templateParams = {

        customer_name: customerName,

        customer_phone: customerPhone,

        order_items: cart.join(", "),

        owner_email: "ashuu7461@gmail.com"

      };

      emailjs.send(
        "YOUR_SERVICE_ID",
        "YOUR_TEMPLATE_ID",
        templateParams
      )

      .then(function(){

        alert("Order Sent Successfully!");

        document.getElementById("orderForm").reset();

        cart = [];

        updateCart();

      })

      .catch(function(error){

        alert("Failed To Send Order!");

        console.log(error);

      });

    });

  </script>

</body>
</html>