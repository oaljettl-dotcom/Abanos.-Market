# Abanos.-Market
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>أبانوس - هايبر ماركت مصراتة</title>
<link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;800;900&family=Playfair+Display:wght@700;900&display=swap" rel="stylesheet">
<style>
  :root {
    --green-deep: #1a5c2a;
    --green-mid: #2d8a45;
    --green-bright: #3ab54a;
    --green-light: #72c57e;
    --green-pale: #e8f5eb;
    --orange: #f5a623;
    --orange-warm: #f7b731;
    --yellow: #ffd700;
    --white: #ffffff;
    --cream: #fafaf7;
    --text-dark: #1a2e1e;
    --text-mid: #3d5c44;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Tajawal', sans-serif;
    background: var(--cream);
    color: var(--text-dark);
    overflow-x: hidden;
  }

  /* ---- NAV ---- */
  nav {
    position: fixed; top: 0; width: 100%; z-index: 100;
    background: rgba(26,92,42,0.97);
    backdrop-filter: blur(12px);
    padding: 0 5%;
    display: flex; align-items: center; justify-content: space-between;
    height: 70px;
    box-shadow: 0 2px 30px rgba(0,0,0,0.2);
  }

  .nav-logo {
    display: flex; align-items: center; gap: 12px;
  }

  .logo-icon {
    width: 44px; height: 44px; position: relative;
  }

  .logo-ring {
    width: 36px; height: 36px;
    border: 7px solid var(--orange);
    border-radius: 50%;
    position: absolute; bottom: 0; left: 4px;
  }

  .logo-leaf {
    width: 16px; height: 12px;
    background: var(--green-bright);
    border-radius: 50% 0 50% 0;
    position: absolute; top: 0; left: 16px;
    transform: rotate(-20deg);
  }

  .logo-text {
    font-size: 1.6rem; font-weight: 800;
    color: var(--white);
    letter-spacing: 1px;
  }

  .logo-text span { color: var(--orange); }

  .nav-links {
    display: flex; gap: 2rem; list-style: none;
  }

  .nav-links a {
    color: rgba(255,255,255,0.85);
    text-decoration: none;
    font-size: 1rem; font-weight: 500;
    transition: color 0.2s;
    position: relative;
  }

  .nav-links a::after {
    content: ''; position: absolute; bottom: -4px; right: 0;
    width: 0; height: 2px;
    background: var(--orange);
    transition: width 0.3s;
  }

  .nav-links a:hover { color: var(--orange-warm); }
  .nav-links a:hover::after { width: 100%; }

  .nav-cta {
    background: var(--orange);
    color: var(--white) !important;
    padding: 8px 20px;
    border-radius: 25px;
    font-weight: 700 !important;
    transition: transform 0.2s, box-shadow 0.2s !important;
  }
  .nav-cta:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 20px rgba(245,166,35,0.5);
    color: var(--white) !important;
  }
  .nav-cta::after { display: none !important; }

  /* ---- HERO ---- */
  .hero {
    min-height: 100vh;
    background: linear-gradient(135deg, var(--green-deep) 0%, var(--green-mid) 50%, #1e7a35 100%);
    display: flex; align-items: center;
    position: relative; overflow: hidden;
    padding-top: 70px;
  }

  .hero-bg-circles {
    position: absolute; inset: 0; pointer-events: none;
  }

  .circle {
    position: absolute; border-radius: 50%;
    background: rgba(255,255,255,0.04);
    animation: floatCircle 8s ease-in-out infinite;
  }

  .circle-1 { width: 500px; height: 500px; top: -150px; left: -100px; animation-delay: 0s; }
  .circle-2 { width: 300px; height: 300px; bottom: -80px; right: 10%; animation-delay: 2s; }
  .circle-3 { width: 200px; height: 200px; top: 30%; left: 40%; animation-delay: 4s; }

  @keyframes floatCircle {
    0%, 100% { transform: translateY(0) scale(1); }
    50% { transform: translateY(-20px) scale(1.03); }
  }

  .hero-content {
    position: relative; z-index: 2;
    padding: 0 8%;
    display: grid; grid-template-columns: 1fr 1fr;
    align-items: center; gap: 4rem;
    width: 100%;
  }

  .hero-text { animation: fadeUp 0.8s ease forwards; }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(40px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .hero-badge {
    display: inline-block;
    background: rgba(245,166,35,0.2);
    border: 1px solid rgba(245,166,35,0.5);
    color: var(--orange-warm);
    padding: 6px 16px; border-radius: 20px;
    font-size: 0.85rem; font-weight: 600;
    margin-bottom: 1.5rem;
    letter-spacing: 1px;
  }

  .hero-title {
    font-size: clamp(2.8rem, 5vw, 4.5rem);
    font-weight: 900;
    color: var(--white);
    line-height: 1.15;
    margin-bottom: 1rem;
  }

  .hero-title .highlight {
    color: var(--orange);
    position: relative;
  }

  .hero-title .highlight::after {
    content: '';
    position: absolute; bottom: 0; right: 0; left: 0;
    height: 4px;
    background: var(--orange);
    border-radius: 2px;
    opacity: 0.4;
  }

  .hero-subtitle {
    font-size: 1.15rem; color: rgba(255,255,255,0.78);
    line-height: 1.7; margin-bottom: 2.5rem;
    max-width: 480px;
  }

  .hero-actions { display: flex; gap: 1rem; flex-wrap: wrap; }

  .btn-primary {
    background: var(--orange);
    color: var(--white);
    padding: 14px 32px; border-radius: 30px;
    font-size: 1.05rem; font-weight: 700;
    text-decoration: none; border: none; cursor: pointer;
    transition: all 0.3s;
    box-shadow: 0 6px 25px rgba(245,166,35,0.4);
  }

  .btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 35px rgba(245,166,35,0.55);
    background: #e8951a;
  }

  .btn-secondary {
    background: transparent;
    color: var(--white);
    padding: 14px 32px; border-radius: 30px;
    font-size: 1.05rem; font-weight: 600;
    text-decoration: none; border: 2px solid rgba(255,255,255,0.4);
    cursor: pointer;
    transition: all 0.3s;
  }

  .btn-secondary:hover {
    border-color: var(--white);
    background: rgba(255,255,255,0.1);
  }

  .hero-visual {
    display: flex; justify-content: center; align-items: center;
    animation: fadeUp 0.8s 0.2s ease both;
  }

  .hero-logo-big {
    position: relative; width: 320px; height: 320px;
    display: flex; align-items: center; justify-content: center;
  }

  .big-ring {
    width: 250px; height: 250px;
    border: 40px solid var(--orange);
    border-radius: 50%;
    position: absolute;
    box-shadow: 0 0 80px rgba(245,166,35,0.35),
                inset 0 0 40px rgba(245,166,35,0.1);
    animation: pulseRing 3s ease-in-out infinite;
  }

  @keyframes pulseRing {
    0%, 100% { box-shadow: 0 0 80px rgba(245,166,35,0.35); }
    50% { box-shadow: 0 0 120px rgba(245,166,35,0.6); }
  }

  .big-leaf {
    position: absolute;
    top: 10px; right: 60px;
    width: 80px; height: 55px;
    background: linear-gradient(135deg, var(--green-bright), var(--green-light));
    border-radius: 50% 0 50% 0;
    transform: rotate(-20deg);
    box-shadow: 0 8px 25px rgba(58,181,74,0.4);
    animation: leafSway 4s ease-in-out infinite;
  }

  @keyframes leafSway {
    0%, 100% { transform: rotate(-20deg); }
    50% { transform: rotate(-10deg) scale(1.05); }
  }

  .brand-name-big {
    font-size: 2.8rem; font-weight: 900;
    color: var(--white);
    text-shadow: 0 4px 20px rgba(0,0,0,0.3);
    z-index: 2;
  }

  .hero-stats {
    position: absolute; bottom: 40px; left: 8%; right: 8%;
    display: flex; gap: 2rem;
    z-index: 2;
    flex-wrap: wrap;
  }

  .stat-card {
    background: rgba(255,255,255,0.1);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255,255,255,0.15);
    border-radius: 16px;
    padding: 16px 24px;
    text-align: center;
    flex: 1; min-width: 120px;
  }

  .stat-number {
    font-size: 1.8rem; font-weight: 900;
    color: var(--orange-warm);
    display: block;
  }

  .stat-label {
    font-size: 0.8rem; color: rgba(255,255,255,0.75);
    font-weight: 500;
  }

  /* ---- SECTION HEADERS ---- */
  .section { padding: 90px 8%; }

  .section-tag {
    display: inline-block;
    background: var(--green-pale);
    color: var(--green-mid);
    padding: 5px 14px; border-radius: 20px;
    font-size: 0.8rem; font-weight: 700;
    letter-spacing: 1px; margin-bottom: 1rem;
    border: 1px solid rgba(45,138,69,0.2);
  }

  .section-title {
    font-size: clamp(1.8rem, 3vw, 2.8rem);
    font-weight: 900; color: var(--green-deep);
    margin-bottom: 0.5rem;
  }

  .section-sub {
    color: var(--text-mid); font-size: 1rem;
    line-height: 1.7; max-width: 550px;
    margin-bottom: 3rem;
  }

  /* ---- CATEGORIES ---- */
  .categories-bg {
    background: var(--white);
  }

  .categories-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
    gap: 1.2rem;
  }

  .cat-card {
    background: var(--green-pale);
    border-radius: 20px;
    padding: 28px 16px;
    text-align: center;
    cursor: pointer;
    transition: all 0.3s;
    border: 2px solid transparent;
    text-decoration: none;
    display: block;
  }

  .cat-card:hover {
    border-color: var(--green-mid);
    transform: translateY(-6px);
    box-shadow: 0 15px 40px rgba(45,138,69,0.15);
    background: var(--white);
  }

  .cat-icon {
    font-size: 2.6rem;
    display: block; margin-bottom: 10px;
  }

  .cat-name {
    font-size: 0.95rem; font-weight: 700;
    color: var(--green-deep);
    display: block;
  }

  .cat-count {
    font-size: 0.75rem; color: var(--text-mid);
    margin-top: 4px; display: block;
  }

  /* ---- PRODUCTS ---- */
  .products-bg { background: var(--cream); }

  .products-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
    gap: 1.5rem;
  }

  .product-card {
    background: var(--white);
    border-radius: 20px;
    overflow: hidden;
    transition: all 0.3s;
    box-shadow: 0 2px 15px rgba(0,0,0,0.06);
    position: relative;
  }

  .product-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 20px 50px rgba(26,92,42,0.15);
  }

  .product-badge {
    position: absolute; top: 12px; right: 12px;
    background: var(--green-mid);
    color: var(--white);
    padding: 4px 10px; border-radius: 12px;
    font-size: 0.72rem; font-weight: 700;
    z-index: 2;
  }

  .product-badge.offer { background: #e74c3c; }

  .product-img {
    width: 100%; height: 160px;
    display: flex; align-items: center; justify-content: center;
    font-size: 4rem;
    background: linear-gradient(135deg, var(--green-pale), #d4edda);
  }

  .product-info { padding: 16px; }

  .product-name {
    font-size: 0.95rem; font-weight: 700;
    color: var(--text-dark); margin-bottom: 4px;
  }

  .product-origin {
    font-size: 0.78rem; color: var(--text-mid);
    margin-bottom: 10px;
  }

  .product-footer {
    display: flex; align-items: center; justify-content: space-between;
  }

  .product-price {
    font-size: 1.1rem; font-weight: 800;
    color: var(--green-mid);
  }

  .product-price .old {
    font-size: 0.78rem; color: #aaa;
    text-decoration: line-through;
    margin-right: 6px; font-weight: 400;
  }

  .add-btn {
    width: 36px; height: 36px;
    border-radius: 50%;
    background: var(--green-mid);
    border: none; cursor: pointer;
    color: var(--white);
    font-size: 1.2rem;
    display: flex; align-items: center; justify-content: center;
    transition: all 0.2s;
  }

  .add-btn:hover {
    background: var(--green-deep);
    transform: scale(1.1);
  }

  /* ---- WHY US ---- */
  .why-bg {
    background: linear-gradient(135deg, var(--green-deep), var(--green-mid));
    color: var(--white);
  }

  .why-bg .section-title { color: var(--white); }
  .why-bg .section-sub { color: rgba(255,255,255,0.75); }
  .why-bg .section-tag { background: rgba(255,255,255,0.15); color: var(--orange-warm); border-color: rgba(245,166,35,0.3); }

  .features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
    gap: 1.5rem;
  }

  .feature-card {
    background: rgba(255,255,255,0.08);
    border: 1px solid rgba(255,255,255,0.12);
    border-radius: 20px; padding: 30px 24px;
    transition: all 0.3s;
  }

  .feature-card:hover {
    background: rgba(255,255,255,0.14);
    transform: translateY(-4px);
  }

  .feature-icon {
    font-size: 2.5rem; margin-bottom: 16px;
    display: block;
  }

  .feature-title {
    font-size: 1.1rem; font-weight: 700;
    margin-bottom: 8px; color: var(--orange-warm);
  }

  .feature-desc {
    font-size: 0.88rem; color: rgba(255,255,255,0.72);
    line-height: 1.7;
  }

  /* ---- OFFERS BANNER ---- */
  .offers-banner {
    background: linear-gradient(135deg, var(--orange) 0%, #e8951a 100%);
    padding: 60px 8%;
    display: flex; align-items: center; justify-content: space-between;
    gap: 2rem; flex-wrap: wrap;
    position: relative; overflow: hidden;
  }

  .offers-banner::before {
    content: '🛒';
    font-size: 12rem;
    position: absolute; left: -2rem; top: 50%;
    transform: translateY(-50%);
    opacity: 0.08;
  }

  .offer-text h2 {
    font-size: clamp(1.8rem, 3vw, 2.5rem);
    font-weight: 900; color: var(--white);
    margin-bottom: 0.5rem;
  }

  .offer-text p {
    color: rgba(255,255,255,0.85);
    font-size: 1rem; line-height: 1.6;
  }

  .btn-white {
    background: var(--white);
    color: var(--orange);
    padding: 14px 36px; border-radius: 30px;
    font-size: 1.05rem; font-weight: 800;
    text-decoration: none;
    transition: all 0.3s;
    white-space: nowrap;
    box-shadow: 0 6px 25px rgba(0,0,0,0.15);
  }

  .btn-white:hover {
    transform: translateY(-3px);
    box-shadow: 0 12px 35px rgba(0,0,0,0.2);
  }

  /* ---- CONTACT ---- */
  .contact-bg { background: var(--white); }

  .contact-grid {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 4rem; align-items: start;
  }

  .contact-info-block { display: flex; flex-direction: column; gap: 1.5rem; }

  .contact-item {
    display: flex; align-items: flex-start; gap: 16px;
    background: var(--green-pale);
    border-radius: 16px; padding: 20px;
  }

  .contact-item-icon {
    font-size: 1.8rem; flex-shrink: 0;
    width: 50px; height: 50px;
    background: var(--white);
    border-radius: 12px;
    display: flex; align-items: center; justify-content: center;
  }

  .contact-item-text h4 {
    font-size: 0.85rem; color: var(--text-mid);
    margin-bottom: 4px; font-weight: 600;
  }

  .contact-item-text p {
    font-size: 1rem; color: var(--green-deep);
    font-weight: 700; line-height: 1.5;
  }

  .contact-form {
    background: var(--green-pale);
    border-radius: 24px; padding: 36px;
  }

  .contact-form h3 {
    font-size: 1.4rem; font-weight: 800;
    color: var(--green-deep); margin-bottom: 1.5rem;
  }

  .form-group { margin-bottom: 1.2rem; }

  .form-group label {
    display: block; font-size: 0.85rem;
    font-weight: 600; color: var(--text-mid);
    margin-bottom: 6px;
  }

  .form-group input,
  .form-group textarea {
    width: 100%;
    background: var(--white);
    border: 2px solid transparent;
    border-radius: 12px;
    padding: 12px 16px;
    font-family: 'Tajawal', sans-serif;
    font-size: 0.95rem; color: var(--text-dark);
    outline: none;
    transition: border-color 0.2s;
    direction: rtl;
  }

  .form-group input:focus,
  .form-group textarea:focus { border-color: var(--green-mid); }

  .form-group textarea { resize: vertical; min-height: 100px; }

  .form-submit {
    width: 100%;
    background: var(--green-mid);
    color: var(--white);
    padding: 14px;
    border-radius: 12px;
    border: none; cursor: pointer;
    font-family: 'Tajawal', sans-serif;
    font-size: 1rem; font-weight: 700;
    transition: all 0.3s;
  }

  .form-submit:hover {
    background: var(--green-deep);
    transform: translateY(-2px);
  }

  /* ---- FOOTER ---- */
  footer {
    background: var(--green-deep);
    color: rgba(255,255,255,0.8);
    padding: 50px 8% 24px;
  }

  .footer-grid {
    display: grid;
    grid-template-columns: 2fr 1fr 1fr 1fr;
    gap: 3rem; margin-bottom: 3rem;
  }

  .footer-brand .logo-text { color: var(--white); font-size: 1.8rem; }
  .footer-brand .tagline {
    color: rgba(255,255,255,0.6);
    font-size: 0.9rem; margin-top: 0.8rem;
    line-height: 1.6;
  }

  .footer-col h4 {
    color: var(--orange-warm);
    font-size: 1rem; font-weight: 700;
    margin-bottom: 1.2rem;
  }

  .footer-col ul { list-style: none; display: flex; flex-direction: column; gap: 0.6rem; }
  .footer-col a {
    color: rgba(255,255,255,0.65);
    text-decoration: none; font-size: 0.9rem;
    transition: color 0.2s;
  }
  .footer-col a:hover { color: var(--orange-warm); }

  .footer-bottom {
    border-top: 1px solid rgba(255,255,255,0.1);
    padding-top: 20px;
    display: flex; justify-content: space-between;
    align-items: center; flex-wrap: wrap; gap: 1rem;
  }

  .footer-bottom p { font-size: 0.82rem; color: rgba(255,255,255,0.45); }

  .social-links { display: flex; gap: 10px; }
  .social-btn {
    width: 36px; height: 36px;
    border-radius: 50%;
    background: rgba(255,255,255,0.1);
    color: var(--white);
    display: flex; align-items: center; justify-content: center;
    text-decoration: none; font-size: 0.9rem;
    transition: all 0.2s;
    border: 1px solid rgba(255,255,255,0.15);
  }
  .social-btn:hover { background: var(--orange); border-color: var(--orange); }

  /* ---- SCROLL REVEAL ---- */
  .reveal {
    opacity: 0; transform: translateY(30px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }
  .reveal.visible { opacity: 1; transform: translateY(0); }
  .reveal-delay-1 { transition-delay: 0.1s; }
  .reveal-delay-2 { transition-delay: 0.2s; }
  .reveal-delay-3 { transition-delay: 0.3s; }
  .reveal-delay-4 { transition-delay: 0.4s; }

  /* ---- RESPONSIVE ---- */
  @media (max-width: 900px) {
    .hero-content { grid-template-columns: 1fr; text-align: center; }
    .hero-visual { display: none; }
    .hero-stats { position: relative; bottom: auto; margin-top: 3rem; justify-content: center; }
    .hero { min-height: auto; padding: 120px 5% 60px; }
    .hero-subtitle { margin: 0 auto 2rem; }
    .hero-actions { justify-content: center; }
    .contact-grid { grid-template-columns: 1fr; }
    .footer-grid { grid-template-columns: 1fr 1fr; }
    nav { padding: 0 4%; }
    .nav-links { display: none; }
  }

  @media (max-width: 600px) {
    .section { padding: 60px 5%; }
    .footer-grid { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">
    <div class="logo-icon">
      <div class="logo-ring"></div>
      <div class="logo-leaf"></div>
    </div>
    <span class="logo-text">Aban<span>ó</span>s</span>
  </div>
  <ul class="nav-links">
    <li><a href="#categories">الأقسام</a></li>
    <li><a href="#products">المنتجات</a></li>
    <li><a href="#offers">العروض</a></li>
    <li><a href="#contact">تواصل معنا</a></li>
    <li><a href="#contact" class="nav-cta">🛒 تسوّق الآن</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-bg-circles">
    <div class="circle circle-1"></div>
    <div class="circle circle-2"></div>
    <div class="circle circle-3"></div>
  </div>
  <div class="hero-content">
    <div class="hero-text">
      <span class="hero-badge">📍 مصراتة، ليبيا</span>
      <h1 class="hero-title">
        طازج كل يوم،<br>
        <span class="highlight">أبانوس</span> في بيتك
      </h1>
      <p class="hero-subtitle">
        أفضل هايبر ماركت في مصراتة — خضار وفواكه طازجة، منتجات متنوعة، وأسعار لا تُقارن. كل ما تحتاجه تحت سقف واحد.
      </p>
      <div class="hero-actions">
        <a href="#products" class="btn-primary">🛍️ تصفّح المنتجات</a>
        <a href="#contact" class="btn-secondary">📞 تواصل معنا</a>
      </div>
    </div>
    <div class="hero-visual">
      <div class="hero-logo-big">
        <div class="big-ring"></div>
        <div class="big-leaf"></div>
        <span class="brand-name-big">Abanos</span>
      </div>
    </div>
  </div>
  <div class="hero-stats">
    <div class="stat-card">
      <span class="stat-number">+5000</span>
      <span class="stat-label">منتج متوفر</span>
    </div>
    <div class="stat-card">
      <span class="stat-number">+10K</span>
      <span class="stat-label">عميل راضٍ</span>
    </div>
    <div class="stat-card">
      <span class="stat-number">يومي</span>
      <span class="stat-label">توصيل طازج</span>
    </div>
    <div class="stat-card">
      <span class="stat-number">أفضل</span>
      <span class="stat-label">أسعار في مصراتة</span>
    </div>
  </div>
</section>

<!-- CATEGORIES -->
<section class="section categories-bg" id="categories">
  <div class="reveal">
    <span class="section-tag">الأقسام</span>
    <h2 class="section-title">تسوّق بالقسم</h2>
    <p class="section-sub">اختر من بين مئات المنتجات في كل قسم، كلها طازجة ومنتقاة بعناية.</p>
  </div>
  <div class="categories-grid">
    <a href="#" class="cat-card reveal reveal-delay-1">
      <span class="cat-icon">🥦</span>
      <span class="cat-name">خضروات</span>
      <span class="cat-count">+120 صنف</span>
    </a>
    <a href="#" class="cat-card reveal reveal-delay-1">
      <span class="cat-icon">🍊</span>
      <span class="cat-name">فواكه</span>
      <span class="cat-count">+80 صنف</span>
    </a>
    <a href="#" class="cat-card reveal reveal-delay-2">
      <span class="cat-icon">🥩</span>
      <span class="cat-name">لحوم ودواجن</span>
      <span class="cat-count">+60 صنف</span>
    </a>
    <a href="#" class="cat-card reveal reveal-delay-2">
      <span class="cat-icon">🐟</span>
      <span class="cat-name">أسماك</span>
      <span class="cat-count">+40 صنف</span>
    </a>
    <a href="#" class="cat-card reveal reveal-delay-3">
      <span class="cat-icon">🧀</span>
      <span class="cat-name">ألبان وأجبان</span>
      <span class="cat-count">+90 صنف</span>
    </a>
    <a href="#" class="cat-card reveal reveal-delay-3">
      <span class="cat-icon">🍞</span>
      <span class="cat-name">مخبوزات</span>
      <span class="cat-count">+50 صنف</span>
    </a>
    <a href="#" class="cat-card reveal reveal-delay-4">
      <span class="cat-icon">🥫</span>
      <span class="cat-name">معلبات وجاف</span>
      <span class="cat-count">+200 صنف</span>
    </a>
    <a href="#" class="cat-card reveal reveal-delay-4">
      <span class="cat-icon">🧴</span>
      <span class="cat-name">مواد تنظيف</span>
      <span class="cat-count">+150 صنف</span>
    </a>
  </div>
</section>

<!-- PRODUCTS -->
<section class="section products-bg" id="products">
  <div class="reveal">
    <span class="section-tag">منتجاتنا</span>
    <h2 class="section-title">أبرز المنتجات</h2>
    <p class="section-sub">منتقاة يومياً بأعلى معايير الجودة والطزاجة.</p>
  </div>
  <div class="products-grid">
    <div class="product-card reveal reveal-delay-1">
      <span class="product-badge">جديد</span>
      <div class="product-img">🥑</div>
      <div class="product-info">
        <div class="product-name">أفوكادو طازج</div>
        <div class="product-origin">🌍 مستورد</div>
        <div class="product-footer">
          <div class="product-price">5.50 د.ل</div>
          <button class="add-btn">+</button>
        </div>
      </div>
    </div>
    <div class="product-card reveal reveal-delay-1">
      <span class="product-badge offer">خصم 20%</span>
      <div class="product-img">🍅</div>
      <div class="product-info">
        <div class="product-name">طماطم كيلو</div>
        <div class="product-origin">📍 محلي - مصراتة</div>
        <div class="product-footer">
          <div class="product-price"><span class="old">2.50</span> 2.00 د.ل</div>
          <button class="add-btn">+</button>
        </div>
      </div>
    </div>
    <div class="product-card reveal reveal-delay-2">
      <div class="product-img">🍊</div>
      <div class="product-info">
        <div class="product-name">برتقال طازج</div>
        <div class="product-origin">📍 محلي</div>
        <div class="product-footer">
          <div class="product-price">3.00 د.ل</div>
          <button class="add-btn">+</button>
        </div>
      </div>
    </div>
    <div class="product-card reveal reveal-delay-2">
      <span class="product-badge">مميز</span>
      <div class="product-img">🫒</div>
      <div class="product-info">
        <div class="product-name">زيت زيتون ليبي</div>
        <div class="product-origin">🌿 ليبي أصيل</div>
        <div class="product-footer">
          <div class="product-price">18.00 د.ل</div>
          <button class="add-btn">+</button>
        </div>
      </div>
    </div>
    <div class="product-card reveal reveal-delay-3">
      <div class="product-img">🥬</div>
      <div class="product-info">
        <div class="product-name">خس طازج</div>
        <div class="product-origin">📍 محلي</div>
        <div class="product-footer">
          <div class="product-price">1.50 د.ل</div>
          <button class="add-btn">+</button>
        </div>
      </div>
    </div>
    <div class="product-card reveal reveal-delay-3">
      <span class="product-badge offer">عرض</span>
      <div class="product-img">🧅</div>
      <div class="product-info">
        <div class="product-name">بصل - كيلو</div>
        <div class="product-origin">📍 محلي</div>
        <div class="product-footer">
          <div class="product-price"><span class="old">1.50</span> 1.00 د.ل</div>
          <button class="add-btn">+</button>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- OFFERS BANNER -->
<section class="offers-banner" id="offers">
  <div class="offer-text reveal">
    <h2>عروض الأسبوع 🔥</h2>
    <p>خصومات تصل إلى 40% على مئات المنتجات المختارة.<br>لا تفوّت الفرصة — العرض محدود!</p>
  </div>
  <a href="#contact" class="btn-white reveal reveal-delay-2">اكتشف العروض</a>
</section>

<!-- WHY US -->
<section class="section why-bg">
  <div class="reveal">
    <span class="section-tag">لماذا أبانوس؟</span>
    <h2 class="section-title">أكثر من مجرد متجر</h2>
    <p class="section-sub">نحن نؤمن بأن التسوق يجب أن يكون تجربة ممتعة، سريعة، وموثوقة.</p>
  </div>
  <div class="features-grid">
    <div class="feature-card reveal reveal-delay-1">
      <span class="feature-icon">🌱</span>
      <div class="feature-title">منتجات طازجة يومياً</div>
      <p class="feature-desc">نستقبل شحنات الخضار والفواكه كل صباح مباشرة من المزارعين المحليين.</p>
    </div>
    <div class="feature-card reveal reveal-delay-2">
      <span class="feature-icon">💰</span>
      <div class="feature-title">أفضل الأسعار</div>
      <p class="feature-desc">أسعار تنافسية لا تجدها في أي مكان آخر في مصراتة — نضمن ذلك.</p>
    </div>
    <div class="feature-card reveal reveal-delay-3">
      <span class="feature-icon">🚚</span>
      <div class="feature-title">توصيل سريع</div>
      <p class="feature-desc">خدمة توصيل لجميع أحياء مصراتة خلال ساعات قليلة من الطلب.</p>
    </div>
    <div class="feature-card reveal reveal-delay-4">
      <span class="feature-icon">✅</span>
      <div class="feature-title">جودة مضمونة</div>
      <p class="feature-desc">كل منتج يمر بفحص دقيق قبل وصوله إلى رفوفنا أو طاولتك.</p>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="section contact-bg" id="contact">
  <div class="reveal">
    <span class="section-tag">تواصل معنا</span>
    <h2 class="section-title">نحن هنا لخدمتك</h2>
    <p class="section-sub">لأي استفسار أو طلب، فريقنا جاهز دائماً.</p>
  </div>
  <div class="contact-grid">
    <div class="contact-info-block reveal">
      <div class="contact-item">
        <div class="contact-item-icon">📍</div>
        <div class="contact-item-text">
          <h4>الموقع</h4>
          <p>مصراتة، ليبيا<br>شارع الجمهورية الرئيسي</p>
        </div>
      </div>
      <div class="contact-item">
        <div class="contact-item-icon">📞</div>
        <div class="contact-item-text">
          <h4>الهاتف</h4>
          <p>+218 91 XXX XXXX<br>+218 92 XXX XXXX</p>
        </div>
      </div>
      <div class="contact-item">
        <div class="contact-item-icon">🕐</div>
        <div class="contact-item-text">
          <h4>أوقات العمل</h4>
          <p>يومياً من 8 صباحاً حتى 11 مساءً</p>
        </div>
      </div>
      <div class="contact-item">
        <div class="contact-item-icon">📱</div>
        <div class="contact-item-text">
          <h4>تواصل عبر</h4>
          <p>واتساب · فيسبوك · إنستغرام<br>@Abanos.ly</p>
        </div>
      </div>
    </div>
    <div class="contact-form reveal reveal-delay-2">
      <h3>📬 أرسل لنا رسالة</h3>
      <div class="form-group">
        <label>الاسم الكامل</label>
        <input type="text" placeholder="أدخل اسمك">
      </div>
      <div class="form-group">
        <label>رقم الهاتف</label>
        <input type="tel" placeholder="09X XXXX XXXX">
      </div>
      <div class="form-group">
        <label>الرسالة</label>
        <textarea placeholder="اكتب استفسارك أو طلبك..."></textarea>
      </div>
      <button class="form-submit">إرسال الرسالة ✉️</button>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-grid">
    <div class="footer-brand">
      <div class="nav-logo" style="margin-bottom:12px;">
        <div class="logo-icon">
          <div class="logo-ring"></div>
          <div class="logo-leaf"></div>
        </div>
        <span class="logo-text" style="font-size:1.8rem;">Aban<span style="color:var(--orange)">ó</span>s</span>
      </div>
      <p class="tagline">هايبر ماركت أبانوس — مصراتة، ليبيا.<br>طازج كل يوم، وأسعار لا تُقارن.</p>
    </div>
    <div class="footer-col">
      <h4>روابط سريعة</h4>
      <ul>
        <li><a href="#categories">الأقسام</a></li>
        <li><a href="#products">المنتجات</a></li>
        <li><a href="#offers">العروض</a></li>
        <li><a href="#contact">من نحن</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>الأقسام</h4>
      <ul>
        <li><a href="#">خضروات وفواكه</a></li>
        <li><a href="#">لحوم وأسماك</a></li>
        <li><a href="#">ألبان وأجبان</a></li>
        <li><a href="#">معلبات وجاف</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>خدمة العملاء</h4>
      <ul>
        <li><a href="#">سياسة الإرجاع</a></li>
        <li><a href="#">الشحن والتوصيل</a></li>
        <li><a href="#">الأسئلة الشائعة</a></li>
        <li><a href="#contact">تواصل معنا</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <p>© 2026 Abanos Hypermarket — مصراتة، ليبيا. جميع الحقوق محفوظة.</p>
    <div class="social-links">
      <a href="#" class="social-btn">f</a>
      <a href="#" class="social-btn">in</a>
      <a href="#" class="social-btn">w</a>
      <a href="#" class="social-btn">📸</a>
    </div>
  </div>
</footer>

<script>
  // Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
      }
    });
  }, { threshold: 0.12 });
  reveals.forEach(el => observer.observe(el));

  // Add to cart micro-interaction
  document.querySelectorAll('.add-btn').forEach(btn => {
    btn.addEventListener('click', function() {
      const original = this.textContent;
      this.textContent = '✓';
      this.style.background = '#27ae60';
      setTimeout(() => {
        this.textContent = original;
        this.style.background = '';
      }, 1000);
    });
  });
</script>
</body>
</html>
