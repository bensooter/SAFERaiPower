<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>SAFERai.power | AI Operational Risk Framework & Open-Source Tools</title>
  <meta name="description" content="SAFERai.power is an EPRI-led, OPAI-aligned initiative to build an AI operational risk framework, evidence templates, and open-source assessment tools for the electric sector." />
  <meta name="theme-color" content="#173f63" />
  <meta property="og:title" content="SAFERai.power" />
  <meta property="og:description" content="AI operational risk framework and open-source tools for trusted AI in the electric sector." />
  <meta property="og:type" content="website" />
  <style>
    :root {
      --navy: #173f63;
      --navy-dark: #0b2238;
      --blue: #2e75b6;
      --blue-soft: #eaf4ff;
      --sky: #bdd7ee;
      --gold: #f4a01c;
      --gold-soft: #fff4df;
      --ink: #102033;
      --muted: #5d7088;
      --line: #d8e4f0;
      --paper: #ffffff;
      --wash: #f4f7fb;
      --green: #26744d;
      --shadow: 0 22px 60px rgba(13, 41, 67, .14);
      --shadow-soft: 0 12px 32px rgba(13, 41, 67, .08);
      --radius-xl: 30px;
      --radius-lg: 22px;
      --radius-md: 16px;
      --max: 1160px;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; scroll-padding-top: 118px; }
    body {
      margin: 0;
      background: var(--wash);
      color: var(--ink);
      font-family: Arial, Helvetica, sans-serif;
      line-height: 1.55;
      -webkit-font-smoothing: antialiased;
      text-rendering: optimizeLegibility;
      overflow-x: hidden;
    }

    /* Keeps the site full-width even if GitHub Pages/Jekyll wraps HTML in a narrow theme container. */
    #saferai-site {
      position: relative;
      width: 100vw;
      max-width: 100vw;
      margin-left: calc(50% - 50vw);
      overflow-x: hidden;
      background: var(--wash);
    }

    a { color: inherit; }
    img, svg { max-width: 100%; display: block; }
    .container { width: min(var(--max), calc(100% - 40px)); margin: 0 auto; }
    .section { padding: clamp(58px, 7vw, 92px) 0; }
    .section-tight { padding: clamp(42px, 6vw, 72px) 0; }
    .white { background: #fff; }
    .skip-link {
      position: absolute;
      left: 16px;
      top: -90px;
      z-index: 100;
      background: var(--gold);
      color: #111827;
      border-radius: 999px;
      padding: 10px 14px;
      font-weight: 900;
      text-decoration: none;
    }
    .skip-link:focus { top: 14px; }

    .topbar {
      background: var(--navy-dark);
      color: #dcecff;
      font-size: 13px;
      border-bottom: 1px solid rgba(255,255,255,.12);
    }
    .topbar-inner {
      min-height: 40px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 16px;
    }
    .topbar p { margin: 0; }
    .topbar strong { color: #fff; }
    .topbar a { color: #fff; text-decoration: none; font-weight: 900; white-space: nowrap; }

    .site-header { position: sticky; top: 0; z-index: 50; }
    .nav {
      background: rgba(255,255,255,.96);
      border-bottom: 1px solid rgba(23,63,99,.15);
      box-shadow: 0 10px 30px rgba(13,41,67,.06);
      backdrop-filter: blur(12px);
    }
    .nav-inner {
      min-height: 76px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 24px;
    }
    .brand {
      display: inline-flex;
      align-items: center;
      gap: 12px;
      text-decoration: none;
      min-width: max-content;
    }
    .brand-mark {
      width: 46px;
      height: 46px;
      border-radius: 15px;
      display: grid;
      place-items: center;
      color: #fff;
      background: linear-gradient(135deg, var(--navy), var(--blue));
      box-shadow: 0 14px 30px rgba(23,63,99,.22);
    }
    .brand-mark svg { width: 34px; height: 34px; }
    .brand-name {
      display: block;
      color: var(--navy);
      font-family: Georgia, 'Times New Roman', serif;
      font-weight: 900;
      font-size: 25px;
      letter-spacing: -.04em;
      line-height: 1;
    }
    .brand-sub {
      display: block;
      margin-top: 4px;
      color: var(--muted);
      font-size: 11px;
      font-weight: 900;
      letter-spacing: .12em;
      text-transform: uppercase;
    }
    .nav-links { display: flex; align-items: center; gap: 4px; }
    .nav-links a {
      text-decoration: none;
      color: #29455e;
      font-weight: 900;
      font-size: 14px;
      padding: 10px 12px;
      border-radius: 999px;
      white-space: nowrap;
    }
    .nav-links a:hover { background: var(--blue-soft); color: var(--navy); }
    .nav-links a.nav-cta {
      background: var(--gold);
      color: #151515;
      box-shadow: 0 12px 28px rgba(244,160,28,.24);
      border: 1px solid rgba(184,93,0,.22);
    }
    .nav-links a.nav-cta:hover { background: #ffb53f; color: #111; }
    .mobile-menu { display: none; }

    .hero {
      position: relative;
      overflow: hidden;
      color: #fff;
      background:
        radial-gradient(circle at 12% 12%, rgba(244,160,28,.23), transparent 25%),
        radial-gradient(circle at 86% 18%, rgba(189,215,238,.22), transparent 30%),
        linear-gradient(135deg, #071e32 0%, #173f63 50%, #2e75b6 100%);
      border-bottom: 5px solid var(--gold);
    }
    .hero::before {
      content: "";
      position: absolute;
      inset: 0;
      opacity: .16;
      background-image:
        linear-gradient(rgba(255,255,255,.22) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,.22) 1px, transparent 1px);
      background-size: 46px 46px;
    }
    .hero-grid {
      position: relative;
      display: grid;
      grid-template-columns: minmax(0, 1.12fr) minmax(340px, .88fr);
      gap: clamp(28px, 5vw, 60px);
      align-items: center;
    }
    .eyebrow, .kicker {
      display: inline-flex;
      align-items: center;
      gap: 9px;
      margin: 0 0 12px;
      color: var(--blue);
      font-weight: 950;
      font-size: 12px;
      line-height: 1.2;
      letter-spacing: .14em;
      text-transform: uppercase;
    }
    .eyebrow { color: #cfe9ff; }
    .eyebrow::before, .kicker::before {
      content: "";
      width: 26px;
      height: 3px;
      border-radius: 999px;
      background: var(--gold);
    }
    h1, h2, h3 { margin: 0; line-height: 1.08; letter-spacing: -.04em; }
    h1 {
      max-width: 850px;
      font-family: Georgia, 'Times New Roman', serif;
      font-size: clamp(43px, 6vw, 76px);
      font-weight: 900;
    }
    h2 {
      color: var(--navy);
      font-family: Georgia, 'Times New Roman', serif;
      font-size: clamp(32px, 4vw, 52px);
      font-weight: 900;
    }
    h3 { color: var(--navy); font-size: 23px; }
    .hero-lede {
      max-width: 760px;
      color: #e6f2ff;
      font-size: clamp(18px, 2vw, 23px);
      line-height: 1.45;
      margin: 24px 0 16px;
    }
    .hero-note {
      max-width: 720px;
      margin: 0 0 28px;
      color: #c7dff7;
      font-weight: 750;
    }
    .hero-actions { display: flex; flex-wrap: wrap; gap: 13px; align-items: center; }
    .button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-height: 52px;
      padding: 14px 20px;
      border-radius: 999px;
      border: 1px solid transparent;
      text-decoration: none;
      font-weight: 950;
      cursor: pointer;
      transition: transform .15s ease, box-shadow .15s ease, background .15s ease;
    }
    .button:hover { transform: translateY(-2px); }
    .button-primary { background: var(--gold); color: #111827; box-shadow: 0 16px 36px rgba(244,160,28,.3); }
    .button-primary:hover { background: #ffb53f; }
    .button-secondary { background: rgba(255,255,255,.12); color: #fff; border-color: rgba(255,255,255,.28); }
    .button-secondary:hover { background: rgba(255,255,255,.2); }
    .button-outline { background: #fff; color: var(--navy); border-color: var(--line); box-shadow: var(--shadow-soft); }
    .button-outline:hover { background: var(--blue-soft); }

    .hero-panel {
      background: rgba(255,255,255,.97);
      color: var(--ink);
      border-radius: var(--radius-xl);
      box-shadow: 0 28px 80px rgba(0,0,0,.28);
      border: 1px solid rgba(255,255,255,.36);
      padding: clamp(24px, 3.4vw, 34px);
    }
    .panel-label {
      display: inline-block;
      margin-bottom: 15px;
      padding: 7px 11px;
      border-radius: 999px;
      background: var(--blue-soft);
      border: 1px solid #cfe1f3;
      color: var(--navy);
      font-size: 12px;
      font-weight: 950;
      letter-spacing: .1em;
      text-transform: uppercase;
    }
    .hero-panel h2 { font-size: clamp(28px, 3.2vw, 40px); }
    .hero-panel p { color: var(--muted); margin: 12px 0 0; }
    .build-list { display: grid; gap: 12px; margin-top: 22px; }
    .build-list div {
      border: 1px solid var(--line);
      border-radius: 17px;
      padding: 15px 16px;
      background: #fbfdff;
    }
    .build-list strong { display: block; color: var(--navy); font-size: 17px; }
    .build-list span { display: block; color: var(--muted); margin-top: 3px; }

    .section-head { max-width: 840px; margin-bottom: 30px; }
    .section-head.center { margin-left: auto; margin-right: auto; text-align: center; }
    .section-head.center .kicker { justify-content: center; }
    .section-head p:not(.kicker) { color: var(--muted); font-size: 18px; margin: 15px 0 0; }

    .split {
      display: grid;
      grid-template-columns: .95fr 1.05fr;
      gap: clamp(24px, 5vw, 54px);
      align-items: start;
    }
    .callout {
      background: #fff;
      border: 1px solid var(--line);
      border-radius: var(--radius-xl);
      padding: clamp(24px, 3vw, 34px);
      box-shadow: var(--shadow-soft);
    }
    .callout h3 { margin-bottom: 10px; font-size: 28px; }
    .callout p { color: var(--muted); margin: 0; }
    .callout + .callout { margin-top: 18px; }
    .pressure-grid { display: grid; gap: 13px; }
    .pressure-card {
      display: grid;
      grid-template-columns: 42px 1fr;
      gap: 14px;
      align-items: start;
      background: #fff;
      border: 1px solid var(--line);
      border-radius: 18px;
      padding: 18px;
      box-shadow: 0 10px 24px rgba(13,41,67,.06);
    }
    .pressure-card span {
      width: 42px;
      height: 42px;
      border-radius: 14px;
      display: grid;
      place-items: center;
      background: var(--navy);
      color: #fff;
      font-weight: 950;
    }
    .pressure-card h3 { font-size: 20px; margin-bottom: 5px; }
    .pressure-card p { color: var(--muted); margin: 0; }

    .navy-section {
      color: #fff;
      background:
        radial-gradient(circle at 12% 10%, rgba(244,160,28,.18), transparent 24%),
        linear-gradient(135deg, var(--navy-dark), var(--navy));
    }
    .navy-section h2, .navy-section h3 { color: #fff; }
    .navy-section .section-head p:not(.kicker) { color: #dcecff; }
    .deliver-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 18px;
    }
    .deliver-card {
      background: rgba(255,255,255,.08);
      border: 1px solid rgba(255,255,255,.16);
      border-radius: var(--radius-lg);
      padding: 24px;
      box-shadow: 0 14px 36px rgba(0,0,0,.08);
    }
    .deliver-card .num {
      display: inline-flex;
      margin-bottom: 16px;
      padding: 5px 10px;
      border-radius: 999px;
      background: var(--gold);
      color: #111827;
      font-weight: 950;
      font-size: 12px;
    }
    .deliver-card p { color: #dcecff; margin: 10px 0 0; }
    .principles {
      margin-top: 24px;
      display: grid;
      grid-template-columns: repeat(5, minmax(0,1fr));
      gap: 10px;
    }
    .principles span {
      display: grid;
      place-items: center;
      min-height: 58px;
      padding: 10px;
      border-radius: 16px;
      color: #fff;
      background: rgba(255,255,255,.08);
      border: 1px solid rgba(255,255,255,.14);
      font-weight: 950;
      text-align: center;
    }

    .framework-grid {
      display: grid;
      grid-template-columns: repeat(4, minmax(0,1fr));
      gap: 16px;
    }
    .layer {
      background: #fff;
      border: 1px solid var(--line);
      border-radius: var(--radius-lg);
      padding: 22px;
      box-shadow: var(--shadow-soft);
    }
    .layer span {
      display: inline-block;
      margin-bottom: 12px;
      color: #ad5b00;
      font-size: 12px;
      font-weight: 950;
      letter-spacing: .12em;
      text-transform: uppercase;
    }
    .layer p { color: var(--muted); margin: 10px 0 0; }
    .evidence-card {
      margin-top: 22px;
      display: grid;
      grid-template-columns: .82fr 1.18fr;
      gap: 0;
      border-radius: var(--radius-xl);
      overflow: hidden;
      border: 1px solid var(--line);
      background: #fff;
      box-shadow: var(--shadow);
    }
    .evidence-copy { padding: clamp(24px, 3vw, 34px); background: var(--navy); color: #fff; }
    .evidence-copy h3 { color: #fff; font-size: clamp(27px, 3vw, 38px); }
    .evidence-copy p { color: #dcecff; margin: 12px 0 0; }
    .evidence-list {
      padding: clamp(22px, 3vw, 30px);
      display: grid;
      grid-template-columns: repeat(2, minmax(0,1fr));
      gap: 10px;
      background: linear-gradient(135deg, #ffffff, #f3f9ff);
    }
    .evidence-list span {
      background: #fff;
      border: 1px solid var(--line);
      border-radius: 14px;
      padding: 12px;
      color: #334b63;
      font-weight: 850;
      font-size: 14px;
    }

    .pricing-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0,1fr));
      gap: 20px;
      align-items: stretch;
    }
    .price-card {
      display: flex;
      flex-direction: column;
      background: #fff;
      border: 1px solid var(--line);
      border-radius: var(--radius-lg);
      box-shadow: var(--shadow-soft);
      overflow: hidden;
    }
    .price-head { background: var(--navy); color: #fff; padding: 25px 24px; }
    .price-card.medium .price-head { background: var(--blue); }
    .price-card.small .price-head { background: #5b9bd5; }
    .price-head p { margin: 0 0 8px; font-weight: 950; letter-spacing: .1em; text-transform: uppercase; font-size: 12px; }
    .price-head h3 { color: #fff; font-size: clamp(40px, 5vw, 54px); }
    .price-head span { display: block; color: rgba(255,255,255,.84); font-weight: 800; margin-top: 4px; }
    .price-body { padding: 24px; display: flex; flex-direction: column; flex: 1; gap: 16px; }
    .price-body p { margin: 0; color: #334b63; font-weight: 760; }
    .price-body ul { margin: 0; padding-left: 20px; color: var(--muted); }
    .price-body li { margin: 7px 0; }
    .price-body .button { margin-top: auto; width: 100%; }

    .participation-notes {
      margin-top: 24px;
      display: grid;
      grid-template-columns: repeat(3, minmax(0,1fr));
      gap: 16px;
    }
    .note-card {
      background: #fff;
      border: 1px solid var(--line);
      border-radius: var(--radius-lg);
      padding: 22px;
      box-shadow: var(--shadow-soft);
    }
    .note-card h3 { margin-bottom: 8px; }
    .note-card p { color: var(--muted); margin: 0; }

    .roadmap { display: grid; grid-template-columns: repeat(4, minmax(0,1fr)); gap: 16px; }
    .road-card {
      background: #fff;
      border: 1px solid var(--line);
      border-radius: var(--radius-lg);
      padding: 22px;
      box-shadow: var(--shadow-soft);
    }
    .road-card span {
      display: inline-block;
      margin-bottom: 12px;
      color: #ad5b00;
      font-size: 12px;
      font-weight: 950;
      letter-spacing: .12em;
      text-transform: uppercase;
    }
    .road-card h3 { margin-bottom: 8px; }
    .road-card p { color: var(--muted); margin: 0; }

    .faq-list { display: grid; gap: 10px; max-width: 920px; margin: 0 auto; }
    .faq-list details {
      background: #fff;
      border: 1px solid var(--line);
      border-radius: 18px;
      overflow: hidden;
      box-shadow: 0 8px 20px rgba(13,41,67,.05);
    }
    .faq-list summary {
      list-style: none;
      cursor: pointer;
      color: var(--navy);
      font-weight: 950;
      padding: 18px 20px;
      display: flex;
      justify-content: space-between;
      gap: 16px;
    }
    .faq-list summary::-webkit-details-marker { display: none; }
    .faq-list summary::after { content: "+"; color: var(--blue); font-size: 24px; line-height: 1; }
    .faq-list details[open] summary::after { content: "−"; }
    .faq-list div { padding: 0 20px 20px; color: #40566f; }
    .faq-list p { margin: 0; }

    .cta-section { background: #fff; }
    .cta-card {
      display: grid;
      grid-template-columns: 1fr auto;
      gap: 24px;
      align-items: center;
      color: #fff;
      background:
        radial-gradient(circle at 10% 20%, rgba(244,160,28,.25), transparent 26%),
        linear-gradient(135deg, var(--navy-dark), var(--navy));
      border-radius: var(--radius-xl);
      padding: clamp(30px, 5vw, 54px);
      box-shadow: var(--shadow);
    }
    .cta-card h2 { color: #fff; }
    .cta-card p:not(.kicker) { color: #dcecff; max-width: 760px; font-size: 18px; margin: 14px 0 0; }
    .cta-card .button { min-width: 180px; }

    .footer { background: #071e32; color: #d8e4f0; padding: 32px 0; }
    .footer-grid { display: flex; justify-content: space-between; align-items: flex-start; gap: 22px; flex-wrap: wrap; }
    .footer-brand { color: #fff; font-family: Georgia, 'Times New Roman', serif; font-size: 26px; font-weight: 900; text-decoration: none; }
    .footer p { max-width: 760px; margin: 8px 0 0; color: #b8c8d8; font-size: 14px; }
    .footer-links { display: flex; gap: 14px; flex-wrap: wrap; }
    .footer-links a { color: #fff; text-decoration: none; font-weight: 850; }
    .mobile-contact { display: none; }

    @media (max-width: 1080px) {
      .hero-grid, .split, .evidence-card, .cta-card { grid-template-columns: 1fr; }
      .deliver-grid, .pricing-grid, .participation-notes { grid-template-columns: 1fr; max-width: 760px; margin-left: auto; margin-right: auto; }
      .framework-grid, .roadmap { grid-template-columns: repeat(2, minmax(0,1fr)); }
    }
    @media (max-width: 840px) {
      .container { width: min(100% - 28px, var(--max)); }
      .topbar-inner { justify-content: center; text-align: center; }
      .topbar a { display: none; }
      .nav-inner { min-height: 68px; }
      .brand-mark { width: 42px; height: 42px; border-radius: 13px; }
      .brand-name { font-size: 21px; }
      .brand-sub { display: none; }
      .nav-links { display: none; }
      .mobile-menu { display: block; position: relative; }
      .mobile-menu summary {
        list-style: none;
        cursor: pointer;
        border: 1px solid var(--line);
        background: #fff;
        color: var(--navy);
        border-radius: 12px;
        padding: 10px 12px;
        font-weight: 950;
      }
      .mobile-menu summary::-webkit-details-marker { display: none; }
      .mobile-menu[open] summary { background: var(--blue-soft); }
      .mobile-panel {
        position: fixed;
        left: 14px;
        right: 14px;
        top: 110px;
        z-index: 60;
        display: grid;
        gap: 8px;
        padding: 16px;
        background: #fff;
        border: 1px solid var(--line);
        border-radius: 18px;
        box-shadow: var(--shadow);
      }
      .mobile-panel a {
        text-decoration: none;
        color: var(--navy);
        font-weight: 950;
        padding: 13px 14px;
        border-radius: 14px;
        background: #f8fbff;
      }
      .mobile-panel a.nav-cta { background: var(--gold); color: #111827; text-align: center; }
      .principles, .framework-grid, .evidence-list, .roadmap { grid-template-columns: 1fr; }
      .hero-actions .button, .cta-card .button { width: 100%; }
      .mobile-contact {
        display: block;
        position: fixed;
        left: 14px;
        right: 14px;
        bottom: 12px;
        z-index: 60;
        background: var(--gold);
        color: #111827;
        text-align: center;
        text-decoration: none;
        font-weight: 950;
        padding: 14px 18px;
        border-radius: 999px;
        box-shadow: 0 18px 40px rgba(13,41,67,.24);
      }
      #saferai-site { padding-bottom: 74px; }
    }
    @media (max-width: 520px) {
      .section { padding: 50px 0; }
      h1 { font-size: 40px; }
      h2 { font-size: 31px; }
      .hero-panel, .callout, .deliver-card, .layer, .note-card, .road-card, .price-body { padding: 20px; }
      .pressure-card { grid-template-columns: 1fr; }
      .pressure-card span { width: 38px; height: 38px; border-radius: 13px; }
      .topbar { font-size: 12px; }
    }
    @media (prefers-reduced-motion: reduce) {
      html { scroll-behavior: auto; }
      .button { transition: none; }
      .button:hover { transform: none; }
    }
  </style>
</head>
<body>
<div id="saferai-site">
  <a class="skip-link" href="#main">Skip to content</a>

  <header class="site-header" id="top">
    <div class="topbar">
      <div class="container topbar-inner">
        <p><strong>Founding member engagement | 2026–2028</strong> · EPRI-led · OPAI-aligned · Open-source toolkit path</p>
        <a href="mailto:bsooter@epri.com?subject=SAFERai.power%20Participation%20Inquiry&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us</a>
      </div>
    </div>

    <nav class="nav" aria-label="Primary navigation">
      <div class="container nav-inner">
        <a class="brand" href="#top" aria-label="SAFERai.power home">
          <span class="brand-mark" aria-hidden="true">
            <svg viewBox="0 0 64 64" role="img" focusable="false">
              <path d="M32 4 56 16v16c0 15.6-9.9 24.6-24 28C17.9 56.6 8 47.6 8 32V16L32 4Z" fill="currentColor" opacity=".18"/>
              <path d="M32 9 51 18.5V32c0 12.1-7.4 19.2-19 22-11.6-2.8-19-9.9-19-22V18.5L32 9Z" fill="none" stroke="currentColor" stroke-width="4"/>
              <path d="M24 34h12l-4 13 12-19H32l4-11-12 17Z" fill="#f4a01c"/>
            </svg>
          </span>
          <span>
            <span class="brand-name">SAFERai.power</span>
            <span class="brand-sub">Electric Power Research Institute</span>
          </span>
        </a>

        <div class="nav-links">
          <a href="#why">Why now</a>
          <a href="#deliverables">Deliverables</a>
          <a href="#participate">Participate</a>
          <a href="#roadmap">Roadmap</a>
          <a href="#faq">FAQ</a>
          <a class="nav-cta" href="mailto:bsooter@epri.com?subject=SAFERai.power%20Participation%20Inquiry&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us</a>
        </div>

        <details class="mobile-menu">
          <summary>Menu</summary>
          <div class="mobile-panel">
            <a href="#why">Why now</a>
            <a href="#deliverables">Deliverables</a>
            <a href="#participate">Participate</a>
            <a href="#roadmap">Roadmap</a>
            <a href="#faq">FAQ</a>
            <a class="nav-cta" href="mailto:bsooter@epri.com?subject=SAFERai.power%20Participation%20Inquiry&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us</a>
          </div>
        </details>
      </div>
    </nav>
  </header>

  <main id="main">
    <section class="hero section">
      <div class="container hero-grid">
        <div>
          <p class="eyebrow">Operational risk framework + open-source tools</p>
          <h1>Trusted AI for the electric sector needs an operational risk layer.</h1>
          <p class="hero-lede">SAFERai.power is an EPRI-led, OPAI-aligned initiative to build the risk framework, evidence templates, and open-source assessment tools needed before AI is deployed into utility workflows.</p>
          <p class="hero-note">It is not a new general AI governance model. It extends existing frameworks with power-sector evidence, testing, monitoring, and guardrails for specific utility functions.</p>
          <div class="hero-actions">
            <a class="button button-primary" href="mailto:bsooter@epri.com?subject=SAFERai.power%20Participation%20Inquiry&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us</a>
            <a class="button button-secondary" href="#participate">View participation options</a>
          </div>
        </div>

        <aside class="hero-panel" aria-label="SAFERai.power focus">
          <div class="panel-label">What it creates</div>
          <h2>A common way to evaluate AI by use case, consequence, autonomy, and operating context.</h2>
          <p>Built for utility operations, technology partner diligence, OPAI sandbox learning, and regulatory-facing evidence conversations.</p>
          <div class="build-list">
            <div><strong>Risk framework</strong><span>Risk scenarios, failure modes, autonomy levels, guardrails, and use-case tiers.</span></div>
            <div><strong>Evidence packages</strong><span>AI System Risk File templates for provider and deployer evidence.</span></div>
            <div><strong>Assessment tools</strong><span>Registry-backed workflow, TEVV protocols, monitoring triggers, and open-source components.</span></div>
          </div>
        </aside>
      </div>
    </section>

    <section class="section white" id="why">
      <div class="container split">
        <div>
          <div class="section-head">
            <p class="kicker">Why now</p>
            <h2>AI adoption is accelerating faster than reusable risk evidence.</h2>
            <p>Utilities are moving from experimentation to live use across customer operations, planning, asset analytics, field work, restoration, DER integration, and emerging agentic workflows. Without a shared assessment layer, every utility, provider, and reviewer has to invent its own approach.</p>
          </div>
          <div class="callout">
            <h3>How SAFERai.power fits with OPAI</h3>
            <p>EPRI’s Open Power AI Consortium convenes the ecosystem around shared datasets, open-source libraries, AI accelerators, sandbox evaluation, use-case groups, and implementation partners. SAFERai.power adds the complementary operational risk framework and assessment tools that help evaluate those AI assets before deployment.</p>
          </div>
          <div class="callout">
            <h3>Designed to enhance, not replace</h3>
            <p>The initiative maps to NIST AI RMF, ISO/IEC 42001, IEC 62443, NERC CIP concepts, the EU AI Act, and mature utility programs. The goal is to operationalize those frameworks for electric-sector use cases, not duplicate them.</p>
          </div>
        </div>

        <div class="pressure-grid" aria-label="Sector pressures">
          <article class="pressure-card"><span>1</span><div><h3>Physical consequences</h3><p>AI failures can affect public and worker safety, asset integrity, system stability, and service continuity.</p></div></article>
          <article class="pressure-card"><span>2</span><div><h3>Interconnected systems</h3><p>Actions in one control area can propagate across interconnected operations and markets.</p></div></article>
          <article class="pressure-card"><span>3</span><div><h3>Data constraints</h3><p>Operational, customer, cyber-sensitive, and restricted data require disciplined provenance, access, and evidence handling.</p></div></article>
          <article class="pressure-card"><span>4</span><div><h3>Lifecycle volatility</h3><p>AI performance can drift with weather, DER behavior, topology, load shapes, and changing field reality.</p></div></article>
          <article class="pressure-card"><span>5</span><div><h3>AI supply chain</h3><p>Utilities rely on technology partners, embedded platform features, foundation models, integrators, agents, and update streams.</p></div></article>
        </div>
      </div>
    </section>

    <section class="section navy-section" id="deliverables">
      <div class="container">
        <div class="section-head">
          <p class="kicker">What we are building</p>
          <h2>Not just a document. A framework package that produces usable artifacts.</h2>
          <p>SAFERai.power turns broad principles into evidence templates, assessment protocols, registry fields, pilot playbooks, and open-source toolkit components.</p>
        </div>

        <div class="deliver-grid">
          <article class="deliver-card"><span class="num">01</span><h3>AI System Risk File</h3><p>A minimum evidence package for material AI use cases: purpose, data provenance, capabilities, limitations, oversight, TEVV, deployment conditions, monitoring, incidents, and reassessment triggers.</p></article>
          <article class="deliver-card"><span class="num">02</span><h3>U-SAFER assessment method</h3><p>A stable question set that adapts by utility function, consequence, autonomy level, system access, write authority, and deployment context.</p></article>
          <article class="deliver-card"><span class="num">03</span><h3>AI System Registry schema</h3><p>Minimum fields for owners, providers, deployers, intended purpose, dependencies, permissions, autonomy, risk tier, approval state, monitoring, and change triggers.</p></article>
          <article class="deliver-card"><span class="num">04</span><h3>TEVV and monitoring protocols</h3><p>Testing, evaluation, verification, validation, benchmarking, guardrails, safe fallback behavior, drift monitoring, anomaly monitoring, and revalidation triggers.</p></article>
          <article class="deliver-card"><span class="num">05</span><h3>Provider and deployer evidence</h3><p>Separate evidence tracks for technology partner product claims and local utility deployment reality: configuration, permissions, integrations, training, procedures, and monitoring.</p></article>
          <article class="deliver-card"><span class="num">06</span><h3>Open-source toolkit components</h3><p>Reference components for LLM-assisted intake, registry-backed evidence management, assessment workflow, human review, and reassessment.</p></article>
        </div>

        <div class="principles" aria-label="SAFER principles">
          <span>Safety</span>
          <span>Accountability</span>
          <span>Fairness</span>
          <span>Explainability</span>
          <span>Reliability</span>
        </div>
      </div>
    </section>

    <section class="section white" id="approach">
      <div class="container">
        <div class="section-head center">
          <p class="kicker">Framework architecture</p>
          <h2>Four layers, scaled by risk.</h2>
          <p>Low-consequence uses should be lightweight. Reliability-adjacent, OT-connected, safety-relevant, or actuation-capable uses require deeper evidence, stronger review, and ongoing surveillance.</p>
        </div>

        <div class="framework-grid">
          <article class="layer"><span>Layer 1</span><h3>Data and system context</h3><p>Risk-relevant questions about intended purpose, data sources, rights, quality, restrictions, operating environment, and affected stakeholders.</p></article>
          <article class="layer"><span>Layer 2</span><h3>Registry and lifecycle context</h3><p>System ownership, provider and deployer roles, dependencies, permissions, oversight design, approval status, and change triggers.</p></article>
          <article class="layer"><span>Layer 3</span><h3>Testing and monitoring</h3><p>SAFER attribute assessment, performance and robustness benchmarking, guardrails, safe fallback behavior, drift, and anomaly monitoring.</p></article>
          <article class="layer"><span>Layer 4</span><h3>Risk evidence and continuous monitoring</h3><p>Tiered evidence packages, readiness reviews, monitoring rules, incident playbooks, corrective action, and reassessment triggers.</p></article>
        </div>

        <div class="evidence-card">
          <div class="evidence-copy">
            <h3>Product evidence and deployment evidence are both required.</h3>
            <p>A well-documented AI product can still be deployed unsafely in a specific environment. SAFERai.power addresses both sides of the value chain so providers know what evidence utilities need, and deployers know what local controls must exist.</p>
          </div>
          <div class="evidence-list">
            <span>Provider system card and intended purpose</span>
            <span>Known limits and out-of-scope uses</span>
            <span>Validation and security evidence</span>
            <span>Supplier update and support commitments</span>
            <span>Local deployment architecture</span>
            <span>Permissions, integrations, and procedures</span>
            <span>Human oversight and training</span>
            <span>Monitoring, incident, and rollback plan</span>
          </div>
        </div>
      </div>
    </section>

    <section class="section" id="participate">
      <div class="container">
        <div class="section-head center">
          <p class="kicker">Participation</p>
          <h2>Founding members help shape the framework before expectations harden without them.</h2>
          <p>Participation is a two-year commitment to co-develop the risk framework, evidence templates, OPAI-aligned pilots, and open-source assessment toolkit.</p>
        </div>

        <div class="pricing-grid" aria-label="Participation tiers">
          <article class="price-card large">
            <div class="price-head"><p>Large Scale</p><h3>$40,000</h3><span>per year · $80,000 over two years · annual or upfront payment</span></div>
            <div class="price-body">
              <p>Designed for large organizations.</p>
              <ul>
                <li>Large utilities and major IPPs</li>
                <li>Hyperscalers and AI platform providers</li>
                <li>Infrastructure companies</li>
              </ul>
              <a class="button button-outline" href="mailto:bsooter@epri.com?subject=SAFERai.power%20Participation%20Inquiry&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us</a>
            </div>
          </article>

          <article class="price-card medium">
            <div class="price-head"><p>Medium Scale</p><h3>$25,000</h3><span>per year · $50,000 over two years · annual or upfront payment</span></div>
            <div class="price-body">
              <p>Designed for mid-size organizations.</p>
              <ul>
                <li>Mid-size utilities and regional operators</li>
                <li>ISOs/RTOs</li>
                <li>Established AI solution providers, implementation partners, and advisory partners</li>
              </ul>
              <a class="button button-outline" href="mailto:bsooter@epri.com?subject=SAFERai.power%20Participation%20Inquiry&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us</a>
            </div>
          </article>

          <article class="price-card small">
            <div class="price-head"><p>Small Scale</p><h3>$15,000</h3><span>per year · $30,000 over two years · annual or upfront payment</span></div>
            <div class="price-body">
              <p>Designed for smaller organizations.</p>
              <ul>
                <li>Smaller utilities and electric cooperatives</li>
                <li>Public power districts and municipal utilities</li>
                <li>Early-stage technology companies</li>
              </ul>
              <a class="button button-outline" href="mailto:bsooter@epri.com?subject=SAFERai.power%20Participation%20Inquiry&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us</a>
            </div>
          </article>
        </div>

        <div class="participation-notes">
          <article class="note-card"><h3>Equal substantive access</h3><p>Tier differences reflect organizational scale and capacity to contribute, not commercial control or depth of engagement.</p></article>
          <article class="note-card"><h3>Active SME contribution</h3><p>Each participant is expected to contribute approximately 80 hours of skilled subject-matter-expert time, scoped with the EPRI project team.</p></article>
          <article class="note-card"><h3>APEX stakeholder pathway</h3><p>Government, nonprofit, regulatory, compliance, standards, and policy organizations may engage through EPRI’s APEX pathway on a case-by-case basis.</p></article>
        </div>
      </div>
    </section>

    <section class="section white" id="roadmap">
      <div class="container">
        <div class="section-head center">
          <p class="kicker">Roadmap</p>
          <h2>A learn-and-do cycle that produces value before the final toolkit release.</h2>
          <p>The detailed scope and schedule will be finalized with founding participants, but the two-year development arc is designed to deliver usable artifacts throughout the initiative.</p>
        </div>

        <div class="roadmap">
          <article class="road-card"><span>Months 1–6</span><h3>Foundation</h3><p>OPAI-aligned charter, draft AI System Risk File schema, initial risk classification, autonomy guidance, onboarding, and APEX listening sessions.</p></article>
          <article class="road-card"><span>Months 7–12</span><h3>Build and Pilot</h3><p>Tiered test protocols, AI System Registry prototype, open-source assessment components, monitoring runbooks, and pilot evaluations.</p></article>
          <article class="road-card"><span>Months 13–18</span><h3>Scale and Evidence</h3><p>SAFERai.power v1.0 publication, high-risk safety and reliability case template, product/deployment evidence guidance, and onboarding kit.</p></article>
          <article class="road-card"><span>2028 target</span><h3>Toolkit Release</h3><p>Full open-source toolkit release and transition to an enduring framework stewardship approach.</p></article>
        </div>
      </div>
    </section>

    <section class="section" id="faq">
      <div class="container">
        <div class="section-head center">
          <p class="kicker">FAQ</p>
          <h2>The questions most likely to matter before joining.</h2>
          <p>Kept intentionally focused. The goal is to answer the decision-making questions without turning the website into the prospectus.</p>
        </div>

        <div class="faq-list">
          <details open>
            <summary>Is SAFERai.power an AI governance framework?</summary>
            <div><p>Not in the broad, general sense. SAFERai.power is an operational risk assessment framework, evidence-package model, and open-source tool-building initiative for AI deployed in electric-sector contexts. It supports governance programs by supplying the sector-specific evidence layer they need.</p></div>
          </details>
          <details>
            <summary>How is it different from NIST AI RMF, ISO/IEC 42001, IEC 62443, NERC CIP, or the EU AI Act?</summary>
            <div><p>Those frameworks and requirements are important reference points. SAFERai.power does not replace them. It translates broad lifecycle, safety, cybersecurity, reliability, and management-system concepts into electric-sector use cases, evidence templates, assessment methods, and operational guardrails.</p></div>
          </details>
          <details>
            <summary>How does SAFERai.power relate to OPAI?</summary>
            <div><p>OPAI convenes the ecosystem around shared datasets, open-source libraries, AI accelerators, sandbox evaluation, use-case work groups, and implementation partnering. SAFERai.power adds the complementary operational risk framework and open-source assessment tools for evaluating AI assets and use cases before deployment.</p></div>
          </details>
          <details>
            <summary>What is the AI System Risk File?</summary>
            <div><p>The AI System Risk File is the minimum common evidence package for a material AI use case. It covers intended purpose, data provenance, capabilities and limitations, autonomy and oversight, TEVV results, deployment conditions, monitoring, incidents, and reassessment triggers.</p></div>
          </details>
          <details>
            <summary>What will founding members actually receive?</summary>
            <div><p>Founding members receive working group input, direct engagement with EPRI technical leadership, early access to framework artifacts, participation in pilot use-case development, access to reference implementations and open-source toolkit components ahead of public release, roadmap reviews, and founding member recognition at major milestones.</p></div>
          </details>
          <details>
            <summary>Do all tiers get the same substantive access?</summary>
            <div><p>Yes. Tier differences reflect organizational scale and capacity to contribute. They do not buy commercial advantage over framework design, and they do not create a separate level of access to the substantive work.</p></div>
          </details>
          <details>
            <summary>Can participation be paid all at once or over time?</summary>
            <div><p>Yes. Participation can be paid as a single upfront payment for the full two-year commitment or as two payments across the two-year project.</p></div>
          </details>
          <details>
            <summary>Can Self Direct Funds (SDF) be used for this project?</summary>
            <div><p>Yes. SAFERai.power qualifies for Self Direct Funds (SDF), and SDF funds can be used to pay for participation in the project.</p></div>
          </details>
          <details>
            <summary>Is SME time expected?</summary>
            <div><p>Yes. Each participating organization is expected to contribute approximately 80 hours of skilled SME time. Contributions may come from operational domains such as grid operations, planning, asset management, customer operations, field work, vegetation management, and OT environments, or from digital and AI domains such as AI lifecycle, open-source tooling, testing, evaluation, agentic systems, and risk assessment automation.</p></div>
          </details>
          <details>
            <summary>Why separate product evidence from deployment evidence?</summary>
            <div><p>A technology partner product can be appropriate in principle but still be deployed unsafely in a specific utility environment. Product evidence addresses the provider’s claims, product version, intended purpose, limitations, validation, and support commitments. Deployment evidence addresses local permissions, integrations, procedures, training, oversight, monitoring, and incident response.</p></div>
          </details>
          <details>
            <summary>Will the toolkit make final approval decisions automatically?</summary>
            <div><p>No. The toolkit is intended to help collect evidence, route questions, draft documentation, manage registry-backed workflows, and trigger reassessment. Human owners, reviewers, operators, and domain experts retain authority for consequential decisions.</p></div>
          </details>
          <details>
            <summary>How does SAFERai.power handle autonomy and agentic AI?</summary>
            <div><p>Autonomy is treated as a governed capability, not a feature toggle. The framework considers advisory systems, supervised action, guarded autonomy, and exceptional autonomous use, with stronger safeguards as consequence, system access, write authority, and operational reach increase.</p></div>
          </details>
          <details>
            <summary>Can smaller utilities or early-stage companies participate?</summary>
            <div><p>Yes. The Small Scale tier is designed for smaller utilities, cooperatives, public power districts, municipal utilities, and early-stage technology companies. The framework is also intended to produce templates and tools usable by organizations without large internal AI programs.</p></div>
          </details>
          <details>
            <summary>Can regulatory, standards, or policy organizations engage?</summary>
            <div><p>Government and nonprofit regulatory, compliance, standards, and policy organizations that cannot otherwise join EPRI’s collaborative may be able to participate through EPRI’s APEX pathway on a case-by-case basis.</p></div>
          </details>
          <details>
            <summary>How do we start?</summary>
            <div><p>Start with an initial briefing. The EPRI SAFERai.power team can discuss fit, participation tier, fee structure, potential use cases, SME contribution profile, and working group onboarding.</p></div>
          </details>
        </div>
      </div>
    </section>

    <section class="section-tight cta-section" id="contact">
      <div class="container cta-card">
        <div>
          <p class="kicker">Next step</p>
          <h2>Help define trusted AI adoption for the electric sector.</h2>
          <p>Schedule an initial briefing to discuss the initiative, OPAI alignment, participation tier, and the contribution profile that fits your organization.</p>
        </div>
        <a class="button button-primary" href="mailto:bsooter@epri.com?subject=SAFERai.power%20Participation%20Inquiry&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us</a>
      </div>
    </section>
  </main>

  <footer class="footer">
    <div class="container footer-grid">
      <div>
        <a class="footer-brand" href="#top">SAFERai.power</a>
        <p>AI operational risk framework and open-source tools for trusted AI in the electric sector.</p>
        <p>© 2026 Electric Power Research Institute (EPRI), Inc. All rights reserved. Electric Power Research Institute, EPRI, and TOGETHER…SHAPING THE FUTURE OF ENERGY are registered marks of the Electric Power Research Institute, Inc. in the U.S. and worldwide.</p>
      </div>
      <div class="footer-links">
        <a href="#deliverables">Deliverables</a>
        <a href="#participate">Participate</a>
        <a href="#faq">FAQ</a>
        <a href="mailto:bsooter@epri.com?subject=SAFERai.power%20Participation%20Inquiry&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us</a>
      </div>
    </div>
  </footer>

  <a class="mobile-contact" href="mailto:bsooter@epri.com?subject=SAFERai.power%20Participation%20Inquiry&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us</a>
</div>
  <script>
    document.querySelectorAll('.mobile-panel a').forEach(function(link) {
      link.addEventListener('click', function() {
        var menu = document.querySelector('.mobile-menu');
        if (menu) menu.removeAttribute('open');
      });
    });
  </script>

</body>
</html>
