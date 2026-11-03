<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, viewport-fit=cover">
  <title>DH CLUB - Digital Hub Club</title>

  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Plus Jakarta Sans', Arial, sans-serif;
      background: #080d1a;
      color: white;
      min-height: 100vh;
      overflow-x: hidden;
      position: relative;
    }

    /* BACKGROUND LOGO FLOU BACKGROUND */
    .bg-logo-layer {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      z-index: 0;
      pointer-events: none;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .bg-logo-layer img {
      width: clamp(320px, 60vw, 750px);
      height: auto;
      opacity: 0.18;
      filter: blur(28px);
      transform: scale(1.1);
    }

    /* NAVBAR */
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 18px 8%;
      background: rgba(15, 23, 42, 0.75);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      border-bottom: 1px solid rgba(56, 189, 248, 0.15);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .logo {
      font-size: 22px;
      font-weight: 800;
      color: #38bdf8;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    nav ul {
      display: flex;
      gap: 24px;
      list-style: none;
    }

    nav a {
      color: #e2e8f0;
      text-decoration: none;
      font-size: 15px;
      font-weight: 500;
      transition: 0.3s;
    }

    nav a:hover {
      color: #38bdf8;
      text-shadow: 0 0 10px rgba(56, 189, 248, 0.5);
    }

    /* INTRO HERO */
    #intro {
      position: relative;
      z-index: 1;
      text-align: center;
      padding: clamp(80px, 15vh, 140px) 20px;
    }

    #intro h1 {
      font-size: clamp(40px, 7vw, 68px);
      font-weight: 800;
      margin-bottom: 20px;
      letter-spacing: -1px;
    }

    #intro span {
      color: #38bdf8;
      text-shadow: 0 0 25px rgba(56, 189, 248, 0.4);
    }

    #intro p {
      color: #94a3b8;
      font-size: clamp(16px, 2vw, 20px);
      margin-bottom: 35px;
      max-width: 600px;
      margin-left: auto;
      margin-right: auto;
    }

    .btn {
      display: inline-block;
      background: linear-gradient(135deg, #38bdf8, #0284c7);
      color: #080d1a;
      padding: 14px 32px;
      border-radius: 12px;
      text-decoration: none;
      font-weight: 700;
      box-shadow: 0 6px 20px rgba(56, 189, 248, 0.3);
      transition: 0.3s ease;
    }

    .btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 28px rgba(56, 189, 248, 0.5);
    }

    /* SECTIONS */
    section {
      position: relative;
      z-index: 1;
      padding: clamp(50px, 8vw, 80px) 8%;
    }

    h2 {
      text-align: center;
      margin-bottom: 45px;
      color: #38bdf8;
      font-size: clamp(24px, 4vw, 32px);
      font-weight: 700;
    }

    /* CARDS GRID */
    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 22px;
    }

    .card {
      background: rgba(15, 23, 42, 0.65);
      backdrop-filter: blur(14px);
      -webkit-backdrop-filter: blur(14px);
      padding: 30px 24px;
      border-radius: 18px;
      border: 1px solid rgba(56, 189, 248, 0.15);
      transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    }

    .card:hover {
      transform: translateY(-6px);
      border-color: #38bdf8;
      box-shadow: 0 12px 30px rgba(56, 189, 248, 0.2);
    }

    .card h3 {
      margin-bottom: 12px;
      font-size: 19px;
    }

    .card p {
      color: #94a3b8;
      line-height: 1.65;
      font-size: 14.5px;
    }

    /* CONTACT FORM */
    form {
      max-width: 580px;
      margin: auto;
      background: rgba(15, 23, 42, 0.6);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      padding: 30px;
      border-radius: 20px;
      border: 1px solid rgba(56, 189, 248, 0.15);
    }

    input, textarea {
      width: 100%;
      padding: 15px 18px;
      margin-bottom: 18px;
      background: rgba(8, 13, 26, 0.7);
      border: 1px solid #334155;
      border-radius: 12px;
      color: white;
      font-size: 15px;
      outline: none;
      transition: 0.3s;
    }

    input:focus, textarea:focus {
      border-color: #38bdf8;
      box-shadow: 0 0 15px rgba(56, 189, 248, 0.2);
    }

    textarea {
      height: 130px;
      resize: vertical;
    }

    button {
      width: 100%;
      padding: 15px;
      background: linear-gradient(135deg, #38bdf8, #0ea5e9);
      color: #080d1a;
      border: none;
      border-radius: 12px;
      font-weight: 700;
      font-size: 16px;
      cursor: pointer;
      transition: 0.3s;
      box-shadow: 0 4px 18px rgba(56, 189, 248, 0.3);
    }

    button:hover {
      transform: translateY(-2px);
      box-shadow: 0 8px 25px rgba(56, 189, 248, 0.5);
    }

    #message {
      text-align: center;
      margin-top: 20px;
      font-weight: 600;
      color: #38bdf8;
    }

    /* FOOTER CLEANED */
    footer {
      position: relative;
      z-index: 1;
      text-align: center;
      padding: 30px 20px;
      color: #94a3b8;
      background: rgba(15, 23, 42, 0.85);
      border-top: 1px solid rgba(56, 189, 248, 0.1);
      font-size: 14px;
    }

    /* RESPONSIVE DESIGN (IPHONE, ANDROID & PC) */
    @media (max-width: 680px) {
      nav {
        flex-direction: column;
        gap: 16px;
        padding: 16px;
      }

      nav ul {
        gap: 16px;
        flex-wrap: wrap;
        justify-content: center;
      }

      #intro {
        padding: 60px 16px;
      }

      form {
        padding: 20px;
      }
    }
  </style>
</head>

<body>

  <!-- BACKGROUND LOGO FLOU -->
  <div class="bg-logo-layer">
    <img src="https://i.ibb.co/6y4nJpx/dh-logo.jpg" alt="DH HUB Logo">
  </div>

  <!-- NAVBAR -->
  <nav>
    <div class="logo">⚡ DH CLUB</div>
    <ul>
      <li><a href="#intro">Intro</a></li>
      <li><a href="#specialites">Spécialités</a></li>
      <li><a href="#projets">Projets</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- INTRO -->
  <section id="intro">
    <h1>Digital <span>Hub</span></h1>
    <p>Créativité, technologie et innovation. Bienvenue dans notre communauté.</p>
    <a href="#specialites" class="btn">Découvrir</a>
  </section>

  <!-- SPECIALITES -->
  <section id="specialites">
    <h2>Nos spécialités</h2>
    <div class="cards">
      <div class="card">
        <h3>💻 Programmation</h3>
        <p>HTML, CSS, JavaScript et création de sites web.</p>
      </div>

      <div class="card">
        <h3>🎨 Design graphique</h3>
        <p>Création de logos, affiches et identités visuelles.</p>
      </div>

      <div class="card">
        <h3>🌐 3D et Animation</h3>
        <p>Modélisation 3D et création avec Blender.</p>
      </div>

      <div class="card">
        <h3>📊 Gestion de projets</h3>
        <p>Planification, organisation et gestion efficace des projets digitaux.</p>
      </div>

      <div class="card">
        <h3>🖼️ Histoire de l'art</h3>
        <p>Étude des courants artistiques, esthétique et inspiration visuelle.</p>
      </div>
    </div>
  </section>

  <!-- PROJETS -->
  <section id="projets">
    <h2>Nos projets</h2>
    <div class="cards">
      <div class="card">
        <h3>Développement Web</h3>
        <p>Création de sites web modernes.</p>
      </div>

      <div class="card">
        <h3>Création graphique</h3>
        <p>Logos, affiches et design.</p>
      </div>

      <div class="card">
        <h3>Modélisation 3D</h3>
        <p>Création de modèles et environnements 3D.</p>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <h2>Contactez-nous</h2>
    <form id="contactForm">
      <input type="text" name="name" placeholder="Votre nom" required>
      <input type="email" name="email" placeholder="Votre email" required>
      <textarea name="message" placeholder="Votre message" required></textarea>
      <button type="submit">Envoyer le message</button>
    </form>
    <p id="message"></p>
  </section>

  <!-- FOOTER CLEAN -->
  <footer>
    © 2026 Digital Hub Club — Tous droits réservés.
  </footer>

  <script>
    const form = document.getElementById("contactForm");
    const message = document.getElementById("message");

    form.addEventListener("submit", async function(e) {
      e.preventDefault();
      message.textContent = "Envoi en cours...";
      const data = new FormData(form);

      try {
        const response = await fetch("https://formspree.io/f/xeewnkek", {
          method: "POST",
          body: data,
          headers: {
            Accept: "application/json"
          }
        });

        if (response.ok) {
          message.textContent = "Message envoyé avec succès !";
          form.reset();
        } else {
          message.textContent = "Erreur lors de l'envoi.";
        }
      } catch (error) {
        message.textContent = "Erreur de connexion.";
      }
    });
  </script>
</body>
</html>
