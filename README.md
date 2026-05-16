<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Lottus Depi&Spa by FER. — Centro de Estética y Bienestar</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Jost:wght@300;400;500;600&display=swap" rel="stylesheet">
  <style>
    :root {
      --ivory:    #d0e6cb;
      --cream:    #d2f3cc;
      --sand:     #C8B89A;
      --forest:   #178a63;
      --moss:     #2C5F43;
      --sage:     #4A7C5E;
      --gold:     #C49A3C;
      --gold-lt:  #fced1e;
      --charcoal: #0a5042;
      --white:    #FFFFFF;
    }

    *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'Jost', sans-serif;
      background: var(--ivory);
      color: var(--charcoal);
      overflow-x: hidden;
    }

    /* ── HEADER ─────────────────────────────────── */
    header {
      background: var(--forest);
      padding: 0 40px;
      position: sticky;
      top: 0;
      z-index: 200;
      display: flex;
      align-items: center;
      justify-content: space-between;
      height: 80px;
      border-bottom: 1px solid rgba(196,154,60,0.3);
    }

    .logo-lockup {
      display: flex;
      align-items: center;
      gap: 16px;
    }

    .logo-lockup img {
      height: 48px;
      width: 48px;
      object-fit: cover;
      border-radius: 50%;
      border: 1.5px solid var(--gold);
    }

    .logo-wordmark {
      display: flex;
      flex-direction: column;
      line-height: 1;
    }

    .logo-wordmark .brand-name {
      font-family: 'Cormorant Garamond', serif;
      font-weight: 300;
      font-style: italic;
      font-size: 28px;
      color: var(--white);
      letter-spacing: 4px;
      text-transform: uppercase;
    }

    .logo-wordmark .brand-sub {
      font-family: 'Jost', sans-serif;
      font-weight: 300;
      font-size: 9px;
      letter-spacing: 5px;
      color: var(--gold-lt);
      text-transform: uppercase;
      margin-top: 4px;
    }

    .header-avatar {
      width: 46px;
      height: 46px;
      border-radius: 50%;
      object-fit: cover;
      border: 2px solid var(--gold);
    }

    /* ── NAV ─────────────────────────────────────── */
    nav {
      background: var(--charcoal);
      border-bottom: 1px solid rgba(196,154,60,0.2);
    }

    nav ul {
      display: flex;
      list-style: none;
      justify-content: center;
      gap: 0;
      flex-wrap: wrap;
      max-width: 1100px;
      margin: 0 auto;
    }

    nav a {
      display: block;
      color: rgba(255,255,255,0.6);
      text-decoration: none;
      font-family: 'Jost', sans-serif;
      font-weight: 400;
      font-size: 11px;
      letter-spacing: 3px;
      text-transform: uppercase;
      padding: 16px 22px;
      transition: color 0.25s;
      position: relative;
    }

    nav a::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 22px;
      right: 22px;
      height: 1px;
      background: var(--gold);
      transform: scaleX(0);
      transition: transform 0.25s;
    }

    nav a:hover { color: var(--gold-lt); }
    nav a:hover::after { transform: scaleX(1); }

    /* ── HERO ────────────────────────────────────── */
    .hero {
      background: var(--forest);
      min-height: 560px;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 80px 24px;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: '';
      position: absolute;
      inset: 0;
      background:
        radial-gradient(ellipse 60% 50% at 80% 20%, rgba(44,95,67,0.5) 0%, transparent 70%),
        radial-gradient(ellipse 40% 60% at 10% 80%, rgba(196,154,60,0.12) 0%, transparent 60%);
    }

    .hero-inner { position: relative; max-width: 720px; }

    .hero-eyebrow {
      font-family: 'Jost', sans-serif;
      font-weight: 300;
      font-size: 11px;
      letter-spacing: 6px;
      color: var(--gold-lt);
      text-transform: uppercase;
      margin-bottom: 24px;
    }

    .hero h1 {
      font-family: 'Cormorant Garamond', serif;
      font-weight: 300;
      font-style: italic;
      font-size: clamp(52px, 8vw, 88px);
      color: var(--white);
      line-height: 1.05;
      letter-spacing: 2px;
      margin-bottom: 28px;
    }

    .hero h1 em {
      font-style: normal;
      color: var(--gold-lt);
    }

    .hero-desc {
      font-family: 'Jost', sans-serif;
      font-weight: 300;
      font-size: 15px;
      letter-spacing: 1.5px;
      color: rgba(255,255,255,0.65);
      margin-bottom: 40px;
      text-transform: uppercase;
    }

    .hero-divider {
      width: 60px;
      height: 1px;
      background: var(--gold);
      margin: 0 auto 40px;
    }

    .btn-primary {
      display: inline-block;
      background: var(--gold);
      color: var(--forest);
      font-family: 'Jost', sans-serif;
      font-weight: 600;
      font-size: 11px;
      letter-spacing: 3px;
      text-transform: uppercase;
      text-decoration: none;
      padding: 16px 40px;
      border: none;
      cursor: pointer;
      transition: background 0.25s, transform 0.2s;
    }

    .btn-primary:hover { background: var(--gold-lt); transform: translateY(-2px); }

    .btn-outline {
      display: inline-block;
      background: transparent;
      color: var(--gold-lt);
      border: 1px solid var(--gold);
      font-family: 'Jost', sans-serif;
      font-weight: 400;
      font-size: 11px;
      letter-spacing: 3px;
      text-transform: uppercase;
      text-decoration: none;
      padding: 15px 40px;
      cursor: pointer;
      transition: background 0.25s, color 0.25s;
      margin-left: 16px;
    }

    .btn-outline:hover { background: var(--gold); color: var(--forest); }

    /* ── SECTION BASE ────────────────────────────── */
    .section {
      padding: 90px 24px;
      max-width: 1100px;
      margin: 0 auto;
    }

    .section-full {
      padding: 90px 24px;
    }

    .section-label {
      font-family: 'Jost', sans-serif;
      font-weight: 300;
      font-size: 10px;
      letter-spacing: 5px;
      text-transform: uppercase;
      color: var(--sage);
      margin-bottom: 12px;
      text-align: center;
    }

    .section-title {
      font-family: 'Cormorant Garamond', serif;
      font-weight: 300;
      font-style: italic;
      font-size: clamp(36px, 5vw, 56px);
      color: var(--forest);
      text-align: center;
      margin-bottom: 16px;
      letter-spacing: 1px;
    }

    .section-rule {
      width: 48px;
      height: 1px;
      background: var(--gold);
      margin: 0 auto 56px;
    }

    /* ── ABOUT ───────────────────────────────────── */
    #sobre { background: var(--ivory); }

    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 72px;
      align-items: center;
    }

    .about-img-wrap {
      position: relative;
    }

    .about-img-wrap img {
      width: 100%;
      height: 480px;
      object-fit: cover;
      display: block;
    }

    .about-img-wrap::after {
      content: '';
      position: absolute;
      bottom: -16px;
      right: -16px;
      width: 60%;
      height: 60%;
      border: 1px solid var(--gold);
      pointer-events: none;
    }

    .about-text .label {
      font-family: 'Jost', sans-serif;
      font-weight: 300;
      font-size: 10px;
      letter-spacing: 5px;
      text-transform: uppercase;
      color: var(--sage);
      margin-bottom: 16px;
    }

    .about-text h3 {
      font-family: 'Cormorant Garamond', serif;
      font-weight: 300;
      font-style: italic;
      font-size: 38px;
      color: var(--forest);
      line-height: 1.2;
      margin-bottom: 28px;
    }

    .about-text p {
      font-family: 'Jost', sans-serif;
      font-weight: 300;
      font-size: 15px;
      color: #555;
      line-height: 1.9;
      margin-bottom: 16px;
    }

    /* ── SERVICIOS ───────────────────────────────── */
    #servicios { background: var(--charcoal); }

    #servicios .section-title { color: var(--white); }
    #servicios .section-label { color: var(--gold-lt); }

    .cards-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1px;
      background: rgba(255,255,255,0.06);
      border: 1px solid rgba(255,255,255,0.06);
    }

    .service-card {
      background: var(--charcoal);
      padding: 48px 36px;
      transition: background 0.3s;
      position: relative;
      overflow: hidden;
    }

    .service-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 2px;
      background: var(--gold);
      transform: scaleX(0);
      transition: transform 0.35s;
    }

    .service-card:hover { background: #232323; }
    .service-card:hover::before { transform: scaleX(1); }

    .service-number {
      font-family: 'Cormorant Garamond', serif;
      font-weight: 300;
      font-size: 60px;
      color: rgba(196,154,60,0.15);
      line-height: 1;
      margin-bottom: 20px;
    }

    .service-card h3 {
      font-family: 'Cormorant Garamond', serif;
      font-weight: 400;
      font-style: italic;
      font-size: 26px;
      color: var(--white);
      margin-bottom: 16px;
    }

    .service-card p {
      font-family: 'Jost', sans-serif;
      font-weight: 300;
      font-size: 14px;
      color: rgba(255,255,255,0.5);
      line-height: 1.8;
    }

    /* ── BENEFICIOS ──────────────────────────────── */
    #beneficios-wrap {
      background: var(--cream);
      padding: 72px 24px;
    }

    .beneficios-inner {
      max-width: 1100px;
      margin: 0 auto;
    }

    .ben-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 0;
      border: 1px solid var(--sand);
      margin-top: 48px;
    }

    .ben-item {
      padding: 36px 32px;
      border-right: 1px solid var(--sand);
      border-bottom: 1px solid var(--sand);
    }

    .ben-item:nth-child(3n) { border-right: none; }
    .ben-item:nth-child(n+4) { border-bottom: none; }

    .ben-check {
      font-family: 'Cormorant Garamond', serif;
      font-size: 22px;
      color: var(--gold);
      margin-bottom: 10px;
    }

    .ben-item p {
      font-family: 'Jost', sans-serif;
      font-weight: 400;
      font-size: 14px;
      color: var(--forest);
      line-height: 1.7;
    }

    /* ── PROMOS ──────────────────────────────────── */
    #promos { background: var(--ivory); }

    .promos-list { display: flex; flex-direction: column; gap: 2px; }

    .promo-row {
      display: grid;
      grid-template-columns: 80px 1fr auto;
      align-items: center;
      gap: 40px;
      background: var(--white);
      padding: 36px 40px;
      border-left: 3px solid transparent;
      transition: border-color 0.25s, background 0.25s;
      cursor: default;
    }

    .promo-row:hover { border-left-color: var(--gold); background: #fdfaf5; }

    .promo-num {
      font-family: 'Cormorant Garamond', serif;
      font-weight: 300;
      font-style: italic;
      font-size: 48px;
      color: var(--sand);
      line-height: 1;
    }

    .promo-body h3 {
      font-family: 'Cormorant Garamond', serif;
      font-weight: 400;
      font-size: 22px;
      color: var(--forest);
      margin-bottom: 6px;
    }

    .promo-body p {
      font-family: 'Jost', sans-serif;
      font-weight: 300;
      font-size: 14px;
      color: #777;
      line-height: 1.7;
    }

    .promo-tag {
      font-family: 'Jost', sans-serif;
      font-size: 10px;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: var(--gold);
      border: 1px solid var(--gold);
      padding: 6px 14px;
      white-space: nowrap;
    }

    /* ── TIENDA (old — keep for reference, new below) ── */

    /* ── CONTACTO ────────────────────────────────── */
    #contacto {
      background: var(--charcoal);
      padding: 90px 24px;
      text-align: center;
    }

    #contacto .section-title { color: var(--white); }
    #contacto .section-label { color: var(--gold-lt); }

    .contact-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1px;
      background: rgba(255,255,255,0.07);
      max-width: 860px;
      margin: 48px auto 48px;
      border: 1px solid rgba(255,255,255,0.07);
    }

    .contact-item {
      background: var(--charcoal);
      padding: 40px 28px;
    }

    .contact-item-label {
      font-family: 'Jost', sans-serif;
      font-size: 10px;
      letter-spacing: 4px;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 12px;
    }

    .contact-item p {
      font-family: 'Cormorant Garamond', serif;
      font-weight: 300;
      font-style: italic;
      font-size: 20px;
      color: rgba(255,255,255,0.75);
      line-height: 1.5;
    }

    .contact-item a {
      color: var(--gold-lt);
      text-decoration: none;
    }

    /* ── FOOTER ──────────────────────────────────── */
    footer {
      background: #111;
      color: rgba(255,255,255,0.35);
      text-align: center;
      padding: 36px 24px;
      border-top: 1px solid rgba(196,154,60,0.15);
    }

    .footer-brand {
      font-family: 'Cormorant Garamond', serif;
      font-weight: 300;
      font-style: italic;
      font-size: 22px;
      letter-spacing: 4px;
      color: rgba(255,255,255,0.5);
      margin-bottom: 12px;
    }

    footer p {
      font-family: 'Jost', sans-serif;
      font-weight: 300;
      font-size: 12px;
      letter-spacing: 1px;
      margin: 6px 0;
    }

    footer a { color: var(--gold); text-decoration: none; }
    footer a:hover { color: var(--gold-lt); }

    /* ── GALLERY MODAL ────────────────────────────── */
    .gallery-overlay {
      display: none;
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.92);
      z-index: 999;
      justify-content: center;
      align-items: center;
      padding: 40px 24px;
      backdrop-filter: blur(4px);
    }

    .gallery-overlay.active { display: flex; }

    .gallery-modal {
      max-width: 960px;
      width: 100%;
      max-height: 90vh;
      overflow-y: auto;
      position: relative;
    }

    .gallery-close {
      position: absolute;
      top: -40px;
      right: 0;
      background: none;
      border: none;
      color: #fff;
      font-size: 32px;
      cursor: pointer;
      opacity: 0.6;
      transition: opacity 0.25s;
      font-family: 'Jost', sans-serif;
    }

    .gallery-close:hover { opacity: 1; }

    .gallery-title {
      font-family: 'Cormorant Garamond', serif;
      font-weight: 300;
      font-style: italic;
      font-size: 32px;
      color: var(--gold);
      margin-bottom: 32px;
      letter-spacing: 2px;
    }

    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
    }

    .gallery-grid img {
      width: 100%;
      height: 260px;
      object-fit: cover;
      border-radius: 4px;
      transition: transform 0.3s, opacity 0.3s;
      cursor: pointer;
      border: 1px solid rgba(255,255,255,0.08);
    }

    .gallery-grid img:hover {
      transform: scale(1.03);
      opacity: 0.85;
    }

    .gallery-empty {
      grid-column: 1 / -1;
      text-align: center;
      padding: 60px 20px;
      border: 2px dashed rgba(255,255,255,0.15);
      border-radius: 8px;
    }

    .gallery-empty p {
      font-family: 'Jost', sans-serif;
      font-weight: 300;
      font-size: 15px;
      color: rgba(255,255,255,0.35);
      letter-spacing: 2px;
      line-height: 1.8;
    }

    .gallery-empty .icon {
      font-size: 48px;
      display: block;
      margin-bottom: 16px;
      opacity: 0.5;
    }

    .service-card { cursor: pointer; }

    /* ── TIENDA LUXURY ────────────────────────────── */
    .tienda-luxury .section-title {
      font-size: clamp(42px, 6vw, 64px);
      letter-spacing: 4px;
    }

    .tienda-luxury .section-label {
      font-family: 'Cormorant Garamond', serif;
      font-weight: 300;
      font-style: italic;
      font-size: 14px;
      letter-spacing: 6px;
      color: var(--gold);
    }

    .tienda-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 32px;
      margin-top: 48px;
    }

    .prod-card {
      background: rgba(255,255,255,0.03);
      border: 1px solid rgba(196,154,60,0.15);
      padding: 48px 32px 36px;
      transition: all 0.4s;
      text-align: center;
      position: relative;
    }

    .prod-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 2px;
      background: linear-gradient(90deg, transparent, var(--gold), transparent);
      transform: scaleX(0);
      transition: transform 0.5s;
    }

    .prod-card:hover {
      background: rgba(255,255,255,0.07);
      border-color: var(--gold);
      transform: translateY(-4px);
    }

    .prod-card:hover::before { transform: scaleX(1); }

    .prod-icon {
      font-size: 48px;
      margin-bottom: 24px;
      display: block;
      opacity: 0.7;
    }

    .prod-card h3 {
      font-family: 'Cormorant Garamond', serif;
      font-weight: 400;
      font-style: italic;
      font-size: 26px;
      color: var(--white);
      margin-bottom: 10px;
      letter-spacing: 1px;
    }

    .prod-card p {
      font-family: 'Cormorant Garamond', serif;
      font-weight: 300;
      font-style: italic;
      font-size: 15px;
      color: rgba(255,255,255,0.4);
      margin-bottom: 20px;
      letter-spacing: 1px;
    }

    .prod-price {
      font-family: 'Jost', sans-serif;
      font-weight: 400;
      font-size: 20px;
      color: var(--gold);
      letter-spacing: 2px;
      margin-bottom: 24px;
    }

    .btn-prod {
      display: block;
      width: 100%;
      background: transparent;
      border: 1px solid var(--gold);
      color: var(--gold);
      font-family: 'Jost', sans-serif;
      font-size: 10px;
      letter-spacing: 4px;
      text-transform: uppercase;
      padding: 14px;
      cursor: pointer;
      transition: all 0.4s;
    }

    .btn-prod:hover {
      background: var(--gold);
      color: var(--forest);
    }

    .tienda-desc {
      text-align: center;
      font-family: 'Cormorant Garamond', serif;
      font-weight: 300;
      font-style: italic;
      font-size: 17px;
      color: rgba(255,255,255,0.35);
      letter-spacing: 2px;
      max-width: 480px;
      margin: -24px auto 0;
      line-height: 1.7;
    }

    /* ── RESPONSIVE ──────────────────────────────── */
    @media (max-width: 860px) {
      header { padding: 0 20px; }

      .about-grid { grid-template-columns: 1fr; gap: 40px; }
      .about-img-wrap::after { display: none; }
      .about-img-wrap img { height: 320px; }

      .cards-grid { grid-template-columns: 1fr; }
      .ben-grid { grid-template-columns: 1fr 1fr; }
      .ben-item:nth-child(2n) { border-right: none; }
      .ben-item:nth-child(n+5) { border-bottom: none; }

      .tienda-grid { grid-template-columns: 1fr; }

      .promo-row { grid-template-columns: 1fr; gap: 12px; }
      .promo-num { font-size: 32px; }

      .contact-grid { grid-template-columns: 1fr; }

      .btn-outline { margin-left: 0; margin-top: 12px; display: block; text-align: center; }
    }

    @media (max-width: 560px) {
      .logo-wordmark .brand-name { font-size: 22px; letter-spacing: 2px; }
      nav a { font-size: 10px; padding: 14px 12px; letter-spacing: 2px; }
      .ben-grid { grid-template-columns: 1fr; }
      .ben-item { border-right: none; }
      .ben-item:last-child { border-bottom: none; }
    }
  </style>
</head>
<body>

<!-- HEADER -->
<header>
  <div class="logo-lockup">
    <img src="logo real lottus depi&spa.jpeg" alt="Logo Lottus Depispa">
    <div class="logo-wordmark">
      <span class="brand-name">Lottus Depi&amp;Spa</span>
      <span class="brand-sub">Centro de Estética &amp; Bienestar</span>
    </div>
  </div>
  <img src="foto propietaria LA REAL.jpeg" alt="Propietaria" class="header-avatar">
</header>

<!-- NAV -->
<nav>
  <ul>
    <li><a href="#inicio">Inicio</a></li>
    <li><a href="#sobre">Nosotros</a></li>
    <li><a href="#servicios">Servicios</a></li>
    <li><a href="#promos">Promociones</a></li>
    <li><a href="#tienda">Tienda</a></li>
    <li><a href="#contacto">Contacto</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero" id="inicio">
  <div class="hero-inner">
    <p class="hero-eyebrow">Alajuela · El Roble, Las Vegas · Costa Rica</p>
    <h1>Lottus<br><em>Depi&amp;Spa</em></h1>
    <div class="hero-divider"></div>
    <p class="hero-desc">Depilación Láser &nbsp;·&nbsp; Dermapen &nbsp;·&nbsp; Masajes Reductivos</p>
    <button class="btn-primary" onclick="contactarWhatsApp()">Agendar Cita</button>
    <a href="#servicios" class="btn-outline">Ver Servicios</a>
  </div>
</section>

<!-- SOBRE NOSOTROS -->
<section id="sobre">
  <div class="section">
    <p class="section-label">Quiénes somos</p>
    <h2 class="section-title">Nuestra historia</h2>
    <div class="section-rule"></div>
    <div class="about-grid">
      <div class="about-img-wrap">
        <img src="foto propietaria LA REAL.jpeg" alt="Propietaria Lottus Depispa">
      </div>
      <div class="about-text">
        <p class="label">Bienvenida</p>
        <h3>Donde la belleza<br>encuentra el bienestar</h3>
        <p>En Lottus Depispa creemos que la belleza y el bienestar van de la mano. Contamos con profesionales altamente capacitados que utilizan técnicas innovadoras y productos de calidad para brindarte los mejores resultados.</p>
        <p>Nuestro objetivo es que te sientas cómoda, confiada y radiante. Cada tratamiento está personalizado según tus necesidades, porque cada cliente es única.</p>
        <p>Ubicados en Alajuela, en el Roble Las Vegas, estamos listos para acompañarte en tu camino hacia tu mejor versión.</p>
        <br>
        <button class="btn-primary" onclick="contactarWhatsApp()">Reservar ahora</button>
      </div>
    </div>
  </div>
</section>

<!-- SERVICIOS -->
<div id="servicios" class="section-full">
  <div class="section">
    <p class="section-label">Lo que ofrecemos</p>
    <h2 class="section-title">Nuestros Servicios</h2>
    <div class="section-rule"></div>
  </div>
  <div style="max-width:1100px; margin: 0 auto 0; padding: 0 24px;">
    <div class="cards-grid">
      <div class="service-card" onclick="abrirGaleria('depilacion')">
        <div class="service-number">01</div>
        <h3>Depilación Láser</h3>
        <p>Tecnología avanzada de última generación que elimina el vello de forma permanente. Resultados visibles desde las primeras sesiones con total seguridad y comodidad.</p>
      </div>
      <div class="service-card" onclick="abrirGaleria('dermapen')">
        <div class="service-number">02</div>
        <h3>Dermapen</h3>
        <p>Tratamiento profesional de microneedling que rejuvenece, revitaliza y renueva la piel. Ideal para cicatrices, arrugas y flacidez. Tecnología de vanguardia.</p>
      </div>
      <div class="service-card" onclick="abrirGaleria('masajes')">
        <div class="service-number">03</div>
        <h3>Masajes Reductivos</h3>
        <p>Reduce medidas, moldea tu figura y propicia la relajación completa. Técnicas profesionales con resultados visibles y duraderos adaptados a tu cuerpo.</p>
      </div>
    </div>
  </div>
</div>

<!-- BENEFICIOS -->
<div id="beneficios-wrap">
  <div class="beneficios-inner">
    <p class="section-label">Por qué elegirnos</p>
    <h2 class="section-title">Nuestros Beneficios</h2>
    <div class="section-rule"></div>
    <div class="ben-grid">
      <div class="ben-item">
        <div class="ben-check">✦</div>
        <p>Piel suave, radiante y libre de vello</p>
      </div>
      <div class="ben-item">
        <div class="ben-check">✦</div>
        <p>Reduce medidas y moldea tu figura</p>
      </div>
      <div class="ben-item">
        <div class="ben-check">✦</div>
        <p>Relajación, bienestar y rejuvenecimiento</p>
      </div>
      <div class="ben-item">
        <div class="ben-check">✦</div>
        <p>Atención profesional y completamente personalizada</p>
      </div>
      <div class="ben-item">
        <div class="ben-check">✦</div>
        <p>Productos de calidad premium garantizada</p>
      </div>
      <div class="ben-item">
        <div class="ben-check">✦</div>
        <p>Técnicas innovadoras y probadas internacionalmente</p>
      </div>
    </div>
  </div>
</div>

<!-- PROMOCIONES -->
<section id="promos">
  <div class="section">
    <p class="section-label">Ofertas exclusivas</p>
    <h2 class="section-title">Promociones Especiales</h2>
    <div class="section-rule"></div>
    <div class="promos-list">
      <div class="promo-row">
        <div class="promo-num">01</div>
        <div class="promo-body">
          <h3>Depilación Láser en Promoción</h3>
          <p>Luce la piel que siempre has querido con nuestro tratamiento premium de depilación láser. Resultados permanentes, técnica segura y efectiva.</p>
        </div>
        <div class="promo-tag">Ver oferta</div>
      </div>
      <div class="promo-row">
        <div class="promo-num">02</div>
        <div class="promo-body">
          <h3>Masajes Reductivos Especiales</h3>
          <p>Redefine tu figura y relájate en cada sesión. Descuentos exclusivos por sesión con técnicas profesionales y atención personalizada.</p>
        </div>
        <div class="promo-tag">Ver oferta</div>
      </div>
      <div class="promo-row">
        <div class="promo-num">03</div>
        <div class="promo-body">
          <h3>Tratamientos con Dermapen</h3>
          <p>Rejuvenece y renueva tu piel con la tecnología más avanzada en microneedling. Reduce arrugas, cicatrices y flacidez.</p>
        </div>
        <div class="promo-tag">Ver oferta</div>
      </div>
    </div>
    <p style="text-align:center; margin-top: 48px; font-family:'Jost',sans-serif; font-size:13px; letter-spacing:2px; color: var(--sage); text-transform:uppercase;">
      Contáctanos para conocer precios y disponibilidad
    </p>
    <div style="text-align:center; margin-top:20px;">
      <button class="btn-primary" onclick="contactarWhatsApp()">Consultar por WhatsApp</button>
    </div>
  </div>
</section>

<!-- TIENDA (LUXURY) -->
<div id="tienda" class="section-full tienda-luxury">
  <div class="section">
    <p class="section-label">✦ Moda &amp; Estilo ✦</p>
    <h2 class="section-title">Boutique Exclusiva</h2>
    <div class="section-rule"></div>
    <p class="tienda-desc">
      Piezas seleccionadas con estilo, elegancia y carácter. Cada prenda cuenta una historia.
    </p>
  </div>
  <div style="max-width:1100px; margin: 0 auto; padding: 0 24px 0;">
    <div class="tienda-grid">
      <div class="prod-card">
        <span class="prod-icon">🤍</span>
        <h3>Colección Casual Chic</h3>
        <p>Elegancia para el día a día</p>
        <p class="prod-price">Desde ₡8,000</p>
        <button class="btn-prod" onclick="contactarWhatsApp()">Consultar</button>
      </div>
      <div class="prod-card">
        <span class="prod-icon">✨</span>
        <h3>Colección Sport Luxe</h3>
        <p>Comodidad con actitud</p>
        <p class="prod-price">Desde ₡10,000</p>
        <button class="btn-prod" onclick="contactarWhatsApp()">Consultar</button>
      </div>
      <div class="prod-card">
        <span class="prod-icon">💎</span>
        <h3>Alta Costura &amp; Eventos</h3>
        <p>Para momentos inolvidables</p>
        <p class="prod-price">Desde ₡15,000</p>
        <button class="btn-prod" onclick="contactarWhatsApp()">Consultar</button>
      </div>
    </div>
    <div style="text-align:center; margin-top: 48px;">
      <button class="btn-primary" onclick="contactarWhatsApp()" style="background:transparent; border:1px solid var(--gold); color:var(--gold); padding:16px 52px;">
        Solicitar Catálogo VIP
      </button>
    </div>
  </div>
</div>

<!-- CONTACTO -->
<section id="contacto">
  <p class="section-label">Estamos para ti</p>
  <h2 class="section-title">Contáctanos</h2>
  <div class="section-rule"></div>
  <div class="contact-grid">
    <div class="contact-item">
      <p class="contact-item-label">Ubicación</p>
      <p>Alajuela<br>El Roble, Las Vegas<br>Costa Rica</p>
    </div>
    <div class="contact-item">
      <p class="contact-item-label">Teléfono</p>
      <p>7093-0742</p>
    </div>
    <div class="contact-item">
      <p class="contact-item-label">WhatsApp</p>
      <p><a href="https://wa.me/50670930742">Escribirnos ahora</a></p>
    </div>
  </div>
  <button class="btn-primary" onclick="contactarWhatsApp()" style="font-size:12px; padding:18px 48px; letter-spacing:4px;">
    Agendar mi Cita
  </button>
</section>

<!-- GALLERY MODAL -->
<div class="gallery-overlay" id="galleryOverlay" onclick="if(event.target===this)cerrarGaleria()">
  <div class="gallery-modal">
    <button class="gallery-close" onclick="cerrarGaleria()">✕ Cerrar</button>
    <div class="gallery-title" id="galleryTitle">Servicio</div>
    <div class="gallery-grid" id="galleryGrid"></div>
  </div>
</div>

<!-- FOOTER -->
<footer>
  <div class="footer-brand">Lottus Depi&amp;Spa</div>
  <p>Centro de Estética y Bienestar &mdash; Alajuela, Costa Rica</p>
  <p style="margin-top:8px;">
    Instagram: <a href="https://www.instagram.com/lottusdepispa1788/" target="_blank">@lottusdepispa1788</a>
  </p>
  <p style="margin-top:16px; font-size:11px;">&copy; 2026 Lottus Depispa. Todos los derechos reservados.</p>
</footer>

<script>
  function contactarWhatsApp() {
    const numero = "50670930742";
    const mensaje = "Hola! Me interesa agendar una cita para conocer los servicios de Lottus Depispa.";
    window.open(`https://wa.me/${numero}?text=${encodeURIComponent(mensaje)}`, '_blank');
  }

  document.querySelectorAll('.promo-row').forEach(row => {
    row.addEventListener('click', () => contactarWhatsApp());
  });

  // ── GALERÍA DE SERVICIOS ──────────────────────────
  const fotosServicios = {
    depilacion: {
      titulo: "Depilación Láser",
      fotos: [
        "Captura de pantalla 2026-05-15 084917.jpg",
        "Captura de pantalla 2026-05-15 085052.jpg",
        "Captura de pantalla 2026-05-15 085125.jpg"
      ]
    },
    dermapen: {
      titulo: "Dermapen — Microneedling",
      fotos: []
    },
    masajes: {
      titulo: "Masajes Reductivos",
      fotos: []
    }
  };

  function abrirGaleria(servicio) {
    const data = fotosServicios[servicio];
    if (!data) return;

    document.getElementById('galleryTitle').textContent = data.titulo;
    const grid = document.getElementById('galleryGrid');
    grid.innerHTML = '';

    if (data.fotos.length === 0) {
      grid.innerHTML = `
        <div class="gallery-empty">
          <span class="icon">📸</span>
          <p>Pronto agregaremos fotos de este servicio.<br>
          Mientras tanto, <strong>contáctanos por WhatsApp</strong> para mostrarte resultados.</p>
          <br>
          <button class="btn-primary" onclick="contactarWhatsApp()" style="font-size:10px; padding:12px 32px;">
            Preguntar por WhatsApp
          </button>
        </div>
      `;
    } else {
      data.fotos.forEach(foto => {
        const img = document.createElement('img');
        img.src = foto;
        img.alt = data.titulo;
        img.loading = 'lazy';
        img.onclick = () => window.open(foto, '_blank');
        grid.appendChild(img);
      });
    }

    document.getElementById('galleryOverlay').classList.add('active');
    document.body.style.overflow = 'hidden';
  }

  function cerrarGaleria() {
    document.getElementById('galleryOverlay').classList.remove('active');
    document.body.style.overflow = '';
  }

  document.addEventListener('keydown', e => {
    if (e.key === 'Escape') cerrarGaleria();
  });
</script>
</body>
</html>>
