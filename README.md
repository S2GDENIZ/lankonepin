
<html lang="az">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LANKONEPIN - Gaming Store</title>
<link rel="icon" href="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s" type="image/x-icon">
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&display=swap" rel="stylesheet">
<style>
    * { margin:0; padding:0; box-sizing:border-box; }
    body { font-family: 'Orbitron', sans-serif; min-height:100vh; overflow-x:hidden; color:#fff; background:#0a0015; transition: 0.5s; scroll-behavior: smooth; }

    /* NEON ARXAFON */
    #background { position:fixed; top:0; left:0; width:100%; height:100%; z-index:-1; overflow:hidden; }
    .neon-dot { position:absolute; width:6px; height:6px; border-radius:50%; box-shadow: 0 0 10px, 0 0 20px, 0 0 30px; animation: float 10s linear infinite; }
    @keyframes float { 0% { transform: translateY(0) translateX(0); opacity:0; } 50% { opacity:1; } 100% { transform: translateY(-120vh) translateX(50vw); opacity:0; } }

    /* HEADER */
    header { 
        display:flex; align-items:center; justify-content: space-between; 
        padding:15px 40px; background: rgba(0, 0, 0, 0.95); 
        border-bottom:2px solid #e7000c; position: sticky; top: 0; z-index: 1000;
    }
    .logo-area { display: flex; align-items: center; gap: 15px; }
    header img { width:50px; border-radius:10px; border: 1px solid #ff0c0c; }
    header h1 { font-size:1.5rem; color:#ff0c0c; text-shadow: 0 0 10px #ff0c0c; }
    
    .nav-links { display: flex; gap: 20px; list-style: none; }
    .nav-links a { color: #fff; text-decoration: none; font-size: 13px; transition: 0.3s; opacity: 0.8; }
    .nav-links a:hover { opacity: 1; color: #ff0c0c; }

    .auth-nav { display: flex; align-items: center; gap: 15px; }
    .btn-auth { background: transparent; border: 1px solid #ff0c0c; color: #fff; padding: 8px 15px; border-radius: 5px; cursor: pointer; font-family: 'Orbitron'; font-size: 11px; transition: 0.3s; }
    .btn-auth:hover { background: #ff0c0c; box-shadow: 0 0 15px #ff0c0c; }
    #cart { font-size:16px; cursor:pointer; background:#e7000c; color:#fff; padding:8px 15px; border-radius:6px; font-weight: bold; }

    /* KATEQORİYA SEÇİMİ */
    .category-selector { text-align: center; padding: 50px 20px 20px; }
    .cat-btn { 
        background: #111; color: #fff; border: 1px solid #333; 
        padding: 12px 25px; margin: 8px; cursor: pointer; 
        font-family: 'Orbitron'; border-radius: 8px; transition: 0.4s; font-size: 12px;
    }
    .cat-btn:hover, .cat-btn.active { 
        border-color: #ff0c0c; background: #ff0c0c; box-shadow: 0 0 20px rgba(255, 12, 12, 0.4); 
    }

    /* MEHSULLAR */
    .cat-content { display: none; padding: 20px; flex-wrap: wrap; justify-content: center; gap: 25px; animation: fadeIn 0.5s ease; }
    .cat-content.active { display: flex; }
    @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

    .card { width:260px; background: rgba(17,17,17,0.95); border:1px solid #222; border-radius:15px; text-align:center; padding:20px; transition:0.4s; }
    .card:hover { border-color: #ff0c0c; transform: translateY(-8px); box-shadow: 0 10px 30px rgba(231, 0, 12, 0.2); }
    .card img { width:100%; height: 150px; object-fit: cover; border-radius:10px; margin-bottom:15px; }
    .card h2 { font-size:1.1rem; color:#fff; margin-bottom: 8px;}
    .price { font-size:1.1rem; font-weight:bold; color: #ff0c0c; margin-bottom:15px; }
    .card button { width: 100%; padding:10px; background:#e7000c; border:none; color:#fff; font-weight:bold; cursor:pointer; border-radius:8px; font-family: 'Orbitron'; font-size: 11px; }

    /* SECTIONS */
    .section-title { text-align: center; color: #ff0c0c; margin: 60px 0 30px; text-shadow: 0 0 10px #ff0c0c; }
    .info-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; max-width: 1100px; margin: 0 auto; padding: 20px; }
    .info-card { background: #111; padding: 25px; border-radius: 12px; border-left: 3px solid #ff0c0c; }
    
    .contact-area { display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; padding-bottom: 50px; }
    .contact-link { text-decoration: none; color: #fff; padding: 15px 30px; border-radius: 50px; font-weight: bold; font-size: 13px; transition: 0.3s; }
    .whatsapp { background: #25d366; }
    .instagram { background: linear-gradient(45deg, #f09433, #dc2743, #bc1888); }

    /* SEBET */
    #cartPopup { display:none; position:fixed; top:80px; right:40px; width:300px; background: #fff; color:#000; border-radius:10px; box-shadow:0 10px 30px rgba(0,0,0,0.5); z-index:2000; padding:15px; }
    .cart-item { display:flex; justify-content:space-between; margin-bottom:10px; border-bottom:1px solid #eee; padding-bottom: 5px; font-size: 12px; font-family: sans-serif; color: #333;}

    /* MODAL */
    .modal-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.85); display: none; align-items: center; justify-content: center; z-index: 3000; }
    .auth-container { background: #0a0015; padding: 35px; border: 2px solid #ff0000; border-radius: 20px; width: 340px; text-align: center; position: relative; }
    .close-modal { position: absolute; top: 10px; right: 15px; cursor: pointer; color: #ff0000; font-size: 20px; }
    .auth-container input { width: 100%; padding: 12px; margin: 10px 0; background: #111; border: 1px solid #333; color: #fff; border-radius: 5px; outline: none; }
    .auth-container button { width: 100%; padding: 12px; background: #ff0000; border: none; color: #fff; font-weight: bold; cursor: pointer; border-radius: 5px; margin-top: 10px; font-family: 'Orbitron'; }

    footer { text-align:center; padding:40px; background: #000; border-top:1px solid #222; font-size: 12px; color: #555; }
</style>
</head>
<body>

<div id="background"></div>

<header>
    <div class="logo-area">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s">
        <h1>LANKONEPIN</h1>
    </div>
    <ul class="nav-links">
        <li><a href="#store">MAĞAZA</a></li>
        <li><a href="#about">HAQQIMIZDA</a></li>
        <li><a href="#contact">ƏLAQƏ</a></li>
    </ul>
    <div class="auth-nav">
        <div id="cart" onclick="toggleCartPopup()">🛒 0</div>
        <div id="userArea">
            <button class="btn-auth" onclick="openModal('login')">GİRİŞ</button>
        </div>
    </div>
</header>

<div id="mainContent">
    <div class="category-selector" id="store">
        <button class="cat-btn active" onclick="openCategory(event, 'pubg')">PUBG MOBILE</button>
        <button class="cat-btn" onclick="openCategory(event, 'ff')">FREE FIRE</button>
        <button class="cat-btn" onclick="openCategory(event, 'valorant')">VALORANT</button>
    </div>

    <div id="pubg" class="cat-content active">
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>60 UC</h2><div class="price">1.87 AZN</div><button onclick="addToCart('60 UC',1.87)">SƏBƏTƏ AT</button></div>
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>325 UC</h2><div class="price">8.20 AZN</div><button onclick="addToCart('325 UC',8.20)">SƏBƏTƏ AT</button></div>
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>660 UC</h2><div class="price">16.11 AZN</div><button onclick="addToCart('660 UC',16.11)">SƏBƏTƏ AT</button></div>
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>1800 UC</h2><div class="price">41.20 AZN</div><button onclick="addToCart('1800 UC',41.20)">SƏBƏTƏ AT</button></div>
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>3850 UC</h2><div class="price">83.90 AZN</div><button onclick="addToCart('3850 UC',83.90)">SƏBƏTƏ AT</button></div>
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>8100 UC</h2><div class="price">163.04 AZN</div><button onclick="addToCart('8100 UC',163.04)">SƏBƏTƏ AT</button></div>
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>16200 UC</h2><div class="price">320.00 AZN</div><button onclick="addToCart('16200 UC',320.00)">SƏBƏTƏ AT</button></div>
    </div>

    <div id="ff" class="cat-content">
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>100 Diamonds</h2><div class="price">2.20 AZN</div><button onclick="addToCart('100 FF Diamonds',2.20)">SƏBƏTƏ AT</button></div>
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>210 Diamonds</h2><div class="price">4.40 AZN</div><button onclick="addToCart('210 FF Diamonds',4.40)">SƏBƏTƏ AT</button></div>
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>530 Diamonds</h2><div class="price">10.50 AZN</div><button onclick="addToCart('530 FF Diamonds',10.50)">SƏBƏTƏ AT</button></div>
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>1080 Diamonds</h2><div class="price">20.80 AZN</div><button onclick="addToCart('1080 FF Diamonds',20.80)">SƏBƏTƏ AT</button></div>
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>2200 Diamonds</h2><div class="price">40.50 AZN</div><button onclick="addToCart('2200 FF Diamonds',40.50)">SƏBƏTƏ AT</button></div>
    </div>

    <div id="valorant" class="cat-content">
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>600 VP</h2><div class="price">10.50 AZN</div><button onclick="addToCart('600 VP',10.50)">SƏBƏTƏ AT</button></div>
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>1200 VP</h2><div class="price">19.80 AZN</div><button onclick="addToCart('1200 VP',19.80)">SƏBƏTƏ AT</button></div>
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>2850 VP</h2><div class="price">45.00 AZN</div><button onclick="addToCart('2850 VP',45.00)">SƏBƏTƏ AT</button></div>
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>5250 VP</h2><div class="price">82.00 AZN</div><button onclick="addToCart('5250 VP',82.00)">SƏBƏTƏ AT</button></div>
        <div class="card"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3oW9PFt8LZ8xR7SE8FJa0VW6JL6ba9h7OCg&s"><h2>8500 VP</h2><div class="price">130.00 AZN</div><button onclick="addToCart('8500 VP',130.00)">SƏBƏTƏ AT</button></div>
    </div>

    <section id="about">
        <h2 class="section-title">NİYƏ LANKONEPIN?</h2>
        <div class="info-grid">
            <div class="info-card"><h3>⚡ Sürətli Təslim</h3><p style="color:#777; font-size:13px; margin-top:10px;">5-15 dəqiqə ərzində avtomatik yükləmə.</p></div>
            <div class="info-card"><h3>🛡️ Tam Təhlükəsiz</h3><p style="color:#777; font-size:13px; margin-top:10px;">Rəsmi və zəmanətli xidmət.</p></div>
            <div class="info-card"><h3>💎 Ucuz Qiymət</h3><p style="color:#777; font-size:13px; margin-top:10px;">Bazarda ən sərfəli təkliflər.</p></div>
        </div>
    </section>

    <section id="contact">
        <h2 class="section-title">ƏLAQƏ</h2>
        <div class="contact-area">
            <a href="https://wa.me/994557133003" class="contact-link whatsapp">WhatsApp</a>
            <a href="https://instagram.com/lankonepin" class="contact-link instagram">Instagram</a>
        </div>
    </section>

    <footer>© 2026 LANKONEPIN - Bütün hüquqlar qorunur.</footer>
</div>

<div id="cartPopup">
    <h3 style="font-size: 14px; margin-bottom: 10px; border-bottom: 1px solid #ddd; padding-bottom: 5px;">Səbətiniz</h3>
    <div id="cartItems"></div>
    <div id="total" style="font-size: 14px; font-weight: bold; margin-top: 10px; color: #e7000c;">Ümumi: 0.00 AZN</div>
    <button onclick="prepareOrder()" style="width:100%; padding:10px; background:#000; color:#fff; border:none; border-radius:5px; margin-top:10px; cursor:pointer; font-family:'Orbitron'; font-size:10px;">SİFARİŞİ TAMAMLA</button>
</div>

<div class="modal-overlay" id="modalOverlay">
    <div id="loginBox" class="auth-container" style="display:none;">
        <span class="close-modal" onclick="closeModal()">&times;</span>
        <h2 style="color:#ff0000; margin-bottom:15px; font-size: 1.2rem;">GİRİŞ</h2>
        <input type="email" id="lEmail" placeholder="Gmail">
        <input type="password" id="lPass" placeholder="Şifrə">
        <button onclick="checkLogin()">DAXİL OL</button>
        <p style="font-size:10px; margin-top:15px; cursor:pointer; color:#777" onclick="switchModal('reg')">Hesabınız yoxdur? Qeydiyyat</p>
    </div>
    
    <div id="regBox" class="auth-container" style="display:none;">
        <span class="close-modal" onclick="closeModal()">&times;</span>
        <h2 style="color:#ff0000; margin-bottom:15px; font-size: 1.2rem;">QEYDİYYAT</h2>
        <input type="text" id="rName" placeholder="Ad Soyad">
        <input type="email" id="rEmail" placeholder="Gmail">
        <input type="tel" id="rPhone" placeholder="Telefon Nömrəsi">
        <input type="password" id="rPass" placeholder="Şifrə">
        <button onclick="saveReg()">TAMAMLA</button>
        <p style="font-size:10px; margin-top:15px; cursor:pointer; color:#777" onclick="switchModal('login')">Hesabınız var? Giriş</p>
    </div>

    <div id="checkoutBox" class="auth-container" style="display:none;">
        <span class="close-modal" onclick="closeModal()">&times;</span>
        <h2 style="color:#ff0000; margin-bottom:15px; font-size: 1.2rem;">SİFARİŞİ TAMAMLA</h2>
        <input type="text" id="cName" placeholder="Ad Soyad">
        <input type="tel" id="cPhone" placeholder="Telefon Nömrəsi">
        <input type="text" id="cGameId" placeholder="Oyun ID (və ya link)">
        <button onclick="submitWhatsApp()">SİFARİŞİ GÖNDƏR</button>
    </div>
</div>

<script>
    for(let i=0; i<30; i++){
        let dot = document.createElement("div");
        dot.className="neon-dot";
        dot.style.left=Math.random()*100+"vw";
        dot.style.top=Math.random()*100+"vh";
        dot.style.background="red";
        document.getElementById("background").appendChild(dot);
    }

    function openCategory(evt, catName) {
        let contents = document.getElementsByClassName("cat-content");
        for (let i = 0; i < contents.length; i++) { contents[i].style.display = "none"; }
        let btns = document.getElementsByClassName("cat-btn");
        for (let i = 0; i < btns.length; i++) { btns[i].classList.remove("active"); }
        document.getElementById(catName).style.display = "flex";
        evt.currentTarget.classList.add("active");
    }

    let cart = [];
    function addToCart(name, price){
        cart.push({name, price});
        updateCartUI();
    }
    function removeFromCart(index) {
        cart.splice(index, 1);
        updateCartUI();
    }
    function updateCartUI() {
        document.getElementById("cart").innerText = `🛒 ${cart.length}`;
        let div = document.getElementById("cartItems");
        div.innerHTML = "";
        let total = 0;
        cart.forEach((item, index) => {
            total += item.price;
            div.innerHTML += `<div class="cart-item"><span>${item.name}</span><span>${item.price} AZN <button onclick="removeFromCart(${index})" style="background:none; border:none; color:red; cursor:pointer; font-weight:bold;">x</button></span></div>`;
        });
        document.getElementById("total").innerText = `Ümumi: ${total.toFixed(2)} AZN`;
    }
    function toggleCartPopup() {
        let p = document.getElementById("cartPopup");
        p.style.display = p.style.display === "block" ? "none" : "block";
    }

    function prepareOrder() {
        if(cart.length === 0) return alert("Səbət boşdur!");
        toggleCartPopup();
        openModal('checkout');
    }

    function submitWhatsApp() {
        let name = document.getElementById('cName').value;
        let phone = document.getElementById('cPhone').value;
        let gameId = document.getElementById('cGameId').value;

        if(!name || !phone || !gameId) {
            alert("Zəhmət olmasa bütün xanaları doldurun!");
            return;
        }

        let msg = `YENİ SİFARİŞ!%0A%0A` +
                  `Müştəri: ${name}%0A` +
                  `Telefon: ${phone}%0A` +
                  `Oyun ID: ${gameId}%0A%0A` +
                  `Məhsullar:%0A` + 
                  cart.map(i => "- " + i.name).join("%0A");

        window.open("https://wa.me/994557133003?text=" + msg);
        closeModal();
    }

    function openModal(type) { document.getElementById('modalOverlay').style.display = 'flex'; switchModal(type); }
    function closeModal() { document.getElementById('modalOverlay').style.display = 'none'; }
    function switchModal(type) {
        document.getElementById('loginBox').style.display = type === 'login' ? 'block' : 'none';
        document.getElementById('regBox').style.display = type === 'reg' ? 'block' : 'none';
        document.getElementById('checkoutBox').style.display = type === 'checkout' ? 'block' : 'none';
    }
    
    function saveReg() {
        let name = document.getElementById('rName').value;
        let email = document.getElementById('rEmail').value;
        let phone = document.getElementById('rPhone').value;
        let pass = document.getElementById('rPass').value;

        let emailPattern = /^[a-zA-Z0-9._%+-]+@gmail\.com$/;
        if (!emailPattern.test(email)) {
            alert("Zəhmət olmasa düzgün bir @gmail.com ünvanı daxil edin!");
            return;
        }

        let phonePattern = /^[0-9]{10}$/; 
        if (!phonePattern.test(phone)) {
            alert("Zəhmət olmasa düzgün telefon nömrəsi daxil edin (məsələn: 0501234567)");
            return;
        }

        if (name === "" || pass === "") {
            alert("Zəhmət olmasa bütün sahələri doldurun!");
            return;
        }

        localStorage.setItem("u_email", email);
        localStorage.setItem("u_pass", pass);
        localStorage.setItem("u_name", name);
        localStorage.setItem("u_phone", phone);
        alert("Qeydiyyat tamamlandı! Giriş edin."); 
        switchModal('login');
    }

    function checkLogin() {
        if(document.getElementById('lEmail').value === localStorage.getItem("u_email") && 
           document.getElementById('lPass').value === localStorage.getItem("u_pass")) {
            document.getElementById('userArea').innerHTML = `<span style="color:#ff0c0c; font-size:12px;">${localStorage.getItem("u_name")}</span>`;
            closeModal();
        } else { alert("Gmail və ya şifrə səhvdir!"); }
    }
</script>
</body>
</html>
