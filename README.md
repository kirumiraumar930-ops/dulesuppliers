<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Dule Suppliers (U) Ltd — Industrial Refrigeration & Compressed Air</title>
  <link href="https://fonts.googleapis.com/css2?family=Barlow:wght@400;500;600&family=Barlow+Condensed:wght@700;800&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --navy: #0A1F44;
      --navy-mid: #122860;
      --gold: #C9A84C;
      --gold-light: #F0D080;
      --gold-pale: #FDF6E3;
      --white: #ffffff;
      --gray: #F4F6F9;
      --text: #1A1A2E;
      --text-light: #5A6270;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'Barlow', sans-serif;
      color: var(--text);
      background: var(--white);
      overflow-x: hidden;
    }

    /* ── NAV ── */
    nav {
      position: fixed; top: 0; width: 100%; z-index: 100;
      background: rgba(10, 31, 68, 0.97);
      backdrop-filter: blur(8px);
      display: flex; align-items: center; justify-content: space-between;
      padding: 0 5%;
      height: 64px;
      border-bottom: 2px solid var(--gold);
    }
    .nav-logo {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 1.3rem; font-weight: 800;
      color: var(--white); letter-spacing: 0.04em;
      text-decoration: none;
    }
    .nav-logo span { color: var(--gold); }
    .nav-links { display: flex; gap: 2rem; list-style: none; }
    .nav-links a {
      color: rgba(255,255,255,0.8); text-decoration: none;
      font-size: 0.9rem; font-weight: 500; letter-spacing: 0.05em;
      text-transform: uppercase;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--gold); }
    .nav-cta {
      background: var(--gold); color: var(--navy) !important;
      padding: 0.4rem 1.1rem; border-radius: 2px;
      font-weight: 600 !important;
    }
    .nav-cta:hover { background: var(--gold-light) !important; color: var(--navy) !important; }
    .hamburger { display: none; flex-direction: column; gap: 5px; cursor: pointer; }
    .hamburger span { width: 24px; height: 2px; background: var(--white); display: block; }

    /* ── HERO ── */
    #hero {
      min-height: 100vh;
      background: linear-gradient(135deg, var(--navy) 0%, var(--navy-mid) 60%, #1A3A6B 100%);
      display: flex; align-items: center;
      padding: 100px 5% 60px;
      position: relative; overflow: hidden;
    }
    #hero::before {
      content: '';
      position: absolute; top: 0; right: 0;
      width: 55%; height: 100%;
      background: url("data:image/svg+xml,%3Csvg width='600' height='600' viewBox='0 0 600 600' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' stroke='%23C9A84C' stroke-width='0.5' opacity='0.15'%3E%3Ccircle cx='300' cy='300' r='280'/%3E%3Ccircle cx='300' cy='300' r='220'/%3E%3Ccircle cx='300' cy='300' r='160'/%3E%3Ccircle cx='300' cy='300' r='100'/%3E%3Cline x1='20' y1='300' x2='580' y2='300'/%3E%3Cline x1='300' y1='20' x2='300' y2='580'/%3E%3Cline x1='100' y1='100' x2='500' y2='500'/%3E%3Cline x1='500' y1='100' x2='100' y2='500'/%3E%3C/g%3E%3C/svg%3E") center/cover no-repeat;
      opacity: 0.4;
    }
    .hero-content { max-width: 620px; position: relative; z-index: 2; }
    .hero-tag {
      display: inline-block;
      background: var(--gold); color: var(--navy);
      font-size: 0.75rem; font-weight: 700; letter-spacing: 0.12em;
      text-transform: uppercase; padding: 0.3rem 0.8rem;
      margin-bottom: 1.5rem;
    }
    .hero-title {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: clamp(2.8rem, 6vw, 4.5rem);
      font-weight: 800; line-height: 1.0;
      color: var(--white);
      text-transform: uppercase;
      margin-bottom: 1.2rem;
      letter-spacing: 0.02em;
    }
    .hero-title em { color: var(--gold); font-style: normal; display: block; }
    .hero-sub {
      font-size: 1.1rem; color: rgba(255,255,255,0.75);
      line-height: 1.7; margin-bottom: 2.5rem; max-width: 480px;
    }
    .hero-btns { display: flex; gap: 1rem; flex-wrap: wrap; }
    .btn-primary {
      background: var(--gold); color: var(--navy);
      padding: 0.85rem 2rem; font-weight: 700;
      font-size: 0.95rem; text-decoration: none;
      letter-spacing: 0.06em; text-transform: uppercase;
      transition: background 0.2s, transform 0.2s;
      border-radius: 2px;
    }
    .btn-primary:hover { background: var(--gold-light); transform: translateY(-2px); }
    .btn-outline {
      border: 2px solid rgba(255,255,255,0.4); color: var(--white);
      padding: 0.85rem 2rem; font-weight: 600;
      font-size: 0.95rem; text-decoration: none;
      letter-spacing: 0.06em; text-transform: uppercase;
      transition: border-color 0.2s, transform 0.2s;
      border-radius: 2px;
    }
    .btn-outline:hover { border-color: var(--gold); color: var(--gold); transform: translateY(-2px); }

    .hero-stats {
      display: flex; gap: 2.5rem; margin-top: 3.5rem;
      padding-top: 2rem;
      border-top: 1px solid rgba(201,168,76,0.3);
    }
    .stat-num {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 2rem; font-weight: 800; color: var(--gold);
    }
    .stat-label { font-size: 0.8rem; color: rgba(255,255,255,0.6); text-transform: uppercase; letter-spacing: 0.08em; }

    /* ── SECTIONS ── */
    section { padding: 80px 5%; }
    .section-tag {
      font-size: 0.75rem; font-weight: 700; letter-spacing: 0.15em;
      text-transform: uppercase; color: var(--gold);
      margin-bottom: 0.6rem;
    }
    .section-title {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: clamp(2rem, 4vw, 2.8rem);
      font-weight: 800; text-transform: uppercase;
      color: var(--navy); line-height: 1.1;
      margin-bottom: 1rem;
    }
    .section-sub {
      font-size: 1rem; color: var(--text-light);
      line-height: 1.7; max-width: 520px;
    }

    /* ── SERVICES ── */
    #services { background: var(--gray); }
    .services-header { margin-bottom: 3rem; }
    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 1.5rem;
    }
    .service-card {
      background: var(--white);
      padding: 2rem;
      border-top: 3px solid var(--gold);
      transition: transform 0.2s, box-shadow 0.2s;
      position: relative;
    }
    .service-card:hover { transform: translateY(-4px); box-shadow: 0 12px 32px rgba(10,31,68,0.12); }
    .service-icon {
      font-size: 2.2rem; margin-bottom: 1rem;
    }
    .service-name {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 1.25rem; font-weight: 700;
      color: var(--navy); text-transform: uppercase;
      margin-bottom: 0.6rem; letter-spacing: 0.03em;
    }
    .service-desc { font-size: 0.92rem; color: var(--text-light); line-height: 1.65; }

    /* ── ABOUT ── */
    #about {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 4rem; align-items: center;
    }
    .about-visual {
      background: var(--navy);
      padding: 3rem;
      position: relative;
    }
    .about-visual::before {
      content: '';
      position: absolute; top: -8px; left: -8px;
      width: 100%; height: 100%;
      border: 2px solid var(--gold);
      z-index: -1;
    }
    .about-quote {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 1.6rem; font-weight: 700;
      color: var(--white); line-height: 1.3;
      text-transform: uppercase;
    }
    .about-quote span { color: var(--gold); }
    .about-divider {
      width: 40px; height: 3px;
      background: var(--gold); margin: 1.5rem 0;
    }
    .about-sub-text { color: rgba(255,255,255,0.65); font-size: 0.9rem; line-height: 1.7; }
    .about-points { list-style: none; margin-top: 1.5rem; }
    .about-points li {
      padding: 0.6rem 0;
      border-bottom: 1px solid rgba(255,255,255,0.1);
      color: rgba(255,255,255,0.8);
      font-size: 0.9rem;
      display: flex; align-items: center; gap: 0.6rem;
    }
    .about-points li::before { content: '▸'; color: var(--gold); }

    /* ── CLIENTS ── */
    #clients { background: var(--navy); text-align: center; }
    #clients .section-title { color: var(--white); }
    #clients .section-tag { color: var(--gold); }
    #clients .section-sub { color: rgba(255,255,255,0.6); margin: 0 auto 3rem; }
    .clients-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 1px;
      background: rgba(201,168,76,0.2);
      border: 1px solid rgba(201,168,76,0.2);
      margin-top: 3rem;
    }
    .client-card {
      background: rgba(255,255,255,0.04);
      padding: 2rem 1.5rem;
      text-align: center;
      transition: background 0.2s;
    }
    .client-card:hover { background: rgba(201,168,76,0.1); }
    .client-name {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 1.1rem; font-weight: 700;
      color: var(--white); text-transform: uppercase;
      letter-spacing: 0.05em; margin-bottom: 0.3rem;
    }
    .client-loc { font-size: 0.8rem; color: var(--gold); letter-spacing: 0.08em; }

    /* ── WHY US ── */
    #why { background: var(--gold-pale); }
    .why-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 2rem; margin-top: 3rem;
    }
    .why-item { display: flex; gap: 1rem; align-items: flex-start; }
    .why-icon {
      width: 44px; height: 44px; flex-shrink: 0;
      background: var(--navy);
      display: flex; align-items: center; justify-content: center;
      font-size: 1.2rem;
    }
    .why-title {
      font-weight: 700; font-size: 0.95rem;
      color: var(--navy); margin-bottom: 0.3rem;
      text-transform: uppercase; letter-spacing: 0.04em;
    }
    .why-desc { font-size: 0.88rem; color: var(--text-light); line-height: 1.6; }

    /* ── CONTACT ── */
    #contact {
      background: var(--navy);
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 4rem; align-items: start;
    }
    #contact .section-title { color: var(--white); }
    #contact .section-tag { color: var(--gold); }
    #contact .section-sub { color: rgba(255,255,255,0.6); }
    .contact-items { margin-top: 2rem; display: flex; flex-direction: column; gap: 1.2rem; }
    .contact-item { display: flex; align-items: flex-start; gap: 1rem; }
    .contact-icon {
      width: 40px; height: 40px; flex-shrink: 0;
      background: rgba(201,168,76,0.15);
      border: 1px solid rgba(201,168,76,0.3);
      display: flex; align-items: center; justify-content: center;
      font-size: 1rem;
    }
    .contact-label { font-size: 0.75rem; color: var(--gold); text-transform: uppercase; letter-spacing: 0.1em; margin-bottom: 0.2rem; }
    .contact-value { color: var(--white); font-size: 0.95rem; }
    .contact-value a { color: var(--white); text-decoration: none; }
    .contact-value a:hover { color: var(--gold); }

    .contact-form-area {
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(201,168,76,0.2);
      padding: 2rem;
    }
    .form-title {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 1.3rem; font-weight: 700;
      color: var(--white); text-transform: uppercase;
      margin-bottom: 1.5rem; letter-spacing: 0.05em;
    }
    .form-group { margin-bottom: 1rem; }
    .form-group label {
      display: block; font-size: 0.78rem; font-weight: 600;
      color: var(--gold); text-transform: uppercase;
      letter-spacing: 0.08em; margin-bottom: 0.4rem;
    }
    .form-group input, .form-group textarea, .form-group select {
      width: 100%; background: rgba(255,255,255,0.06);
      border: 1px solid rgba(255,255,255,0.15);
      color: var(--white); padding: 0.7rem 0.9rem;
      font-family: 'Barlow', sans-serif; font-size: 0.9rem;
      outline: none; transition: border-color 0.2s;
    }
    .form-group input:focus, .form-group textarea:focus, .form-group select:focus {
      border-color: var(--gold);
    }
    .form-group textarea { resize: vertical; min-height: 90px; }
    .form-group select option { background: var(--navy); }
    .btn-submit {
      width: 100%; background: var(--gold); color: var(--navy);
      border: none; padding: 0.9rem;
      font-family: 'Barlow', sans-serif;
      font-size: 0.95rem; font-weight: 700;
      text-transform: uppercase; letter-spacing: 0.08em;
      cursor: pointer; transition: background 0.2s;
    }
    .btn-submit:hover { background: var(--gold-light); }

    /* ── FOOTER ── */
    footer {
      background: #060F22;
      padding: 2rem 5%;
      display: flex; align-items: center; justify-content: space-between;
      flex-wrap: wrap; gap: 1rem;
      border-top: 2px solid var(--gold);
    }
    .footer-logo {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 1.1rem; font-weight: 800;
      color: var(--white); letter-spacing: 0.04em;
    }
    .footer-logo span { color: var(--gold); }
    .footer-text { font-size: 0.82rem; color: rgba(255,255,255,0.4); }
    .footer-links { display: flex; gap: 1.5rem; }
    .footer-links a {
      font-size: 0.82rem; color: rgba(255,255,255,0.5);
      text-decoration: none; text-transform: uppercase;
      letter-spacing: 0.06em;
    }
    .footer-links a:hover { color: var(--gold); }

    /* ── WHATSAPP FLOAT ── */
    .wa-float {
      position: fixed; bottom: 24px; right: 24px; z-index: 200;
      width: 56px; height: 56px;
      background: #25D366;
      border-radius: 50%;
      display: flex; align-items: center; justify-content: center;
      text-decoration: none; font-size: 1.6rem;
      box-shadow: 0 4px 16px rgba(37,211,102,0.4);
      transition: transform 0.2s;
    }
    .wa-float:hover { transform: scale(1.1); }

    /* ── RESPONSIVE ── */
    @media (max-width: 768px) {
      .nav-links { display: none; }
      .hamburger { display: flex; }
      #about, #contact { grid-template-columns: 1fr; gap: 2rem; }
      .hero-stats { gap: 1.5rem; }
      .about-visual::before { display: none; }
      footer { flex-direction: column; text-align: center; }
      .footer-links { justify-content: center; }
    }
  </style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">DULE <span>SUPPLIERS</span></a>
  <ul class="nav-links">
    <li><a href="#services">Services</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#clients">Clients</a></li>
    <li><a href="#contact" class="nav-cta">Contact Us</a></li>
  </ul>
  <div class="hamburger" onclick="toggleMenu()">
    <span></span><span></span><span></span>
  </div>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-content">
    <div class="hero-tag">Kampala, Uganda</div>
    <h1 class="hero-title">
      Industrial Refrigeration
      <em>&amp; Compressed Air</em>
      Specialists
    </h1>
    <p class="hero-sub">
      Dule Suppliers (U) Ltd delivers expert servicing, maintenance, and repair of industrial refrigeration systems, screw compressors, and compressed air solutions across Uganda.
    </p>
    <div class="hero-btns">
      <a href="#contact" class="btn-primary">Request a Service</a>
      <a href="#services" class="btn-outline">Our Services</a>
    </div>
    <div class="hero-stats">
      <div>
        <div class="stat-num">3+</div>
        <div class="stat-label">Major Industrial Clients</div>
      </div>
      <div>
        <div class="stat-num">24/7</div>
        <div class="stat-label">Emergency Response</div>
      </div>
      <div>
        <div class="stat-num">100%</div>
        <div class="stat-label">Commitment to Quality</div>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services">
  <div class="services-header">
    <div class="section-tag">What We Do</div>
    <h2 class="section-title">Our Services</h2>
    <p class="section-sub">Comprehensive industrial maintenance and repair services for refrigeration, compressed air, and electrical systems.</p>
  </div>
  <div class="services-grid">
    <div class="service-card">
      <div class="service-icon">❄️</div>
      <div class="service-name">Industrial Refrigeration</div>
      <p class="service-desc">Full servicing and repair of industrial chillers, cold rooms, and refrigeration systems including Weco, Danfoss, and Carel controlled units.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">💨</div>
      <div class="service-name">Screw Compressors</div>
      <p class="service-desc">Maintenance, fault diagnosis, and repair of Kaishan, Ingersoll Rand, Shangair, and ELGi screw compressors for industrial applications.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">🌬️</div>
      <div class="service-name">Compressed Air Systems</div>
      <p class="service-desc">Installation, servicing, and maintenance of complete compressed air systems including dryers, filters, and distribution pipework.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">⚡</div>
      <div class="service-name">Electrical Services</div>
      <p class="service-desc">Industrial electrical installation, panel wiring, motor control systems, and fault finding for manufacturing and processing facilities.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">🔧</div>
      <div class="service-name">Generator Servicing</div>
      <p class="service-desc">Maintenance and repair of industrial generators including Kirloskar units with DSE controller diagnostics and configuration.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">🛢️</div>
      <div class="service-name">Compressor Oils &amp; Parts</div>
      <p class="service-desc">Supply of genuine compressor oils, filters, and spare parts through our sister company Mumbai Trading Uganda Limited.</p>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="about-visual">
    <div class="about-quote">
      Keeping Uganda's <span>Industry Running</span> Around the Clock
    </div>
    <div class="about-divider"></div>
    <p class="about-sub-text">From screw compressors to industrial chillers, we bring hands-on technical expertise directly to your facility.</p>
    <ul class="about-points">
      <li>Certified technicians with field experience</li>
      <li>On-site servicing across Kampala and surrounding areas</li>
      <li>Genuine parts and approved lubricants</li>
      <li>Carel pCO5 commissioning and programming</li>
      <li>Fast response to breakdowns and emergencies</li>
    </ul>
  </div>
  <div class="about-text">
    <div class="section-tag">About Us</div>
    <h2 class="section-title">Who We Are</h2>
    <p class="section-sub" style="margin-bottom:1.2rem;">
      Dule Suppliers (U) Ltd is a Kampala-based industrial servicing company specialising in refrigeration systems, compressed air solutions, and electrical services for manufacturing and processing industries in Uganda.
    </p>
    <p style="font-size:0.95rem; color:var(--text-light); line-height:1.7; margin-bottom:1.2rem;">
      We work with some of Uganda's leading manufacturers, providing preventive maintenance contracts, emergency breakdown support, and major overhaul projects. Our technical team has hands-on experience with leading brands including Kaishan, Ingersoll Rand, Weco, Danfoss, Carel, Grundfos, and ELGi.
    </p>
    <p style="font-size:0.95rem; color:var(--text-light); line-height:1.7;">
      Our sister company, <strong>Mumbai Trading Uganda Limited</strong>, ensures a reliable local supply of compressor oils, filters, and spare parts.
    </p>
    <div style="margin-top:2rem; padding: 1.2rem; background: var(--gold-pale); border-left: 3px solid var(--gold);">
      <div style="font-size:0.8rem; font-weight:700; color:var(--navy); text-transform:uppercase; letter-spacing:0.08em; margin-bottom:0.3rem;">Banking Details</div>
      <div style="font-size:0.88rem; color:var(--text-light);">Stanbic Bank Uganda | Account: Dule Suppliers (U) Ltd</div>
    </div>
  </div>
</section>

<!-- CLIENTS -->
<section id="clients">
  <div class="section-tag">Trusted By</div>
  <h2 class="section-title">Our Clients</h2>
  <p class="section-sub">We are proud to serve some of Uganda's leading industrial and manufacturing companies.</p>
  <div class="clients-grid">
    <div class="client-card">
      <div class="client-name">Luuka Plastics Ltd</div>
      <div class="client-loc">Kawempe · Matugga · Namanve</div>
    </div>
    <div class="client-card">
      <div class="client-name">Amos Dairies</div>
      <div class="client-loc">Uganda</div>
    </div>
    <div class="client-card">
      <div class="client-name">Imperial Tissue Uganda Ltd</div>
      <div class="client-loc">Uganda</div>
    </div>
    <div class="client-card">
      <div class="client-name">HSC Technical Exhibition</div>
      <div class="client-loc">Uganda</div>
    </div>
  </div>
</section>

<!-- WHY US -->
<section id="why">
  <div class="section-tag">Why Choose Us</div>
  <h2 class="section-title">The Dule Advantage</h2>
  <div class="why-grid">
    <div class="why-item">
      <div class="why-icon">⚙️</div>
      <div>
        <div class="why-title">Hands-On Expertise</div>
        <div class="why-desc">Our technicians work directly on your equipment — no subcontracting, no shortcuts.</div>
      </div>
    </div>
    <div class="why-item">
      <div class="why-icon">🚗</div>
      <div>
        <div class="why-title">On-Site Service</div>
        <div class="why-desc">We come to your facility anywhere in Kampala and surrounding industrial areas.</div>
      </div>
    </div>
    <div class="why-item">
      <div class="why-icon">📋</div>
      <div>
        <div class="why-title">Full Documentation</div>
        <div class="why-desc">Proper job cards, service reports, and invoices for every job — compliant with WHT requirements.</div>
      </div>
    </div>
    <div class="why-item">
      <div class="why-icon">🔩</div>
      <div>
        <div class="why-title">Genuine Parts</div>
        <div class="why-desc">Parts and oils supplied through Mumbai Trading Uganda — quality guaranteed.</div>
      </div>
    </div>
    <div class="why-item">
      <div class="why-icon">📞</div>
      <div>
        <div class="why-title">Responsive Support</div>
        <div class="why-desc">Fast response to breakdowns. We understand that downtime costs your business money.</div>
      </div>
    </div>
    <div class="why-item">
      <div class="why-icon">📊</div>
      <div>
        <div class="why-title">Preventive Maintenance</div>
        <div class="why-desc">Scheduled service contracts to keep your equipment running efficiently year-round.</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div>
    <div class="section-tag">Get In Touch</div>
    <h2 class="section-title">Contact Us</h2>
    <p class="section-sub">Ready to service your equipment? Get in touch and we'll respond promptly.</p>
    <div class="contact-items">
      <div class="contact-item">
        <div class="contact-icon">📍</div>
        <div>
          <div class="contact-label">Location</div>
          <div class="contact-value">Kampala, Uganda</div>
        </div>
      </div>
      <div class="contact-item">
        <div class="contact-icon">📞</div>
        <div>
          <div class="contact-label">Phone / WhatsApp</div>
          <div class="contact-value"><a href="tel:+256000000000">+256 (0) ___ ______</a></div>
        </div>
      </div>
      <div class="contact-item">
        <div class="contact-icon">✉️</div>
        <div>
          <div class="contact-label">Email</div>
          <div class="contact-value"><a href="mailto:info@dulesuppliers.co.ug">info@dulesuppliers.co.ug</a></div>
        </div>
      </div>
      <div class="contact-item">
        <div class="contact-icon">🕐</div>
        <div>
          <div class="contact-label">Working Hours</div>
          <div class="contact-value">Mon – Fri: 8:00am – 6:00pm<br/>Sat: 8:00am – 2:00pm</div>
        </div>
      </div>
    </div>
  </div>
  <div class="contact-form-area">
    <div class="form-title">Send Us a Message</div>
    <div class="form-group">
      <label>Your Name</label>
      <input type="text" placeholder="Full name"/>
    </div>
    <div class="form-group">
      <label>Company</label>
      <input type="text" placeholder="Company name"/>
    </div>
    <div class="form-group">
      <label>Phone / WhatsApp</label>
      <input type="tel" placeholder="+256 ..."/>
    </div>
    <div class="form-group">
      <label>Service Required</label>
      <select>
        <option value="">Select a service...</option>
        <option>Industrial Refrigeration</option>
        <option>Screw Compressor Service</option>
        <option>Compressed Air System</option>
        <option>Electrical Services</option>
        <option>Generator Servicing</option>
        <option>Parts / Oils Supply</option>
        <option>Other</option>
      </select>
    </div>
    <div class="form-group">
      <label>Message</label>
      <textarea placeholder="Describe your equipment and what service you need..."></textarea>
    </div>
    <button class="btn-submit" onclick="submitForm()">Send Message →</button>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">DULE <span>SUPPLIERS</span> (U) LTD</div>
  <div class="footer-text">© 2026 Dule Suppliers (U) Ltd · Kampala, Uganda · All rights reserved</div>
  <div class="footer-links">
    <a href="#services">Services</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </div>
</footer>

<!-- WHATSAPP FLOAT -->
<a href="https://wa.me/256000000000" class="wa-float" target="_blank" title="Chat on WhatsApp">💬</a>

<script>
  function toggleMenu() {
    const links = document.querySelector('.nav-links');
    links.style.display = links.style.display === 'flex' ? 'none' : 'flex';
    links.style.flexDirection = 'column';
    links.style.position = 'absolute';
    links.style.top = '64px';
    links.style.left = '0';
    links.style.width = '100%';
    links.style.background = 'rgba(10,31,68,0.98)';
    links.style.padding = '1rem 5%';
    links.style.gap = '1rem';
  }

  function submitForm() {
    alert('Thank you! We will contact you shortly.\n\nFor urgent matters, please WhatsApp us directly.');
  }

  // Smooth active nav highlight
  const sections = document.querySelectorAll('section[id]');
  const navLinks = document.querySelectorAll('.nav-links a');
  window.addEventListener('scroll', () => {
    let current = '';
    sections.forEach(s => {
      if (window.scrollY >= s.offsetTop - 80) current = s.id;
    });
    navLinks.forEach(a => {
      a.style.color = a.getAttribute('href') === '#' + current ? '#C9A84C' : '';
    });
  });
</script>
</body>
</html>
