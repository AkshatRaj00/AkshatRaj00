<!DOCTYPE html>
<html lang="en" data-theme="dark">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Akshat Raj — OnePersonAI</title>
<meta name="description" content="Akshat Raj — AI Engineer, Founder of OnePersonAI. Conscious Artificial Intelligence from India.">
<meta name="keywords" content="Akshat Raj, AkshatRaj00, OnePersonAI, AI Engineer, Conscious AI, AGI Developer, Indore, India, Full Stack Developer">
<meta property="og:title" content="Akshat Raj — OnePersonAI">
<meta property="og:description" content="Founder of OnePersonAI. Building Conscious AI.">
<meta property="og:url" content="https://onepersonai.in">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@100;300;400;500;700&family=Space+Grotesk:wght@300;400;500;700&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #020408;
  --surface: #060b10;
  --surface-2: #0a1018;
  --border: rgba(0,255,136,0.08);
  --green: #00ff88;
  --green-faint: rgba(0,255,136,0.06);
  --green-glow: rgba(0,255,136,0.35);
  --text: #e8f5f0;
  --text-muted: #5a8a6e;
  --text-faint: #1e3a2a;
  --red: #ff3355;
  --blue: #00aaff;
  --mono: 'JetBrains Mono', monospace;
  --body: 'Space Grotesk', sans-serif;
  --ease: cubic-bezier(0.16,1,0.3,1);
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
html{scroll-behavior:smooth;}
body{background:var(--bg);color:var(--text);font-family:var(--body);min-height:100dvh;overflow-x:hidden;cursor:crosshair;}
::selection{background:rgba(0,255,136,0.15);color:var(--green);}

/* SCANLINES */
body::before{content:'';position:fixed;inset:0;background:repeating-linear-gradient(0deg,transparent,transparent 2px,rgba(0,0,0,0.025) 2px,rgba(0,0,0,0.025) 4px);pointer-events:none;z-index:9999;}

#matrix-canvas{position:fixed;top:0;left:0;width:100%;height:100%;opacity:0.035;z-index:0;pointer-events:none;}

.cursor-dot{position:fixed;width:5px;height:5px;background:var(--green);border-radius:50%;pointer-events:none;z-index:10000;transform:translate(-50%,-50%);box-shadow:0 0 10px var(--green-glow);transition:opacity .3s;}
.cursor-ring{position:fixed;width:32px;height:32px;border:1px solid rgba(0,255,136,0.35);border-radius:50%;pointer-events:none;z-index:9999;transform:translate(-50%,-50%);transition:width .2s var(--ease),height .2s var(--ease),border-color .2s;}

.wrap{position:relative;z-index:1;min-height:100dvh;display:flex;flex-direction:column;}

/* NAV */
nav{position:fixed;top:0;left:0;right:0;z-index:100;padding:1.4rem 3rem;display:flex;align-items:center;justify-content:space-between;border-bottom:1px solid var(--border);background:linear-gradient(to bottom,rgba(2,4,8,0.96),transparent);backdrop-filter:blur(16px);}
.nav-logo{font-family:var(--mono);font-size:.7rem;color:var(--green);letter-spacing:.2em;text-transform:uppercase;text-decoration:none;}
.nav-logo em{color:var(--text-muted);font-style:normal;}
.nav-status{display:flex;align-items:center;gap:.5rem;font-family:var(--mono);font-size:.6rem;color:var(--text-muted);letter-spacing:.1em;}
.dot-live{width:6px;height:6px;background:var(--green);border-radius:50%;animation:pulse 2s ease-in-out infinite;box-shadow:0 0 8px var(--green);}
@keyframes pulse{0%,100%{opacity:1;transform:scale(1);}50%{opacity:.4;transform:scale(.7);}}

/* HERO */
.hero{min-height:100dvh;display:flex;flex-direction:column;justify-content:center;padding:8rem 3rem 4rem;position:relative;overflow:hidden;}
.hero-gridlines{position:absolute;inset:0;background-image:linear-gradient(rgba(0,255,136,0.025) 1px,transparent 1px),linear-gradient(90deg,rgba(0,255,136,0.025) 1px,transparent 1px);background-size:64px 64px;mask-image:radial-gradient(ellipse 75% 65% at 50% 50%,black,transparent);}
.hero-glow{position:absolute;width:700px;height:700px;background:radial-gradient(circle,rgba(0,255,136,0.05) 0%,transparent 65%);top:50%;left:50%;transform:translate(-50%,-50%);animation:glow 5s ease-in-out infinite;pointer-events:none;}
@keyframes glow{0%,100%{opacity:.5;transform:translate(-50%,-50%) scale(1);}50%{opacity:1;transform:translate(-50%,-50%) scale(1.2);}}

.hero-inner{position:relative;max-width:820px;}

.hero-pre{font-family:var(--mono);font-size:.65rem;color:var(--green);letter-spacing:.25em;text-transform:uppercase;margin-bottom:1.5rem;display:flex;align-items:center;gap:.75rem;opacity:0;animation:fadeup .7s var(--ease) .3s forwards;}
.hero-pre::before{content:'';width:36px;height:1px;background:var(--green);}

.hero-name{font-family:var(--mono);font-size:clamp(3.5rem,9vw,8rem);font-weight:700;line-height:.88;color:var(--text);margin-bottom:1.5rem;opacity:0;animation:fadeup .7s var(--ease) .5s forwards;}
.hero-name .accent{color:var(--green);position:relative;display:inline-block;}
.hero-name .accent::after{content:'';position:absolute;bottom:-2px;left:0;right:0;height:2px;background:var(--green);box-shadow:0 0 18px var(--green-glow);transform:scaleX(0);transform-origin:left;animation:linerev .5s var(--ease) 1.2s forwards;}
@keyframes linerev{to{transform:scaleX(1);}}

.hero-sub{font-family:var(--mono);font-size:clamp(.65rem,1.4vw,.85rem);color:var(--text-muted);letter-spacing:.08em;margin-bottom:2.5rem;opacity:0;animation:fadeup .7s var(--ease) .7s forwards;}
.hero-sub .sep{margin:0 .9rem;color:var(--text-faint);}

.typer-wrap{font-family:var(--mono);font-size:clamp(.8rem,1.7vw,1rem);color:var(--green);min-height:1.7em;margin-bottom:3rem;opacity:0;animation:fadeup .7s var(--ease) .9s forwards;}
.blink{display:inline-block;width:2px;height:1em;background:var(--green);vertical-align:text-bottom;margin-left:2px;animation:blink 1s step-end infinite;}
@keyframes blink{0%,100%{opacity:1;}50%{opacity:0;}}

.cta-row{display:flex;align-items:center;gap:1.25rem;flex-wrap:wrap;opacity:0;animation:fadeup .7s var(--ease) 1.1s forwards;}
.btn-p{font-family:var(--mono);font-size:.7rem;letter-spacing:.15em;text-transform:uppercase;color:var(--bg);background:var(--green);border:none;padding:.85rem 1.8rem;cursor:pointer;text-decoration:none;display:inline-flex;align-items:center;gap:.5rem;transition:box-shadow .2s var(--ease),transform .2s var(--ease);}
.btn-p:hover{box-shadow:0 0 28px var(--green-glow);transform:translateY(-2px);}
.btn-p:active{transform:translateY(0);}
.btn-g{font-family:var(--mono);font-size:.7rem;letter-spacing:.15em;text-transform:uppercase;color:var(--text-muted);background:none;border:1px solid var(--border);padding:.85rem 1.8rem;cursor:pointer;text-decoration:none;display:inline-flex;align-items:center;gap:.5rem;transition:border-color .2s,color .2s,transform .2s;}
.btn-g:hover{border-color:var(--green);color:var(--green);transform:translateY(-2px);}

/* TERMINAL */
.terminal{background:var(--surface);border:1px solid var(--border);padding:1.4rem;font-family:var(--mono);font-size:.72rem;line-height:1.85;max-width:440px;position:absolute;right:3rem;top:50%;transform:translateY(-50%);opacity:0;animation:fadeup .7s var(--ease) 1.3s forwards;}
.t-bar{display:flex;align-items:center;gap:.45rem;margin-bottom:1.1rem;padding-bottom:.65rem;border-bottom:1px solid var(--border);}
.td{width:10px;height:10px;border-radius:50%;}
.td.r{background:#ff5f57;}.td.y{background:#ffbd2e;}.td.g{background:#28ca41;}
.t-ttl{color:var(--text-faint);font-size:.6rem;letter-spacing:.1em;margin-left:auto;}
.tl .p{color:var(--green);}.tl .v{color:var(--blue);}.tl .s{color:#ffd700;}.tl .c{color:var(--text-faint);}

@keyframes fadeup{from{opacity:0;transform:translateY(16px);}to{opacity:1;transform:translateY(0);}}

/* SECTIONS */
section{padding:5.5rem 3rem;position:relative;z-index:1;}
.slabel{font-family:var(--mono);font-size:.6rem;color:var(--green);letter-spacing:.3em;text-transform:uppercase;margin-bottom:.6rem;display:flex;align-items:center;gap:.6rem;}
.slabel::before{content:attr(data-n);color:var(--text-faint);}
.stitle{font-family:var(--mono);font-size:clamp(1.3rem,2.8vw,2.2rem);font-weight:700;color:var(--text);margin-bottom:2.5rem;line-height:1.1;}

/* GLITCH */
.glitch{position:relative;}
.glitch::before,.glitch::after{content:attr(data-t);position:absolute;top:0;left:0;width:100%;height:100%;pointer-events:none;}
.glitch::before{color:var(--red);animation:glitch 7s step-end infinite;clip-path:inset(0 0 50% 0);}
.glitch::after{color:var(--blue);animation:glitch 7s step-end infinite .1s;clip-path:inset(50% 0 0 0);}
@keyframes glitch{0%,93%,100%{clip-path:none;transform:none;}94%{clip-path:inset(20% 0 50% 0);transform:translate(-3px,0);}95%{clip-path:inset(60% 0 10% 0);transform:translate(3px,0);}96%{clip-path:inset(40% 0 30% 0);transform:translate(-1px,0);}97%{clip-path:none;transform:none;}}

/* STATS */
.stats{display:flex;border:1px solid var(--border);max-width:860px;margin-bottom:0;}
.sblock{flex:1;padding:2rem 2.2rem;border-right:1px solid var(--border);}
.sblock:last-child{border-right:none;}
.snum{font-family:var(--mono);font-size:clamp(1.8rem,3.2vw,2.6rem);font-weight:700;color:var(--green);display:block;line-height:1;margin-bottom:.4rem;}
.slbl{font-family:var(--mono);font-size:.58rem;color:var(--text-faint);text-transform:uppercase;letter-spacing:.15em;}

/* STACK GRID */
.sgrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(130px,1fr));gap:1px;background:var(--border);border:1px solid var(--border);max-width:860px;}
.si{background:var(--bg);padding:1.1rem 1.3rem;font-family:var(--mono);font-size:.68rem;color:var(--text-muted);letter-spacing:.04em;transition:color .18s,background .18s;cursor:default;position:relative;overflow:hidden;}
.si::before{content:'';position:absolute;bottom:0;left:0;width:0;height:1px;background:var(--green);transition:width .3s var(--ease);}
.si:hover{color:var(--green);background:var(--green-faint);}
.si:hover::before{width:100%;}
.scat{font-size:.52rem;color:var(--text-faint);text-transform:uppercase;letter-spacing:.18em;margin-bottom:.2rem;display:block;}

/* LINKS */
.lgrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(250px,1fr));gap:1px;background:var(--border);border:1px solid var(--border);max-width:860px;}
.li{background:var(--bg);padding:1.6rem 1.8rem;display:flex;align-items:center;gap:1.3rem;text-decoration:none;transition:background .18s;position:relative;overflow:hidden;}
.li::after{content:'';position:absolute;left:0;top:0;bottom:0;width:0;background:var(--green);transition:width .3s var(--ease);}
.li:hover{background:var(--green-faint);}
.li:hover::after{width:2px;}
.lico{font-family:var(--mono);font-size:1.1rem;color:var(--green);width:22px;text-align:center;flex-shrink:0;}
.linfo{flex:1;}
.lname{font-family:var(--mono);font-size:.7rem;color:var(--text);letter-spacing:.05em;display:block;margin-bottom:.15rem;}
.lhandle{font-family:var(--mono);font-size:.6rem;color:var(--text-muted);}
.larrow{color:var(--text-faint);font-size:.75rem;font-family:var(--mono);transition:color .18s,transform .18s;}
.li:hover .larrow{color:var(--green);transform:translateX(4px);}

/* FOOTER */
footer{border-top:1px solid var(--border);padding:1.75rem 3rem;display:flex;align-items:center;justify-content:space-between;position:relative;z-index:1;}
.fcopy{font-family:var(--mono);font-size:.6rem;color:var(--text-faint);letter-spacing:.1em;}
.fcopy span{color:var(--green);}

hr.divider{border:none;border-top:1px solid var(--border);margin:0 3rem;}

/* REVEAL */
.reveal{opacity:1;}
@supports (animation-timeline: scroll()) {
  .reveal{opacity:0;clip-path:inset(100% 0 0 0);animation:rclip linear both;animation-timeline:view();animation-range:entry 0% entry 80%;}
  @keyframes rclip{to{opacity:1;clip-path:inset(0 0 0 0);}}
}

/* SEO HIDDEN */
.seo{position:absolute;width:1px;height:1px;overflow:hidden;clip:rect(0,0,0,0);white-space:nowrap;}

/* MOBILE */
@media(max-width:900px){
  nav{padding:1.1rem 1.4rem;}
  .hero{padding:6.5rem 1.4rem 3.5rem;}
  .terminal{display:none;}
  section{padding:3.5rem 1.4rem;}
  .stats{flex-direction:column;}
  .sblock{border-right:none;border-bottom:1px solid var(--border);}
  .sblock:last-child{border-bottom:none;}
  footer{flex-direction:column;gap:.75rem;padding:1.4rem;text-align:center;}
  hr.divider{margin:0 1.4rem;}
}
</style>
</head>
<body>

<div class="seo" aria-hidden="true">
  <h1>Akshat Raj AkshatRaj00 AI Engineer Founder OnePersonAI India</h1>
  <p>Akshat Raj is an AI Engineer, Full-Stack Developer, and Founder of OnePersonAI from Indore, Madhya Pradesh, India. GitHub AkshatRaj00, LinkedIn akshatraj00, building Conscious Artificial Intelligence systems. Website onepersonai.in</p>
</div>

<canvas id="matrix-canvas"></canvas>
<div class="cursor-dot" id="cdot"></div>
<div class="cursor-ring" id="cring"></div>

<div class="wrap">

<nav>
  <a href="#" class="nav-logo">AKSHAT<em>.</em>RAJ</a>
  <div class="nav-status">
    <div class="dot-live"></div>
    <span>ONLINE — INDORE, INDIA</span>
  </div>
</nav>

<section class="hero">
  <div class="hero-gridlines"></div>
  <div class="hero-glow"></div>
  <div class="hero-inner">
    <div class="hero-pre">IDENTITY.LOAD()</div>
    <h1 class="hero-name">
      <span class="glitch" data-t="AKSHAT">AKSHAT</span><br>
      <span class="accent">RAJ</span>
    </h1>
    <p class="hero-sub">AI ENGINEER<span class="sep">//</span>FULL-STACK DEV<span class="sep">//</span>FOUNDER@ONEPERSONAI</p>
    <div class="typer-wrap"><span id="typer"></span><span class="blink"></span></div>
    <div class="cta-row">
      <a href="https://onepersonai.in" target="_blank" rel="noopener noreferrer" class="btn-p">&#x2192; ONEPERSONAI.IN</a>
      <a href="https://github.com/AkshatRaj00" target="_blank" rel="noopener noreferrer" class="btn-g">&#x2295; GITHUB</a>
    </div>
  </div>

  <div class="terminal" aria-hidden="true">
    <div class="t-bar">
      <div class="td r"></div><div class="td y"></div><div class="td g"></div>
      <span class="t-ttl">akshat@onepersonai ~ zsh</span>
    </div>
    <div class="tl"><span class="p">&#x276F;</span> <span style="color:var(--text)">whoami</span></div>
    <div class="tl"><span class="v">akshat_raj</span> <span class="c">// AkshatRaj00</span></div>
    <div class="tl">&nbsp;</div>
    <div class="tl"><span class="p">&#x276F;</span> <span style="color:var(--text)">cat</span> <span class="s">mission.txt</span></div>
    <div class="tl"><span class="v">Building Conscious AI</span></div>
    <div class="tl"><span class="v">where machines understand,</span></div>
    <div class="tl"><span class="v">not just compute.</span></div>
    <div class="tl">&nbsp;</div>
    <div class="tl"><span class="p">&#x276F;</span> <span style="color:var(--text)">ping</span> <span class="s">onepersonai.in</span></div>
    <div class="tl"><span class="v">64 bytes: ttl=64</span> <span class="c">// online</span></div>
    <div class="tl"><span class="p">&#x276F;</span> <span id="livetime"></span><span class="blink"></span></div>
  </div>
</section>

<hr class="divider">

<section>
  <div class="slabel" data-n="01_">METRICS</div>
  <div class="stats reveal">
    <div class="sblock"><span class="snum" data-target="10">0</span><span class="slbl">// production apps</span></div>
    <div class="sblock"><span class="snum" data-target="3">0</span><span class="slbl">// years building</span></div>
    <div class="sblock"><span class="snum" data-target="1">0</span><span class="slbl">// company founded</span></div>
    <div class="sblock"><span class="snum">&#x221E;</span><span class="slbl">// limits</span></div>
  </div>
</section>

<hr class="divider">

<section>
  <div class="slabel" data-n="02_">STACK</div>
  <h2 class="stitle">TECH.STACK()</h2>
  <div class="sgrid reveal">
    <div class="si"><span class="scat">Frontend</span>Next.js</div>
    <div class="si"><span class="scat">Frontend</span>React</div>
    <div class="si"><span class="scat">Style</span>Tailwind CSS</div>
    <div class="si"><span class="scat">Mobile</span>Flutter</div>
    <div class="si"><span class="scat">Mobile</span>Dart</div>
    <div class="si"><span class="scat">Language</span>TypeScript</div>
    <div class="si"><span class="scat">Language</span>Python</div>
    <div class="si"><span class="scat">Backend</span>FastAPI</div>
    <div class="si"><span class="scat">Backend</span>Node.js</div>
    <div class="si"><span class="scat">Database</span>Supabase</div>
    <div class="si"><span class="scat">Database</span>Firebase</div>
    <div class="si"><span class="scat">AI</span>Gemini API</div>
    <div class="si"><span class="scat">AI</span>TensorFlow</div>
    <div class="si"><span class="scat">Cloud</span>Vercel</div>
    <div class="si"><span class="scat">Tool</span>Docker</div>
    <div class="si"><span class="scat">Payment</span>Razorpay</div>
  </div>
</section>

<hr class="divider">

<section>
  <div class="slabel" data-n="03_">CONNECT</div>
  <h2 class="stitle">REACH.OUT()</h2>
  <div class="lgrid reveal">
    <a href="https://onepersonai.in" target="_blank" rel="noopener noreferrer" class="li">
      <div class="lico">&#x25A1;</div>
      <div class="linfo"><span class="lname">ONEPERSONAI</span><span class="lhandle">onepersonai.in</span></div>
      <span class="larrow">&#x2192;</span>
    </a>
    <a href="https://github.com/AkshatRaj00" target="_blank" rel="noopener noreferrer" class="li">
      <div class="lico">&#x2295;</div>
      <div class="linfo"><span class="lname">GITHUB</span><span class="lhandle">@AkshatRaj00</span></div>
      <span class="larrow">&#x2192;</span>
    </a>
    <a href="https://linkedin.com/in/akshatraj00" target="_blank" rel="noopener noreferrer" class="li">
      <div class="lico">&#x25CE;</div>
      <div class="linfo"><span class="lname">LINKEDIN</span><span class="lhandle">akshatraj00</span></div>
      <span class="larrow">&#x2192;</span>
    </a>
    <a href="mailto:akshat@onepersonai.com" class="li">
      <div class="lico">&#x2709;</div>
      <div class="linfo"><span class="lname">EMAIL</span><span class="lhandle">akshat@onepersonai.com</span></div>
      <span class="larrow">&#x2192;</span>
    </a>
    <a href="https://akshat-raj-portfolio-lfy7.vercel.app" target="_blank" rel="noopener noreferrer" class="li">
      <div class="lico">&#x25B3;</div>
      <div class="linfo"><span class="lname">PORTFOLIO</span><span class="lhandle">akshat-raj-portfolio</span></div>
      <span class="larrow">&#x2192;</span>
    </a>
    <a href="https://www.youtube.com/@OnePersonAI" target="_blank" rel="noopener noreferrer" class="li">
      <div class="lico">&#x25BA;</div>
      <div class="linfo"><span class="lname">YOUTUBE</span><span class="lhandle">@OnePersonAI</span></div>
      <span class="larrow">&#x2192;</span>
    </a>
  </div>
</section>

<footer>
  <p class="fcopy">&#x00A9; 2024-2026 <span>AKSHAT RAJ</span> // ONEPERSONAI.IN</p>
  <p class="fcopy" id="ftime"></p>
</footer>

</div>

<script>
// MATRIX RAIN
(function(){
  const c=document.getElementById('matrix-canvas'),ctx=c.getContext('2d');
  let cols,drops;
  function resize(){c.width=innerWidth;c.height=innerHeight;cols=Math.floor(c.width/18);drops=Array(cols).fill(1);}
  resize();addEventListener('resize',resize);
  const ch='アイウエオABCDEF0123456789><{}[]';
  function draw(){
    ctx.fillStyle='rgba(2,4,8,0.045)';ctx.fillRect(0,0,c.width,c.height);
    ctx.fillStyle='#00ff88';ctx.font='13px JetBrains Mono,monospace';
    drops.forEach((y,i)=>{
      ctx.fillText(ch[Math.floor(Math.random()*ch.length)],i*18,y*18);
      if(y*18>c.height&&Math.random()>.975)drops[i]=0;
      drops[i]++;
    });
  }
  setInterval(draw,55);
})();

// CURSOR
(function(){
  const dot=document.getElementById('cdot'),ring=document.getElementById('cring');
  let mx=0,my=0,rx=0,ry=0;
  document.addEventListener('mousemove',e=>{mx=e.clientX;my=e.clientY;dot.style.left=mx+'px';dot.style.top=my+'px';});
  (function anim(){rx+=(mx-rx)*.11;ry+=(my-ry)*.11;ring.style.left=rx+'px';ring.style.top=ry+'px';requestAnimationFrame(anim);})();
  document.querySelectorAll('a,button,.si').forEach(el=>{
    el.addEventListener('mouseenter',()=>{ring.style.width='52px';ring.style.height='52px';ring.style.borderColor='rgba(0,255,136,.7)';});
    el.addEventListener('mouseleave',()=>{ring.style.width='32px';ring.style.height='32px';ring.style.borderColor='rgba(0,255,136,.35)';});
  });
})();

// TYPEWRITER
(function(){
  const el=document.getElementById('typer');
  const lines=['BUILDING CONSCIOUS AI SYSTEMS','FOUNDER @ ONEPERSONAI','FULL-STACK DEVELOPER','AGI RESEARCHER','EMOTION-AWARE ARCHITECTURES'];
  let li=0,ci=0,del=false;
  function type(){
    const cur=lines[li];
    if(!del){el.textContent=cur.slice(0,++ci);if(ci===cur.length){del=true;setTimeout(type,2200);return;}}
    else{el.textContent=cur.slice(0,--ci);if(ci===0){del=false;li=(li+1)%lines.length;}}
    setTimeout(type,del?35:75);
  }
  setTimeout(type,1900);
})();

// LIVE TIME
(function(){
  const t=document.getElementById('livetime'),f=document.getElementById('ftime');
  function u(){const s=new Date().toISOString().replace('T',' ').slice(0,19)+' IST';if(t)t.textContent='date // '+s;if(f)f.textContent=s;}
  u();setInterval(u,1000);
})();

// COUNTER
(function(){
  const obs=new IntersectionObserver(entries=>{
    entries.forEach(e=>{
      if(!e.isIntersecting)return;
      const el=e.target,tgt=parseInt(el.dataset.target);
      if(!tgt)return;
      const start=performance.now(),dur=1100;
      (function tick(now){
        const p=Math.min((now-start)/dur,1),ease=1-Math.pow(1-p,3);
        el.textContent=Math.round(ease*tgt)+(tgt>=10?'+':'');
        if(p<1)requestAnimationFrame(tick);
        else el.textContent=tgt+(tgt>=10?'+':'');
      })(start);
      obs.unobserve(el);
    });
  },{threshold:.5});
  document.querySelectorAll('.snum[data-target]').forEach(n=>obs.observe(n));
})();
</script>
</body>
</html>
