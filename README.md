<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Erfan Akhavan Rad — Profile</title>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;600&family=IBM+Plex+Sans:wght@300;400;500;600&display=swap" rel="stylesheet" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg:        #0e1117;
    --surface:   #161b22;
    --border:    #21262d;
    --gold:      #C9974A;
    --gold-dim:  #8c6830;
    --text:      #e6e1d8;
    --muted:     #8b949e;
    --white:     #f0ece4;
    --page-w:    780px;
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'IBM Plex Sans', sans-serif;
    font-size: 15px;
    line-height: 1.7;
    padding: 60px 24px 80px;
  }

  /* ── Page shell ── */
  .letter {
    max-width: var(--page-w);
    margin: 0 auto;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 56px 64px;
  }

  /* ── Header ── */
  .header {
    border-bottom: 1px solid var(--border);
    padding-bottom: 36px;
    margin-bottom: 40px;
  }

  .header h1 {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 26px;
    font-weight: 600;
    color: var(--white);
    letter-spacing: -0.5px;
    margin-bottom: 6px;
  }

  .header h1 span { color: var(--gold); }

  .header p {
    color: var(--muted);
    font-size: 13.5px;
    font-family: 'IBM Plex Mono', monospace;
    letter-spacing: 0.4px;
  }

  /* ── Bio block ── */
  .bio {
    margin-bottom: 40px;
    font-size: 15.5px;
    color: var(--text);
    line-height: 1.75;
  }

  .bio strong {
    color: var(--white);
    font-weight: 600;
  }

  /* ── Section headings ── */
  h2 {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 2.5px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 20px;
    padding-bottom: 8px;
    border-bottom: 1px solid var(--border);
  }

  section { margin-bottom: 44px; }

  /* ── Tech stack grid ── */
  .stack-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
  }

  .stack-group h3 {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 1.8px;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 12px;
  }

  .badges {
    display: flex;
    flex-wrap: wrap;
    gap: 7px;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    padding: 4px 10px;
    border-radius: 4px;
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    font-weight: 600;
    border: 1px solid var(--border);
    background: var(--bg);
    color: var(--text);
    white-space: nowrap;
  }

  .badge-dot {
    width: 7px; height: 7px;
    border-radius: 50%;
    flex-shrink: 0;
  }

  /* Core */
  .c-java    { background:#ED8B00; }
  .c-kotlin  { background:#7F52FF; }
  .c-spring  { background:#6DB33F; }
  .c-rest    { background:#FF6B35; }
  /* DB */
  .c-oracle  { background:#F80000; }
  .c-mssql   { background:#CC2927; }
  .c-redis   { background:#DC382D; }
  /* DevOps */
  .c-docker  { background:#2496ED; }
  .c-jenkins { background:#D24939; }
  .c-git     { background:#F05032; }
  .c-maven   { background:#C71A36; }
  .c-linux   { background:#FCC624; }
  .c-liqui   { background:#2962FF; }
  /* Monitor */
  .c-prom    { background:#E6522C; }
  .c-grafana { background:#F46800; }
  .c-elk     { background:#005571; }
  /* AI */
  .c-opencv  { background:#5C3EE8; }
  .c-python  { background:#3776AB; }

  /* ── Projects ── */
  .project {
    padding: 22px 24px;
    border: 1px solid var(--border);
    border-radius: 5px;
    background: var(--bg);
    margin-bottom: 14px;
  }

  .project:last-child { margin-bottom: 0; }

  .project-header {
    display: flex;
    align-items: baseline;
    gap: 10px;
    margin-bottom: 10px;
  }

  .project-icon {
    font-size: 16px;
    line-height: 1;
    flex-shrink: 0;
  }

  .project-title {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 14px;
    font-weight: 600;
    color: var(--white);
  }

  .project-org {
    font-size: 12px;
    color: var(--gold-dim);
    font-family: 'IBM Plex Mono', monospace;
    margin-left: auto;
    white-space: nowrap;
  }

  .project p {
    font-size: 14px;
    color: var(--muted);
    line-height: 1.65;
    margin-bottom: 12px;
  }

  .tech-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }

  .tech-tag {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 10.5px;
    color: var(--gold);
    background: rgba(201,151,74,.08);
    border: 1px solid rgba(201,151,74,.2);
    padding: 2px 8px;
    border-radius: 3px;
  }

  /* ── Stats (centered) ── */
  .stats-center {
    text-align: center;
    padding: 24px 0;
  }

  .stats-center img {
    border-radius: 4px;
    max-width: 100%;
  }

  /* ── Connect (centered) ── */
  .connect-center {
    text-align: center;
    padding-top: 8px;
  }

  .location-note {
    font-size: 13.5px;
    color: var(--muted);
    margin-bottom: 24px;
    font-family: 'IBM Plex Mono', monospace;
  }

  .cta-links {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 28px;
  }

  .cta-link {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    padding: 9px 18px;
    border-radius: 4px;
    font-family: 'IBM Plex Mono', monospace;
    font-size: 12px;
    font-weight: 600;
    text-decoration: none;
    transition: opacity .15s;
  }

  .cta-link:hover { opacity: .8; }

  .cta-linkedin  { background: #0A66C2; color: #fff; }
  .cta-portfolio { background: var(--gold); color: #111; }
  .cta-email     { background: #EA4335; color: #fff; }

  /* ── Footer tagline (centered) ── */
  .tagline {
    text-align: center;
    margin-top: 40px;
    padding-top: 28px;
    border-top: 1px solid var(--border);
  }

  .tagline blockquote {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 12.5px;
    color: var(--muted);
    font-style: italic;
    margin-bottom: 12px;
  }

  .footer-meta {
    font-size: 12px;
    color: var(--gold-dim);
    font-family: 'IBM Plex Mono', monospace;
  }

  /* ── Responsive ── */
  @media (max-width: 620px) {
    .letter { padding: 32px 24px; }
    .stack-grid { grid-template-columns: 1fr; }
    .project-org { display: none; }
  }
</style>
</head>
<body>
<div class="letter">

  <!-- Header -->
  <div class="header">
    <h1>👋 Hey, I'm <span>Erfan</span></h1>
    <p>📍 Oldenburg, Germany · Backend Engineer · Werkstudent (20 hrs/week)</p>
  </div>

  <!-- Bio -->
  <div class="bio">
    I'm a backend engineer with <strong>5+ years</strong> building production-grade systems in <strong>Java and Spring Boot</strong> — from insurtech APIs handling high-traffic insurance flows, to a neobank's distributed cheque processing platform, to a real-time KYC liveness detection engine.<br /><br />
    I care about systems that are fast, maintainable, and designed to last. I'm the kind of engineer who writes the C4 diagram <em>and</em> the pessimistic lock — then refactors 30% of the legacy codebase for good measure.
  </div>

  <!-- Tech Stack -->
  <section>
    <h2>🛠️ Tech Stack</h2>

    <!-- Core Backend — full width -->
    <div style="margin-bottom:20px;">
      <div class="stack-group">
        <h3>☕ Core Backend</h3>
        <div class="badges">
          <span class="badge"><span class="badge-dot c-java"></span>Java</span>
          <span class="badge"><span class="badge-dot c-kotlin"></span>Kotlin</span>
          <span class="badge"><span class="badge-dot c-spring"></span>Spring Boot</span>
          <span class="badge"><span class="badge-dot c-spring"></span>Spring Security</span>
          <span class="badge"><span class="badge-dot c-rest"></span>REST APIs</span>
        </div>
      </div>
    </div>

    <div class="stack-grid">
      <div class="stack-group">
        <h3>🗄️ Databases &amp; Cache</h3>
        <div class="badges">
          <span class="badge"><span class="badge-dot c-oracle"></span>Oracle</span>
          <span class="badge"><span class="badge-dot c-mssql"></span>MS SQL Server</span>
          <span class="badge"><span class="badge-dot c-redis"></span>Redis</span>
        </div>
      </div>

      <div class="stack-group">
        <h3>🐳 DevOps &amp; Tools</h3>
        <div class="badges">
          <span class="badge"><span class="badge-dot c-docker"></span>Docker</span>
          <span class="badge"><span class="badge-dot c-jenkins"></span>Jenkins</span>
          <span class="badge"><span class="badge-dot c-git"></span>Git</span>
          <span class="badge"><span class="badge-dot c-maven"></span>Maven</span>
          <span class="badge"><span class="badge-dot c-linux" style="background:#FCC624;"></span>Linux</span>
          <span class="badge"><span class="badge-dot c-liqui"></span>Liquibase</span>
        </div>
      </div>

      <div class="stack-group">
        <h3>📊 Monitoring</h3>
        <div class="badges">
          <span class="badge"><span class="badge-dot c-prom"></span>Prometheus</span>
          <span class="badge"><span class="badge-dot c-grafana"></span>Grafana</span>
          <span class="badge"><span class="badge-dot c-elk"></span>ELK Stack</span>
        </div>
      </div>

      <div class="stack-group">
        <h3>🤖 AI / Computer Vision</h3>
        <div class="badges">
          <span class="badge"><span class="badge-dot c-opencv"></span>OpenCV</span>
          <span class="badge"><span class="badge-dot c-python"></span>Python</span>
        </div>
      </div>
    </div>
  </section>

  <!-- Projects -->
  <section>
    <h2>🏗️ What I've Built</h2>

    <div class="project">
      <div class="project-header">
        <span class="project-icon">🏦</span>
        <span class="project-title">Chequead — Distributed Online Cheque System</span>
        <span class="project-org">ABank</span>
      </div>
      <p>A fully distributed cheque management platform built for Iran's ABank (Neo Bank of Ayandeh Bank). Covered the entire cheque lifecycle: <strong>issuance → ownership transfer → validation → blocking → bouncing</strong>. Focused on transaction security, audit traceability, and integration with core banking services. Documented with C4 architecture diagrams.</p>
      <div class="tech-tags">
        <span class="tech-tag">Spring Boot</span>
        <span class="tech-tag">Distributed Systems</span>
        <span class="tech-tag">Oracle</span>
        <span class="tech-tag">REST API</span>
        <span class="tech-tag">C4</span>
      </div>
    </div>

    <div class="project">
      <div class="project-header">
        <span class="project-icon">🔍</span>
        <span class="project-title">KYC Liveness Detection Engine</span>
        <span class="project-org">ABank</span>
      </div>
      <p>Real-time video analysis system for ABank's KYC onboarding to prevent identity spoofing. Analyzed <strong>moiré patterns, blur, blink detection, lip movement, emotional shifts, and demographic variance</strong> using a combination of DeepFace deep learning models, OpenCV preprocessing pipelines, and custom heuristics.</p>
      <div class="tech-tags">
        <span class="tech-tag">OpenCV</span>
        <span class="tech-tag">DeepFace</span>
        <span class="tech-tag">Python</span>
        <span class="tech-tag">Spring Boot</span>
        <span class="tech-tag">Computer Vision</span>
      </div>
    </div>

    <div class="project">
      <div class="project-header">
        <span class="project-icon">🎁</span>
        <span class="project-title">Digital Present — P2P Money Gifting Feature</span>
        <span class="project-org">ABank</span>
      </div>
      <p>Peer-to-peer money gifting system eliminating the need for physical gift cards. Features: automatic expiration with fund reversal, unique redemption code generation, and eligibility verification for secure transactions.</p>
      <div class="tech-tags">
        <span class="tech-tag">Spring Boot</span>
        <span class="tech-tag">Redis</span>
        <span class="tech-tag">Banking APIs</span>
        <span class="tech-tag">Security</span>
      </div>
    </div>

    <div class="project">
      <div class="project-header">
        <span class="project-icon">📅</span>
        <span class="project-title">High-Performance Reservation System</span>
        <span class="project-org">Personal Project</span>
      </div>
      <p>Reservation engine designed for millions of concurrent time-slot records. Solved double-booking using <strong>pessimistic locking</strong> at the database level. Built lightweight REST endpoints for real-time availability checks and used Redis caching to offload read pressure from hot slot ranges.</p>
      <div class="tech-tags">
        <span class="tech-tag">Spring Boot</span>
        <span class="tech-tag">Redis</span>
        <span class="tech-tag">Docker</span>
        <span class="tech-tag">Pessimistic Locking</span>
        <span class="tech-tag">Concurrency</span>
      </div>
    </div>

    <div class="project">
      <div class="project-header">
        <span class="project-icon">⚡</span>
        <span class="project-title">Tax Clearance System — Built in 45 Days</span>
        <span class="project-org">Taraz Group</span>
      </div>
      <p>When Iran's National Tax Administration (INTA) declared a new invoicing law in 2022, our team designed, developed, tested, and deployed a nationwide <strong>tax clearance system in 45 days</strong>. Zero buffer. Full lifecycle.</p>
      <div class="tech-tags">
        <span class="tech-tag">Spring Boot</span>
        <span class="tech-tag">REST API</span>
        <span class="tech-tag">Oracle</span>
        <span class="tech-tag">Agile</span>
      </div>
    </div>
  </section>

  <!-- GitHub Stats (centered) -->
  <section>
    <h2>📈 GitHub Stats</h2>
    <div class="stats-center">
      <img
        src="https://github-readme-stats.vercel.app/api/top-langs/?username=erfanakhavanrad&layout=compact&theme=dark&bg_color=111318&title_color=C9974A&text_color=E8E5DF&border_color=21252E"
        alt="Top Languages"
      />
    </div>
  </section>

  <!-- Connect (centered) -->
  <section>
    <h2>📬 Let's Connect</h2>
    <div class="connect-center">
      <p class="location-note">Based in Oldenburg, Germany · Open to Werkstudent roles (20 hrs/week), remote or on-site.</p>
      <div class="cta-links">
        <a class="cta-link cta-linkedin"  href="https://linkedin.com/in/erfan-akhavan-rad" target="_blank">🔗 Connect on LinkedIn</a>
        <a class="cta-link cta-portfolio" href="https://erfanakhavanrad.github.io"          target="_blank">🌐 Visit Portfolio</a>
        <a class="cta-link cta-email"     href="mailto:erfanakhavanrad@gmail.com"            target="_blank">✉️ Send Email</a>
      </div>
    </div>
  </section>

  <!-- Tagline footer (centered) -->
  <div class="tagline">
    <blockquote>"Ship systems that scale. Write code that lasts. Never stop refactoring."</blockquote>
    <div class="footer-meta">📍 Oldenburg, Germany · ☕ Powered by Java &amp; too much coffee</div>
  </div>

</div>
</body>
</html>
