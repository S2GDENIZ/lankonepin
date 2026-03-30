<!DOCTYPE html>
<html lang="az">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LANKONEPIN - PUBG Mobile UC Satış</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&display=swap" rel="stylesheet">
<style>
* { margin:0; padding:0; box-sizing:border-box; }
body {
  font-family: 'Orbitron', sans-serif;
  background: radial-gradient(circle at top, #0a0015, #1a0a2e);
  color: #fff;
  min-height:100vh;
}
header {
  display:flex;
  align-items:center;
  justify-content:center;
  gap:15px;
  padding:20px;
  background:linear-gradient(90deg,#000000,#ffffff);
  box-shadow:0 0 15px #ff0241;
  position:relative;
}
header img { width:70px; }
header h1 { font-size:2rem; text-transform:uppercase; letter-spacing:2px; }
#cart {
  position:absolute;
  right:20px;
  font-size:18px;
  cursor:pointer;
  background:#e7000c;
  color:#fff;
  padding:5px 10px;
  border-radius:6px;
}

/* Cards */
.container { padding:40px 20px; display:flex; flex-wrap:wrap; gap:30px; justify-content:center; }
.card { width:280px; background:#111; border:2px solid #e7000c; border-radius:15px; text-align:center; padding:20px; transition:0.3s; }
.card:hover { transform:translateY(-8px); box-shadow:0 0 15px #e90316; }
.card img { width:100%; border-radius:10px; margin-bottom:12px; }
.card h2 { font-size:1.3rem; margin-bottom:8px; color:#ff0c0c; }
.card p { font-size:1rem; margin-bottom:10px; color:#ff0707; }
.price { font-size:1.1rem; font-weight:bold; margin-bottom:12px; }
.card button { padding:11px 18px; background:#f80202; border:none; color:#000; font-weight:bold; cursor:pointer; border-radius:8px; transition:0.3s; }
.card button:hover { background:#fff; color:#ff4c4c; }

/* Footer */
footer { text-align:center; padding:15px; margin-top:40px; background:linear-gradient(90deg,#ffffff,#db0c0c); }

/* Səbət popup */
#cartPopup {
  display:none;
  position:fixed;
  top:60px;
  right:20px;
  width:320px;
  max-height:500px;
  background:#fff;
  color:#000;
  border-radius:10px;
  box-shadow:0 0 15px rgba(0,0,0,0.4);
  overflow-y:auto;
  z-index:100;
  padding:15px;
}
#cartPopup h3 { margin-bottom:10px; color:#e7000c; }
.cart-item { display:flex; justify-content:space-between; margin-bottom:10px; padding:5px; border-bottom:1px solid #ddd; }
#total { margin-top:10px; text-align:right; font-weight:bold; color:#e7000c; }
#checkoutBtn { display:block; width:100%; padding:10px; margin-top:10px; background:#e7000c; color:#fff; border:none; border-radius:6px; cursor:pointer; font-weight:bold; }
#checkoutBtn:hover { background:#ff4c4c; }
</style>
</head>
<body>

<header>
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h1>LANKONEPIN</h1>
  <div id="cart">🛒 0</div>
</header>

<div id="cartPopup">
  <h3>Səbətiniz</h3>
  <div id="cartItems"></div>
  <div id="total">Ümumi: 0 AZN</div>
  <button id="checkoutBtn">Ödənişə davam et</button>
</div>

<div class="container">
<!-- Bütün paketlər 60-dan 16000 UC-a -->
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>60 UC</h2><p>Kiçik paket</p><div class="price">1.87</div>
  <button onclick="addToCart('60 UC',1.87)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>325 UC</h2><p>Orta paket</p><div class="price">8.20</div>
  <button onclick="addToCart('325 UC',8.20)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>660 UC</h2><p>Böyük paket</p><div class="price">16.11</div>
  <button onclick="addToCart('660 UC',16.11)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>1800 UC</h2><p>Populyar paket</p><div class="price">41.20</div>
  <button onclick="addToCart('1800 UC',41.20)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>3850 UC</h2><p>Premium paket</p><div class="price">83.90</div>
  <button onclick="addToCart('3850 UC',83.90)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>8100 UC</h2><p>Ən böyük paket</p><div class="price">163.04</div>
  <button onclick="addToCart('8100 UC',163.04)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>16000 UC</h2><p>Ultra paket</p><div class="price">334.07</div>
  <button onclick="addToCart('16000 UC',334.07)">Satın Al</button>
</div>
</div>

<footer>© 2026 LANKONEPIN</footer>

<script>
let cart = [];
function addToCart(name, price) {
  cart.push({name, price});
  document.getElementById("cart").innerText = `🛒 ${cart.length}`;
  updateCartPopup();
}
function updateCartPopup() {
  let cartItemsDiv = document.getElementById("cartItems");
  cartItemsDiv.innerHTML = "";
  let total = 0;
  cart.forEach(item => {
    total += item.price;
    let div = document.createElement("div");
    div.className = "cart-item";
    div.innerHTML = `<span>${item.name}</span><span>${item.price.toFixed(2)} AZN</span>`;
    cartItemsDiv.appendChild(div);
  });
  document.getElementById("total").innerText = `Ümumi: ${total.toFixed(2)} AZN`;
}
document.getElementById("cart").addEventListener("click", ()=>{
  let popup = document.getElementById("cartPopup");
  popup.style.display = popup.style.display === "block" ? "none" : "block";
});
document.getElementById("checkoutBtn").addEventListener("click", ()=>{
  alert("Checkout düyməsi klikləndi! Ödəniş sistemi əlavə olunmalıdır.");
});
</script>
</body>
</html><!DOCTYPE html>
<html lang="az">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LANKONEPIN - PUBG Mobile UC Satış</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&display=swap" rel="stylesheet">
<style>
* { margin:0; padding:0; box-sizing:border-box; }
body {
  font-family: 'Orbitron', sans-serif;
  background: radial-gradient(circle at top, #0a0015, #1a0a2e);
  color: #fff;
  min-height:100vh;
}
header {
  display:flex;
  align-items:center;
  justify-content:center;
  gap:15px;
  padding:20px;
  background:linear-gradient(90deg,#000000,#ffffff);
  box-shadow:0 0 15px #ff0241;
  position:relative;
}
header img { width:70px; }
header h1 { font-size:2rem; text-transform:uppercase; letter-spacing:2px; }
#cart {
  position:absolute;
  right:20px;
  font-size:18px;
  cursor:pointer;
  background:#e7000c;
  color:#fff;
  padding:5px 10px;
  border-radius:6px;
}

/* Cards */
.container { padding:40px 20px; display:flex; flex-wrap:wrap; gap:30px; justify-content:center; }
.card { width:280px; background:#111; border:2px solid #e7000c; border-radius:15px; text-align:center; padding:20px; transition:0.3s; }
.card:hover { transform:translateY(-8px); box-shadow:0 0 15px #e90316; }
.card img { width:100%; border-radius:10px; margin-bottom:12px; }
.card h2 { font-size:1.3rem; margin-bottom:8px; color:#ff0c0c; }
.card p { font-size:1rem; margin-bottom:10px; color:#ff0707; }
.price { font-size:1.1rem; font-weight:bold; margin-bottom:12px; }
.card button { padding:11px 18px; background:#f80202; border:none; color:#000; font-weight:bold; cursor:pointer; border-radius:8px; transition:0.3s; }
.card button:hover { background:#fff; color:#ff4c4c; }

/* Footer */
footer { text-align:center; padding:15px; margin-top:40px; background:linear-gradient(90deg,#ffffff,#db0c0c); }

/* Səbət popup */
#cartPopup {
  display:none;
  position:fixed;
  top:60px;
  right:20px;
  width:320px;
  max-height:500px;
  background:#fff;
  color:#000;
  border-radius:10px;
  box-shadow:0 0 15px rgba(0,0,0,0.4);
  overflow-y:auto;
  z-index:100;
  padding:15px;
}
#cartPopup h3 { margin-bottom:10px; color:#e7000c; }
.cart-item { display:flex; justify-content:space-between; margin-bottom:10px; padding:5px; border-bottom:1px solid #ddd; }
#total { margin-top:10px; text-align:right; font-weight:bold; color:#e7000c; }
#checkoutBtn { display:block; width:100%; padding:10px; margin-top:10px; background:#e7000c; color:#fff; border:none; border-radius:6px; cursor:pointer; font-weight:bold; }
#checkoutBtn:hover { background:#ff4c4c; }
</style>
</head>
<body>

<header>
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h1>LANKONEPIN</h1>
  <div id="cart">🛒 0</div>
</header>

<div id="cartPopup">
  <h3>Səbətiniz</h3>
  <div id="cartItems"></div>
  <div id="total">Ümumi: 0 AZN</div>
  <button id="checkoutBtn">Ödənişə davam et</button>
</div>

<div class="container">
<!-- Bütün paketlər 60-dan 16000 UC-a -->
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>60 UC</h2><p>Kiçik paket</p><div class="price">1.87</div>
  <button onclick="addToCart('60 UC',1.87)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>325 UC</h2><p>Orta paket</p><div class="price">8.20</div>
  <button onclick="addToCart('325 UC',8.20)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>660 UC</h2><p>Böyük paket</p><div class="price">16.11</div>
  <button onclick="addToCart('660 UC',16.11)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>1800 UC</h2><p>Populyar paket</p><div class="price">41.20</div>
  <button onclick="addToCart('1800 UC',41.20)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>3850 UC</h2><p>Premium paket</p><div class="price">83.90</div>
  <button onclick="addToCart('3850 UC',83.90)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>8100 UC</h2><p>Ən böyük paket</p><div class="price">163.04</div>
  <button onclick="addToCart('8100 UC',163.04)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>16000 UC</h2><p>Ultra paket</p><div class="price">334.07</div>
  <button onclick="addToCart('16000 UC',334.07)">Satın Al</button>
</div>
</div>

<footer>© 2026 LANKONEPIN</footer>

<script>
let cart = [];
function addToCart(name, price) {
  cart.push({name, price});
  document.getElementById("cart").innerText = `🛒 ${cart.length}`;
  updateCartPopup();
}
function updateCartPopup() {
  let cartItemsDiv = document.getElementById("cartItems");
  cartItemsDiv.innerHTML = "";
  let total = 0;
  cart.forEach(item => {
    total += item.price;
    let div = document.createElement("div");
    div.className = "cart-item";
    div.innerHTML = `<span>${item.name}</span><span>${item.price.toFixed(2)} AZN</span>`;
    cartItemsDiv.appendChild(div);
  });
  document.getElementById("total").innerText = `Ümumi: ${total.toFixed(2)} AZN`;
}
document.getElementById("cart").addEventListener("click", ()=>{
  let popup = document.getElementById("cartPopup");
  popup.style.display = popup.style.display === "block" ? "none" : "block";
});
document.getElementById("checkoutBtn").addEventListener("click", ()=>{
  alert("Checkout düyməsi klikləndi! Ödəniş sistemi əlavə olunmalıdır.");
});
</script>
</body>
</html><!DOCTYPE html>
<html lang="az">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LANKONEPIN - PUBG Mobile UC Satış</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&display=swap" rel="stylesheet">
<style>
* { margin:0; padding:0; box-sizing:border-box; }
body {
  font-family: 'Orbitron', sans-serif;
  background: radial-gradient(circle at top, #0a0015, #1a0a2e);
  color: #fff;
  min-height:100vh;
}
header {
  display:flex;
  align-items:center;
  justify-content:center;
  gap:15px;
  padding:20px;
  background:linear-gradient(90deg,#000000,#ffffff);
  box-shadow:0 0 15px #ff0241;
  position:relative;
}
header img { width:70px; }
header h1 { font-size:2rem; text-transform:uppercase; letter-spacing:2px; }
#cart {
  position:absolute;
  right:20px;
  font-size:18px;
  cursor:pointer;
  background:#e7000c;
  color:#fff;
  padding:5px 10px;
  border-radius:6px;
}

/* Cards */
.container { padding:40px 20px; display:flex; flex-wrap:wrap; gap:30px; justify-content:center; }
.card { width:280px; background:#111; border:2px solid #e7000c; border-radius:15px; text-align:center; padding:20px; transition:0.3s; }
.card:hover { transform:translateY(-8px); box-shadow:0 0 15px #e90316; }
.card img { width:100%; border-radius:10px; margin-bottom:12px; }
.card h2 { font-size:1.3rem; margin-bottom:8px; color:#ff0c0c; }
.card p { font-size:1rem; margin-bottom:10px; color:#ff0707; }
.price { font-size:1.1rem; font-weight:bold; margin-bottom:12px; }
.card button { padding:11px 18px; background:#f80202; border:none; color:#000; font-weight:bold; cursor:pointer; border-radius:8px; transition:0.3s; }
.card button:hover { background:#fff; color:#ff4c4c; }

/* Footer */
footer { text-align:center; padding:15px; margin-top:40px; background:linear-gradient(90deg,#ffffff,#db0c0c); }

/* Səbət popup */
#cartPopup {
  display:none;
  position:fixed;
  top:60px;
  right:20px;
  width:320px;
  max-height:500px;
  background:#fff;
  color:#000;
  border-radius:10px;
  box-shadow:0 0 15px rgba(0,0,0,0.4);
  overflow-y:auto;
  z-index:100;
  padding:15px;
}
#cartPopup h3 { margin-bottom:10px; color:#e7000c; }
.cart-item { display:flex; justify-content:space-between; margin-bottom:10px; padding:5px; border-bottom:1px solid #ddd; }
#total { margin-top:10px; text-align:right; font-weight:bold; color:#e7000c; }
#checkoutBtn { display:block; width:100%; padding:10px; margin-top:10px; background:#e7000c; color:#fff; border:none; border-radius:6px; cursor:pointer; font-weight:bold; }
#checkoutBtn:hover { background:#ff4c4c; }
</style>
</head>
<body>

<header>
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h1>LANKONEPIN</h1>
  <div id="cart">🛒 0</div>
</header>

<div id="cartPopup">
  <h3>Səbətiniz</h3>
  <div id="cartItems"></div>
  <div id="total">Ümumi: 0 AZN</div>
  <button id="checkoutBtn">Ödənişə davam et</button>
</div>

<div class="container">
<!-- Bütün paketlər 60-dan 16000 UC-a -->
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>60 UC</h2><p>Kiçik paket</p><div class="price">1.87</div>
  <button onclick="addToCart('60 UC',1.87)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>325 UC</h2><p>Orta paket</p><div class="price">8.20</div>
  <button onclick="addToCart('325 UC',8.20)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>660 UC</h2><p>Böyük paket</p><div class="price">16.11</div>
  <button onclick="addToCart('660 UC',16.11)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>1800 UC</h2><p>Populyar paket</p><div class="price">41.20</div>
  <button onclick="addToCart('1800 UC',41.20)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>3850 UC</h2><p>Premium paket</p><div class="price">83.90</div>
  <button onclick="addToCart('3850 UC',83.90)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>8100 UC</h2><p>Ən böyük paket</p><div class="price">163.04</div>
  <button onclick="addToCart('8100 UC',163.04)">Satın Al</button>
</div>
<div class="card">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>16000 UC</h2><p>Ultra paket</p><div class="price">334.07</div>
  <button onclick="addToCart('16000 UC',334.07)">Satın Al</button>
</div>
</div>

<footer>© 2026 LANKONEPIN</footer>

<script>
let cart = [];
function addToCart(name, price) {
  cart.push({name, price});
  document.getElementById("cart").innerText = `🛒 ${cart.length}`;
  updateCartPopup();
}
function updateCartPopup() {
  let cartItemsDiv = document.getElementById("cartItems");
  cartItemsDiv.innerHTML = "";
  let total = 0;
  cart.forEach(item => {
    total += item.price;
    let div = document.createElement("div");
    div.className = "cart-item";
    div.innerHTML = `<span>${item.name}</span><span>${item.price.toFixed(2)} AZN</span>`;
    cartItemsDiv.appendChild(div);
  });
  document.getElementById("total").innerText = `Ümumi: ${total.toFixed(2)} AZN`;
}
document.getElementById("cart").addEventListener("click", ()=>{
  let popup = document.getElementById("cartPopup");
  popup.style.display = popup.style.display === "block" ? "none" : "block";
});
document.getElementById("checkoutBtn").addEventListener("click", ()=>{
  alert("Checkout düyməsi klikləndi! Ödəniş sistemi əlavə olunmalıdır.");
});
</script>
</body>
</html>
