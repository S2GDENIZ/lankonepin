<!DOCTYPE html>
<html lang="az">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LANKONEPIN - PUBG Mobile UC Satış</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&display=swap" rel="stylesheet">
<style>
* { margin:0; padding:0; box-sizing:border-box; }
body { font-family: 'Orbitron', sans-serif; min-height:100vh; overflow-x:hidden; color:#fff; position:relative; transition:0.5s; background:#0a0015; }

/* BACKGROUND DOTS */
#background { position:fixed; top:0; left:0; width:100%; height:100%; z-index:-1; overflow:hidden; }
.neon-dot { position:absolute; width:6px; height:6px; border-radius:50%; box-shadow: 0 0 10px, 0 0 20px, 0 0 30px; animation: float 10s linear infinite; }
@keyframes float { 0% { transform: translateY(0) translateX(0); opacity:0; } 50% { opacity:1; } 100% { transform: translateY(-120vh) translateX(50vw); opacity:0; } }

/* AUTH SECTION */
#authSection { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: #000; z-index: 2000; display: flex; align-items: center; justify-content: center; }
.auth-container { background: #0a0015; padding: 40px; border: 2px solid #ff0000; border-radius: 20px; box-shadow: 0 0 25px #ff0000; width: 380px; text-align: center; }
.auth-container h2 { margin-bottom: 20px; color: #ff0000; text-shadow: 0 0 10px #ff0000; }
.auth-container input { width: 100%; padding: 12px; margin: 10px 0; background: #111; border: 1px solid #ff0000; color: #fff; border-radius: 5px; outline: none; }
.auth-container button { width: 100%; padding: 12px; background: #ff0000; border: none; color: #fff; font-weight: bold; cursor: pointer; border-radius: 5px; margin-top: 10px; transition: 0.3s; font-family: 'Orbitron'; }
.auth-container button:hover { background: #fff; color: #ff0000; }
.toggle-link { margin-top: 15px; font-size: 12px; cursor: pointer; color: #aaa; }
.toggle-link b { color: #ff0000; }

#mainContent { display: none; }

/* HEADER */
header { display:flex; align-items:center; justify-content:center; gap:15px; padding:20px; background: linear-gradient(90deg,#000,#111); box-shadow:0 0 20px #ff0241; position: relative; z-index:10; border-bottom:2px solid #e7000c; }
header img { width:70px; border-radius:10px; }
header h1 { font-size:2rem; text-transform:uppercase; letter-spacing:2px; color:#ff0c0c; }
#cart { position:absolute; right:20px; font-size:18px; cursor:pointer; background:#e7000c; color:#fff; padding:5px 10px; border-radius:6px; transition:0.3s; }

/* TOGGLE BG BUTTON */
#toggleBg { position:absolute; left:20px; font-size:14px; padding:5px 10px; border:none; border-radius:6px; background:#e7000c; color:#fff; cursor:pointer; z-index:15; }

/* CARD STYLE */
.container { padding:40px 20px; display:flex; flex-wrap:wrap; gap:30px; justify-content:center; }
.card { width:280px; background: rgba(17,17,17,0.85); border:2px solid #e7000c; border-radius:20px; text-align:center; padding:20px; transition:0.4s; backdrop-filter: blur(5px); }
.card:hover { transform: translateY(-10px); }
.card img { width:100%; border-radius:12px; margin-bottom:12px; }
.card h2 { font-size:1.4rem; color:#ff0c0c; }
.price { font-size:1.2rem; font-weight:bold; margin-bottom:12px; }
.card button { padding:12px 20px; background:#f80202; border:none; color:#000; font-weight:bold; cursor:pointer; border-radius:10px; }

.card.neon { animation: neonGradient 3s linear infinite; }
@keyframes neonGradient {
  0% { box-shadow: 0 0 15px #ff0c0c; border-color:#ff0c0c; }
  50% { box-shadow: 0 0 15px #00f; border-color:#00f; }
  100% { box-shadow: 0 0 15px #ff0c0c; border-color:#ff0c0c; }
}

/* CART POPUP */
#cartPopup { display:none; position:fixed; top:70px; right:20px; width:320px; max-height:500px; background: rgba(255,255,255,0.95); color:#000; border-radius:15px; box-shadow:0 0 25px rgba(0,0,0,0.5); overflow-y:auto; z-index:100; padding:15px; }
.cart-item { display:flex; justify-content:space-between; margin-bottom:10px; padding:5px; border-bottom:1px solid #ddd; align-items:center; }
.cart-item button { background:red; color:white; border:none; border-radius:5px; padding:2px 7px; cursor:pointer; font-weight:bold; }
#total { margin-top:10px; text-align:right; font-weight:bold; color:#e7000c; }
#checkoutBtn { display:block; width:100%; padding:12px; margin-top:10px; background:#e7000c; color:#fff; border:none; border-radius:8px; cursor:pointer; font-weight:bold; }

footer { text-align:center; padding:20px; margin-top:40px; background: #111; border-top:2px solid #e7000c; }
</style>
</head>
<body>

<div id="background"></div>

<div id="authSection">
    <div id="loginBox" class="auth-container">
        <h2>GİRİŞ</h2>
        <input type="email" id="lEmail" placeholder="Gmail">
        <input type="password" id="lPass" placeholder="Şifrə">
        <button onclick="checkLogin()">DAXİL OL</button>
        <p class="toggle-link" onclick="toggleForm()">Hesabın yoxdur? <b>Qeydiyyat</b></p>
    </div>
    <div id="regBox" class="auth-container" style="display:none;">
        <h2>QEYDİYYAT</h2>
        <input type="text" id="rName" placeholder="Ad">
        <input type="text" id="rSurname" placeholder="Soyad">
        <input type="tel" id="rTel" placeholder="Tel Nömrəsi">
        <input type="email" id="rEmail" placeholder="Gmail">
        <input type="password" id="rPass" placeholder="Şifrə">
        <button onclick="saveReg()">TAMAMLA</button>
        <p class="toggle-link" onclick="toggleForm()">Hesabın var? <b>Giriş</b></p>
    </div>
</div>

<div id="mainContent">
    <button id="toggleBg">Arxa fon dəyiş</button>
    <header>
      <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
      <h1>LANKONEPIN</h1>
      <div id="cart" onclick="toggleCartPopup()">🛒 0</div>
    </header>

    <div id="cartPopup">
      <h3 style="text-align:center">Səbətiniz</h3>
      <div id="cartItems"></div>
      <div id="total">Ümumi: 0.00 AZN</div>
      <button id="checkoutBtn" onclick="sendOrder()">Ödənişə davam et</button>
    </div>

    <div class="container">
      <div class="card neon"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>60 UC</h2><div class="price">1.87 AZN</div><button onclick="addToCart('60 UC',1.87)">Satın Al</button></div>
      <div class="card neon"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>325 UC</h2><div class="price">8.20 AZN</div><button onclick="addToCart('325 UC',8.20)">Satın Al</button></div>
      <div class="card neon"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>660 UC</h2><div class="price">16.11 AZN</div><button onclick="addToCart('660 UC',16.11)">Satın Al</button></div>
      <div class="card neon"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>1800 UC</h2><div class="price">41.20 AZN</div><button onclick="addToCart('1800 UC',41.20)">Satın Al</button></div>
      <div class="card neon"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>8100 UC</h2><div class="price">163.04 AZN</div><button onclick="addToCart('3850 UC',83.90)">Satın Al</button></div>
      <div class="card neon"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>8100 UC</h2><div class="price">163.04 AZN</div><button onclick="addToCart('8100 UC',163.04)">Satın Al</button></div>
      <div class="card neon"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>16200 UC</h2><div class="price">334.08 AZN</div><button onclick="addToCart('16200 UC',334.08)">Satın Al</button></div>
    </div>
    <footer>© 2026 LANKONEPIN</footer>
</div>

<script>
// BACKGROUND
for(let i=0;i<50;i++){
  let dot = document.createElement("div");
  dot.className="neon-dot";
  dot.style.left=Math.random()*100+"vw";
  dot.style.top=Math.random()*100+"vh";
  dot.style.background="red";
  document.getElementById("background").appendChild(dot);
}

// AUTH
function toggleForm() {
    document.getElementById('loginBox').style.display = document.getElementById('loginBox').style.display === "none" ? "block" : "none";
    document.getElementById('regBox').style.display = document.getElementById('regBox').style.display === "none" ? "block" : "none";
}
function saveReg() {
    localStorage.setItem("u_email", document.getElementById('rEmail').value);
    localStorage.setItem("u_pass", document.getElementById('rPass').value);
    alert("Qeydiyyat uğurludur!"); toggleForm();
}
function checkLogin() {
    if(document.getElementById('lEmail').value === localStorage.getItem("u_email") && document.getElementById('lPass').value === localStorage.getItem("u_pass")) {
        document.getElementById('authSection').style.display = 'none';
        document.getElementById('mainContent').style.display = 'block';
    } else { alert("Xəta!"); }
}

// CART SYSTEM (SİLMƏ FUNKSİYASI İLƏ)
let cart = [];

function addToCart(name, price){
  cart.push({name, price});
  updateCartUI();
}

// SƏBƏTDƏN SİLMƏ KODU BURADADIR
function removeFromCart(index) {
    cart.splice(index, 1); // Siyahıdan həmin indeksi silir
    updateCartUI(); // Səbəti yeniləyir
}

function updateCartUI() {
    document.getElementById("cart").innerText = `🛒 ${cart.length}`;
    let cartItemsDiv = document.getElementById("cartItems");
    cartItemsDiv.innerHTML = "";
    let total = 0;

    cart.forEach((item, index) => {
        total += item.price;
        cartItemsDiv.innerHTML += `
            <div class="cart-item">
                <span>${item.name} - ${item.price} AZN</span>
                <button onclick="removeFromCart(${index})">X</button>
            </div>`;
    });
    document.getElementById("total").innerText = `Ümumi: ${total.toFixed(2)} AZN`;
}

function toggleCartPopup() {
    let p = document.getElementById("cartPopup");
    p.style.display = p.style.display === "block" ? "none" : "block";
}

function sendOrder() {
    if(cart.length === 0) return alert("Səbət boşdur!");
    let msg = "Sifarişlərim:\n" + cart.map(i => i.name).join("\n");
    window.open("https://wa.me/0557133003?text=" + encodeURIComponent(msg));
}

let isBlack = true;
document.getElementById("toggleBg").onclick = () => {
    isBlack = !isBlack;
    document.body.style.background = isBlack ? "#0a0015" : "#fff";
};
</script>
</body>
</html>
