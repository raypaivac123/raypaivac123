<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Rayssa Paiva | Perfil</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --bg-1: #0f172a;
      --bg-2: #111827;
      --card: rgba(255, 255, 255, 0.08);
      --card-strong: rgba(255, 255, 255, 0.12);
      --text: #f8fafc;
      --muted: #cbd5e1;
      --accent: #38bdf8;
      --accent-2: #a78bfa;
      --accent-3: #22c55e;
      --border: rgba(255,255,255,0.14);
      --shadow: 0 20px 40px rgba(0,0,0,0.35);
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      color: var(--text);
      min-height: 100vh;
      background:
        radial-gradient(circle at top left, rgba(56,189,248,0.25), transparent 28%),
        radial-gradient(circle at 85% 15%, rgba(167,139,250,0.22), transparent 25%),
        radial-gradient(circle at 50% 100%, rgba(34,197,94,0.14), transparent 25%),
        linear-gradient(135deg, var(--bg-1), var(--bg-2));
      overflow-x: hidden;
      position: relative;
    }

    .particles {
      position: fixed;
      inset: 0;
      overflow: hidden;
      pointer-events: none;
      z-index: 0;
    }

    .particle {
      position: absolute;
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: rgba(255,255,255,0.18);
      animation: floatUp linear infinite;
    }

    @keyframes floatUp {
      from {
        transform: translateY(110vh) scale(0.8);
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      90% {
        opacity: 0.8;
      }
      to {
        transform: translateY(-15vh) scale(1.25);
        opacity: 0;
      }
    }

    .container {
      position: relative;
      z-index: 1;
      width: min(1100px, 92%);
      margin: 0 auto;
      padding: 48px 0 70px;
    }

    .hero {
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 28px;
      align-items: stretch;
      margin-bottom: 28px;
    }

    .card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 28px;
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      box-shadow: var(--shadow);
    }

    .hero-main {
      padding: 34px;
      position: relative;
      overflow: hidden;
    }

    .hero-main::before {
      content: "";
      position: absolute;
      width: 220px;
      height: 220px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(56,189,248,0.22), transparent 70%);
      top: -70px;
      right: -60px;
      animation: pulse 4s ease-in-out infinite;
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); opacity: 0.9; }
      50% { transform: scale(1.12); opacity: 0.55; }
    }

    .tag {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 8px 14px;
      border-radius: 999px;
      background: rgba(255,255,255,0.08);
      border: 1px solid rgba(255,255,255,0.12);
      color: var(--muted);
      font-size: 14px;
      margin-bottom: 18px;
      animation: slideDown 0.8s ease;
    }

    @keyframes slideDown {
      from { opacity: 0; transform: translateY(-18px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h1 {
      font-size: clamp(2.1rem, 5vw, 3.6rem);
      line-height: 1.08;
      margin-bottom: 14px;
      animation: fadeUp 0.9s ease both;
    }

    .gradient-text {
      background: linear-gradient(90deg, #38bdf8, #a78bfa, #22c55e);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      background-size: 220% auto;
      animation: shine 6s linear infinite;
    }

    @keyframes shine {
      to { background-position: 220% center; }
    }

    .subtitle {
      color: var(--muted);
      font-size: 1.08rem;
      line-height: 1.75;
      max-width: 700px;
      animation: fadeUp 1.1s ease both;
    }

    .typing-line {
      margin-top: 18px;
      min-height: 32px;
      font-size: 1rem;
      color: #e2e8f0;
      font-weight: bold;
      animation: fadeUp 1.3s ease both;
    }

    .typing-line span {
      color: var(--accent);
      border-right: 2px solid var(--accent);
      padding-right: 4px;
      animation: blink 0.8s infinite;
    }

    @keyframes blink {
      50% { border-color: transparent; }
    }

    .hero-side {
      padding: 28px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      gap: 18px;
      animation: fadeUp 1.2s ease both;
    }

    .profile-badge {
      display: grid;
      place-items: center;
      min-height: 220px;
      border-radius: 24px;
      background: linear-gradient(145deg, rgba(56,189,248,0.18), rgba(167,139,250,0.12));
      border: 1px solid rgba(255,255,255,0.12);
      text-align: center;
      padding: 24px;
    }

    .avatar {
      width: 110px;
      height: 110px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      font-size: 44px;
      margin-bottom: 12px;
      background: rgba(255,255,255,0.12);
      box-shadow: 0 12px 30px rgba(0,0,0,0.25);
      animation: levitate 3s ease-in-out infinite;
    }

    @keyframes levitate {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    .profile-badge h2 {
      font-size: 1.35rem;
      margin-bottom: 6px;
    }

    .profile-badge p {
      color: var(--muted);
      line-height: 1.6;
    }

    .socials {
      display: grid;
      gap: 12px;
    }

    .social-link {
      text-decoration: none;
      color: var(--text);
      border: 1px solid rgba(255,255,255,0.12);
      background: rgba(255,255,255,0.05);
      padding: 14px 16px;
      border-radius: 16px;
      transition: transform 0.25s ease, background 0.25s ease, border-color 0.25s ease;
    }

    .social-link:hover {
      transform: translateY(-4px);
      background: rgba(255,255,255,0.1);
      border-color: rgba(56,189,248,0.45);
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 28px;
      margin-bottom: 28px;
    }

    .section {
      padding: 28px;
      animation: fadeUp 1s ease both;
    }

    @keyframes fadeUp {
      from {
        opacity: 0;
        transform: translateY(24px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .section-title {
      font-size: 1.4rem;
      margin-bottom: 18px;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .section-title::before {
      content: "";
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: linear-gradient(90deg, var(--accent), var(--accent-2));
      box-shadow: 0 0 20px rgba(56,189,248,0.6);
    }

    .about-text {
      color: var(--muted);
      line-height: 1.8;
      font-size: 1rem;
    }

    .tech-list {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .tech {
      padding: 12px 16px;
      border-radius: 999px;
      background: rgba(255,255,255,0.07);
      border: 1px solid rgba(255,255,255,0.12);
      color: #f8fafc;
      font-weight: bold;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
      cursor: default;
    }

    .tech:hover {
      transform: scale(1.06);
      box-shadow: 0 10px 25px rgba(0,0,0,0.25);
    }

    .stats {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 14px;
      margin-top: 20px;
    }

    .stat-box {
      padding: 18px;
      border-radius: 20px;
      background: rgba(255,255,255,0.06);
      border: 1px solid rgba(255,255,255,0.1);
      text-align: center;
      transition: transform 0.25s ease;
    }

    .stat-box:hover {
      transform: translateY(-5px);
    }

    .stat-number {
      font-size: 1.7rem;
      font-weight: bold;
      color: var(--accent);
      margin-bottom: 6px;
    }

    .stat-label {
      color: var(--muted);
      font-size: 0.95rem;
    }

    .full {
      padding: 28px;
    }

    .timeline {
      display: grid;
      gap: 16px;
      margin-top: 12px;
    }

    .timeline-item {
      position: relative;
      padding: 18px 18px 18px 22px;
      border-left: 3px solid rgba(56,189,248,0.45);
      background: rgba(255,255,255,0.05);
      border-radius: 0 18px 18px 0;
      color: var(--muted);
      line-height: 1.7;
      transition: transform 0.25s ease, background 0.25s ease;
    }

    .timeline-item:hover {
      transform: translateX(6px);
      background: rgba(255,255,255,0.08);
    }

    .timeline-item strong {
      color: var(--text);
      display: block;
      margin-bottom: 4px;
    }

    .footer-note {
      text-align: center;
      color: var(--muted);
      margin-top: 28px;
      font-size: 0.95rem;
      opacity: 0.9;
    }

    .btn-row {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 24px;
    }

    .btn {
      text-decoration: none;
      color: var(--text);
      padding: 12px 18px;
      border-radius: 14px;
      border: 1px solid rgba(255,255,255,0.14);
      background: rgba(255,255,255,0.08);
      transition: transform 0.25s ease, background 0.25s ease, box-shadow 0.25s ease;
      font-weight: bold;
    }

    .btn:hover {
      transform: translateY(-4px);
      background: rgba(56,189,248,0.18);
      box-shadow: 0 12px 24px rgba(0,0,0,0.22);
    }

    @media (max-width: 900px) {
      .hero,
      .grid {
        grid-template-columns: 1fr;
      }

      .stats {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 560px) {
      .container {
        width: 94%;
        padding-top: 22px;
      }

      .hero-main,
      .hero-side,
      .section,
      .full {
        padding: 22px;
      }

      h1 {
        font-size: 2rem;
      }

      .subtitle,
      .about-text,
      .timeline-item {
        font-size: 0.96rem;
      }
    }
  </style>
</head>
<body>
  <div class="particles" id="particles"></div>

  <main class="container">
    <section class="hero">
      <div class="card hero-main">
        <div class="tag">✨ Portfólio em evolução • Backend • Java • SENAC</div>
        <h1>Olá 👋, eu sou <span class="gradient-text">Rayssa Paiva</span></h1>
        <p class="subtitle">
          Formada em Ciência da Computação, instrutora de tecnologia no SENAC e desenvolvedora backend em formação.
          Estou aprimorando minhas habilidades em Java, Spring Boot, APIs REST e bancos de dados, com foco em construir
          projetos reais, bem estruturados e com propósito.
        </p>
        <div class="typing-line">Foco atual: <span id="typed-text"></span></div>

        <div class="btn-row">
          <a class="btn" href="https://www.linkedin.com/in/rayssa-paiva-0565301b9/" target="_blank">LinkedIn</a>
          <a class="btn" href="mailto:rayssa.estudos25@gmail.com">E-mail</a>
          <a class="btn" href="https://github.com/raypaivac123" target="_blank">GitHub</a>
        </div>
      </div>

      <aside class="card hero-side">
        <div class="profile-badge">
          <div class="avatar">💻</div>
          <h2>Backend em construção</h2>
          <p>Projetos, estudo contínuo e evolução prática rumo a oportunidades internacionais.</p>
        </div>

        <div class="socials">
          <a class="social-link" href="https://www.linkedin.com/in/rayssa-paiva-0565301b9/" target="_blank">
            <strong>LinkedIn</strong><br>
            Conecte-se comigo profissionalmente
          </a>
          <a class="social-link" href="mailto:rayssa.estudos25@gmail.com">
            <strong>E-mail</strong><br>
            rayssa.estudos25@gmail.com
          </a>
        </div>
      </aside>
    </section>

    <section class="grid">
      <div class="card section">
        <h2 class="section-title">Sobre mim</h2>
        <p class="about-text">
          Sou apaixonada por tecnologia, ensino e construção de soluções que possam ser aplicadas no mundo real.
          Minha jornada une prática, estudo e desenvolvimento constante, com foco especial em backend com Java.
          Atualmente, estou fortalecendo meus conhecimentos em APIs REST, banco de dados, arquitetura de software
          e boas práticas de programação.
        </p>

        <div class="stats">
          <div class="stat-box">
            <div class="stat-number" data-target="8">0</div>
            <div class="stat-label">Tecnologias em foco</div>
          </div>
          <div class="stat-box">
            <div class="stat-number" data-target="100">0</div>
            <div class="stat-label">Determinação</div>
          </div>
          <div class="stat-box">
            <div class="stat-number" data-target="24">0</div>
            <div class="stat-label">Aprendizado contínuo</div>
          </div>
        </div>
      </div>

      <div class="card section">
        <h2 class="section-title">Linguagens e Ferramentas</h2>
        <div class="tech-list">
          <div class="tech">Java</div>
          <div class="tech">Spring Boot</div>
          <div class="tech">MySQL</div>
          <div class="tech">HTML</div>
          <div class="tech">CSS</div>
          <div class="tech">JavaScript</div>
          <div class="tech">Git</div>
          <div class="tech">GitHub</div>
          <div class="tech">APIs REST</div>
          <div class="tech">Banco de Dados</div>
        </div>
      </div>
    </section>

    <section class="card full">
      <h2 class="section-title">Minha jornada</h2>
      <div class="timeline">
        <div class="timeline-item">
          <strong>Formação em Ciência da Computação</strong>
          Base sólida em lógica, programação e desenvolvimento de sistemas.
        </div>
        <div class="timeline-item">
          <strong>Instrutora de Tecnologia no SENAC</strong>
          Experiência com ensino, projetos práticos e incentivo ao aprendizado aplicado.
        </div>
        <div class="timeline-item">
          <strong>Especialização prática em Backend</strong>
          Desenvolvimento de projetos com Java, Spring Boot, APIs REST e integração com banco de dados.
        </div>
        <div class="timeline-item">
          <strong>Objetivo profissional</strong>
          Crescer como desenvolvedora backend, construir projetos robustos e conquistar oportunidades internacionais.
        </div>
      </div>
    </section>

    <p class="footer-note">
      Feito com dedicação, criatividade e muita vontade de evoluir na tecnologia. ✨
    </p>
  </main>

  <script>
    const phrases = [
      "Java e Spring Boot",
      "APIs REST e integração web",
      "Banco de dados e boas práticas",
      "Projetos reais para portfólio",
      "Oportunidades internacionais"
    ];

    const typedText = document.getElementById("typed-text");
    let phraseIndex = 0;
    let charIndex = 0;
    let deleting = false;

    function typeEffect() {
      const current = phrases[phraseIndex];

      if (!deleting) {
        typedText.textContent = current.slice(0, charIndex + 1);
        charIndex++;

        if (charIndex === current.length) {
          deleting = true;
          setTimeout(typeEffect, 1300);
          return;
        }
      } else {
        typedText.textContent = current.slice(0, charIndex - 1);
        charIndex--;

        if (charIndex === 0) {
          deleting = false;
          phraseIndex = (phraseIndex + 1) % phrases.length;
        }
      }

      setTimeout(typeEffect, deleting ? 45 : 90);
    }

    typeEffect();

    const counters = document.querySelectorAll(".stat-number");

    const animateCounter = (counter) => {
      const target = Number(counter.dataset.target);
      let current = 0;
      const increment = Math.max(1, Math.ceil(target / 45));

      const update = () => {
        current += increment;
        if (current > target) current = target;
        counter.textContent = current;
        if (current < target) requestAnimationFrame(update);
      };

      update();
    };

    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          animateCounter(entry.target);
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.8 });

    counters.forEach(counter => observer.observe(counter));

    const particleContainer = document.getElementById("particles");
    for (let i = 0; i < 28; i++) {
      const particle = document.createElement("div");
      particle.className = "particle";
      particle.style.left = Math.random() * 100 + "%";
      particle.style.animationDuration = (8 + Math.random() * 12) + "s";
      particle.style.animationDelay = (Math.random() * 8) + "s";
      particle.style.opacity = Math.random().toFixed(2);
      particle.style.transform = `scale(${0.6 + Math.random()})`;
      particleContainer.appendChild(particle);
    }
  </script>
</body>
</html>
