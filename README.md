<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>black_pods_ngm</title>

<style>
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: #0f0f0f;
    color: #fff;
}

header {
    background: linear-gradient(90deg,#00ff99,#00ccff);
    color: #000;
    padding: 20px;
    text-align: center;
}

.container {
    padding: 20px;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px,1fr));
    gap: 20px;
}

.card {
    background: #1c1c1c;
    border-radius: 10px;
    padding: 15px;
    box-shadow: 0 0 10px rgba(0,255,200,0.3);
}

.card h3 {
    margin: 0;
    color: #00ffcc;
}

.price {
    font-size: 18px;
    margin: 10px 0;
    color: #00ff99;
}

button {
    background: #00ff99;
    border: none;
    padding: 10px;
    width: 100%;
    border-radius: 5px;
    font-size: 16px;
    cursor: pointer;
}

button:hover {
    background: #00cc77;
}

.cart {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    background: #000;
    padding: 15px;
    border-top: 2px solid #00ff99;
}

.cart span {
    font-size: 18px;
}

.checkout {
    background: #00ff99;
    color: #000;
    padding: 10px;
    border-radius: 5px;
    float: right;
    text-decoration: none;
    font-weight: bold;
}
</style>
</head>

<body>

<header>
<h1>🔥 black_pods_ngm 🔥</h1>
<p>Os melhores pods do mercado</p>
</header>

<div class="container">

<div class="card">
<h3>Refil Life Pod 8k</h3>
<p>Tropical Ice • Lemon Mint</p>
<p class="price">R$ 75,00</p>
<button onclick="addToCart(75)">Adicionar</button>
</div>

<div class="card">
<h3>OxBar 8k</h3>
<p>Rainbow Drop</p>
<p class="price">R$ 90,00</p>
<button onclick="addToCart(90)">Adicionar</button>
</div>

<div class="card">
<h3>Refil Life Pod 10k</h3>
<p>Menthol • Love 66 • Mint Bubblegum • Passion Mango Ice</p>
<p class="price">R$ 90,00</p>
<button onclick="addToCart(90)">Adicionar</button>
</div>

<div class="card">
<h3>IGNITE V80</h3>
<p>Strawberry Ice • Grape Ice • Blueberry Ice</p>
<p class="price">R$ 100,00</p>
<button onclick="addToCart(100)">Adicionar</button>
</div>

<div class="card">
<h3>IGNITE V80 Chrome</h3>
<p>Icy Mint • Menthol • Blueberry Ice • Passion Fruit Kiwi</p>
<p class="price">R$ 110,00</p>
<button onclick="addToCart(110)">Adicionar</button>
</div>

<div class="card">
<h3>Lost Mary MT 35k</h3>
<p>Strawberry Kiwi</p>
<p class="price">R$ 130,00</p>
<button onclick="addToCart(130)">Adicionar</button>
</div>

<div class="card">
<h3>ElfBar Ice King 40k</h3>
<p>Passion Flash</p>
<p class="price">R$ 140,00</p>
<button onclick="addToCart(140)">Adicionar</button>
</div>

<div class="card">
<h3>Ignite V400 Mix</h3>
<p>Sabores Duplos</p>
<p class="price">R$ 180,00</p>
<button onclick="addToCart(180)">Adicionar</button>
</div>

</div>

<div class="cart">
<span>Total: R$ <span id="total">0</span></span>

<a class="checkout" id="checkout" target="_blank">
Finalizar no WhatsApp (PIX)
</a>
</div>

<script>
let total = 0;

function addToCart(value) {
    total += value;
    document.getElementById("total").innerText = total;
    updateLink();
}

function updateLink() {
    let msg = "Olá! Quero finalizar minha compra. Total: R$ " + total + " (PIX)";
    let phone = "5544991679883"; // COLOQUE SEU NÚMERO AQUI
    document.getElementById("checkout").href =
    "https://wa.me/" + phone + "?text=" + encodeURIComponent(msg);
}
</script>

</body>
</html>
