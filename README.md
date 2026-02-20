<div align="center">

<!--  ╔══════════════════════════════════════╗  -->
<!--  ║     ANIMATED HEADER — TOBE/GOJO     ║  -->
<!--  ╚══════════════════════════════════════╝  -->

<svg width="860" height="180" viewBox="0 0 860 180" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="nameGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#60c8ff"/>
      <stop offset="50%"  stop-color="#c084fc"/>
      <stop offset="100%" stop-color="#60c8ff"/>
      <animateTransform attributeName="gradientTransform" type="translate" from="-1 0" to="1 0" dur="3s" repeatCount="indefinite"/>
    </linearGradient>
    <linearGradient id="subGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#4a5568"/>
      <stop offset="50%"  stop-color="#60c8ff" stop-opacity="0.6"/>
      <stop offset="100%" stop-color="#4a5568"/>
    </linearGradient>
    <!-- ring glow -->
    <radialGradient id="ringGlow" cx="50%" cy="50%" r="50%">
      <stop offset="0%"   stop-color="#60c8ff" stop-opacity="0.08"/>
      <stop offset="100%" stop-color="#60c8ff" stop-opacity="0"/>
    </radialGradient>
    <filter id="glow">
      <feGaussianBlur stdDeviation="3" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
  </defs>

  <!-- Background -->
  <rect width="860" height="180" fill="#030712" rx="12"/>

  <!-- Infinity rings -->
  <g transform="translate(430,90)" opacity="0.25">
    <ellipse cx="0" cy="0" rx="60"  ry="60"  fill="none" stroke="#60c8ff" stroke-width="0.5">
      <animate attributeName="rx" values="60;65;60" dur="5s" repeatCount="indefinite"/>
      <animate attributeName="ry" values="60;65;60" dur="5s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.25;0.5;0.25" dur="5s" repeatCount="indefinite"/>
    </ellipse>
    <ellipse cx="0" cy="0" rx="100" ry="100" fill="none" stroke="#c084fc" stroke-width="0.5">
      <animate attributeName="rx" values="100;107;100" dur="6s" repeatCount="indefinite"/>
      <animate attributeName="ry" values="100;107;100" dur="6s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.2;0.4;0.2" dur="6s" repeatCount="indefinite"/>
    </ellipse>
    <ellipse cx="0" cy="0" rx="150" ry="150" fill="none" stroke="#60c8ff" stroke-width="0.4">
      <animate attributeName="rx" values="150;160;150" dur="7s" repeatCount="indefinite"/>
      <animate attributeName="ry" values="150;160;150" dur="7s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.15;0.3;0.15" dur="7s" repeatCount="indefinite"/>
    </ellipse>
  </g>

  <!-- Eyebrow -->
  <text x="430" y="38" text-anchor="middle" font-family="monospace" font-size="10" letter-spacing="6" fill="#60c8ff" opacity="0.7">
    ∞  FULL  STACK  DEVELOPER  ∞
    <animate attributeName="opacity" values="0.4;0.9;0.4" dur="3s" repeatCount="indefinite"/>
  </text>

  <!-- Main name -->
  <text x="430" y="120" text-anchor="middle"
        font-family="'Trebuchet MS', sans-serif"
        font-size="88" font-weight="900" letter-spacing="18"
        fill="url(#nameGrad)" filter="url(#glow)">
    TOBE
  </text>

  <!-- Sub -->
  <text x="430" y="155" text-anchor="middle" font-family="monospace" font-size="11" letter-spacing="5" fill="url(#subGrad)">
    teethaking  ·  open to work
  </text>

  <!-- Corner glyphs -->
  <text x="24" y="30"  font-family="monospace" font-size="10" fill="#60c8ff" opacity="0.3">✦</text>
  <text x="836" y="30" font-family="monospace" font-size="10" fill="#60c8ff" opacity="0.3">✦</text>
  <text x="24" y="165" font-family="monospace" font-size="10" fill="#c084fc" opacity="0.3">∞</text>
  <text x="833" y="165" font-family="monospace" font-size="10" fill="#c084fc" opacity="0.3">∞</text>
</svg>

<br/>

<!--  ╔══════════════════╗  -->
<!--  ║  ROTATING QUOTE  ║  -->
<!--  ╚══════════════════╝  -->

<svg width="700" height="52" viewBox="0 0 700 52" xmlns="http://www.w3.org/2000/svg">
  <rect width="700" height="52" fill="transparent"/>

  <!-- Quote 1 — cocky -->
  <text x="350" y="28" text-anchor="middle" font-family="Georgia, serif" font-size="13" font-style="italic" fill="#f0f4ff" opacity="0">
    "Throughout Heaven and Earth — I alone am the honored one."
    <animate attributeName="opacity" values="0;0;0.7;0.7;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0" dur="28s" repeatCount="indefinite"/>
  </text>

  <!-- Quote 2 — cold -->
  <text x="350" y="28" text-anchor="middle" font-family="Georgia, serif" font-size="13" font-style="italic" fill="#f0f4ff" opacity="0">
    "Don't worry. I already won before I started."
    <animate attributeName="opacity" values="0;0;0;0;0;0;0.7;0.7;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0" dur="28s" repeatCount="indefinite"/>
  </text>

  <!-- Quote 3 — hyped -->
  <text x="350" y="28" text-anchor="middle" font-family="Georgia, serif" font-size="13" font-style="italic" fill="#f0f4ff" opacity="0">
    "Limitless. The technique. Also my commit history."
    <animate attributeName="opacity" values="0;0;0;0;0;0;0;0;0;0;0;0;0.7;0.7;0;0;0;0;0;0;0;0;0;0" dur="28s" repeatCount="indefinite"/>
  </text>

  <!-- Quote 4 — cold -->
  <text x="350" y="28" text-anchor="middle" font-family="Georgia, serif" font-size="13" font-style="italic" fill="#f0f4ff" opacity="0">
    "I'm the strongest. Sorry to keep you waiting."
    <animate attributeName="opacity" values="0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.7;0.7;0;0;0;0" dur="28s" repeatCount="indefinite"/>
  </text>

  <!-- Quote 5 — chaotic -->
  <text x="350" y="28" text-anchor="middle" font-family="Georgia, serif" font-size="13" font-style="italic" fill="#f0f4ff" opacity="0">
    "My pull requests don't need reviewing. They're already perfect."
    <animate attributeName="opacity" values="0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.7;0.7" dur="28s" repeatCount="indefinite"/>
  </text>
</svg>

<br/>

<!--  STATUS PILL  -->

<svg width="200" height="30" viewBox="0 0 200 30" xmlns="http://www.w3.org/2000/svg">
  <rect width="200" height="30" rx="15" fill="transparent" stroke="#60c8ff" stroke-width="0.8" stroke-opacity="0.25"/>
  <circle cx="20" cy="15" r="4" fill="#4ade80">
    <animate attributeName="opacity" values="1;0.2;1" dur="1.4s" repeatCount="indefinite"/>
  </circle>
  <text x="34" y="20" font-family="monospace" font-size="10" letter-spacing="3" fill="#60c8ff" opacity="0.8">OPEN TO WORK</text>
</svg>

</div>

---

<br/>

<div align="center">

<!--  ╔══════════════════════════════╗  -->
<!--  ║     CURSED ENERGY BARS      ║  -->
<!--  ╚══════════════════════════════╝  -->

<svg width="700" height="260" viewBox="0 0 700 260" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="barBlue" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#60c8ff"/>
      <stop offset="100%" stop-color="#c084fc"/>
    </linearGradient>
    <linearGradient id="barRed" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#ff4c6a"/>
      <stop offset="100%" stop-color="#c084fc"/>
    </linearGradient>
    <linearGradient id="barInf" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#c084fc"/>
      <stop offset="100%" stop-color="#60c8ff"/>
    </linearGradient>
    <filter id="barGlow">
      <feGaussianBlur stdDeviation="2" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
  </defs>

  <rect width="700" height="260" fill="#030712" rx="12"/>
  <rect width="700" height="260" fill="none" stroke="#60c8ff" stroke-width="0.5" stroke-opacity="0.12" rx="12"/>

  <!-- Section label -->
  <text x="350" y="32" text-anchor="middle" font-family="monospace" font-size="9" letter-spacing="5" fill="#60c8ff" opacity="0.5">⌇  CURSED  ENERGY  OUTPUT</text>

  <!-- Row 1: Frontend -->
  <text x="40" y="68" font-family="monospace" font-size="10" letter-spacing="2" fill="#4a5568">FRONTEND</text>
  <rect x="180" y="57" width="460" height="1.5" rx="1" fill="#ffffff" fill-opacity="0.04"/>
  <rect x="180" y="57" width="0" height="1.5" rx="1" fill="url(#barBlue)" filter="url(#barGlow)">
    <animate attributeName="width" from="0" to="424" dur="1.5s" begin="0.3s" fill="freeze" calcMode="spline" keySplines="0.16 1 0.3 1"/>
  </rect>
  <text x="654" y="68" font-family="monospace" font-size="10" fill="#60c8ff" opacity="0.6">92</text>

  <!-- Row 2: Backend -->
  <text x="40" y="108" font-family="monospace" font-size="10" letter-spacing="2" fill="#4a5568">BACKEND</text>
  <rect x="180" y="97" width="460" height="1.5" rx="1" fill="#ffffff" fill-opacity="0.04"/>
  <rect x="180" y="97" width="0" height="1.5" rx="1" fill="url(#barBlue)" filter="url(#barGlow)">
    <animate attributeName="width" from="0" to="391" dur="1.5s" begin="0.6s" fill="freeze" calcMode="spline" keySplines="0.16 1 0.3 1"/>
  </rect>
  <text x="654" y="108" font-family="monospace" font-size="10" fill="#60c8ff" opacity="0.6">85</text>

  <!-- Row 3: Databases -->
  <text x="40" y="148" font-family="monospace" font-size="10" letter-spacing="2" fill="#4a5568">DATABASES</text>
  <rect x="180" y="137" width="460" height="1.5" rx="1" fill="#ffffff" fill-opacity="0.04"/>
  <rect x="180" y="137" width="0" height="1.5" rx="1" fill="url(#barRed)" filter="url(#barGlow)">
    <animate attributeName="width" from="0" to="368" dur="1.5s" begin="0.9s" fill="freeze" calcMode="spline" keySplines="0.16 1 0.3 1"/>
  </rect>
  <text x="654" y="148" font-family="monospace" font-size="10" fill="#ff4c6a" opacity="0.6">80</text>

  <!-- Row 4: Problem Solving -->
  <text x="40" y="188" font-family="monospace" font-size="10" letter-spacing="2" fill="#4a5568">PROBLEM SOLVING</text>
  <rect x="180" y="177" width="460" height="1.5" rx="1" fill="#ffffff" fill-opacity="0.04"/>
  <rect x="180" y="177" width="0" height="1.5" rx="1" fill="url(#barRed)" filter="url(#barGlow)">
    <animate attributeName="width" from="0" to="437" dur="1.5s" begin="1.2s" fill="freeze" calcMode="spline" keySplines="0.16 1 0.3 1"/>
  </rect>
  <text x="654" y="188" font-family="monospace" font-size="10" fill="#ff4c6a" opacity="0.6">95</text>

  <!-- Row 5: Ego / Infinity -->
  <text x="40" y="228" font-family="monospace" font-size="10" letter-spacing="2" fill="#4a5568">EGO</text>
  <rect x="180" y="217" width="460" height="1.5" rx="1" fill="#ffffff" fill-opacity="0.04"/>
  <rect x="180" y="217" width="460" height="1.5" rx="1" fill="url(#barInf)" filter="url(#barGlow)">
    <animate attributeName="opacity" values="0.6;1;0.6" dur="2s" repeatCount="indefinite"/>
  </rect>
  <text x="654" y="228" font-family="monospace" font-size="10" fill="#c084fc" opacity="0.8">∞</text>
</svg>

<br/><br/>

<!--  ╔════════════════════════════╗  -->
<!--  ║     TECH STACK CHIPS      ║  -->
<!--  ╚════════════════════════════╝  -->

<svg width="700" height="200" viewBox="0 0 700 200" xmlns="http://www.w3.org/2000/svg">
  <rect width="700" height="200" fill="#030712" rx="12"/>
  <rect width="700" height="200" fill="none" stroke="#60c8ff" stroke-width="0.5" stroke-opacity="0.12" rx="12"/>

  <text x="350" y="30" text-anchor="middle" font-family="monospace" font-size="9" letter-spacing="5" fill="#60c8ff" opacity="0.5">⌇  TECHNIQUE  ARSENAL</text>

  <!-- Row 1 -->
  <g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.5s" begin="0.2s" fill="freeze"/>
    <rect x="40"  y="50" width="90" height="34" rx="5" fill="none" stroke="#60c8ff" stroke-width="0.6" stroke-opacity="0.25"/>
    <text x="85"  y="72" text-anchor="middle" font-family="monospace" font-size="10" fill="#f0f4ff" opacity="0.6">JavaScript</text>
  </g>
  <g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.5s" begin="0.35s" fill="freeze"/>
    <rect x="148" y="50" width="90" height="34" rx="5" fill="none" stroke="#60c8ff" stroke-width="0.6" stroke-opacity="0.25"/>
    <text x="193" y="72" text-anchor="middle" font-family="monospace" font-size="10" fill="#f0f4ff" opacity="0.6">TypeScript</text>
  </g>
  <g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.5s" begin="0.5s" fill="freeze"/>
    <rect x="256" y="50" width="90" height="34" rx="5" fill="none" stroke="#c084fc" stroke-width="0.6" stroke-opacity="0.25"/>
    <text x="301" y="72" text-anchor="middle" font-family="monospace" font-size="10" fill="#f0f4ff" opacity="0.6">React</text>
  </g>
  <g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.5s" begin="0.65s" fill="freeze"/>
    <rect x="364" y="50" width="90" height="34" rx="5" fill="none" stroke="#c084fc" stroke-width="0.6" stroke-opacity="0.25"/>
    <text x="409" y="72" text-anchor="middle" font-family="monospace" font-size="10" fill="#f0f4ff" opacity="0.6">Next.js</text>
  </g>
  <g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.5s" begin="0.8s" fill="freeze"/>
    <rect x="472" y="50" width="90" height="34" rx="5" fill="none" stroke="#60c8ff" stroke-width="0.6" stroke-opacity="0.25"/>
    <text x="517" y="72" text-anchor="middle" font-family="monospace" font-size="10" fill="#f0f4ff" opacity="0.6">Python</text>
  </g>

  <!-- Row 2 -->
  <g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.5s" begin="0.95s" fill="freeze"/>
    <rect x="40"  y="102" width="90" height="34" rx="5" fill="none" stroke="#60c8ff" stroke-width="0.6" stroke-opacity="0.25"/>
    <text x="85"  y="124" text-anchor="middle" font-family="monospace" font-size="10" fill="#f0f4ff" opacity="0.6">Node.js</text>
  </g>
  <g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.5s" begin="1.1s" fill="freeze"/>
    <rect x="148" y="102" width="90" height="34" rx="5" fill="none" stroke="#c084fc" stroke-width="0.6" stroke-opacity="0.25"/>
    <text x="193" y="124" text-anchor="middle" font-family="monospace" font-size="10" fill="#f0f4ff" opacity="0.6">Tailwind</text>
  </g>
  <g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.5s" begin="1.25s" fill="freeze"/>
    <rect x="256" y="102" width="90" height="34" rx="5" fill="none" stroke="#ff4c6a" stroke-width="0.6" stroke-opacity="0.25"/>
    <text x="301" y="124" text-anchor="middle" font-family="monospace" font-size="10" fill="#f0f4ff" opacity="0.6">PostgreSQL</text>
  </g>
  <g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.5s" begin="1.4s" fill="freeze"/>
    <rect x="364" y="102" width="90" height="34" rx="5" fill="none" stroke="#ff4c6a" stroke-width="0.6" stroke-opacity="0.25"/>
    <text x="409" y="124" text-anchor="middle" font-family="monospace" font-size="10" fill="#f0f4ff" opacity="0.6">MongoDB</text>
  </g>

  <!-- Footer label -->
  <text x="350" y="175" text-anchor="middle" font-family="monospace" font-size="9" letter-spacing="3" fill="#4a5568">FULL STACK · BLUE · RED · HOLLOW PURPLE</text>
</svg>

<br/><br/>

<!--  ╔══════════════════════════╗  -->
<!--  ║    DOMAIN EXPANSION     ║  -->
<!--  ╚══════════════════════════╝  -->

<svg width="700" height="160" viewBox="0 0 700 160" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="domainGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%"   stop-color="#60c8ff"/>
      <stop offset="50%"  stop-color="#c084fc"/>
      <stop offset="100%" stop-color="#ff4c6a"/>
      <animateTransform attributeName="gradientTransform" type="translate" from="-1 0" to="1 0" dur="4s" repeatCount="indefinite"/>
    </linearGradient>
    <filter id="domGlow">
      <feGaussianBlur stdDeviation="4" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
  </defs>

  <rect width="700" height="160" fill="#030712" rx="12"/>
  <!-- animated border -->
  <rect width="700" height="160" fill="none" rx="12" stroke="url(#domainGrad)" stroke-width="0.8" stroke-opacity="0.4">
    <animate attributeName="stroke-opacity" values="0.2;0.6;0.2" dur="3s" repeatCount="indefinite"/>
  </rect>

  <!-- Rings -->
  <ellipse cx="350" cy="80" rx="55" ry="55" fill="none" stroke="#60c8ff" stroke-width="0.4" stroke-opacity="0.15">
    <animate attributeName="rx" values="55;62;55" dur="5s" repeatCount="indefinite"/>
    <animate attributeName="ry" values="55;62;55" dur="5s" repeatCount="indefinite"/>
  </ellipse>
  <ellipse cx="350" cy="80" rx="80" ry="80" fill="none" stroke="#c084fc" stroke-width="0.4" stroke-opacity="0.1">
    <animate attributeName="rx" values="80;90;80" dur="6s" repeatCount="indefinite"/>
    <animate attributeName="ry" values="80;90;80" dur="6s" repeatCount="indefinite"/>
  </ellipse>

  <!-- Title -->
  <text x="350" y="72" text-anchor="middle"
        font-family="'Trebuchet MS', sans-serif"
        font-size="46" font-weight="900" letter-spacing="12"
        fill="url(#domainGrad)" filter="url(#domGlow)">
    UNLIMITED VOID
    <animate attributeName="opacity" values="1;1;0.7;1;1" dur="5s" repeatCount="indefinite"/>
  </text>

  <text x="350" y="100" text-anchor="middle" font-family="monospace" font-size="9" letter-spacing="6" fill="#ffffff" opacity="0.2">DOMAIN  EXPANSION  —  ACTIVE</text>

  <!-- Orbs -->
  <circle cx="270" cy="135" r="10" fill="none" stroke="#60c8ff" stroke-width="0.8" stroke-opacity="0.5">
    <animate attributeName="r" values="10;13;10" dur="3s" repeatCount="indefinite"/>
    <animate attributeName="stroke-opacity" values="0.3;0.8;0.3" dur="3s" repeatCount="indefinite"/>
  </circle>
  <text x="270" y="139" text-anchor="middle" font-family="monospace" font-size="7" fill="#60c8ff" opacity="0.7">BLUE</text>

  <circle cx="350" cy="135" r="10" fill="none" stroke="#c084fc" stroke-width="0.8" stroke-opacity="0.5">
    <animate attributeName="r" values="10;13;10" dur="3s" begin="1s" repeatCount="indefinite"/>
    <animate attributeName="stroke-opacity" values="0.3;0.8;0.3" dur="3s" begin="1s" repeatCount="indefinite"/>
  </circle>
  <text x="350" y="139" text-anchor="middle" font-family="monospace" font-size="9" fill="#c084fc" opacity="0.7">∞</text>

  <circle cx="430" cy="135" r="10" fill="none" stroke="#ff4c6a" stroke-width="0.8" stroke-opacity="0.5">
    <animate attributeName="r" values="10;13;10" dur="3s" begin="2s" repeatCount="indefinite"/>
    <animate attributeName="stroke-opacity" values="0.3;0.8;0.3" dur="3s" begin="2s" repeatCount="indefinite"/>
  </circle>
  <text x="430" y="139" text-anchor="middle" font-family="monospace" font-size="7" fill="#ff4c6a" opacity="0.7">RED</text>
</svg>

<br/>

<!--  FOOTER  -->

<svg width="500" height="30" viewBox="0 0 500 30" xmlns="http://www.w3.org/2000/svg">
  <text x="250" y="20" text-anchor="middle" font-family="monospace" font-size="9" letter-spacing="4" fill="#4a5568">
    ∞  ·  teethaking  ·  Tobe  ·  all domains  ·  ∞
  </text>
</svg>

</div>
