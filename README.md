
Claude terminou a resposta
faça um html animado para mai git meu nome weyk lopes focado em back end tacnologias html java e python. bem chamativo e atrativo

22:58

Visualizou um arquivo, criou um arquivo, leu um arquivo
Visualizou um arquivo, criou um arquivo, leu um arquivo
Aqui está o seu perfil HTML, Weyk! 🔥

O que foi incluído:

Visual & Animações

Grid de fundo estilo terminal/matrix com scanlines
Partículas flutuantes coloridas
Efeito de pulso no avatar com iniciais WL
Barra superior com gradiente animado
Cantos decorativos estilo HUD
Conteúdo

Bloco de terminal com efeito de digitação automática
Cards das 3 tecnologias (Java ☕, Python 🐍, HTML 🌐) com hover e barras de proficiência
Contadores animados (repos, commits, APIs, cafés)
Barras de habilidades (REST APIs, Spring Boot, FastAPI, DB, DevOps)
Status de disponibilidade + badges técnicos
Tema: Cyberpunk/Terminal escuro com ciano, laranja e verde neon — diferente e marcante.

Quer ajustar cores, números, textos ou adicionar alguma seção?


Weyk lopes github
Código · HTML 





Claude é uma IA e pode cometer erros. Por favor, verifique as respostas.


raw
Weyk lopes github · HTML
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Weyk Lopes — Backend Developer</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Syne:wght@400;700;800;900&display=swap');
 
  :root {
    --bg: #050a0f;
    --surface: #0d1620;
    --border: #1a2d42;
    --accent: #00e5ff;
    --accent2: #ff6b35;
    --accent3: #7fff6e;
    --text: #c8d8e8;
    --muted: #4a6a8a;
    --java: #f89820;
    --python: #3572A5;
    --html: #e34c26;
  }
 
  * { margin: 0; padding: 0; box-sizing: border-box; }
 
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Space Mono', monospace;
    min-height: 100vh;
    overflow-x: hidden;
  }
 
  /* === GRID BG === */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,229,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,229,255,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }
 
  /* === SCANLINE === */
  body::after {
    content: '';
    position: fixed;
    inset: 0;
    background: repeating-linear-gradient(
      0deg,
      transparent,
      transparent 2px,
      rgba(0,0,0,0.07) 2px,
      rgba(0,0,0,0.07) 4px
    );
    pointer-events: none;
    z-index: 0;
  }
 
  .container {
    position: relative;
    z-index: 1;
    max-width: 900px;
    margin: 0 auto;
    padding: 40px 20px 80px;
  }
 
  /* === HEADER === */
  .header {
    display: flex;
    align-items: flex-start;
    gap: 36px;
    margin-bottom: 48px;
    padding: 36px;
    border: 1px solid var(--border);
    background: var(--surface);
    position: relative;
    overflow: hidden;
    animation: slideDown 0.8s cubic-bezier(0.16, 1, 0.3, 1) both;
  }
 
  .header::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--accent), var(--accent2), var(--accent3));
    animation: shimmer 3s linear infinite;
    background-size: 200% 100%;
  }
 
  @keyframes shimmer {
    0% { background-position: 200% 0; }
    100% { background-position: -200% 0; }
  }
 
  .corner {
    position: absolute;
    width: 20px; height: 20px;
    border-color: var(--accent);
    border-style: solid;
    opacity: 0.6;
  }
  .corner.tl { top: 0; left: 0; border-width: 2px 0 0 2px; }
  .corner.tr { top: 0; right: 0; border-width: 2px 2px 0 0; }
  .corner.bl { bottom: 0; left: 0; border-width: 0 0 2px 2px; }
  .corner.br { bottom: 0; right: 0; border-width: 0 2px 2px 0; }
 
  .avatar-wrap {
    position: relative;
    flex-shrink: 0;
  }
 
  .avatar {
    width: 110px;
    height: 110px;
    border-radius: 50%;
    border: 2px solid var(--accent);
    background: var(--bg);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Syne', sans-serif;
    font-size: 2.4rem;
    font-weight: 900;
    color: var(--accent);
    letter-spacing: -2px;
    position: relative;
    animation: pulse-ring 2s ease-in-out infinite;
  }
 
  @keyframes pulse-ring {
    0%, 100% { box-shadow: 0 0 0 0 rgba(0,229,255,0.4), 0 0 20px rgba(0,229,255,0.1); }
    50% { box-shadow: 0 0 0 12px rgba(0,229,255,0), 0 0 40px rgba(0,229,255,0.2); }
  }
 
  .status-dot {
    position: absolute;
    bottom: 6px;
    right: 6px;
    width: 14px;
    height: 14px;
    border-radius: 50%;
    background: var(--accent3);
    border: 2px solid var(--bg);
    animation: blink 2s step-end infinite;
  }
 
  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.3; }
  }
 
  .info { flex: 1; }
 
  .role-badge {
    display: inline-block;
    font-size: 0.65rem;
    letter-spacing: 0.2em;
    color: var(--accent);
    background: rgba(0,229,255,0.08);
    border: 1px solid rgba(0,229,255,0.2);
    padding: 3px 12px;
    margin-bottom: 10px;
    text-transform: uppercase;
  }
 
  h1 {
    font-family: 'Syne', sans-serif;
    font-size: clamp(2rem, 5vw, 3.2rem);
    font-weight: 900;
    color: #fff;
    line-height: 1;
    margin-bottom: 8px;
    letter-spacing: -1px;
  }
 
  h1 span {
    background: linear-gradient(90deg, var(--accent), #00b4d8);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
 
  .tagline {
    font-size: 0.8rem;
    color: var(--muted);
    margin-bottom: 16px;
    line-height: 1.6;
  }
 
  .tagline em {
    color: var(--accent2);
    font-style: normal;
  }
 
  .meta-row {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
    font-size: 0.72rem;
    color: var(--muted);
  }
 
  .meta-row span { display: flex; align-items: center; gap: 6px; }
  .meta-row .dot { color: var(--accent3); }
 
  /* === TYPING === */
  .typing-block {
    background: #0a1520;
    border: 1px solid var(--border);
    border-left: 3px solid var(--accent);
    padding: 20px 24px;
    margin-bottom: 32px;
    font-size: 0.82rem;
    line-height: 2;
    animation: slideDown 0.8s 0.2s cubic-bezier(0.16, 1, 0.3, 1) both;
  }
 
  .typing-block .prompt { color: var(--accent3); }
  .typing-block .cmd { color: var(--accent); }
 
  .typed-text {
    color: var(--text);
  }
 
  .cursor {
    display: inline-block;
    width: 8px;
    height: 1em;
    background: var(--accent);
    vertical-align: text-bottom;
    animation: blink-cursor 0.8s step-end infinite;
  }
 
  @keyframes blink-cursor {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
  }
 
  /* === TECH STACK === */
  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 12px;
  }
 
  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }
 
  .tech-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
    margin-bottom: 32px;
    animation: slideDown 0.8s 0.4s cubic-bezier(0.16, 1, 0.3, 1) both;
  }
 
  .tech-card {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 24px 20px;
    position: relative;
    overflow: hidden;
    cursor: default;
    transition: transform 0.3s ease, border-color 0.3s ease;
  }
 
  .tech-card::before {
    content: '';
    position: absolute;
    inset: 0;
    opacity: 0;
    transition: opacity 0.3s ease;
  }
 
  .tech-card:hover {
    transform: translateY(-4px);
    border-color: var(--card-color, var(--accent));
  }
 
  .tech-card:hover::before { opacity: 1; }
 
  .tech-card.java { --card-color: var(--java); }
  .tech-card.java::before { background: radial-gradient(ellipse at top left, rgba(248,152,32,0.08), transparent 70%); }
 
  .tech-card.python { --card-color: var(--python); }
  .tech-card.python::before { background: radial-gradient(ellipse at top left, rgba(53,114,165,0.12), transparent 70%); }
 
  .tech-card.html { --card-color: var(--html); }
  .tech-card.html::before { background: radial-gradient(ellipse at top left, rgba(227,76,38,0.1), transparent 70%); }
 
  .tech-icon {
    font-size: 2.4rem;
    margin-bottom: 14px;
    display: block;
    filter: drop-shadow(0 0 12px var(--card-color, var(--accent)));
  }
 
  .tech-name {
    font-family: 'Syne', sans-serif;
    font-size: 1rem;
    font-weight: 800;
    color: #fff;
    margin-bottom: 6px;
  }
 
  .tech-desc {
    font-size: 0.68rem;
    color: var(--muted);
    line-height: 1.6;
  }
 
  .tech-bar-wrap {
    margin-top: 14px;
    height: 3px;
    background: var(--border);
    border-radius: 2px;
    overflow: hidden;
  }
 
  .tech-bar {
    height: 100%;
    background: var(--card-color, var(--accent));
    border-radius: 2px;
    width: 0;
    animation: grow-bar 1.2s 1s ease forwards;
  }
 
  @keyframes grow-bar {
    to { width: var(--bar-width, 80%); }
  }
 
  /* === STATS === */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 12px;
    margin-bottom: 32px;
    animation: slideDown 0.8s 0.6s cubic-bezier(0.16, 1, 0.3, 1) both;
  }
 
  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 20px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
 
  .stat-card::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    height: 2px;
    background: linear-gradient(90deg, transparent, var(--accent), transparent);
    opacity: 0;
    transition: opacity 0.3s;
  }
 
  .stat-card:hover::after { opacity: 1; }
 
  .stat-num {
    font-family: 'Syne', sans-serif;
    font-size: 1.8rem;
    font-weight: 900;
    color: var(--accent);
    display: block;
    counter-reset: num var(--n);
  }
 
  .stat-label {
    font-size: 0.62rem;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.1em;
    margin-top: 4px;
    display: block;
  }
 
  /* === SKILLS BAR === */
  .skills-section {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 28px;
    margin-bottom: 32px;
    animation: slideDown 0.8s 0.7s cubic-bezier(0.16, 1, 0.3, 1) both;
  }
 
  .skill-row {
    display: grid;
    grid-template-columns: 120px 1fr 36px;
    align-items: center;
    gap: 16px;
    margin-bottom: 16px;
  }
 
  .skill-row:last-child { margin-bottom: 0; }
 
  .skill-name {
    font-size: 0.72rem;
    color: var(--text);
  }
 
  .skill-track {
    height: 6px;
    background: var(--border);
    border-radius: 3px;
    overflow: hidden;
  }
 
  .skill-fill {
    height: 100%;
    border-radius: 3px;
    width: 0;
    animation: fill-skill 1.5s 1.2s ease forwards;
  }
 
  @keyframes fill-skill {
    to { width: var(--w); }
  }
 
  .skill-pct {
    font-size: 0.65rem;
    color: var(--muted);
    text-align: right;
  }
 
  /* === FOOTER === */
  .footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px 28px;
    background: var(--surface);
    border: 1px solid var(--border);
    font-size: 0.7rem;
    animation: slideDown 0.8s 0.9s cubic-bezier(0.16, 1, 0.3, 1) both;
  }
 
  .footer-left { color: var(--muted); }
  .footer-left strong { color: var(--accent); }
 
  .badges { display: flex; gap: 8px; flex-wrap: wrap; }
 
  .badge {
    padding: 4px 12px;
    border: 1px solid var(--border);
    font-size: 0.62rem;
    letter-spacing: 0.1em;
    color: var(--muted);
    text-transform: uppercase;
    transition: all 0.2s;
    cursor: default;
  }
 
  .badge:hover {
    border-color: var(--accent);
    color: var(--accent);
    background: rgba(0,229,255,0.05);
  }
 
  /* === FLOATING PARTICLES === */
  .particles {
    position: fixed;
    inset: 0;
    pointer-events: none;
    z-index: 0;
    overflow: hidden;
  }
 
  .particle {
    position: absolute;
    width: 2px;
    height: 2px;
    background: var(--accent);
    border-radius: 50%;
    opacity: 0;
    animation: float-particle var(--dur, 8s) var(--delay, 0s) linear infinite;
  }
 
  @keyframes float-particle {
    0% { transform: translateY(100vh) translateX(0); opacity: 0; }
    10% { opacity: 0.5; }
    90% { opacity: 0.3; }
    100% { transform: translateY(-20px) translateX(var(--drift, 40px)); opacity: 0; }
  }
 
  @keyframes slideDown {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
 
  @media (max-width: 640px) {
    .header { flex-direction: column; align-items: center; text-align: center; }
    .tech-grid { grid-template-columns: 1fr; }
    .stats-row { grid-template-columns: repeat(2, 1fr); }
    .skill-row { grid-template-columns: 90px 1fr 30px; }
    .footer { flex-direction: column; gap: 12px; align-items: flex-start; }
  }
</style>
</head>
<body>
 
<!-- Floating particles -->
<div class="particles" id="particles"></div>
 
<div class="container">
 
  <!-- HEADER -->
  <div class="header">
    <div class="corner tl"></div>
    <div class="corner tr"></div>
    <div class="corner bl"></div>
    <div class="corner br"></div>
 
    <div class="avatar-wrap">
      <div class="avatar">WL</div>
      <div class="status-dot" title="Disponível para projetos"></div>
    </div>
 
    <div class="info">
      <div class="role-badge">// Backend Developer</div>
      <h1>Weyk <span>Lopes</span></h1>
      <p class="tagline">
        Construindo o <em>invisível</em> que faz tudo funcionar.<br>
        APIs, servidores e lógica que sustentam o mundo digital.
      </p>
      <div class="meta-row">
        <span><span class="dot">▸</span> Fortaleza, BR</span>
        <span><span class="dot">▸</span> Backend Engineering</span>
        <span><span class="dot">▸</span> Open to collab</span>
      </div>
    </div>
  </div>
 
  <!-- TERMINAL BLOCK -->
  <div class="typing-block">
    <div><span class="prompt">weyk@dev</span>:<span style="color:var(--accent2)">~</span>$ <span class="cmd">whoami</span></div>
    <div class="typed-text" id="typed"></div>
    <div><span class="cursor"></span></div>
  </div>
 
  <!-- TECH STACK -->
  <div class="section-title">// stack principal</div>
  <div class="tech-grid">
 
    <div class="tech-card java">
      <span class="tech-icon">☕</span>
      <div class="tech-name">Java</div>
      <div class="tech-desc">Spring Boot · APIs REST · Microserviços · JVM Performance</div>
      <div class="tech-bar-wrap">
        <div class="tech-bar" style="--bar-width: 88%; background: var(--java);"></div>
      </div>
    </div>
 
    <div class="tech-card python">
      <span class="tech-icon">🐍</span>
      <div class="tech-name">Python</div>
      <div class="tech-desc">FastAPI · Django · Automação · Scripting · Data Processing</div>
      <div class="tech-bar-wrap">
        <div class="tech-bar" style="--bar-width: 85%; background: var(--python);"></div>
      </div>
    </div>
 
    <div class="tech-card html">
      <span class="tech-icon">🌐</span>
      <div class="tech-name">HTML</div>
      <div class="tech-desc">Semântica · Templates · Integração Frontend · Web Standards</div>
      <div class="tech-bar-wrap">
        <div class="tech-bar" style="--bar-width: 75%; background: var(--html);"></div>
      </div>
    </div>
 
  </div>
 
  <!-- STATS -->
  <div class="section-title">// números</div>
  <div class="stats-row">
    <div class="stat-card">
      <span class="stat-num" id="repos">0</span>
      <span class="stat-label">Repositórios</span>
    </div>
    <div class="stat-card">
      <span class="stat-num" id="commits">0</span>
      <span class="stat-label">Commits</span>
    </div>
    <div class="stat-card">
      <span class="stat-num" id="apis">0</span>
      <span class="stat-label">APIs Criadas</span>
    </div>
    <div class="stat-card">
      <span class="stat-num" id="coffee">0</span>
      <span class="stat-label">Cafés ☕</span>
    </div>
  </div>
 
  <!-- SKILLS -->
  <div class="section-title">// habilidades</div>
  <div class="skills-section">
 
    <div class="skill-row">
      <span class="skill-name">REST APIs</span>
      <div class="skill-track">
        <div class="skill-fill" style="--w: 92%; background: linear-gradient(90deg, var(--accent), #0077b6);"></div>
      </div>
      <span class="skill-pct">92%</span>
    </div>
 
    <div class="skill-row">
      <span class="skill-name">Spring Boot</span>
      <div class="skill-track">
        <div class="skill-fill" style="--w: 85%; background: linear-gradient(90deg, var(--java), #d4850a);"></div>
      </div>
      <span class="skill-pct">85%</span>
    </div>
 
    <div class="skill-row">
      <span class="skill-name">Python/FastAPI</span>
      <div class="skill-track">
        <div class="skill-fill" style="--w: 82%; background: linear-gradient(90deg, var(--python), #2e5f8a);"></div>
      </div>
      <span class="skill-pct">82%</span>
    </div>
 
    <div class="skill-row">
      <span class="skill-name">Banco de Dados</span>
      <div class="skill-track">
        <div class="skill-fill" style="--w: 80%; background: linear-gradient(90deg, var(--accent2), #c84b1a);"></div>
      </div>
      <span class="skill-pct">80%</span>
    </div>
 
    <div class="skill-row">
      <span class="skill-name">Docker / DevOps</span>
      <div class="skill-track">
        <div class="skill-fill" style="--w: 70%; background: linear-gradient(90deg, #48cae4, #0077b6);"></div>
      </div>
      <span class="skill-pct">70%</span>
    </div>
 
  </div>
 
  <!-- FOOTER -->
  <div class="footer">
    <div class="footer-left">
      <strong>@weyrlopes</strong> · Atualizado 2025<br>
      <span style="color: var(--accent3);">▸ Disponível para novos projetos</span>
    </div>
    <div class="badges">
      <div class="badge">Git</div>
      <div class="badge">Docker</div>
      <div class="badge">SQL</div>
      <div class="badge">Linux</div>
      <div class="badge">CI/CD</div>
    </div>
  </div>
 
</div>
 
<script>
  // === PARTICLES ===
  const container = document.getElementById('particles');
  for (let i = 0; i < 25; i++) {
    const p = document.createElement('div');
    p.className = 'particle';
    p.style.left = Math.random() * 100 + 'vw';
    p.style.setProperty('--dur', (6 + Math.random() * 10) + 's');
    p.style.setProperty('--delay', (Math.random() * 8) + 's');
    p.style.setProperty('--drift', (Math.random() * 80 - 40) + 'px');
    if (i % 3 === 0) p.style.background = '#ff6b35';
    if (i % 5 === 0) p.style.background = '#7fff6e';
    container.appendChild(p);
  }
 
  // === TYPING ===
  const text = "Backend developer · Java & Python · APIs, serviços e sistemas robustos. Apaixonado por código limpo e arquitetura escalável.";
  let i = 0;
  const el = document.getElementById('typed');
  function type() {
    if (i < text.length) {
      el.textContent += text[i++];
      setTimeout(type, 28 + Math.random() * 20);
    }
  }
  setTimeout(type, 800);
 
  // === COUNTERS ===
  function animateCount(id, target, suffix = '') {
    const el = document.getElementById(id);
    let current = 0;
    const step = Math.ceil(target / 50);
    const interval = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent = current + suffix;
      if (current >= target) clearInterval(interval);
    }, 30);
  }
 
  setTimeout(() => {
    animateCount('repos', 24);
    animateCount('commits', 312, '+');
    animateCount('apis', 18);
    animateCount('coffee', 999, '+');
  }, 600);
</script>
</body>
</html>
 
