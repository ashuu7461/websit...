# websit...
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>ABJ Local Shop</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family:'Poppins',sans-serif;
    }

    body{
      background:#f8f8f8;
      color:#222;
      overflow-x:hidden;
    }

    html{
      scroll-behavior:smooth;
    }

    /* HERO */
    .hero{
      height:100vh;
      width:100%;
      background:url('https://share.google/UI4sCuwIv6VU8nU3K') center/cover no-repeat;
      position:relative;
      display:flex;
      align-items:center;
      justify-content:center;
      text-align:center;
      color:white;
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
      padding:20px;
    }

    .hero h1{
      font-size:3rem;
      margin-bottom:15px;
      font-weight:700;
    }

    .hero p{
      font-size:1.2rem;
      margin-bottom:25px;
    }

    .btn{
      display:inline-block;
      padding:14px 30px;
      background:#ff9800;
      color:white;
      text-decoration:none;
      border-radius:50px;
      font-weight:600;
      transition:0.3s;
    }

    .btn:hover{
      background:#e68900;
      transform:translateY(-2px);
    }

    /* SECTION */
    section{
      padding:60px 20px;
    }

    .section-title{
      text-align:center;
      font-size:2rem;
      margin-bottom:35px;
      font-weight:700;
    }

    /* PRODUCT CAROUSEL */
    .carousel{
      display:flex;
      gap:20px;
      overflow-x:auto;
      scroll-snap-type:x mandatory;
      padding-bottom:10px;
    }

    .carousel::-webkit-scrollbar{
      height:8px;
    }

    .carousel::-webkit-scrollbar-thumb{
      background:#ccc;
      border-radius:10px;
    }

    .product-card{
      min-width:280px;
      max-width:280px;
      background:white;
      border-radius:20px;
      overflow:hidden;
      box-shadow:0 5px 15px rgba(0,0,0,0.08);
      scroll-snap-align:start;
      transition:0.3s;
    }

    .product-card:hover{
      transform:translateY(-5px);
    }

    .product-card img{
      width:100%;
      height:220px;
      object-fit:cover;
    }

    .product-info{
      padding:18px;
    }

    .product-info h3{
      font-size:1.2rem;
      margin-bottom:10px;
    }

    .product-info p{
      font-size:0.95rem;
      color:#666;
      margin-bottom:15px;
    }

    .product-info button{
      width:100%;
      padding:12px;
      border:none;
      background:#111;
      color:white;
      border-radius:10px;
      cursor:pointer;
      font-weight:600;
    }

    .product-info button:hover{
      background:#ff9800;
    }

    /* CART FORM */
    .order-section{
      background:white;
      border-radius:20px;
      padding:30px;
      max-width:700px;
      margin:auto;
      box-shadow:0 5px 15px rgba(0,0,0,0.08);
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
      outline:none;
      font-size:1rem;
    }

    .cart-items{
      margin:20px 0;
      background:#f3f3f3;
      padding:15px;
      border-radius:12px;
    }

    .cart-items ul{
      padding-left:20px;
    }

    .submit-btn{
      width:100%;
      padding:15px;
      border:none;
      background:#ff9800;
      color:white;
      font-size:1rem;
      border-radius:12px;
      cursor:pointer;
      font-weight:600;
    }

    .submit-btn:hover{
      background:#e68900;
    }

    /* FOOTER */
    footer{
      text-align:center;
      padding:25px;
      background:#111;
      color:white;
      margin-top:40px;
    }

    /* WHATSAPP */
    .whatsapp-btn{
      position:fixed;
      right:20px;
      bottom:20px;
      width:60px;
      height:60px;
      background:#25D366;
      border-radius:50%;
      display:flex;
      align-items:center;
      justify-content:center;
      text-decoration:none;
      color:white;
      font-size:30px;
      box-shadow:0 5px 15px rgba(0,0,0,0.3);
      z-index:999;
    }

    @media(max-width:768px){
      .hero h1{
        font-size:2.2rem;
      }

      .hero p{
        font-size:1rem;
      }
    }
  </style>
</head>

<body>

  <!-- HERO -->
  <section class="hero">
    <div class="hero-content">
      <h1>ABJ Local Shop</h1>
      <p>Fresh Finds, Best Prices</p>

      <a href="#products" class="btn">
        Shop Now
      </a>
    </div>
  </section>

  <!-- PRODUCTS -->
  <section id="products">
    <h2 class="section-title">Our Products</h2>

    <div class="carousel">

      <div class="product-card">
        <img src="https://i.ibb.co/VWFmZDtc/IMG-20260508-WA0018.jpg" alt="Product">

        <div class="product-info">
          <h3>Premium Product</h3>

          <p>
            High-quality local product with affordable pricing and excellent freshness.
          </p>

          <button onclick="addToCart('Premium Product')">
            Add To Cart
          </button>
        </div>
      </div>

      <div class="product-card">
        <img src="https://i.ibb.co/VWFmZDtc/IMG-20260508-WA0018.jpg" alt="Product">

        <div class="product-info">
          <h3>Daily Essentials</h3>

          <p>
            Best quality grocery essentials for your everyday needs.
          </p>

          <button onclick="addToCart('Daily Essentials')">
            Add To Cart
          </button>
        </div>
      </div>

      <div class="product-card">
        <img src="https://i.ibb.co/VWFmZDtc/IMG-20260508-WA0018.jpg" alt="Product">

        <div class="product-info">
          <h3>Fresh Collection</h3>

          <p>
            Carefully selected products with trusted quality and value.
          </p>

          <button onclick="addToCart('Fresh Collection')">
            Add To Cart
          </button>
        </div>
      </div>

    </div>
  </section>

  <!-- ORDER FORM -->
  <section>
    <h2 class="section-title">Place Your Order</h2>

    <div class="order-section">

      <form id="orderForm">

        <div class="form-group">
          <label>Customer Name</label>

          <input 
            type="text" 
            id="customerName"
            placeholder="Enter your name"
            required
          />
        </div>

        <div class="form-group">
          <label>Phone Number</label>

          <input 
            type="tel" 
            id="customerPhone"
            placeholder="Enter phone number"
            required
          />
        </div>

        <div class="cart-items">
          <h3>Cart Items</h3>

          <ul id="cartList">
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
    <p>© 2026 ABJ Local Shop | All Rights Reserved</p>
  </footer>

  <!-- WHATSAPP BUTTON -->
  <a 
    href="https://wa.me/8969242471"
    class="whatsapp-btn"
    target="_blank"
  >
    💬
  </a>

  <!-- EMAILJS -->
  <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>

  <script>
    // EMAILJS INIT
    emailjs.init("YOUR_PUBLIC_KEY");

    const cart = [];

    function addToCart(product){
      cart.push(product);

      updateCart();

      alert(product + " added to cart!");
    }

    function updateCart(){
      const cartList = document.getElementById("cartList");

      cartList.innerHTML = "";

      if(cart.length === 0){
        cartList.innerHTML = "<li>No items added</li>";
        return;
      }

      cart.forEach(item => {
        const li = document.createElement("li");
        li.textContent = item;
        cartList.appendChild(li);
      });
    }

    // FORM SUBMIT
    document
      .getElementById("orderForm")
      .addEventListener("submit", function(e){

      e.preventDefault();

      const customerName =
        document.getElementById("customerName").value;

      const customerPhone =
        document.getElementById("customerPhone").value;

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
      .then(function(response){

        alert("Order Sent Successfully!");

        document.getElementById("orderForm").reset();

        cart.length = 0;

        updateCart();

      }, function(error){

        alert("Failed to send order!");

      });

    });
  </script>

</body>
</html>