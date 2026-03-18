<!DOCTYPE html>
<html lang="cs">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Stovka Podyjím 2026</title>
<meta name="description" content="Stovka Podyjím 2026 – 112 km divoké přírody, lesů a stezek mezi Uherčicemi a Znojmem.">

<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@600;700;800&family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">

<style>
:root{
  --bg:#0e0f11;
  --bg2:#15171a;
  --card:#1b1e22;
  --card2:#20242a;
  --text:#f3f4f6;
  --muted:#c5c8ce;
  --muted2:#9ba3af;
  --accent:#d5a44a;
  --accent-dark:#b9872d;
  --line:rgba(255,255,255,0.08);
  --max:1200px;
  --radius:18px;
  --shadow:0 18px 40px rgba(0,0,0,0.35);
}

*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  margin:0;
  background:var(--bg);
  color:var(--text);
  font-family:Roboto, sans-serif;
  line-height:1.6;
}

a{color:inherit;text-decoration:none}
img{max-width:100%;display:block}

.container{
  width:min(var(--max), calc(100% - 40px));
  margin:auto;
}

.topbar{
  position:fixed;
  top:0;
  left:0;
  width:100%;
  z-index:50;
  background:linear-gradient(to bottom, rgba(0,0,0,0.55), rgba(0,0,0,0.15));
}

.nav{
  display:flex;
  align-items:center;
  justify-content:space-between;
  min-height:82px;
  gap:20px;
}

.logo{
  font-family:Montserrat, sans-serif;
  font-weight:800;
  letter-spacing:0.08em;
  text-transform:uppercase;
  font-size:1rem;
}

.menu{
  display:flex;
  gap:26px;
  flex-wrap:wrap;
}

.menu a{
  font-size:0.95rem;
  color:rgba(255,255,255,0.92);
  font-weight:500;
}

.menu a:hover{
  color:var(--accent);
}

.nav-btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  padding:12px 18px;
  border:1px solid rgba(255,255,255,0.22);
  border-radius:999px;
  color:#fff;
  font-weight:700;
  transition:.2s ease;
}

.nav-btn:hover{
  background:rgba(255,255,255,0.08);
  border-color:rgba(255,255,255,0.4);
}

.hero{
  min-height:100vh;
  position:relative;
  display:flex;
  align-items:flex-end;
  padding:140px 0 70px;
  background:
    linear-gradient(to bottom, rgba(0,0,0,0.25), rgba(0,0,0,0.45) 38%, rgba(0,0,0,0.82) 100%),
    url("./images/podyji-hero.png") center center / cover no-repeat;
}

.hero::after{
  content:"";
  position:absolute;
  inset:0;
  background:
    radial-gradient(circle at 20% 25%, rgba(213,164,74,0.14), transparent 30%),
    radial-gradient(circle at 80% 20%, rgba(255,255,255,0.08), transparent 22%);
  pointer-events:none;
}

.hero-inner{
  position:relative;
  z-index:2;
  max-width:860px;
}

.kicker{
  display:inline-block;
  margin-bottom:18px;
  padding:8px 14px;
  border:1px solid rgba(255,255,255,0.18);
  background:rgba(255,255,255,0.08);
  border-radius:999px;
  color:rgba(255,255,255,0.92);
  font-size:0.9rem;
  letter-spacing:0.04em;
}

.hero h1{
  margin:0 0 18px;
  font-family:Montserrat, sans-serif;
  font-size:clamp(3rem, 8vw, 6rem);
  line-height:0.95;
  font-weight:800;
  text-transform:uppercase;
  letter-spacing:0.02em;
}

.hero p{
  margin:0 0 28px;
  max-width:680px;
  font-size:1.12rem;
  color:rgba(255,255,255,0.9);
}

.hero-actions{
  display:flex;
  flex-wrap:wrap;
  gap:14px;
  margin-bottom:42px;
}

.btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  padding:15px 28px;
  border-radius:999px;
  font-weight:700;
  transition:.2s ease;
}

.btn-primary{
  background:var(--accent);
  color:#111;
}

.btn-primary:hover{
  background:#e0b25a;
  transform:translateY(-1px);
}

.btn-secondary{
  border:1px solid rgba(255,255,255,0.24);
  color:#fff;
  background:rgba(255,255,255,0.06);
}

.btn-secondary:hover{
  background:rgba(255,255,255,0.12);
}

.quick-stats{
  display:grid;
  grid-template-columns:repeat(4, 1fr);
  gap:16px;
}

.stat{
  background:rgba(23,25,28,0.78);
  border:1px solid rgba(255,255,255,0.08);
  backdrop-filter:blur(5px);
  border-radius:16px;
  padding:18px 18px 16px;
  box-shadow:var(--shadow);
}

.stat .label{
  display:block;
  color:var(--muted2);
  font-size:0.85rem;
  text-transform:uppercase;
  letter-spacing:0.08em;
  margin-bottom:8px;
}

.stat strong{
  font-size:1.2rem;
  color:#fff;
}

main{
  position:relative;
  z-index:2;
}

section{
  padding:84px 0;
}

.section-dark{
  background:var(--bg);
}

.section-soft{
  background:var(--bg2);
}

.section-head{
  max-width:720px;
  margin-bottom:34px;
}

.section-head .overline{
  color:var(--accent);
  text-transform:uppercase;
  letter-spacing:0.08em;
  font-size:0.85rem;
  font-weight:700;
  margin-bottom:10px;
}

.section-head h2{
  margin:0 0 12px;
  font-family:Montserrat, sans-serif;
  font-size:2.4rem;
  line-height:1.1;
  text-transform:uppercase;
}

.section-head p{
  margin:0;
  color:var(--muted);
}

.grid-2{
  display:grid;
  grid-template-columns:1.1fr 0.9fr;
  gap:28px;
}

.panel{
  background:var(--card);
  border:1px solid var(--line);
  border-radius:var(--radius);
  padding:28px;
  box-shadow:var(--shadow);
}

.panel p:last-child{
  margin-bottom:0;
}

.race-cards{
  display:grid;
  grid-template-columns:repeat(4, 1fr);
  gap:18px;
}

.race-card{
  background:linear-gradient(180deg, var(--card2), var(--card));
  border:1px solid var(--line);
  border-radius:18px;
  padding:22px;
  box-shadow:var(--shadow);
  transition:.2s ease;
}

.race-card:hover{
  transform:translateY(-4px);
  border-color:rgba(213,164,74,0.35);
}

.race-card .distance{
  font-family:Montserrat, sans-serif;
  font-size:2rem;
  line-height:1;
  color:var(--accent);
  margin-bottom:12px;
}

.race-card h3{
  margin:0 0 10px;
  font-size:1rem;
  text-transform:uppercase;
  letter-spacing:0.04em;
}

.race-card ul{
  list-style:none;
  padding:0;
  margin:0;
}

.race-card li{
  padding:7px 0;
  border-bottom:1px solid var(--line);
  color:var(--muted);
  font-size:0.95rem;
}

.race-card li:last-child{
  border-bottom:none;
}

.info-list{
  display:grid;
  gap:14px;
}

.info-item{
  display:flex;
  gap:14px;
  align-items:flex-start;
  padding:14px 0;
  border-bottom:1px solid var(--line);
}

.info-item:last-child{
  border-bottom:none;
}

.info-icon{
  width:38px;
  height:38px;
  border-radius:50%;
  display:flex;
  align-items:center;
  justify-content:center;
  background:rgba(213,164,74,0.12);
  color:var(--accent);
  font-weight:800;
  flex-shrink:0;
}

.info-item strong{
  display:block;
  margin-bottom:4px;
  color:#fff;
}

.cta-box{
  background:
    linear-gradient(135deg, rgba(213,164,74,0.15), rgba(213,164,74,0.05)),
    var(--card);
  border:1px solid rgba(213,164,74,0.2);
  border-radius:24px;
  padding:34px;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:22px;
  flex-wrap:wrap;
  box-shadow:var(--shadow);
}

.cta-box h2{
  margin:0 0 10px;
  font-family:Montserrat, sans-serif;
  text-transform:uppercase;
  font-size:2rem;
  line-height:1.05;
}

.cta-box p{
  margin:0;
  color:var(--muted);
}

footer{
  padding:36px 0;
  border-top:1px solid var(--line);
  background:#0b0c0e;
}

.footer-wrap{
  display:flex;
  justify-content:space-between;
  gap:16px;
  flex-wrap:wrap;
  color:var(--muted2);
  font-size:0.95rem;
}

@media (max-width: 1024px){
  .quick-stats,
  .race-cards{
    grid-template-columns:repeat(2,1fr);
  }

  .grid-2{
    grid-template-columns:1fr;
  }
}

@media (max-width: 760px){
  .menu{
    display:none;
  }

  .hero{
    min-height:auto;
    padding:130px 0 50px;
  }

  .hero h1{
    font-size:clamp(2.5rem, 12vw, 4rem);
  }

  .quick-stats,
  .race-cards{
    grid-template-columns:1fr;
  }

  .section-head h2{
    font-size:1.9rem;
  }
}
</style>
</head>
<body>

<header class="topbar">
  <div class="container nav">
    <div class="logo">Stovka Podyjím</div>

    <nav class="menu">
      <a href="#zavod">Závod</a>
      <a href="#trasy">Trasy</a>
      <a href="#info">Informace</a>
      <a href="#registrace">Registrace</a>
      <a href="#kontakt">Kontakt</a>
    </nav>

    <a class="nav-btn" href="#registrace">Přihlásit se</a>
  </div>
</header>

<section class="hero">
  <div class="container hero-inner">
    <div class="kicker">4.–6. září 2026 • Uherčice – Znojmo</div>
    <h1>112 km<br>divokým Podyjím</h1>
    <p>
      Ultra výzva napříč jedním z nejkrásnějších koutů jižní Moravy. Lesy, řeka Dyje,
      hluboká údolí a dlouhý den, který prověří nohy i hlavu.
    </p>

    <div class="hero-actions">
      <a class="btn btn-primary" href="#registrace">Chci na start</a>
      <a class="btn btn-secondary" href="#trasy">Prozkoumat trasu</a>
    </div>

    <div class="quick-stats">
      <div class="stat">
        <span class="label">Délka</span>
        <strong>112 km</strong>
      </div>
      <div class="stat">
        <span class="label">Termín</span>
        <strong>4.–6. 9. 2026</strong>
      </div>
      <div class="stat">
        <span class="label">Start</span>
        <strong>Uherčice</strong>
      </div>
      <div class="stat">
        <span class="label">Startovné</span>
        <strong>500 Kč</strong>
      </div>
    </div>
  </div>
</section>

<main>
  <section id="zavod" class="section-dark">
    <div class="container">
      <div class="section-head">
        <div class="overline">O závodě</div>
        <h2>Ne jen závod. Výprava krajinou.</h2>
        <p>
          Stovka Podyjím má být syrová, krásná a poctivá ultra akce. Míň pozlátka,
          víc terénu, atmosféry a zážitku, na který se nezapomíná.
        </p>
      </div>

      <div class="grid-2">
        <div class="panel">
          <p>
            Trať vede podél Dyje, přes lesy, vyhlídky a dlouhé pasáže, kde si člověk
            musí tempo i energii hlídat sám. První ročník chceme postavit na silném
            místě, dobré organizaci a autentické atmosféře.
          </p>
          <p>
            Nejde jen o čas v cíli. Jde o to, co všechno musíš zvládnout po cestě.
          </p>
        </div>

        <div class="panel">
          <div class="info-list">
            <div class="info-item">
              <div class="info-icon">1</div>
              <div>
                <strong>Divoká příroda</strong>
                Lesy, meandry Dyje a terén, který má vlastní charakter.
              </div>
            </div>

            <div class="info-item">
              <div class="info-icon">2</div>
              <div>
                <strong>Ultra formát</strong>
                Dlouhá trať pro lidi, kteří mají rádi skutečnou výzvu.
              </div>
            </div>

            <div class="info-item">
              <div class="info-icon">3</div>
              <div>
                <strong>První ročník</strong>
                Možnost být u zrodu nové tradice.
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="trasy" class="section-soft">
    <div class="container">
      <div class="section-head">
        <div class="overline">Trasy</div>
        <h2>Hlavní závodní karta</h2>
        <p>
          Stylově podobně jako ultra závody – výrazná karta, rychle čitelné parametry,
          všechno důležité na první pohled.
        </p>
      </div>

      <div class="race-cards">
        <div class="race-card">
          <div class="distance">112 km</div>
          <h3>Stovka Podyjím</h3>
          <ul>
            <li>Start: Uherčice</li>
            <li>Cíl: Znojmo</li>
            <li>Termín: 4.–6. září 2026</li>
            <li>Startovné: 500 Kč</li>
          </ul>
        </div>

        <div class="race-card">
          <div class="distance">?</div>
          <h3>Převýšení</h3>
          <ul>
            <li>Doplnit po finalizaci GPX</li>
            <li>Může být výrazný argument</li>
            <li>Patří sem i limit závodu</li>
            <li>Případně povinná výbava</li>
          </ul>
        </div>

        <div class="race-card">
          <div class="distance">MAPA</div>
          <h3>Trasa</h3>
          <ul>
            <li>Vložit GPX / iframe mapu</li>
            <li>Profil tratě</li>
            <li>Občerstvovací stanice</li>
            <li>Klíčové body tratě</li>
          </ul>
        </div>

        <div class="race-card">
          <div class="distance">FAQ</div>
          <h3>Prakticky</h3>
          <ul>
            <li>Registrace</li>
            <li>Pravidla</li>
            <li>Doprava na start</li>
            <li>Zázemí v cíli</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <section id="info" class="section-dark">
    <div class="container">
      <div class="section-head">
        <div class="overline">Informace</div>
        <h2>Co doplnit jako další krok</h2>
        <p>
          Tady už je největší přidaná hodnota proti současné jednoduché verzi webu.
        </p>
      </div>

      <div class="grid-2">
        <div class="panel">
          <div class="info-list">
            <div class="info-item">
              <div class="info-icon">✓</div>
              <div>
                <strong>Mapa a profil tratě</strong>
                Bez toho bude web působit stále spíš jako teaser.
              </div>
            </div>

            <div class="info-item">
              <div class="info-icon">✓</div>
              <div>
                <strong>Pravidla a limity</strong>
                Přesně tohle běžci hledají mezi prvními.
              </div>
            </div>

            <div class="info-item">
              <div class="info-icon">✓</div>
              <div>
                <strong>Fotky z Podyjí</strong>
                Udělají identitu závodu víc než jakýkoli text.
              </div>
            </div>

            <div class="info-item">
              <div class="info-icon">✓</div>
              <div>
                <strong>Reálná registrace</strong>
                Ideálně formulář nebo odkaz na přihlášky místo samotného mailu.
              </div>
            </div>
          </div>
        </div>

        <div class="panel">
          <p>
            Vizuálně bych držel tmavé pozadí, zlatý akcent a velké fotky přírody.
            To bude působit mnohem víc „ultra race“ než světlé klasické sekce.
          </p>
          <p>
            Když chceš být blíž stylu těch polských stránek, důležité je hlavně:
            velká hero fotka, tmavá atmosféra, závodní karty a méně textu v horní části.
          </p>
        </div>
      </div>
    </div>
  </section>

  <section id="registrace" class="section-soft">
    <div class="container">
      <div class="cta-box">
        <div>
          <h2>Připravený postavit se na start?</h2>
          <p>
            Kapacita prvního ročníku bude omezená. Přidej se včas.
          </p>
        </div>

        <a class="btn btn-primary" href="mailto:johny@korys.cz?subject=Stovka%20Podyj%C3%ADm%202026%20-%20registrace">
          Kontaktovat pořadatele
        </a>
      </div>
    </div>
  </section>
</main>

<footer id="kontakt">
  <div class="container footer-wrap">
    <div>Stovka Podyjím 2026 • Uherčice – Znojmo</div>
    <div>Kontakt: johny@korys.cz</div>
  </div>
</footer>

</body>
</html>
