<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Mohit Shivankar | Full Stack Developer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Outfit:wght@300;400;600&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#070b14;--surface:#0e1626;--line:#1c2a44;--text:#d7e3f4;--muted:#7f93b2;
  --accent:#00ffff;--accent2:#7c5cff;--ok:#3dffa0;
  --mono:"Share Tech Mono",ui-monospace,Consolas,monospace;
  --sans:"Outfit",system-ui,-apple-system,"Segoe UI",sans-serif;
  box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px);
}
@media (prefers-color-scheme:light){
  :root:not([data-theme="dark"]){--bg:#f2f7fb;--surface:#ffffff;--line:#cfdbe8;--text:#12203a;--muted:#52678a;--accent:#007c8a;--accent2:#5b3fd9;--ok:#08874f}
}
:root[data-theme="dark"]{--bg:#070b14;--surface:#0e1626;--line:#1c2a44;--text:#d7e3f4;--muted:#7f93b2;--accent:#00ffff;--accent2:#7c5cff;--ok:#3dffa0}
html{scroll-padding-top:env(safe-area-inset-top,0px);scroll-behavior:smooth}
*,*::before,*::after{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--text);font-family:var(--sans);line-height:1.6;overflow-x:hidden}
#fx{position:fixed;inset:0;width:100%;height:100%;z-index:0;opacity:.55;pointer-events:none}
main{position:relative;z-index:1;max-width:980px;margin:0 auto;padding:0 22px 80px}
a{color:inherit}
:focus-visible{outline:2px solid var(--accent);outline-offset:3px;border-radius:4px}

/* hero */
.hero{min-height:88vh;display:flex;flex-direction:column;justify-content:center;gap:28px;padding:70px 0 40px}
.status{display:inline-flex;align-items:center;gap:10px;font-family:var(--mono);color:var(--ok);font-size:.95rem;width:fit-content;border:1px solid var(--line);border-radius:999px;padding:6px 14px;background:var(--surface)}
.dot{width:9px;height:9px;border-radius:50%;background:var(--ok);box-shadow:0 0 0 0 var(--ok);animation:pulse 2s infinite}
@keyframes pulse{0%{box-shadow:0 0 0 0 color-mix(in srgb,var(--ok) 70%,transparent)}70%{box-shadow:0 0 0 12px transparent}100%{box-shadow:0 0 0 0 transparent}}
h1{font-family:var(--mono);font-weight:400;font-size:clamp(2.1rem,6.2vw,4.4rem);line-height:1.08;margin:0;letter-spacing:-.01em;min-height:2.3em}
h1 .caret{display:inline-block;width:.5ch;height:.95em;background:var(--accent);vertical-align:-.1em;margin-left:4px;animation:blink 1s steps(1) infinite;box-shadow:0 0 16px var(--accent)}
@keyframes blink{50%{opacity:0}}
.sub{font-size:1.2rem;color:var(--muted);max-width:52ch;margin:0}
.sub b{color:var(--text);font-weight:600}
.cta{display:flex;flex-wrap:wrap;gap:12px}
.btn{font-family:var(--mono);text-decoration:none;padding:12px 22px;border-radius:8px;border:1px solid var(--accent);color:var(--accent);transition:background .2s,color .2s,box-shadow .2s}
.btn:hover{background:var(--accent);color:var(--bg);box-shadow:0 0 24px color-mix(in srgb,var(--accent) 50%,transparent)}
.btn.alt{border-color:var(--line);color:var(--text)}
.btn.alt:hover{background:var(--surface);color:var(--accent);border-color:var(--accent)}

/* terminal */
section{padding:46px 0 10px}
h2{font-family:var(--mono);font-weight:400;font-size:1.7rem;margin:0 0 20px;color:var(--text)}
h2::before{content:"~/";color:var(--accent)}
.term{background:var(--surface);border:1px solid var(--line);border-radius:12px;overflow:hidden;box-shadow:0 20px 60px -30px #000}
.bar{display:flex;align-items:center;gap:7px;padding:11px 16px;border-bottom:1px solid var(--line);font-family:var(--mono);color:var(--muted);font-size:.85rem}
.bar i{width:11px;height:11px;border-radius:50%;background:#ff5f57}.bar i:nth-child(2){background:#febc2e}.bar i:nth-child(3){background:#28c840}
.bar span{margin-left:10px}
.term pre{margin:0;padding:22px;font-family:var(--mono);font-size:clamp(.82rem,2.4vw,1.02rem);line-height:1.85;white-space:pre-wrap;word-break:break-word;min-height:17em}
.k{color:var(--accent)}.v{color:var(--text)}.p{color:var(--ok)}.c{color:var(--muted)}

/* about list */
.facts{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:16px}
.fact{border:1px solid var(--line);border-left:3px solid var(--accent2);border-radius:10px;padding:16px 18px;background:var(--surface)}
.fact h3{margin:0 0 4px;font-size:1.05rem;font-weight:600}
.fact p{margin:0;color:var(--muted)}

/* stack */
.group{margin-bottom:26px}
.group h3{font-family:var(--mono);font-weight:400;color:var(--muted);font-size:1rem;margin:0 0 12px}
.chips{display:flex;flex-wrap:wrap;gap:10px}
.chip{font-family:var(--mono);font-size:.95rem;padding:7px 14px;border:1px solid var(--line);border-radius:6px;background:var(--surface);transition:transform .2s,border-color .2s,color .2s}
.chip:hover{transform:translateY(-3px);border-color:var(--accent);color:var(--accent)}

/* contact */
.links{display:grid;grid-template-columns:repeat(auto-fit,minmax(210px,1fr));gap:14px}
.link{display:block;text-decoration:none;border:1px solid var(--line);background:var(--surface);border-radius:10px;padding:16px 18px;transition:border-color .2s,transform .2s}
.link:hover{border-color:var(--accent);transform:translateY(-3px)}
.link small{display:block;color:var(--muted);font-family:var(--mono)}
.link span{overflow-wrap:anywhere}
footer{margin-top:60px;color:var(--muted);font-family:var(--mono);font-size:.9rem;text-align:center}

/* reveal for lower sections only */
.rv{opacity:0;transform:translateY(18px);transition:opacity .7s,transform .7s}
.rv.in{opacity:1;transform:none}
@media (prefers-reduced-motion:reduce){
  *{animation:none!important;transition:none!important}
  .rv{opacity:1;transform:none}
  html{scroll-behavior:auto}
}
</style>
</head>
<body>
<canvas id="fx" aria-hidden="true"></canvas>
<main>
  <header class="hero">
    <div class="status"><span class="dot"></span>open to opportunities</div>
    <h1 id="type" aria-label="Programming is the power to create BIG"><span id="t"></span><span class="caret"></span></h1>
    <p class="sub"><b>Mohit Shivankar</b> builds modern Android apps and full stack products, with a soft spot for algorithms, clean architecture and secure code.</p>
    <div class="cta">
      <a class="btn" href="#contact">Get in touch</a>
      <a class="btn alt" href="#stack">See the stack</a>
    </div>
  </header>

  <section id="about" class="rv">
    <h2>whoami</h2>
    <div class="term">
      <div class="bar"><i></i><i></i><i></i><span>mohit@nagpur: ~</span></div>
      <pre id="term" aria-label="whoami output: Mohit Shivankar, Full Stack Developer, Nagpur Maharashtra India, BSc in Data Science 2024 to 2027, exploring data structures, backend systems, ML models, Flutter and cyber security, open to opportunities."></pre>
    </div>
  </section>

  <section class="rv">
    <h2>focus</h2>
    <div class="facts">
      <div class="fact"><h3>Android and Flutter</h3><p>Building modern mobile apps in Java and Dart.</p></div>
      <div class="fact"><h3>Algorithms and architecture</h3><p>Clean structure, solid data structures, backend systems.</p></div>
      <div class="fact"><h3>Cyber security</h3><p>Secure coding habits from the first commit.</p></div>
      <div class="fact"><h3>Data science and ML</h3><p>BSc in Data Science (2024 to 2027), working with PyTorch and scikit-learn.</p></div>
    </div>
    <p style="color:var(--muted);margin-top:18px;font-family:var(--mono)">Always shipping. Always learning.</p>
  </section>

  <section id="stack" class="rv">
    <h2>stack</h2>
    <div class="group"><h3>languages and shell</h3><div class="chips">
      <span class="chip">Java</span><span class="chip">Python</span><span class="chip">Dart</span><span class="chip">Bash</span><span class="chip">PowerShell</span><span class="chip">Windows Terminal</span></div></div>
    <div class="group"><h3>mobile and desktop</h3><div class="chips">
      <span class="chip">Flutter</span><span class="chip">JavaFX</span><span class="chip">OpenGL</span></div></div>
    <div class="group"><h3>backend</h3><div class="chips">
      <span class="chip">Flask</span><span class="chip">FastAPI</span><span class="chip">Django</span><span class="chip">Node.js</span><span class="chip">Express</span><span class="chip">Apache</span><span class="chip">Postman</span><span class="chip">Thunder Client</span><span class="chip">JSON</span></div></div>
    <div class="group"><h3>databases</h3><div class="chips">
      <span class="chip">MySQL</span><span class="chip">SQLite</span><span class="chip">Supabase</span><span class="chip">MongoDB</span></div></div>
    <div class="group"><h3>data and ML</h3><div class="chips">
      <span class="chip">NumPy</span><span class="chip">Pandas</span><span class="chip">PyTorch</span><span class="chip">scikit-learn</span><span class="chip">Matplotlib</span><span class="chip">OpenCV</span></div></div>
    <div class="group"><h3>tools and design</h3><div class="chips">
      <span class="chip">Git</span><span class="chip">GitHub</span><span class="chip">GitLab</span><span class="chip">GitHub Actions</span><span class="chip">Krita</span><span class="chip">Canva</span></div></div>
  </section>

  <section id="contact" class="rv">
    <h2>contact</h2>
    <div class="links">
      <a class="link" href="mailto:Contact@mr-silicon.in"><small>email</small><span>Contact@mr-silicon.in</span></a>
      <a class="link" href="tel:+918788358100"><small>phone</small><span>+91 87883-58100</span></a>
      <a class="link" href="https://linkedin.com/in/mohit-shivankar-a87964340" target="_blank" rel="noopener"><small>linkedin</small><span>mohit-shivankar</span></a>
      <a class="link" href="https://x.com/codexpr000" target="_blank" rel="noopener"><small>x</small><span>@codexpr000</span></a>
      <a class="link" href="https://instagram.com/code_x_pro1" target="_blank" rel="noopener"><small>instagram</small><span>@code_x_pro1</span></a>
      <a class="link" href="https://discord.gg/.codexpro" target="_blank" rel="noopener"><small>discord</small><span>.codexpro</span></a>
    </div>
    <footer>Nagpur, Maharashtra, India 🇮🇳</footer>
  </section>
</main>

<script>
(function(){
  var reduce = window.matchMedia("(prefers-reduced-motion: reduce)").matches;

  /* hero typing */
  var phrases = ["Programming is the Power to Create BIG","Android Developer | Java | Flutter","Always shipping. Always learning."];
  var el = document.getElementById("t");
  if(reduce){ el.textContent = phrases[0]; }
  else {
    var pi=0, ci=0, del=false;
    (function tick(){
      var s = phrases[pi];
      if(!del){ ci++; el.textContent = s.slice(0,ci); if(ci===s.length){ del=true; return setTimeout(tick, pi===0?3200:1800);} return setTimeout(tick,70); }
      ci--; el.textContent = s.slice(0,ci);
      if(ci===0){ del=false; pi=(pi+1)%phrases.length; return setTimeout(tick,350);} setTimeout(tick,32);
    })();
  }

  /* whoami terminal */
  var lines = [
    '<span class="p">$</span> whoami --verbose',
    '',
    '<span class="k">name</span>                : <span class="v">Mohit Shivankar</span>',
    '<span class="k">role</span>                : <span class="v">Full Stack Developer</span>',
    '<span class="k">location</span>            : <span class="v">Nagpur, Maharashtra, India</span>',
    '<span class="k">education</span>           : <span class="v">BSc in Data Science (2024 - 2027)</span>',
    '<span class="k">currently_exploring</span> : <span class="v">Data Structures, Backend Systems, ML Models, Android (Flutter), Cyber Security</span>',
    '<span class="k">status</span>              : <span class="p">open to opportunities</span>'
  ];
  var term = document.getElementById("term");
  var started = false;
  function run(){
    if(started) return; started = true;
    if(reduce){ term.innerHTML = lines.join("\n"); return; }
    var i = 0;
    (function next(){
      if(i >= lines.length){ term.innerHTML += '\n<span class="p">$</span> <span class="caret-t" style="background:var(--accent);display:inline-block;width:.6ch;height:1em;vertical-align:-.15em;animation:blink 1s steps(1) infinite"></span>'; return; }
      term.innerHTML += (i? "\n":"") + lines[i]; i++;
      setTimeout(next, i===1 ? 700 : 260);
    })();
  }

  /* reveal on scroll */
  var rv = document.querySelectorAll(".rv");
  if("IntersectionObserver" in window){
    var io = new IntersectionObserver(function(es){
      es.forEach(function(e){
        if(e.isIntersecting){ e.target.classList.add("in"); if(e.target.id==="about") run(); io.unobserve(e.target); }
      });
    },{threshold:.15});
    rv.forEach(function(n){ io.observe(n); });
  } else { rv.forEach(function(n){ n.classList.add("in"); }); run(); }

  /* background: drifting binary rain in cyan */
  var cv = document.getElementById("fx");
  if(!cv || reduce) return;
  var ctx = cv.getContext("2d"), cols, drops, fs = 16, W, H;
  function size(){
    W = cv.width = innerWidth; H = cv.height = innerHeight;
    cols = Math.ceil(W/fs); drops = [];
    for(var i=0;i<cols;i++) drops[i] = Math.random()*H/fs;
  }
  size(); addEventListener("resize", size);
  var glyphs = "01{}<>/;=+*#";
  var accent = getComputedStyle(document.documentElement).getPropertyValue("--accent").trim() || "#00ffff";
  var last = 0;
  function draw(t){
    requestAnimationFrame(draw);
    if(t - last < 60) return; last = t;
    var bg = getComputedStyle(document.documentElement).getPropertyValue("--bg").trim();
    accent = getComputedStyle(document.documentElement).getPropertyValue("--accent").trim();
    ctx.fillStyle = bg + "22"; ctx.fillRect(0,0,W,H);
    ctx.font = fs + "px monospace"; ctx.fillStyle = accent;
    for(var i=0;i<cols;i++){
      if(Math.random() < .35) ctx.fillText(glyphs.charAt(Math.floor(Math.random()*glyphs.length)), i*fs, drops[i]*fs);
      if(drops[i]*fs > H && Math.random() > .975) drops[i] = 0;
      drops[i] += .5;
    }
  }
  requestAnimationFrame(draw);
})();
</script>
</body>
</html>
