<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1"/>
<title>teethaking</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Rajdhani:wght@300;400;600;700&family=Share+Tech+Mono&display=swap');

*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --void:#000008;
  --b:#00d4ff;
  --r:#ff2d55;
  --p:#bf5fff;
  --w:#e8f0ff;
}

html,body{width:100%;height:100%;overflow:hidden;background:var(--void);color:var(--w);font-family:'Rajdhani',sans-serif}

/* ── CANVAS BG ── */
#bg{position:fixed;inset:0;z-index:0}

/* ── SCAN LINES ── */
#scan{
  position:fixed;inset:0;z-index:1;pointer-events:none;
  background:repeating-linear-gradient(0deg,transparent,transparent 2px,rgba(0,0,10,.15) 2px,rgba(0,0,10,.15) 4px);
}
#scan::after{
  content:'';position:absolute;inset:0;
  background:linear-gradient(180deg,transparent 0%,rgba(0,212,255,.015) 50%,transparent 100%);
  animation:scanline 4s linear infinite;
}
@keyframes scanline{from{transform:translateY(-100%)}to{transform:translateY(100%)}}

/* ── VIGNETTE ── */
#vig{
  position:fixed;inset:0;z-index:2;pointer-events:none;
  background:radial-gradient(ellipse at center,transparent 40%,rgba(0,0,8,.85) 100%);
}

/* ── GLITCH OVERLAY ── */
#glitch-overlay{
  position:fixed;inset:0;z-index:3;pointer-events:none;
  mix-blend-mode:screen;opacity:0;
  background:linear-gradient(135deg,rgba(0,212,255,.08),rgba(191,95,255,.08));
  animation:glitch-flash 7s infinite;
}
@keyframes glitch-flash{
  0%,95%,100%{opacity:0}
  96%{opacity:1;transform:translate(-3px,1px)}
  97%{opacity:0}
  98%{opacity:1;transform:translate(3px,-1px)}
  99%{opacity:0}
}

/* ── MAIN ── */
#main{
  position:relative;z-index:10;
  width:100%;height:100vh;
  display:flex;flex-direction:column;align-items:center;justify-content:center;
  gap:0;
}

/* ── DOMAIN RINGS ── */
#rings{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;pointer-events:none;z-index:1}
.ring{
  position:absolute;border-radius:50%;border:1px solid;
  animation:ring-expand linear infinite;
}
.ring:nth-child(1){width:120px;height:120px;border-color:rgba(0,212,255,.6);animation-duration:3s;animation-delay:0s}
.ring:nth-child(2){width:120px;height:120px;border-color:rgba(191,95,255,.5);animation-duration:3s;animation-delay:.6s}
.ring:nth-child(3){width:120px;height:120px;border-color:rgba(255,45,85,.4);animation-duration:3s;animation-delay:1.2s}
.ring:nth-child(4){width:120px;height:120px;border-color:rgba(0,212,255,.35);animation-duration:3s;animation-delay:1.8s}
.ring:nth-child(5){width:120px;height:120px;border-color:rgba(191,95,255,.3);animation-duration:3s;animation-delay:2.4s}
@keyframes ring-expand{
  0%{transform:scale(1);opacity:.8}
  100%{transform:scale(12);opacity:0}
}

/* ── HERO SECTION ── */
#hero{position:relative;z-index:10;text-align:center}

.eyebrow{
  font-family:'Share Tech Mono',monospace;
  font-size:11px;letter-spacing:.5em;color:var(--b);
  text-transform:uppercase;margin-bottom:16px;
  animation:flicker 3s ease-in-out infinite;
}
@keyframes flicker{
  0%,100%{opacity:.7}40%{opacity:.7}41%{opacity:.2}42%{opacity:.7}85%{opacity:.7}86%{opacity:.15}87%{opacity:.7}
}

.hero-name{
  font-family:'Bebas Neue',sans-serif;
  font-size:clamp(100px,20vw,200px);
  line-height:.85;letter-spacing:.06em;
  position:relative;display:inline-block;
  background:linear-gradient(135deg,#fff 0%,var(--b) 35%,var(--p) 65%,var(--r) 100%);
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;
  background-size:300% 300%;
  animation:name-gradient 4s ease infinite, name-in 1s ease both;
  filter:drop-shadow(0 0 40px rgba(0,212,255,.4));
}
@keyframes name-gradient{
  0%{background-position:0% 50%}50%{background-position:100% 50%}100%{background-position:0% 50%}
}
@keyframes name-in{from{opacity:0;transform:translateY(40px) scale(.9)}to{opacity:1;transform:none}}

/* Glitch effect on name */
.hero-name::before,.hero-name::after{
  content:'TOBE';
  position:absolute;top:0;left:0;right:0;
  font-family:'Bebas Neue',sans-serif;
  font-size:inherit;letter-spacing:inherit;
  -webkit-text-fill-color:transparent;
  background-clip:text;-webkit-background-clip:text;
}
.hero-name::before{
  background:linear-gradient(135deg,var(--b),transparent);
  animation:glitch-1 6s infinite;clip-path:polygon(0 30%,100% 30%,100% 50%,0 50%);
}
.hero-name::after{
  background:linear-gradient(135deg,var(--r),transparent);
  animation:glitch-2 6s infinite;clip-path:polygon(0 60%,100% 60%,100% 75%,0 75%);
}
@keyframes glitch-1{
  0%,90%,100%{transform:none;opacity:0}
  91%{transform:translate(-4px,2px);opacity:.6}
  92%{transform:translate(4px,-2px);opacity:.6}
  93%{transform:none;opacity:0}
  94%{transform:translate(-2px,1px);opacity:.4}
  95%{transform:none;opacity:0}
}
@keyframes glitch-2{
  0%,88%,100%{transform:none;opacity:0}
  89%{transform:translate(4px,-2px);opacity:.5}
  90%{transform:translate(-4px,2px);opacity:.5}
  91%{transform:none;opacity:0}
  93%{transform:translate(2px,-1px);opacity:.3}
  94%{transform:none;opacity:0}
}

.sub-row{
  display:flex;align-items:center;justify-content:center;gap:24px;
  margin-top:12px;opacity:0;animation:fadeUp .8s ease .4s both;
}
.sub-tag{
  font-family:'Share Tech Mono',monospace;font-size:11px;letter-spacing:.3em;color:rgba(232,240,255,.35);
}
.sub-divider{width:40px;height:1px;background:linear-gradient(90deg,transparent,rgba(0,212,255,.4),transparent)}

/* ── QUOTE ── */
#quote-box{
  margin-top:32px;height:28px;position:relative;
  opacity:0;animation:fadeUp .8s ease .6s both;
}
.q{
  position:absolute;left:50%;transform:translateX(-50%);
  font-family:'Rajdhani',sans-serif;font-size:15px;font-weight:300;
  font-style:italic;color:rgba(232,240,255,.45);
  white-space:nowrap;opacity:0;transition:opacity .6s ease;
  letter-spacing:.05em;
}
.q.show{opacity:1}

/* ── STATUS ── */
.status-row{
  display:flex;align-items:center;justify-content:center;gap:12px;
  margin-top:28px;opacity:0;animation:fadeUp .8s ease .8s both;
}
.dot{width:7px;height:7px;border-radius:50%;background:#39ff14;position:relative}
.dot::after{
  content:'';position:absolute;inset:-4px;border-radius:50%;
  border:1px solid #39ff14;
  animation:ping 1.5s ease-out infinite;
}
@keyframes ping{0%{transform:scale(1);opacity:.8}100%{transform:scale(2.5);opacity:0}}
.status-txt{font-family:'Share Tech Mono',monospace;font-size:10px;letter-spacing:.4em;color:rgba(57,255,20,.7)}

/* ── BARS ── */
#bars{
  margin-top:48px;width:min(580px,85vw);
  opacity:0;animation:fadeUp .8s ease 1s both;
}
.bar-label-row{display:flex;justify-content:space-between;align-items:center;margin-bottom:6px}
.bl{font-family:'Share Tech Mono',monospace;font-size:9px;letter-spacing:.3em;color:rgba(232,240,255,.3)}
.bv{font-family:'Share Tech Mono',monospace;font-size:9px;letter-spacing:.1em;color:rgba(0,212,255,.5)}
.track{height:2px;background:rgba(255,255,255,.04);border-radius:2px;overflow:visible;margin-bottom:18px;position:relative}
.fill{height:2px;border-radius:2px;position:relative;width:0;transition:width 2s cubic-bezier(.16,1,.3,1)}
.fill::after{content:'';position:absolute;right:0;top:-3px;width:6px;height:6px;border-radius:50%;background:inherit;filter:blur(2px)}
.fill-b{background:linear-gradient(90deg,var(--b),var(--p))}
.fill-r{background:linear-gradient(90deg,var(--r),var(--p))}
.fill-inf{background:linear-gradient(90deg,var(--p),var(--b),var(--r));animation:inf-pulse 2s ease-in-out infinite;width:100%!important}
@keyframes inf-pulse{0%,100%{opacity:.6;filter:brightness(1)}50%{opacity:1;filter:brightness(1.5)}}

/* ── CHIPS ── */
#chips{
  display:flex;flex-wrap:wrap;justify-content:center;gap:10px;
  margin-top:32px;width:min(620px,90vw);
  opacity:0;animation:fadeUp .8s ease 1.2s both;
}
.chip{
  padding:7px 16px;border-radius:4px;
  font-family:'Share Tech Mono',monospace;font-size:10px;letter-spacing:.2em;
  border:1px solid rgba(0,212,255,.15);color:rgba(232,240,255,.5);
  background:rgba(0,212,255,.03);
  position:relative;overflow:hidden;cursor:default;
  transition:all .25s ease;
}
.chip::before{
  content:'';position:absolute;inset:0;
  background:linear-gradient(135deg,rgba(0,212,255,.1),rgba(191,95,255,.1));
  opacity:0;transition:opacity .25s;
}
.chip:hover::before{opacity:1}
.chip:hover{border-color:rgba(0,212,255,.5);color:var(--w);transform:translateY(-2px);
  box-shadow:0 8px 24px rgba(0,212,255,.15)}

/* ── DOMAIN BANNER ── */
#domain{
  margin-top:40px;
  font-family:'Bebas Neue',sans-serif;
  font-size:clamp(28px,5vw,52px);
  letter-spacing:.2em;
  position:relative;
  background:linear-gradient(90deg,var(--b),var(--p),var(--r),var(--p),var(--b));
  background-size:300% 100%;
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;
  animation:domain-shimmer 3s linear infinite, fadeUp .8s ease 1.4s both, domain-glitch 8s infinite;
  opacity:0;
}
@keyframes domain-shimmer{0%{background-position:0%}100%{background-position:300%}}
@keyframes domain-glitch{
  0%,96%,100%{transform:none;filter:none}
  97%{transform:translate(-3px,0) skewX(-5deg);filter:hue-rotate(90deg)}
  98%{transform:translate(3px,0) skewX(3deg);filter:hue-rotate(-90deg)}
  99%{transform:none;filter:none}
}

/* ── ORBS ── */
#orbs{
  display:flex;gap:48px;margin-top:20px;
  opacity:0;animation:fadeUp .8s ease 1.5s both;
}
.orb{
  width:52px;height:52px;border-radius:50%;
  display:flex;align-items:center;justify-content:center;
  font-family:'Share Tech Mono',monospace;font-size:8px;letter-spacing:.15em;
  position:relative;
}
.orb::before{
  content:'';position:absolute;inset:-8px;border-radius:50%;
  animation:orb-glow 2.5s ease-in-out infinite;
}
.ob{border:1px solid rgba(0,212,255,.5);color:var(--b);background:rgba(0,212,255,.06)}
.ob::before{background:radial-gradient(var(--b),transparent 70%);animation-delay:0s}
.op{border:1px solid rgba(191,95,255,.5);color:var(--p);background:rgba(191,95,255,.06)}
.op::before{background:radial-gradient(var(--p),transparent 70%);animation-delay:.8s}
.or_{border:1px solid rgba(255,45,85,.5);color:var(--r);background:rgba(255,45,85,.06)}
.or_::before{background:radial-gradient(var(--r),transparent 70%);animation-delay:1.6s}
@keyframes orb-glow{
  0%,100%{transform:scale(1);opacity:.15}
  50%{transform:scale(1.6);opacity:.4}
}

/* ── FOOTER ── */
#foot{
  margin-top:28px;
  font-family:'Share Tech Mono',monospace;font-size:9px;letter-spacing:.4em;
  color:rgba(232,240,255,.12);
  opacity:0;animation:fadeUp .6s ease 1.8s both;
}

@keyframes fadeUp{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:none}}
</style>
</head>
<body>

<canvas id="bg"></canvas>
<div id="scan"></div>
<div id="vig"></div>
<div id="glitch-overlay"></div>

<div id="main">
  <div id="rings">
    <div class="ring"></div><div class="ring"></div><div class="ring"></div>
    <div class="ring"></div><div class="ring"></div>
  </div>

  <div id="hero">
    <div class="eyebrow">∞ &nbsp; full stack developer &nbsp; ∞</div>
    <div class="hero-name">TOBE</div>
    <div class="sub-row">
      <div class="sub-divider"></div>
      <span class="sub-tag">teethaking</span>
      <div class="sub-divider"></div>
    </div>
  </div>

  <div id="quote-box">
    <div class="q show" id="q0">"Throughout Heaven and Earth — I alone am the honored one."</div>
    <div class="q" id="q1">"I'm the strongest. Sorry to keep you waiting."</div>
    <div class="q" id="q2">"Don't worry. I already won before I started."</div>
    <div class="q" id="q3">"Limitless. The technique. Also my commit history."</div>
    <div class="q" id="q4">"My pull requests don't need reviewing. They're already perfect."</div>
    <div class="q" id="q5">"You can't hit what your eyes can't follow. Bugs included."</div>
  </div>

  <div class="status-row">
    <div class="dot"></div>
    <span class="status-txt">open &nbsp;to &nbsp;work</span>
  </div>

  <div id="bars">
    <div class="bar-label-row"><span class="bl">FRONTEND</span><span class="bv">92</span></div>
    <div class="track"><div class="fill fill-b" data-w="92"></div></div>

    <div class="bar-label-row"><span class="bl">BACKEND</span><span class="bv">85</span></div>
    <div class="track"><div class="fill fill-b" data-w="85"></div></div>

    <div class="bar-label-row"><span class="bl">DATABASES</span><span class="bv">80</span></div>
    <div class="track"><div class="fill fill-r" data-w="80"></div></div>

    <div class="bar-label-row"><span class="bl">PROBLEM SOLVING</span><span class="bv">95</span></div>
    <div class="track"><div class="fill fill-r" data-w="95"></div></div>

    <div class="bar-label-row"><span class="bl">EGO</span><span class="bv" style="color:var(--p)">∞</span></div>
    <div class="track"><div class="fill fill-inf"></div></div>
  </div>

  <div id="chips">
    <div class="chip">JavaScript</div>
    <div class="chip">TypeScript</div>
    <div class="chip">React</div>
    <div class="chip">Next.js</div>
    <div class="chip">Python</div>
    <div class="chip">Node.js</div>
    <div class="chip">Tailwind</div>
    <div class="chip">PostgreSQL</div>
    <div class="chip">MongoDB</div>
  </div>

  <div id="domain">✦ &nbsp; UNLIMITED VOID &nbsp; ✦</div>

  <div id="orbs">
    <div class="orb ob">BLUE</div>
    <div class="orb op">∞</div>
    <div class="orb or_">RED</div>
  </div>

  <div id="foot">∞ · teethaking · tobe · all domains · ∞</div>
</div>

<script>
// ── PARTICLE CANVAS ──
const canvas = document.getElementById('bg');
const ctx = canvas.getContext('2d');
let W, H;

function resize(){W=canvas.width=window.innerWidth;H=canvas.height=window.innerHeight}
resize(); window.addEventListener('resize',resize);

// Particles
const COLS=['rgba(0,212,255,','rgba(191,95,255,','rgba(255,45,85,'];
const pts=[];
for(let i=0;i<120;i++){
  pts.push({
    x:Math.random()*2000,y:Math.random()*2000,
    vx:(Math.random()-.5)*.4,vy:(Math.random()-.5)*.4,
    r:Math.random()*1.2+.2,
    c:COLS[Math.floor(Math.random()*COLS.length)],
    a:Math.random()*.4+.05
  });
}

// Energy lines (lightning-like streaks)
const lines=[];
for(let i=0;i<6;i++){
  lines.push({
    x1:Math.random()*2000,y1:Math.random()*2000,
    x2:Math.random()*2000,y2:Math.random()*2000,
    alpha:0,ttl:0,maxTTL:40,
    c:COLS[Math.floor(Math.random()*COLS.length)]
  });
}

let t=0;
function draw(){
  ctx.clearRect(0,0,W,H);
  // Deep void bg
  ctx.fillStyle='#000008';
  ctx.fillRect(0,0,W,H);

  // Central glow
  const grd=ctx.createRadialGradient(W/2,H/2,0,W/2,H/2,Math.min(W,H)*.55);
  grd.addColorStop(0,'rgba(0,212,255,0.04)');
  grd.addColorStop(.5,'rgba(191,95,255,0.025)');
  grd.addColorStop(1,'transparent');
  ctx.fillStyle=grd; ctx.fillRect(0,0,W,H);

  // Particles
  pts.forEach(p=>{
    p.x+=p.vx; p.y+=p.vy;
    if(p.x<0)p.x=W; if(p.x>W)p.x=0;
    if(p.y<0)p.y=H; if(p.y>H)p.y=0;
    ctx.beginPath();
    ctx.arc(p.x%W,p.y%H,p.r,0,Math.PI*2);
    ctx.fillStyle=p.c+p.a+')'; ctx.fill();
  });

  // Connection lines between nearby particles
  for(let i=0;i<pts.length;i++){
    for(let j=i+1;j<pts.length;j++){
      const dx=pts[i].x-pts[j].x, dy=pts[i].y-pts[j].y;
      const d=Math.sqrt(dx*dx+dy*dy);
      if(d<80){
        ctx.beginPath();
        ctx.moveTo(pts[i].x,pts[i].y);
        ctx.lineTo(pts[j].x,pts[j].y);
        ctx.strokeStyle=`rgba(0,212,255,${.04*(1-d/80)})`;
        ctx.lineWidth=.4; ctx.stroke();
      }
    }
  }

  // Energy bursts
  lines.forEach(l=>{
    if(l.ttl<=0){
      if(Math.random()<.008){
        const cx=W/2+(Math.random()-.5)*400,cy=H/2+(Math.random()-.5)*300;
        const ang=Math.random()*Math.PI*2, len=80+Math.random()*180;
        l.x1=cx; l.y1=cy;
        l.x2=cx+Math.cos(ang)*len; l.y2=cy+Math.sin(ang)*len;
        l.ttl=l.maxTTL; l.c=COLS[Math.floor(Math.random()*COLS.length)];
      }
    } else {
      l.ttl--;
      const progress=l.ttl/l.maxTTL;
      const alpha=progress<.5?progress*2:(1-progress)*2;
      ctx.beginPath(); ctx.moveTo(l.x1,l.y1); ctx.lineTo(l.x2,l.y2);
      ctx.strokeStyle=l.c+(alpha*.7)+')'; ctx.lineWidth=.8+alpha; ctx.stroke();
      // glow
      ctx.strokeStyle=l.c+(alpha*.2)+')'; ctx.lineWidth=4; ctx.stroke();
    }
  });

  // Pulsing center orb
  const pulse=Math.sin(t*.04);
  const orbGrd=ctx.createRadialGradient(W/2,H/2,0,W/2,H/2,60+pulse*15);
  orbGrd.addColorStop(0,`rgba(0,212,255,${.06+pulse*.02})`);
  orbGrd.addColorStop(1,'transparent');
  ctx.fillStyle=orbGrd; ctx.fillRect(0,0,W,H);

  t++;
  requestAnimationFrame(draw);
}
draw();

// ── BARS ANIMATE ──
setTimeout(()=>{
  document.querySelectorAll('.fill[data-w]').forEach(f=>{
    f.style.width=f.dataset.w+'%';
  });
},1200);

// ── QUOTE ROTATOR ──
const qs=document.querySelectorAll('.q');
let qi=0;
setInterval(()=>{
  qs[qi].classList.remove('show');
  qi=(qi+1)%qs.length;
  qs[qi].classList.add('show');
},3800);
</script>
</body>
</html>
