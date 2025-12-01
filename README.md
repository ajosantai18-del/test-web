# test-web[aprinabag_enhanced.html](https://github.com/user-attachments/files/23854683/aprinabag_enhanced.html)
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aprina Bag - Tas Ramah Lingkungan</title>

<style>
/* Reset */
* { margin:0; padding:0; box-sizing:border-box; }

/* Body */
body {
    font-family: Arial, sans-serif;
    background:#f5fff5;
    color:#333;
    animation: fadeIn 1s ease;
}
@keyframes fadeIn { from {opacity:0;} to {opacity:1;} }

/* Header */
header {
    background: linear-gradient(135deg,#4CAF50,#66BB6A,#81C784);
    padding:50px 20px;
    color:white;
    text-align:center;
    box-shadow:0 5px 10px rgba(0,0,0,0.2);
}
header h1 { font-size:3em; }

/* Slider */
.slider-container {
    width:100%;
    max-width:900px;
    margin:40px auto;
    position:relative;
    overflow:hidden;
    border-radius:20px;
    box-shadow:0 8px 20px rgba(0,0,0,0.2);
}
.slider-track {
    display:flex;
    transition:transform 0.6s ease-in-out;
}
.slider-track img {
    width:100%;
    height:350px;
    object-fit:cover;
}

/* Slider buttons */
.slider-btn {
    position:absolute;
    top:50%;
    transform:translateY(-50%);
    background:rgba(0,0,0,0.4);
    color:white;
    border:none;
    font-size:2em;
    padding:10px 15px;
    cursor:pointer;
    border-radius:50%;
}
.prev { left:10px; }
.next { right:10px; }

/* Products */
.products {
    padding:30px 20px;
    text-align:center;
}
.product-list {
    display:flex;
    flex-wrap:wrap;
    justify-content:center;
    gap:25px;
}
.product {
    width:280px;
    background:white;
    border-radius:15px;
    padding-bottom:15px;
    box-shadow:0 5px 12px rgba(0,0,0,0.15);
    transition:transform .4s, box-shadow .4s;
}
.product:hover {
    transform:translateY(-10px) scale(1.03);
    box-shadow:0 12px 20px rgba(0,0,0,0.25);
}
.product img {
    width:100%;
    height:220px;
    object-fit:cover;
    border-radius:15px 15px 0 0;
}

/* Contact Section */
.contact {
    background:#e8f5e8;
    padding:50px 20px;
    border-radius:20px;
    max-width:600px;
    margin:50px auto;
}
.contact input, .contact textarea {
    width:100%;
    padding:15px;
    margin:10px 0;
    border:2px solid #4CAF50;
    border-radius:10px;
    font-size:1em;
}
.contact button {
    background:#4CAF50;
    border:none;
    color:white;
    padding:15px;
    width:100%;
    font-size:1.1em;
    cursor:pointer;
    border-radius:10px;
    transition:.3s;
}
.contact button:hover {
    background:#45a049;
}

/* WhatsApp Button */
.whatsapp-btn {
    position:fixed;
    bottom:25px;
    right:25px;
    background:#25D366;
    padding:15px 20px;
    border-radius:50px;
    color:white;
    font-size:1.2em;
    text-decoration:none;
    box-shadow:0 8px 20px rgba(0,0,0,0.3);
    animation:bounce 1.5s infinite;
}
@keyframes bounce {
    0%,100% { transform:translateY(0); }
    50% { transform:translateY(-8px); }
}

/* Mobile */
@media(max-width:768px){
    header h1{ font-size:2.2em; }
    .slider-track img{ height:250px; }
    .product{ width:90%; }
}
</style>
</head>

<body>

<header>
<h1>Aprina Bag - Tas Ramah Lingkungan</h1>
<p>Tas daur ulang berkualitas tinggi untuk gaya hidup hijau.</p>
</header>

<!-- SLIDER -->
<div class="slider-container">
    <div class="slider-track" id="slider">
        <img src="https://i.ibb.co.com/B5wngxtQ/Whats-App-Image-2025-11-29-at-01-52-32.jpg">
    </div>
    <button class="slider-btn prev" onclick="moveSlide(-1)">❮</button>
    <button class="slider-btn next" onclick="moveSlide(1)">❯</button>
</div>

<!-- PRODUCTS -->
<section class="products">
<h2>Produk Kami</h2>
<div class="product-list">

<div class="product">
    <img src="https://i.ibb.co.com/B5wngxtQ/Whats-App-Image-2025-11-29-at-01-52-32.jpg">
    <h3>Aprina Bag</h3>
    <p>Tas organik tahan lama dan stylish.</p>
    <p><b>Rp 15.000</b></p>
</div>

</div>
</section>

<!-- CONTACT -->
<section class="contact">
<h2>Hubungi Kami</h2>

<form id="contactForm">
    <input type="text" id="name" placeholder="Nama Anda" required>
    <input type="email" id="email" placeholder="Email Anda" required>
    <input type="tel" id="phone" placeholder="Nomor Telepon" required>
    <textarea id="message" rows="4" placeholder="Pesan Anda" required></textarea>
    <button type="submit">Kirim Pesan</button>
</form>

</section>

<!-- WHATSAPP -->
<a href="https://wa.me/6281234567890" class="whatsapp-btn" target="_blank">💬 Chat WhatsApp</a>

<footer style="text-align:center;padding:30px;background:#4CAF50;color:white;margin-top:40px;">
&copy; 2025 Aprina Bag Official Store.
</footer>

<script>
// Slider
let slideIndex = 0;
function moveSlide(n){
    const slider = document.getElementById("slider");
    const slides = slider.children.length;
    slideIndex = (slideIndex + n + slides) % slides;
    slider.style.transform = "translateX(" + (-slideIndex * 100) + "%)";
}

// Contact form validation
document.getElementById("contactForm").addEventListener("submit", function(e){
    e.preventDefault();
    alert("Pesan berhasil dikirim!");
    this.reset();
});
</script>

</body>
</html>
