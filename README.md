<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>teethaking — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Syne:wght@400;700;800&family=DM+Mono:ital,wght@0,400;0,500;1,400&display=swap" rel="stylesheet" />
<style>
  :root {
    --void: #030712;
    --blue: #60c8ff;
    --red: #ff4c6a;
    --purple: #c084fc;
    --white: #f0f4ff;
    --muted: #4a5568;
    --border: rgba(96, 200, 255, 0.15);
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--void);
    color: var(--white);
    font-family: 'Syne', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
    cursor: none;
  }

  /* Custom cursor */
  .cursor {
    position: fixed;
    width: 12px; height: 12px;
    background: var(--blue);
    border-radius: 50%;
    pointer-events: none;
    z-index: 9999;
    transition: transform 0.1s ease;
    mix-blend-mode: screen;
  }
  .cursor-ring {
    position: fixed;
    width: 36px; height: 36px;
    border: 1px solid rgba(96,200,255,0.4);
    border-radius: 50%;
    pointer-events: none;
    z-index: 9998;
    transition: all 0.15s ease;
  }

  /* Particle canvas */
  #particles {
    position: fixed;
    inset: 0;
    z-index: 0;
    pointer-events: none;
  }

  /* Infinity rings background */
  .infinity-bg {
    position: fixed;
    inset: 0;
    z-index: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    pointer-events: none;
    overflow: hidden;
  }
  .ring {
    position: absolute;
    border-radius: 50%;
    border: 1px solid rgba(96, 200, 255, 0.04);
    animation: pulse-ring 8s ease-in-out infinite;
  }
  .ring:nth-child(1) { width: 300px; height: 300px; animation-delay: 0s; }
  .ring:nth-child(2) { width: 550px; height: 550px; animation-delay: 1s; border-color: rgba(192,132,252,0.04); }
  .ring:nth-child(3) { width: 800px; height: 800px; animation-delay: 2s; }
  .ring:nth-child(4) { width: 1100px; height: 1100px; animation-delay: 3s; border-color: rgba(255,76,106,0.03); }
  .ring:nth-child(5) { width: 1400px; height: 1400px; animation-delay: 4s; }

  @keyframes pulse-ring {
    0%, 100% { transform: scale(1); opacity: 0.5; }
    50% { transform: scale(1.04); opacity: 1; }
  }

  /* Main layout */
  .container {
    position: relative;
    z-index: 1;
    max-width: 860px;
    margin: 0 auto;
    padding: 80px 32px 120px;
  }

  /* ── HERO ── */
  .hero {
    text-align: center;
    margin-bottom: 100px;
    animation: fadeUp 1s ease both;
  }

  .hero-eyebrow {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.3em;
    color: var(--blue);
    text-transform: uppercase;
    margin-bottom: 24px;
    opacity: 0;
    animation: fadeUp 0.8s ease 0.2s both;
  }

  .hero-name {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(72px, 14vw, 140px);
    line-height: 0.9;
    letter-spacing: 0.02em;
    background: linear-gradient(135deg, var(--white) 0%, var(--blue) 50%, var(--purple) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    opacity: 0;
    animation: fadeUp 0.8s ease 0.4s both, shimmer 6s linear 1.2s infinite;
    background-size: 200% 200%;
  }

  @keyframes shimmer {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }

  .hero-sub {
    font-family: 'DM Mono', monospace;
    font-size: 13px;
    color: var(--muted);
    letter-spacing: 0.15em;
    margin-top: 20px;
    opacity: 0;
    animation: fadeUp 0.8s ease 0.6s both;
  }

  /* Rotating quote */
  .quote-wrap {
    margin-top: 48px;
    height: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    animation: fadeUp 0.8s ease 0.8s both;
  }
  .quote {
    font-family: 'Syne', sans-serif;
    font-size: clamp(13px, 2vw, 16px);
    font-style: italic;
    color: rgba(240,244,255,0.55);
    max-width: 520px;
    text-align: center;
    position: absolute;
    opacity: 0;
    transition: opacity 0.8s ease;
  }
  .quote.active { opacity: 1; }

  /* Status pill */
  .status {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    margin-top: 32px;
    padding: 8px 20px;
    border: 1px solid rgba(96,200,255,0.2);
    border-radius: 100px;
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.15em;
    color: var(--blue);
    opacity: 0;
    animation: fadeUp 0.8s ease 1s both;
  }
  .status-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: #4ade80;
    animation: blink 1.4s ease-in-out infinite;
  }
  @keyframes blink {
    0%,100% { opacity: 1; }
    50% { opacity: 0.2; }
  }

  /* ── DIVIDER ── */
  .divider {
    display: flex;
    align-items: center;
    gap: 16px;
    margin: 64px 0 48px;
    opacity: 0;
    animation: fadeUp 0.6s ease both;
  }
  .divider-line { flex: 1; height: 1px; background: var(--border); }
  .divider-glyph {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.2em;
    color: rgba(96,200,255,0.3);
  }

  /* ── SECTION LABEL ── */
  .section-label {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.35em;
    color: var(--blue);
    text-transform: uppercase;
    margin-bottom: 32px;
    opacity: 0;
    animation: fadeUp 0.6s ease both;
  }

  /* ── TECH GRID ── */
  .tech-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
    gap: 12px;
    margin-bottom: 80px;
  }

  .tech-chip {
    position: relative;
    padding: 14px 16px;
    border: 1px solid var(--border);
    border-radius: 6px;
    text-align: center;
    font-family: 'DM Mono', monospace;
    font-size: 12px;
    color: rgba(240,244,255,0.65);
    overflow: hidden;
    cursor: none;
    opacity: 0;
    animation: fadeUp 0.5s ease both;
    transition: border-color 0.3s, color 0.3s, transform 0.3s;
    background: rgba(255,255,255,0.015);
  }
  .tech-chip::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, rgba(96,200,255,0.06), rgba(192,132,252,0.06));
    opacity: 0;
    transition: opacity 0.3s;
  }
  .tech-chip:hover::before { opacity: 1; }
  .tech-chip:hover {
    border-color: rgba(96,200,255,0.4);
    color: var(--white);
    transform: translateY(-3px);
  }
  .tech-chip .tech-icon {
    display: block;
    font-size: 20px;
    margin-bottom: 6px;
  }

  /* ── CURSED ENERGY BARS ── */
  .bars { margin-bottom: 80px; }
  .bar-row {
    display: flex;
    align-items: center;
    gap: 20px;
    margin-bottom: 20px;
    opacity: 0;
    animation: fadeUp 0.5s ease both;
  }
  .bar-label {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.2em;
    color: rgba(240,244,255,0.4);
    width: 120px;
    flex-shrink: 0;
    text-transform: uppercase;
  }
  .bar-track {
    flex: 1;
    height: 2px;
    background: rgba(255,255,255,0.05);
    border-radius: 2px;
    overflow: hidden;
  }
  .bar-fill {
    height: 100%;
    border-radius: 2px;
    width: 0%;
    transition: width 1.5s cubic-bezier(0.16, 1, 0.3, 1);
  }
  .bar-fill.blue  { background: linear-gradient(90deg, var(--blue), var(--purple)); }
  .bar-fill.red   { background: linear-gradient(90deg, var(--red), var(--purple)); }
  .bar-fill.inf   { background: linear-gradient(90deg, var(--purple), var(--blue)); animation: pulse-bar 2s ease-in-out infinite; }
  @keyframes pulse-bar {
    0%,100% { opacity:1; }
    50% { opacity:0.6; }
  }
  .bar-val {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    color: rgba(96,200,255,0.6);
    width: 28px;
    text-align: right;
  }

  /* ── DOMAIN EXPANSION ── */
  .domain {
    position: relative;
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 48px 40px;
    text-align: center;
    overflow: hidden;
    margin-bottom: 80px;
    opacity: 0;
    animation: fadeUp 0.8s ease both;
  }
  .domain::before {
    content: '';
    position: absolute;
    inset: -1px;
    border-radius: 12px;
    background: linear-gradient(135deg, rgba(96,200,255,0.1), transparent, rgba(192,132,252,0.1));
    z-index: -1;
  }
  .domain-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 56px;
    letter-spacing: 0.12em;
    background: linear-gradient(90deg, var(--blue), var(--purple), var(--red));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: domain-flicker 4s ease-in-out infinite;
  }
  @keyframes domain-flicker {
    0%,100% { opacity:1; filter: blur(0px); }
    48% { opacity:1; filter: blur(0px); }
    50% { opacity:0.6; filter: blur(1px); }
    52% { opacity:1; filter: blur(0px); }
  }
  .domain-sub {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.3em;
    color: rgba(240,244,255,0.25);
    margin-top: 8px;
    text-transform: uppercase;
  }
  .domain-orbs {
    display: flex;
    justify-content: center;
    gap: 32px;
    margin-top: 36px;
  }
  .orb {
    width: 48px; height: 48px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'DM Mono', monospace;
    font-size: 9px;
    letter-spacing: 0.1em;
    position: relative;
  }
  .orb::before {
    content: '';
    position: absolute;
    inset: -6px;
    border-radius: 50%;
    opacity: 0.15;
    animation: orb-pulse 3s ease-in-out infinite;
  }
  .orb-blue { background: rgba(96,200,255,0.1); border: 1px solid rgba(96,200,255,0.3); color: var(--blue); }
  .orb-blue::before { background: radial-gradient(var(--blue), transparent); animation-delay: 0s; }
  .orb-red  { background: rgba(255,76,106,0.1); border: 1px solid rgba(255,76,106,0.3); color: var(--red); }
  .orb-red::before  { background: radial-gradient(var(--red), transparent); animation-delay: 1s; }
  .orb-prp  { background: rgba(192,132,252,0.1); border: 1px solid rgba(192,132,252,0.3); color: var(--purple); }
  .orb-prp::before  { background: radial-gradient(var(--purple), transparent); animation-delay: 2s; }
  @keyframes orb-pulse {
    0%,100% { transform: scale(1); opacity: 0.15; }
    50% { transform: scale(1.5); opacity: 0.3; }
  }

  /* ── FOOTER ── */
  .footer {
    text-align: center;
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.25em;
    color: rgba(240,244,255,0.15);
    text-transform: uppercase;
    opacity: 0;
    animation: fadeUp 0.6s ease both;
  }
  .footer span { color: rgba(96,200,255,0.3); }

  @keyframes fadeUp {
    from { opacity:0; transform: translateY(24px); }
    to   { opacity:1; transform: translateY(0); }
  }
</style>
</head>
<body>

<div class="cursor" id="cursor"></div>
<div class="cursor-ring" id="cursorRing"></div>

<canvas id="particles"></canvas>

<div class="infinity-bg">
  <div class="ring"></div>
  <div class="ring"></div>
  <div class="ring"></div>
  <div class="ring"></div>
  <div class="ring"></div>
</div>

<div class="container">

  <!-- HERO -->
  <div class="hero">
    <p class="hero-eyebrow">∞ &nbsp; Full Stack Developer &nbsp; ∞</p>
    <h1 class="hero-name">TOBE</h1>
    <p class="hero-sub">teethaking &nbsp;/&nbsp; open to work</p>

    <div class="quote-wrap">
      <p class="quote active" id="q0">"Throughout Heaven and Earth — I alone am the honored one."</p>
      <p class="quote" id="q1">"I'm the strongest. Sorry to keep you waiting."</p>
      <p class="quote" id="q2">"Don't worry. I'm the strongest there is."</p>
      <p class="quote" id="q3">"If you were wondering — yes, I do look this good while shipping."</p>
      <p class="quote" id="q4">"Limitless. That's the technique. Also the commit history."</p>
      <p class="quote" id="q5">"I don't need to open a domain. My pull requests do it for me."</p>
    </div>

    <div class="status">
      <span class="status-dot"></span>
      OPEN TO WORK
    </div>
  </div>

  <!-- TECH -->
  <div class="divider" style="animation-delay:1.1s">
    <div class="divider-line"></div>
    <div class="divider-glyph">CURSED TOOLS</div>
    <div class="divider-line"></div>
  </div>

  <p class="section-label" style="animation-delay:1.2s">⌇ TECHNIQUE ARSENAL</p>

  <div class="tech-grid">
    <div class="tech-chip" style="animation-delay:1.3s"><span class="tech-icon">⚡</span>JavaScript</div>
    <div class="tech-chip" style="animation-delay:1.35s"><span class="tech-icon">🔷</span>TypeScript</div>
    <div class="tech-chip" style="animation-delay:1.4s"><span class="tech-icon">⚛️</span>React</div>
    <div class="tech-chip" style="animation-delay:1.45s"><span class="tech-icon">▲</span>Next.js</div>
    <div class="tech-chip" style="animation-delay:1.5s"><span class="tech-icon">🐍</span>Python</div>
    <div class="tech-chip" style="animation-delay:1.55s"><span class="tech-icon">🟩</span>Node.js</div>
    <div class="tech-chip" style="animation-delay:1.6s"><span class="tech-icon">🌊</span>Tailwind</div>
    <div class="tech-chip" style="animation-delay:1.65s"><span class="tech-icon">🐘</span>PostgreSQL</div>
    <div class="tech-chip" style="animation-delay:1.7s"><span class="tech-icon">🍃</span>MongoDB</div>
  </div>

  <!-- BARS -->
  <div class="divider" style="animation-delay:1.75s">
    <div class="divider-line"></div>
    <div class="divider-glyph">SIX EYES</div>
    <div class="divider-line"></div>
  </div>

  <p class="section-label" style="animation-delay:1.8s">⌇ CURSED ENERGY OUTPUT</p>

  <div class="bars">
    <div class="bar-row" style="animation-delay:1.85s">
      <span class="bar-label">Frontend</span>
      <div class="bar-track"><div class="bar-fill blue" data-w="92"></div></div>
      <span class="bar-val">92</span>
    </div>
    <div class="bar-row" style="animation-delay:1.9s">
      <span class="bar-label">Backend</span>
      <div class="bar-track"><div class="bar-fill blue" data-w="85"></div></div>
      <span class="bar-val">85</span>
    </div>
    <div class="bar-row" style="animation-delay:1.95s">
      <span class="bar-label">Databases</span>
      <div class="bar-track"><div class="bar-fill red" data-w="80"></div></div>
      <span class="bar-val">80</span>
    </div>
    <div class="bar-row" style="animation-delay:2.0s">
      <span class="bar-label">Problem Solving</span>
      <div class="bar-track"><div class="bar-fill red" data-w="95"></div></div>
      <span class="bar-val">95</span>
    </div>
    <div class="bar-row" style="animation-delay:2.05s">
      <span class="bar-label">Ego</span>
      <div class="bar-track"><div class="bar-fill inf" data-w="100"></div></div>
      <span class="bar-val">∞</span>
    </div>
  </div>

  <!-- DOMAIN -->
  <div class="divider" style="animation-delay:2.1s">
    <div class="divider-line"></div>
    <div class="divider-glyph">∞</div>
    <div class="divider-line"></div>
  </div>

  <div class="domain" style="animation-delay:2.2s">
    <div class="domain-title">UNLIMITED VOID</div>
    <p class="domain-sub">Domain Expansion — Active</p>
    <div class="domain-orbs">
      <div class="orb orb-blue">BLUE</div>
      <div class="orb orb-prp">∞</div>
      <div class="orb orb-red">RED</div>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer" style="animation-delay:2.5s">
    <span>∞</span> &nbsp; teethaking &nbsp; · &nbsp; Tobe &nbsp; · &nbsp; All Domains &nbsp; <span>∞</span>
  </div>

</div>

<script>
  // Cursor
  const cursor = document.getElementById('cursor');
  const ring = document.getElementById('cursorRing');
  let mx = 0, my = 0, rx = 0, ry = 0;
  document.addEventListener('mousemove', e => {
    mx = e.clientX; my = e.clientY;
    cursor.style.left = mx - 6 + 'px';
    cursor.style.top  = my - 6 + 'px';
  });
  (function animateRing() {
    rx += (mx - rx - 18) * 0.12;
    ry += (my - ry - 18) * 0.12;
    ring.style.left = rx + 'px';
    ring.style.top  = ry + 'px';
    requestAnimationFrame(animateRing);
  })();

  // Particles
  const canvas = document.getElementById('particles');
  const ctx = canvas.getContext('2d');
  let W, H, particles = [];
  function resize() {
    W = canvas.width  = window.innerWidth;
    H = canvas.height = window.innerHeight;
  }
  resize();
  window.addEventListener('resize', resize);

  const COLORS = ['rgba(96,200,255,', 'rgba(192,132,252,', 'rgba(255,76,106,'];
  for (let i = 0; i < 55; i++) {
    particles.push({
      x: Math.random() * 1920,
      y: Math.random() * 1080,
      r: Math.random() * 1.5 + 0.3,
      dx: (Math.random() - 0.5) * 0.3,
      dy: (Math.random() - 0.5) * 0.3,
      c: COLORS[Math.floor(Math.random() * COLORS.length)],
      a: Math.random() * 0.5 + 0.1
    });
  }

  function drawParticles() {
    ctx.clearRect(0, 0, W, H);
    particles.forEach(p => {
      p.x += p.dx; p.y += p.dy;
      if (p.x < 0) p.x = W; if (p.x > W) p.x = 0;
      if (p.y < 0) p.y = H; if (p.y > H) p.y = 0;
      ctx.beginPath();
      ctx.arc(p.x, p.y, p.r, 0, Math.PI * 2);
      ctx.fillStyle = p.c + p.a + ')';
      ctx.fill();
    });
    requestAnimationFrame(drawParticles);
  }
  drawParticles();

  // Quote rotator
  const quotes = document.querySelectorAll('.quote');
  let qi = 0;
  setInterval(() => {
    quotes[qi].classList.remove('active');
    qi = (qi + 1) % quotes.length;
    quotes[qi].classList.add('active');
  }, 3500);

  // Animate bars on scroll / load
  function animateBars() {
    document.querySelectorAll('.bar-fill').forEach(bar => {
      const w = bar.getAttribute('data-w');
      bar.style.width = w + '%';
    });
  }
  setTimeout(animateBars, 2200);
</script>
</body>
</html>
