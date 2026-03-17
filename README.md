<!DOCTYPE html>
<html lang="cs">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Stovka Podyjím 2026</title>
<style>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  line-height: 1.6;
  color: #333;
}

/* Header s obrázkem Dyje */
header {
  background: url("https://upload.wikimedia.org/wikipedia/commons/5/52/The_Dyje_river_%28Thaya_in_German%29_in_National_Park_Podyj%C3%AD.jpg") center center / cover no-repeat;
  height: 75vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: white;
  text-shadow: 2px 2px 6px rgba(0,0,0,0.6);
}

header h1 {
  font-size: 52px;
  margin-bottom: 10px;
  font-weight: bold;
}

header .info {
  font-size: 22px;
  margin-bottom: 15px;
}

.button {
  display: inline-block;
  padding: 12px 25px;
  background: #2f7d32;
  color: white;
  text-decoration: none;
  border-radius: 6px;
  font-weight: bold;
  transition: background 0.3s;
}

.button:hover {
  background: #1f5a23;
}

section {
  padding: 60px 20px;
  max-width: 900px;
  margin: auto;
}

.info {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
}

footer {
  background: #111;
  color: white;
  text-align: center;
  padding: 30px;
  margin-top: 40px;
}

/* Responzivita pro mobil */
@media(max-width:700px){
  header h1 { font-size: 36px; }
  header .info { font-size: 16px; }
  .button { padding: 10px 20px; }
  .info { grid-template-columns: 1fr; }
}
</style>
</head>

<body>

<header>
  <h1>Stovka Podyjím 2026</h1>
  <div class="info">Délka 112 km &nbsp;|&nbsp; Převýšení 3400 m</div>
  <a class="button" href="#registrace">Registrace</a>
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
<div class="info">
  <div><strong>Termín:</strong><br>4.–6. září 2026</div>
  <div><strong>Start:</strong><br>Uherčice</div>
  <div><strong>Cíl:</strong><br>Znojmo</div>
  <div><strong>Startovné:</strong><br>500 Kč</div>
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
<a class="button" href="mailto:johny@korýš.cz">Kontaktovat pořadatele</a>
</section>

<footer>
<p>
Stovka Podyjím 2026<br>
kontakt: johny@korýš.cz
</p>
</footer>

</body>
</html>
