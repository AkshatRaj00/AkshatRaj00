<svg width="900" height="420" viewBox="0 0 900 420" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#0B1220"/>
      <stop offset="100%" stop-color="#0F1B33"/>
    </linearGradient>
    <linearGradient id="accent" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#36BCF7"/>
      <stop offset="100%" stop-color="#8B5CF6"/>
    </linearGradient>
    <style>
      .row { font-family: 'JetBrains Mono', 'Courier New', monospace; }
      .title { font-size: 42px; font-weight: 700; fill: #FFFFFF; letter-spacing: 2px; }
      .sub   { font-size: 18px; fill: #93C5FD; }
      .line  { font-size: 16px; fill: #CBD5E1; }
      .tag   { font-size: 14px; fill: #36BCF7; }
    </style>
  </defs>

  <rect width="900" height="420" rx="14" fill="url(#bg)"/>

  <!-- each row starts invisible + shifted up, then drops into place -->

  <g class="row" transform="translate(40,70)" opacity="0">
    <text class="title">AKSHAT RAJ</text>
    <animateTransform attributeName="transform" type="translate"
      values="40,40; 40,70" dur="0.6s" begin="0.1s" fill="freeze"/>
    <animate attributeName="opacity" values="0;1" dur="0.6s" begin="0.1s" fill="freeze"/>
  </g>

  <g class="row" transform="translate(40,105)" opacity="0">
    <text class="sub">Founder @ OnePersonAI — AI Systems · Automation · Cloud</text>
    <animateTransform attributeName="transform" type="translate"
      values="40,75; 40,105" dur="0.6s" begin="0.5s" fill="freeze"/>
    <animate attributeName="opacity" values="0;1" dur="0.6s" begin="0.5s" fill="freeze"/>
  </g>

  <!-- drawing divider line -->
  <line x1="40" y1="130" x2="860" y2="130" stroke="url(#accent)" stroke-width="2"
        stroke-dasharray="820" stroke-dashoffset="820">
    <animate attributeName="stroke-dashoffset" values="820;0" dur="0.9s" begin="0.9s" fill="freeze"/>
  </line>

  <g class="row" transform="translate(40,165)" opacity="0">
    <text class="line">runtime      :: Rust · Go · Python</text>
    <animateTransform attributeName="transform" type="translate"
      values="40,135; 40,165" dur="0.5s" begin="1.3s" fill="freeze"/>
    <animate attributeName="opacity" values="0;1" dur="0.5s" begin="1.3s" fill="freeze"/>
  </g>

  <g class="row" transform="translate(40,195)" opacity="0">
    <text class="line">interface   :: React · Next.js · Flutter</text>
    <animateTransform attributeName="transform" type="translate"
      values="40,165; 40,195" dur="0.5s" begin="1.6s" fill="freeze"/>
    <animate attributeName="opacity" values="0;1" dur="0.5s" begin="1.6s" fill="freeze"/>
  </g>

  <g class="row" transform="translate(40,225)" opacity="0">
    <text class="line">intelligence:: LLMs · Agents · Automation</text>
    <animateTransform attributeName="transform" type="translate"
      values="40,195; 40,225" dur="0.5s" begin="1.9s" fill="freeze"/>
    <animate attributeName="opacity" values="0;1" dur="0.5s" begin="1.9s" fill="freeze"/>
  </g>

  <g class="row" transform="translate(40,255)" opacity="0">
    <text class="line">infra       :: AWS · Docker · Linux</text>
    <animateTransform attributeName="transform" type="translate"
      values="40,225; 40,255" dur="0.5s" begin="2.2s" fill="freeze"/>
    <animate attributeName="opacity" values="0;1" dur="0.5s" begin="2.2s" fill="freeze"/>
  </g>

  <!-- second divider -->
  <line x1="40" y1="280" x2="860" y2="280" stroke="#1E293B" stroke-width="1"
        stroke-dasharray="820" stroke-dashoffset="820">
    <animate attributeName="stroke-dashoffset" values="820;0" dur="0.8s" begin="2.5s" fill="freeze"/>
  </line>

  <g class="row" transform="translate(40,320)" opacity="0">
    <text class="tag">$ whoami</text>
    <animateTransform attributeName="transform" type="translate"
      values="40,290; 40,320" dur="0.4s" begin="2.9s" fill="freeze"/>
    <animate attributeName="opacity" values="0;1" dur="0.4s" begin="2.9s" fill="freeze"/>
  </g>

  <g class="row" transform="translate(40,348)" opacity="0">
    <text class="line" fill="#22D3EE">akshat — one person, full stack, end to end</text>
    <animateTransform attributeName="transform" type="translate"
      values="40,318; 40,348" dur="0.4s" begin="3.2s" fill="freeze"/>
    <animate attributeName="opacity" values="0;1" dur="0.4s" begin="3.2s" fill="freeze"/>
  </g>

  <!-- blinking status dot -->
  <circle cx="828" cy="345" r="6" fill="#22C55E" opacity="0">
    <animate attributeName="opacity" values="0;1" dur="0.3s" begin="3.6s" fill="freeze"/>
    <animate attributeName="opacity" values="1;0.3;1" dur="1.4s" begin="3.9s" repeatCount="indefinite"/>
  </circle>
  <text x="782" y="349" class="tag" opacity="0" font-size="13">ONLINE
    <animate attributeName="opacity" values="0;1" dur="0.3s" begin="3.6s" fill="freeze"/>
  </text>
</svg>
