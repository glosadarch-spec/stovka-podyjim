<!DOCTYPE html>
<html lang="cs">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>STOVKA PODYJÍM</title>
  <meta
    name="description"
    content="STOVKA PODYJÍM – XI. ročník. Trasy 160 km, 112 km a 60 km. Další informace koncem jara, přihlašování v létě."
  />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=Montserrat:wght@600;700;800&family=Roboto:wght@400;500;700&display=swap"
    rel="stylesheet"
  />

  <style>
    :root{
      --bg:#0d0f12;
      --bg-soft:#15191e;
      --bg-card:#1b2026;
      --bg-card-2:#222831;
      --text:#f3f4f6;
      --text-soft:#c8cdd5;
      --muted:#95a0ad;
      --accent:#d5a44a;
      --accent-dark:#b8862d;
      --line:rgba(255,255,255,0.09);
      --white:#ffffff;
      --shadow:0 20px 45px rgba(0,0,0,0.32);
      --radius:20px;
      --max:1220px;
    }

    *{
      box-sizing:border-box;
    }

    html{
      scroll-behavior:smooth;
    }

    body{
      margin:0;
      background:var(--bg);
      color:var(--text);
      font-family:Roboto, sans-serif;
      line-height:1.6;
    }

    img{
      max-width:100%;
      display:block;
    }

    a{
      color:inherit;
      text-decoration:none;
    }

    .container{
      width:min(var(--max), calc(100% - 40px));
      margin:auto;
    }

    .topbar{
      position:fixed;
      inset:0 0 auto 0;
      z-index:50;
      background:linear-gradient(to bottom, rgba(0,0,0,0.62), rgba(0,0,0,0.18));
    }

    .nav{
      min-height:84px;
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:24px;
    }

    .logo{
      font-family:Montserrat, sans-serif;
      font-size:1.05rem;
      font-weight:800;
      letter-spacing:0.08em;
      text-transform:uppercase;
      color:var(--white);
      white-space:nowrap;
    }

    .menu{
      display:flex;
      align-items:center;
      gap:26px;
      flex-wrap:wrap;
    }

    .menu a{
      color:rgba(255,255,255,0.92);
      font-weight:500;
      font-size:0.95rem;
    }

    .menu a:hover{
      color:var(--accent);
    }

    .nav-btn{
      display:inline-flex;
      align-items:center;
      justify-content:center;
      padding:12px 18px;
      border-radius:999px;
      border:1px solid rgba(255,255,255,0.22);
      background:rgba(255,255,255,0.06);
      color:#fff;
      font-weight:700;
      transition:0.2s ease;
    }

    .nav-btn:hover{
      background:rgba(255,255,255,0.14);
      border-color:rgba(255,255,255,0.35);
    }

    .hero{
      position:relative;
      min-height:100vh;
      display:flex;
      align-items:flex-end;
      padding:150px 0 78px;
      background:
        linear-gradient(to bottom, rgba(0,0,0,0.22), rgba(0,0,0,0.42) 38%, rgba(0,0,0,0.84) 100%),
        url("./podyji.jpg") center center / cover no-repeat;
      overflow:hidden;
    }

    .hero::before{
      content:"";
      position:absolute;
      inset:0;
      background:
        radial-gradient(circle at 18% 24%, rgba(213,164,74,0.14), transparent 28%),
        radial-gradient(circle at 84% 20%, rgba(255,255,255,0.08), transparent 22%);
      pointer-events:none;
    }

    .hero-inner{
      position:relative;
      z-index:1;
      max-width:900px;
    }

    .hero-kicker{
      display:inline-block;
      margin-bottom:18px;
      padding:8px 14px;
      border-radius:999px;
      border:1px solid rgba(255,255,255,0.18);
      background:rgba(255,255,255,0.09);
      color:rgba(255,255,255,0.95);
      font-size:0.92rem;
      letter-spacing:0.04em;
    }

    .hero h1{
      margin:0 0 18px;
      font-family:Montserrat, sans-serif;
      font-size:clamp(2.9rem, 8vw, 6rem);
      line-height:0.94;
      font-weight:800;
      letter-spacing:0.02em;
      text-transform:uppercase;
    }

    .hero p{
      margin:0 0 30px;
      max-width:720px;
      color:rgba(255,255,255,0.92);
      font-size:1.12rem;
    }

    .hero-actions{
      display:flex;
      gap:14px;
      flex-wrap:wrap;
      margin-bottom:42px;
    }

    .btn{
      display:inline-flex;
      align-items:center;
      justify-content:center;
      padding:15px 28px;
      border-radius:999px;
      font-weight:700;
      transition:0.2s ease;
      cursor:pointer;
    }

    .btn-primary{
      background:var(--accent);
      color:#111;
    }

    .btn-primary:hover{
      background:#e0b25b;
      transform:translateY(-1px);
    }

    .btn-secondary{
      background:rgba(255,255,255,0.08);
      border:1px solid rgba(255,255,255,0.20);
      color:#fff;
    }

    .btn-secondary:hover{
      background:rgba(255,255,255,0.14);
    }

    .hero-stats{
      display:grid;
      grid-template-columns:repeat(4, 1fr);
      gap:16px;
      max-width:980px;
    }

    .stat{
      background:rgba(24,28,33,0.78);
      border:1px solid rgba(255,255,255,0.09);
      backdrop-filter:blur(5px);
      border-radius:16px;
      padding:18px 18px 16px;
      box-shadow:var(--shadow);
    }

    .stat .label{
      display:block;
      color:var(--muted);
      text-transform:uppercase;
      font-size:0.8rem;
      letter-spacing:0.08em;
      margin-bottom:8px;
    }

    .stat strong{
      font-size:1.2rem;
      color:#fff;
    }

    main{
      position:relative;
      z-index:1;
    }

    section{
      padding:90px 0;
    }

    .section-dark{
      background:var(--bg);
    }

    .section-soft{
      background:var(--bg-soft);
    }

    .section-head{
      max-width:760px;
      margin-bottom:36px;
    }

    .section-head .overline{
      margin-bottom:10px;
      color:var(--accent);
      text-transform:uppercase;
      letter-spacing:0.08em;
      font-size:0.84rem;
      font-weight:700;
    }

    .section-head h2{
      margin:0 0 12px;
      font-family:Montserrat, sans-serif;
      font-size:2.35rem;
      line-height:1.08;
      text-transform:uppercase;
    }

    .section-head p{
      margin:0;
      color:var(--text-soft);
    }

    .cards-3{
      display:grid;
      grid-template-columns:repeat(3, 1fr);
      gap:22px;
    }

    .track-card{
      background:linear-gradient(180deg, var(--bg-card-2), var(--bg-card));
      border:1px solid var(--line);
      border-radius:20px;
      padding:26px;
      box-shadow:var(--shadow);
      transition:0.2s ease;
    }

    .track-card:hover{
      transform:translateY(-4px);
      border-color:rgba(213,164,74,0.35);
    }

    .track-distance{
      margin-bottom:12px;
      font-family:Montserrat, sans-serif;
      font-size:2.2rem;
      line-height:1;
      color:var(--accent);
    }

    .track-card h3{
      margin:0 0 10px;
      font-size:1.02rem;
      text-transform:uppercase;
      letter-spacing:0.04em;
    }

    .track-card p{
      margin:0 0 14px;
      color:var(--text-soft);
    }

    .track-meta{
      display:grid;
      gap:8px;
      color:var(--muted);
      font-size:0.95rem;
    }

    .grid-2{
      display:grid;
      grid-template-columns:1.1fr 0.9fr;
      gap:28px;
    }

    .panel{
      background:var(--bg-card);
      border:1px solid var(--line);
      border-radius:var(--radius);
      padding:28px;
      box-shadow:var(--shadow);
    }

    .panel p:last-child{
      margin-bottom:0;
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
      width:40px;
      height:40px;
      border-radius:50%;
      flex-shrink:0;
      display:flex;
      align-items:center;
      justify-content:center;
      background:rgba(213,164,74,0.14);
      color:var(--accent);
      font-weight:800;
    }

    .info-item strong{
      display:block;
      margin-bottom:4px;
      color:#fff;
    }

    .notice{
      background:linear-gradient(135deg, rgba(213,164,74,0.12), rgba(213,164,74,0.04));
      border:1px solid rgba(213,164,74,0.20);
      border-radius:18px;
      padding:20px 22px;
      color:var(--text);
    }

    .notice strong{
      color:#fff;
    }

    .fee-grid{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:22px;
    }

    .fee-card{
      background:var(--bg-card);
      border:1px solid var(--line);
      border-radius:18px;
      padding:24px;
      box-shadow:var(--shadow);
    }

    .fee-card h3{
      margin:0 0 14px;
      font-family:Montserrat, sans-serif;
      text-transform:uppercase;
      font-size:1.1rem;
    }

    .fee-card ul{
      margin:0;
      padding-left:18px;
      color:var(--text-soft);
    }

    .fee-card li + li{
      margin-top:10px;
    }

    .rules{
      display:grid;
      gap:16px;
    }

    details.rule{
      background:var(--bg-card);
      border:1px solid var(--line);
      border-radius:16px;
      padding:0;
      box-shadow:var(--shadow);
      overflow:hidden;
    }

    details.rule summary{
      list-style:none;
      cursor:pointer;
      padding:22px 24px;
      font-weight:700;
      font-size:1.02rem;
      position:relative;
    }

    details.rule summary::-webkit-details-marker{
      display:none;
    }

    details.rule summary::after{
      content:"+";
      position:absolute;
      right:22px;
      top:50%;
      transform:translateY(-50%);
      color:var(--accent);
      font-size:1.4rem;
      line-height:1;
    }

    details.rule[open] summary::after{
      content:"–";
    }

    .rule-content{
      padding:0 24px 24px;
      color:var(--text-soft);
    }

    .rule-content ul{
      padding-left:18px;
      margin:0;
    }

    .rule-content li + li{
      margin-top:10px;
    }

    .cta-box{
      background:
        linear-gradient(135deg, rgba(213,164,74,0.15), rgba(213,164,74,0.05)),
        var(--bg-card);
      border:1px solid rgba(213,164,74,0.22);
      border-radius:24px;
      padding:36px;
      display:flex;
      justify-content:space-between;
      align-items:center;
      gap:24px;
      flex-wrap:wrap;
      box-shadow:var(--shadow);
    }

    .cta-box h2{
      margin:0 0 10px;
      font-family:Montserrat, sans-serif;
      font-size:2rem;
      line-height:1.05;
      text-transform:uppercase;
    }

    .cta-box p{
      margin:0;
      color:var(--text-soft);
      max-width:700px;
    }

    .contact-grid{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:22px;
    }

    .contact-card{
      background:var(--bg-card);
      border:1px solid var(--line);
      border-radius:18px;
      padding:24px;
      box-shadow:var(--shadow);
    }

    .contact-card h3{
      margin:0 0 12px;
      font-family:Montserrat, sans-serif;
      text-transform:uppercase;
      font-size:1.05rem;
    }

    .contact-main{
      font-size:1.45rem;
      font-weight:700;
      color:#fff;
    }

    .muted{
      color:var(--muted);
    }

    footer{
      padding:38px 0;
      background:#090b0d;
      border-top:1px solid var(--line);
    }

    .footer-wrap{
      display:flex;
      justify-content:space-between;
      gap:18px;
      flex-wrap:wrap;
      color:var(--muted);
      font-size:0.95rem;
    }

    @media (max-width: 1100px){
      .hero-stats,
      .cards-3,
      .fee-grid,
      .contact-grid{
        grid-template-columns:repeat(2, 1fr);
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
        padding:130px 0 54px;
      }

      .hero h1{
        font-size:clamp(2.4rem, 12vw, 4rem);
      }

      .hero-stats,
      .cards-3,
      .fee-grid,
      .contact-grid{
        grid-template-columns:1fr;
      }

      section{
        padding:74px 0;
      }

      .section-head h2{
        font-size:1.9rem;
      }

      .cta-box{
        padding:28px;
      }

      .cta-box h2{
        font-size:1.65rem;
      }
    }
  </style>
</head>
<body>

  <header class="topbar">
    <div class="container nav">
      <a href="#top" class="logo">STOVKA PODYJÍM</a>

      <nav class="menu">
        <a href="#zavod">Závod</a>
        <a href="#trasy">Trasy</a>
        <a href="#startovne">Startovné</a>
        <a href="#pravidla">Pravidla</a>
        <a href="#kontakt">Kontakt</a>
      </nav>

      <a class="nav-btn" href="#registrace">Aktuální info</a>
    </div>
  </header>

  <section class="hero" id="top">
    <div class="container hero-inner">
      <div class="hero-kicker">XI. ročník • 160 km • 112 km • 60 km</div>
      <h1>STOVKA<br>PODYJÍM</h1>
      <p>
        Dálkový pochod a ultra výzva v krajině Podyjí. Lesy, řeka Dyje, hluboká údolí
        a trasy, které prověří vytrvalost, hlavu i charakter.
      </p>

      <div class="hero-actions">
        <a class="btn btn-primary" href="#trasy">Prozkoumat trasy</a>
        <a class="btn btn-secondary" href="#startovne">Startovné a podmínky</a>
      </div>

      <div class="hero-stats">
        <div class="stat">
          <span class="label">Ročník</span>
          <strong>XI. ročník</strong>
        </div>
        <div class="stat">
          <span class="label">Trasy</span>
          <strong>160 km / 112 km / 60 km</strong>
        </div>
        <div class="stat">
          <span class="label">Další info</span>
          <strong>Koncem jara</strong>
        </div>
        <div class="stat">
          <span class="label">Přihlášky</span>
          <strong>Spuštění v létě</strong>
        </div>
      </div>
    </div>
  </section>

  <main>
    <section id="zavod" class="section-dark">
      <div class="container">
        <div class="section-head">
          <div class="overline">O akci</div>
          <h2>Poctivá výzva v jednom z nejkrásnějších koutů jižní Moravy</h2>
          <p>
            STOVKA PODYJÍM staví na dlouhé trase, silné krajině a atmosféře, kterou nejde
            nahradit. Méně pozlátka, více skutečného pohybu, terénu a zážitku.
          </p>
        </div>

        <div class="grid-2">
          <div class="panel">
            <p>
              Závod je určen pro účastníky, kteří mají rádi dálkové pochody, vytrvalostní
              akce a silný kontakt s krajinou. Podyjí umí být nádherné i nekompromisní.
              Právě v tom je jeho kouzlo.
            </p>
            <p>
              Další informace k novému ročníku budou zveřejněny koncem jara. Přihlašování
              na trasy bude spuštěno v létě. Kapacita je omezená.
            </p>
          </div>

          <div class="panel">
            <div class="info-list">
              <div class="info-item">
                <div class="info-icon">1</div>
                <div>
                  <strong>Tři trasy</strong>
                  Na výběr bude 160 km, 112 km a 60 km.
                </div>
              </div>

              <div class="info-item">
                <div class="info-icon">2</div>
                <div>
                  <strong>Silná krajina</strong>
                  Dyje, lesy, údolí, vyhlídky a dlouhé pasáže bez zbytečných kulis.
                </div>
              </div>

              <div class="info-item">
                <div class="info-icon">3</div>
                <div>
                  <strong>Omezená kapacita</strong>
                  Míst nebude neomezeně, vyplatí se sledovat spuštění registrací.
                </div>
              </div>

              <div class="info-item">
                <div class="info-icon">4</div>
                <div>
                  <strong>XI. ročník</strong>
                  Zavedená akce s tradicí, ne jednorázový pokus.
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
          <h2>Tři varianty, jedna krajina</h2>
          <p>
            Přesné detaily k jednotlivým trasám budou doplněny později. Základní členění
            ročníku už je ale dané.
          </p>
        </div>

        <div class="cards-3">
          <article class="track-card">
            <div class="track-distance">160 km</div>
            <h3>Nejdelší výzva</h3>
            <p>
              Trasa pro nejvytrvalejší účastníky, kteří chtějí maximum kilometrů i času v terénu.
            </p>
            <div class="track-meta">
              <div>• Ultra formát</div>
              <div>• Detailní informace později</div>
              <div>• Registrace v létě</div>
            </div>
          </article>

          <article class="track-card">
            <div class="track-distance">112 km</div>
            <h3>Klasická Stovka</h3>
            <p>
              Hlavní formát akce, tradiční dálková výzva s kompletním servisním zázemím.
            </p>
            <div class="track-meta">
              <div>• Hlavní trať akce</div>
              <div>• Startovné viz níže</div>
              <div>• Omezená kapacita</div>
            </div>
          </article>

          <article class="track-card">
            <div class="track-distance">60 km</div>
            <h3>Šedesátka</h3>
            <p>
              Kratší varianta pro ty, kteří chtějí silný zážitek v Podyjí, ale neplánují nejdelší trať.
            </p>
            <div class="track-meta">
              <div>• Samostatná pravidla</div>
              <div>• Startovné viz níže</div>
              <div>• Registrace v létě</div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="registrace" class="section-dark">
      <div class="container">
        <div class="cta-box">
          <div>
            <h2>Další informace koncem jara, přihlášky v létě</h2>
            <p>
              Sleduj web kvůli zveřejnění detailů k trasám, organizačním informacím a spuštění
              registrací. Kapacita akce je omezená.
            </p>
          </div>

          <a class="btn btn-primary" href="#kontakt">Kontakt na organizátory</a>
        </div>
      </div>
    </section>

    <section id="startovne" class="section-soft">
      <div class="container">
        <div class="section-head">
          <div class="overline">Startovné</div>
          <h2>Poplatky a platební podmínky</h2>
          <p>
            Níže je přehled startovného a základních pravidel platby. Text jsem rozdělil do
            čitelnější podoby pro web.
          </p>
        </div>

        <div class="notice" style="margin-bottom:22px;">
          <strong>Aktualizováno 1. 8. 2025</strong><br>
          V ceně je mimo jiné občerstvení a voda na kontrolních stanovištích na trase,
          doprava ze Znojma na start v Uherčicích a možnost noclehu v cíli.
          <br><br>
          <strong>English:</strong> The participation fee includes small refreshment and water
          on control points, transfer from Znojmo to the start in Uherčice and accommodation in the finish.
        </div>

        <div class="fee-grid">
          <div class="fee-card">
            <h3>Startovné na Stovku</h3>
            <ul>
              <li>Přihlášení přes internet s platbou na účet: <strong>650 Kč</strong></li>
              <li>Přihlášení ve Znojmě před startem v případě nenaplnění kapacity: <strong>750 Kč / 30 EUR</strong></li>
              <li>Payment in Znojmo before the start: <strong>750 Kč / 28 Euros</strong></li>
              <li>Prvních 10 účastníků, kteří přivedou organizátorům pomocníka, mají snížené startovné. Sleva může být až 50 %.</li>
              <li>Motorizovaní pomocníci mají další výhody.</li>
              <li>Členové ČTU mají při prokázání průkazem na startu poloviční startovné.</li>
            </ul>
          </div>

          <div class="fee-card">
            <h3>Startovné na Šedesátku</h3>
            <ul>
              <li><strong>350 Kč nebo 15 EUR</strong> na startu ve Vranově nebo bankovním převodem v případě naplnění kapacity.</li>
              <li>Platba probíhá dle pravidel pro účastníky Stovky.</li>
              <li>Další podmínky se řídí pravidly pochodu uvedenými níže.</li>
            </ul>
          </div>
        </div>

        <div class="grid-2" style="margin-top:22px;">
          <div class="panel">
            <h3 style="margin-top:0; font-family:Montserrat, sans-serif; text-transform:uppercase;">Platba bankovním převodem</h3>
            <p>
              Platba bankovním převodem je určena <strong>pouze pro platby v CZK</strong>.
              Startovné plaťte převodem na účet číslo:
            </p>
            <p style="font-size:1.35rem; font-weight:700; color:#fff; margin:8px 0 16px;">
              2301608801 / 2010
            </p>
            <p class="muted" style="margin-bottom:0;">
              Je nutné být už přihlášen přes internet.
            </p>
          </div>

          <div class="panel">
            <h3 style="margin-top:0; font-family:Montserrat, sans-serif; text-transform:uppercase;">Podmínky platby</h3>
            <ul style="margin:0; padding-left:18px; color:var(--text-soft);">
              <li>Do zprávy pro příjemce napiš své jméno a příjmení a do variabilního symbolu jedničku.</li>
              <li>Nic dalšího do zprávy nepiš.</li>
              <li>Potřebuješ-li k platbě něco doplnit, použij e-mail: <strong>podyji@vyskovnice.cz</strong></li>
              <li>Platbu je nutno provést do 2 týdnů od přihlášení, nejpozději však do pondělí před pochodem.</li>
              <li>V seznamu účastníků si může každý zkontrolovat, zda má zaplaceno. Údaje se aktualizují přibližně jednou týdně.</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section id="pravidla" class="section-dark">
      <div class="container">
        <div class="section-head">
          <div class="overline">Pravidla pochodu</div>
          <h2>Přehledně a bez zbytečného chaosu</h2>
          <p>
            Původní text je poměrně dlouhý, proto je tady rozdělen do rozbalovacích bloků.
            To je pro web praktičtější.
          </p>
        </div>

        <div class="rules">
          <details class="rule" open>
            <summary>Kdo se stane účastníkem pochodu</summary>
            <div class="rule-content">
              <ul>
                <li>V den startu mu bude alespoň 15 let a pochodu se účastní osoba ve věku alespoň 18 let, která za něj zodpovídá.</li>
                <li>Uvede do registračního formuláře nebo na startu čitelně své jméno, příjmení a datum narození.</li>
                <li>Zaplatí startovné.</li>
                <li>Je vybaven bezpečnostními prvky pro pohyb po silnici za snížené viditelnosti.</li>
                <li>Po celou dobu pochodu si nese psací potřebu.</li>
              </ul>
            </div>
          </details>

          <details class="rule">
            <summary>Povinné bezpečnostní vybavení</summary>
            <div class="rule-content">
              <ul>
                <li>2 světelné zdroje různé barvy, ideálně bílá a červená, bílá ve směru chůze, červená vzadu.</li>
                <li>Nebo 1 světelný zdroj a bezpečnostní prvek z retroreflexního materiálu umístěný místo druhého světelného zdroje.</li>
              </ul>
            </div>
          </details>

          <details class="rule">
            <summary>Co organizátor zaručuje</summary>
            <div class="rule-content">
              <ul>
                <li>Osobní údaje nebudou zneužity.</li>
                <li>Účastník obdrží informační arch s kilometráží trasy.</li>
                <li>První tři účastníci obou pohlaví, kteří dle pravidel dorazí do cíle, získají věcné ocenění.</li>
                <li>Každý úspěšný účastník dostane diplom.</li>
              </ul>
            </div>
          </details>

          <details class="rule">
            <summary>Základní pravidla pohybu na trase</summary>
            <div class="rule-content">
              <ul>
                <li>Účastník se smí pohybovat výlučně vlastní silou bez mechanických převodníků s výjimkou turistických holí.</li>
                <li>V případě nouze je možno pochod přerušit, například za účelem ošetření nebo přivolání pomoci.</li>
                <li>Pokračovat v pochodu se však musí z místa, kde byl pochod přerušen, a přerušení je nutno nahlásit organizátorům.</li>
                <li>Doba přerušení pochodu se počítá do celkové doby pochodu.</li>
              </ul>
            </div>
          </details>

          <details class="rule">
            <summary>Kontroly a průchod tratí</summary>
            <div class="rule-content">
              <ul>
                <li>Na trase budou rozmístěny hlavní kontroly, mezikontroly a případně pohyblivé kontroly.</li>
                <li>Průchod kontrolami bude sledován organizátory a potvrzen účastníkům na identifikační arch s kilometráží.</li>
                <li>Účastník bude seznámen pouze s rozmístěním hlavních kontrol.</li>
                <li>Při setkání s kontrolou se účastník sám hlásí označenému pořadateli a požaduje potvrzení průchodu.</li>
              </ul>
            </div>
          </details>

          <details class="rule">
            <summary>Dodržování trasy a zapisování časů</summary>
            <div class="rule-content">
              <ul>
                <li>Účastník je povinen dodržovat trasu.</li>
                <li>Odchylky jsou povoleny pouze za účelem doplnění zásob v blízkosti trasy nebo v případech uvedených v protizabloudivém jističi.</li>
                <li>Do tabulky s kilometráží účastník zaznamená čas průchodu všemi kontrolami počínaje startem.</li>
              </ul>
            </div>
          </details>

          <details class="rule">
            <summary>Dodržování zákonů ČR</summary>
            <div class="rule-content">
              <ul>
                <li>Účastník je povinen dodržovat zákony ČR.</li>
                <li>Organizátoři budou dohlížet zejména na dodržování zákona o lesích a zákona o provozu na pozemních komunikacích.</li>
                <li>Patří sem mimo jiné zákaz kouření v lese, znečišťování lesa odpadky a pravidla chůze po komunikacích.</li>
              </ul>
            </div>
          </details>

          <details class="rule">
            <summary>Povolené způsoby pohybu</summary>
            <div class="rule-content">
              <ul>
                <li>Chůze, chůze s turistickými holemi.</li>
                <li>Běh, skok.</li>
                <li>Lezení, plazení, kotoulení, válení.</li>
                <li>Smykový sjezd bez snižovače tření.</li>
                <li>Plavání ve stojaté vodě, případně v proudící vodě ne ve směru jejího toku, pokud nedojde ke zkrácení trasy.</li>
                <li>Chůze o berlích či francouzských holích je povolena pouze držitelům příslušného lékařského potvrzení.</li>
              </ul>
            </div>
          </details>

          <details class="rule">
            <summary>Zakázané způsoby pohybu</summary>
            <div class="rule-content">
              <ul>
                <li>Chůze na kolečkových botách a skákacích mechanismech.</li>
                <li>Jízda na kolečkových bruslích nebo lyžích, skateboardu, jednokolce, koloběžce, kole, dvojkolce, tříkolce, čtyřkolce či jiné vícekolce.</li>
                <li>Tažení, tlačení nebo nesení jiným živočichem či strojem.</li>
                <li>Využití atmosférických pohonů, například drak, paragliding nebo kluzák.</li>
                <li>Lanový sjezd.</li>
                <li>Plavba na plavidle.</li>
              </ul>
            </div>
          </details>
        </div>
      </div>
    </section>

    <section id="kontakt" class="section-soft">
      <div class="container">
        <div class="section-head">
          <div class="overline">Kontakt</div>
          <h2>Organizátoři</h2>
          <p>
            Pro základní dotazy využij telefonní kontakt níže. Další informace budou doplněny
            na web postupně.
          </p>
        </div>

        <div class="contact-grid">
          <div class="contact-card">
            <h3>Telefonní kontakt</h3>
            <div class="contact-main">608 771 429</div>
            <div class="muted">Johnny</div>
          </div>

          <div class="contact-card">
            <h3>E-mail k platbám a dotazům</h3>
            <div class="contact-main" style="font-size:1.1rem;">podyji@vyskovnice.cz</div>
            <div class="muted">Použij zejména při řešení plateb a identifikace převodu.</div>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container footer-wrap">
      <div>STOVKA PODYJÍM • XI. ročník</div>
      <div>160 km • 112 km • 60 km</div>
      <div>Další informace koncem jara • Registrace v létě</div>
    </div>
  </footer>

</body>
</html>
