https://upload.wikimedia.org/wikipedia/commons/4/47/River_landscape_nature.jpg
```  [oai_citation:1‡commons.wikimedia.org](https://commons.wikimedia.org/wiki/File%3ARiver_landscape_nature.jpg?utm_source=chatgpt.com)

---

## ✅ Kompletní webový kód s fungujícím obrázkem  
*(můžeš ho dát přímo jako `index.html` na GitHub Pages)*

```html
<!DOCTYPE html>
<html lang="cs">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Stovka Podyjím 2026</title>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@700&family=Roboto:wght@400;500&display=swap" rel="stylesheet">
<style>

/* Základní styl */
body {
  font-family: 'Roboto', sans-serif;
  margin: 0;
  color: #333;
  background: #fff;
  line-height: 1.6;
}

/* Hero header s fungujícím obrázkem (řeka/les) */
header {
  background: url("https://upload.wikimedia.org/wikipedia/commons/4/47/River_landscape_nature.jpg") center center / cover no-repeat;
  height: 90vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  color: white;
  position: relative;
  padding: 0 20px;
}

/* Černá maska přes obrázek pro lepší čitelnost textu */
header::after {
  content:"";
  position:absolute;
  top:0; left:0;
  width:100%; height:100%;
  background: rgba(0,0,0,0.45);
}

/* Nadpis */
header h1 {
  font-family: 'Montserrat', sans-serif;
  font-size: 3rem;
  margin-bottom: 10px;
  z-index: 1;
}

/* Podnadpis s výzvou */
header .sub {
  font-size: 1.4rem;
  margin-bottom: 20px;
  font-weight: bold;
  z-index: 1;
}

/* Info o závodě */
header .info {
  font-size: 1.2rem;
  margin-bottom: 15px;
  z-index: 1;
}

/* Velké tlačítko */
.header-button {
  display: inline-block;
  padding: 15px 35px;
  background: #2f7d32;
  color: white;
  font-weight: bold;
  border-radius: 6px;
  text-decoration: none;
  z-index: 1;
  transition: background 0.3s;
}

.header-button:hover {
  background: #1f5a23;
}

/* Sekce textů */
section {
  padding: 60px 20px;
  max-width: 1000px;
  margin: auto;
}

/* Karty s info */
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(200px,1fr));
  gap: 20px;
  margin-top: 30px;
}

.card {
  background: #f6f6f6;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
  font-weight: bold;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
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

/* Responzivní styl */
@media(max-width:700px){
  header h1 { font-size: 2.4rem; }
  header .info { font-size: 1rem; }
}
</style>
</head>
<body>

<header>
  <h1>Stovka Podyjím 2026</h1>
  <div class="sub">Přijmi největší výzvu svého života!</div>
  <div class="info">112 km divoké přírody &nbsp;|&nbsp; Převýšení 3400 m</div>
  <a class="header-button" href="#registrace">Připoj se teď</a>
</header>

<section>
<h2>Proč se zapojit?</h2>
<p>
Stovka Podyjím není obyčejný závod — je to dobrodružství, které tě provede malebnými údolími,
lesy a úchvatnými výhledy. Překonej své hranice, poznej své limity a užij si jedinečnou
atmosféru nemilosrdné trasy.
</p>
</section>

<section>
<h2>Základní informace</h2>
<div class="cards">
  <div class="card">Termín<br><strong>4.–6. září 2026</strong></div>
  <div class="card">Start<br><strong>Uherčice</strong></div>
  <div class="card">Cíl<br><strong>Znojmo</strong></div>
  <div class="card">Startovné<br><strong>500 Kč</strong></div>
</div>
</section>

<section>
<h2>Trasa a výzva</h2>
<p>
Trasa vede podél řek a starých lesů, přes historické stezky a vyhlídky, které odmění ty,
kteří vydrží. Připrav se na bezprecedentní zážitek — běh nebo trek, který změní tvůj pohled
na výzvy a vytrvalost.
</p>
</section>

<section id="registrace">
<h2>Registrace</h2>
<p>
Kapacita je omezená. Nečekej — vstupenky mizí! Přijmi výzvu a staň se součástí legendy.
</p>
<a class="section-button" href="mailto:johny@korýš.cz">Kontaktovat pořadatele</a>
</section>

<footer>
<p>Stovka Podyjím 2026 – Tvoje největší výzva.</p>
<p>kontakt: johny@korýš.cz</p>
</footer>

</body>
</html>
