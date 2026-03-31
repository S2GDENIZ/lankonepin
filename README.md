<!DOCTYPE html>
<html lang="az">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LANKONEPIN - PUBG Mobile UC Satış</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&display=swap" rel="stylesheet">
<style>
/* RESET & BODY */
* { margin:0; padding:0; box-sizing:border-box; }
body {
  font-family: 'Orbitron', sans-serif;
  min-height:100vh;
  overflow-x:hidden;
  color:#fff;
  background:#0a0015;
  position:relative;
}

/* ANIMATED NEON BACKGROUND */
#background {
  position:fixed;
  top:0; left:0; width:100%; height:100%; z-index:-1;
  overflow:hidden;
}
.neon-dot {
  position:absolute;
  width:6px; height:6px;
  border-radius:50%;
  background: linear-gradient(45deg,#ff0c0c,#ff4c4c,#e7000c);
  box-shadow: 0 0 10px #ff0c0c, 0 0 20px #ff4c4c, 0 0 30px #e7000c;
  animation: float 10s linear infinite;
}
@keyframes float {
  0% { transform: translateY(0) translateX(0); opacity:0; }
  50% { opacity:1; }
  100% { transform: translateY(-120vh) translateX(50vw); opacity:0; }
}

/* HEADER */
header {
  display:flex;
  align-items:center;
  justify-content:center;
  gap:15px;
  padding:20px;
  background: linear-gradient(90deg,#000,#111);
  box-shadow:0 0 20px #ff0241;
  position: relative;
  z-index:10;
  border-bottom:2px solid #e7000c;
}
header img { width:70px; border-radius:10px; transition:0.3s; }
header h1 { font-size:2rem; text-transform:uppercase; letter-spacing:2px; color:#ff0c0c; }
#cart {
  position:absolute;
  right:20px;
  font-size:18px;
  cursor:pointer;
  background:#e7000c;
  color:#fff;
  padding:5px 10px;
  border-radius:6px;
  transition:0.3s;
}
#cart:hover { background:#ff4c4c; }

/* MODERN CARD STYLE */
.container {
  padding:40px 20px;
  display:flex;
  flex-wrap:wrap;
  gap:30px;
  justify-content:center;
}
.card {
  width:280px;
  background: rgba(17,17,17,0.85);
  border:2px solid #e7000c;
  border-radius:20px;
  text-align:center;
  padding:20px;
  transition:0.4s;
  backdrop-filter: blur(5px);
}
.card:hover { 
  transform: translateY(-10px); 
  box-shadow:0 0 25px #e90316, 0 0 50px #ff0c0c70;
}
.card img { width:100%; border-radius:12px; margin-bottom:12px; transition:0.3s; }
.card img:hover { transform: scale(1.05); }
.card h2 { font-size:1.4rem; margin-bottom:8px; color:#ff0c0c; }
.card p { font-size:1rem; margin-bottom:10px; color:#ff0707; }
.price { font-size:1.2rem; font-weight:bold; margin-bottom:12px; }
.card button {
  padding:12px 20px;
  background:#f80202;
  border:none;
  color:#000;
  font-weight:bold;
  cursor:pointer;
  border-radius:10px;
  transition:0.3s;
}
.card button:hover { background:#fff; color:#ff4c4c; }

/* VIP EFFECT (16000 UC) */
.card.vip {
  border:3px solid gold;
  box-shadow:0 0 30px gold,0 0 60px gold;
}

/* FOOTER */
footer { text-align:center; padding:20px; margin-top:40px; background: linear-gradient(90deg,#111,#222); border-top:2px solid #e7000c; }

/* CART POPUP */
#cartPopup {
  display:none;
  position:fixed;
  top:70px;
  right:20px;
  width:320px;
  max-height:500px;
  background: rgba(255,255,255,0.95);
  color:#000;
  border-radius:15px;
  box-shadow:0 0 25px rgba(0,0,0,0.5);
  overflow-y:auto;
  z-index:100;
  padding:15px;
}
#cartPopup h3 { margin-bottom:10px; color:#e7000c; text-align:center; }
.cart-item { display:flex; justify-content:space-between; margin-bottom:10px; padding:5px; border-bottom:1px solid #ddd; align-items:center; }
.cart-item button { background:red; color:white; border:none; border-radius:5px; padding:3px 6px; cursor:pointer; transition:0.3s; }
.cart-item button:hover { background:#ff4c4c; }
#total { margin-top:10px; text-align:right; font-weight:bold; color:#e7000c; }
#checkoutBtn { display:block; width:100%; padding:12px; margin-top:10px; background:#e7000c; color:#fff; border:none; border-radius:8px; cursor:pointer; font-weight:bold; transition:0.3s; }
#checkoutBtn:hover { background:#ff4c4c; }
</style>
</head>
<body>

<div id="background"></div>

<header>
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s" alt="Logo">
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
<!-- Pakətlər -->
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
<div class="card vip">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
  <h2>16000 UC</h2><p>Ultra paket</p><div class="price">334.07</div>
  <button onclick="addToCart('16000 UC',334.07)">Satın Al</button>
</div>
</div>

<footer>© 2026 LANKONEPIN</footer>

<script>
// BACKGROUND NEON DOTS
for(let i=0;i<60;i++){
  let dot = document.createElement("div");
  dot.className="neon-dot";
  dot.style.left=Math.random()*100+"vw";
  dot.style.top=Math.random()*100+"vh";
  dot.style.animationDuration=(5+Math.random()*10)+"s";
  dot.style.width=(2+Math.random()*5)+"px";
  dot.style.height=(2+Math.random()*5)+"px";
  document.getElementById("background").appendChild(dot);
}

// CART SYSTEM
let cart = JSON.parse(localStorage.getItem("cart")) || [];
document.getElementById("cart").innerText = `🛒 ${cart.length}`;

function addToCart(name, price){
  cart.push({name, price});
  localStorage.setItem("cart", JSON.stringify(cart));
  document.getElementById("cart").innerText = `🛒 ${cart.length}`;
  updateCartPopup();
}

function removeItem(index){
  cart.splice(index,1);
  localStorage.setItem("cart", JSON.stringify(cart));
  document.getElementById("cart").innerText = `🛒 ${cart.length}`;
  updateCartPopup();
}

function updateCartPopup(){
  let cartItemsDiv = document.getElementById("cartItems");
  cartItemsDiv.innerHTML = "";
  let total = 0;

  cart.forEach((item,index)=>{
    total += item.price;
    let div = document.createElement("div");
    div.className = "cart-item";
    div.innerHTML = `
      <span>${item.name}</span>
      <span>${item.price.toFixed(2)} AZN</span>
      <button onclick="removeItem(${index})">X</button>
    `;
    cartItemsDiv.appendChild(div);
  });

  document.getElementById("total").innerText = `Ümumi: ${total.toFixed(2)} AZN`;
}

document.getElementById("cart").addEventListener("click", ()=>{
  let popup = document.getElementById("cartPopup");
  popup.style.display = popup.style.display === "block" ? "none" : "block";
});

document.getElementById("checkoutBtn").addEventListener("click", ()=>{
  if(cart.length===0){ alert("Səbət boşdur!"); return; }
  let text = "Salam, sifariş:\n";
  cart.forEach(item=>text+=`${item.name} - ${item.price.toFixed(2)} AZN\n`);
  let total = cart.reduce((sum,i)=>sum+i.price,0);
  text += `Toplam: ${total.toFixed(2)} AZN\nNomre: 0557133003`;
  window.open("https://wa.me/?text="+encodeURIComponent(text));
});

updateCartPopup();
</script>
</body>
</html>
