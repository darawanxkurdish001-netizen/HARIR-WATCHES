HARIR WATCHES
<html lang="ku">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>HARIR WATCHS</title>

<!-- ICONS -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

<style>
body {
    margin:0;
    font-family: Arial;
    background:#f5f5f5;
}

/* HEADER */
header {
    background:black;
    color:white;
    text-align:center;
    padding:20px;
}

.logo {
    width: 90px;
    margin-bottom: 10px;
}

/* SEARCH */
.search-box {
    text-align:center;
    padding:10px;
}

.search-box input {
    width:80%;
    padding:10px;
    border-radius:10px;
    border:1px solid #ccc;
}

/* GRID */
.container {
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(180px,1fr));
    gap:15px;
    padding:20px;
}

/* PRODUCT */
.product {
    background:white;
    border-radius:12px;
    overflow:hidden;
    box-shadow:0 3px 10px rgba(0,0,0,0.1);
    transition:0.3s;
}

.product:hover {
    transform:scale(1.05);
}

.product img {
    width:100%;
    height:180px;
    object-fit:cover;
}

.product h4 {
    margin:10px;
}

.price {
    color:green;
    font-weight:bold;
}

/* BUTTONS */
.btn {
    display:block;
    background:black;
    color:white;
    margin:5px 10px;
    padding:8px;
    border-radius:8px;
    text-decoration:none;
    text-align:center;
}

.fav {
    background:red;
}

/* CONTACT */
.contact {
    background:black;
    color:white;
    text-align:center;
    padding:20px;
}

.social a {
    display:inline-block;
    margin:10px;
    padding:10px 15px;
    border-radius:8px;
    color:white;
    text-decoration:none;
}

.facebook { background:#1877f2; }
.snapchat { background:#fffc00; color:black; }
.whatsapp { background:#25d366; }

/* FLOATING WHATSAPP */
.whatsapp-float {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background: #25d366;
    color: white;
    font-size: 28px;
    padding: 15px;
    border-radius: 50%;
    box-shadow: 0 4px 10px rgba(0,0,0,0.3);
    z-index: 1000;
}
</style>
</head>

<body>

<header>
    <img src="Logo.ping333"="HARIR WATCHS Logo">
    <h1>⌚ HARIR WATCHS</h1>
    <p>فروشتنی ئیکسسواراتی کوران و کچان</p>
    <p>فروشتن و چاککردنەوەی هەموو کاتژمێری</p>
</header>

<div class="search-box">
    <input type="text" id="search" placeholder="گەڕان بۆ سەعات..." onkeyup="searchProduct()">
</div>

<div class="container" id="products"></div>

<div class="contact">
    <h2>پەیوەندی</h2>
    <p>📞 0750 430 7316</p>

    <div class="social">
        <a class="facebook" href="https://www.facebook.com/share/17Q6HzNqRQ/" target="_blank">
            <i class="fab fa-facebook"></i> Facebook
        </a>

        <a class="snapchat" href="https://www.snapchat.com/add/harir_wotchs?share_id=D7t7n2XT1qU&locale=ar-IQ" target="_blank">
            <i class="fab fa-snapchat"></i> Snapchat
        </a>

        <a class="whatsapp" href="https://wa.me/9647504307316" target="_blank">
            <i class="fab fa-whatsapp"></i> 0750 430 7316
        </a>
    </div>
</div>

<!-- FLOATING WHATSAPP -->
<a href="https://wa.me/9647504307316?text=سڵاو%20دەمەوێت%20سەعات%20بکڕم" 
   class="whatsapp-float" target="_blank">
   <i class="fab fa-whatsapp"></i>
</a>

<script>
let container = document.getElementById("products");

for(let i=1;i<=21;i++){
    container.innerHTML += `
    <div class="product">
        <img src="${i}.jpg">
        <h4>سەعات ${i}</h4>
        <p class="price">$${40+i}</p>

        <a class="btn" href="https://wa.me/9647504307316?text=دەمەوێت سەعات ${i}">کڕین</a>
        <button class="btn fav" onclick="addFav(${i})">❤️ دڵخواز</button>
    </div>
    `;
}

function searchProduct(){
    let input = document.getElementById("search").value.toLowerCase();
    let items = document.querySelectorAll(".product");

    items.forEach(item=>{
        let text = item.innerText.toLowerCase();
        item.style.display = text.includes(input) ? "block" : "none";
    });
}

function addFav(id){
    alert("سەعات "+id+" زیادکرا بۆ دڵخواز ❤️");
}
</script>

</body>
</html>
