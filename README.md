<div align="center">

<svg width="860" height="220" xmlns="http://www.w3.org/2000/svg">
<defs>
  <linearGradient id="g1" x1="0%" y1="0%" x2="100%" y2="0%">
    <stop offset="0%" stop-color="#00d4ff"><animate attributeName="stop-color" values="#00d4ff;#bf5fff;#ff2d55;#bf5fff;#00d4ff" dur="4s" repeatCount="indefinite"/></stop>
    <stop offset="50%" stop-color="#bf5fff"><animate attributeName="stop-color" values="#bf5fff;#ff2d55;#00d4ff;#ff2d55;#bf5fff" dur="4s" repeatCount="indefinite"/></stop>
    <stop offset="100%" stop-color="#ff2d55"><animate attributeName="stop-color" values="#ff2d55;#00d4ff;#bf5fff;#00d4ff;#ff2d55" dur="4s" repeatCount="indefinite"/></stop>
  </linearGradient>
  <linearGradient id="g2" x1="0%" y1="0%" x2="100%" y2="0%">
    <stop offset="0%" stop-color="#00d4ff" stop-opacity="0.0"/>
    <stop offset="50%" stop-color="#00d4ff" stop-opacity="0.4"/>
    <stop offset="100%" stop-color="#00d4ff" stop-opacity="0.0"/>
  </linearGradient>
  <radialGradient id="rg1" cx="50%" cy="50%" r="50%">
    <stop offset="0%" stop-color="#00d4ff" stop-opacity="0.08"/>
    <stop offset="100%" stop-color="#00d4ff" stop-opacity="0"/>
  </radialGradient>
  <filter id="f1" x="-20%" y="-20%" width="140%" height="140%">
    <feGaussianBlur stdDeviation="6" result="b"/>
    <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
  </filter>
  <filter id="f2" x="-5%" y="-5%" width="110%" height="110%">
    <feGaussianBlur stdDeviation="2" result="b"/>
    <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
  </filter>
</defs>

<!-- Void -->
<rect width="860" height="220" fill="#000008" rx="16"/>

<!-- Scanlines -->
<rect width="860" height="220" rx="16" fill="url(#rg1)"/>

<!-- Pulsing center glow -->
<ellipse cx="430" cy="110" rx="200" ry="120" fill="url(#rg1)">
  <animate attributeName="rx" values="200;240;200" dur="4s" repeatCount="indefinite"/>
  <animate attributeName="ry" values="120;150;120" dur="4s" repeatCount="indefinite"/>
</ellipse>

<!-- Domain rings — expanding outward -->
<circle cx="430" cy="110" r="30" fill="none" stroke="#00d4ff" stroke-width="0.8" stroke-opacity="0">
  <animate attributeName="r" values="30;380" dur="3s" repeatCount="indefinite" begin="0s"/>
  <animate attributeName="stroke-opacity" values="0.8;0" dur="3s" repeatCount="indefinite" begin="0s"/>
</circle>
<circle cx="430" cy="110" r="30" fill="none" stroke="#bf5fff" stroke-width="0.6" stroke-opacity="0">
  <animate attributeName="r" values="30;380" dur="3s" repeatCount="indefinite" begin="0.75s"/>
  <animate attributeName="stroke-opacity" values="0.6;0" dur="3s" repeatCount="indefinite" begin="0.75s"/>
</circle>
<circle cx="430" cy="110" r="30" fill="none" stroke="#ff2d55" stroke-width="0.6" stroke-opacity="0">
  <animate attributeName="r" values="30;380" dur="3s" repeatCount="indefinite" begin="1.5s"/>
  <animate attributeName="stroke-opacity" values="0.5;0" dur="3s" repeatCount="indefinite" begin="1.5s"/>
</circle>
<circle cx="430" cy="110" r="30" fill="none" stroke="#00d4ff" stroke-width="0.5" stroke-opacity="0">
  <animate attributeName="r" values="30;380" dur="3s" repeatCount="indefinite" begin="2.25s"/>
  <animate attributeName="stroke-opacity" values="0.4;0" dur="3s" repeatCount="indefinite" begin="2.25s"/>
</circle>

<!-- Eyebrow -->
<text x="430" y="52" text-anchor="middle" font-family="monospace" font-size="10" letter-spacing="7" fill="#00d4ff">
  ∞   FULL STACK DEVELOPER   ∞
  <animate attributeName="opacity" values="0.3;0.9;0.3" dur="2.5s" repeatCount="indefinite"/>
</text>

<!-- TOBE — main name with glow layer -->
<text x="430" y="152" text-anchor="middle" font-family="'Arial Black',sans-serif" font-size="110" font-weight="900" letter-spacing="20" fill="#00d4ff" opacity="0.06" filter="url(#f1)">TOBE</text>
<text x="430" y="152" text-anchor="middle" font-family="'Arial Black',sans-serif" font-size="110" font-weight="900" letter-spacing="20" fill="url(#g1)" filter="url(#f2)">TOBE
  <animate attributeName="opacity" values="1;0.85;1" dur="5s" repeatCount="indefinite"/>
</text>

<!-- Glitch layer 1 -->
<text x="427" y="152" text-anchor="middle" font-family="'Arial Black',sans-serif" font-size="110" font-weight="900" letter-spacing="20" fill="#00d4ff" opacity="0" clip-path="inset(35% 0 45% 0)">TOBE
  <animate attributeName="opacity" values="0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.5;0;0.5;0;0" dur="7s" repeatCount="indefinite"/>
  <animate attributeName="x" values="427;423;431;427" dur="7s" repeatCount="indefinite"/>
</text>
<!-- Glitch layer 2 -->
<text x="433" y="152" text-anchor="middle" font-family="'Arial Black',sans-serif" font-size="110" font-weight="900" letter-spacing="20" fill="#ff2d55" opacity="0" clip-path="inset(60% 0 20% 0)">TOBE
  <animate attributeName="opacity" values="0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0;0.4;0;0.4;0" dur="7s" repeatCount="indefinite"/>
  <animate attributeName="x" values="433;437;429;433" dur="7s" repeatCount="indefinite"/>
</text>

<!-- Sub -->
<text x="430" y="192" text-anchor="middle" font-family="monospace" font-size="11" letter-spacing="6" fill="#ffffff" opacity="0.2">teethaking  ·  open to work</text>

<!-- Corner accents -->
<line x1="24" y1="24" x2="54" y2="24" stroke="#00d4ff" stroke-width="1" stroke-opacity="0.4"/>
<line x1="24" y1="24" x2="24" y2="54" stroke="#00d4ff" stroke-width="1" stroke-opacity="0.4"/>
<line x1="836" y1="24" x2="806" y2="24" stroke="#00d4ff" stroke-width="1" stroke-opacity="0.4"/>
<line x1="836" y1="24" x2="836" y2="54" stroke="#00d4ff" stroke-width="1" stroke-opacity="0.4"/>
<line x1="24" y1="196" x2="54" y2="196" stroke="#bf5fff" stroke-width="1" stroke-opacity="0.4"/>
<line x1="24" y1="196" x2="24" y2="166" stroke="#bf5fff" stroke-width="1" stroke-opacity="0.4"/>
<line x1="836" y1="196" x2="806" y2="196" stroke="#bf5fff" stroke-width="1" stroke-opacity="0.4"/>
<line x1="836" y1="196" x2="836" y2="166" stroke="#bf5fff" stroke-width="1" stroke-opacity="0.4"/>

<!-- Animated border -->
<rect width="860" height="220" rx="16" fill="none" stroke="url(#g1)" stroke-width="1" stroke-opacity="0.3">
  <animate attributeName="stroke-opacity" values="0.15;0.5;0.15" dur="3s" repeatCount="indefinite"/>
</rect>
</svg>

<br/>

<!-- QUOTES -->
<svg width="700" height="36" xmlns="http://www.w3.org/2000/svg">
<rect width="700" height="36" fill="transparent"/>
<text x="350" y="22" text-anchor="middle" font-family="Georgia,serif" font-size="13" font-style="italic" fill="#e8f0ff" opacity="0">
  "Throughout Heaven and Earth — I alone am the honored one."
  <animate attributeName="opacity" values="0;0.65;0.65;0;0;0;0;0;0;0;0;0" dur="30s" repeatCount="indefinite"/>
</text>
<text x="350" y="22" text-anchor="middle" font-family="Georgia,serif" font-size="13" font-style="italic" fill="#e8f0ff" opacity="0">
  "I'm the strongest. Sorry to keep you waiting."
  <animate attributeName="opacity" values="0;0;0;0;0.65;0.65;0;0;0;0;0;0" dur="30s" repeatCount="indefinite"/>
</text>
<text x="350" y="22" text-anchor="middle" font-family="Georgia,serif" font-size="13" font-style="italic" fill="#e8f0ff" opacity="0">
  "Limitless. The technique. Also my commit history."
  <animate attributeName="opacity" values="0;0;0;0;0;0;0;0.65;0.65;0;0;0" dur="30s" repeatCount="indefinite"/>
</text>
<text x="350" y="22" text-anchor="middle" font-family="Georgia,serif" font-size="13" font-style="italic" fill="#e8f0ff" opacity="0">
  "My pull requests don't need reviewing. They're already perfect."
  <animate attributeName="opacity" values="0;0;0;0;0;0;0;0;0;0;0.65;0.65" dur="30s" repeatCount="indefinite"/>
</text>
</svg>

<!-- STATUS -->
<svg width="200" height="32" xmlns="http://www.w3.org/2000/svg">
<rect width="200" height="32" rx="16" fill="none" stroke="#00d4ff" stroke-width="0.6" stroke-opacity="0.2"/>
<circle cx="22" cy="16" r="4" fill="#39ff14">
  <animate attributeName="opacity" values="1;0.1;1" dur="1.4s" repeatCount="indefinite"/>
  <animate attributeName="r" values="4;5;4" dur="1.4s" repeatCount="indefinite"/>
</circle>
<circle cx="22" cy="16" r="8" fill="none" stroke="#39ff14" stroke-width="0.6">
  <animate attributeName="r" values="5;12;5" dur="1.8s" repeatCount="indefinite"/>
  <animate attributeName="stroke-opacity" values="0.6;0;0.6" dur="1.8s" repeatCount="indefinite"/>
</circle>
<text x="38" y="21" font-family="monospace" font-size="10" letter-spacing="3" fill="#39ff14" opacity="0.75">OPEN TO WORK</text>
</svg>

</div>

---

<div align="center">

<!-- ENERGY BARS -->
<svg width="700" height="270" xmlns="http://www.w3.org/2000/svg">
<defs>
  <linearGradient id="bb" x1="0%" y1="0%" x2="100%" y2="0%">
    <stop offset="0%" stop-color="#00d4ff"/>
    <stop offset="100%" stop-color="#bf5fff"/>
  </linearGradient>
  <linearGradient id="br" x1="0%" y1="0%" x2="100%" y2="0%">
    <stop offset="0%" stop-color="#ff2d55"/>
    <stop offset="100%" stop-color="#bf5fff"/>
  </linearGradient>
  <linearGradient id="bi" x1="0%" y1="0%" x2="100%" y2="0%">
    <stop offset="0%" stop-color="#bf5fff"><animate attributeName="stop-color" values="#bf5fff;#00d4ff;#ff2d55;#bf5fff" dur="3s" repeatCount="indefinite"/></stop>
    <stop offset="100%" stop-color="#00d4ff"><animate attributeName="stop-color" values="#00d4ff;#ff2d55;#bf5fff;#00d4ff" dur="3s" repeatCount="indefinite"/></stop>
  </linearGradient>
  <filter id="bg"><feGaussianBlur stdDeviation="2.5" result="b"/><feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge></filter>
</defs>

<rect width="700" height="270" fill="#000008" rx="12"/>
<rect width="700" height="270" fill="none" stroke="#00d4ff" stroke-width="0.5" stroke-opacity="0.1" rx="12"/>

<!-- Animated border sweep -->
<rect width="700" height="270" fill="none" rx="12" stroke="url(#bb)" stroke-width="0.8" stroke-opacity="0">
  <animate attributeName="stroke-opacity" values="0;0.3;0" dur="4s" repeatCount="indefinite"/>
</rect>

<text x="350" y="30" text-anchor="middle" font-family="monospace" font-size="9" letter-spacing="6" fill="#00d4ff" opacity="0.4">
  ⌇  CURSED  ENERGY  OUTPUT  ⌇
  <animate attributeName="opacity" values="0.3;0.6;0.3" dur="2s" repeatCount="indefinite"/>
</text>

<!-- FRONTEND -->
<text x="36" y="66" font-family="monospace" font-size="9" letter-spacing="3" fill="#4a5568">FRONTEND</text>
<text x="664" y="66" font-family="monospace" font-size="9" fill="#00d4ff" opacity="0.6">92</text>
<rect x="170" y="57" width="480" height="1.5" rx="1" fill="#ffffff" fill-opacity="0.03"/>
<rect x="170" y="57" width="0" height="1.5" rx="1" fill="url(#bb)" filter="url(#bg)">
  <animate attributeName="width" from="0" to="441" dur="1.6s" begin="0.2s" fill="freeze" calcMode="spline" keySplines="0.16 1 0.3 1"/>
</rect>

<!-- BACKEND -->
<text x="36" y="106" font-family="monospace" font-size="9" letter-spacing="3" fill="#4a5568">BACKEND</text>
<text x="664" y="106" font-family="monospace" font-size="9" fill="#00d4ff" opacity="0.6">85</text>
<rect x="170" y="97" width="480" height="1.5" rx="1" fill="#ffffff" fill-opacity="0.03"/>
<rect x="170" y="97" width="0" height="1.5" rx="1" fill="url(#bb)" filter="url(#bg)">
  <animate attributeName="width" from="0" to="408" dur="1.6s" begin="0.5s" fill="freeze" calcMode="spline" keySplines="0.16 1 0.3 1"/>
</rect>

<!-- DATABASES -->
<text x="36" y="146" font-family="monospace" font-size="9" letter-spacing="3" fill="#4a5568">DATABASES</text>
<text x="664" y="146" font-family="monospace" font-size="9" fill="#ff2d55" opacity="0.6">80</text>
<rect x="170" y="137" width="480" height="1.5" rx="1" fill="#ffffff" fill-opacity="0.03"/>
<rect x="170" y="137" width="0" height="1.5" rx="1" fill="url(#br)" filter="url(#bg)">
  <animate attributeName="width" from="0" to="384" dur="1.6s" begin="0.8s" fill="freeze" calcMode="spline" keySplines="0.16 1 0.3 1"/>
</rect>

<!-- PROBLEM SOLVING -->
<text x="36" y="186" font-family="monospace" font-size="9" letter-spacing="3" fill="#4a5568">PROBLEM SOLVING</text>
<text x="664" y="186" font-family="monospace" font-size="9" fill="#ff2d55" opacity="0.6">95</text>
<rect x="170" y="177" width="480" height="1.5" rx="1" fill="#ffffff" fill-opacity="0.03"/>
<rect x="170" y="177" width="0" height="1.5" rx="1" fill="url(#br)" filter="url(#bg)">
  <animate attributeName="width" from="0" to="456" dur="1.6s" begin="1.1s" fill="freeze" calcMode="spline" keySplines="0.16 1 0.3 1"/>
</rect>

<!-- EGO ∞ -->
<text x="36" y="226" font-family="monospace" font-size="9" letter-spacing="3" fill="#4a5568">EGO</text>
<text x="664" y="226" font-family="monospace" font-size="9" fill="#bf5fff" opacity="0.9">∞
  <animate attributeName="opacity" values="0.5;1;0.5" dur="1.5s" repeatCount="indefinite"/>
</text>
<rect x="170" y="217" width="480" height="1.5" rx="1" fill="#ffffff" fill-opacity="0.03"/>
<rect x="170" y="217" width="480" height="1.5" rx="1" fill="url(#bi)" filter="url(#bg)">
  <animate attributeName="opacity" values="0.5;1;0.5" dur="1.5s" repeatCount="indefinite"/>
</rect>

<text x="350" y="255" text-anchor="middle" font-family="monospace" font-size="8" letter-spacing="4" fill="#4a5568" opacity="0.5">BLUE · RED · HOLLOW PURPLE</text>
</svg>

<br/>

<!-- TECH CHIPS -->
<svg width="700" height="170" xmlns="http://www.w3.org/2000/svg">
<defs>
  <linearGradient id="cg" x1="0%" y1="0%" x2="100%" y2="100%">
    <stop offset="0%" stop-color="#00d4ff" stop-opacity="0.08"/>
    <stop offset="100%" stop-color="#bf5fff" stop-opacity="0.08"/>
  </linearGradient>
</defs>
<rect width="700" height="170" fill="#000008" rx="12"/>
<rect width="700" height="170" fill="none" stroke="#00d4ff" stroke-width="0.5" stroke-opacity="0.1" rx="12"/>

<text x="350" y="28" text-anchor="middle" font-family="monospace" font-size="9" letter-spacing="6" fill="#00d4ff" opacity="0.4">⌇  TECHNIQUE  ARSENAL  ⌇</text>

<!-- Row 1 -->
<g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.4s" begin="0.1s" fill="freeze"/>
<rect x="30" y="44" width="94" height="30" rx="4" fill="url(#cg)" stroke="#00d4ff" stroke-width="0.6" stroke-opacity="0.25"/>
<text x="77" y="64" text-anchor="middle" font-family="monospace" font-size="10" letter-spacing="1" fill="#e8f0ff" opacity="0.6">JavaScript</text></g>

<g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.4s" begin="0.2s" fill="freeze"/>
<rect x="136" y="44" width="94" height="30" rx="4" fill="url(#cg)" stroke="#00d4ff" stroke-width="0.6" stroke-opacity="0.25"/>
<text x="183" y="64" text-anchor="middle" font-family="monospace" font-size="10" letter-spacing="1" fill="#e8f0ff" opacity="0.6">TypeScript</text></g>

<g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.4s" begin="0.3s" fill="freeze"/>
<rect x="242" y="44" width="94" height="30" rx="4" fill="url(#cg)" stroke="#bf5fff" stroke-width="0.6" stroke-opacity="0.25"/>
<text x="289" y="64" text-anchor="middle" font-family="monospace" font-size="10" letter-spacing="1" fill="#e8f0ff" opacity="0.6">React</text></g>

<g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.4s" begin="0.4s" fill="freeze"/>
<rect x="348" y="44" width="94" height="30" rx="4" fill="url(#cg)" stroke="#bf5fff" stroke-width="0.6" stroke-opacity="0.25"/>
<text x="395" y="64" text-anchor="middle" font-family="monospace" font-size="10" letter-spacing="1" fill="#e8f0ff" opacity="0.6">Next.js</text></g>

<g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.4s" begin="0.5s" fill="freeze"/>
<rect x="454" y="44" width="94" height="30" rx="4" fill="url(#cg)" stroke="#00d4ff" stroke-width="0.6" stroke-opacity="0.25"/>
<text x="501" y="64" text-anchor="middle" font-family="monospace" font-size="10" letter-spacing="1" fill="#e8f0ff" opacity="0.6">Python</text></g>

<g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.4s" begin="0.55s" fill="freeze"/>
<rect x="560" y="44" width="110" height="30" rx="4" fill="url(#cg)" stroke="#00d4ff" stroke-width="0.6" stroke-opacity="0.25"/>
<text x="615" y="64" text-anchor="middle" font-family="monospace" font-size="10" letter-spacing="1" fill="#e8f0ff" opacity="0.6">Node.js</text></g>

<!-- Row 2 -->
<g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.4s" begin="0.65s" fill="freeze"/>
<rect x="83" y="90" width="94" height="30" rx="4" fill="url(#cg)" stroke="#bf5fff" stroke-width="0.6" stroke-opacity="0.25"/>
<text x="130" y="110" text-anchor="middle" font-family="monospace" font-size="10" letter-spacing="1" fill="#e8f0ff" opacity="0.6">Tailwind</text></g>

<g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.4s" begin="0.75s" fill="freeze"/>
<rect x="195" y="90" width="114" height="30" rx="4" fill="url(#cg)" stroke="#ff2d55" stroke-width="0.6" stroke-opacity="0.25"/>
<text x="252" y="110" text-anchor="middle" font-family="monospace" font-size="10" letter-spacing="1" fill="#e8f0ff" opacity="0.6">PostgreSQL</text></g>

<g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.4s" begin="0.85s" fill="freeze"/>
<rect x="327" y="90" width="94" height="30" rx="4" fill="url(#cg)" stroke="#ff2d55" stroke-width="0.6" stroke-opacity="0.25"/>
<text x="374" y="110" text-anchor="middle" font-family="monospace" font-size="10" letter-spacing="1" fill="#e8f0ff" opacity="0.6">MongoDB</text></g>

<g opacity="0"><animate attributeName="opacity" from="0" to="1" dur="0.4s" begin="0.95s" fill="freeze"/>
<rect x="439" y="90" width="80" height="30" rx="4" fill="url(#cg)" stroke="#bf5fff" stroke-width="0.6" stroke-opacity="0.25"/>
<text x="479" y="110" text-anchor="middle" font-family="monospace" font-size="10" letter-spacing="1" fill="#e8f0ff" opacity="0.6">MySQL</text></g>

<text x="350" y="150" text-anchor="middle" font-family="monospace" font-size="8" letter-spacing="5" fill="#4a5568" opacity="0.5">∞  FULL  STACK  ∞</text>
</svg>

<br/>

<!-- DOMAIN EXPANSION -->
<svg width="700" height="150" xmlns="http://www.w3.org/2000/svg">
<defs>
  <linearGradient id="dg" x1="0%" y1="0%" x2="100%" y2="0%">
    <stop offset="0%" stop-color="#00d4ff"><animate attributeName="stop-color" values="#00d4ff;#bf5fff;#ff2d55;#bf5fff;#00d4ff" dur="3s" repeatCount="indefinite"/></stop>
    <stop offset="50%" stop-color="#bf5fff"><animate attributeName="stop-color" values="#bf5fff;#ff2d55;#00d4ff;#ff2d55;#bf5fff" dur="3s" repeatCount="indefinite"/></stop>
    <stop offset="100%" stop-color="#ff2d55"><animate attributeName="stop-color" values="#ff2d55;#00d4ff;#bf5fff;#00d4ff;#ff2d55" dur="3s" repeatCount="indefinite"/></stop>
  </linearGradient>
  <filter id="df"><feGaussianBlur stdDeviation="5" result="b"/><feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge></filter>
</defs>

<rect width="700" height="150" fill="#000008" rx="12"/>
<rect width="700" height="150" fill="none" rx="12" stroke="url(#dg)" stroke-width="1">
  <animate attributeName="stroke-opacity" values="0.2;0.7;0.2" dur="2.5s" repeatCount="indefinite"/>
</rect>

<!-- Expanding rings from domain center -->
<circle cx="350" cy="75" r="10" fill="none" stroke="#00d4ff" stroke-width="0.5" stroke-opacity="0">
  <animate attributeName="r" values="10;300" dur="2.5s" repeatCount="indefinite" begin="0s"/>
  <animate attributeName="stroke-opacity" values="0.5;0" dur="2.5s" repeatCount="indefinite" begin="0s"/>
</circle>
<circle cx="350" cy="75" r="10" fill="none" stroke="#bf5fff" stroke-width="0.5" stroke-opacity="0">
  <animate attributeName="r" values="10;300" dur="2.5s" repeatCount="indefinite" begin="0.83s"/>
  <animate attributeName="stroke-opacity" values="0.5;0" dur="2.5s" repeatCount="indefinite" begin="0.83s"/>
</circle>
<circle cx="350" cy="75" r="10" fill="none" stroke="#ff2d55" stroke-width="0.5" stroke-opacity="0">
  <animate attributeName="r" values="10;300" dur="2.5s" repeatCount="indefinite" begin="1.66s"/>
  <animate attributeName="stroke-opacity" values="0.4;0" dur="2.5s" repeatCount="indefinite" begin="1.66s"/>
</circle>

<!-- Title -->
<text x="350" y="58" text-anchor="middle" font-family="monospace" font-size="9" letter-spacing="6" fill="#ffffff" opacity="0.2">DOMAIN EXPANSION</text>
<text x="350" y="96" text-anchor="middle" font-family="'Arial Black',Impact,sans-serif" font-size="44" font-weight="900" letter-spacing="10" fill="url(#dg)" filter="url(#df)">
  UNLIMITED VOID
  <animate attributeName="opacity" values="1;0.8;1;1;0.6;1;1" dur="6s" repeatCount="indefinite"/>
</text>

<!-- Orbs -->
<circle cx="254" cy="128" r="11" fill="none" stroke="#00d4ff" stroke-width="0.8">
  <animate attributeName="stroke-opacity" values="0.3;0.9;0.3" dur="2s" repeatCount="indefinite" begin="0s"/>
  <animate attributeName="r" values="11;15;11" dur="2s" repeatCount="indefinite" begin="0s"/>
</circle>
<text x="254" y="132" text-anchor="middle" font-family="monospace" font-size="7" letter-spacing="1" fill="#00d4ff" opacity="0.8">BLUE</text>

<circle cx="350" cy="128" r="11" fill="none" stroke="#bf5fff" stroke-width="0.8">
  <animate attributeName="stroke-opacity" values="0.3;0.9;0.3" dur="2s" repeatCount="indefinite" begin="0.66s"/>
  <animate attributeName="r" values="11;15;11" dur="2s" repeatCount="indefinite" begin="0.66s"/>
</circle>
<text x="350" y="132" text-anchor="middle" font-family="monospace" font-size="10" fill="#bf5fff" opacity="0.8">∞</text>

<circle cx="446" cy="128" r="11" fill="none" stroke="#ff2d55" stroke-width="0.8">
  <animate attributeName="stroke-opacity" values="0.3;0.9;0.3" dur="2s" repeatCount="indefinite" begin="1.33s"/>
  <animate attributeName="r" values="11;15;11" dur="2s" repeatCount="indefinite" begin="1.33s"/>
</circle>
<text x="446" y="132" text-anchor="middle" font-family="monospace" font-size="7" letter-spacing="1" fill="#ff2d55" opacity="0.8">RED</text>
</svg>

<br/>

<svg width="500" height="24" xmlns="http://www.w3.org/2000/svg">
<text x="250" y="16" text-anchor="middle" font-family="monospace" font-size="9" letter-spacing="5" fill="#4a5568">
  ∞  ·  teethaking  ·  tobe  ·  all domains  ·  ∞
  <animate attributeName="opacity" values="0.3;0.6;0.3" dur="3s" repeatCount="indefinite"/>
</text>
</svg>

</div>
