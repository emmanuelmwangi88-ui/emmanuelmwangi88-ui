<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Denji — Emmanuel Mwangi · Statement of Work</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700;800&family=IBM+Plex+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --paper:#EDEAE0;
    --paper-behind:#DAD6C8;
    --ink:#1C211D;
    --ledger-green:#1B6B4A;
    --stamp-red:#B23A2E;
    --faded:#8B8B7A;
    --gold:#C9A227;
    --mono:'JetBrains Mono', monospace;
    --sans:'IBM Plex Sans', sans-serif;
  }

  *{box-sizing:border-box; margin:0; padding:0;}

  body{
    background:var(--paper-behind);
    color:var(--ink);
    font-family:var(--sans);
    line-height:1.5;
    -webkit-font-smoothing:antialiased;
  }

  ::selection{ background:var(--ledger-green); color:var(--paper); }

  a{ color:inherit; }

  /* ===== Ticker ===== */
  .ticker{
    background:var(--ink);
    color:var(--paper);
    font-family:var(--mono);
    font-size:13px;
    letter-spacing:0.08em;
    overflow:hidden;
    white-space:nowrap;
    padding:9px 0;
    position:relative;
    z-index:10;
  }
  .ticker-track{
    display:inline-block;
    padding-left:100%;
    animation:scroll-left 32s linear infinite;
  }
  .ticker-track span{ margin:0 28px; }
  .ticker-track .up{ color:#7FD99A; }
  @keyframes scroll-left{
    0%{ transform:translateX(0); }
    100%{ transform:translateX(-50%); }
  }

  /* ===== Statement container ===== */
  .statement{
    max-width:860px;
    margin:48px auto;
    background:var(--paper);
    box-shadow:0 30px 60px -20px rgba(0,0,0,0.35);
    position:relative;
  }

  .perf{
    height:18px;
    background-image:radial-gradient(circle at 9px 9px, var(--paper-behind) 7px, transparent 7.5px);
    background-size:18px 18px;
    background-repeat:repeat-x;
  }

  section{ padding:40px 52px; }
  @media (max-width:640px){ section{ padding:32px 24px; } }

  .eyebrow{
    font-family:var(--mono);
    font-size:11px;
    letter-spacing:0.18em;
    text-transform:uppercase;
    color:var(--faded);
    display:flex;
    align-items:center;
    gap:10px;
    margin-bottom:18px;
  }
  .eyebrow::after{
    content:"";
    flex:1;
    height:1px;
    background:repeating-linear-gradient(90deg, var(--faded) 0 4px, transparent 4px 8px);
    opacity:0.5;
  }

  /* ===== Hero ===== */
  .hero{ padding-top:46px; }
  .hero-row{
    display:flex;
    align-items:flex-start;
    justify-content:space-between;
    gap:24px;
    flex-wrap:wrap;
  }
  .hero-id{ display:flex; gap:20px; align-items:center; }
  .avatar{
    width:74px; height:74px;
    border-radius:4px;
    border:2px solid var(--ink);
    object-fit:cover;
    filter:grayscale(45%) contrast(1.05);
  }
  .hero h1{
    font-family:var(--mono);
    font-weight:800;
    font-size:clamp(34px,6vw,52px);
    letter-spacing:-0.01em;
    line-height:0.95;
  }
  .hero .role{
    font-family:var(--mono);
    font-size:14px;
    color:var(--ledger-green);
    margin-top:8px;
    letter-spacing:0.02em;
  }

  .stamp{
    font-family:var(--mono);
    font-weight:800;
    font-size:13px;
    letter-spacing:0.12em;
    color:var(--stamp-red);
    border:2.5px solid var(--stamp-red);
    border-radius:6px;
    padding:8px 14px;
    transform:rotate(-7deg);
    white-space:nowrap;
    opacity:0.85;
    animation:stamp-in 0.6s ease-out 0.2s both;
  }
  @keyframes stamp-in{
    0%{ transform:rotate(-7deg) scale(2); opacity:0; }
    70%{ opacity:0.9; }
    100%{ transform:rotate(-7deg) scale(1); opacity:0.85; }
  }

  .meta-grid{
    margin-top:30px;
    display:grid;
    grid-template-columns:repeat(auto-fit, minmax(180px,1fr));
    gap:18px 28px;
    font-family:var(--mono);
    font-size:13px;
    border-top:1px solid rgba(28,33,29,0.12);
    padding-top:22px;
  }
  .meta-grid dt{ color:var(--faded); font-size:10.5px; letter-spacing:0.12em; text-transform:uppercase; margin-bottom:5px; }
  .meta-grid dd a{ text-decoration:none; border-bottom:1px solid currentColor; }
  .meta-grid dd a:hover{ color:var(--ledger-green); }

  /* ===== Statement of Work (projects) ===== */
  .txn-list{ display:flex; flex-direction:column; }
  .txn{
    display:grid;
    grid-template-columns:64px 1fr auto;
    gap:18px;
    align-items:start;
    padding:18px 14px;
    border-bottom:1px dashed rgba(28,33,29,0.18);
    transition:background 0.2s ease, transform 0.2s ease;
  }
  .txn:hover{ background:rgba(27,107,74,0.06); transform:translateX(4px); }
  .txn:last-child{ border-bottom:none; }

  .txn-id{
    font-family:var(--mono);
    font-size:11px;
    color:var(--faded);
    padding-top:3px;
  }
  .txn-body h3{ font-size:18px; font-weight:600; margin-bottom:5px; }
  .txn-body p{ font-size:13.5px; color:#4a4d45; max-width:46ch; }
  .txn-stack{
    margin-top:9px;
    display:flex; flex-wrap:wrap; gap:6px;
  }
  .txn-stack span{
    font-family:var(--mono);
    font-size:10.5px;
    letter-spacing:0.03em;
    background:rgba(28,33,29,0.06);
    border:1px solid rgba(28,33,29,0.12);
    border-radius:3px;
    padding:2.5px 7px;
    color:var(--ink);
  }
  .txn-status{
    font-family:var(--mono);
    font-size:10.5px;
    letter-spacing:0.1em;
    font-weight:700;
    padding:4px 9px;
    border-radius:3px;
    white-space:nowrap;
    height:fit-content;
  }
  .status-live{ background:rgba(27,107,74,0.14); color:var(--ledger-green); }
  .status-build{ background:rgba(201,162,39,0.16); color:#8a6b13; }
  .status-archive{ background:rgba(139,139,122,0.16); color:var(--faded); }

  /* ===== Skills ledger ===== */
  .ledger-table{ width:100%; border-collapse:collapse; font-family:var(--mono); font-size:13px; }
  .ledger-table tr{ border-bottom:1px solid rgba(28,33,29,0.1); }
  .ledger-table tr:last-child{ border-bottom:none; }
  .ledger-table td{ padding:13px 8px; vertical-align:middle; }
  .ledger-table td:first-child{ font-weight:600; width:42%; }
  .tier{
    font-size:10px;
    letter-spacing:0.1em;
    color:var(--faded);
    width:130px;
    text-transform:uppercase;
  }
  .bar-track{
    height:7px;
    background:rgba(28,33,29,0.08);
    border-radius:2px;
    overflow:hidden;
  }
  .bar-fill{ height:100%; background:var(--ledger-green); border-radius:2px; }

  /* ===== Contact ===== */
  .contact-panel{
    background:var(--ink);
    color:var(--paper);
  }
  .contact-panel .eyebrow{ color:rgba(237,234,224,0.55); }
  .contact-panel .eyebrow::after{ background:repeating-linear-gradient(90deg, rgba(237,234,224,0.4) 0 4px, transparent 4px 8px); }
  .contact-panel h2{
    font-family:var(--mono);
    font-weight:700;
    font-size:clamp(24px,4vw,32px);
    max-width:18ch;
    margin-bottom:28px;
  }
  .contact-links{
    display:grid;
    grid-template-columns:repeat(auto-fit, minmax(200px,1fr));
    gap:14px;
  }
  .contact-link{
    display:flex;
    justify-content:space-between;
    align-items:center;
    border:1px solid rgba(237,234,224,0.22);
    border-radius:5px;
    padding:14px 16px;
    text-decoration:none;
    color:var(--paper);
    font-family:var(--mono);
    font-size:13px;
    transition:border-color 0.2s ease, background 0.2s ease;
  }
  .contact-link:hover{ border-color:#7FD99A; background:rgba(127,217,154,0.07); }
  .contact-link .arrow{ opacity:0.5; }

  /* ===== Footer ===== */
  footer{
    text-align:center;
    font-family:var(--mono);
    font-size:11px;
    letter-spacing:0.14em;
    color:var(--faded);
    padding:26px 20px 6px;
  }

  /* ===== Reveal on scroll ===== */
  .reveal{ opacity:0; transform:translateY(14px); transition:opacity 0.6s ease, transform 0.6s ease; }
  .reveal.in{ opacity:1; transform:translateY(0); }

  @media (prefers-reduced-motion: reduce){
    .ticker-track{ animation:none; }
    .stamp{ animation:none; }
    .reveal{ opacity:1; transform:none; transition:none; }
  }
</style>
</head>
<body>

  <div class="ticker">
    <div class="ticker-track">
      <span><span class="up">▲</span> KOTLIN / ANDROID</span>
      <span><span class="up">▲</span> JAVASCRIPT</span>
      <span><span class="up">▲</span> PYTHON</span>
      <span><span class="up">▲</span> DJANGO</span>
      <span><span class="up">▲</span> JUPYTER</span>
      <span><span class="up">▲</span> M-PESA API</span>
      <span><span class="up">▲</span> NSE MARKET DATA</span>
      <span><span class="up">▲</span> NODE.JS / EXPRESS</span>
      <span><span class="up">▲</span> REACT</span>
      <span><span class="up">▲</span> NAIROBI, KE</span>
      <!-- duplicate for seamless loop -->
      <span><span class="up">▲</span> KOTLIN / ANDROID</span>
      <span><span class="up">▲</span> JAVASCRIPT</span>
      <span><span class="up">▲</span> PYTHON</span>
      <span><span class="up">▲</span> DJANGO</span>
      <span><span class="up">▲</span> JUPYTER</span>
      <span><span class="up">▲</span> M-PESA API</span>
      <span><span class="up">▲</span> NSE MARKET DATA</span>
      <span><span class="up">▲</span> NODE.JS / EXPRESS</span>
      <span><span class="up">▲</span> REACT</span>
      <span><span class="up">▲</span> NAIROBI, KE</span>
    </div>
  </div>

  <main class="statement">

    <section class="hero">
      <div class="hero-row">
        <div class="hero-id">
          <img class="avatar" src="https://avatars.githubusercontent.com/u/266476807?v=4" alt="Emmanuel Mwangi">
          <div>
            <h1>DENJI</h1>
            <div class="role">EMMANUEL MWANGI — SOFTWARE DEVELOPER</div>
          </div>
        </div>
        <div class="stamp">VERIFIED ✓ KE</div>
      </div>

      <dl class="meta-grid">
        <div>
          <dt>Based in</dt>
          <dd>Kiambu, Kenya</dd>
        </div>
        <div>
          <dt>Acct No. (Call / WhatsApp)</dt>
          <dd><a href="tel:+254758382850">+254 758 382 850</a></dd>
        </div>
        <div>
          <dt>GitHub</dt>
          <dd><a href="https://github.com/emmanuelmwangi88-ui" target="_blank" rel="noopener">emmanuelmwangi88-ui</a></dd>
        </div>
        <div>
          <dt>Instagram</dt>
          <dd><a href="https://www.instagram.com/itadori_manu/" target="_blank" rel="noopener">@itadori_manu</a></dd>
        </div>
      </dl>
    </section>

    <div class="perf"></div>

    <section class="reveal">
      <div class="eyebrow">Statement of Work</div>
      <div class="txn-list">

        <div class="txn">
          <div class="txn-id">TXN#001</div>
          <div class="txn-body">
            <h3>Kenya Homes Finder</h3>
            <p>Real estate platform with an agent control dashboard — tenant management, rent tracking, maintenance &amp; expense logging, M-Pesa and multi-method payments, JWT authentication.</p>
            <div class="txn-stack">
              <span>Node.js</span><span>Express</span><span>SQLite</span><span>M-Pesa API</span><span>JWT</span>
            </div>
          </div>
          <div class="txn-status status-build">IN PROGRESS</div>
        </div>

        <div class="txn">
          <div class="txn-id">TXN#002</div>
          <div class="txn-body">
            <h3>NSE Market Dashboard</h3>
            <p>Financial dashboard covering the Nairobi Securities Exchange plus global markets — forex, crypto, indices — with a dark terminal aesthetic and live data feeds.</p>
            <div class="txn-stack">
              <span>FastAPI/Django</span><span>PostgreSQL</span><span>TimescaleDB</span><span>React</span><span>D3.js</span>
            </div>
          </div>
          <div class="txn-status status-build">IN PROGRESS</div>
        </div>

        <div class="txn">
          <div class="txn-id">TXN#003</div>
          <div class="txn-body">
            <h3>PrimeHaven</h3>
            <p>Add a one-line description of what this project does — what problem it solves and who it's for.</p>
            <div class="txn-stack">
              <span>HTML</span><span>CSS</span><span>JavaScript</span>
            </div>
          </div>
          <div class="txn-status status-live">LIVE</div>
        </div>

        <div class="txn">
          <div class="txn-id">TXN#004</div>
          <div class="txn-body">
            <h3>Personal Portfolio (v1)</h3>
            <p>Earlier portfolio site — first version of an online presence, since superseded by this statement-style rebuild.</p>
            <div class="txn-stack">
              <span>HTML</span><span>CSS</span>
            </div>
          </div>
          <div class="txn-status status-archive">ARCHIVE</div>
        </div>

        <div class="txn">
          <div class="txn-id">TXN#005</div>
          <div class="txn-body">
            <h3>Kotlin Basics &amp; First App</h3>
            <p>Android fundamentals and first native build — entry point into Kotlin and the MVVM pattern.</p>
            <div class="txn-stack">
              <span>Kotlin</span><span>Android Studio</span>
            </div>
          </div>
          <div class="txn-status status-archive">ARCHIVE</div>
        </div>

      </div>
    </section>

    <div class="perf"></div>

    <section class="reveal">
      <div class="eyebrow">Skills Ledger</div>
      <table class="ledger-table">
        <tbody>
          <tr>
            <td>Kotlin / Android (MVVM)</td>
            <td class="tier">Core</td>
            <td><div class="bar-track"><div class="bar-fill" style="width:90%"></div></div></td>
          </tr>
          <tr>
            <td>JavaScript / Node.js</td>
            <td class="tier">Core</td>
            <td><div class="bar-track"><div class="bar-fill" style="width:88%"></div></div></td>
          </tr>
          <tr>
            <td>Python</td>
            <td class="tier">Core</td>
            <td><div class="bar-track"><div class="bar-fill" style="width:85%"></div></div></td>
          </tr>
          <tr>
            <td>Django</td>
            <td class="tier">Proficient</td>
            <td><div class="bar-track"><div class="bar-fill" style="width:70%"></div></div></td>
          </tr>
          <tr>
            <td>React</td>
            <td class="tier">Proficient</td>
            <td><div class="bar-track"><div class="bar-fill" style="width:68%"></div></div></td>
          </tr>
          <tr>
            <td>SQL (PostgreSQL / SQLite)</td>
            <td class="tier">Proficient</td>
            <td><div class="bar-track"><div class="bar-fill" style="width:72%"></div></div></td>
          </tr>
          <tr>
            <td>Jupyter / Data Notebooks</td>
            <td class="tier">Working</td>
            <td><div class="bar-track"><div class="bar-fill" style="width:50%"></div></div></td>
          </tr>
        </tbody>
      </table>
    </section>

    <div class="perf"></div>

    <section class="contact-panel reveal">
      <div class="eyebrow">New Transaction</div>
      <h2>Open to freelance &amp; collaboration on fintech, real estate &amp; mobile builds.</h2>
      <div class="contact-links">
        <a class="contact-link" href="tel:+254758382850">Call <span class="arrow">→</span></a>
        <a class="contact-link" href="https://wa.me/254758382850" target="_blank" rel="noopener">WhatsApp <span class="arrow">→</span></a>
        <a class="contact-link" href="https://github.com/emmanuelmwangi88-ui" target="_blank" rel="noopener">GitHub <span class="arrow">→</span></a>
        <a class="contact-link" href="https://www.instagram.com/itadori_manu/" target="_blank" rel="noopener">Instagram <span class="arrow">→</span></a>
        <a class="contact-link" href="mailto:your-email@example.com">Email <span class="arrow">→</span></a>
      </div>
    </section>

    <div class="perf"></div>

    <footer>
      THANK YOU FOR VISITING · STATEMENT GENERATED {{YEAR}} · NAIROBI, KE
    </footer>

  </main>

<script>
  document.querySelector('footer').innerHTML =
    document.querySelector('footer').innerHTML.replace('{{YEAR}}', new Date().getFullYear());

  const reveals = document.querySelectorAll('.reveal');
  if ('IntersectionObserver' in window){
    const io = new IntersectionObserver((entries)=>{
      entries.forEach(e=>{
        if(e.isIntersecting){ e.target.classList.add('in'); io.unobserve(e.target); }
      });
    }, { threshold:0.15 });
    reveals.forEach(el=>io.observe(el));
  } else {
    reveals.forEach(el=>el.classList.add('in'));
  }
</script>

</body>
</html>