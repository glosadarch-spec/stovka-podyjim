<!DOCTYPE html>
<html lang="cs">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Stovka Podyjím 2026</title>

<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@700&family=Roboto:wght@400;500&display=swap" rel="stylesheet">

<style>

body{
margin:0;
font-family:Roboto, sans-serif;
color:#333;
line-height:1.6;
}

header{
background:url("https://images.unsplash.com/photo-1501785888041-af3ef285b470?auto=format&fit=crop&w=2000&q=80") center/cover no-repeat;
height:90vh;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
color:white;
position:relative;
padding:20px;
}

header:after{
content:"";
position:absolute;
top:0;
left:0;
width:100%;
height:100%;
background:rgba(0,0,0,0.45);
}

header h1{
font-family:Montserrat,sans-serif;
font-size:3rem;
margin:0;
z-index:1;
}

header p{
font-size:1.3rem;
margin:15px 0;
z-index:1;
}

.btn{
display:inline-block;
background:#2f7d32;
color:white;
padding:14px 32px;
border-radius:6px;
text-decoration:none;
font-weight:bold;
z-index:1;
}

section{
max-width:1000px;
margin:auto;
padding:60px 20px;
}

.cards{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
gap:20px;
margin-top:30px;
}

.card{
background:#f5f5f5;
padding:25px;
border-radius:10px;
text-align:center;
font-weight:bold;
}

footer{
background:#111;
color:white;
text-align:center;
padding:30px;
}

@media(max-width:700px){
header h1{font-size:2.2rem;}
}

</style>
</head>

<body>

<header>
<h1>Stovka Podyjím 2026</h1>
<p>Přijmi výzvu. 112 km divoké přírody.</p>
<a class="btn" href="#registrace">Chci se přihlásit</a>
</header>

<section>
<h2>Výzva</h2>
<p>
Stovka Podyjím není jen závod. Je to dobrodružství.  
112 kilometrů lesů, údolí a řeky Dyje prověří tvou vytrvalost, hlavu i charakter.  
Připoj se k těm, kteří chtějí zjistit, kam až dokážou dojít.
</p>
</section>

<section>
<h2>Základní informace</h2>

<div class="cards">

<div class="card">
Termín<br>
4.–6. září 2026
</div>

<div class="card">
Start<br>
Uherčice
</div>

<div class="card">
Cíl<br>
Znojmo
</div>

<div class="card">
Startovné<br>
500 Kč
</div>

</div>

</section>

<section>
<h2>Trasa</h2>
<p>
Trasa vede podél řeky Dyje přes hluboké lesy národního parku Podyjí.  
Čekají tě dlouhá údolí, vyhlídky a nekonečné stezky.  
Každý kilometr tě posune blíž k cíli – a možná i k sobě samému.
</p>
</section>

<section id="registrace">
<h2>Registrace</h2>
<p>
Kapacita závodu je omezená. Přidej se k výzvě a buď součástí prvního ročníku.
</p>

<a class="btn" href="mailto:johny@korýš.cz">Kontaktovat pořadatele</a>

</section>

<footer>
Stovka Podyjím 2026<br>
johny@korýš.cz
</footer>

</body>
</html>
