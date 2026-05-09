<html lang="it">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Lancelot — AI Automation Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@300;400;600;700;900&family=Barlow:wght@300;400;500;600&display=swap" rel="stylesheet"/>
<style>
*{margin:0;padding:0;box-sizing:border-box}
:root{--lime:#ccff00;--lime-dim:rgba(204,255,0,0.1);--lime-glow:rgba(204,255,0,0.3);--bg:#0a0a0a;--surface:#111111;--surface2:#161616;--border:rgba(204,255,0,0.15);--grey:#666;--grey-mid:#999;--white:#f0f0f0}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--white);font-family:'Barlow',sans-serif;overflow-x:hidden}
body::before{content:'';position:fixed;inset:0;background-image:linear-gradient(rgba(204,255,0,0.02) 1px,transparent 1px),linear-gradient(90deg,rgba(204,255,0,0.02) 1px,transparent 1px);background-size:80px 80px;pointer-events:none;z-index:0}

nav{position:fixed;top:0;left:0;right:0;z-index:100;display:flex;align-items:center;justify-content:space-between;padding:1.2rem 3rem;background:rgba(10,10,10,0.92);backdrop-filter:blur(12px);border-bottom:1px solid rgba(204,255,0,0.08)}
.nav-logo{font-family:'Barlow Condensed',sans-serif;font-weight:900;font-size:1.2rem;letter-spacing:0.18em;text-transform:uppercase;color:var(--lime)}
.nav-links{display:flex;gap:2rem;list-style:none}
.nav-links a{font-size:0.7rem;letter-spacing:0.2em;text-transform:uppercase;color:var(--grey);text-decoration:none;transition:color 0.2s}
.nav-links a:hover{color:var(--lime)}

section{position:relative;z-index:1}

#hero{min-height:100vh;display:flex;align-items:center;padding:8rem 3rem 4rem;overflow:hidden}
.hero-grid{max-width:1200px;margin:0 auto;width:100%;display:grid;grid-template-columns:1.1fr 0.9fr;gap:4rem;align-items:center}
.hero-eyebrow{display:inline-flex;align-items:center;gap:0.6rem;font-size:0.65rem;letter-spacing:0.35em;text-transform:uppercase;color:var(--lime);margin-bottom:1.5rem;animation:fadeUp 0.7s ease 0.2s both}
.hero-eyebrow::before{content:'';width:24px;height:1px;background:var(--lime)}
.hero-h1{font-family:'Barlow Condensed',sans-serif;font-weight:900;font-size:clamp(3rem,6vw,5.5rem);line-height:0.95;letter-spacing:-0.01em;text-transform:uppercase;animation:fadeUp 0.8s ease 0.4s both}
.hero-h1 .accent{color:var(--lime)}
.hero-h1 .outline{-webkit-text-stroke:1px var(--white);color:transparent}
.hero-sub{margin-top:2rem;font-size:1rem;line-height:1.7;color:var(--grey-mid);max-width:480px;font-weight:300;animation:fadeUp 0.8s ease 0.6s both}
.hero-cta-row{margin-top:2.5rem;display:flex;gap:1rem;align-items:center;flex-wrap:wrap;animation:fadeUp 0.8s ease 0.8s both}
.btn-lime{display:inline-flex;align-items:center;gap:0.6rem;background:var(--lime);color:#0a0a0a;font-family:'Barlow Condensed',sans-serif;font-weight:700;font-size:0.8rem;letter-spacing:0.2em;text-transform:uppercase;padding:0.85rem 2rem;border:none;cursor:pointer;text-decoration:none;transition:box-shadow 0.3s,transform 0.2s;clip-path:polygon(0 0,calc(100% - 10px) 0,100% 10px,100% 100%,10px 100%,0 calc(100% - 10px))}
.btn-lime:hover{box-shadow:0 0 40px var(--lime-glow);transform:translateY(-2px)}
.btn-outline{font-size:0.7rem;letter-spacing:0.2em;text-transform:uppercase;color:var(--grey-mid);text-decoration:none;border:1px solid rgba(255,255,255,0.15);padding:0.85rem 1.8rem;transition:border-color 0.3s,color 0.3s}
.btn-outline:hover{border-color:var(--lime);color:var(--lime)}
.hero-visual{display:flex;align-items:center;justify-content:center;position:relative;animation:fadeUp 1s ease 0.5s both}
.hex-grid{display:grid;grid-template-columns:repeat(5,1fr);gap:4px;transform:rotate(-10deg);animation:float 6s ease-in-out infinite}
.hex{width:52px;height:52px;border:1px solid;display:flex;align-items:center;justify-content:center;font-size:0.55rem;letter-spacing:0.1em;text-align:center;clip-path:polygon(50% 0%,100% 25%,100% 75%,50% 100%,0% 75%,0% 25%)}
.hex-lime{border-color:var(--lime);background:var(--lime-dim);color:var(--lime)}
.hex-dim{border-color:rgba(255,255,255,0.06);background:rgba(255,255,255,0.02);color:rgba(255,255,255,0.15)}
.hex-mid{border-color:rgba(204,255,0,0.3);background:rgba(204,255,0,0.05);color:rgba(204,255,0,0.5)}
.metric-float{position:absolute;background:var(--surface);border:1px solid var(--border);padding:0.7rem 1.1rem;font-size:0.6rem;letter-spacing:0.1em;color:var(--grey-mid)}
.metric-float .val{font-family:'Barlow Condensed',sans-serif;font-size:1.5rem;font-weight:900;color:var(--lime);display:block;line-height:1}
.mf1{top:-5%;right:-8%}
.mf2{bottom:5%;left:-10%}

#bio{padding:7rem 3rem;border-top:1px solid rgba(255,255,255,0.05)}
.section-inner{max-width:1200px;margin:0 auto}
.sec-label{font-size:0.62rem;letter-spacing:0.35em;text-transform:uppercase;color:var(--lime);display:flex;align-items:center;gap:0.8rem;margin-bottom:1.5rem}
.sec-label::before{content:'';width:28px;height:1px;background:var(--lime)}
.sec-h2{font-family:'Barlow Condensed',sans-serif;font-size:clamp(2.2rem,4vw,3.5rem);font-weight:900;text-transform:uppercase;letter-spacing:-0.01em;line-height:1}
.bio-inner{display:grid;grid-template-columns:1fr 1.6fr;gap:5rem;align-items:center;margin-top:3.5rem}
.bio-photo-wrap{display:flex;flex-direction:column;align-items:center;gap:1.5rem}
.bio-photo-frame{width:240px;height:240px;border:1px solid var(--border);position:relative;clip-path:polygon(0 0,calc(100% - 20px) 0,100% 20px,100% 100%,20px 100%,0 calc(100% - 20px));overflow:hidden;background:var(--surface);flex-shrink:0}
.bio-photo-frame img{width:100%;height:100%;object-fit:cover;display:block;filter:grayscale(20%) contrast(1.05)}
.bio-photo-placeholder{width:100%;height:100%;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:0.8rem;color:var(--grey);font-size:0.65rem;letter-spacing:0.15em;text-align:center;padding:1rem}
.bio-photo-placeholder svg{color:rgba(204,255,0,0.3)}
.photo-corner{position:absolute;width:16px;height:16px;border-color:var(--lime);border-style:solid;border-width:0}
.photo-corner.tl{top:6px;left:6px;border-top-width:2px;border-left-width:2px}
.photo-corner.br{bottom:6px;right:6px;border-bottom-width:2px;border-right-width:2px}
.bio-name{font-family:'Barlow Condensed',sans-serif;font-size:1rem;font-weight:700;text-transform:uppercase;letter-spacing:0.2em;color:var(--lime);text-align:center}
.bio-role{font-size:0.65rem;letter-spacing:0.15em;text-transform:uppercase;color:var(--grey);text-align:center}
.bio-quote{font-family:'Barlow Condensed',sans-serif;font-size:1.6rem;font-weight:700;line-height:1.2;color:var(--white);margin-bottom:2rem;border-left:3px solid var(--lime);padding-left:1.5rem}
.bio-text{font-size:0.9rem;line-height:1.95;color:var(--grey-mid);margin-bottom:1.5rem}
.bio-text .highlight{color:var(--lime);font-weight:600}
.bio-tags{display:flex;flex-wrap:wrap;gap:0.6rem;margin-top:2rem}
.bio-tag{font-size:0.6rem;letter-spacing:0.2em;text-transform:uppercase;color:var(--lime);border:1px solid rgba(204,255,0,0.2);padding:0.35rem 0.9rem}

#pain{padding:7rem 3rem;border-top:1px solid rgba(255,255,255,0.05)}
.pain-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:rgba(255,255,255,0.05);margin-top:3.5rem}
.pain-card{background:var(--bg);padding:2.5rem 1.8rem;border-top:2px solid transparent;transition:all 0.3s}
.pain-card:hover{background:var(--surface);border-top-color:rgba(255,60,60,0.6)}
.pain-kpi{font-family:'Barlow Condensed',sans-serif;font-size:2rem;font-weight:900;color:rgba(255,80,80,0.7);margin-bottom:0.3rem}
.pain-title{font-family:'Barlow Condensed',sans-serif;font-size:1.1rem;font-weight:700;text-transform:uppercase;letter-spacing:0.05em;color:var(--white);margin-bottom:0.8rem}
.pain-text{font-size:0.78rem;line-height:1.8;color:var(--grey)}

#solution{padding:7rem 3rem;background:var(--surface);border-top:1px solid var(--border)}
.sol-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem;margin-top:3.5rem}
.sol-card{border:1px solid var(--border);background:var(--bg);padding:2.5rem 2rem;position:relative;overflow:hidden;transition:all 0.3s}
.sol-card:hover{border-color:var(--lime);box-shadow:0 0 30px rgba(204,255,0,0.06)}
.sol-icon{width:48px;height:48px;background:var(--lime-dim);border:1px solid var(--lime);display:flex;align-items:center;justify-content:center;margin-bottom:1.8rem;color:var(--lime)}
.sol-title{font-family:'Barlow Condensed',sans-serif;font-size:1.25rem;font-weight:700;text-transform:uppercase;letter-spacing:0.05em;margin-bottom:0.5rem;color:var(--lime)}
.sol-sub{font-size:0.7rem;letter-spacing:0.15em;text-transform:uppercase;color:var(--grey);margin-bottom:1rem}
.sol-text{font-size:0.8rem;line-height:1.85;color:var(--grey-mid)}

#techstack{padding:7rem 3rem;border-top:1px solid rgba(255,255,255,0.05)}
.stack-layout{display:grid;grid-template-columns:1fr 1fr;gap:5rem;align-items:start;margin-top:3.5rem}
.stack-grid{display:grid;grid-template-columns:1fr 1fr;gap:1px;background:rgba(255,255,255,0.05)}
.stack-item{background:var(--bg);padding:1.8rem 1.5rem;border-left:2px solid transparent;transition:all 0.3s}
.stack-item:hover{background:var(--surface);border-left-color:var(--lime)}
.stack-tool{font-family:'Barlow Condensed',sans-serif;font-size:1.4rem;font-weight:900;color:var(--lime);letter-spacing:0.05em;margin-bottom:0.4rem}
.stack-role{font-size:0.65rem;letter-spacing:0.2em;text-transform:uppercase;color:var(--grey);margin-bottom:0.7rem}
.stack-desc{font-size:0.75rem;line-height:1.7;color:var(--grey-mid)}
.vibe-box{border:1px solid var(--border);background:var(--surface);padding:2.5rem}
.vibe-title{font-family:'Barlow Condensed',sans-serif;font-size:2rem;font-weight:900;text-transform:uppercase;color:var(--lime);margin-bottom:1rem;letter-spacing:0.05em}
.vibe-text{font-size:0.82rem;line-height:1.9;color:var(--grey-mid);margin-bottom:1.5rem}
.terminal{background:#050505;border:1px solid rgba(204,255,0,0.1);padding:1.5rem;font-family:monospace;font-size:0.7rem;line-height:1.9}
.t-prompt{color:var(--lime)}
.t-cmd{color:var(--white)}
.t-out{color:rgba(204,255,0,0.5);padding-left:1rem}
.t-comment{color:var(--grey)}
.blink{display:inline-block;width:7px;height:12px;background:var(--lime);animation:blink 1s step-end infinite;vertical-align:middle}

#links{padding:7rem 3rem;background:var(--surface);border-top:1px solid var(--border)}
.links-grid{display:grid;grid-template-columns:1fr 1fr;gap:1.5rem;margin-top:3.5rem}
.link-card{border:1px solid rgba(255,255,255,0.08);background:var(--bg);padding:3rem 2.5rem;text-decoration:none;display:block;position:relative;overflow:hidden;transition:all 0.4s}
.link-card:hover{border-color:var(--lime);transform:translateY(-4px);box-shadow:0 20px 60px rgba(204,255,0,0.08)}
.link-number{font-family:'Barlow Condensed',sans-serif;font-size:4rem;font-weight:900;color:rgba(204,255,0,0.06);position:absolute;top:1rem;right:1.5rem;line-height:1}
.link-tag{font-size:0.6rem;letter-spacing:0.3em;text-transform:uppercase;color:var(--lime);margin-bottom:1.5rem;display:flex;align-items:center;gap:0.6rem}
.link-tag::before{content:'';width:20px;height:1px;background:var(--lime)}
.link-title{font-family:'Barlow Condensed',sans-serif;font-size:1.8rem;font-weight:900;text-transform:uppercase;letter-spacing:0.03em;color:var(--white);margin-bottom:0.8rem;line-height:1.1}
.link-desc{font-size:0.78rem;line-height:1.7;color:var(--grey);margin-bottom:2rem}
.link-arrow{display:inline-flex;align-items:center;gap:0.6rem;font-size:0.7rem;letter-spacing:0.2em;text-transform:uppercase;color:var(--lime);font-family:'Barlow Condensed',sans-serif;font-weight:700}

footer{padding:3rem;border-top:1px solid rgba(255,255,255,0.05);display:flex;justify-content:space-between;align-items:center;position:relative;z-index:1}
.foot-copy{font-size:0.65rem;color:var(--grey);letter-spacing:0.1em}
.foot-badge{font-size:0.6rem;letter-spacing:0.25em;text-transform:uppercase;color:var(--lime);border:1px solid rgba(204,255,0,0.2);padding:0.4rem 1rem}

.reveal{opacity:0;transform:translateY(32px);transition:opacity 0.7s ease,transform 0.7s ease}
.reveal.visible{opacity:1;transform:translateY(0)}
.reveal-d1{transition-delay:0.1s}
.reveal-d2{transition-delay:0.2s}
.reveal-d3{transition-delay:0.3s}
.reveal-d4{transition-delay:0.4s}

@keyframes fadeUp{from{opacity:0;transform:translateY(28px)}to{opacity:1;transform:translateY(0)}}
@keyframes blink{0%,100%{opacity:1}50%{opacity:0}}
@keyframes float{0%,100%{transform:translateY(0) rotate(-10deg)}50%{transform:translateY(-12px) rotate(-10deg)}}

@media(max-width:900px){
  nav{padding:1rem 1.5rem}
  .nav-links{gap:1rem}
  .nav-links a{font-size:0.6rem}
  .hero-grid,.bio-inner,.pain-grid,.sol-grid,.stack-layout,.links-grid{grid-template-columns:1fr}
  .hex-grid,.mf1,.mf2{display:none}
  #hero,#bio,#pain,#solution,#techstack,#links{padding-left:1.5rem;padding-right:1.5rem}
}
</style>
</head>
<body>

<nav>
  <div class="nav-logo">Lancelot</div>
  <ul class="nav-links">
    <li><a href="#bio">Chi Sono</a></li>
    <li><a href="#pain">Il Problema</a></li>
    <li><a href="#solution">La Soluzione</a></li>
    <li><a href="#techstack">Stack</a></li>
    <li><a href="#links">Connect</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-grid">
    <div>
      <div class="hero-eyebrow">Bridge Builder · AI × Industrial Automation</div>
      <h1 class="hero-h1">
        <span class="outline">Robotica</span><br>
        <span class="accent">Intuitiva</span><br>
        come uno<br>
        <span class="outline">Smartphone</span>
      </h1>
      <p class="hero-sub">
        Libero i Plant Manager dall'incubo del downtime e dalla schiavitù del codice legacy. Trasformo fabbriche rigide in ecosistemi autonomi — abbattendo i tempi di sviluppo di un ordine di grandezza.
      </p>
      <div class="hero-cta-row">
        <a href="#links" class="btn-lime">
          <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
          Inizia la Conversazione
        </a>
        <a href="#bio" class="btn-outline">Chi Sono</a>
      </div>
    </div>
    <div class="hero-visual">
      <div class="hex-grid">
        <div class="hex hex-dim"></div><div class="hex hex-mid">AI</div><div class="hex hex-dim"></div><div class="hex hex-lime">KRL→NL</div><div class="hex hex-dim"></div>
        <div class="hex hex-lime">PLC</div><div class="hex hex-dim"></div><div class="hex hex-lime">ML</div><div class="hex hex-dim"></div><div class="hex hex-mid">IoT</div>
        <div class="hex hex-dim"></div><div class="hex hex-lime">RUL</div><div class="hex hex-mid">OPC</div><div class="hex hex-dim"></div><div class="hex hex-lime">5.0</div>
        <div class="hex hex-dim"></div><div class="hex hex-mid">SCADA</div><div class="hex hex-dim"></div><div class="hex hex-lime">HMI</div><div class="hex hex-dim"></div>
        <div class="hex hex-mid">Edge</div><div class="hex hex-lime">AGI</div><div class="hex hex-dim"></div><div class="hex hex-mid">Cobot</div><div class="hex hex-dim"></div>
      </div>
      <div class="metric-float mf1"><span class="val">−73%</span>Downtime ridotto</div>
      <div class="metric-float mf2"><span class="val">10×</span>Velocità sviluppo</div>
    </div>
  </div>
</section>

<!-- BIO -->
<section id="bio">
  <div class="section-inner">
    <div class="reveal">
      <div class="sec-label">Chi Sono — Il Bridge Builder</div>
      <h2 class="sec-h2">Dall'Officina<br><span style="color:var(--lime)">al Business</span></h2>
    </div>
    <div class="bio-inner">
      <div class="bio-photo-wrap reveal reveal-d1">
        <div class="bio-photo-frame">
          <!--
            PER AGGIUNGERE LA TUA FOTO:
            Sostituisci il blocco .bio-photo-placeholder qui sotto con:
            <img src="foto.jpg" alt="Lancelot" />
            Assicurati che la foto sia nella stessa cartella del file HTML.
          -->
          <img src="profilo.jpg" alt="Lancelot" />
            <svg width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1">
              <path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"/>
              <circle cx="12" cy="7" r="4"/>
            </svg>
            <span>Carica qui<br>la tua foto</span>
            <span style="color:rgba(204,255,0,0.4);font-size:0.55rem">240×240px consigliato</span>
          </div>
          <div class="photo-corner tl"></div>
          <div class="photo-corner br"></div>
        </div>
        <div class="bio-name">Trevisi Matteo</div>
        <div class="bio-role">Automation Engineer · AI Bridge Builder</div>
      </div>
      <div class="reveal reveal-d2">
        <div class="bio-quote">
          "Ho smesso di guardare solo ai bit e ai bulloni per guardare al valore di business."
        </div>
        <p class="bio-text">
          Sono un <span class="highlight">Ingegnere dell'Automazione</span> che ha smesso di guardare solo ai bit e ai bulloni per guardare al valore di business. Mi definisco un <span class="highlight">'Bridge Builder'</span> tra l'Intelligenza Artificiale Generativa e la meccanica industriale.
        </p>
        <p class="bio-text">
          Il mio obiettivo è trasformare fabbriche rigide in ecosistemi autonomi, usando il <span class="highlight">#VIBECODING</span> per abbattere i tempi di sviluppo e i costi di integrazione.
        </p>
        <div class="bio-tags">
          <span class="bio-tag">Industria 5.0</span>
          <span class="bio-tag">#VibeCoding</span>
          <span class="bio-tag">Generative AI</span>
          <span class="bio-tag">Robotica Industriale</span>
          <span class="bio-tag">PLC / SCADA</span>
          <span class="bio-tag">Machine Learning</span>
        </div>
      </div>
    </div>
</section>

<!-- PAIN -->
<section id="pain">
  <div class="section-inner">
    <div class="reveal">
      <div class="sec-label">Il Problema — Prima del Mio Intervento</div>
      <h2 class="sec-h2">La Fabbrica<br><span style="color:rgba(255,80,80,0.8)">Ostaggio</span><br>di Sé Stessa</h2>
    </div>
    <div class="pain-grid">
      <div class="pain-card reveal reveal-d1">
        <div class="pain-kpi">47h</div>
        <div class="pain-title">Linee Ferme</div>
        <p class="pain-text">Un guasto non previsto blocca l'intera produzione. Ogni ora costa migliaia di euro e nessuno sa quando si riprende.</p>
      </div>
      <div class="pain-card reveal reveal-d2">
        <div class="pain-kpi">0</div>
        <div class="pain-title">Programmatori Reperibili</div>
        <p class="pain-text">KRL, RAPID, Structured Text — linguaggi proprietari che richiedono anni di formazione e specialisti introvabili sul mercato.</p>
      </div>
      <div class="pain-card reveal reveal-d3">
        <div class="pain-kpi">91%</div>
        <div class="pain-title">Dati Sprecati</div>
        <p class="pain-text">I sensori raccolgono terabyte di dati operativi che dormono su server locali, mai analizzati, mai trasformati in valore.</p>
      </div>
      <div class="pain-card reveal reveal-d4">
        <div class="pain-kpi">∞</div>
        <div class="pain-title">Stress Operativo</div>
        <p class="pain-text">Il Plant Manager vive nel terrore del prossimo fermo. Le decisioni vengono prese sull'onda dell'emergenza, non dei dati.</p>
      </div>
    </div>
  </div>
</section>

<!-- SOLUTION -->
<section id="solution">
  <div class="section-inner">
    <div class="reveal">
      <div class="sec-label">La Soluzione — Dopo il Mio Intervento</div>
      <h2 class="sec-h2">Tre Leve.<br><span style="color:var(--lime)">Un Sistema</span><br>Integrato.</h2>
    </div>
    <div class="sol-grid">
      <div class="sol-card reveal reveal-d1">
        <div class="sol-icon">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/></svg>
        </div>
        <div class="sol-title">Zero Skill Gap</div>
        <div class="sol-sub">Natural Language Interfaces</div>
        <p class="sol-text">Dimentica KRL e RAPID. I tuoi operatori interagiscono con i robot in italiano, attraverso interfacce linguistiche che traducono l'intenzione in codice macchina. Zero formazione specialistica. Zero dipendenza da integratori esterni.</p>
      </div>
      <div class="sol-card reveal reveal-d2">
        <div class="sol-icon">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M22 12h-4l-3 9L9 3l-3 9H2"/></svg>
        </div>
        <div class="sol-title">Predictive Peace</div>
        <div class="sol-sub">Algoritmi Predittivi</div>
        <p class="sol-text">I modelli ML analizzano vibrazione, temperatura e corrente 24/7 e stimano il Remaining Useful Life di ogni componente critico. Ricevi l'alert 12 giorni prima del guasto — non dopo. Da reattivo a proattivo.</p>
      </div>
      <div class="sol-card reveal reveal-d3">
        <div class="sol-icon">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="17 1 21 5 17 9"/><path d="M3 11V9a4 4 0 0 1 4-4h14"/><polyline points="7 23 3 19 7 15"/><path d="M21 13v2a4 4 0 0 1-4 4H3"/></svg>
        </div>
        <div class="sol-title">Agile Reconfiguration</div>
        <div class="sol-sub">Setup in Minuti, non Giorni</div>
        <p class="sol-text">Con architetture modulari e interfacce No-Code, il reconfiguring di una cella robotica passa da 3 giorni a 40 minuti. La flessibilità che il mercato richiede, senza il caos che temevi.</p>
      </div>
    </div>
  </div>
</section>

<!-- TECH STACK -->
<section id="techstack">
  <div class="section-inner">
    <div class="reveal">
      <div class="sec-label">Tech Stack & #VibeCoding</div>
      <h2 class="sec-h2">Come Costruisco<br><span style="color:var(--lime)">10× più Veloce</span></h2>
    </div>
    <div class="stack-layout">
      <div class="stack-grid reveal reveal-d1">
        <div class="stack-item">
          <div class="stack-tool">Claude</div>
          <div class="stack-role">AI Architecture Partner</div>
          <p class="stack-desc">Progettazione di algoritmi, refactoring di codice legacy e generazione di documentazione tecnica in tempo reale.</p>
        </div>
        <div class="stack-item">
          <div class="stack-tool">Cursor</div>
          <div class="stack-role">AI-Powered IDE</div>
          <p class="stack-desc">Sviluppo di logiche PLC e script Python con autocompletamento contestuale e review del codice assistita da LLM.</p>
        </div>
        <div class="stack-item">
          <div class="stack-tool">Python</div>
          <div class="stack-role">ML & Data Pipeline</div>
          <p class="stack-desc">scikit-learn, PyTorch e pandas per i modelli predittivi. FastAPI per esporre le inferenze ai sistemi SCADA via REST/OPC-UA.</p>
        </div>
        <div class="stack-item">
          <div class="stack-tool">Miro</div>
          <div class="stack-role">System Design Canvas</div>
          <p class="stack-desc">Architetture di sistema, Business Model Canvas e workshop di co-design con il cliente in un unico spazio collaborativo.</p>
        </div>
      </div>
      <div class="vibe-box reveal reveal-d2">
        <div class="vibe-title">#VibeCoding</div>
        <p class="vibe-text">Il VibeCoding non è scrivere codice con l'AI. È un dialogo iterativo tra expertise ingegneristica e intelligenza generativa — dove l'AI amplifica il pensiero, non lo sostituisce.</p>
        <p class="vibe-text">Prototipo in ore ciò che richiederebbe settimane. Ogni output viene validato con rigore IEC, ma il ritmo è quello di una startup.</p>
        <div class="terminal">
          <div><span class="t-prompt">$</span> <span class="t-cmd">ai-eng init --project predictive_maint</span></div>
          <div class="t-out">✓ Dataset sensori caricato (4.2GB)</div>
          <div class="t-out">✓ Feature engineering: 42 features estratte</div>
          <div class="t-out">✓ LSTM addestrato → accuracy: 97.3%</div>
          <div><span class="t-prompt">$</span> <span class="t-cmd">deploy --env prod --target scada</span></div>
          <div class="t-out">✓ OPC-UA bridge attivo</div>
          <div class="t-out">⚠ Alert: Motore_03 RUL = 847h</div>
          <div><span class="t-prompt">$</span> <span class="t-comment"># ↑ Tutto in 4 ore di lavoro</span></div>
          <div><span class="t-prompt">$</span> <span class="blink"></span></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- LINKS -->
<section id="links">
  <div class="section-inner">
    <div class="reveal">
      <div class="sec-label">Connect — Parliamoci</div>
      <h2 class="sec-h2">Due Porte.<br><span style="color:var(--lime)">Un Obiettivo.</span></h2>
    </div>
    <div class="links-grid">
      <a href="https://www.linkedin.com/in/matteotrevisi/" target="_blank" class="link-card reveal reveal-d1">
        <div class="link-number">01</div>
        <div class="link-tag">Profilo Professionale</div>
        <div class="link-title">Il Mio<br>Hammer su<br>LinkedIn</div>
        <p class="link-desc">Il mio track record, i progetti industriali, le competenze certificate e le riflessioni sul futuro dell'Industria 5.0.</p>
        <div class="link-arrow">
          Visita il Profilo
          <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
        </div>
      </a>
      <a href="https://miro.com/welcomeonboard/QlFvNXRUa1BPZEsyTmdUSGYrWHFwK05wN2IyZXl1dnhiQW5pM3ZQZlRWeGdnZy8wUm9ydzlja2tjdmk2YTIrbW9Ec0IvbVAxQklMNHFEeUZBOUloazVoTHNHSE9RNFVlNzhucXZWZVRhcW50WEplTkwwa05DTG9INERheWRXQk1yVmtkMG5hNDA3dVlncnBvRVB2ZXBnPT0hdjE=?share_link_id=573611647287" target="_blank" class="link-card reveal reveal-d2">
        <div class="link-number">02</div>
        <div class="link-tag">Business Model Canvas</div>
        <div class="link-title">La Strategia<br>Integrale<br>su Miro</div>
        <p class="link-desc">Il Business Model Canvas completo, la value proposition mappata e i percorsi di trasformazione per le PMI manifatturiere.</p>
        <div class="link-arrow">
          Apri la Board
          <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
        </div>
      </a>
    </div>
  </div>
</section>

<footer>
  <div class="foot-copy">© 2025 — Lancelot · Ingegnere dell'Automazione AI-Driven</div>
  <div class="foot-badge">Industria 5.0 Ready</div>
</footer>

<script>
const obs = new IntersectionObserver(entries => {
  entries.forEach(e => { if(e.isIntersecting) e.target.classList.add('visible'); });
}, {threshold: 0.08});
document.querySelectorAll('.reveal').forEach(el => obs.observe(el));
</script>
</body>
</html>
