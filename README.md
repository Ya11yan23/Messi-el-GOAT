# Messi-el-GOAT
Mi primer repositorio en GitHub
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Messi · El Rey de Qatar 2022</title>
<style>
  :root{
    --azul:#4EA8DE;
    --azul-hondo:#0A2540;
    --azul-noche:#061627;
    --rojo:#E63946;
    --oro:#FFC93C;
    --oro-hondo:#D99B00;
    --cielo:#8ECAE6;
    --blanco:#F7FBFF;
  }
  *{margin:0;padding:0;box-sizing:border-box}
  html{scroll-behavior:smooth}
  body{
    font-family:'Segoe UI',system-ui,sans-serif;
    background:var(--azul-noche);
    color:var(--blanco);
    overflow-x:hidden;
  }
  h1,h2,h3{font-weight:900;letter-spacing:-.02em;line-height:.95}

  /* ---------- PROGRESO ---------- */
  .progress{
    position:fixed;top:0;left:0;height:4px;width:0;z-index:999;
    background:linear-gradient(90deg,var(--azul),var(--oro),var(--rojo));
    box-shadow:0 0 12px var(--oro);
  }

  /* ---------- HERO ---------- */
  .hero{
    min-height:100vh;display:flex;flex-direction:column;
    align-items:center;justify-content:center;text-align:center;
    position:relative;padding:2rem;
    background:
      radial-gradient(circle at 50% 30%,rgba(78,168,222,.35),transparent 60%),
      radial-gradient(circle at 50% 80%,rgba(230,57,70,.18),transparent 55%),
      var(--azul-noche);
  }
  .stars{position:absolute;inset:0;overflow:hidden;z-index:0}
  .star{position:absolute;background:var(--oro);border-radius:50%;
    animation:twinkle 3s infinite ease-in-out}
  @keyframes twinkle{0%,100%{opacity:.2;transform:scale(.6)}50%{opacity:1;transform:scale(1.2)}}

  .eyebrow{
    font-size:.85rem;letter-spacing:.5em;text-transform:uppercase;
    color:var(--oro);margin-bottom:1.5rem;z-index:2;
    padding:.4rem 1.2rem;border:1px solid rgba(255,201,60,.4);border-radius:40px;
  }
  .hero h1{
    font-size:clamp(3.5rem,14vw,10rem);z-index:2;
    background:linear-gradient(180deg,var(--blanco),var(--cielo) 55%,var(--azul));
    -webkit-background-clip:text;background-clip:text;color:transparent;
    text-shadow:0 0 60px rgba(78,168,222,.4);
  }
  .hero .sub{
    font-size:clamp(1rem,3vw,1.6rem);margin-top:1.2rem;z-index:2;
    color:var(--cielo);font-weight:600;
  }
  .cup{
    font-size:clamp(4rem,12vw,7rem);margin:2rem 0 .5rem;z-index:2;
    filter:drop-shadow(0 0 30px var(--oro));
    animation:float 4s ease-in-out infinite;
  }
  @keyframes float{0%,100%{transform:translateY(0) rotate(-3deg)}50%{transform:translateY(-18px) rotate(3deg)}}
  .scroll-hint{position:absolute;bottom:2rem;z-index:2;color:var(--cielo);
    font-size:.8rem;letter-spacing:.3em;animation:bounce 2s infinite}
  @keyframes bounce{0%,100%{transform:translateY(0)}50%{transform:translateY(10px)}}

  /* ---------- CINTA ---------- */
  .ribbon{
    background:linear-gradient(90deg,var(--rojo),var(--oro),var(--azul));
    color:var(--azul-noche);font-weight:900;overflow:hidden;white-space:nowrap;
    padding:.8rem 0;text-transform:uppercase;letter-spacing:.15em;
  }
  .ribbon span{display:inline-block;padding-left:100%;animation:slide 18s linear infinite}
  @keyframes slide{0%{transform:translateX(0)}100%{transform:translateX(-100%)}}

  /* ---------- SECCIONES ---------- */
  section{padding:6rem 1.5rem;max-width:1100px;margin:0 auto}
  .reveal{opacity:0;transform:translateY(40px);transition:.9s cubic-bezier(.2,.8,.2,1)}
  .reveal.on{opacity:1;transform:none}
  .section-title{font-size:clamp(2rem,6vw,3.5rem);margin-bottom:.6rem}
  .section-title .accent{color:var(--oro)}
  .lead{color:var(--cielo);font-size:1.15rem;max-width:640px;margin-bottom:3rem;line-height:1.6}

  /* ---------- STATS ---------- */
  .stats{display:grid;grid-template-columns:repeat(auto-fit,minmax(160px,1fr));gap:1.2rem}
  .stat{
    background:linear-gradient(145deg,rgba(78,168,222,.12),rgba(6,22,39,.6));
    border:1px solid rgba(78,168,222,.25);border-radius:20px;padding:2rem 1.2rem;
    text-align:center;transition:.35s;cursor:default;position:relative;overflow:hidden;
  }
  .stat::before{content:"";position:absolute;inset:0;
    background:radial-gradient(circle at 50% 0%,rgba(255,201,60,.25),transparent 70%);
    opacity:0;transition:.35s}
  .stat:hover{transform:translateY(-8px);border-color:var(--oro)}
  .stat:hover::before{opacity:1}
  .stat .num{font-size:2.8rem;font-weight:900;color:var(--oro);display:block}
  .stat .lbl{font-size:.85rem;color:var(--cielo);text-transform:uppercase;letter-spacing:.1em;margin-top:.4rem}

  /* ---------- TIMELINE FINAL ---------- */
  .timeline{border-left:3px solid var(--azul);margin-left:1rem;padding-left:2rem}
  .tl-item{margin-bottom:2.5rem;position:relative;cursor:pointer}
  .tl-item::before{content:"";position:absolute;left:-2.65rem;top:.3rem;
    width:18px;height:18px;border-radius:50%;background:var(--azul-noche);
    border:3px solid var(--oro);box-shadow:0 0 12px var(--oro);transition:.3s}
  .tl-item:hover::before{background:var(--oro);transform:scale(1.3)}
  .tl-time{color:var(--rojo);font-weight:900;font-size:1.1rem}
  .tl-desc{color:var(--blanco);margin-top:.3rem}
  .tl-detail{max-height:0;overflow:hidden;transition:.5s;color:var(--cielo);font-size:.95rem}
  .tl-item.open .tl-detail{max-height:120px;margin-top:.6rem}

  /* ---------- COMPARADOR ---------- */
  .versus{
    background:linear-gradient(160deg,rgba(10,37,64,.9),rgba(6,22,39,.95));
    border:1px solid rgba(255,201,60,.2);border-radius:24px;padding:2.5rem 1.5rem;
  }
  .versus h3{text-align:center;font-size:1.9rem;margin-bottom:.5rem}
  .versus .hint{text-align:center;color:var(--cielo);margin-bottom:2rem;font-size:.95rem}
  .compare{display:grid;grid-template-columns:1fr auto 1fr;gap:1rem;align-items:center}
  .col{text-align:center}
  .col h4{font-size:1.3rem;margin-bottom:.3rem}
  .col.messi h4{color:var(--azul)}
  .col.cr7 h4{color:var(--rojo)}
  .col .flag{font-size:.8rem;color:var(--cielo);letter-spacing:.1em}
  .vs{font-size:1.6rem;font-weight:900;color:var(--oro)}
  .rows{margin-top:2rem}
  .row{display:grid;grid-template-columns:1fr auto 1fr;gap:.6rem;align-items:center;
    padding:1rem 0;border-top:1px solid rgba(78,168,222,.15)}
  .cell{text-align:center;font-weight:800;font-size:1.5rem}
  .row .label{font-size:.75rem;color:var(--cielo);text-transform:uppercase;letter-spacing:.1em;
    align-self:center;font-weight:600}
  .win{color:var(--oro);position:relative}
  .win::after{content:"★";position:absolute;top:-14px;left:50%;transform:translateX(-50%);
    font-size:.8rem;color:var(--oro)}
  .lose{color:rgba(247,251,255,.35)}

  /* ---------- LO QUE CR7 NUNCA TENDRÁ ---------- */
  .never{text-align:center;background:
    radial-gradient(circle at 50% 50%,rgba(230,57,70,.15),transparent 70%),var(--azul-noche);
    border-radius:24px;padding:4rem 1.5rem;border:1px solid rgba(230,57,70,.3)}
  .never .big{
    font-size:clamp(2.5rem,10vw,6rem);font-weight:900;
    background:linear-gradient(90deg,var(--oro),var(--blanco),var(--oro));
    -webkit-background-clip:text;background-clip:text;color:transparent;
    animation:shine 3s linear infinite;background-size:200% auto;
  }
  @keyframes shine{to{background-position:200% center}}
  .never p{color:var(--cielo);max-width:560px;margin:1.5rem auto 0;font-size:1.1rem;line-height:1.6}

  /* ---------- GALERÍA TROFEOS ---------- */
  .trophies{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:1rem;margin-top:1rem}
  .trophy{background:linear-gradient(145deg,rgba(255,201,60,.1),rgba(6,22,39,.7));
    border:1px solid rgba(255,201,60,.25);border-radius:16px;padding:1.8rem 1rem;text-align:center;
    transition:.35s;cursor:default}
  .trophy:hover{transform:scale(1.05) rotate(-2deg);border-color:var(--oro);
    box-shadow:0 10px 30px rgba(255,201,60,.25)}
  .trophy .ico{font-size:2.5rem;filter:drop-shadow(0 0 10px var(--oro))}
  .trophy .t-name{font-weight:800;margin-top:.6rem;font-size:.95rem}
  .trophy .t-sub{color:var(--cielo);font-size:.78rem;margin-top:.2rem}

  /* ---------- FRASE ---------- */
  .quote{text-align:center;padding:6rem 1.5rem}
  .quote blockquote{font-size:clamp(1.5rem,5vw,2.6rem);font-weight:900;
    max-width:800px;margin:0 auto;line-height:1.2}
  .quote blockquote span{color:var(--oro)}
  .quote cite{display:block;margin-top:1.5rem;color:var(--cielo);font-style:normal;
    letter-spacing:.2em;text-transform:uppercase;font-size:.85rem}

  /* ---------- FOOTER ---------- */
  footer{text-align:center;padding:3rem 1.5rem;background:var(--azul-hondo);
    border-top:3px solid var(--oro)}
  footer .goat{font-size:2rem;font-weight:900;color:var(--oro)}
  footer p{color:var(--cielo);margin-top:.5rem;font-size:.9rem}

  @media(max-width:600px){
    .compare,.row{grid-template-columns:1fr auto 1fr}
    .cell{font-size:1.2rem}
    section{padding:4rem 1.2rem}
  }
</style>
</head>
<body>

<div class="progress" id="bar"></div>

<!-- HERO -->
<header class="hero">
  <div class="stars" id="stars"></div>
  <div class="eyebrow">Qatar · 18 de diciembre de 2022</div>
  <h1>LIONEL<br>MESSI</h1>
  <div class="cup">🏆</div>
  <p class="sub">El mejor jugador del mundo · Campeón del Mundo</p>
  <div class="scroll-hint">DESLIZA ▾</div>
</header>

<!-- CINTA -->
<div class="ribbon"><span>MESSI CAMPEÓN DEL MUNDO ✦ BALÓN DE ORO DEL TORNEO ✦ ARGENTINA 3 (4) — FRANCIA 3 (2) ✦ LA CONSAGRACIÓN DEL G.O.A.T ✦ </span></div>

<!-- INTRO -->
<section class="reveal">
  <h2 class="section-title">La cima del <span class="accent">fútbol</span></h2>
  <p class="lead">En Qatar 2022, Lionel Messi levantó la única copa que le faltaba y cerró la discusión: el mejor jugador de la historia. Una final eterna, un capitán inmortal y un país entero rendido a sus pies.</p>
  <div class="stats">
    <div class="stat"><span class="num" data-target="7">0</span><span class="lbl">Goles en el Mundial</span></div>
    <div class="stat"><span class="num" data-target="3">0</span><span class="lbl">Asistencias</span></div>
    <div class="stat"><span class="num" data-target="2">0</span><span class="lbl">Balones de Oro FIFA</span></div>
    <div class="stat"><span class="num" data-target="7">0</span><span class="lbl">Partidos jugados</span></div>
  </div>
</section>

<!-- FINAL TIMELINE -->
<section class="reveal">
  <h2 class="section-title">La final <span class="accent">inolvidable</span></h2>
  <p class="lead">Toca cada momento para revivir la noche más grande. Argentina y Francia firmaron la mejor final de la historia.</p>
  <div class="timeline" id="tl">
    <div class="tl-item"><div class="tl-time">23'</div><div class="tl-desc">Gol de Messi — penal</div><div class="tl-detail">El capitán abre el marcador con la calma de siempre. Argentina toma el control absoluto del partido.</div></div>
    <div class="tl-item"><div class="tl-time">36'</div><div class="tl-desc">Gol de Di María</div><div class="tl-detail">Una jugada colectiva de manual termina en el 2-0. La banda argentina explota de alegría.</div></div>
    <div class="tl-item"><div class="tl-time">108'</div><div class="tl-desc">Gol de Messi — prórroga</div><div class="tl-detail">En tiempo extra, Messi vuelve a aparecer para poner el 3-2 y acercar el sueño.</div></div>
    <div class="tl-item"><div class="tl-time">120'</div><div class="tl-desc">Atajada del Dibu Martínez</div><div class="tl-detail">El arquero salva el gol que habría sido la derrota. Héroe absoluto.</div></div>
    <div class="tl-item"><div class="tl-time">Penales</div><div class="tl-desc">¡ARGENTINA CAMPEÓN!</div><div class="tl-detail">4-2 en la tanda. Messi levanta la copa y sella su leyenda para siempre.</div></div>
  </div>
</section>

<!-- COMPARADOR -->
<section class="reveal">
  <div class="versus">
    <h3>El comparador <span style="color:var(--oro)">definitivo</span></h3>
    <p class="hint">Números que hablan por sí solos ✦ pasa el cursor sobre las tarjetas</p>
    <div class="compare">
      <div class="col messi"><h4>Messi</h4><div class="flag">🇦🇷 ARGENTINA</div></div>
      <div class="vs">VS</div>
      <div class="col cr7"><h4>Cristiano</h4><div class="flag">🇵🇹 PORTUGAL</div></div>
    </div>
    <div class="rows">
      <div class="row"><div class="cell win">1</div><div class="label">Copa del Mundo</div><div class="cell lose">0</div></div>
      <div class="row"><div class="cell win">8</div><div class="label">Balones de Oro</div><div class="cell lose">5</div></div>
      <div class="row"><div class="cell win">SÍ</div><div class="label">Balón de Oro del Mundial</div><div class="cell lose">NO</div></div>
      <div class="row"><div class="cell win">1</div><div class="label">Copa América</div><div class="cell lose">0</div></div>
    </div>
  </div>
</section>

<!-- LO QUE CR7 NUNCA TENDRÁ -->
<section class="reveal">
  <div class="never">
    <div class="eyebrow" style="display:inline-block;margin-bottom:1.5rem">Lo que Cristiano nunca podrá tener</div>
    <div class="big">LA COPA<br>DEL MUNDO</div>
    <p>Cristiano Ronaldo es un jugador extraordinario, pero hay un logro que su carrera nunca alcanzará: <strong style="color:var(--blanco)">levantar el trofeo más importante del planeta</strong>. Messi lo tiene. Esa es la diferencia entre ser grande y ser eterno.</p>
  </div>
</section>

<!-- TROFEOS -->
<section class="reveal">
  <h2 class="section-title">La <span class="accent">vitrina</span> del rey</h2>
  <p class="lead">Una carrera irrepetible, condecorada con todo lo que el fútbol puede dar.</p>
  <div class="trophies">
    <div class="trophy"><div class="ico">🏆</div><div class="t-name">Mundial 2022</div><div class="t-sub">Qatar</div></div>
    <div class="trophy"><div class="ico">🥇</div><div class="t-name">8 Balones de Oro</div><div class="t-sub">Récord absoluto</div></div>
    <div class="trophy"><div class="ico">⭐</div><div class="t-name">Copa América 2021</div><div class="t-sub">Con Argentina</div></div>
    <div class="trophy"><div class="ico">🏅</div><div class="t-name">Finalissima 2022</div><div class="t-sub">vs Italia</div></div>
    <div class="trophy"><div class="ico">🔵</div><div class="t-name">4 Champions</div><div class="t-sub">Barcelona</div></div>
    <div class="trophy"><div class="ico">👑</div><div class="t-name">Balón de Oro FIFA</div><div class="t-sub">Mejor del torneo</div></div>
  </div>
</section>

<!-- FRASE -->
<section class="quote reveal">
  <blockquote>"Sabía que <span>Dios</span> me iba a regalar esta copa. Presentía que iba a ser <span>ésta</span>."</blockquote>
  — Lionel Messi
</section>

<!-- FOOTER -->
<footer>
  <div class="goat">🐐 EL G.O.A.T.</div>
  <p>Lionel Andrés Messi · Campeón del Mundo Qatar 2022</p>
</footer>

<script>
  // barra de progreso
  const bar=document.getElementById('bar');
  addEventListener('scroll',()=>{
    const h=document.documentElement.scrollHeight-innerHeight;
    bar.style.width=(scrollY/h*100)+'%';
  });

  // estrellas doradas
  const sc=document.getElementById('stars');
  for(let i=0;i<45;i++){
    const s=document.createElement('div');s.className='star';
    const sz=Math.random()*3+1;
    s.style.width=s.style.height=sz+'px';
    s.style.left=Math.random()*100+'%';
    s.style.top=Math.random()*100+'%';
    s.style.animationDelay=Mat
