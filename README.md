<!DOCTYPE html>
google-site-verification=eiZAEA4uVNyC0DrBdyJXB-0BCE8AfyXWFJE1XUW0_Z0
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Creator Ansh — Digital Marketing & Creative Studio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,500;0,9..144,600;1,9..144,400;1,9..144,500&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --c-darkest:#190019;
    --c-dark:#2B124C;
    --c-mid:#522B5B;
    --c-mauve:#854F6C;
    --c-blush:#DFB6B2;
    --c-cream:#FBE4D8;
    --font-display:'Fraunces', serif;
    --font-body:'Space Grotesk', sans-serif;
    --maxw:1180px;
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--c-darkest);
    color:var(--c-cream);
    font-family:var(--font-body);
    line-height:1.5;
    -webkit-font-smoothing:antialiased;
    overflow-x:hidden;
  }
  a{color:inherit; text-decoration:none;}
  img{max-width:100%; display:block;}
  ::selection{background:var(--c-mauve); color:var(--c-cream);}
  :focus-visible{outline:2px solid var(--c-blush); outline-offset:3px;}

  .wrap{max-width:var(--maxw); margin:0 auto; padding:0 32px;}
  @media (max-width:640px){ .wrap{padding:0 22px;} }

  /* ---------- NAV ---------- */
  header{
    position:fixed; top:0; left:0; right:0; z-index:100;
    padding:22px 0;
    background:rgba(25,0,25,0.72);
    backdrop-filter:blur(10px);
    -webkit-backdrop-filter:blur(10px);
    border-bottom:1px solid rgba(223,182,178,0.08);
    transition:padding .3s ease, background .3s ease;
  }
  header.scrolled{ padding:14px 0; background:rgba(25,0,25,0.92); }
  nav.wrap{display:flex; align-items:center; justify-content:space-between;}
  .logo{
    font-family:var(--font-display); font-weight:500; font-style:italic;
    font-size:22px; letter-spacing:0.2px; color:var(--c-cream);
  }
  .nav-links{display:flex; gap:36px; align-items:center;}
  .nav-links a{
    font-size:14.5px; color:var(--c-blush); position:relative; padding:4px 0;
  }
  .nav-links a::after{
    content:''; position:absolute; left:0; bottom:0; height:1px; width:0;
    background:var(--c-cream); transition:width .3s ease;
  }
  .nav-links a:hover::after{width:100%;}
  .nav-links a:hover{color:var(--c-cream);}
  .nav-cta{
    border:1px solid var(--c-blush); padding:9px 20px; border-radius:100px;
    font-size:14px; color:var(--c-cream) !important;
  }
  .nav-cta:hover{ background:var(--c-blush); color:var(--c-darkest) !important; }
  .nav-cta::after{display:none;}
  .burger{display:none; flex-direction:column; gap:5px; cursor:pointer; background:none; border:none;}
  .burger span{width:24px; height:2px; background:var(--c-cream); display:block;}
  @media (max-width:860px){
    .nav-links{
      position:fixed; top:0; right:0; height:100vh; width:min(300px,80vw);
      background:var(--c-dark); flex-direction:column; justify-content:center;
      align-items:flex-start; padding:0 40px; gap:28px;
      transform:translateX(100%); transition:transform .4s ease; z-index:99;
    }
    .nav-links.open{transform:translateX(0);}
    .burger{display:flex;}
  }

  /* ---------- HERO ---------- */
  .hero{
    position:relative; min-height:100vh; display:flex; align-items:center;
    padding-top:120px; padding-bottom:80px; overflow:hidden;
  }
  .hero-glow{
    position:absolute; inset:0; z-index:0; pointer-events:none;
  }
  .hero-glow span{
    position:absolute; border-radius:50%; filter:blur(90px); opacity:0.55;
    animation:drift 16s ease-in-out infinite alternate;
  }
  .hero-glow span:nth-child(1){
    width:480px; height:480px; background:var(--c-mid); top:-140px; left:-120px;
  }
  .hero-glow span:nth-child(2){
    width:420px; height:420px; background:var(--c-mauve); bottom:-160px; right:-100px;
    animation-delay:-6s;
  }
  @keyframes drift{
    0%{ transform:translate(0,0) scale(1); }
    100%{ transform:translate(40px,-30px) scale(1.12); }
  }
  .hero-grid{
    position:relative; z-index:1; display:grid;
    grid-template-columns:1.25fr 0.9fr; gap:60px; align-items:center;
  }
  @media (max-width:920px){ .hero-grid{grid-template-columns:1fr;} }

  .kicker{
    font-size:14px; color:var(--c-blush); font-weight:500;
    display:inline-flex; align-items:center; gap:10px; margin-bottom:22px;
  }
  .kicker .dot{width:7px; height:7px; border-radius:50%; background:var(--c-blush);}

  .hero h1{
    font-family:var(--font-display); font-weight:500;
    font-size:clamp(42px, 6.4vw, 88px); line-height:1.03; letter-spacing:-0.5px;
    opacity:0; transform:translateY(28px);
    animation:riseIn .9s cubic-bezier(.2,.8,.2,1) forwards;
    animation-delay:.15s;
  }
  .hero h1 em{font-style:italic; color:var(--c-blush); font-weight:400;}
  .hero p.lead{
    margin-top:26px; max-width:46ch; font-size:18px; color:rgba(251,228,216,0.78);
    opacity:0; transform:translateY(20px);
    animation:riseIn .9s cubic-bezier(.2,.8,.2,1) forwards; animation-delay:.4s;
  }
  @keyframes riseIn{ to{ opacity:1; transform:translateY(0); } }

  .hero-actions{
    margin-top:38px; display:flex; gap:18px; align-items:center; flex-wrap:wrap;
    opacity:0; transform:translateY(20px);
    animation:riseIn .9s cubic-bezier(.2,.8,.2,1) forwards; animation-delay:.6s;
  }
  .btn-primary{
    position:relative; overflow:hidden; padding:16px 32px; border-radius:100px;
    font-weight:600; font-size:15px; color:var(--c-darkest);
    background:linear-gradient(120deg, var(--c-cream), var(--c-blush), var(--c-cream));
    background-size:220% 100%; background-position:0% 0%;
    transition:background-position .6s ease, transform .25s ease;
    display:inline-block;
  }
  .btn-primary:hover{ background-position:100% 0%; transform:translateY(-2px); }
  .btn-ghost{
    padding:16px 26px; border-radius:100px; font-size:15px; font-weight:500;
    border:1px solid rgba(251,228,216,0.35); color:var(--c-cream);
    transition:border-color .25s ease, background .25s ease;
  }
  .btn-ghost:hover{ border-color:var(--c-cream); background:rgba(251,228,216,0.06); }

  /* orbiting skill cluster */
  .orbit-wrap{
    position:relative; height:420px;
    display:flex; align-items:center; justify-content:center;
    opacity:0; animation:fadeOnly 1s ease forwards; animation-delay:.7s;
  }
  @keyframes fadeOnly{ to{opacity:1;} }
  .orbit-core{
    width:150px; height:150px; border-radius:50%;
    background:radial-gradient(circle at 35% 30%, var(--c-blush), var(--c-mauve) 70%);
    display:flex; align-items:center; justify-content:center; text-align:center;
    font-family:var(--font-display); font-style:italic; font-size:16px; color:var(--c-darkest);
    font-weight:500; box-shadow:0 0 70px rgba(133,79,108,0.55);
    z-index:2; padding:10px;
  }
  .orbit-ring{
    position:absolute; border:1px dashed rgba(223,182,178,0.28); border-radius:50%;
  }
  .orbit-ring.r1{width:280px; height:280px; animation:spin 30s linear infinite;}
  .orbit-ring.r2{width:400px; height:400px; animation:spin 46s linear infinite reverse;}
  @keyframes spin{ to{ transform:rotate(360deg); } }
  .orbit-tag{
    position:absolute; padding:9px 16px; border-radius:100px; font-size:13px;
    background:rgba(43,18,76,0.85); border:1px solid rgba(223,182,178,0.25);
    white-space:nowrap; backdrop-filter:blur(4px);
  }
  @media (max-width:920px){ .orbit-wrap{height:320px; margin-top:20px;} .orbit-ring.r1{width:220px;height:220px;} .orbit-ring.r2{width:300px;height:300px;} }
  @media (max-width:480px){ .orbit-wrap{transform:scale(0.82);} }

  /* ---------- SECTION shared ---------- */
  section{padding:120px 0;}
  @media (max-width:640px){ section{padding:80px 0;} }
  .section-head{max-width:640px; margin-bottom:64px;}
  .section-head h2{
    font-family:var(--font-display); font-weight:500; font-size:clamp(30px,4vw,46px);
    line-height:1.12; letter-spacing:-0.3px;
  }
  .section-head p{margin-top:16px; color:rgba(251,228,216,0.7); font-size:16.5px; max-width:52ch;}

  .reveal{opacity:0; transform:translateY(26px); transition:opacity .8s ease, transform .8s ease;}
  .reveal.in-view{opacity:1; transform:translateY(0);}

  /* ---------- ABOUT ---------- */
  .about{background:var(--c-dark); border-top:1px solid rgba(223,182,178,0.08); border-bottom:1px solid rgba(223,182,178,0.08);}
  .about-grid{display:grid; grid-template-columns:0.7fr 1fr; gap:70px; align-items:start;}
  @media (max-width:820px){ .about-grid{grid-template-columns:1fr; gap:36px;} }
  .about-label{
    font-family:var(--font-display); font-style:italic; font-size:24px; color:var(--c-blush);
  }
  .about p{font-size:17.5px; color:rgba(251,228,216,0.82); max-width:58ch;}
  .about p + p{margin-top:18px;}
  .about-loc{
    margin-top:30px; display:inline-flex; gap:10px; align-items:baseline;
    font-size:14.5px; color:var(--c-blush); border-top:1px solid rgba(223,182,178,0.2); padding-top:18px;
  }

  /* ---------- SERVICES ---------- */
  .services-grid{display:grid; grid-template-columns:repeat(3,1fr); gap:1px; background:rgba(223,182,178,0.14); border:1px solid rgba(223,182,178,0.14);}
  @media (max-width:900px){ .services-grid{grid-template-columns:repeat(2,1fr);} }
  @media (max-width:600px){ .services-grid{grid-template-columns:1fr;} }
  .service-card{
    background:var(--c-darkest); padding:40px 32px; min-height:220px;
    display:flex; flex-direction:column; justify-content:space-between;
    transition:background .35s ease, transform .35s ease;
    position:relative;
  }
  .service-card:hover{ background:var(--c-dark); transform:translateY(-4px); }
  .service-card h3{
    font-family:var(--font-display); font-weight:500; font-size:22px; margin-top:26px;
  }
  .service-card p{font-size:14.5px; color:rgba(251,228,216,0.62); margin-top:10px;}
  .service-mark{
    width:38px; height:38px; border-radius:50%; border:1px solid var(--c-blush);
    display:flex; align-items:center; justify-content:center; font-size:15px; color:var(--c-blush);
    transition:background .3s ease, color .3s ease;
  }
  .service-card:hover .service-mark{background:var(--c-blush); color:var(--c-darkest);}

  /* ---------- WHY / COUNTERS ---------- */
  .why{background:var(--c-dark);}
  .why-grid{display:grid; grid-template-columns:1fr 1fr; gap:60px; align-items:center;}
  @media (max-width:860px){ .why-grid{grid-template-columns:1fr; gap:40px;} }
  .usp-list{display:flex; flex-direction:column; gap:22px;}
  .usp-item{display:flex; gap:16px; align-items:flex-start; padding-bottom:20px; border-bottom:1px solid rgba(223,182,178,0.12);}
  .usp-item:last-child{border-bottom:none;}
  .usp-item .mark{color:var(--c-blush); font-family:var(--font-display); font-style:italic; font-size:20px;}
  .usp-item h4{font-size:16.5px; font-weight:600;}
  .usp-item p{font-size:14.5px; color:rgba(251,228,216,0.65); margin-top:4px;}

  .counters{display:grid; grid-template-columns:1fr 1fr; gap:30px;}
  .counter{
    border:1px solid rgba(223,182,178,0.2); border-radius:18px; padding:30px 26px;
    background:rgba(25,0,25,0.35);
  }
  .counter .num{
    font-family:var(--font-display); font-size:46px; font-weight:500; color:var(--c-cream);
    display:flex; align-items:baseline; gap:2px;
  }
  .counter .label{margin-top:8px; font-size:14px; color:var(--c-blush);}

  /* ---------- PORTFOLIO ---------- */
  .work-grid{display:grid; grid-template-columns:repeat(2,1fr); gap:26px;}
  @media (max-width:760px){ .work-grid{grid-template-columns:1fr;} }
  .work-card{
    position:relative; border-radius:22px; overflow:hidden; aspect-ratio:4/3;
    border:1px solid rgba(223,182,178,0.15); cursor:pointer;
  }
  .work-bg{
    position:absolute; inset:0; transition:transform .6s cubic-bezier(.2,.8,.2,1);
  }
  .work-card:hover .work-bg{transform:scale(1.08);}
  .work-overlay{
    position:absolute; inset:0; display:flex; flex-direction:column; justify-content:flex-end;
    padding:26px; background:linear-gradient(to top, rgba(25,0,25,0.88), rgba(25,0,25,0) 55%);
  }
  .work-overlay .tag{font-size:12.5px; color:var(--c-blush); margin-bottom:6px;}
  .work-overlay h3{font-family:var(--font-display); font-weight:500; font-size:22px;}

  /* ---------- TESTIMONIALS ---------- */
  .testi{background:var(--c-dark);}
  .testi-wrap{max-width:760px; margin:0 auto; text-align:center; position:relative;}
  .testi-slide{display:none;}
  .testi-slide.active{display:block; animation:fadeOnly .6s ease;}
  .testi-slide p.quote{
    font-family:var(--font-display); font-style:italic; font-weight:400;
    font-size:clamp(20px,2.6vw,28px); line-height:1.5; color:var(--c-cream);
  }
  .testi-who{margin-top:26px; font-size:14.5px; color:var(--c-blush);}
  .testi-controls{display:flex; justify-content:center; gap:14px; margin-top:38px;}
  .testi-dot{
    width:9px; height:9px; border-radius:50%; background:rgba(223,182,178,0.3);
    border:none; cursor:pointer; transition:background .3s ease, transform .3s ease;
  }
  .testi-dot.active{background:var(--c-blush); transform:scale(1.3);}

  /* ---------- CONTACT ---------- */
  .contact-grid{display:grid; grid-template-columns:0.85fr 1fr; gap:70px;}
  @media (max-width:860px){ .contact-grid{grid-template-columns:1fr; gap:44px;} }
  .contact-info a{display:block; font-size:16.5px; margin-top:14px; color:var(--c-cream); width:fit-content; position:relative;}
  .contact-info a::after{content:''; position:absolute; left:0; bottom:-2px; height:1px; width:0; background:var(--c-blush); transition:width .3s ease;}
  .contact-info a:hover::after{width:100%;}
  .contact-info h4{font-size:13px; text-transform:none; color:var(--c-blush); margin-top:34px;}
  .contact-info h4:first-child{margin-top:0;}
  .social-row{display:flex; gap:16px; margin-top:34px;}
  .social-row a{
    width:42px; height:42px; border-radius:50%; border:1px solid rgba(223,182,178,0.3);
    display:flex; align-items:center; justify-content:center; font-size:14px;
    transition:background .3s ease, border-color .3s ease;
  }
  .social-row a:hover{background:var(--c-blush); color:var(--c-darkest); border-color:var(--c-blush);}
  .social-row a::after{display:none;}

  form.contact-form{display:flex; flex-direction:column; gap:18px;}
  .field{display:flex; flex-direction:column; gap:8px;}
  .field label{font-size:13.5px; color:var(--c-blush);}
  .field input, .field textarea{
    background:transparent; border:none; border-bottom:1px solid rgba(223,182,178,0.3);
    padding:10px 2px; color:var(--c-cream); font-family:var(--font-body); font-size:15.5px;
    transition:border-color .3s ease;
  }
  .field input:focus, .field textarea:focus{border-color:var(--c-cream); outline:none;}
  .field textarea{resize:vertical; min-height:90px;}
  .submit-btn{
    margin-top:8px; align-self:flex-start; padding:15px 30px; border-radius:100px;
    background:var(--c-cream); color:var(--c-darkest); font-weight:600; font-size:15px;
    border:none; cursor:pointer; transition:transform .25s ease, background .3s ease;
  }
  .submit-btn:hover{transform:translateY(-2px); background:var(--c-blush);}
  .form-note{font-size:13.5px; color:rgba(251,228,216,0.55); margin-top:4px;}

  footer{
    padding:40px 0; border-top:1px solid rgba(223,182,178,0.1);
    display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:14px;
  }
  footer .flogo{font-family:var(--font-display); font-style:italic; font-size:17px;}
  footer small{color:rgba(251,228,216,0.5); font-size:13px;}

  /* ---------- FINAL CTA BAND ---------- */
  .cta-band{
    background:linear-gradient(120deg, var(--c-mid), var(--c-mauve));
    padding:90px 0; text-align:center; position:relative; overflow:hidden;
  }
  .cta-band::before{
    content:''; position:absolute; inset:0;
    background:radial-gradient(circle at 30% 20%, rgba(251,228,216,0.18), transparent 55%);
  }
  .cta-band h2{
    font-family:var(--font-display); font-weight:500; font-size:clamp(28px,4.2vw,46px);
    max-width:680px; margin:0 auto; position:relative; z-index:1; line-height:1.15;
  }
  .cta-band p{
    margin-top:16px; color:rgba(251,228,216,0.85); font-size:16.5px; position:relative; z-index:1;
  }
  .cta-band .hero-actions{ justify-content:center; margin-top:34px; opacity:1; transform:none; animation:none; position:relative; z-index:1; }
  .cta-band .btn-primary{ background:linear-gradient(120deg, var(--c-cream), var(--c-blush), var(--c-cream)); }

  /* ---------- QUICK CONTACT (floating) ---------- */
  .quick-contact{
    position:fixed; right:22px; bottom:22px; z-index:90;
    display:flex; flex-direction:column; gap:12px;
    opacity:0; transform:translateY(14px);
    animation:riseIn .6s ease forwards; animation-delay:1.1s;
  }
  .qc-btn{
    width:54px; height:54px; border-radius:50%;
    display:flex; align-items:center; justify-content:center;
    font-size:20px; color:var(--c-darkest);
    box-shadow:0 6px 24px rgba(25,0,25,0.5);
    transition:transform .25s ease, box-shadow .25s ease;
  }
  .qc-btn.call{ background:linear-gradient(135deg, var(--c-cream), var(--c-blush)); }
  .qc-btn.mail{ background:linear-gradient(135deg, var(--c-blush), var(--c-mauve)); color:var(--c-cream); }
  .qc-btn:hover{ transform:translateY(-3px) scale(1.05); box-shadow:0 10px 30px rgba(25,0,25,0.65); }
  .qc-label{
    position:absolute; right:64px; top:50%; transform:translateY(-50%);
    background:var(--c-dark); color:var(--c-cream); font-size:13px; padding:7px 12px;
    border-radius:8px; white-space:nowrap; opacity:0; pointer-events:none;
    transition:opacity .2s ease;
  }
  .qc-btn:hover .qc-label{opacity:1;}
  @media (max-width:480px){
    .quick-contact{ right:16px; bottom:16px; }
    .qc-btn{ width:48px; height:48px; font-size:18px; }
  }

  @media (prefers-reduced-motion: reduce){
    *{animation-duration:0.01ms !important; animation-iteration-count:1 !important; transition-duration:0.01ms !important;}
    .hero h1, .hero p.lead, .hero-actions, .orbit-wrap{opacity:1 !important; transform:none !important;}
  }
</style>
</head>
<body>

<header id="siteHeader">
  <nav class="wrap">
    <a href="#top" class="logo">Creator Ansh</a>
    <div class="nav-links" id="navLinks">
      <a href="tel:+919424553398">094245 53398</a>
      <a href="mailto:anshsonix@gmail.com">anshsonix@gmail.com</a>
      <a href="#contact" class="nav-cta">Get a free quote</a>
    </div>
    <button class="burger" id="burgerBtn" aria-label="Toggle menu">
      <span></span><span></span><span></span>
    </button>
  </nav>
</header>

<div class="quick-contact">
  <a href="mailto:anshsonix@gmail.com" class="qc-btn mail" aria-label="Email Creator Ansh">
    <span class="qc-label">anshsonix@gmail.com</span>✉
  </a>
  <a href="tel:+919424553398" class="qc-btn call" aria-label="Call Creator Ansh">
    <span class="qc-label">Call 094245 53398</span>☎
  </a>
</div>

<main id="top">

  <!-- HERO -->
  <section class="hero">
    <div class="hero-glow"><span></span><span></span></div>
    <div class="wrap hero-grid">
      <div>
        <div class="kicker"><span class="dot"></span>Based in Jabalpur, Madhya Pradesh</div>
        <h1>Marketing &amp; creative work,<br>made by <em>one studio.</em></h1>
        <p class="lead">Creator Ansh is a one-stop digital studio — strategy, design, film and code under a single roof, built for brands who don't want to manage five vendors to launch one campaign.</p>
        <div class="hero-actions">
          <a href="#contact" class="btn-primary">Get a free quote</a>
          <a href="#services" class="btn-ghost">What we do</a>
        </div>
      </div>
      <div class="orbit-wrap">
        <div class="orbit-ring r1"></div>
        <div class="orbit-ring r2"></div>
        <div class="orbit-core">Creator<br>Ansh</div>
        <div class="orbit-tag" style="top:6%; left:52%;">Digital Marketing</div>
        <div class="orbit-tag" style="top:32%; left:0%;">Web Development</div>
        <div class="orbit-tag" style="bottom:26%; left:2%;">Cinematography</div>
        <div class="orbit-tag" style="bottom:4%; left:46%;">Editing</div>
        <div class="orbit-tag" style="top:30%; right:-2%;">Designing</div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section class="about" id="about">
    <div class="wrap about-grid">
      <div class="reveal">
        <span class="about-label">About the studio</span>
      </div>
      <div class="reveal">
        <p>Creator Ansh started as one person doing everything a small brand needed — shooting the product, cutting the reel, writing the caption, running the ad, building the page it linked to. That's still how the studio works today: fewer handoffs, one point of contact, and a team that understands how each piece connects to the next.</p>
        <p>We work with entrepreneurs and small teams who need marketing that actually ships — not a 40-slide strategy deck, but campaigns, sites and films that go live and get measured.</p>
        <div class="about-loc">📍 Hathital Colony, Jabalpur, Madhya Pradesh 410091</div>
      </div>
    </div>
  </section>

  <!-- SERVICES -->
  <section id="services">
    <div class="wrap">
      <div class="section-head reveal">
        <h2>Five disciplines, one studio.</h2>
        <p>Every service below is handled in-house, so strategy, visuals and execution stay consistent from the first brief to the last export.</p>
      </div>
    </div>
    <div class="services-grid wrap" style="max-width:var(--maxw); margin:0 auto;">
      <div class="service-card">
        <div class="service-mark">↗</div>
        <div>
          <h3>Digital Marketing</h3>
          <p>SEO, paid ads, social media and content strategy built around measurable growth.</p>
        </div>
      </div>
      <div class="service-card">
        <div class="service-mark">◇</div>
        <div>
          <h3>Web Development</h3>
          <p>Fast, responsive websites and landing pages that turn traffic into enquiries.</p>
        </div>
      </div>
      <div class="service-card">
        <div class="service-mark">▷</div>
        <div>
          <h3>Cinematography</h3>
          <p>Product shoots, brand films and reels shot with intent, not just a phone gimbal.</p>
        </div>
      </div>
      <div class="service-card">
        <div class="service-mark">✂</div>
        <div>
          <h3>Editing</h3>
          <p>Colour, pacing and sound design that make raw footage feel like a finished story.</p>
        </div>
      </div>
      <div class="service-card">
        <div class="service-mark">◈</div>
        <div>
          <h3>Designing</h3>
          <p>Logos, decks and social systems built on a palette and type scale that actually holds together.</p>
        </div>
      </div>
      <div class="service-card">
        <div class="service-mark">＋</div>
        <div>
          <h3>Branding</h3>
          <p>Positioning and voice work so every future post, ad and page sounds like the same brand.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- WHY CHOOSE US -->
  <section class="why" id="why">
    <div class="wrap why-grid">
      <div>
        <div class="section-head reveal" style="margin-bottom:34px;">
          <h2>Why brands stay with us</h2>
        </div>
        <div class="usp-list reveal">
          <div class="usp-item">
            <span class="mark">＊</span>
            <div><h4>One team, every discipline</h4><p>No briefing three agencies separately — strategy, shoot and site come from the same room.</p></div>
          </div>
          <div class="usp-item">
            <span class="mark">＊</span>
            <div><h4>Built to launch, not just pitch</h4><p>Every engagement ends in something live: a campaign, a site, a film — not just a proposal.</p></div>
          </div>
          <div class="usp-item">
            <span class="mark">＊</span>
            <div><h4>Direct access to the person doing the work</h4><p>You talk to the person editing the film or writing the code, not an account manager relaying notes.</p></div>
          </div>
        </div>
      </div>
      <div class="counters reveal">
        <div class="counter"><div class="num"><span class="count-up" data-target="80">0</span>+</div><div class="label">Projects delivered</div></div>
        <div class="counter"><div class="num"><span class="count-up" data-target="5">0</span></div><div class="label">Services under one roof</div></div>
        <div class="counter"><div class="num"><span class="count-up" data-target="30">0</span>+</div><div class="label">Brands worked with</div></div>
        <div class="counter"><div class="num"><span class="count-up" data-target="100">0</span>%</div><div class="label">In-house execution</div></div>
      </div>
    </div>
  </section>

  <!-- PORTFOLIO -->
  <section id="work">
    <div class="wrap">
      <div class="section-head reveal">
        <h2>Recent work</h2>
        <p>A few of the projects that moved through the studio — from first shoot to final ad set.</p>
      </div>
      <div class="work-grid reveal">
        <div class="work-card">
          <div class="work-bg" style="background:linear-gradient(135deg,#522B5B,#854F6C);"></div>
          <div class="work-overlay"><div class="tag">Brand film + reels</div><h3>Local Roots Café</h3></div>
        </div>
        <div class="work-card">
          <div class="work-bg" style="background:linear-gradient(135deg,#2B124C,#522B5B);"></div>
          <div class="work-overlay"><div class="tag">Web design &amp; build</div><h3>Studio Nine Interiors</h3></div>
        </div>
        <div class="work-card">
          <div class="work-bg" style="background:linear-gradient(135deg,#854F6C,#DFB6B2);"></div>
          <div class="work-overlay"><div class="tag">Paid ads &amp; SEO</div><h3>Vantage Fitness</h3></div>
        </div>
        <div class="work-card">
          <div class="work-bg" style="background:linear-gradient(135deg,#190019,#522B5B);"></div>
          <div class="work-overlay"><div class="tag">Brand identity</div><h3>Kagaz Stationery Co.</h3></div>
        </div>
      </div>
    </div>
  </section>

  <!-- TESTIMONIALS -->
  <section class="testi" id="testimonials">
    <div class="wrap testi-wrap">
      <div class="section-head reveal" style="margin:0 auto 50px; text-align:center;">
        <h2>What clients say</h2>
      </div>
      <div class="reveal">
        <div class="testi-slide active">
          <p class="quote">"We went from three vendors to one call. The site, the reels and the ad copy finally look like they belong to the same brand."</p>
          <div class="testi-who">— Founder, Local Roots Café</div>
        </div>
        <div class="testi-slide">
          <p class="quote">"Fast turnaround and none of the usual back-and-forth over revisions. What we asked for is what we got, on time."</p>
          <div class="testi-who">— Owner, Studio Nine Interiors</div>
        </div>
        <div class="testi-slide">
          <p class="quote">"Our enquiry rate doubled within the first month of the new site and ad setup going live."</p>
          <div class="testi-who">— Marketing Lead, Vantage Fitness</div>
        </div>
        <div class="testi-controls">
          <button class="testi-dot active" data-i="0" aria-label="Testimonial 1"></button>
          <button class="testi-dot" data-i="1" aria-label="Testimonial 2"></button>
          <button class="testi-dot" data-i="2" aria-label="Testimonial 3"></button>
        </div>
      </div>
    </div>
  </section>

  <!-- FINAL CTA -->
  <section class="cta-band">
    <div class="wrap">
      <h2>Have a launch date in mind? Let's work backward from it.</h2>
      <p>One message gets you a straight answer on timeline and cost — no discovery-call runaround.</p>
      <div class="hero-actions">
        <a href="#contact" class="btn-primary">Get a free quote</a>
        <a href="tel:+919424553398" class="btn-ghost">Call 094245 53398</a>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <div class="wrap contact-grid">
      <div class="reveal">
        <div class="section-head" style="margin-bottom:0;">
          <h2>Let's start something.</h2>
          <p>Tell us a little about the brand and what you're trying to launch — we'll reply within a day.</p>
        </div>
        <div class="contact-info">
          <h4>Call</h4>
          <a href="tel:+919424553398">094245 53398</a>
          <h4>Email</h4>
          <a href="mailto:anshsonix@gmail.com">anshsonix@gmail.com</a>
          <h4>Studio</h4>
          <a href="#" onclick="return false;">Hathital Colony, Jabalpur, MP 410091</a>
        </div>
        <div class="social-row">
          <a href="https://instagram.com/creatoansh" target="_blank" rel="noopener" aria-label="Instagram">IG</a>
          <a href="mailto:anshsonix@gmail.com" aria-label="Email">@</a>
          <a href="tel:+919424553398" aria-label="Call">☎</a>
        </div>
      </div>
      <div class="reveal">
        <form class="contact-form" id="contactForm">
          <div class="field">
            <label for="cf-name">Name</label>
            <input id="cf-name" type="text" required placeholder="Your name">
          </div>
          <div class="field">
            <label for="cf-email">Email</label>
            <input id="cf-email" type="email" required placeholder="you@company.com">
          </div>
          <div class="field">
            <label for="cf-msg">What are you looking to build?</label>
            <textarea id="cf-msg" required placeholder="Tell us about the project"></textarea>
          </div>
          <button type="submit" class="submit-btn">Send message</button>
          <p class="form-note" id="formNote">This opens your email app addressed to Creator Ansh.</p>
        </form>
      </div>
    </div>
  </section>

</main>

<footer class="wrap">
  <span class="flogo">Creator Ansh</span>
  <small>© 2026 Creator Ansh, Jabalpur · Digital Marketing & Creative Studio</small>
</footer>

<script>
  // header shrink on scroll
  const header = document.getElementById('siteHeader');
  window.addEventListener('scroll', () => {
    header.classList.toggle('scrolled', window.scrollY > 30);
  });

  // mobile nav
  const burger = document.getElementById('burgerBtn');
  const navLinks = document.getElementById('navLinks');
  burger.addEventListener('click', () => navLinks.classList.toggle('open'));
  navLinks.querySelectorAll('a').forEach(a => a.addEventListener('click', () => navLinks.classList.remove('open')));

  // scroll reveal
  const revealEls = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('in-view'); io.unobserve(e.target); } });
  }, { threshold: 0.15 });
  revealEls.forEach(el => io.observe(el));

  // counters
  const counters = document.querySelectorAll('.count-up');
  const counterIO = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (!entry.isIntersecting) return;
      const el = entry.target;
      const target = parseInt(el.dataset.target, 10);
      const dur = 1400;
      const start = performance.now();
      function tick(now){
        const p = Math.min((now - start) / dur, 1);
        const eased = 1 - Math.pow(1 - p, 3);
        el.textContent = Math.round(eased * target);
        if (p < 1) requestAnimationFrame(tick);
      }
      requestAnimationFrame(tick);
      counterIO.unobserve(el);
    });
  }, { threshold: 0.6 });
  counters.forEach(c => counterIO.observe(c));

  // testimonial carousel
  const slides = document.querySelectorAll('.testi-slide');
  const dots = document.querySelectorAll('.testi-dot');
  let current = 0;
  function showSlide(i){
    slides[current].classList.remove('active');
    dots[current].classList.remove('active');
    current = i;
    slides[current].classList.add('active');
    dots[current].classList.add('active');
  }
  dots.forEach(d => d.addEventListener('click', () => showSlide(parseInt(d.dataset.i,10))));
  let autoTimer = setInterval(() => showSlide((current + 1) % slides.length), 5500);
  document.querySelector('.testi-wrap').addEventListener('mouseenter', () => clearInterval(autoTimer));
  document.querySelector('.testi-wrap').addEventListener('mouseleave', () => {
    autoTimer = setInterval(() => showSlide((current + 1) % slides.length), 5500);
  });

  // contact form -> mailto
  const form = document.getElementById('contactForm');
  form.addEventListener('submit', function(e){
    e.preventDefault();
    const name = document.getElementById('cf-name').value;
    const email = document.getElementById('cf-email').value;
    const msg = document.getElementById('cf-msg').value;
    const subject = encodeURIComponent('New project enquiry from ' + name);
    const body = encodeURIComponent(msg + '\n\nReply to: ' + email);
    window.location.href = `mailto:anshsonix@gmail.com?subject=${subject}&body=${body}`;
    document.getElementById('formNote').textContent = 'Opening your email app now…';
  });
</script>

</body>
</html>
