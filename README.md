# Haf-s
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Haf's | Modest Fashion Designer</title>
  <meta name="description" content="Haf's - Elegant Muslim fashion designer portfolio featuring modest couture, abayas, hijabs, and Eid collections." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@500;600;700&family=Manrope:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    /* ========== Global Styles ========== */
    :root{
      --navy:#07162d;
      --navy-2:#0d2145;
      --navy-3:#132d5a;
      --white:#f8fbff;
      --muted:#cfd8e8;
      --gold:#d7b977;
      --gold-soft:#f0dfb0;
      --line:rgba(240,223,176,0.15);
      --glass:rgba(255,255,255,0.08);
      --glass-2:rgba(255,255,255,0.05);
      --shadow:0 20px 60px rgba(0,0,0,0.28);
      --radius:24px;
      --transition:all 0.45s ease;
    }

    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0;
      font-family:"Manrope",sans-serif;
      color:var(--white);
      background:
        radial-gradient(circle at 20% 15%, rgba(215,185,119,0.12), transparent 18%),
        radial-gradient(circle at 80% 20%, rgba(255,255,255,0.06), transparent 20%),
        radial-gradient(circle at 50% 100%, rgba(19,45,90,0.6), transparent 32%),
        linear-gradient(180deg, #061226 0%, #091a33 40%, #0a1e3b 100%);
      overflow-x:hidden;
    }

    body::before{
      content:"";
      position:fixed;
      inset:0;
      pointer-events:none;
      opacity:0.42;
      background-image:
        radial-gradient(circle at 25px 25px, rgba(215,185,119,0.08) 2px, transparent 2px),
        radial-gradient(circle at 75px 75px, rgba(215,185,119,0.06) 1.6px, transparent 1.6px),
        linear-gradient(rgba(215,185,119,0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(215,185,119,0.03) 1px, transparent 1px);
      background-size:100px 100px;
      z-index:-2;
    }

    img,svg{display:block;max-width:100%}
    a{text-decoration:none;color:inherit}
    button,input,textarea{font:inherit}
    .container{width:min(1180px, calc(100% - 32px)); margin-inline:auto}
    .section{padding:110px 0; position:relative}
    .section-head{
      display:flex;
      flex-direction:column;
      gap:10px;
      margin-bottom:38px;
      text-align:center;
      align-items:center;
    }
    .section-kicker{
      color:var(--gold-soft);
      letter-spacing:0.22em;
      text-transform:uppercase;
      font-size:12px;
    }
    .section-title{
      margin:0;
      font-family:"Cormorant Garamond",serif;
      font-size:clamp(2.25rem, 4vw, 4.2rem);
      line-height:0.95;
      letter-spacing:0.02em;
    }
    .section-desc{
      max-width:680px;
      color:var(--muted);
      margin:0;
      line-height:1.8;
    }

    .grain{
      position:fixed;
      inset:0;
      pointer-events:none;
      opacity:0.06;
      background-image:
        linear-gradient(transparent 0%, rgba(255,255,255,0.05) 100%);
      mix-blend-mode:soft-light;
      z-index:-1;
    }

    /* ========== Navigation ========== */
    .nav{
      position:fixed;
      top:0; left:0; right:0;
      z-index:50;
      backdrop-filter:blur(16px);
      background:linear-gradient(180deg, rgba(7,22,45,0.78), rgba(7,22,45,0.45));
      border-bottom:1px solid rgba(255,255,255,0.06);
    }
    .nav-inner{
      display:flex;
      align-items:center;
      justify-content:space-between;
      min-height:78px;
      gap:20px;
    }
    .brand{
      font-family:"Cormorant Garamond",serif;
      font-size:2rem;
      font-weight:700;
      letter-spacing:0.04em;
      display:flex;
      align-items:center;
      gap:10px;
    }
    .brand::after{
      content:"☾";
      color:var(--gold);
      font-size:1rem;
      transform:translateY(-2px);
      opacity:0.9;
    }
    .nav-links{
      display:flex;
      align-items:center;
      gap:24px;
    }
    .nav-links a{
      color:var(--muted);
      font-size:0.95rem;
      transition:var(--transition);
      position:relative;
    }
    .nav-links a::after{
      content:"";
      position:absolute;
      left:0; bottom:-8px;
      width:100%; height:1px;
      background:linear-gradient(90deg, transparent, var(--gold), transparent);
      transform:scaleX(0);
      transform-origin:center;
      transition:transform 0.35s ease;
    }
    .nav-links a:hover{color:var(--white)}
    .nav-links a:hover::after{transform:scaleX(1)}
    .nav-toggle{
      display:none;
      width:46px;height:46px;
      border-radius:50%;
      border:1px solid rgba(255,255,255,0.12);
      background:rgba(255,255,255,0.06);
      color:var(--white);
      cursor:pointer;
    }

    /* ========== Hero Section ========== */
    .hero{
      min-height:100vh;
      display:flex;
      align-items:center;
      position:relative;
      overflow:hidden;
      padding-top:90px;
    }
    .hero::before{
      content:"";
      position:absolute;
      inset:8% 12% auto auto;
      width:360px;
      height:360px;
      border-radius:50%;
      background:radial-gradient(circle, rgba(215,185,119,0.14), transparent 65%);
      filter:blur(10px);
      pointer-events:none;
    }
    .hero-grid{
      display:grid;
      grid-template-columns:1.15fr 0.85fr;
      align-items:center;
      gap:40px;
      width:100%;
      position:relative;
      z-index:2;
    }
    .hero-copy{max-width:620px}
    .eyebrow{
      margin:0 0 12px;
      color:var(--gold-soft);
      letter-spacing:0.18em;
      text-transform:uppercase;
      font-size:0.78rem;
      opacity:0;
      animation:riseFade 0.8s ease 0.05s forwards;
    }
    .hafs-title{
      margin:0;
      font-family:"Cormorant Garamond",serif;
      font-weight:700;
      line-height:0.9;
      letter-spacing:0.04em;
      font-size:clamp(4rem, 11vw, 8rem);
      background:linear-gradient(90deg, #ffffff 0%, var(--gold-soft) 25%, #ffffff 50%, var(--gold) 75%, #ffffff 100%);
      background-size:200% auto;
      -webkit-background-clip:text;
      background-clip:text;
      color:transparent;
      text-shadow:0 0 28px rgba(215,185,119,0.12);
      opacity:0;
      animation:riseFade 1s ease 0.18s forwards, shine 7s linear infinite 1.2s;
    }
    .subtitle{
      margin:10px 0 16px;
      color:var(--white);
      font-size:clamp(1.15rem, 2vw, 1.6rem);
      letter-spacing:0.08em;
      text-transform:uppercase;
      opacity:0;
      animation:riseFade 0.8s ease 0.38s forwards;
    }
    .hero-text{
      margin:0;
      color:var(--muted);
      max-width:560px;
      font-size:1.02rem;
      line-height:1.9;
      opacity:0;
      animation:riseFade 0.8s ease 0.55s forwards;
    }
    .cta-group{
      display:flex;
      flex-wrap:wrap;
      gap:14px;
      margin-top:28px;
      opacity:0;
      animation:riseFade 0.8s ease 0.72s forwards;
    }
    .btn{
      position:relative;
      display:inline-flex;
      align-items:center;
      justify-content:center;
      gap:10px;
      padding:14px 22px;
      border-radius:999px;
      border:1px solid rgba(255,255,255,0.14);
      transition:var(--transition);
      overflow:hidden;
      cursor:pointer;
    }
    .btn::before{
      content:"";
      position:absolute;
      inset:0;
      background:linear-gradient(90deg, transparent, rgba(255,255,255,0.16), transparent);
      transform:translateX(-110%);
      transition:transform 0.7s ease;
    }
    .btn:hover::before{transform:translateX(110%)}
    .btn-primary{
      background:linear-gradient(135deg, rgba(215,185,119,0.26), rgba(215,185,119,0.14));
      border-color:rgba(215,185,119,0.4);
      box-shadow:0 0 0 0 rgba(215,185,119,0.25), 0 14px 32px rgba(0,0,0,0.22);
    }
    .btn-primary:hover{
      transform:translateY(-2px);
      box-shadow:0 0 28px rgba(215,185,119,0.22), 0 18px 40px rgba(0,0,0,0.28);
    }
    .btn-secondary{
      background:rgba(255,255,255,0.04);
      color:var(--white);
    }
    .btn-secondary:hover{
      transform:translateY(-2px);
      background:rgba(255,255,255,0.08);
      box-shadow:0 0 20px rgba(255,255,255,0.06);
    }

    .hero-art{
      position:relative;
      opacity:0;
      animation:riseFade 1s ease 0.5s forwards;
    }
    .art-card{
      position:relative;
      border-radius:32px;
      overflow:hidden;
      background:linear-gradient(180deg, rgba(255,255,255,0.08), rgba(255,255,255,0.03));
      border:1px solid rgba(255,255,255,0.08);
      box-shadow:var(--shadow);
      padding:12px;
      isolation:isolate;
    }
    .art-card::before{
      content:"";
      position:absolute;
      inset:-30% 20% auto auto;
      width:180px;
      height:180px;
      background:radial-gradient(circle, rgba(215,185,119,0.18), transparent 70%);
      filter:blur(12px);
      z-index:-1;
    }

    .floating-scene{
      position:absolute;
      inset:0;
      overflow:hidden;
      pointer-events:none;
      z-index:1;
    }
    .float-item{
      position:absolute;
      bottom:-10vh;
      color:rgba(240,223,176,0.25);
      text-shadow:0 0 18px rgba(215,185,119,0.16);
      animation:floatUp linear infinite;
      user-select:none;
      will-change:transform, opacity;
    }
    .scroll-indicator{
      position:absolute;
      left:50%;
      bottom:24px;
      transform:translateX(-50%);
      color:rgba(255,255,255,0.7);
      font-size:0.82rem;
      letter-spacing:0.18em;
      text-transform:uppercase;
      display:flex;
      flex-direction:column;
      align-items:center;
      gap:8px;
      z-index:2;
    }
    .scroll-indicator::after{
      content:"";
      width:1px;height:42px;
      background:linear-gradient(180deg, rgba(215,185,119,0), rgba(215,185,119,0.9), rgba(215,185,119,0));
      animation:pulseLine 1.8s ease-in-out infinite;
    }

    /* ========== Cards / Panels ========== */
    .panel{
      background:linear-gradient(180deg, rgba(255,255,255,0.06), rgba(255,255,255,0.03));
      border:1px solid rgba(255,255,255,0.08);
      border-radius:var(--radius);
      box-shadow:var(--shadow);
    }

    /* ========== About ========== */
    .about-grid{
      display:grid;
      grid-template-columns:1.05fr 0.95fr;
      gap:28px;
      align-items:stretch;
    }
    .about-text,
    .about-panel{
      padding:34px;
    }
    .about-text p,
    .about-panel p{
      margin:0;
      color:var(--muted);
      line-height:1.9;
    }
    .quote{
      margin-top:24px;
      padding:20px;
      border-radius:18px;
      background:rgba(255,255,255,0.03);
      border:1px solid rgba(255,255,255,0.08);
      color:var(--white);
      font-family:"Cormorant Garamond",serif;
      font-size:1.55rem;
      line-height:1.2;
    }
    .chips{
      display:flex;
      flex-wrap:wrap;
      gap:10px;
      margin-top:24px;
    }
    .chip{
      padding:10px 14px;
      border-radius:999px;
      background:rgba(215,185,119,0.1);
      border:1px solid rgba(215,185,119,0.2);
      color:var(--gold-soft);
      font-size:0.88rem;
    }
    .crescent-mark{
      width:72px;height:72px;
      border-radius:50%;
      position:relative;
      margin-bottom:20px;
      background:radial-gradient(circle, rgba(215,185,119,0.16), transparent 70%);
      display:grid;place-items:center;
    }
    .crescent-mark::before{
      content:"☾";
      color:var(--gold);
      font-size:2.2rem;
      transform:translateX(2px);
    }

    /* ========== Collection ========== */
    .cards{
      display:grid;
      grid-template-columns:repeat(3, 1fr);
      gap:24px;
    }
    .collection-card{
      overflow:hidden;
      transition:var(--transition);
      position:relative;
    }
    .collection-card:hover{
      transform:translateY(-8px);
      box-shadow:0 0 30px rgba(215,185,119,0.16), var(--shadow);
      border-color:rgba(215,185,119,0.18);
    }
    .card-media{
      aspect-ratio:4/4.8;
      overflow:hidden;
      border-bottom:1px solid rgba(255,255,255,0.08);
      background:#09182f;
    }
    .card-media svg{
      width:100%;
      height:100%;
      transition:transform 0.7s ease;
    }
    .collection-card:hover .card-media svg{transform:scale(1.06)}
    .card-body{
      padding:24px;
    }
    .card-title{
      margin:0 0 10px;
      font-family:"Cormorant Garamond",serif;
      font-size:2rem;
    }
    .card-body p{
      margin:0;
      color:var(--muted);
      line-height:1.8;
      font-size:0.97rem;
    }

    /* ========== Gallery ========== */
    .gallery-grid{
      display:grid;
      grid-template-columns:repeat(3, 1fr);
      gap:18px;
    }
    .gallery-item{
      padding:0;
      border:none;
      background:none;
      cursor:pointer;
      border-radius:22px;
      overflow:hidden;
      position:relative;
    }
    .gallery-item .thumb{
      border-radius:22px;
      overflow:hidden;
      border:1px solid rgba(255,255,255,0.08);
      background:linear-gradient(180deg, rgba(255,255,255,0.05), rgba(255,255,255,0.03));
      transition:var(--transition);
      box-shadow:0 18px 30px rgba(0,0,0,0.22);
    }
    .gallery-item svg{
      aspect-ratio:4/5;
      width:100%;
      height:100%;
      transition:transform 0.6s ease, filter 0.6s ease;
    }
    .gallery-item::after{
      content:attr(data-caption);
      position:absolute;
      left:18px; right:18px; bottom:16px;
      padding:12px 14px;
      border-radius:14px;
      font-size:0.9rem;
      color:var(--white);
      background:linear-gradient(180deg, rgba(7,22,45,0.15), rgba(7,22,45,0.72));
      border:1px solid rgba(255,255,255,0.08);
      opacity:0;
      transform:translateY(10px);
      transition:var(--transition);
      pointer-events:none;
    }
    .gallery-item:hover .thumb{
      box-shadow:0 0 24px rgba(215,185,119,0.16), 0 18px 30px rgba(0,0,0,0.25);
    }
    .gallery-item:hover svg{
      transform:scale(1.04);
      filter:saturate(1.08);
    }
    .gallery-item:hover::after{
      opacity:1;
      transform:translateY(0);
    }

    /* ========== Contact ========== */
    .contact-shell{
      display:grid;
      grid-template-columns:0.9fr 1.1fr;
      gap:24px;
      align-items:stretch;
    }
    .contact-copy,
    .contact-form{
      padding:34px;
    }
    .contact-copy p{
      margin:0;
      color:var(--muted);
      line-height:1.9;
    }
    .contact-info{
      margin-top:24px;
      display:grid;
      gap:12px;
    }
    .info-item{
      padding:14px 16px;
      border-radius:16px;
      background:rgba(255,255,255,0.04);
      border:1px solid rgba(255,255,255,0.08);
      color:var(--muted);
    }
    .form-grid{
      display:grid;
      gap:14px;
    }
    .field{
      display:grid;
      gap:8px;
    }
    .field label{
      color:var(--gold-soft);
      font-size:0.9rem;
    }
    .field input,
    .field textarea{
      width:100%;
      border:none;
      outline:none;
      border-radius:16px;
      padding:15px 16px;
      background:rgba(255,255,255,0.05);
      border:1px solid rgba(255,255,255,0.08);
      color:var(--white);
      transition:var(--transition);
      resize:vertical;
    }
    .field input::placeholder,
    .field textarea::placeholder{color:rgba(207,216,232,0.65)}
    .field input:focus,
    .field textarea:focus{
      border-color:rgba(215,185,119,0.45);
      box-shadow:0 0 0 4px rgba(215,185,119,0.08), 0 0 22px rgba(215,185,119,0.08);
    }
    .submit-row{
      display:flex;
      align-items:center;
      gap:14px;
      margin-top:6px;
      flex-wrap:wrap;
    }
    .form-note{
      color:var(--muted);
      font-size:0.9rem;
    }

    /* ========== Footer ========== */
    .footer{
      padding:26px 0 34px;
      border-top:1px solid rgba(255,255,255,0.08);
      color:rgba(255,255,255,0.75);
      text-align:center;
      position:relative;
    }
    .footer span{
      color:var(--gold-soft);
      letter-spacing:0.08em;
    }

    /* ========== Lightbox ========== */
    .lightbox{
      position:fixed;
      inset:0;
      background:rgba(4,10,20,0.84);
      backdrop-filter:blur(10px);
      display:flex;
      align-items:center;
      justify-content:center;
      padding:20px;
      opacity:0;
      visibility:hidden;
      transition:var(--transition);
      z-index:100;
    }
    .lightbox.active{
      opacity:1;
      visibility:visible;
    }
    .lightbox-inner{
      width:min(920px, 100%);
      position:relative;
    }
    .lightbox-card{
      border-radius:28px;
      overflow:hidden;
      border:1px solid rgba(255,255,255,0.1);
      background:linear-gradient(180deg, rgba(255,255,255,0.08), rgba(255,255,255,0.04));
      box-shadow:0 24px 80px rgba(0,0,0,0.45);
    }
    .lightbox-media{background:#08162b}
    .lightbox-media svg{
      width:100%;
      max-height:78vh;
      height:auto;
      aspect-ratio:4/5;
    }
    .lightbox-caption{
      padding:16px 18px;
      color:var(--white);
      border-top:1px solid rgba(255,255,255,0.08);
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:16px;
    }
    .lightbox-close{
      position:absolute;
      top:-10px;
      right:-10px;
      width:46px;
      height:46px;
      border:none;
      border-radius:50%;
      background:rgba(255,255,255,0.12);
      color:var(--white);
      cursor:pointer;
      border:1px solid rgba(255,255,255,0.14);
      transition:var(--transition);
    }
    .lightbox-close:hover{
      transform:rotate(90deg);
      background:rgba(215,185,119,0.18);
      box-shadow:0 0 20px rgba(215,185,119,0.2);
    }

    /* ========== Reveal Animations ========== */
    .reveal{
      opacity:0;
      transform:translateY(26px);
      transition:opacity 0.9s ease, transform 0.9s ease;
    }
    .reveal.visible{
      opacity:1;
      transform:translateY(0);
    }

    .toast{
      position:fixed;
      left:50%;
      bottom:20px;
      transform:translateX(-50%) translateY(20px);
      padding:14px 18px;
      border-radius:999px;
      background:rgba(7,22,45,0.92);
      border:1px solid rgba(215,185,119,0.28);
      color:var(--white);
      box-shadow:0 18px 40px rgba(0,0,0,0.3);
      opacity:0;
      visibility:hidden;
      transition:var(--transition);
      z-index:120;
    }
    .toast.show{
      opacity:1;
      visibility:visible;
      transform:translateX(-50%) translateY(0);
    }

    /* ========== Keyframes ========== */
    @keyframes riseFade{
      from{opacity:0; transform:translateY(22px)}
      to{opacity:1; transform:translateY(0)}
    }
    @keyframes shine{
      0%{background-position:0% center}
      100%{background-position:200% center}
    }
    @keyframes pulseLine{
      0%,100%{opacity:0.35; transform:scaleY(0.8)}
      50%{opacity:1; transform:scaleY(1)}
    }
    @keyframes floatUp{
      0%{transform:translate3d(0,0,0) rotate(0deg); opacity:0}
      10%{opacity:0.65}
      100%{transform:translate3d(var(--drift, 30px), -120vh, 0) rotate(90deg); opacity:0}
    }

    /* ========== Responsive ========== */
    @media (max-width: 1024px){
      .hero-grid,
      .about-grid,
      .contact-shell{
        grid-template-columns:1fr;
      }
      .cards,
      .gallery-grid{
        grid-template-columns:repeat(2, 1fr);
      }
      .hero{
        padding-top:110px;
        padding-bottom:80px;
      }
      .hero-copy{max-width:100%}
    }

    @media (max-width: 760px){
      .section{padding:88px 0}
      .nav-toggle{display:inline-grid; place-items:center}
      .nav-links{
        position:absolute;
        top:86px;
        left:16px;
        right:16px;
        background:rgba(7,22,45,0.96);
        border:1px solid rgba(255,255,255,0.08);
        border-radius:20px;
        padding:16px;
        display:grid;
        gap:14px;
        transform:translateY(-12px);
        opacity:0;
        visibility:hidden;
        transition:var(--transition);
        box-shadow:var(--shadow);
      }
      .nav-links.open{
        opacity:1;
        visibility:visible;
        transform:translateY(0);
      }
      .cards,
      .gallery-grid{
        grid-template-columns:1fr;
      }
      .about-text,
      .about-panel,
      .contact-copy,
      .contact-form{
        padding:24px;
      }
      .scroll-indicator{display:none}
      .lightbox-close{
        top:12px;
        right:12px;
      }
    }
  </style>
</head>
<body>
  <div class="grain"></div>

  <!-- Navigation -->
  <header class="nav">
    <div class="container nav-inner">
      <a href="#home" class="brand">Haf's</a>
      <button class="nav-toggle" id="navToggle" aria-label="Open navigation">☰</button>
      <nav class="nav-links" id="navMenu">
        <a href="#about">About</a>
        <a href="#collection">Collection</a>
        <a href="#gallery">Gallery</a>
        <a href="#contact">Contact</a>
      </nav>
    </div>
  </header>

  <main>
    <!-- Hero -->
    <section class="hero" id="home">
      <div class="floating-scene" id="floatingScene" aria-hidden="true"></div>
      <div class="container hero-grid">
        <div class="hero-copy">
          <p class="eyebrow">Elegant Modest Couture</p>
          <h1 class="hafs-title">Haf's</h1>
          <p class="subtitle">Modest Fashion Designer</p>
          <p class="hero-text">
            Timeless silhouettes inspired by faith, femininity, and refined detail — where soft luxury meets Islamic modest fashion.
          </p>
          <div class="cta-group">
            <a href="#collection" class="btn btn-primary">View Collection</a>
            <a href="#contact" class="btn btn-secondary">Let's Connect</a>
          </div>
        </div>

        <div class="hero-art">
          <div class="art-card">
            <svg viewBox="0 0 600 780" xmlns="http://www.w3.org/2000/svg" aria-label="Featured modest fashion artwork">
              <defs>
                <linearGradient id="heroBg" x1="0" y1="0" x2="1" y2="1">
                  <stop offset="0%" stop-color="#0f2750"/>
                  <stop offset="100%" stop-color="#07162d"/>
                </linearGradient>
                <radialGradient id="heroGlow" cx="70%" cy="20%" r="40%">
                  <stop offset="0%" stop-color="rgba(240,223,176,0.35)"/>
                  <stop offset="100%" stop-color="rgba(240,223,176,0)"/>
                </radialGradient>
              </defs>
              <rect width="600" height="780" rx="28" fill="url(#heroBg)"/>
              <circle cx="460" cy="120" r="110" fill="url(#heroGlow)"/>
              <path d="M390 95a42 42 0 1 1-25-78a34 34 0 1 0 25 78Z" fill="#e4c98c" opacity="0.95"/>
              <path d="M160 160 Q300 70 440 160" fill="none" stroke="rgba(240,223,176,0.28)" stroke-width="2"/>
              <path d="M120 640 Q300 715 480 640" fill="none" stroke="rgba(240,223,176,0.18)" stroke-width="2"/>
              <path d="M180 180 Q300 40 420 180" fill="none" stroke="rgba(255,255,255,0.08)" stroke-width="1.5"/>
              <path d="M170 190 V610 Q300 690 430 610 V190" fill="none" stroke="rgba(240,223,176,0.18)" stroke-width="1.5"/>
              <g opacity="0.7">
                <circle cx="130" cy="260" r="3" fill="#e4c98c"/>
                <circle cx="150" cy="245" r="3" fill="#e4c98c"/>
                <circle cx="165" cy="265" r="3" fill="#e4c98c"/>
                <circle cx="148" cy="282" r="3" fill="#e4c98c"/>
                <circle cx="115" cy="282" r="3" fill="#e4c98c"/>
                <circle cx="430" cy="560" r="3" fill="#e4c98c"/>
                <circle cx="450" cy="545" r="3" fill="#e4c98c"/>
                <circle cx="465" cy="565" r="3" fill="#e4c98c"/>
                <circle cx="448" cy="582" r="3" fill="#e4c98c"/>
                <circle cx="415" cy="582" r="3" fill="#e4c98c"/>
              </g>
              <g transform="translate(0 10)">
                <circle cx="300" cy="185" r="32" fill="rgba(255,255,255,0.06)" stroke="rgba(240,223,176,0.55)" stroke-width="2"/>
                <path d="M276 175q24-30 48 0v24q-10 18-24 22q-14-4-24-22Z" fill="rgba(240,223,176,0.12)" stroke="rgba(240,223,176,0.65)" stroke-width="2"/>
                <path d="M250 255q22-34 50-34q28 0 50 34q-6 52-6 94l53 267q4 24-17 36q-21 12-80 12t-80-12q-21-12-17-36l53-267q0-42-6-94Z"
                      fill="rgba(255,255,255,0.04)" stroke="rgba(240,223,176,0.7)" stroke-width="2.2"/>
                <path d="M300 222v442" stroke="rgba(240,223,176,0.35)" stroke-width="1.4" stroke-dasharray="6 10"/>
                <path d="M250 255q-20 30-42 68q-15 28-8 42q7 14 32 10l43-26" fill="none" stroke="rgba(240,223,176,0.55)" stroke-width="2"/>
                <path d="M350 255q20 30 42 68q15 28 8 42q-7 14-32 10l-43-26" fill="none" stroke="rgba(240,223,176,0.55)" stroke-width="2"/>
                <path d="M247 428q53 26 106 0" fill="none" stroke="rgba(240,223,176,0.45)" stroke-width="1.8"/>
                <path d="M236 510q64 34 128 0" fill="none" stroke="rgba(240,223,176,0.34)" stroke-width="1.8"/>
              </g>
              <text x="300" y="735" text-anchor="middle" fill="#f4e8c8" font-family="Cormorant Garamond, serif" font-size="44" letter-spacing="4">MODEST ELEGANCE</text>
            </svg>
          </div>
        </div>
      </div>
      <div class="scroll-indicator">Scroll</div>
    </section>

    <!-- About -->
    <section class="section" id="about">
      <div class="container">
        <div class="section-head reveal">
          <span class="section-kicker">About</span>
          <h2 class="section-title">Designing grace through modest fashion</h2>
          <p class="section-desc">
            Haf's creates refined pieces for women who love softness, structure, and intentional style — rooted in modesty, elegance, and Islamic beauty.
          </p>
        </div>

        <div class="about-grid">
          <div class="panel about-text reveal">
            <p>
              Inspired by floral forms, moonlit tones, and delicate geometry, Haf's blends contemporary design with timeless modest wear. Each piece is imagined to feel graceful, comfortable, and elevated for everyday sophistication or special celebrations.
            </p>
            <div class="chips">
              <span class="chip">Abaya Styling</span>
              <span class="chip">Hijab Design</span>
              <span class="chip">Eid Couture</span>
              <span class="chip">Premium Modesty</span>
            </div>
            <div class="quote">
              “Soft silhouettes, elegant detail, and modest beauty designed with intention.”
            </div>
          </div>

          <div class="panel about-panel reveal">
            <div class="crescent-mark"></div>
            <p>
              With a premium yet minimal approach, every collection at Haf's reflects feminine poise and spiritual calm. The vision is simple: to create fashion that feels luxurious without excess, and expressive without losing modest essence.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Collection -->
    <section class="section" id="collection">
      <div class="container">
        <div class="section-head reveal">
          <span class="section-kicker">Collection</span>
          <h2 class="section-title">Signature pieces</h2>
          <p class="section-desc">
            Discover a curated wardrobe of flowing abayas, soft hijab styling, and luminous festive looks.
          </p>
        </div>

        <div class="cards">
          <article class="panel collection-card reveal">
            <div class="card-media">
              <svg viewBox="0 0 600 720" xmlns="http://www.w3.org/2000/svg" aria-label="Abaya collection artwork">
                <defs>
                  <linearGradient id="abayaBg" x1="0" y1="0" x2="1" y2="1">
                    <stop offset="0%" stop-color="#10274f"/>
                    <stop offset="100%" stop-color="#061327"/>
                  </linearGradient>
                </defs>
                <rect width="600" height="720" fill="url(#abayaBg)"/>
                <circle cx="470" cy="120" r="100" fill="rgba(215,185,119,0.12)"/>
                <path d="M420 100a38 38 0 1 1-22-70a30 30 0 1 0 22 70Z" fill="#e4c98c"/>
                <path d="M170 150 Q300 75 430 150" fill="none" stroke="rgba(240,223,176,0.2)" stroke-width="2"/>
                <g transform="translate(0 12)">
                  <circle cx="300" cy="178" r="28" fill="rgba(255,255,255,0.05)" stroke="rgba(240,223,176,0.6)" stroke-width="2"/>
                  <path d="M252 244q22-32 48-32q26 0 48 32q-5 50-5 84l46 242q4 20-14 31q-18 11-75 11q-57 0-75-11q-18-11-14-31l46-242q0-34-5-84Z" fill="rgba(255,255,255,0.04)" stroke="rgba(240,223,176,0.72)" stroke-width="2"/>
                  <path d="M300 212v400" stroke="rgba(240,223,176,0.34)" stroke-width="1.5" stroke-dasharray="6 10"/>
                  <path d="M243 450q57 28 114 0" fill="none" stroke="rgba(240,223,176,0.42)" stroke-width="1.8"/>
                </g>
                <g opacity="0.65">
                  <circle cx="120" cy="250" r="3.2" fill="#e4c98c"/>
                  <circle cx="140" cy="235" r="3.2" fill="#e4c98c"/>
                  <circle cx="155" cy="255" r="3.2" fill="#e4c98c"/>
                  <circle cx="138" cy="272" r="3.2" fill="#e4c98c"/>
                  <circle cx="105" cy="272" r="3.2" fill="#e4c98c"/>
                </g>
                <text x="300" y="668" text-anchor="middle" fill="#f4e8c8" font-family="Cormorant Garamond, serif" font-size="46" letter-spacing="4">ABAYA</text>
              </svg>
            </div>
            <div class="card-body">
              <h3 class="card-title">Abaya</h3>
              <p>Flowing silhouettes with clean drape, soft structure, and refined gold-accent detailing for timeless everyday elegance.</p>
            </div>
          </article>

          <article class="panel collection-card reveal">
            <div class="card-media">
              <svg viewBox="0 0 600 720" xmlns="http://www.w3.org/2000/svg" aria-label="Hijab collection artwork">
                <defs>
                  <linearGradient id="hijabBg" x1="0" y1="0" x2="1" y2="1">
                    <stop offset="0%" stop-color="#0c2142"/>
                    <stop offset="100%" stop-color="#07162d"/>
                  </linearGradient>
                </defs>
                <rect width="600" height="720" fill="url(#hijabBg)"/>
                <path d="M150 165 Q300 55 450 165" fill="none" stroke="rgba(240,223,176,0.2)" stroke-width="2"/>
                <path d="M188 180 Q300 88 412 180" fill="none" stroke="rgba(255,255,255,0.08)" stroke-width="1.5"/>
                <g transform="translate(0 8)">
                  <circle cx="300" cy="182" r="28" fill="rgba(255,255,255,0.06)" stroke="rgba(240,223,176,0.6)" stroke-width="2"/>
                  <path d="M267 180q15-33 33-33q18 0 33 33v28q-12 20-33 24q-21-4-33-24Z" fill="rgba(240,223,176,0.12)" stroke="rgba(240,223,176,0.68)" stroke-width="2"/>
                  <path d="M250 230q18 12 50 12q32 0 50-12l22 140q9 70-20 102q-28 31-52 31t-52-31q-29-32-20-102Z"
                        fill="rgba(255,255,255,0.04)" stroke="rgba(240,223,176,0.72)" stroke-width="2"/>
                  <path d="M246 250q18 70 54 120q36-50 54-120" fill="none" stroke="rgba(240,223,176,0.4)" stroke-width="1.8"/>
                </g>
                <g opacity="0.65">
                  <circle cx="460" cy="210" r="3.2" fill="#e4c98c"/>
                  <circle cx="480" cy="195" r="3.2" fill="#e4c98c"/>
                  <circle cx="495" cy="215" r="3.2" fill="#e4c98c"/>
                  <circle cx="478" cy="232" r="3.2" fill="#e4c98c"/>
                  <circle cx="445" cy="232" r="3.2" fill="#e4c98c"/>
                </g>
                <circle cx="130" cy="580" r="90" fill="rgba(215,185,119,0.08)"/>
                <text x="300" y="668" text-anchor="middle" fill="#f4e8c8" font-family="Cormorant Garamond, serif" font-size="46" letter-spacing="4">HIJAB</text>
              </svg>
            </div>
            <div class="card-body">
              <h3 class="card-title">Hijab</h3>
              <p>Elegant draping and soft textures designed to complement modest wardrobes with effortless femininity and polish.</p>
            </div>
          </article>

          <article class="panel collection-card reveal">
            <div class="card-media">
              <svg viewBox="0 0 600 720" xmlns="http://www.w3.org/2000/svg" aria-label="Eid collection artwork">
                <defs>
                  <linearGradient id="eidBg" x1="0" y1="0" x2="1" y2="1">
                    <stop offset="0%" stop-color="#122c58"/>
                    <stop offset="100%" stop-color="#07162d"/>
                  </linearGradient>
                </defs>
                <rect width="600" height="720" fill="url(#eidBg)"/>
                <circle cx="470" cy="115" r="95" fill="rgba(215,185,119,0.14)"/>
                <path d="M425 95a34 34 0 1 1-20-62a27 27 0 1 0 20 62Z" fill="#e4c98c"/>
                <path d="M170 160 Q300 65 430 160" fill="none" stroke="rgba(240,223,176,0.2)" stroke-width="2"/>
                <g transform="translate(0 10)">
                  <circle cx="300" cy="175" r="28" fill="rgba(255,255,255,0.05)" stroke="rgba(240,223,176,0.6)" stroke-width="2"/>
                  <path d="M248 240q24-30 52-30q28 0 52 30q-8 44-7 88l58 248q4 18-16 30q-20 12-87 12q-67 0-87-12q-20-12-16-30l58-248q1-44-7-88Z"
                        fill="rgba(255,255,255,0.04)" stroke="rgba(240,223,176,0.74)" stroke-width="2"/>
                  <path d="M246 338q54 28 108 0" fill="none" stroke="rgba(240,223,176,0.4)" stroke-width="1.8"/>
                  <path d="M236 430q64 34 128 0" fill="none" stroke="rgba(240,223,176,0.34)" stroke-width="1.8"/>
                  <path d="M226 524q74 40 148 0" fill="none" stroke="rgba(240,223,176,0.28)" stroke-width="1.8"/>
                </g>
                <g opacity="0.7">
                  <circle cx="120" cy="210" r="3.2" fill="#e4c98c"/>
                  <circle cx="140" cy="195" r="3.2" fill="#e4c98c"/>
                  <circle cx="155" cy="215" r="3.2" fill="#e4c98c"/>
                  <circle cx="138" cy="232" r="3.2" fill="#e4c98c"/>
                  <circle cx="105" cy="232" r="3.2" fill="#e4c98c"/>
                  <circle cx="448" cy="560" r="3.2" fill="#e4c98c"/>
                  <circle cx="468" cy="545" r="3.2" fill="#e4c98c"/>
                  <circle cx="483" cy="565" r="3.2" fill="#e4c98c"/>
                  <circle cx="466" cy="582" r="3.2" fill="#e4c98c"/>
                  <circle cx="433" cy="582" r="3.2" fill="#e4c98c"/>
                </g>
                <text x="300" y="668" text-anchor="middle" fill="#f4e8c8" font-family="Cormorant Garamond, serif" font-size="46" letter-spacing="4">EID</text>
              </svg>
            </div>
            <div class="card-body">
              <h3 class="card-title">Eid Collection</h3>
              <p>Celebration-ready looks with luminous detail, graceful volume, and a luxurious finish for festive occasions.</p>
            </div>
          </article>
        </div>
      </div>
    </section>

    <!-- Gallery -->
    <section class="section" id="gallery">
      <div class="container">
        <div class="section-head reveal">
          <span class="section-kicker">Gallery</span>
          <h2 class="section-title">Aesthetic lookbook</h2>
          <p class="section-desc">
            A refined visual collection featuring soft florals, crescent details, and modest silhouettes in a premium editorial mood.
          </p>
        </div>

        <div class="gallery-grid">
          <button class="gallery-item reveal" data-caption="Moonlit Abaya">
            <div class="thumb">
              <svg viewBox="0 0 600 760" xmlns="http://www.w3.org/2000/svg">
                <rect width="600" height="760" fill="#0b1d3a"/>
                <circle cx="450" cy="120" r="100" fill="rgba(215,185,119,0.14)"/>
                <path d="M410 96a34 34 0 1 1-20-62a27 27 0 1 0 20 62Z" fill="#e4c98c"/>
                <path d="M170 160 Q300 68 430 160" fill="none" stroke="rgba(240,223,176,0.18)" stroke-width="2"/>
                <path d="M170 180 V620 Q300 700 430 620 V180" fill="none" stroke="rgba(240,223,176,0.16)" stroke-width="1.5"/>
                <circle cx="300" cy="190" r="30" fill="rgba(255,255,255,0.05)" stroke="rgba(240,223,176,0.6)" stroke-width="2"/>
                <path d="M248 256q24-34 52-34q28 0 52 34q-8 46-8 92l58 248q5 20-16 32t-86 12q-65 0-86-12t-16-32l58-248q0-46-8-92Z"
                      fill="rgba(255,255,255,0.04)" stroke="rgba(240,223,176,0.72)" stroke-width="2"/>
                <path d="M242 442q58 28 116 0" fill="none" stroke="rgba(240,223,176,0.42)" stroke-width="1.8"/>
                <text x="300" y="710" text-anchor="middle" fill="#f4e8c8" font-family="Cormorant Garamond, serif" font-size="34" letter-spacing="3">NOOR</text>
              </svg>
            </div>
          </button>

          <button class="gallery-item reveal" data-caption="Floral Hijab Edit">
            <div class="thumb">
              <svg viewBox="0 0 600 760" xmlns="http://www.w3.org/2000/svg">
                <rect width="600" height="760" fill="#0a1730"/>
                <circle cx="150" cy="610" r="120" fill="rgba(215,185,119,0.08)"/>
                <g opacity="0.7">
                  <circle cx="440" cy="190" r="3.3" fill="#e4c98c"/>
                  <circle cx="460" cy="175" r="3.3" fill="#e4c98c"/>
                  <circle cx="475" cy="195" r="3.3" fill="#e4c98c"/>
                  <circle cx="458" cy="212" r="3.3" fill="#e4c98c"/>
                  <circle cx="425" cy="212" r="3.3" fill="#e4c98c"/>
                </g>
                <path d="M158 165 Q300 58 442 165" fill="none" stroke="rgba(240,223,176,0.18)" stroke-width="2"/>
                <circle cx="300" cy="188" r="30" fill="rgba(255,255,255,0.05)" stroke="rgba(240,223,176,0.6)" stroke-width="2"/>
                <path d="M266 185q16-34 34-34q18 0 34 34v30q-12 22-34 26q-22-4-34-26Z" fill="rgba(240,223,176,0.12)" stroke="rgba(240,223,176,0.68)" stroke-width="2"/>
                <path d="M250 236q18 16 50 16q32 0 50-16l26 140q10 76-20 110q-30 34-56 34q-26 0-56-34q-30-34-20-110Z"
                      fill="rgba(255,255,255,0.04)" stroke="rgba(240,223,176,0.72)" stroke-width="2"/>
                <path d="M244 258q18 76 56 132q38-56 56-132" fill="none" stroke="rgba(240,223,176,0.4)" stroke-width="1.8"/>
                <text x="300" y="710" text-anchor="middle" fill="#f4e8c8" font-family="Cormorant Garamond, serif" font-size="34" letter-spacing="3">SOFT VEIL</text>
              </svg>
            </div>
          </button>

          <button class="gallery-item reveal" data-caption="Eid Evening Glow">
            <div class="thumb">
              <svg viewBox="0 0 600 760" xmlns="http://www.w3.org/2000/svg">
                <rect width="600" height="760" fill="#10254d"/>
                <circle cx="455" cy="118" r="105" fill="rgba(215,185,119,0.14)"/>
                <path d="M415 95a36 36 0 1 1-22-66a28 28 0 1 0 22 66Z" fill="#e4c98c"/>
                <path d="M170 160 Q300 65 430 160" fill="none" stroke="rgba(240,223,176,0.2)" stroke-width="2"/>
                <circle cx="300" cy="186" r="30" fill="rgba(255,255,255,0.05)" stroke="rgba(240,223,176,0.6)" stroke-width="2"/>
                <path d="M246 252q24-30 54-30q30 0 54 30q-8 46-8 92l60 254q4 20-18 32q-22 12-88 12q-66 0-88-12q-22-12-18-32l60-254q0-46-8-92Z"
                      fill="rgba(255,255,255,0.04)" stroke="rgba(240,223,176,0.72)" stroke-width="2"/>
                <path d="M240 336q60 30 120 0" fill="none" stroke="rgba(240,223,176,0.38)" stroke-width="1.8"/>
                <path d="M230 430q70 36 140 0" fill="none" stroke="rgba(240,223,176,0.32)" stroke-width="1.8"/>
                <path d="M220 528q80 42 160 0" fill="none" stroke="rgba(240,223,176,0.28)" stroke-width="1.8"/>
                <text x="300" y="710" text-anchor="middle" fill="#f4e8c8" font-family="Cormorant Garamond, serif" font-size="34" letter-spacing="3">EID NIGHT</text>
              </svg>
            </div>
          </button>

          <button class="gallery-item reveal" data-caption="Pearl Modest Layers">
            <div class="thumb">
              <svg viewBox="0 0 600 760" xmlns="http://www.w3.org/2000/svg">
                <rect width="600" height="760" fill="#09172e"/>
                <path d="M150 165 Q300 60 450 165" fill="none" stroke="rgba(240,223,176,0.18)" stroke-width="2"/>
                <path d="M180 185 Q300 92 420 185" fill="none" stroke="rgba(255,255,255,0.07)" stroke-width="1.5"/>
                <g opacity="0.72">
                  <circle cx="120" cy="250" r="3.3" fill="#e4c98c"/>
                  <circle cx="140" cy="235" r="3.3" fill="#e4c98c"/>
                  <circle cx="155" cy="255" r="3.3" fill="#e4c98c"/>
                  <circle cx="138" cy="272" r="3.3" fill="#e4c98c"/>
                  <circle cx="105" cy="272" r="3.3" fill="#e4c98c"/>
                </g>
                <circle cx="300" cy="188" r="30" fill="rgba(255,255,255,0.05)" stroke="rgba(240,223,176,0.6)" stroke-width="2"/>
                <path d="M250 254q22-32 50-32q28 0 50 32q-6 40-6 86l52 246q4 20-16 31q-20 11-80 11t-80-11q-20-11-16-31l52-246q0-46-6-86Z"
                      fill="rgba(255,255,255,0.04)" stroke="rgba(240,223,176,0.72)" stroke-width="2"/>
                <path d="M240 410q60 34 120 0" fill="none" stroke="rgba(240,223,176,0.34)" stroke-width="1.8"/>
                <text x="300" y="710" text-anchor="middle" fill="#f4e8c8" font-family="Cormorant Garamond, serif" font-size="34" letter-spacing="3">PEARL</text>
              </svg>
            </div>
          </button>

          <button class="gallery-item reveal" data-caption="Crescent Couture">
            <div class="thumb">
              <svg viewBox="0 0 600 760" xmlns="http://www.w3.org/2000/svg">
                <rect width="600" height="760" fill="#0b2143"/>
                <circle cx="455" cy="116" r="98" fill="rgba(215,185,119,0.14)"/>
                <path d="M415 93a34 34 0 1 1-20-62a27 27 0 1 0 20 62Z" fill="#e4c98c"/>
                <path d="M168 158 Q300 63 432 158" fill="none" stroke="rgba(240,223,176,0.2)" stroke-width="2"/>
                <path d="M170 176 V620 Q300 700 430 620 V176" fill="none" stroke="rgba(240,223,176,0.14)" stroke-width="1.5"/>
                <circle cx="300" cy="188" r="30" fill="rgba(255,255,255,0.05)" stroke="rgba(240,223,176,0.6)" stroke-width="2"/>
                <path d="M248 254q24-32 52-32q28 0 52 32q-8 42-8 88l56 252q4 20-16 32q-20 12-84 12t-84-12q-20-12-16-32l56-252q0-46-8-88Z"
                      fill="rgba(255,255,255,0.04)" stroke="rgba(240,223,176,0.72)" stroke-width="2"/>
                <path d="M244 338q56 30 112 0" fill="none" stroke="rgba(240,223,176,0.4)" stroke-width="1.8"/>
                <path d="M236 430q64 36 128 0" fill="none" stroke="rgba(240,223,176,0.32)" stroke-width="1.8"/>
                <text x="300" y="710" text-anchor="middle" fill="#f4e8c8" font-family="Cormorant Garamond, serif" font-size="34" letter-spacing="3">CRESCENT</text>
              </svg>
            </div>
          </button>

          <button class="gallery-item reveal" data-caption="Garden of Modesty">
            <div class="thumb">
              <svg viewBox="0 0 600 760" xmlns="http://www.w3.org/2000/svg">
                <rect width="600" height="760" fill="#0a1c38"/>
                <circle cx="140" cy="605" r="120" fill="rgba(215,185,119,0.08)"/>
                <path d="M168 160 Q300 65 432 160" fill="none" stroke="rgba(240,223,176,0.18)" stroke-width="2"/>
                <g opacity="0.72">
                  <circle cx="455" cy="240" r="3.3" fill="#e4c98c"/>
                  <circle cx="475" cy="225" r="3.3" fill="#e4c98c"/>
                  <circle cx="490" cy="245" r="3.3" fill="#e4c98c"/>
                  <circle cx="473" cy="262" r="3.3" fill="#e4c98c"/>
                  <circle cx="440" cy="262" r="3.3" fill="#e4c98c"/>
                  <circle cx="120" cy="220" r="3.3" fill="#e4c98c"/>
                  <circle cx="140" cy="205" r="3.3" fill="#e4c98c"/>
                  <circle cx="155" cy="225" r="3.3" fill="#e4c98c"/>
                  <circle cx="138" cy="242" r="3.3" fill="#e4c98c"/>
                  <circle cx="105" cy="242" r="3.3" fill="#e4c98c"/>
                </g>
                <circle cx="300" cy="188" r="30" fill="rgba(255,255,255,0.05)" stroke="rgba(240,223,176,0.6)" stroke-width="2"/>
                <path d="M248 254q22-32 52-32q30 0 52 32q-7 46-7 90l54 250q4 20-16 32q-20 12-83 12q-63 0-83-12q-20-12-16-32l54-250q0-44-7-90Z"
                      fill="rgba(255,255,255,0.04)" stroke="rgba(240,223,176,0.72)" stroke-width="2"/>
                <path d="M244 430q56 28 112 0" fill="none" stroke="rgba(240,223,176,0.4)" stroke-width="1.8"/>
                <text x="300" y="710" text-anchor="middle" fill="#f4e8c8" font-family="Cormorant Garamond, serif" font-size="34" letter-spacing="3">GARDEN</text>
              </svg>
            </div>
          </button>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section class="section" id="contact">
      <div class="container">
        <div class="section-head reveal">
          <span class="section-kicker">Contact</span>
          <h2 class="section-title">Let's create something graceful</h2>
          <p class="section-desc">
            For custom design inquiries, collaborations, or styling conversations, send a message below.
          </p>
        </div>

        <div class="contact-shell">
          <div class="panel contact-copy reveal">
            <p>
              Haf's is rooted in premium modest design — soft, elegant, and made with thoughtful detail. Whether you're looking for a signature Eid piece or a timeless wardrobe addition, your vision is welcome here.
            </p>
            <div class="contact-info">
              <div class="info-item">Elegant inquiries for custom modest wear</div>
              <div class="info-item">Styling concept discussions & collaborations</div>
              <div class="info-item">Responses crafted with care and intention</div>
            </div>
          </div>

          <form class="panel contact-form reveal" id="contactForm">
            <div class="form-grid">
              <div class="field">
                <label for="name">Name</label>
                <input id="name" name="name" type="text" placeholder="Your name" required />
              </div>
              <div class="field">
                <label for="email">Email</label>
                <input id="email" name="email" type="email" placeholder="Your email" required />
              </div>
              <div class="field">
                <label for="message">Message</label>
                <textarea id="message" name="message" rows="5" placeholder="Tell me about your idea..." required></textarea>
              </div>
              <div class="submit-row">
                <button type="submit" class="btn btn-primary">Send Message</button>
                <span class="form-note">Softly styled, thoughtfully designed.</span>
              </div>
            </div>
          </form>
        </div>
      </div>
    </section>
  </main>

  <!-- Footer -->
  <footer class="footer">
    <div class="container">Create by <span>Hafsa</span></div>
  </footer>

  <!-- Lightbox -->
  <div class="lightbox" id="lightbox" aria-hidden="true">
    <div class="lightbox-inner">
      <button class="lightbox-close" id="lightboxClose" aria-label="Close gallery">✕</button>
      <div class="lightbox-card">
        <div class="lightbox-media" id="lightboxMedia"></div>
        <div class="lightbox-caption">
          <span id="lightboxCaption">Gallery Preview</span>
        </div>
      </div>
    </div>
  </div>

  <div class="toast" id="toast">Message sent with grace ✨</div>

  <script>
    // Mobile navigation
    const navToggle = document.getElementById('navToggle');
    const navMenu = document.getElementById('navMenu');

    navToggle.addEventListener('click', () => {
      navMenu.classList.toggle('open');
    });

    navMenu.querySelectorAll('a').forEach(link => {
      link.addEventListener('click', () => navMenu.classList.remove('open'));
    });

    // Scroll reveal
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) entry.target.classList.add('visible');
      });
    }, { threshold: 0.14 });

    document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

    // Floating flowers / particles
    const floatingScene = document.getElementById('floatingScene');
    const symbols = ['❁', '✿', '✦', '•', '☾'];
    for (let i = 0; i < 24; i++) {
      const item = document.createElement('span');
      item.className = 'float-item';
      item.textContent = symbols[Math.floor(Math.random() * symbols.length)];
      item.style.left = Math.random() * 100 + '%';
      item.style.fontSize = (Math.random() * 18 + 12) + 'px';
      item.style.animationDuration = (Math.random() * 9 + 12) + 's';
      item.style.animationDelay = (Math.random() * -18) + 's';
      item.style.setProperty('--drift', (Math.random() * 80 - 40) + 'px');
      item.style.opacity = Math.random() * 0.5 + 0.15;
      floatingScene.appendChild(item);
    }

    // Gallery lightbox
    const lightbox = document.getElementById('lightbox');
    const lightboxMedia = document.getElementById('lightboxMedia');
    const lightboxCaption = document.getElementById('lightboxCaption');
    const lightboxClose = document.getElementById('lightboxClose');

    document.querySelectorAll('.gallery-item').forEach(item => {
      item.addEventListener('click', () => {
        const svg = item.querySelector('svg').cloneNode(true);
        lightboxMedia.innerHTML = '';
        lightboxMedia.appendChild(svg);
        lightboxCaption.textContent = item.dataset.caption || 'Gallery Preview';
        lightbox.classList.add('active');
        lightbox.setAttribute('aria-hidden', 'false');
      });
    });

    function closeLightbox() {
      lightbox.classList.remove('active');
      lightbox.setAttribute('aria-hidden', 'true');
    }

    lightboxClose.addEventListener('click', closeLightbox);
    lightbox.addEventListener('click', (e) => {
      if (e.target === lightbox) closeLightbox();
    });
    document.addEventListener('keydown', (e) => {
      if (e.key === 'Escape') closeLightbox();
    });

    // Contact form toast
    const contactForm = document.getElementById('contactForm');
    const toast = document.getElementById('toast');

    contactForm.addEventListener('submit', (e) => {
      e.preventDefault();
      toast.classList.add('show');
      contactForm.reset();
      setTimeout(() => toast.classList.remove('show'), 2600);
    });
  </script>
</body>
</html>
