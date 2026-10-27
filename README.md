# mz-phonez-and-accessories-
.MZ PHONED
<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>MZ Phones and Accessories - Kampala</title>
<link rel="stylesheet" href="style.css">
</head>
<body>

<header>
<h1>MZ PHONES</h1>
<p>0708838099 | 0751329525 | 0773594560</p>
<nav>
<a href="#home">Home</a>
<a href="#phones">Phones</a>
<a href="#accessories">Accessories</a>
<a href="#services">Services</a>
<a href="#contact">Contact</a>
</nav>
</header>

<section id="home" class="hero">
<h2>Original Phones in Kampala</h2>
<p>Best Prices - 1 Year Warranty - Pay on Delivery</p>
<a href="#phones" class="btn">View Phones</a>
<a href="https://wa.me/256708838099" class="btn green">WhatsApp Order</a>
</section>

<section id="phones">
<h3 class="section-title">🔥 NEW STOCK - HOT DEALS</h3>
<div class="grid" id="phone-grid"></div>
</section>

<section id="accessories">
<h3 class="section-title">🎧 Accessories</h3>
<div class="grid">
<div class="card"><img src="https://via.placeholder.com/300?text=Power+Bank"><h4>Power Bank 20,000mAh</h4><p>UGX 80,000</p></div>
<div class="card"><img src="https://via.placeholder.com/300?text=Charger"><h4>Fast Chargers</h4><p>UGX 30,000</p></div>
<div class="card"><img src="https://via.placeholder.com/300?text=Covers"><h4>Phone Covers</h4><p>UGX 15,000</p></div>
<div class="card"><img src="https://via.placeholder.com/300?text=Screen+Protector"><h4>Screen Protectors</h4><p>UGX 10,000</p></div>
</div>
</section>

<section id="services">
<h3 class="section-title">🔧 Our Services</h3>
<div class="services-box">
<div class="service">📱 <b>Phone Sales</b><br>New & UK Used - Tecno, Infinix, Samsung, iPhone, Redmi, Pixel, Villaon</div>
<div class="service">🎧 <b>Accessories</b><br>Chargers, Covers, Power Banks, Speakers, Earphones, Cables</div>
<div class="service">🔧 <b>Repair & Flashing</b><br>Screen replacement, Flashing, Unlocking, Software</div>
<div class="service">🔄 <b>Swap & Top-up</b><br>Bring old phone, add money and get new one</div>
<div class="service">🚚 <b>Delivery</b><br>Same day delivery in Kampala, Wakiso, Mukono</div>
<div class="service">💰 <b>Wholesale</b><br>Special price for shops & resellers</div>
</div>
</section>

<section id="contact" class="contact-box">
<h3>📞 Contact MZ Phones</h3>
<p><b>Call:</b> 0708838099 / 0751329525 / 0773594560</p>
<p><b>Location:</b> Kampala, Uganda</p>
<p><b>Hours:</b> 8am - 8pm Daily</p>
<a href="tel:0708838099" class="btn">Call Now</a>
<a href="https://wa.me/256708838099?text=Hello%20MZ%20Phones,%20I%20want%20to%20buy" class="btn green">WhatsApp Us</a>
</section>

<footer>© 2026 MZ Phones and Accessories - All phones with warranty</footer>

<script src="script.js"></script>
</body>
</html>body{margin:0;font-family:sans-serif;background:#f2f2f2}
header{background:#0D47A1;color:white;padding:10px;text-align:center;position:sticky;top:0;z-index:20}
header h1{margin:5px}
nav a{color:white;margin:0 10px;text-decoration:none;font-weight:bold;font-size:14px}
.hero{background:white;padding:30px 15px;text-align:center}
.btn{display:inline-block;background:#0D47A1;color:white;padding:12px 20px;border-radius:8px;text-decoration:none;margin:5px;font-weight:bold}
.btn.green{background:#25D366}
.section-title{padding:15px;background:white;margin:15px 0 0 0;border-left:5px solid #0D47A1}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;padding:10px}
.card{background:white;padding:10px;border-radius:10px;text-align:center;position:relative;box-shadow:0 2px 5px #0001}
.card img{width:100%;border-radius:8px;height:160px;object-fit:contain;background:white}
.price{color:#0D47A1;font-weight:bold;font-size:18px}
.tag{background:red;color:white;padding:2px 6px;font-size:11px;border-radius:4px;position:absolute;top:10px;left:10px}
.card button{background:#0D47A1;color:white;border:none;padding:8px;width:100%;border-radius:5px;margin-top:5px}
.call-btn{background:#333 !important}
.services-box{display:grid;grid-template-columns:1fr 1fr;gap:10px;padding:10px}
.service{background:white;padding:15px;border-radius:10px;font-size:14px;box-shadow:0 2px 4px #0001}
.contact-box{background:white;padding:20px;text-align:center;margin:10px;border-radius:10px}
footer{background:black;color:white;text-align:center;padding:15px}let allPhones = [
  {
    name: "Redmi 17 - 12GB RAM / 256GB ROM",
    price: "650,000",
    img: "redmi17.jpg",
    tag: "NEW ARRIVAL"
  },
  {
    name: "Google Pixel 9 - 128GB - Lavender",
    price: "2,100,000",
    img: "pixel9.jpg",
    tag: "UK USED"
  },
  {
    name: "Samsung Galaxy A03s - 3 Colors",
    price: "450,000",
    img: "a03s.jpg",
    tag: "NEW"
  },
  {
    name: "VILLAON - 4 Camera - 128GB",
    price: "350,000",
    img: "villaon.jpg",
    tag: "NEW"
  }
];

let container = document.getElementById("phone-grid");
let html = "";
allPhones.forEach(p => {
  html += `
    <div class="card">
      <span class="tag">${p.tag}</span>
      <img src="${p.img}">
      <h4>${p.name}</h4>
      <p class="price">UGX ${p.price}</p>
      <button onclick="order('${p.name}')">Order on WhatsApp</button>
      <button class="call-btn" onclick="call()">Call to Order</button>
    </div>
  `;
});
container.innerHTML = html;

function order(name){
  window.open(`https://wa.me/256708838099?text=Hello%20MZ%20Phones,%20I%20want%20to%20buy%20${encodeURIComponent(name)}`, "_blank");
}
function call(){
  window.open("tel:0708838099");
}file:///data/user/0/com.foxdebug.acodefree/files/public/Marah/Marahhttps://via.placeholder.com/300?text=Power+Bankhttps://wa.me/256708838099?text=Hello%20MZ%20Phones,%20I%20want%20to%20buybody{margin:0;font-family:sans-serif;background:#f2f2f2}
header{background:#0D47A1;color:white;padding:10px;text-align:center;position:sticky;top:0;z-index:20}
header h1{margin:5px}
nav a{color:white;margin:0 10px;text-decoration:none;font-weight:bold;font-size:14px}
.hero{background:white;padding:30px 15px;text-align:center}
.btn{display:inline-block;background:#0D47A1;color:white;padding:12px 20px;border-radius:8px;text-decoration:none;margin:5px;font-weight:bold}
.btn.green{background:#25D366}
.section-title{padding:15px;background:white;margin:15px 0 0 0;border-left:5px solid #0D47A1}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;padding:10px}
.card{background:white;padding:10px;border-radius:10px;text-align:center;position:relative;box-shadow:0 2px 5px #0001}
.card img{width:100%;border-radius:8px;height:160px;object-fit:contain;background:white}
.price{color:#0D47A1;font-weight:bold;font-size:18px}
.tag{background:red;color:white;padding:2px 6px;font-size:11px;border-radius:4px;position:absolute;top:10px;left:10px}
.card button{background:#0D47A1;color:white;border:none;padding:8px;width:100%;border-radius:5px;margin-top:5px}
.call-btn{background:#333 !important}
.services-box{display:grid;grid-template-columns:1fr 1fr;gap:10px;padding:10px}
.service{background:white;padding:15px;border-radius:10px;font-size:14px;box-shadow:0 2px 4px #0001}
.contact-box{background:white;padding:20px;text-align:center;margin:10px;border-radius:10px}
footer{background:black;color:white;text-align:center;padding:15px}https://wa.me/256708838099?text=Hello%20MZ%20Phones,%20I%20want%20to%20buy%20${encodeURIComponent(name)