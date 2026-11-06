<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>DH CLUB — Digital Hub Club</title>
  <meta name="description" content="Digital Hub Club — club informatique et digital : programmation, design, 3D et gestion de projets." />
  
  <!-- Polices Google : Orbitron (futuriste) + Poppins (moderne) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@700;900&family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
  
  <style>
    /* ==========================================================
       VARIABLES & THÈMES
       ========================================================== */
    :root {
      --bg-primary: #f7f9fc;
      --bg-secondary: #ffffff;
      --bg-accent: #eef2f7;
      --text-primary: #1a2233;
      --text-secondary: #4a5568;
      --accent-color: #4f8cff;
      --accent-hover: #356fe0;
      --border-color: #e2e8f0;
      --shadow: 0 4px 20px rgba(0, 0, 0, 0.06);
      --shadow-lg: 0 10px 40px rgba(79, 140, 255, 0.15);
      --radius: 16px;
      --transition: 0.3s ease;
    }

    body.dark {
      --bg-primary: #0f1420;
      --bg-secondary: #1a2233;
      --bg-accent: #141b2b;
      --text-primary: #e8eef7;
      --text-secondary: #a0aec0;
      --border-color: #2d3748;
      --shadow: 0 4px 20px rgba(0, 0, 0, 0.4);
    }

    /* ==========================================================
       RESET & BASE
       ========================================================== */
    *, *::before, *::after {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 80px;
    }

    body {
      font-family: 'Poppins', system-ui, -apple-system, sans-serif;
      background: var(--bg-primary);
      color: var(--text-primary);
      line-height: 1.6;
      transition: background var(--transition), color var(--transition);
    }

    a { color: inherit; text-decoration: none; }
    img { max-width: 100%; display: block; }

    /* ==========================================================
       LOGO "DH" STYLISÉ (remplace l'image)
       ========================================================== */
    .dh-logo {
      font-family: 'Orbitron', sans-serif;
      font-weight: 900;
      font-size: 32px;
      letter-spacing: 2px;
      line-height: 1;
      background: linear-gradient(135deg, #00c6ff 0%, #0072ff 50%, #7c3aed 100%);
      -webkit-background-clip: text;
      background-clip: text;
      -webkit-text-fill-color: transparent;
      filter: drop-shadow(0 0 8px rgba(0, 198, 255, 0.5));
      transition: filter var(--transition), transform var(--transition);
      display: inline-block;
    }

    .dh-logo:hover {
      filter: drop-shadow(0 0 16px rgba(0, 198, 255, 0.9));
      transform: scale(1.05);
    }

    /* ==========================================================
       NAVBAR
       ========================================================== */
    .navbar {
      position: sticky;
      top: 0;
      z-index: 1000;
      display: flex;
      align-items: center;
      gap: 24px;
      padding: 14px 32px;
      background: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--border-color);
      transition: background var(--transition);
    }

    body.dark .navbar { background: rgba(15, 20, 32, 0.85); }

    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 22px;
      font-weight: 800;
    }

    .logo .club-text {
      font-family: 'Orbitron', sans-serif;
      font-weight: 700;
      font-size: 18px;
      color: var(--text-primary);
      letter-spacing: 1px;
    }

    .logo .club-text span {
      color: var(--accent-color);
    }

    .nav-links {
      display: flex;
      gap: 28px;
      list-style: none;
      margin-left: auto;
    }

    .nav-links a {
      font-weight: 500;
      font-size: 15px;
      color: var(--text-secondary);
      transition: color var(--transition);
    }

    .nav-links a:hover { color: var(--accent-color); }

    .nav-actions {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .lang-switch { display: flex; gap: 6px; }

    .lang-btn {
      background: transparent;
      border: 1px solid var(--border-color);
      color: var(--text-primary);
      padding: 6px 10px;
      border-radius: 8px;
      cursor: pointer;
      font-size: 13px;
      font-family: inherit;
      transition: all var(--transition);
    }

    .lang-btn:hover { border-color: var(--accent-color); }

    .lang-btn.active {
      background: var(--accent-color);
      color: #fff;
      border-color: var(--accent-color);
    }

    .icon-btn {
      background: transparent;
      border: 1px solid var(--border-color);
      color: var(--text-primary);
      width: 38px;
      height: 38px;
      border-radius: 10px;
      cursor: pointer;
      font-size: 16px;
      display: grid;
      place-items: center;
      transition: all var(--transition);
    }

    .icon-btn:hover {
      border-color: var(--accent-color);
      color: var(--accent-color);
    }

    .burger { display: none; }

    /* ==========================================================
       HERO
       ========================================================== */
    .hero {
      padding: 100px 24px 80px;
      text-align: center;
      background: radial-gradient(circle at 50% 0%, var(--bg-accent) 0%, var(--bg-primary) 60%);
      transition: background var(--transition);
    }

    .hero-content { max-width: 780px; margin: 0 auto; }

    .hero-badge, .section-badge {
      display: inline-block;
      font-size: 13px;
      font-weight: 600;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: var(--accent-color);
      background: rgba(79, 140, 255, 0.1);
      padding: 6px 14px;
      border-radius: 999px;
      margin-bottom: 20px;
    }

    .hero h1 {
      font-family: 'Orbitron', sans-serif;
      font-size: clamp(42px, 8vw, 84px);
      font-weight: 900;
      letter-spacing: -1px;
      line-height: 1.1;
      margin-bottom: 20px;
      background: linear-gradient(135deg, #00c6ff, #0072ff, #7c3aed);
      -webkit-background-clip: text;
      background-clip: text;
      -webkit-text-fill-color: transparent;
      filter: drop-shadow(0 0 20px rgba(0, 198, 255, 0.3));
    }

    .hero-subtitle {
      font-size: 18px;
      color: var(--text-secondary);
      max-width: 640px;
      margin: 0 auto 32px;
    }

    .hero-buttons {
      display: flex;
      gap: 14px;
      justify-content: center;
      flex-wrap: wrap;
    }

    /* ==========================================================
       BOUTONS
       ========================================================== */
    .btn {
      display: inline-block;
      padding: 12px 26px;
      border-radius: 12px;
      font-weight: 600;
      font-size: 15px;
      font-family: inherit;
      cursor: pointer;
      border: 2px solid transparent;
      transition: all var(--transition);
    }

    .btn-primary {
      background: var(--accent-color);
      color: #fff;
      box-shadow: var(--shadow-lg);
    }

    .btn-primary:hover {
      background: var(--accent-hover);
      transform: translateY(-2px);
    }

    .btn-outline {
      background: transparent;
      color: var(--text-primary);
      border-color: var(--border-color);
    }

    .btn-outline:hover {
      border-color: var(--accent-color);
      color: var(--accent-color);
    }

    /* ==========================================================
       SECTIONS & CARTES
       ========================================================== */
    .section {
      padding: 80px 24px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .section-alt {
      max-width: 100%;
      background: var(--bg-accent);
    }

    .section-alt > * {
      max-width: 1200px;
      margin-left: auto;
      margin-right: auto;
    }

    .section-header {
      text-align: center;
      margin-bottom: 50px;
    }

    .section-header h2 {
      font-size: clamp(28px, 4vw, 44px);
      font-weight: 800;
      letter-spacing: -1px;
      margin-bottom: 14px;
    }

    .section-desc {
      color: var(--text-secondary);
      max-width: 580px;
      margin: 0 auto;
    }

    .grid { display: grid; gap: 24px; }
    .grid-3 { grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); }

    .card {
      background: var(--bg-secondary);
      border: 1px solid var(--border-color);
      border-radius: var(--radius);
      padding: 32px 26px;
      box-shadow: var(--shadow);
      transition: transform var(--transition), box-shadow var(--transition), border-color var(--transition);
    }

    .card:hover {
      transform: translateY(-6px);
      box-shadow: var(--shadow-lg);
      border-color: var(--accent-color);
    }

    .card-icon { font-size: 36px; margin-bottom: 16px; }
    .card h3 { font-size: 19px; font-weight: 700; margin-bottom: 10px; }
    .card p { color: var(--text-secondary); font-size: 15px; }

    .pole-card { position: relative; }

    .pole-tag {
      display: inline-block;
      font-size: 12px;
      font-weight: 600;
      letter-spacing: 1px;
      text-transform: uppercase;
      color: var(--accent-color);
      background: rgba(79, 140, 255, 0.1);
      padding: 4px 12px;
      border-radius: 999px;
      margin-bottom: 14px;
    }

    /* ==========================================================
       FORMULAIRE
       ========================================================== */
    .contact-form {
      max-width: 640px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      gap: 16px;
      background: var(--bg-secondary);
      padding: 32px;
      border-radius: var(--radius);
      border: 1px solid var(--border-color);
      box-shadow: var(--shadow);
    }

    .form-row {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
    }

    .contact-form input,
    .contact-form textarea {
      font-family: inherit;
      font-size: 15px;
      padding: 12px 16px;
      border-radius: 10px;
      border: 1px solid var(--border-color);
      background: var(--bg-primary);
      color: var(--text-primary);
      transition: border-color var(--transition);
      resize: vertical;
    }

    .contact-form input:focus,
    .contact-form textarea:focus {
      outline: none;
      border-color: var(--accent-color);
    }

    .contact-form .btn { align-self: flex-start; }

    .success-message {
      display: none;
      max-width: 640px;
      margin: 24px auto 0;
      text-align: center;
      background: rgba(34, 197, 94, 0.1);
      border: 1px solid rgba(34, 197, 94, 0.4);
      color: #15803d;
      padding: 24px;
      border-radius: var(--radius);
    }

    body.dark .success-message { color: #4ade80; }

    .success-message.show {
      display: block;
      animation: fadeIn 0.4s ease;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    /* ==========================================================
       FOOTER OFFICIEL
       ========================================================== */
    .footer {
      background: var(--bg-secondary);
      border-top: 1px solid var(--border-color);
      padding: 60px 24px 0;
      margin-top: 40px;
      transition: background var(--transition);
    }

    .footer-container {
      max-width: 1200px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: 2fr 1fr 1fr 1.3fr;
      gap: 40px;
      padding-bottom: 50px;
    }

    .footer-col h4 {
      font-size: 15px;
      font-weight: 700;
      margin-bottom: 18px;
      color: var(--text-primary);
      letter-spacing: 0.3px;
    }

    .footer-col ul {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    .footer-col ul a {
      color: var(--text-secondary);
      font-size: 14px;
      transition: color var(--transition);
    }

    .footer-col ul a:hover { color: var(--accent-color); }

    .footer-brand .dh-logo-footer {
      font-family: 'Orbitron', sans-serif;
      font-weight: 900;
      font-size: 48px;
      letter-spacing: 3px;
      background: linear-gradient(135deg, #00c6ff 0%, #0072ff 50%, #7c3aed 100%);
      -webkit-background-clip: text;
      background-clip: text;
      -webkit-text-fill-color: transparent;
      filter: drop-shadow(0 0 10px rgba(0, 198, 255, 0.5));
      margin-bottom: 18px;
      display: inline-block;
    }

    .footer-desc {
      color: var(--text-secondary);
      font-size: 14px;
      line-height: 1.7;
      max-width: 340px;
    }

    .footer-socials {
      display: flex;
      flex-direction: column;
      gap: 10px;
      margin-bottom: 20px;
    }

    .social-btn {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 10px 14px;
      border-radius: 10px;
      background: var(--bg-primary);
      border: 1px solid var(--border-color);
      color: var(--text-primary);
      font-size: 14px;
      font-weight: 500;
      transition: all var(--transition);
      width: fit-content;
    }

    .social-btn:hover {
      border-color: var(--accent-color);
      color: var(--accent-color);
      transform: translateY(-2px);
    }

    .social-btn.instagram:hover {
      background: linear-gradient(45deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888);
      color: #fff;
      border-color: transparent;
    }

    .footer-cta {
      display: inline-block;
      font-weight: 600;
      font-size: 14px;
      color: var(--accent-color);
      transition: transform var(--transition);
    }

    .footer-cta:hover { transform: translateX(4px); }

    .footer-bottom {
      border-top: 1px solid var(--border-color);
      max-width: 1200px;
      margin: 0 auto;
      padding: 22px 0;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 10px;
      font-size: 13px;
      color: var(--text-secondary);
    }

    .footer-bottom strong { color: var(--accent-color); font-weight: 700; }

    /* ==========================================================
       RESPONSIVE
       ========================================================== */
    @media (max-width: 900px) {
      .footer-container { grid-template-columns: 1fr 1fr; }
    }

    @media (max-width: 820px) {
      .navbar { padding: 12px 18px; gap: 10px; }

      .nav-links {
        position: absolute;
        top: 100%;
        left: 0;
        right: 0;
        flex-direction: column;
        gap: 0;
        background: var(--bg-secondary);
        border-bottom: 1px solid var(--border-color);
        padding: 0;
        max-height: 0;
        overflow: hidden;
        transition: max-height var(--transition);
      }

      .nav-links.open { max-height: 320px; }

      .nav-links li {
        padding: 14px 22px;
        border-top: 1px solid var(--border-color);
      }

      .burger { display: grid; }
      .form-row { grid-template-columns: 1fr; }
      .hero { padding: 70px 20px 60px; }
      .section { padding: 60px 20px; }
    }

    @media (max-width: 560px) {
      .footer-container {
        grid-template-columns: 1fr;
        gap: 32px;
        padding-bottom: 36px;
      }
      .footer-bottom { flex-direction: column; text-align: center; }
      .dh-logo { font-size: 26px; }
      .logo .club-text { font-size: 15px; }
      .lang-btn { padding: 5px 8px; font-size: 12px; }
      .hero-buttons .btn { width: 100%; }
    }
  </style>
</head>
<body>

  <!-- ========== NAVBAR ========== -->
  <nav class="navbar">
    <a href="#" class="logo">
      <span class="dh-logo">DH</span>
      <span class="club-text">CLUB<span>.</span></span>
    </a>

    <ul class="nav-links" id="navLinks">
      <li><a href="#hero" data-i18n="nav.home">Accueil</a></li>
      <li><a href="#skills" data-i18n="nav.skills">Compétences</a></li>
      <li><a href="#poles" data-i18n="nav.poles">Nos pôles</a></li>
      <li><a href="#contact" data-i18n="nav.contact">Contact</a></li>
    </ul>

    <div class="nav-actions">
      <div class="lang-switch">
        <button id="lang-fr" class="lang-btn active" onclick="setLang('fr')">🇫🇷 FR</button>
        <button id="lang-en" class="lang-btn" onclick="setLang('en')">🇬🇧 EN</button>
      </div>
      <button id="theme-toggle" class="icon-btn" onclick="toggleTheme()" aria-label="Changer de thème">🌙</button>
      <button class="icon-btn burger" onclick="toggleMenu()" aria-label="Menu">☰</button>
    </div>
  </nav>

  <!-- ========== HERO ========== -->
  <header id="hero" class="hero">
    <div class="hero-content">
      <p class="hero-badge">⚡ <span data-i18n="hero.badge">INTRODUCTION</span></p>
      <h1 data-i18n="hero.title">DH CLUB</h1>
      <p class="hero-subtitle" data-i18n="hero.subtitle">
        Bienvenue au club informatique et digital Digital Hub Club. Notre plateforme rassemble les esprits passionnés par l'innovation, la création visuelle et le développement moderne pour construire le monde numérique de demain.
      </p>
      <div class="hero-buttons">
        <a href="#contact" class="btn btn-primary" data-i18n="hero.cta1">Rejoindre le club</a>
        <a href="#skills" class="btn btn-outline" data-i18n="hero.cta2">Découvrir nos pôles</a>
      </div>
    </div>
  </header>

  <!-- ========== COMPÉTENCES ========== -->
  <section id="skills" class="section">
    <div class="section-header">
      <p class="section-badge">📊 <span data-i18n="skills.badge">Compétences</span></p>
      <h2 data-i18n="skills.title">Notre savoir-faire</h2>
    </div>

    <div class="grid grid-3">
      <article class="card">
        <div class="card-icon">💻</div>
        <h3 data-i18n="skills.1.title">Programmation</h3>
        <p data-i18n="skills.1.desc">Maîtrise des langages et technologies fondamentales du web et du développement logiciel.</p>
      </article>
      <article class="card">
        <div class="card-icon">🎨</div>
        <h3 data-i18n="skills.2.title">Design Graphique</h3>
        <p data-i18n="skills.2.desc">Création visuelle percutante, logos, affiches et identités visuelles sur-mesure.</p>
      </article>
      <article class="card">
        <div class="card-icon">🌐</div>
        <h3 data-i18n="skills.3.title">3D et Animation</h3>
        <p data-i18n="skills.3.desc">Modélisation d'espaces 3D, création d'environnements et animations immersives.</p>
      </article>
      <article class="card">
        <div class="card-icon">📊</div>
        <h3 data-i18n="skills.4.title">Gestion de projets</h3>
        <p data-i18n="skills.4.desc">Planification stratégique, organisation des tâches et gestion d'équipe collaborative.</p>
      </article>
      <article class="card">
        <div class="card-icon">🏛️</div>
        <h3 data-i18n="skills.5.title">Histoire de l'art</h3>
        <p data-i18n="skills.5.desc">Étude approfondie des courants artistiques, esthétiques visuelles et culture artistique.</p>
      </article>
    </div>
  </section>

  <!-- ========== PÔLES ========== -->
  <section id="poles" class="section section-alt">
    <div class="section-header">
      <p class="section-badge">🎓 <span data-i18n="poles.badge">NOS PÔLES</span></p>
      <h2 data-i18n="poles.title">Nos différents groupes</h2>
    </div>

    <div class="grid grid-3">
      <article class="card pole-card">
        <span class="pole-tag" data-i18n="poles.1.tag">Pôle Programmation</span>
        <h3 data-i18n="poles.1.title">Développement Web</h3>
        <p data-i18n="poles.1.desc">Création de sites web fluides et rapides, dotés d'interfaces UI/UX uniques.</p>
      </article>
      <article class="card pole-card">
        <span class="pole-tag" data-i18n="poles.2.tag">Pôle Design</span>
        <h3 data-i18n="poles.2.title">Création 2D</h3>
        <p data-i18n="poles.2.desc">Conception graphique de cartes de visite, logos, identités visuelles, etc.</p>
      </article>
      <article class="card pole-card">
        <span class="pole-tag" data-i18n="poles.3.tag">Pôle Graphisme 3D</span>
        <h3 data-i18n="poles.3.title">Modélisation Blender</h3>
        <p data-i18n="poles.3.desc">Création de décors et d'architectures (maisons, paysages futuristes, intérieurs design).</p>
      </article>
    </div>
  </section>

  <!-- ========== CONTACT ========== -->
  <section id="contact" class="section">
    <div class="section-header">
      <p class="section-badge">📬 <span data-i18n="contact.badge">CONTACT</span></p>
      <h2 data-i18n="contact.title">Démarrer un projet avec notre club</h2>
      <p class="section-desc" data-i18n="contact.desc">
        Remplissez le formulaire ci-dessous pour nous envoyer votre message ou demande d'adhésion.
      </p>
    </div>

    <form class="contact-form" id="contactForm" onsubmit="handleSubmit(event)">
      <div class="form-row">
        <input type="text" name="name" data-i18n-placeholder="contact.name" placeholder="Votre nom" required />
        <input type="email" name="email" data-i18n-placeholder="contact.email" placeholder="Votre email" required />
      </div>
      <textarea name="message" rows="5" data-i18n-placeholder="contact.message" placeholder="Votre message..." required></textarea>
      <button type="submit" class="btn btn-primary" data-i18n="contact.send">Envoyer le message</button>
    </form>

    <div class="success-message" id="successMessage">
      <h3 data-i18n="contact.success.title">Message envoyé !</h3>
      <p data-i18n="contact.success.desc">Merci de nous avoir contactés. Nous vous répondrons sous peu.</p>
    </div>
  </section>

  <!-- ========== FOOTER OFFICIEL 2026 ========== -->
  <footer class="footer">
    <div class="footer-container">
      <!-- Colonne 1 -->
      <div class="footer-col footer-brand">
        <a href="#" class="dh-logo-footer">DH CLUB</a>
        <p class="footer-desc" data-i18n="footer.desc">
          Digital Hub Club — le club informatique et digital qui rassemble les esprits passionnés par l'innovation, la création visuelle et le développement moderne.
        </p>
      </div>

      <!-- Colonne 2 -->
      <div class="footer-col">
        <h4 data-i18n="footer.nav">Navigation</h4>
        <ul>
          <li><a href="#hero" data-i18n="nav.home">Accueil</a></li>
          <li><a href="#skills" data-i18n="nav.skills">Compétences</a></li>
          <li><a href="#poles" data-i18n="nav.poles">Nos pôles</a></li>
          <li><a href="#contact" data-i18n="nav.contact">Contact</a></li>
        </ul>
      </div>

      <!-- Colonne 3 -->
      <div class="footer-col">
        <h4 data-i18n="footer.poles">Nos pôles</h4>
        <ul>
          <li><a href="#poles" data-i18n="poles.1.title">Développement Web</a></li>
          <li><a href="#poles" data-i18n="poles.2.title">Création 2D</a></li>
          <li><a href="#poles" data-i18n="poles.3.title">Modélisation Blender</a></li>
        </ul>
      </div>

      <!-- Colonne 4 -->
      <div class="footer-col">
        <h4 data-i18n="footer.follow">Suivez-nous</h4>
        <div class="footer-socials">
          <a href="https://www.instagram.com/digital_hub.ac?srtk=MTc0YzlhYnJvenlwNg==" 
             target="_blank" rel="noopener" 
             aria-label="Instagram Digital Hub Club"
             class="social-btn instagram">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="2" y="2" width="20" height="20" rx="5" ry="5"></rect>
              <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"></path>
              <line x1="17.5" y1="6.5" x2="17.51" y2="6.5"></line>
            </svg>
            <span>@digital_hub.ac</span>
          </a>
        </div>
        <a href="#contact" class="footer-cta" data-i18n="footer.cta">Rejoindre le club →</a>
      </div>
    </div>

    <div class="footer-bottom">
      <p>© 2026 <strong>Digital Hub Club</strong> — <span data-i18n="footer.rights">Tous droits réservés.</span></p>
      <p class="footer-made" data-i18n="footer.made">Fait avec ❤️ par DH CLUB</p>
    </div>
  </footer>

  <!-- ========== JAVASCRIPT ========== -->
  <script>
    const translations = {
      fr: {
        "nav.home": "Accueil",
        "nav.skills": "Compétences",
        "nav.poles": "Nos pôles",
        "nav.contact": "Contact",
        "hero.badge": "INTRODUCTION",
        "hero.title": "DH CLUB",
        "hero.subtitle": "Bienvenue au club informatique et digital Digital Hub Club. Notre plateforme rassemble les esprits passionnés par l'innovation, la création visuelle et le développement moderne pour construire le monde numérique de demain.",
        "hero.cta1": "Rejoindre le club",
        "hero.cta2": "Découvrir nos pôles",
        "skills.badge": "Compétences",
        "skills.title": "Notre savoir-faire",
        "skills.1.title": "Programmation",
        "skills.1.desc": "Maîtrise des langages et technologies fondamentales du web et du développement logiciel.",
        "skills.2.title": "Design Graphique",
        "skills.2.desc": "Création visuelle percutante, logos, affiches et identités visuelles sur-mesure.",
        "skills.3.title": "3D et Animation",
        "skills.3.desc": "Modélisation d'espaces 3D, création d'environnements et animations immersives.",
        "skills.4.title": "Gestion de projets",
        "skills.4.desc": "Planification stratégique, organisation des tâches et gestion d'équipe collaborative.",
        "skills.5.title": "Histoire de l'art",
        "skills.5.desc": "Étude approfondie des courants artistiques, esthétiques visuelles et culture artistique.",
        "poles.badge": "NOS PÔLES",
        "poles.title": "Nos différents groupes",
        "poles.1.tag": "Pôle Programmation",
        "poles.1.title": "Développement Web",
        "poles.1.desc": "Création de sites web fluides et rapides, dotés d'interfaces UI/UX uniques.",
        "poles.2.tag": "Pôle Design",
        "poles.2.title": "Création 2D",
        "poles.2.desc": "Conception graphique de cartes de visite, logos, identités visuelles, etc.",
        "poles.3.tag": "Pôle Graphisme 3D",
        "poles.3.title": "Modélisation Blender",
        "poles.3.desc": "Création de décors et d'architectures (maisons, paysages futuristes, intérieurs design).",
        "contact.badge": "CONTACT",
        "contact.title": "Démarrer un projet avec notre club",
        "contact.desc": "Remplissez le formulaire ci-dessous pour nous envoyer votre message ou demande d'adhésion.",
        "contact.name": "Votre nom",
        "contact.email": "Votre email",
        "contact.message": "Votre message...",
        "contact.send": "Envoyer le message",
        "contact.success.title": "Message envoyé !",
        "contact.success.desc": "Merci de nous avoir contactés. Nous vous répondrons sous peu.",
        "footer.desc": "Digital Hub Club — le club informatique et digital qui rassemble les esprits passionnés par l'innovation, la création visuelle et le développement moderne.",
        "footer.nav": "Navigation",
        "footer.poles": "Nos pôles",
        "footer.follow": "Suivez-nous",
        "footer.cta": "Rejoindre le club →",
        "footer.rights": "Tous droits réservés.",
        "footer.made": "Fait avec ❤️ par DH CLUB"
      },
      en: {
        "nav.home": "Home",
        "nav.skills": "Skills",
        "nav.poles": "Our poles",
        "nav.contact": "Contact",
        "hero.badge": "INTRODUCTION",
        "hero.title": "DH CLUB",
        "hero.subtitle": "Welcome to Digital Hub Club, the IT and digital club. Our platform brings together minds passionate about innovation, visual creation and modern development to build tomorrow's digital world.",
        "hero.cta1": "Join the club",
        "hero.cta2": "Discover our poles",
        "skills.badge": "Skills",
        "skills.title": "Our expertise",
        "skills.1.title": "Programming",
        "skills.1.desc": "Mastery of the fundamental languages and technologies of web and software development.",
        "skills.2.title": "Graphic Design",
        "skills.2.desc": "Striking visual creation, logos, posters and tailor-made visual identities.",
        "skills.3.title": "3D & Animation",
        "skills.3.desc": "3D space modeling, environment creation and immersive animations.",
        "skills.4.title": "Project Management",
        "skills.4.desc": "Strategic planning, task organization and collaborative team management.",
        "skills.5.title": "Art History",
        "skills.5.desc": "In-depth study of artistic movements, visual aesthetics and artistic culture.",
        "poles.badge": "OUR POLES",
        "poles.title": "Our different groups",
        "poles.1.tag": "Programming Pole",
        "poles.1.title": "Web Development",
        "poles.1.desc": "Creation of fluid and fast websites with unique UI/UX interfaces.",
        "poles.2.tag": "Design Pole",
        "poles.2.title": "2D Creation",
        "poles.2.desc": "Graphic design of business cards, logos, visual identities, etc.",
        "poles.3.tag": "3D Graphics Pole",
        "poles.3.title": "Blender Modeling",
        "poles.3.desc": "Creation of sets and architectures (houses, futuristic landscapes, design interiors).",
        "contact.badge": "CONTACT",
        "contact.title": "Start a project with our club",
        "contact.desc": "Fill in the form below to send us your message or membership request.",
        "contact.name": "Your name",
        "contact.email": "Your email",
        "contact.message": "Your message...",
        "contact.send": "Send message",
        "contact.success.title": "Message sent!",
        "contact.success.desc": "Thank you for contacting us. We will get back to you shortly.",
        "footer.desc": "Digital Hub Club — the IT and digital club that brings together minds passionate about innovation, visual creation and modern development.",
        "footer.nav": "Navigation",
        "footer.poles": "Our poles",
        "footer.follow": "Follow us",
        "footer.cta": "Join the club →",
        "footer.rights": "All rights reserved.",
        "footer.made": "Made with ❤️ by DH CLUB"
      }
    };

    function setLang(lang) {
      localStorage.setItem('lang', lang);
      document.querySelectorAll('[data-i18n]').forEach(el => {
        const key = el.getAttribute('data-i18n');
        if (translations[lang] && translations[lang][key]) {
          el.textContent = translations[lang][key];
        }
      });
      document.querySelectorAll('[data-i18n-placeholder]').forEach(el => {
        const key = el.getAttribute('data-i18n-placeholder');
        if (translations[lang] && translations[lang][key]) {
          el.setAttribute('placeholder', translations[lang][key]);
        }
      });
      document.querySelectorAll('.lang-btn').forEach(b => b.classList.remove('active'));
      const activeBtn = document.getElementById(`lang-${lang}`);
      if (activeBtn) activeBtn.classList.add('active');
      document.documentElement.lang = lang;
    }

    function toggleTheme() {
      document.body.classList.toggle('dark');
      const isDark = document.body.classList.contains('dark');
      localStorage.setItem('theme', isDark ? 'dark' : 'light');
      updateThemeIcon();
    }

    function updateThemeIcon() {
      const btn = document.getElementById('theme-toggle');
      if (!btn) return;
      btn.textContent = document.body.classList.contains('dark') ? '☀️' : '🌙';
    }

    function toggleMenu() {
      document.getElementById('navLinks').classList.toggle('open');
    }

    document.querySelectorAll('.nav-links a').forEach(link => {
      link.addEventListener('click', () => {
        document.getElementById('navLinks').classList.remove('open');
      });
    });

    function handleSubmit(event) {
      event.preventDefault();
      const form = event.target;
      const success = document.getElementById('successMessage');
      form.reset();
      success.classList.add('show');
      setTimeout(() => success.classList.remove('show'), 6000);
    }

    window.addEventListener('DOMContentLoaded', () => {
      const savedLang = localStorage.getItem('lang') || 'fr';
      setLang(savedLang);
      if (localStorage.getItem('theme') === 'dark') {
        document.body.classList.add('dark');
      }
      updateThemeIcon();
    });
  </script>
</body>
</html>
