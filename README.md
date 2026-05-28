<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Arazá — Moda Artesanal de Lujo</title>
  <meta name="description" content="Arazá: Ropa de lujo artesanal elaborada por comunidades artesanas colombianas. Comercio ético, transparencia y pago justo. Slow fashion en ediciones limitadas.">
  <meta name="keywords" content="Arazá, moda artesanal, lujo, slow fashion, Colombia, comercio ético, artesanía">
  <meta property="og:title" content="Arazá — Moda Artesanal de Lujo">
  <meta property="og:description" content="Prendas exclusivas y de lujo artesanal. Comercio ético, transparencia y pago justo.">
  <meta property="og:type" content="website">

  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;0,800;1,400;1,500&display=swap" rel="stylesheet">

  <style>
    /* ══════════════════════════════════════════
       RESET & BASE
    ══════════════════════════════════════════ */
    *, *::before, *::after {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
      font-size: 16px;
    }

    body {
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
      background-color: #F5F0E8;
      color: #1A0F0A;
      line-height: 1.6;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    img {
      display: block;
      max-width: 100%;
      height: auto;
    }

    ul {
      list-style: none;
    }

    button, input, textarea {
      font-family: inherit;
      font-size: inherit;
    }

    /* Custom scrollbar */
    ::-webkit-scrollbar { width: 8px; }
    ::-webkit-scrollbar-track { background: #E8DDD0; }
    ::-webkit-scrollbar-thumb { background: #6B3A2A; border-radius: 4px; }
    ::-webkit-scrollbar-thumb:hover { background: #4A2518; }

    /* ══════════════════════════════════════════
       UTILITIES
    ══════════════════════════════════════════ */
    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 1rem;
    }

    @media (min-width: 640px) {
      .container { padding: 0 1.5rem; }
    }

    @media (min-width: 1024px) {
      .container { padding: 0 2rem; }
    }

    .section-padding {
      padding-top: 5rem;
      padding-bottom: 5rem;
    }

    @media (min-width: 640px) {
      .section-padding { padding-top: 7rem; padding-bottom: 7rem; }
    }

    @media (min-width: 1024px) {
      .section-padding { padding-top: 9rem; padding-bottom: 9rem; }
    }

    .serif { font-family: 'Playfair Display', Georgia, 'Times New Roman', serif; }
    .sans { font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif; }

    .text-center { text-align: center; }
    .mx-auto { margin-left: auto; margin-right: auto; }

    .section-kicker {
      color: #C9A84C;
      font-size: 0.75rem;
      letter-spacing: 0.35em;
      text-transform: uppercase;
      margin-bottom: 1rem;
    }

    @media (min-width: 640px) {
      .section-kicker { font-size: 0.875rem; }
    }

    .section-title {
      font-family: 'Playfair Display', Georgia, serif;
      font-size: 1.875rem;
      font-weight: 700;
      color: #1A0F0A;
      margin-bottom: 1.5rem;
    }

    @media (min-width: 640px) {
      .section-title { font-size: 2.25rem; }
    }

    @media (min-width: 1024px) {
      .section-title { font-size: 3rem; }
    }

    .section-divider {
      width: 4rem;
      height: 2px;
      background-color: #C9A84C;
      margin: 0 auto 1.5rem;
    }

    .section-subtitle {
      font-family: 'Inter', sans-serif;
      color: rgba(26, 15, 10, 0.6);
      max-width: 42rem;
      margin: 0 auto;
      font-size: 1rem;
      line-height: 1.7;
    }

    @media (min-width: 640px) {
      .section-subtitle { font-size: 1.125rem; }
    }

    /* ══════════════════════════════════════════
       NAVBAR
    ══════════════════════════════════════════ */
    .navbar {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      z-index: 1000;
      transition: all 0.5s ease;
      background: transparent;
    }

    .navbar.scrolled {
      background: rgba(245, 240, 232, 0.95);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      box-shadow: 0 1px 3px rgba(0,0,0,0.08);
      border-bottom: 1px solid #D4C8B8;
    }

    .navbar-inner {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 1rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      height: 4rem;
    }

    @media (min-width: 640px) {
      .navbar-inner { height: 5rem; padding: 0 1.5rem; }
    }

    @media (min-width: 1024px) {
      .navbar-inner { padding: 0 2rem; }
    }

    .nav-logo {
      font-family: 'Playfair Display', serif;
      font-size: 1.5rem;
      font-weight: 700;
      letter-spacing: 0.15em;
      color: #6B3A2A;
      transition: color 0.3s;
    }

    @media (min-width: 640px) {
      .nav-logo { font-size: 1.875rem; }
    }

    .nav-logo:hover { color: #4A2518; }

    .nav-links {
      display: none;
      align-items: center;
      gap: 2rem;
    }

    @media (min-width: 768px) {
      .nav-links { display: flex; }
    }

    .nav-links a {
      font-size: 0.875rem;
      font-weight: 500;
      color: rgba(26, 15, 10, 0.7);
      letter-spacing: 0.05em;
      text-transform: uppercase;
      transition: color 0.3s;
    }

    .nav-links a:hover { color: #6B3A2A; }

    .nav-cta {
      display: none;
      background-color: #6B3A2A;
      color: #F5F0E8;
      font-weight: 500;
      letter-spacing: 0.05em;
      padding: 0.5rem 1.5rem;
      border: none;
      cursor: pointer;
      font-size: 0.875rem;
      transition: background-color 0.3s;
    }

    @media (min-width: 768px) {
      .nav-cta { display: inline-block; }
    }

    .nav-cta:hover { background-color: #4A2518; }

    .mobile-toggle {
      display: block;
      background: none;
      border: none;
      color: #6B3A2A;
      cursor: pointer;
      padding: 0.5rem;
    }

    @media (min-width: 768px) {
      .mobile-toggle { display: none; }
    }

    .mobile-toggle svg { width: 24px; height: 24px; }

    .mobile-menu {
      display: none;
      background: rgba(245, 240, 232, 0.98);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border-top: 1px solid #D4C8B8;
      padding: 1rem;
    }

    .mobile-menu.open { display: block; }

    .mobile-menu a {
      display: block;
      font-size: 0.875rem;
      font-weight: 500;
      color: rgba(26, 15, 10, 0.7);
      letter-spacing: 0.05em;
      text-transform: uppercase;
      padding: 0.5rem 0;
      transition: color 0.3s;
    }

    .mobile-menu a:hover { color: #6B3A2A; }

    .mobile-menu .nav-cta-mobile {
      display: block;
      width: 100%;
      background-color: #6B3A2A;
      color: #F5F0E8;
      font-weight: 500;
      letter-spacing: 0.05em;
      padding: 0.625rem 1.5rem;
      border: none;
      cursor: pointer;
      font-size: 0.875rem;
      margin-top: 0.75rem;
      text-align: center;
      transition: background-color 0.3s;
    }

    .mobile-menu .nav-cta-mobile:hover { background-color: #4A2518; }

    /* ══════════════════════════════════════════
       HERO
    ══════════════════════════════════════════ */
    .hero {
      position: relative;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }

    .hero-bg {
      position: absolute;
      inset: 0;
      z-index: 0;
    }

    .hero-bg img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .hero-overlay {
      position: absolute;
      inset: 0;
      background: linear-gradient(to bottom, rgba(26,15,10,0.6), rgba(26,15,10,0.4) 50%, rgba(26,15,10,0.7));
    }

    .hero-line-left,
    .hero-line-right {
      position: absolute;
      width: 1px;
      height: 8rem;
      background: rgba(201, 168, 76, 0.4);
      display: none;
    }

    @media (min-width: 1024px) {
      .hero-line-left, .hero-line-right { display: block; }
    }

    .hero-line-left { top: 25%; left: 2rem; }
    .hero-line-right { bottom: 25%; right: 2rem; }

    .hero-content {
      position: relative;
      z-index: 10;
      text-align: center;
      padding: 0 1rem;
      max-width: 64rem;
    }

    @media (min-width: 640px) {
      .hero-content { padding: 0 1.5rem; }
    }

    .hero-kicker {
      color: #C9A84C;
      font-size: 0.75rem;
      letter-spacing: 0.35em;
      text-transform: uppercase;
      margin-bottom: 1.5rem;
    }

    @media (min-width: 640px) {
      .hero-kicker { font-size: 0.875rem; margin-bottom: 1.75rem; }
    }

    .hero-title {
      font-family: 'Playfair Display', serif;
      font-size: 3rem;
      font-weight: 700;
      color: #F5F0E8;
      letter-spacing: 0.05em;
      margin-bottom: 1.5rem;
      line-height: 1.1;
    }

    @media (min-width: 640px) {
      .hero-title { font-size: 4.5rem; }
    }

    @media (min-width: 1024px) {
      .hero-title { font-size: 6rem; }
    }

    .hero-subtitle {
      font-family: 'Inter', sans-serif;
      color: rgba(245, 240, 232, 0.8);
      font-size: 1rem;
      max-width: 42rem;
      margin: 0 auto 2.5rem;
      line-height: 1.7;
    }

    @media (min-width: 640px) {
      .hero-subtitle { font-size: 1.125rem; }
    }

    @media (min-width: 1024px) {
      .hero-subtitle { font-size: 1.25rem; }
    }

    .hero-btn {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      background-color: #C9A84C;
      color: #1A0F0A;
      font-weight: 600;
      letter-spacing: 0.05em;
      padding: 1rem 2.5rem;
      border: none;
      cursor: pointer;
      font-size: 1rem;
      transition: all 0.3s;
    }

    .hero-btn:hover {
      background-color: #B8963E;
      transform: translateY(-1px);
    }

    .hero-btn svg {
      width: 1rem;
      height: 1rem;
      transition: transform 0.3s;
    }

    .hero-btn:hover svg { transform: translateX(4px); }

    .hero-scroll {
      position: absolute;
      bottom: 2rem;
      left: 50%;
      transform: translateX(-50%);
      animation: bounce 2s infinite;
    }

    .hero-scroll svg {
      width: 1.5rem;
      height: 1.5rem;
      color: rgba(201, 168, 76, 0.6);
    }

    @keyframes bounce {
      0%, 100% { transform: translateX(-50%) translateY(0); }
      50% { transform: translateX(-50%) translateY(-8px); }
    }

    /* ══════════════════════════════════════════
       ABOUT
    ══════════════════════════════════════════ */
    .about { background-color: #F5F0E8; }

    .about-grid {
      display: grid;
      gap: 3rem;
      align-items: center;
      margin-bottom: 5rem;
    }

    @media (min-width: 1024px) {
      .about-grid { grid-template-columns: 1fr 1fr; gap: 4rem; }
    }

    .about-image-wrapper { position: relative; }

    .about-image-wrapper img {
      width: 100%;
      height: 25rem;
      object-fit: cover;
    }

    @media (min-width: 640px) {
      .about-image-wrapper img { height: 31.25rem; }
    }

    .about-frame {
      position: absolute;
      bottom: -1rem;
      right: -1rem;
      width: 100%;
      height: 100%;
      border: 2px solid rgba(201, 168, 76, 0.3);
      z-index: -1;
      display: none;
    }

    @media (min-width: 640px) {
      .about-frame { display: block; }
    }

    .about-text h3 {
      font-family: 'Playfair Display', serif;
      font-size: 1.5rem;
      font-weight: 600;
      color: #6B3A2A;
      margin-bottom: 1.5rem;
    }

    @media (min-width: 640px) {
      .about-text h3 { font-size: 1.875rem; }
    }

    .about-text p {
      color: rgba(26, 15, 10, 0.7);
      line-height: 1.75;
      margin-bottom: 1rem;
      font-size: 1rem;
    }

    @media (min-width: 640px) {
      .about-text p { font-size: 1.125rem; }
    }

    .values-grid {
      display: grid;
      gap: 2rem;
    }

    @media (min-width: 640px) {
      .values-grid { grid-template-columns: 1fr 1fr 1fr; }
    }

    .value-card {
      text-align: center;
      padding: 1.5rem;
      background: #FFFCF7;
      border: 1px solid rgba(212, 200, 184, 0.5);
      transition: all 0.3s;
    }

    @media (min-width: 640px) {
      .value-card { padding: 2rem; }
    }

    .value-card:hover { border-color: rgba(201, 168, 76, 0.5); }

    .value-icon {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 3.5rem;
      height: 3.5rem;
      border-radius: 50%;
      background: rgba(107, 58, 42, 0.1);
      color: #6B3A2A;
      margin-bottom: 1.25rem;
      transition: all 0.3s;
    }

    .value-card:hover .value-icon {
      background: #6B3A2A;
      color: #F5F0E8;
    }

    .value-icon svg { width: 1.5rem; height: 1.5rem; }

    .value-card h4 {
      font-family: 'Playfair Display', serif;
      font-size: 1.125rem;
      font-weight: 600;
      color: #1A0F0A;
      margin-bottom: 0.75rem;
    }

    .value-card p {
      font-size: 0.875rem;
      color: rgba(26, 15, 10, 0.6);
      line-height: 1.7;
    }

    /* ══════════════════════════════════════════
       PRODUCTS
    ══════════════════════════════════════════ */
    .products { background-color: #FFFCF7; }

    .products-grid {
      display: grid;
      gap: 2rem;
    }

    @media (min-width: 640px) {
      .products-grid { grid-template-columns: 1fr 1fr; }
    }

    @media (min-width: 1024px) {
      .products-grid { grid-template-columns: 1fr 1fr 1fr; }
    }

    .product-card {
      background: #F5F0E8;
      border: 1px solid rgba(212, 200, 184, 0.5);
      overflow: hidden;
      transition: all 0.5s;
    }

    .product-card:hover { box-shadow: 0 10px 25px rgba(0,0,0,0.1); }

    .product-image {
      position: relative;
      overflow: hidden;
    }

    .product-image img {
      width: 100%;
      height: 20rem;
      object-fit: cover;
      transition: transform 0.7s;
    }

    .product-card:hover .product-image img { transform: scale(1.05); }

    .product-tag {
      position: absolute;
      top: 1rem;
      left: 1rem;
      background: #6B3A2A;
      color: #F5F0E8;
      padding: 0.25rem 0.75rem;
      font-size: 0.75rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
    }

    .product-body {
      padding: 1.5rem;
    }

    .product-body h3 {
      font-family: 'Playfair Display', serif;
      font-size: 1.25rem;
      font-weight: 600;
      color: #6B3A2A;
      margin-bottom: 0.5rem;
    }

    .product-body p {
      font-size: 0.875rem;
      color: rgba(26, 15, 10, 0.6);
      line-height: 1.7;
      margin-bottom: 1.25rem;
    }

    .product-btn {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.5rem;
      width: 100%;
      padding: 0.5rem 1rem;
      border: 1px solid #6B3A2A;
      background: transparent;
      color: #6B3A2A;
      font-size: 0.875rem;
      letter-spacing: 0.05em;
      cursor: pointer;
      transition: all 0.3s;
    }

    .product-btn:hover {
      background: #6B3A2A;
      color: #F5F0E8;
    }

    .product-btn svg { width: 1rem; height: 1rem; }

    /* Boutique Experience */
    .boutique-grid {
      display: grid;
      gap: 3rem;
      align-items: center;
      margin-top: 5rem;
    }

    @media (min-width: 1024px) {
      .boutique-grid { grid-template-columns: 1fr 1fr; gap: 3rem; }
    }

    .boutique-text { order: 2; }
    .boutique-image { order: 1; }

    @media (min-width: 1024px) {
      .boutique-text { order: 1; }
      .boutique-image { order: 2; }
    }

    .boutique-image img {
      width: 100%;
      height: 22rem;
      object-fit: cover;
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
    }

    @media (min-width: 640px) {
      .boutique-image img { height: 28rem; }
    }

    .boutique-badge {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      background: rgba(201, 168, 76, 0.1);
      padding: 0.5rem 1rem;
      margin-bottom: 1rem;
    }

    .boutique-badge svg { width: 1rem; height: 1rem; color: #C9A84C; }

    .boutique-badge span {
      font-size: 0.75rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: #C9A84C;
      font-weight: 500;
    }

    .boutique-text h3 {
      font-family: 'Playfair Display', serif;
      font-size: 1.5rem;
      font-weight: 600;
      color: #6B3A2A;
      margin-bottom: 1rem;
    }

    @media (min-width: 640px) {
      .boutique-text h3 { font-size: 1.875rem; }
    }

    .boutique-text p {
      color: rgba(26, 15, 10, 0.7);
      line-height: 1.75;
      margin-bottom: 1rem;
    }

    .boutique-features {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      padding-top: 0.5rem;
    }

    .boutique-feature {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      font-size: 0.875rem;
      color: rgba(26, 15, 10, 0.6);
    }

    .boutique-feature svg { width: 1rem; height: 1rem; color: #C9A84C; }

    /* ══════════════════════════════════════════
       CONTACT
    ══════════════════════════════════════════ */
    .contact { background-color: #F5F0E8; }

    .contact-grid {
      display: grid;
      gap: 3rem;
    }

    @media (min-width: 1024px) {
      .contact-grid { grid-template-columns: 1fr 1fr; gap: 4rem; }
    }

    .contact-form-card {
      background: #FFFCF7;
      border: 1px solid rgba(212, 200, 184, 0.5);
      box-shadow: 0 4px 12px rgba(0,0,0,0.08);
    }

    .contact-form-header {
      padding: 1.5rem 1.5rem 0;
    }

    @media (min-width: 640px) {
      .contact-form-header { padding: 1.5rem 2rem 0; }
    }

    .contact-form-header h3 {
      font-family: 'Playfair Display', serif;
      font-size: 1.25rem;
      color: #6B3A2A;
      margin-bottom: 0.25rem;
    }

    .contact-form-header p {
      font-size: 0.875rem;
      color: rgba(26, 15, 10, 0.6);
    }

    .contact-form-body {
      padding: 1.5rem;
    }

    @media (min-width: 640px) {
      .contact-form-body { padding: 1.5rem 2rem 2rem; }
    }

    .form-group {
      margin-bottom: 1.25rem;
    }

    .form-group label {
      display: block;
      font-size: 0.875rem;
      font-weight: 500;
      color: rgba(26, 15, 10, 0.8);
      margin-bottom: 0.5rem;
    }

    .form-group input,
    .form-group textarea {
      width: 100%;
      padding: 0.5rem 0.75rem;
      border: 1px solid #D4C8B8;
      background: transparent;
      font-size: 0.875rem;
      transition: all 0.3s;
      outline: none;
    }

    @media (min-width: 640px) {
      .form-group input, .form-group textarea { font-size: 1rem; }
    }

    .form-group input:focus,
    .form-group textarea:focus {
      border-color: #6B3A2A;
      box-shadow: 0 0 0 3px rgba(107, 58, 42, 0.15);
    }

    .form-group textarea {
      min-height: 7rem;
      resize: none;
    }

    .form-submit {
      width: 100%;
      padding: 1.25rem;
      background: #6B3A2A;
      color: #F5F0E8;
      border: none;
      font-weight: 500;
      letter-spacing: 0.05em;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.5rem;
      transition: background 0.3s;
      font-size: 1rem;
    }

    .form-submit:hover { background: #4A2518; }

    .form-submit:disabled { opacity: 0.7; cursor: not-allowed; }

    .form-submit svg { width: 1rem; height: 1rem; }

    .form-success {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      color: #15803d;
      font-size: 0.875rem;
      margin-top: 0.75rem;
    }

    .form-success svg { width: 1rem; height: 1rem; }

    .form-error {
      color: #dc2626;
      font-size: 0.875rem;
      margin-top: 0.75rem;
    }

    /* Contact Info */
    .contact-info h3 {
      font-family: 'Playfair Display', serif;
      font-size: 1.5rem;
      font-weight: 600;
      color: #6B3A2A;
      margin-bottom: 1.5rem;
    }

    .contact-item {
      display: flex;
      align-items: flex-start;
      gap: 1rem;
      margin-bottom: 1.25rem;
    }

    .contact-item-icon {
      width: 2.5rem;
      height: 2.5rem;
      border-radius: 50%;
      background: rgba(107, 58, 42, 0.1);
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      color: #6B3A2A;
    }

    .contact-item-icon svg { width: 1.25rem; height: 1.25rem; }

    .contact-item-label {
      font-weight: 500;
      color: #1A0F0A;
      font-size: 0.9375rem;
    }

    .contact-item-value {
      font-size: 0.875rem;
      color: rgba(26, 15, 10, 0.6);
    }

    /* Social */
    .social-title {
      font-family: 'Playfair Display', serif;
      font-size: 1.125rem;
      font-weight: 600;
      color: #6B3A2A;
      margin-bottom: 1rem;
      margin-top: 2rem;
    }

    .social-links {
      display: flex;
      gap: 0.75rem;
    }

    .social-link {
      width: 2.75rem;
      height: 2.75rem;
      border-radius: 50%;
      border: 1px solid #D4C8B8;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #6B3A2A;
      transition: all 0.3s;
    }

    .social-link:hover {
      background: #6B3A2A;
      color: #F5F0E8;
      border-color: #6B3A2A;
    }

    .social-link svg { width: 1.25rem; height: 1.25rem; }

    /* Ethical Promise */
    .ethical-promise {
      background: #6B3A2A;
      padding: 1.5rem;
      color: #F5F0E8;
      margin-top: 2rem;
    }

    @media (min-width: 640px) {
      .ethical-promise { padding: 2rem; }
    }

    .ethical-promise-header {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      margin-bottom: 0.75rem;
    }

    .ethical-promise-header svg { width: 1.25rem; height: 1.25rem; color: #C9A84C; }

    .ethical-promise-header span {
      font-size: 0.75rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: #C9A84C;
    }

    .ethical-promise p {
      font-size: 0.875rem;
      line-height: 1.75;
      color: rgba(245, 240, 232, 0.8);
    }

    /* ══════════════════════════════════════════
       FOOTER
    ══════════════════════════════════════════ */
    .footer {
      background: #1A0F0A;
      color: #F5F0E8;
      padding: 3rem 0;
    }

    .footer-grid {
      display: grid;
      gap: 2rem;
      margin-bottom: 2.5rem;
    }

    @media (min-width: 640px) {
      .footer-grid { grid-template-columns: 1fr 1fr; }
    }

    @media (min-width: 1024px) {
      .footer-grid { grid-template-columns: 1fr 1fr 1fr 1fr; }
    }

    .footer-brand-name {
      font-family: 'Playfair Display', serif;
      font-size: 1.5rem;
      font-weight: 700;
      letter-spacing: 0.15em;
      margin-bottom: 1rem;
    }

    .footer-brand p {
      font-size: 0.875rem;
      color: rgba(245, 240, 232, 0.6);
      line-height: 1.7;
    }

    .footer-col-title {
      font-size: 0.75rem;
      font-weight: 600;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: #C9A84C;
      margin-bottom: 1rem;
    }

    .footer-col ul li {
      margin-bottom: 0.5rem;
    }

    .footer-col ul li a {
      font-size: 0.875rem;
      color: rgba(245, 240, 232, 0.6);
      transition: color 0.3s;
    }

    .footer-col ul li a:hover { color: #C9A84C; }

    .footer-col ul li span {
      font-size: 0.875rem;
      color: rgba(245, 240, 232, 0.6);
    }

    .footer-divider {
      border-top: 1px solid rgba(245, 240, 232, 0.1);
      padding-top: 1.5rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0.5rem;
    }

    @media (min-width: 640px) {
      .footer-divider { flex-direction: row; justify-content: space-between; }
    }

    .footer-divider p {
      font-size: 0.75rem;
      color: rgba(245, 240, 232, 0.4);
    }

    /* ══════════════════════════════════════════
       LOADING SPINNER
    ══════════════════════════════════════════ */
    @keyframes spin {
      to { transform: rotate(360deg); }
    }

    .spinner {
      animation: spin 1s linear infinite;
    }
  </style>
</head>
<body>

  <!-- ═══════ NAVBAR ═══════ -->
  <nav class="navbar" id="navbar">
    <div class="navbar-inner">
      <a href="#inicio" class="nav-logo">ARAZÁ</a>
      <div class="nav-links">
        <a href="#inicio">Inicio</a>
        <a href="#nosotros">Nosotros</a>
        <a href="#productos">Productos</a>
        <a href="#contacto">Contacto</a>
        <a href="#contacto" class="nav-cta">Contáctanos</a>
      </div>
      <button class="mobile-toggle" id="mobileToggle" aria-label="Abrir menú">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16"/>
        </svg>
      </button>
    </div>
    <div class="mobile-menu" id="mobileMenu">
      <a href="#inicio">Inicio</a>
      <a href="#nosotros">Nosotros</a>
      <a href="#productos">Productos</a>
      <a href="#contacto">Contacto</a>
      <a href="#contacto" class="nav-cta-mobile">Contáctanos</a>
    </div>
  </nav>

  <!-- ═══════ HERO ═══════ -->
  <section id="inicio" class="hero">
    <div class="hero-bg">
      <img src="/images/hero.png" alt="Arazá - Moda artesanal de lujo">
      <div class="hero-overlay"></div>
    </div>
    <div class="hero-line-left"></div>
    <div class="hero-line-right"></div>
    <div class="hero-content">
      <p class="hero-kicker">Moda artesanal de lujo</p>
      <h1 class="hero-title">ARAZÁ</h1>
      <p class="hero-subtitle">Prendas exclusivas que cuentan historias. Diseño de autor elaborado por comunidades artesanas colombianas bajo un modelo de comercio ético, transparencia y pago justo.</p>
      <a href="#productos" class="hero-btn">
        Descubre la Colección
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M13 7l5 5m0 0l-5 5m5-5H6"/></svg>
      </a>
    </div>
    <div class="hero-scroll">
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M19 9l-7 7-7-7"/></svg>
    </div>
  </section>

  <!-- ═══════ SOBRE NOSOTROS ═══════ -->
  <section id="nosotros" class="about section-padding">
    <div class="container">
      <div class="text-center" style="margin-bottom: 4rem;">
        <p class="section-kicker">Nuestra esencia</p>
        <h2 class="section-title">Sobre Nosotros</h2>
        <div class="section-divider"></div>
      </div>

      <div class="about-grid">
        <div class="about-image-wrapper">
          <img src="/images/about.png" alt="Artesanos colombianos tejiendo">
          <div class="about-frame"></div>
        </div>
        <div class="about-text">
          <h3>Un compromiso con la artesanía y la comunidad</h3>
          <p>Arazá apuesta por moda artesanal con comunidades colombianas, garantizando pago justo y trazabilidad en cada prenda. Nuestro modelo de producción sostenible y limitado promueve el slow fashion, alejándonos por completo de la producción masiva.</p>
          <p>Trabajamos de la mano con la comunidad guayo, elaborando prendas exclusivas en ediciones limitadas que utilizan insumos de alta calidad. Cada pieza es una obra de arte que lleva consigo la historia y el talento de nuestros artesanos.</p>
          <p>Más allá de vender ropa, creamos una estrategia de valor emocional: las personas cuentan una historia a través de sus prendas. En nuestro espacio boutique, el diseño exclusivo se integra con un espacio creativo único.</p>
        </div>
      </div>

      <div class="values-grid">
        <div class="value-card">
          <div class="value-icon">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"/></svg>
          </div>
          <h4>Slow Fashion</h4>
          <p>Producción sostenible y limitada que promueve la durabilidad y el uso de insumos de alta calidad.</p>
        </div>
        <div class="value-card">
          <div class="value-icon">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"/></svg>
          </div>
          <h4>Comercio Ético</h4>
          <p>Pago justo y trazabilidad mediante QR/NFC en cada prenda. Transparencia total en nuestra cadena de valor.</p>
        </div>
        <div class="value-card">
          <div class="value-icon">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"/></svg>
          </div>
          <h4>Valor Emocional</h4>
          <p>Cada prenda cuenta una historia. Más que ropa, una experiencia que conecta con la esencia artesanal.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══════ PRODUCTOS ═══════ -->
  <section id="productos" class="products section-padding">
    <div class="container">
      <div class="text-center" style="margin-bottom: 4rem;">
        <p class="section-kicker">Nuestra oferta</p>
        <h2 class="section-title">Productos y Servicios</h2>
        <div class="section-divider"></div>
        <p class="section-subtitle">Moda de autor en ediciones limitadas que promueve la sostenibilidad, la durabilidad y el uso de insumos de alta calidad.</p>
      </div>

      <div class="products-grid">
        <div class="product-card">
          <div class="product-image">
            <img src="/images/product1.png" alt="Colección Raíces">
            <span class="product-tag">Edición Limitada</span>
          </div>
          <div class="product-body">
            <h3>Colección Raíces</h3>
            <p>Prendas que honran las raíces artesanales de la comunidad guayo. Tejidos a mano con fibras naturales y acabados de alta costura.</p>
            <button class="product-btn">
              Ver Detalles
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M13 7l5 5m0 0l-5 5m5-5H6"/></svg>
            </button>
          </div>
        </div>
        <div class="product-card">
          <div class="product-image">
            <img src="/images/product2.png" alt="Colección Territorio">
            <span class="product-tag">Exclusivo</span>
          </div>
          <div class="product-body">
            <h3>Colección Territorio</h3>
            <p>Diseños inspirados en los paisajes colombianos. Cada pieza refleja la riqueza cultural y la diversidad de nuestra tierra.</p>
            <button class="product-btn">
              Ver Detalles
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M13 7l5 5m0 0l-5 5m5-5H6"/></svg>
            </button>
          </div>
        </div>
        <div class="product-card">
          <div class="product-image">
            <img src="/images/product3.png" alt="Accesorios de Autor">
            <span class="product-tag">Hecho a Mano</span>
          </div>
          <div class="product-body">
            <h3>Accesorios de Autor</h3>
            <p>Complementos artesanales con detalles en oro y técnicas ancestrales de tejido. Piezas únicas que completan tu estilo.</p>
            <button class="product-btn">
              Ver Detalles
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M13 7l5 5m0 0l-5 5m5-5H6"/></svg>
            </button>
          </div>
        </div>
      </div>

      <!-- Boutique Experience -->
      <div class="boutique-grid">
        <div class="boutique-text">
          <div class="boutique-badge">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M5 3l14 9-14 9V3z"/></svg>
            <span>Experiencia Boutique</span>
          </div>
          <h3>Un espacio donde el diseño cobra vida</h3>
          <p>Nuestra tienda boutique integra el diseño exclusivo con un espacio creativo único. Cada visita es una experiencia sensorial donde puedes apreciar de cerca el arte artesanal, conocer la historia detrás de cada prenda y ser parte de nuestra comunidad.</p>
          <div class="boutique-features">
            <div class="boutique-feature">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"/></svg>
              <span>Trazabilidad QR/NFC</span>
            </div>
            <div class="boutique-feature">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"/></svg>
              <span>Ediciones Limitadas</span>
            </div>
            <div class="boutique-feature">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"/></svg>
              <span>Insumos Sostenibles</span>
            </div>
          </div>
        </div>
        <div class="boutique-image">
          <img src="/images/boutique.png" alt="Tienda boutique Arazá">
        </div>
      </div>
    </div>
  </section>

  <!-- ═══════ CONTACTO ═══════ -->
  <section id="contacto" class="contact section-padding">
    <div class="container">
      <div class="text-center" style="margin-bottom: 4rem;">
        <p class="section-kicker">Hablemos</p>
        <h2 class="section-title">Contacto</h2>
        <div class="section-divider"></div>
        <p class="section-subtitle">¿Quieres conocer más sobre nuestras colecciones o visitar nuestra boutique? Estamos aquí para ti.</p>
      </div>

      <div class="contact-grid">
        <!-- Form -->
        <div class="contact-form-card">
          <div class="contact-form-header">
            <h3>Envíanos un mensaje</h3>
            <p>Completa el formulario y te responderemos lo antes posible.</p>
          </div>
          <div class="contact-form-body">
            <form id="contactForm">
              <div class="form-group">
                <label for="name">Nombre completo</label>
                <input type="text" id="name" name="name" placeholder="Tu nombre" required>
              </div>
              <div class="form-group">
                <label for="email">Correo electrónico</label>
                <input type="email" id="email" name="email" placeholder="tu@email.com" required>
              </div>
              <div class="form-group">
                <label for="message">Mensaje</label>
                <textarea id="message" name="message" placeholder="Cuéntanos en qué podemos ayudarte..." rows="5" required></textarea>
              </div>
              <button type="submit" class="form-submit" id="submitBtn">
                <span id="submitText">Enviar Mensaje</span>
                <svg id="submitArrow" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M13 7l5 5m0 0l-5 5m5-5H6"/></svg>
                <svg id="submitSpinner" class="spinner" style="display:none;" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M4 4v5h.582m15.356 2A8.001 8.001 0 004.582 9m0 0H9m11 11v-5h-.581m0 0a8.003 8.003 0 01-15.357-2m15.357 2H15"/></svg>
              </button>
              <div id="formSuccess" class="form-success" style="display:none;">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
                <span>Mensaje enviado con éxito. Te contactaremos pronto.</span>
              </div>
              <div id="formError" class="form-error" style="display:none;">
                Hubo un error al enviar. Por favor, intenta de nuevo.
              </div>
            </form>
          </div>
        </div>

        <!-- Info -->
        <div class="contact-info">
          <h3>Información de Contacto</h3>

          <div class="contact-item">
            <div class="contact-item-icon">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/><path stroke-linecap="round" stroke-linejoin="round" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/></svg>
            </div>
            <div>
              <div class="contact-item-label">Dirección</div>
              <div class="contact-item-value">Boutique Arazá, Centro Histórico<br>Bogotá, Colombia</div>
            </div>
          </div>

          <div class="contact-item">
            <div class="contact-item-icon">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/></svg>
            </div>
            <div>
              <div class="contact-item-label">Teléfono</div>
              <div class="contact-item-value">+57 601 234 5678</div>
            </div>
          </div>

          <div class="contact-item">
            <div class="contact-item-icon">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
            </div>
            <div>
              <div class="contact-item-label">Correo Electrónico</div>
              <div class="contact-item-value">hola@araza.co</div>
            </div>
          </div>

          <h4 class="social-title">Síguenos</h4>
          <div class="social-links">
            <a href="#" class="social-link" aria-label="Instagram">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="2" width="20" height="20" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1112.63 8 4 4 0 0116 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg>
            </a>
            <a href="#" class="social-link" aria-label="Facebook">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z"/></svg>
            </a>
            <a href="#" class="social-link" aria-label="Twitter">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"/></svg>
            </a>
          </div>

          <div class="ethical-promise">
            <div class="ethical-promise-header">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"/></svg>
              <span>Promesa Ética</span>
            </div>
            <p>Arazá comunica con transparencia el origen, proceso y comunidades detrás de cada prenda, promoviendo consumo consciente, trabajo justo y menor impacto ambiental.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══════ FOOTER ═══════ -->
  <footer class="footer">
    <div class="container">
      <div class="footer-grid">
        <div class="footer-brand">
          <div class="footer-brand-name">ARAZÁ</div>
          <p>Moda artesanal de lujo. Prendas exclusivas que cuentan historias, elaboradas con comercio ético y amor por la artesanía colombiana.</p>
        </div>
        <div class="footer-col">
          <div class="footer-col-title">Navegación</div>
          <ul>
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#nosotros">Nosotros</a></li>
            <li><a href="#productos">Productos</a></li>
            <li><a href="#contacto">Contacto</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <div class="footer-col-title">Valores</div>
          <ul>
            <li><span>Slow Fashion</span></li>
            <li><span>Comercio Ético</span></li>
            <li><span>Pago Justo</span></li>
            <li><span>Sostenibilidad</span></li>
          </ul>
        </div>
        <div class="footer-col">
          <div class="footer-col-title">Contacto</div>
          <ul>
            <li><span>hola@araza.co</span></li>
            <li><span>+57 601 234 5678</span></li>
            <li><span>Bogotá, Colombia</span></li>
          </ul>
        </div>
      </div>
      <div class="footer-divider">
        <p>&copy; 2025 Arazá. Todos los derechos reservados.</p>
        <p>Moda artesanal con propósito</p>
      </div>
    </div>
  </footer>

  <!-- ═══════ JAVASCRIPT ═══════ -->
  <script>
    // ── Navbar scroll effect ──
    const navbar = document.getElementById('navbar');
    window.addEventListener('scroll', function() {
      if (window.scrollY > 40) {
        navbar.classList.add('scrolled');
      } else {
        navbar.classList.remove('scrolled');
      }
    }, { passive: true });

    // ── Mobile menu toggle ──
    const mobileToggle = document.getElementById('mobileToggle');
    const mobileMenu = document.getElementById('mobileMenu');
    let menuOpen = false;

    mobileToggle.addEventListener('click', function() {
      menuOpen = !menuOpen;
      mobileMenu.classList.toggle('open', menuOpen);
      mobileToggle.setAttribute('aria-label', menuOpen ? 'Cerrar menú' : 'Abrir menú');
      // Toggle icon
      mobileToggle.innerHTML = menuOpen
        ? '<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"/></svg>'
        : '<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16"/></svg>';
    });

    // Close mobile menu on link click
    mobileMenu.querySelectorAll('a').forEach(function(link) {
      link.addEventListener('click', function() {
        menuOpen = false;
        mobileMenu.classList.remove('open');
        mobileToggle.innerHTML = '<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16"/></svg>';
        mobileToggle.setAttribute('aria-label', 'Abrir menú');
      });
    });

    // ── Contact Form ──
    const contactForm = document.getElementById('contactForm');
    const submitBtn = document.getElementById('submitBtn');
    const submitText = document.getElementById('submitText');
    const submitArrow = document.getElementById('submitArrow');
    const submitSpinner = document.getElementById('submitSpinner');
    const formSuccess = document.getElementById('formSuccess');
    const formError = document.getElementById('formError');

    contactForm.addEventListener('submit', function(e) {
      e.preventDefault();

      // Get form data
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const message = document.getElementById('message').value.trim();

      // Basic validation
      if (!name || !email || !message) return;

      // Show loading state
      submitBtn.disabled = true;
      submitText.textContent = 'Enviando...';
      submitArrow.style.display = 'none';
      submitSpinner.style.display = 'block';
      formSuccess.style.display = 'none';
      formError.style.display = 'none';

      // Simulate API call
      fetch('/api/contact', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ name: name, email: email, message: message })
      })
      .then(function(res) {
        if (!res.ok) throw new Error('Error');
        return res.json();
      })
      .then(function() {
        // Success
        formSuccess.style.display = 'flex';
        contactForm.reset();
        setTimeout(function() { formSuccess.style.display = 'none'; }, 4000);
      })
      .catch(function() {
        // Error
        formError.style.display = 'block';
        setTimeout(function() { formError.style.display = 'none'; }, 4000);
      })
      .finally(function() {
        // Reset button
        submitBtn.disabled = false;
        submitText.textContent = 'Enviar Mensaje';
        submitArrow.style.display = 'block';
        submitSpinner.style.display = 'none';
      });
    });

    // ── Smooth scroll for anchor links ──
    document.querySelectorAll('a[href^="#"]').forEach(function(anchor) {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          target.scrollIntoView({ behavior: 'smooth', block: 'start' });
        }
      });
    });
  </script>
</body>
</html>
