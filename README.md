<!DOCTYPE html>
<html lang="cs">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Stovka Podyjím 2026</title>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@700&family=Roboto:wght@400;500&display=swap" rel="stylesheet">
<style>
body {
  font-family: 'Roboto', sans-serif;
  margin: 0;
  color: #333;
  line-height: 1.6;
}

/* Hero header s fungujícím obrázkem */
header {
  background: url("https://upload.wikimedia.org/wikipedia/commons/e/ea/Wild_forest_and_river_landscape.jpg") center center / cover no-repeat;
  height: 90vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: white;
  position: relative;
}

header::after {
  content:"";
  position:absolute;
  top:0; left:0;
  width:100%; height:100%;
  background: rgba(0,0,0,0.4);
}

header h1 {
  font-family: 'Montserrat', sans-serif;
  font-size: 3rem;
  margin: 0 20px;
  z-index: 1;
}

header .info {
  font-size: 1.3rem;
  margin: 15px 0;
  z-index: 1;
}

.header-button {
  display: inline-block;
  padding: 15px 35px;
  background: #2f7d32;
  color: white;
  font-weight: bold;
  border-radius: 6px;
  text-decoration: none;
  transition: background 0.3s;
  z-index: 1;
}

.header-button:hover {
  background: #1f5a23;
}

/* Sekce */
section {
  padding: 60px 20px;
  max-width: 1000px;
  margin: auto;
}

/* Karty info */
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(200px,1fr));
  gap: 20px;
  margin-top: 30px;
}

.card {
  background: #f5f5f5;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
  transition: transform 0.3s, box-shadow 0.3s;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0,0,0,0.2);
}

.card strong {
  display: block;
  margin-bottom: 10px;
  font-size: 1.2rem;
}

/* Tlačítko v sekci */
.section-button {
  display: inline-block;
  padding: 12px 25px;
  background: #2f7d32;
  color: white;
  text-decoration: none;
  border-radius: 6px;
  font-weight: bold;
  margin-top: 15px;
  transition: background 0.3s;
}

.section-button:hover {
  background: #1f5a23;
}

/* Footer */
footer {
  background: #111;
  color: white;
  text-align: center;
  padding: 30px;
  margin-top: 40px;
}

/* Responzivita */
@media(max-width:700px){
  header h1 { font-size: 2rem; }
  header .info { font-size: 1rem; }
}
</style>
</head>
<body>

<header>
  <h1>Stovka Podyjím 2026</h1>
  <div class="info">Délka 112 km &nbsp;|&nbsp; Převýšení 3400 m</div>
  <a class="header-button" href="#registrace">Registrace</a>
</header>

<section>
<h2>O závodě</h2>
<p>
Stovka Podyjím je vytrvalostní běžecký a turistický závod vedoucí krásnou krajinou 
národního parku Podyjí. Trasa měří přibližně 112 km a nabízí náročné převýšení 3400 m, 
divokou přírodu a jedinečnou atmosféru.
</p>
</section>

<section>
<h2>Základní informace</h2>
<div class="cards">
  <div class="card">
    <strong>Termín</strong>
    4.–6. září 2026
  </div>
  <div class="card">
    <strong>Start</strong>
    Uherčice
  </div>
  <div class="card">
    <strong>Cíl</strong>
    Znojmo
  </div>
  <div class="card">
    <strong>Startovné</strong>
    500 Kč
  </div>
</div>
</section>

<section>
<h2>Trasa</h2>
<p>
Trasa vede podél řeky Dyje přes lesy, vyhlídky a historická místa oblasti 
Podyjí. Přesná mapa a GPX budou zveřejněny před závodem.
</p>
</section>

<section id="registrace">
<h2>Registrace</h2>
<p>
Registrace bude otevřena brzy.
</p>
<a class="section-button" href="mailto:johny@korýš.cz">Kontaktovat pořadatele</a>
</section>

<footer>
<p>
Stovka Podyjím 2026<br>
kontakt: johny@korýš.cz
</p>
</footer>

</body>
</html>
