<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Broadcast Pro - Oficial</title>

<style>
body {
margin:0;
font-family:Arial;
background:black;
color:white;
text-align:center;
}

/* HEADER */
header {
padding:60px 20px;
}

h1 {
color:gold;
}

/* BOTÓN */
.btn {
display:inline-block;
padding:15px 30px;
background:gold;
color:black;
border-radius:10px;
text-decoration:none;
font-weight:bold;
margin-top:20px;
}

/* SECCIONES */
.section {
padding:40px 20px;
}

/* CARDS */
.card {
background:#111;
margin:15px auto;
padding:20px;
border-radius:12px;
max-width:300px;
}

/* WHATSAPP */
.whatsapp {
position:fixed;
bottom:20px;
right:20px;
background:#25D366;
padding:18px;
border-radius:50%;
font-size:22px;
color:white;
text-decoration:none;
}

/* CONTADOR */
.counter {
color:red;
font-size:22px;
animation: blink 1s infinite;
}

@keyframes blink {
50% {opacity:0;}
}

/* NOTIFICACIONES */
.toast {
position:fixed;
bottom:90px;
left:20px;
background:#111;
padding:12px 18px;
border-radius:10px;
font-size:14px;
opacity:0;
transition:0.5s;
}
</style>

<script>
// CONTADOR DE CUPOS
function contador(){
let cupos = 10;
setInterval(function(){
if(cupos>0){cupos--;}
document.getElementById("cupos").innerText = cupos + " cupos disponibles";
},4000);
}

// NOTIFICACIONES FALSAS
const nombres = ["Carlos", "Laura", "Andrés", "Sofía", "Juan", "Camila"];

function notificaciones(){
setInterval(function(){
let nombre = nombres[Math.floor(Math.random()*nombres.length)];
let toast = document.getElementById("toast");
toast.innerText = nombre + " se acaba de unir 🔥";
toast.style.opacity = 1;

setTimeout(()=>{toast.style.opacity=0;},3000);
},5000);
}
</script>

</head>

<body onload="contador(); notificaciones();">

<header>

<!-- 🔥 PON TU LOGO -->
<img src="logo.png" style="width:150px;">

<h1>AGENCIA BROADCAST PRO</h1>
<p>Gana dinero desde casa</p>

<a class="btn" href="https://wa.me/573143750815?text=Hola+quiero+ser+streamer+oficial">
UNIRME AHORA
</a>

<p class="counter" id="cupos">10 cupos disponibles</p>

</header>

<div class="section">
<h2>🔥 Beneficios</h2>

<div class="card">💰 Pagos mensuales</div>
<div class="card">🚀 Activación inmediata</div>
<div class="card">🎯 PK oficiales</div>
<div class="card">📈 Crecimiento rápido</div>

</div>

<div class="section">
<h2>📊 Tabla de Pagos</h2>

<!-- 🔥 TU TABLA -->
<img src="tabla.jpg" style="width:90%; border-radius:12px;">

</div>

<div class="section">
<h2>💬 Testimonios</h2>

<div class="card">"Ya estoy ganando dinero"</div>
<div class="card">"La agencia sí paga"</div>
<div class="card">"Subí rápido de nivel"</div>

</div>

<div class="section">
<h2>⚠️ Últimos cupos</h2>

<a class="btn" href="https://wa.me/573143750815?text=Quiero+información+urgente">
ESCRIBIR YA
</a>

<p>📞 314 375 0815</p>

</div>

<!-- WHATSAPP -->
<a class="whatsapp" href="https://wa.me/573143750815">💬</a>

<!-- NOTIFICACIONES -->
<div id="toast" class="toast"></div>

</body>
</html>
