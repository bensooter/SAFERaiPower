<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>SAFERai.Power | AI Risk Assessment Framework & Tools for the Electric Sector</title>
  <meta name="description" content="SAFERai.Power is an EPRI-led, nonprofit initiative to build a sector-specific AI risk assessment framework, evidence-package templates, and practical tools for AI in electric utility operations." />
  <style>
    :root {
      --navy: #1f4e79;
      --navy-2: #153a5a;
      --blue: #2e75b6;
      --blue-2: #5b9bd5;
      --light: #bdd7ee;
      --sky: #eff6ff;
      --accent: #f4a01c;
      --accent-2: #d97706;
      --green: #2e7d52;
      --green-2: #e8f5ee;
      --ink: #102033;
      --muted: #5d7088;
      --line: #d8e4f0;
      --paper: #ffffff;
      --wash: #f5f8fb;
      --danger: #b42318;
      --shadow: 0 18px 48px rgba(18, 55, 89, .13);
      --shadow-soft: 0 10px 28px rgba(18, 55, 89, .08);
      --radius-lg: 28px;
      --radius-md: 18px;
      --radius-sm: 12px;
      --max: 1180px;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      color: var(--ink);
      background: var(--wash);
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Arial, sans-serif;
      line-height: 1.55;
      -webkit-font-smoothing: antialiased;
      text-rendering: optimizeLegibility;
    }
    a { color: inherit; }
    .wrap { width: min(var(--max), calc(100% - 40px)); margin-inline: auto; }
    .skip-link {
      position: absolute; left: 12px; top: -100px; background: var(--accent); color: #111827;
      padding: 10px 14px; border-radius: 8px; z-index: 50; font-weight: 800;
    }
    .skip-link:focus { top: 12px; }

    .topline {
      background: var(--navy-2);
      color: #dbeafe;
      font-size: 13px;
      letter-spacing: .02em;
      border-bottom: 1px solid rgba(255,255,255,.12);
    }
    .topline .wrap {
      min-height: 42px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 18px;
    }
    .topline strong { color: #fff; }
    .topline a { color: #fff; font-weight: 750; text-decoration: none; }

    .site-header {
      position: sticky;
      top: 0;
      z-index: 40;
      background: rgba(255, 255, 255, .94);
      backdrop-filter: blur(18px);
      border-bottom: 1px solid rgba(31, 78, 121, .16);
    }
    .nav-row {
      display: flex;
      align-items: center;
      justify-content: space-between;
      min-height: 74px;
      gap: 22px;
    }
    .brand {
      display: flex;
      align-items: center;
      gap: 14px;
      text-decoration: none;
      min-width: max-content;
    }
    .brand-mark {
      width: 46px; height: 46px;
      border-radius: 14px;
      background: linear-gradient(135deg, var(--navy), var(--blue));
      color: #fff;
      display: grid;
      place-items: center;
      font-weight: 950;
      box-shadow: 0 10px 24px rgba(31,78,121,.24);
      border: 2px solid rgba(244,160,28,.35);
    }
    .brand-name { font-weight: 950; color: var(--navy); font-size: 23px; line-height: 1; letter-spacing: -.04em; }
    .brand-sub { font-size: 11px; color: var(--muted); font-weight: 800; letter-spacing: .13em; text-transform: uppercase; margin-top: 4px; }

    .nav-links { display: flex; align-items: center; gap: 6px; }
    .nav-links a {
      text-decoration: none;
      color: #27415d;
      font-weight: 760;
      font-size: 14px;
      padding: 10px 12px;
      border-radius: 999px;
      white-space: nowrap;
    }
    .nav-links a:hover { background: var(--sky); color: var(--navy); }
    .cta-small {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      color: #102033 !important;
      background: var(--accent);
      border: 1px solid rgba(180, 95, 0, .2);
      box-shadow: 0 9px 24px rgba(244,160,28,.28);
    }
    .menu-toggle {
      display: none;
      border: 1px solid var(--line);
      background: #fff;
      color: var(--navy);
      font-weight: 850;
      border-radius: 12px;
      padding: 10px 12px;
      cursor: pointer;
    }

    .hero {
      position: relative;
      overflow: hidden;
      background:
        radial-gradient(circle at 8% 12%, rgba(91,155,213,.22), transparent 28%),
        radial-gradient(circle at 92% 16%, rgba(244,160,28,.18), transparent 24%),
        linear-gradient(135deg, #102b46 0%, var(--navy) 50%, #2e75b6 100%);
      color: white;
      border-bottom: 5px solid var(--accent);
    }
    .hero::after {
      content: "";
      position: absolute;
      inset: 0;
      background-image:
        linear-gradient(rgba(255,255,255,.06) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,.06) 1px, transparent 1px);
      background-size: 42px 42px;
      mask-image: linear-gradient(180deg, rgba(0,0,0,.35), rgba(0,0,0,.04));
      pointer-events: none;
    }
    .hero .wrap {
      position: relative;
      z-index: 1;
      display: grid;
      grid-template-columns: 1.08fr .92fr;
      gap: 42px;
      align-items: center;
      padding-block: clamp(58px, 8vw, 106px);
    }
    .eyebrow {
      display: inline-flex;
      gap: 9px;
      align-items: center;
      border: 1px solid rgba(255,255,255,.24);
      background: rgba(255,255,255,.11);
      color: #eaf5ff;
      border-radius: 999px;
      padding: 8px 12px;
      font-size: 13px;
      font-weight: 850;
      letter-spacing: .035em;
      text-transform: uppercase;
      margin-bottom: 18px;
    }
    .pulse { width: 9px; height: 9px; border-radius: 999px; background: var(--accent); box-shadow: 0 0 0 7px rgba(244,160,28,.18); }
    h1, h2, h3 { margin: 0; line-height: 1.05; letter-spacing: -.05em; }
    h1 { font-size: clamp(46px, 6.4vw, 82px); max-width: 810px; }
    .hero-lede {
      font-size: clamp(18px, 2.1vw, 23px);
      color: #dbeafe;
      max-width: 720px;
      margin: 24px 0 28px;
      line-height: 1.45;
    }
    .hero-actions, .section-actions {
      display: flex;
      align-items: center;
      gap: 13px;
      flex-wrap: wrap;
    }
    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      min-height: 50px;
      padding: 13px 18px;
      border-radius: 999px;
      font-weight: 900;
      text-decoration: none;
      border: 1px solid transparent;
      transition: transform .16s ease, box-shadow .16s ease, background .16s ease;
      cursor: pointer;
    }
    .btn:hover { transform: translateY(-2px); }
    .btn-primary { background: var(--accent); color: #141414; box-shadow: 0 14px 34px rgba(244,160,28,.32); }
    .btn-primary:hover { background: #ffb13e; }
    .btn-secondary { color: #fff; background: rgba(255,255,255,.11); border-color: rgba(255,255,255,.24); }
    .btn-secondary:hover { background: rgba(255,255,255,.18); }
    .btn-outline { color: var(--navy); background: #fff; border-color: var(--line); box-shadow: var(--shadow-soft); }
    .btn-outline:hover { background: var(--sky); }
    .microcopy { margin-top: 12px; color: #bfdbfe; font-size: 13px; }
    .microcopy a { color: #fff; font-weight: 850; text-decoration: none; border-bottom: 1px solid rgba(255,255,255,.45); }

    .hero-card {
      background: rgba(255,255,255,.96);
      color: var(--ink);
      border-radius: var(--radius-lg);
      box-shadow: 0 24px 70px rgba(0,0,0,.24);
      overflow: hidden;
      border: 1px solid rgba(255,255,255,.38);
    }
    .hero-card-top { background: linear-gradient(135deg, #f8fbff, #eef6ff); padding: 26px; border-bottom: 1px solid var(--line); }
    .hero-card h2 { font-size: clamp(26px, 3vw, 36px); color: var(--navy); margin-bottom: 10px; }
    .hero-card p { margin: 0; color: var(--muted); }
    .hero-card-body { padding: 24px 26px 26px; }
    .proof-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; margin-top: 18px; }
    .proof-tile {
      padding: 16px 12px;
      border: 1px solid var(--line);
      border-radius: 16px;
      background: white;
      text-align: center;
    }
    .proof-tile strong { display: block; font-size: 25px; color: var(--navy); line-height: 1; letter-spacing: -.04em; }
    .proof-tile span { display: block; margin-top: 6px; color: var(--muted); font-size: 12px; font-weight: 760; }
    .check-list { display: grid; gap: 12px; margin: 0; padding: 0; list-style: none; }
    .check-list li { display: flex; gap: 12px; align-items: flex-start; color: #284158; }
    .check-list li::before {
      content: "✓";
      display: inline-grid;
      place-items: center;
      width: 22px; height: 22px;
      border-radius: 999px;
      flex: 0 0 22px;
      background: var(--green-2);
      color: var(--green);
      font-weight: 950;
      margin-top: 1px;
    }

    section { padding-block: clamp(58px, 8vw, 92px); scroll-margin-top: 90px; }
    .section-head {
      max-width: 850px;
      margin-bottom: 30px;
    }
    .kicker {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      color: var(--blue);
      font-weight: 950;
      letter-spacing: .13em;
      text-transform: uppercase;
      font-size: 12px;
      margin-bottom: 11px;
    }
    .kicker::before { content: ""; width: 24px; height: 3px; border-radius: 999px; background: var(--accent); }
    h2 { font-size: clamp(32px, 4.1vw, 55px); color: var(--navy); }
    .section-lede { font-size: 18px; color: var(--muted); max-width: 820px; margin: 15px 0 0; }

    .card {
      background: var(--paper);
      border: 1px solid var(--line);
      border-radius: var(--radius-md);
      box-shadow: var(--shadow-soft);
    }
    .card-pad { padding: clamp(22px, 3vw, 32px); }
    .grid-2 { display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 22px; }
    .grid-3 { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: 22px; }
    .grid-4 { display: grid; grid-template-columns: repeat(4, minmax(0, 1fr)); gap: 18px; }
    .split { display: grid; grid-template-columns: .92fr 1.08fr; gap: 28px; align-items: stretch; }

    .problem-card { padding: 26px; min-height: 100%; position: relative; overflow: hidden; }
    .problem-card::after { content: ""; position: absolute; inset: auto -40px -60px auto; width: 130px; height: 130px; background: rgba(46,117,182,.09); border-radius: 50%; }
    .problem-card h3 { color: var(--navy); font-size: 21px; margin-bottom: 10px; letter-spacing: -.02em; }
    .problem-card p { color: var(--muted); margin: 0; }
    .failure-list { display: grid; gap: 10px; margin-top: 18px; }
    .failure-pill {
      display: flex;
      justify-content: space-between;
      gap: 12px;
      padding: 12px 14px;
      border-radius: 14px;
      background: #fff;
      border: 1px solid var(--line);
      color: #314a64;
      font-weight: 760;
    }
    .failure-pill span { color: var(--accent-2); font-weight: 950; }

    .principle {
      padding: 22px;
      border-top: 5px solid var(--blue);
      min-height: 100%;
    }
    .principle .icon {
      width: 46px; height: 46px;
      border-radius: 15px;
      display: grid;
      place-items: center;
      background: var(--sky);
      color: var(--navy);
      font-size: 22px;
      margin-bottom: 15px;
    }
    .principle h3 { font-size: 22px; color: var(--navy); margin-bottom: 10px; letter-spacing: -.03em; }
    .principle p { margin: 0; color: var(--muted); }

    .layer-card { padding: 23px; position: relative; overflow: hidden; }
    .layer-num {
      display: inline-grid;
      place-items: center;
      width: 38px; height: 38px;
      border-radius: 12px;
      background: var(--navy);
      color: #fff;
      font-weight: 950;
      margin-bottom: 14px;
    }
    .layer-card h3 { color: var(--navy); font-size: 22px; margin-bottom: 10px; letter-spacing: -.03em; }
    .layer-card p { color: var(--muted); margin: 0; }

    .system-file {
      display: grid;
      grid-template-columns: 1fr 1.25fr;
      gap: 24px;
      align-items: start;
      margin-top: 22px;
      background: linear-gradient(135deg, #fff, #f2f8ff);
      border: 1px solid var(--line);
      border-radius: var(--radius-lg);
      box-shadow: var(--shadow-soft);
      overflow: hidden;
    }
    .system-file .intro { padding: 30px; background: var(--navy); color: #fff; min-height: 100%; }
    .system-file .intro h3 { font-size: 30px; margin-bottom: 12px; }
    .system-file .intro p { color: #dbeafe; margin: 0; }
    .artifact-grid { padding: 24px; display: grid; grid-template-columns: repeat(2, minmax(0,1fr)); gap: 12px; }
    .artifact { background: #fff; border: 1px solid var(--line); border-radius: 14px; padding: 13px 14px; color: #314a64; font-weight: 780; font-size: 14px; }

    .assurance-table {
      overflow: hidden;
      border-radius: var(--radius-md);
      border: 1px solid var(--line);
      box-shadow: var(--shadow-soft);
      background: #fff;
    }
    .assurance-row {
      display: grid;
      grid-template-columns: .8fr 1fr 1fr;
      border-bottom: 1px solid var(--line);
    }
    .assurance-row:last-child { border-bottom: 0; }
    .assurance-row > div { padding: 16px 18px; }
    .assurance-row.header { background: var(--navy); color: #fff; font-weight: 950; }
    .assurance-row:not(.header) > div:first-child { background: var(--sky); color: var(--navy); font-weight: 900; }

    .tier-card { position: relative; overflow: hidden; display: flex; flex-direction: column; min-height: 100%; }
    .tier-head { padding: 24px 24px 18px; color: #fff; background: var(--navy); }
    .tier-head.standard { background: var(--blue); }
    .tier-head.emerging { background: var(--blue-2); }
    .tier-head h3 { font-size: 27px; letter-spacing: -.03em; }
    .tier-head p { margin: 6px 0 0; color: rgba(255,255,255,.86); font-weight: 750; font-size: 14px; }
    .tier-price { padding: 24px; background: #edf4fb; border-bottom: 1px solid var(--line); text-align: center; }
    .tier-price strong { display: block; font-size: clamp(36px, 5vw, 49px); color: var(--navy); line-height: 1; letter-spacing: -.06em; }
    .tier-price span { display: block; font-size: 12px; font-weight: 950; text-transform: uppercase; letter-spacing: .16em; color: #4d6177; margin-top: 8px; }
    .tier-price em { display: block; margin-top: 16px; padding-top: 16px; border-top: 1px solid #d5e4f2; color: var(--navy); font-weight: 900; font-style: normal; }
    .tier-body { padding: 24px; flex: 1; display: flex; flex-direction: column; justify-content: space-between; gap: 20px; }
    .who { font-size: 13px; font-weight: 950; color: var(--blue); letter-spacing: .12em; text-transform: uppercase; margin-bottom: 8px; }
    .tier-body p { margin: 0; color: #314a64; }
    .access-note {
      margin-top: 24px;
      display: grid;
      grid-template-columns: .8fr 1.2fr;
      gap: 20px;
      align-items: center;
      padding: 22px;
      border-radius: var(--radius-md);
      border: 1px dashed rgba(46,117,182,.55);
      background: #f7fbff;
    }
    .access-note strong { color: var(--navy); }

    .receive-card { padding: 23px; min-height: 100%; }
    .receive-card h3 { font-size: 20px; color: var(--navy); margin-bottom: 9px; letter-spacing: -.02em; }
    .receive-card p { margin: 0; color: var(--muted); }

    .roadmap { position: relative; display: grid; gap: 16px; }
    .roadmap::before { content: ""; position: absolute; top: 28px; bottom: 28px; left: 26px; width: 3px; background: #d7e6f5; }
    .road-item { position: relative; display: grid; grid-template-columns: 58px 1fr; gap: 18px; align-items: start; }
    .road-dot { width: 55px; height: 55px; border-radius: 18px; display: grid; place-items: center; background: var(--navy); color: #fff; font-weight: 950; z-index: 1; border: 4px solid #fff; box-shadow: 0 6px 16px rgba(31,78,121,.2); }
    .road-content { padding: 20px 22px; background: #fff; border: 1px solid var(--line); border-radius: 18px; box-shadow: var(--shadow-soft); }
    .road-content h3 { color: var(--navy); font-size: 22px; margin-bottom: 5px; letter-spacing: -.03em; }
    .road-meta { color: var(--accent-2); font-size: 13px; font-weight: 950; letter-spacing: .08em; text-transform: uppercase; margin-bottom: 8px; }
    .road-content p { color: var(--muted); margin: 0; }

    .faq-tools {
      display: grid;
      grid-template-columns: 1fr auto;
      gap: 14px;
      align-items: center;
      margin-bottom: 18px;
    }
    .faq-search {
      width: 100%;
      border: 1px solid var(--line);
      border-radius: 16px;
      min-height: 52px;
      padding: 0 17px;
      font-size: 16px;
      color: var(--ink);
      background: #fff;
      box-shadow: var(--shadow-soft);
    }
    .faq-search:focus { outline: 3px solid rgba(46,117,182,.2); border-color: var(--blue); }
    .faq-filters { display: flex; gap: 8px; flex-wrap: wrap; }
    .filter-btn {
      border: 1px solid var(--line);
      background: #fff;
      color: #314a64;
      padding: 9px 12px;
      border-radius: 999px;
      font-weight: 850;
      cursor: pointer;
    }
    .filter-btn.active { background: var(--navy); color: #fff; border-color: var(--navy); }
    .faq-list { display: grid; gap: 10px; }
    .faq-item {
      background: #fff;
      border: 1px solid var(--line);
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 6px 16px rgba(18,55,89,.05);
    }
    .faq-item[hidden] { display: none; }
    .faq-item summary {
      cursor: pointer;
      padding: 17px 20px;
      font-weight: 900;
      color: var(--navy);
      list-style: none;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 14px;
    }
    .faq-item summary::-webkit-details-marker { display: none; }
    .faq-item summary::after { content: "+"; font-size: 24px; color: var(--blue); font-weight: 850; }
    .faq-item[open] summary::after { content: "–"; }
    .faq-answer { padding: 0 20px 20px; color: #40566f; }
    .faq-answer p { margin: 0; }
    .faq-answer ul { margin: 10px 0 0 20px; padding: 0; }
    .faq-answer li { margin: 6px 0; }
    .faq-count { color: var(--muted); font-size: 14px; font-weight: 780; }

    .final-cta {
      background:
        radial-gradient(circle at 15% 20%, rgba(244,160,28,.22), transparent 25%),
        linear-gradient(135deg, var(--navy-2), var(--navy));
      color: #fff;
      border-radius: var(--radius-lg);
      padding: clamp(30px, 5vw, 54px);
      box-shadow: var(--shadow);
      overflow: hidden;
      position: relative;
    }
    .final-cta h2 { color: #fff; max-width: 760px; }
    .final-cta p { color: #dbeafe; font-size: 18px; max-width: 780px; }
    .contact-panel {
      display: grid;
      grid-template-columns: 1fr auto;
      gap: 20px;
      align-items: center;
      margin-top: 28px;
      background: rgba(255,255,255,.1);
      border: 1px solid rgba(255,255,255,.18);
      border-radius: 22px;
      padding: 20px;
    }
    .contact-panel strong { display: block; font-size: 20px; }
    .contact-panel span { display: block; color: #bfdbfe; margin-top: 2px; }

    footer {
      background: #102033;
      color: #d8e4f0;
      padding: 30px 0;
      font-size: 14px;
    }
    footer .wrap { display: flex; align-items: center; justify-content: space-between; gap: 18px; flex-wrap: wrap; }
    footer a { color: #fff; text-decoration: none; font-weight: 800; }

    .sticky-mobile-cta {
      display: none;
      position: fixed;
      left: 12px;
      right: 12px;
      bottom: 12px;
      z-index: 45;
      background: var(--accent);
      color: #111827;
      box-shadow: 0 18px 46px rgba(17,24,39,.24);
      border-radius: 999px;
      text-align: center;
      padding: 13px 18px;
      font-weight: 950;
      text-decoration: none;
      border: 1px solid rgba(180, 95, 0, .25);
    }

    @media (max-width: 1040px) {
      .nav-links { gap: 2px; }
      .nav-links a { padding-inline: 8px; font-size: 13px; }
      .hero .wrap { grid-template-columns: 1fr; }
      .hero-card { max-width: 760px; }
      .grid-4 { grid-template-columns: repeat(2, minmax(0,1fr)); }
      .grid-3 { grid-template-columns: repeat(2, minmax(0,1fr)); }
      .split, .system-file { grid-template-columns: 1fr; }
      .access-note { grid-template-columns: 1fr; }
      .faq-tools { grid-template-columns: 1fr; }
    }
    @media (max-width: 760px) {
      .wrap { width: min(100% - 28px, var(--max)); }
      .topline .wrap { justify-content: center; text-align: center; }
      .topline .hide-mobile { display: none; }
      .menu-toggle { display: inline-flex; align-items: center; gap: 6px; }
      .nav-row { min-height: 66px; }
      .brand-name { font-size: 20px; }
      .brand-sub { display: none; }
      .brand-mark { width: 41px; height: 41px; border-radius: 12px; }
      .nav-links {
        display: none;
        position: absolute;
        top: 66px;
        left: 0;
        right: 0;
        background: #fff;
        border-bottom: 1px solid var(--line);
        box-shadow: 0 16px 32px rgba(17,24,39,.09);
        padding: 10px 14px 16px;
        flex-direction: column;
        align-items: stretch;
      }
      .nav-links.open { display: flex; }
      .nav-links a { border-radius: 12px; padding: 12px 14px; }
      .nav-links .cta-small { text-align: center; }
      .hero .wrap { padding-block: 50px 64px; }
      .proof-grid { grid-template-columns: 1fr; }
      .hero-actions .btn, .section-actions .btn { width: 100%; }
      .grid-2, .grid-3, .grid-4, .artifact-grid { grid-template-columns: 1fr; }
      .assurance-row { grid-template-columns: 1fr; }
      .assurance-row.header { display: none; }
      .assurance-row > div { border-bottom: 1px solid var(--line); }
      .assurance-row > div:last-child { border-bottom: 0; }
      .contact-panel { grid-template-columns: 1fr; }
      .sticky-mobile-cta { display: block; }
      body { padding-bottom: 72px; }
      footer .wrap { display: block; }
      footer p { margin: 8px 0; }
    }
    @media (prefers-reduced-motion: reduce) {
      html { scroll-behavior: auto; }
      .btn { transition: none; }
      .btn:hover { transform: none; }
    }
  </style>
</head>
<body>
  <a href="#main" class="skip-link">Skip to content</a>

  <div class="topline">
    <div class="wrap">
      <div><strong>Founding Member Engagement</strong> | Practical AI risk assessment, evidence packages, and tools for utility operations</div>
      <div class="hide-mobile">Ready to talk? <a href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Founding%20Member%20Interest&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.Power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">bsooter@epri.com</a></div>
    </div>
  </div>

  <header class="site-header">
    <div class="wrap nav-row">
      <a class="brand" href="#top" aria-label="SAFERai.Power home">
        <div class="brand-mark">S</div>
        <div>
          <div class="brand-name">SAFERai.Power</div>
          <div class="brand-sub">Electric Power Research Institute</div>
        </div>
      </a>
      <button class="menu-toggle" type="button" aria-expanded="false" aria-controls="site-nav">Menu</button>
      <nav id="site-nav" class="nav-links" aria-label="Primary navigation">
        <a href="#scope">Scope</a>
        <a href="#framework">Framework</a>
        <a href="#participate">Participate</a>
        <a href="#roadmap">Roadmap</a>
        <a href="#faq">FAQ</a>
        <a class="cta-small" href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Founding%20Member%20Interest&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.Power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us</a>
      </nav>
    </div>
  </header>

  <main id="main">
    <section id="top" class="hero" aria-label="SAFERai.Power hero">
      <div class="wrap">
        <div>
          <div class="eyebrow"><span class="pulse"></span> Risk assessment & evidence tools for trusted utility AI</div>
          <h1>Practical tools for assessing AI risk in utility operations.</h1>
          <p class="hero-lede">SAFERai.Power is an EPRI-led nonprofit initiative to co-develop a harmonized power-sector AI risk assessment framework, evidence-package templates, and practical tooling for AI solutions deployed across utility operations. It is not a general AI governance model; it provides the operational risk assessment foundation that governance programs need.</p>
          <div class="hero-actions">
            <a class="btn btn-primary" href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Founding%20Member%20Interest&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.Power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us to Join →</a>
            <a class="btn btn-secondary" href="#participate">View participation tiers</a>
          </div>
          <div class="microcopy">Founding member inquiries: <a href="mailto:bsooter@epri.com">bsooter@epri.com</a></div>
        </div>

        <aside class="hero-card" aria-label="SAFERai.Power summary">
          <div class="hero-card-top">
            <h2>Built to help AI move faster where risk is low — and more carefully where consequence is real.</h2>
            <p>Built to standardize the operational evidence that utilities, solution providers, and reviewers need without duplicating broad NIST, ISO/IEC, or internal governance programs.</p>
            <div class="proof-grid" aria-label="Core deliverables snapshot">
              <div class="proof-tile"><strong>Risk</strong><span>tiering & autonomy levels</span></div>
              <div class="proof-tile"><strong>Files</strong><span>evidence package templates</span></div>
              <div class="proof-tile"><strong>Tools</strong><span>registry & assessment workflow</span></div>
            </div>
          </div>
          <div class="hero-card-body">
            <ul class="check-list">
              <li>Harmonized assessment logic for asset management, grid operations, planning, restoration, vegetation, customer/DER, and OT-adjacent workflows.</li>
              <li>Minimum common AI System File and evidence templates for material utility AI use cases.</li>
              <li>Clear distinction between provider product evidence and local deployment evidence.</li>
              <li>Reference registry, assessment workflow, and open-source toolkit components.</li>
            </ul>
          </div>
        </aside>
      </div>
    </section>

    <section id="scope" style="background: #fff;">
      <div class="wrap">
        <div class="section-head">
          <div class="kicker">Clarifying the scope</div>
          <h2>Not another general AI governance model. A power-sector risk framework and toolset.</h2>
          <p class="section-lede">SAFERai.Power is focused on the operational evidence utilities need for AI solutions in asset management, grid operations, system planning, restoration, vegetation management, customer and DER integration, and OT-adjacent environments. The goal is to support existing governance programs with practical risk assessment methods, evidence packages, and tools.</p>
        </div>
        <div class="grid-2">
          <div class="card card-pad">
            <h3 style="font-size: 28px; color: var(--navy); margin-bottom: 16px;">What SAFERai.Power is</h3>
            <ul class="check-list">
              <li>A harmonized AI risk assessment framework for electric-sector operating contexts.</li>
              <li>A set of reusable evidence-package templates that utilities and technology partners can use consistently.</li>
              <li>A practical tool-building effort: registry model, assessment workflow, evidence generator, playbooks, and pilot-tested artifacts.</li>
              <li>A way to create common expectations for product evidence and local deployment evidence before the market fragments.</li>
            </ul>
          </div>
          <div class="card card-pad">
            <h3 style="font-size: 28px; color: var(--navy); margin-bottom: 16px;">What SAFERai.Power is not</h3>
            <ul class="check-list">
              <li>Not a general AI governance model competing with NIST, ISO/IEC, or utility-specific governance programs.</li>
              <li>Not a new law, regulatory regime, or one-size-fits-all compliance checklist.</li>
              <li>Not a vendor selection program or blanket approval of any product, platform, or company.</li>
              <li>Not a paper-only document. The end state is a usable framework, templates, pilots, and open-source tool components.</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section id="why">
      <div class="wrap">
        <div class="section-head">
          <div class="kicker">Why now</div>
          <h2>AI adoption is moving from pilots to operations. Evidence discipline has to catch up before trust breaks.</h2>
          <p class="section-lede">Electric-sector AI is not an ordinary enterprise IT problem. Failures can affect safety, asset integrity, customer outcomes, cybersecurity posture, regulatory exposure, and grid reliability.</p>
        </div>
        <div class="split">
          <div class="card card-pad">
            <h3 style="font-size: 30px; color: var(--navy); margin-bottom: 14px;">The gap is not enthusiasm. The gap is evidence.</h3>
            <p style="color: var(--muted); margin-top: 0;">Without a shared assessment framework and reusable evidence templates, every utility, solution provider, regulator, and auditor invents a different way to classify AI risk, request evidence, monitor drift, bound autonomy, and prove that deployment decisions are defensible.</p>
            <div class="failure-list" aria-label="Recurring AI failure patterns">
              <div class="failure-pill"><span>01</span> Proxy failure</div>
              <div class="failure-pill"><span>02</span> Historical bias</div>
              <div class="failure-pill"><span>03</span> Automation bias</div>
              <div class="failure-pill"><span>04</span> Stale data and context blindness</div>
              <div class="failure-pill"><span>05</span> Misaligned optimization</div>
              <div class="failure-pill"><span>06</span> Accountability gaps</div>
            </div>
          </div>
          <div class="grid-2">
            <div class="card problem-card">
              <h3>Physical consequence</h3>
              <p>AI can influence safety, equipment integrity, operational margins, restoration priorities, and field activity.</p>
            </div>
            <div class="card problem-card">
              <h3>Interconnected systems</h3>
              <p>Actions in one control area can propagate across connected systems, markets, and operating responsibilities.</p>
            </div>
            <div class="card problem-card">
              <h3>Data constraints</h3>
              <p>Customer, operational, cyber-sensitive, nuclear, export-controlled, and BES-sensitive data require careful handling.</p>
            </div>
            <div class="card problem-card">
              <h3>Lifecycle volatility</h3>
              <p>Models can drift as weather, DER behavior, load shapes, field reality, asset condition, and topology change.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section style="background: #fff;" id="framework">
      <div class="wrap">
        <div class="section-head">
          <div class="kicker">The SAFERai.Power approach</div>
          <h2>A utility-specific risk framework that turns broad principles into evidence, tests, and tools.</h2>
          <p class="section-lede">SAFERai.Power complements existing reliability, cybersecurity, risk, and management-system frameworks. It does not replace NIST AI RMF, ISO/IEC 42001, IEC 62443, NERC CIP, the EU AI Act, or internal utility AI governance programs. It supplies the power-sector operational risk assessment layer those programs can use.</p>
        </div>

        <div class="grid-3" aria-label="SAFER principles">
          <div class="card principle"><div class="icon">🛡️</div><h3>Safety</h3><p>Protect public and worker safety, asset integrity, operating margins, and fail-safe behavior.</p></div>
          <div class="card principle"><div class="icon">⚖️</div><h3>Accountability</h3><p>Name owners, decision rights, approvals, change controls, logs, and incident responsibilities.</p></div>
          <div class="card principle"><div class="icon">🤝</div><h3>Fairness</h3><p>Manage unjustified disadvantage for customers, workers, communities, and resource prioritization.</p></div>
          <div class="card principle"><div class="icon">🔎</div><h3>Explainability</h3><p>Make sources, limits, confidence, rationale, provenance, and operating boundaries inspectable.</p></div>
          <div class="card principle"><div class="icon">⚡</div><h3>Reliability</h3><p>Validate AI under representative, stressed, degraded, and changing power-system conditions.</p></div>
          <div class="card principle"><div class="icon">🔐</div><h3>Enabling disciplines</h3><p>Security, privacy, confidentiality, human oversight, and operational resilience run across every layer.</p></div>
        </div>

        <div style="height: 30px;"></div>

        <div class="section-head" style="margin-bottom: 22px;">
          <div class="kicker">Four-layer architecture</div>
          <h2 style="font-size: clamp(30px, 3.6vw, 46px);">Evidence artifacts and assessment tools that scale by use-case risk.</h2>
        </div>
        <div class="grid-4" aria-label="Four framework layers">
          <div class="card layer-card"><div class="layer-num">1</div><h3>Data & system context</h3><p>Data classification, provenance, rights, restrictions, quality, intended purpose, and stakeholder context.</p></div>
          <div class="card layer-card"><div class="layer-num">2</div><h3>AI system registry</h3><p>A practical system of record for identity, ownership, versioning, dependencies, lineage, risk tier, autonomy level, and change triggers.</p></div>
          <div class="card layer-card"><div class="layer-num">3</div><h3>TEVV & monitoring</h3><p>Testing, evaluation, verification, validation, benchmarking, drift monitoring, incident triggers, and revalidation.</p></div>
          <div class="card layer-card"><div class="layer-num">4</div><h3>Evidence review & assurance</h3><p>Tiered evidence review from internal attestation to stronger independent review for high-consequence applications.</p></div>
        </div>

        <div class="system-file" id="system-file">
          <div class="intro">
            <h3>The AI System File</h3>
            <p>The core deliverable: a minimum common evidence package that helps utilities, ISOs/RTOs, technology partners, auditors, and regulators understand what an AI system is for, how it was validated, who owns it, what operating boundaries apply, when it must be reassessed, and how it is monitored after deployment.</p>
          </div>
          <div class="artifact-grid" aria-label="AI System File artifacts">
            <div class="artifact">Impact assessment / intended-use review</div>
            <div class="artifact">AI Use-Case Dossier</div>
            <div class="artifact">Data Sheet & Provenance Record</div>
            <div class="artifact">AI System Card</div>
            <div class="artifact">Autonomy & Human Oversight Plan</div>
            <div class="artifact">TEVV Report</div>
            <div class="artifact">Cyber / OT Integration Assessment</div>
            <div class="artifact">Deployment Profile</div>
            <div class="artifact">Monitoring & Incident Plan</div>
            <div class="artifact">Change & Reassessment Record</div>
          </div>
        </div>
      </div>
    </section>

    <section id="assurance">
      <div class="wrap">
        <div class="section-head">
          <div class="kicker">Assessment where it matters</div>
          <h2>SAFERai.Power separates product evidence from deployment reality.</h2>
          <p class="section-lede">A technology partner product can have strong product evidence and still be deployed unsafely in a particular utility environment. SAFERai.Power addresses both sides of the value chain with practical, scope-bound evidence expectations.</p>
        </div>
        <div class="assurance-table" role="table" aria-label="Product assurance and deployment assurance comparison">
          <div class="assurance-row header" role="row">
            <div role="columnheader">Dimension</div>
            <div role="columnheader">Provider product assurance</div>
            <div role="columnheader">Utility deployment assurance</div>
          </div>
          <div class="assurance-row" role="row">
            <div role="cell">Primary question</div>
            <div role="cell">Is the product, version, and intended use case appropriate for electric-sector deployment?</div>
            <div role="cell">Is the local implementation, permission model, oversight, training, and integration safe in practice?</div>
          </div>
          <div class="assurance-row" role="row">
            <div role="cell">Evidence</div>
            <div role="cell">System card, intended use, dependencies, validation evidence, known limits, security and update discipline.</div>
            <div role="cell">Deployment architecture, integrations, permissions, operator roles, monitoring configuration, procedures, and incident readiness.</div>
          </div>
          <div class="assurance-row" role="row">
            <div role="cell">Change triggers</div>
            <div role="cell">Version changes, new dependencies, expanded intended use, or supplier foundation-model changes.</div>
            <div role="cell">Permission changes, new integrations, increased autonomy, OT boundary changes, or local incidents.</div>
          </div>
        </div>

        <div style="height: 26px;"></div>
        <div class="grid-4" aria-label="Autonomy levels">
          <div class="card receive-card"><h3>Advisory</h3><p>Recommends or drafts; no direct execution. Human decision required.</p></div>
          <div class="card receive-card"><h3>Supervised action</h3><p>Can take limited actions only after explicit approval, with least privilege and rollback.</p></div>
          <div class="card receive-card"><h3>Guarded autonomy</h3><p>Can act within deterministic constraints, escalation logic, and validated boundaries.</p></div>
          <div class="card receive-card"><h3>Autonomous</h3><p>Exceptional for critical workflows; requires enhanced evidence, fail-safe fallback, and executive approval.</p></div>
        </div>
      </div>
    </section>

    <section style="background: #fff;" id="participate">
      <div class="wrap">
        <div class="section-head">
          <div class="kicker">Participation</div>
          <h2>Founding members help build the risk framework and tools before expectations harden without them.</h2>
          <p class="section-lede">Participation is not a license fee. It is a two-year commitment to co-develop the open-source risk assessment framework, evidence-package templates, pilot playbooks, registry model, and practical assessment tools the sector needs, alongside EPRI and fellow founding members.</p>
        </div>
        <div class="grid-3" aria-label="Participation tiers">
          <article class="card tier-card">
            <div class="tier-head"><h3>Lead Partner</h3><p>Sector-shaping participation</p></div>
            <div class="tier-price"><strong>$40,000</strong><span>per year</span><em>$80,000 over two years</em></div>
            <div class="tier-body"><div><div class="who">Who it’s for</div><p>Large utilities, major IPPs, ISOs/RTOs, hyperscalers, AI platform providers, and infrastructure companies.</p></div><a class="btn btn-outline" href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Lead%20Partner%20Interest&body=Hello%2C%0A%0AI%27d%20like%20to%20discuss%20Lead%20Partner%20participation%20in%20SAFERai.Power.%0A%0AOrganization%3A%0ARole%3A%0A">Discuss Lead Partner</a></div>
          </article>
          <article class="card tier-card">
            <div class="tier-head standard"><h3>Standard Partner</h3><p>Core sector participation</p></div>
            <div class="tier-price"><strong>$25,000</strong><span>per year</span><em>$50,000 over two years</em></div>
            <div class="tier-body"><div><div class="who">Who it’s for</div><p>Mid-size utilities, regional operators, established AI vendors, and implementation or advisory partners.</p></div><a class="btn btn-outline" href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Standard%20Partner%20Interest&body=Hello%2C%0A%0AI%27d%20like%20to%20discuss%20Standard%20Partner%20participation%20in%20SAFERai.Power.%0A%0AOrganization%3A%0ARole%3A%0A">Discuss Standard Partner</a></div>
          </article>
          <article class="card tier-card">
            <div class="tier-head emerging"><h3>Emerging Partner</h3><p>Broad sector inclusion</p></div>
            <div class="tier-price"><strong>$15,000</strong><span>per year</span><em>$30,000 over two years</em></div>
            <div class="tier-body"><div><div class="who">Who it’s for</div><p>Smaller utilities, electric cooperatives, public power districts, municipal utilities, and early-stage technology companies.</p></div><a class="btn btn-outline" href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Emerging%20Partner%20Interest&body=Hello%2C%0A%0AI%27d%20like%20to%20discuss%20Emerging%20Partner%20participation%20in%20SAFERai.Power.%0A%0AOrganization%3A%0ARole%3A%0A">Discuss Emerging Partner</a></div>
          </article>
        </div>

        <div class="access-note">
          <div><strong>All tiers receive equivalent substantive access.</strong><br />Tier differentiation reflects organizational scale and capacity to contribute, not depth of engagement or control over the framework.</div>
          <div>No qualified utility, cooperative, or innovator should be excluded because of fee structure alone. Organizations for whom the Emerging Partner tier remains a barrier are encouraged to contact EPRI to discuss participation pathways, including fee adjustments supported by philanthropic or government grant funding.</div>
        </div>

        <div style="height: 32px;"></div>
        <div class="section-head" style="margin-bottom: 20px;">
          <div class="kicker">What participants receive</div>
          <h2 style="font-size: clamp(30px, 3.5vw, 46px);">The value starts before the final toolkit release.</h2>
        </div>
        <div class="grid-3">
          <div class="card receive-card"><h3>Working group seats</h3><p>Input on risk tiers, evidence templates, use-case playbooks, registry fields, tool workflows, and assessment methods, with all tiers participating as equals.</p></div>
          <div class="card receive-card"><h3>Early artifacts</h3><p>AI System File templates, registry schema, U-SAFER assessment protocols, autonomy guidance, provider evidence requests, and deployment evidence packages as they are developed.</p></div>
          <div class="card receive-card"><h3>Pilot participation</h3><p>Opportunities to shape and evaluate representative Tier B and Tier C use cases during the Build and Pilot phase.</p></div>
          <div class="card receive-card"><h3>Convenings</h3><p>Dedicated founding-member working sessions, roadmap reviews, pilot reviews, and cross-sector briefings with EPRI and other participants.</p></div>
          <div class="card receive-card"><h3>Cross-sector engagement</h3><p>Structured engagement with technology providers, regulators, reliability organizations, and policy bodies through APEX.</p></div>
          <div class="card receive-card"><h3>Founding recognition</h3><p>Recognition as a founding member upon v1.0 publication and at major framework milestones.</p></div>
        </div>
      </div>
    </section>

    <section id="roadmap">
      <div class="wrap">
        <div class="section-head">
          <div class="kicker">Development roadmap</div>
          <h2>Two years to move from founding-member buildout to a full open-source toolkit release.</h2>
          <p class="section-lede">Founding members do not wait two years for value. The initiative is structured as a learn-and-do cycle: artifacts are shaped, tested, applied, and improved as they emerge.</p>
        </div>
        <div class="roadmap" aria-label="SAFERai.Power roadmap">
          <div class="road-item"><div class="road-dot">0</div><div class="road-content"><div class="road-meta">Founding member mobilization</div><h3>Onboard the founding cohort</h3><p>Confirm participating organizations, align on scope, identify priority use cases, and organize domain and technology working groups.</p></div></div>
          <div class="road-item"><div class="road-dot">1</div><div class="road-content"><div class="road-meta">Months 1–6</div><h3>Foundation</h3><p>Working group charter, common glossary and data classes, draft AI System File schema, initial risk classification, autonomy guidance, founding member onboarding, APEX listening sessions, and technology-provider working group launch.</p></div></div>
          <div class="road-item"><div class="road-dot">2</div><div class="road-content"><div class="road-meta">Months 7–12</div><h3>Build and Pilot</h3><p>Tiered test protocols, AI System Registry prototype, monitoring and incident runbooks, pilot evaluations on representative use cases, and artifact review cycles.</p></div></div>
          <div class="road-item"><div class="road-dot">3</div><div class="road-content"><div class="road-meta">Months 13–18</div><h3>Scale and Assure</h3><p>SAFERai.Power v1.0 publication, Tier A safety case template, assurance and attestation guidance, onboarding kits, training, and broader sector adoption.</p></div></div>
          <div class="road-item"><div class="road-dot">4</div><div class="road-content"><div class="road-meta">Target: 2028</div><h3>Full open-source toolkit release</h3><p>Release of the full SAFERai.Power toolkit and transition to an enduring stewardship model for the assessment framework and tools.</p></div></div>
        </div>
      </div>
    </section>

    <section style="background: #fff;" id="join-path">
      <div class="wrap">
        <div class="section-head">
          <div class="kicker">Next steps</div>
          <h2>Joining starts with a focused briefing.</h2>
          <p class="section-lede">The decision path is intentionally simple: confirm fit, select participation tier, define the organization’s contribution profile, and onboard into the working groups.</p>
        </div>
        <div class="grid-3">
          <div class="card receive-card"><h3>1. Initial briefing</h3><p>Discuss the risk framework, evidence-package templates, tool roadmap, participation track, expected contribution profile, and questions from your leadership, legal, cyber, operations, or AI teams.</p></div>
          <div class="card receive-card"><h3>2. Participation commitment</h3><p>Confirm tier, annual or two-year upfront fee structure, priority use cases, and SME contribution scope for the working groups.</p></div>
          <div class="card receive-card"><h3>3. Working group onboarding</h3><p>Join SAFERai.Power working groups and begin shaping artifacts, pilots, and assurance expectations.</p></div>
        </div>
        <div class="section-actions" style="margin-top: 26px;">
          <a class="btn btn-primary" href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Initial%20Briefing%20Request&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.Power.%0A%0AOrganization%3A%0ARole%3A%0APotential%20participation%20tier%3A%0AQuestions%3A%0A">Schedule the initial briefing →</a>
          <a class="btn btn-outline" href="#faq">Read the FAQ first</a>
        </div>
      </div>
    </section>

    <section id="faq">
      <div class="wrap">
        <div class="section-head">
          <div class="kicker">FAQ</div>
          <h2>Questions potential participants usually ask before joining.</h2>
          <p class="section-lede">Use the search box or category filters to find the questions most relevant to your organization.</p>
        </div>

        <div class="faq-tools" aria-label="FAQ search and filters">
          <input class="faq-search" id="faqSearch" type="search" placeholder="Search FAQ, e.g., pricing, data sharing, APEX, pilots, open source…" />
          <div class="faq-count" id="faqCount">Showing all FAQs</div>
        </div>
        <div class="faq-filters" role="toolbar" aria-label="FAQ categories">
          <button class="filter-btn active" type="button" data-filter="all">All</button>
          <button class="filter-btn" type="button" data-filter="membership">Membership</button>
          <button class="filter-btn" type="button" data-filter="framework">Framework</button>
          <button class="filter-btn" type="button" data-filter="assurance">Assurance</button>
          <button class="filter-btn" type="button" data-filter="data">Data & security</button>
          <button class="filter-btn" type="button" data-filter="technology">Technology partners</button>
          <button class="filter-btn" type="button" data-filter="regulatory">Regulatory/APEX</button>
          <button class="filter-btn" type="button" data-filter="roadmap">Roadmap</button>
        </div>

        <div class="faq-list" id="faqList">
          <details class="faq-item" data-category="framework" open>
            <summary>What is SAFERai.Power?</summary>
            <div class="faq-answer"><p>SAFERai.Power is an EPRI-led, nonprofit initiative to develop a harmonized AI risk assessment framework, evidence-package templates, and practical tools for AI systems deployed across electric utility operations. It gives utilities, ISOs/RTOs, technology partners, and other stakeholders a common way to classify AI risk, define evidence expectations, bound autonomy, and monitor systems after deployment.</p></div>
          </details>

          <details class="faq-item" data-category="framework">
            <summary>Is SAFERai.Power another AI governance framework?</summary>
            <div class="faq-answer"><p>No. The initiative is being reframed deliberately: SAFERai.Power is a sector-specific AI risk assessment framework, evidence-package model, and tool-building effort. It helps governance by supplying operational risk assessment rigor, but it is not trying to replace broad AI governance frameworks or internal utility programs.</p></div>
          </details>
          <details class="faq-item" data-category="framework">
            <summary>Are you duplicating NIST, ISO/IEC, or existing utility AI programs?</summary>
            <div class="faq-answer"><p>No. NIST, ISO/IEC, regulators, and individual utilities are addressing broad AI governance and management-system needs. SAFERai.Power is narrower: it translates those high-level structures into power-sector risk classifications, evidence templates, test expectations, operating-boundary guidance, and tools for utility use cases.</p></div>
          </details>
          <details class="faq-item" data-category="technology">
            <summary>What tools are you actually trying to build?</summary>
            <div class="faq-answer"><p>The target toolkit includes an AI System Registry reference model, a U-SAFER assessment workflow, evidence-package generators, use-case playbooks, provider evidence request templates, deployment assurance templates, monitoring and reassessment triggers, and human review workflows that remain auditable and registry-backed.</p></div>
          </details>
          <details class="faq-item" data-category="framework">
            <summary>What problem does it solve?</summary>
            <div class="faq-answer"><p>AI adoption is outpacing shared risk assessment and evidence discipline. Without common templates and decision logic, every organization creates its own approach to AI system documentation, validation, autonomy boundaries, supplier diligence, and regulatory defensibility. SAFERai.Power standardizes the evidence and assessment logic so the sector can adopt AI more confidently and consistently.</p></div>
          </details>
          <details class="faq-item" data-category="framework">
            <summary>Why does the electric sector need its own framework?</summary>
            <div class="faq-answer"><p>General-purpose AI governance does not cleanly define the operational evidence needed for utility-specific concerns such as OT boundaries, grid reliability, public and worker safety, asset integrity, customer fairness, system planning assumptions, DER behavior, storm conditions, and regulated operational data. SAFERai.Power translates broad principles into electric-sector risk assessment methods, evidence packages, and tools.</p></div>
          </details>
          <details class="faq-item" data-category="framework">
            <summary>Is SAFERai.Power a compliance checklist?</summary>
            <div class="faq-answer"><p>No. It is a practical assessment framework and tool-building initiative for safe AI scale. It should help teams move faster where risk is low and apply deeper evidence, testing, and review where consequence is high. It is designed to enable adoption, not create a gatekeeping process that blocks useful low-risk AI.</p></div>
          </details>
          <details class="faq-item" data-category="framework">
            <summary>What does SAFER stand for?</summary>
            <div class="faq-answer"><p>SAFER stands for Safety, Accountability, Fairness, Explainability, and Reliability. Reliability is explicit because electric-sector AI must hold up under changing, stressed, and degraded operating conditions, not merely perform well in a demonstration.</p></div>
          </details>
          <details class="faq-item" data-category="framework">
            <summary>How does SAFERai.Power relate to NIST AI RMF, ISO/IEC 42001, IEC 62443, NERC CIP, and the EU AI Act?</summary>
            <div class="faq-answer"><p>SAFERai.Power is designed to complement those structures, not replace them. It maps high-level AI risk, management-system, cybersecurity, reliability, and lifecycle concepts into electric-sector risk classifications, evidence packages, evaluation methods, operating-boundary templates, and assurance pathways.</p></div>
          </details>
          <details class="faq-item" data-category="framework">
            <summary>Will SAFERai.Power replace our internal AI governance program?</summary>
            <div class="faq-answer"><p>No. SAFERai.Power is not a replacement for internal AI governance. Mature organizations can plug its risk assessment methods, evidence templates, and tool workflows into existing risk councils, AI centers of excellence, data governance, cybersecurity, internal audit, legal review, and operational approval processes. Smaller or less mature organizations can use it as a practical starting point.</p></div>
          </details>
          <details class="faq-item" data-category="framework">
            <summary>What is the AI System File?</summary>
            <div class="faq-answer"><p>The AI System File is the minimum common evidence package for a material AI system. It includes intended purpose, data provenance, capabilities and limitations, autonomy and oversight design, TEVV results, deployment conditions, monitoring and incident plans, reassessment triggers, and stronger evidence for higher-consequence applications.</p></div>
          </details>
          <details class="faq-item" data-category="framework">
            <summary>What is U-SAFER?</summary>
            <div class="faq-answer"><p>U-SAFER is the utility/electric-sector assessment method: a stable question set that can be applied across use cases while allowing metrics, thresholds, evidence, and acceptable tradeoffs to vary by domain, risk tier, and autonomy level.</p></div>
          </details>
          <details class="faq-item" data-category="framework">
            <summary>What types of AI will the framework and tools cover?</summary>
            <div class="faq-answer"><p>It is intended to cover traditional machine learning, generative AI, embedded AI features in enterprise platforms, retrieval-augmented systems, agentic workflows, optimization systems, vision systems, operator decision support, and selected OT-connected or control-room-adjacent applications where appropriate.</p></div>
          </details>
          <details class="faq-item" data-category="framework">
            <summary>Will the framework tell us which model or vendor to use?</summary>
            <div class="faq-answer"><p>No. SAFERai.Power standardizes evidence, assessment questions, decision logic, and assurance expectations. It does not prescribe one model architecture, technology stack, vendor, or business model.</p></div>
          </details>
          <details class="faq-item" data-category="framework">
            <summary>How does SAFERai.Power handle human authority?</summary>
            <div class="faq-answer"><p>The framework treats human authority as central. AI may assist consequential work, but it should not become the single point of failure for safety-critical functions. Oversight, escalation, override, appeal, and rollback paths must be explicit and tested for higher-consequence use cases.</p></div>
          </details>
          <details class="faq-item" data-category="assurance">
            <summary>What is the difference between product assurance and deployment assurance?</summary>
            <div class="faq-answer"><p>Product assurance asks whether a provider’s product, version, intended purpose, dependencies, validation evidence, and limitations are suitable for defined electric-sector use cases. Deployment assurance asks whether the local utility implementation, permissions, integrations, procedures, training, monitoring, and human oversight are adequate in practice.</p></div>
          </details>
          <details class="faq-item" data-category="assurance">
            <summary>Will SAFERai.Power certify products or deployments?</summary>
            <div class="faq-answer"><p>The initiative is expected to define assurance and attestation pathways. Any assurance signal should be scope-bound to a product or deployment, version, intended purpose, operating boundary, and reassessment rules. It should not imply blanket approval of an entire company or technology platform.</p></div>
          </details>
          <details class="faq-item" data-category="assurance">
            <summary>What are the risk tiers?</summary>
            <div class="faq-answer"><p>The working model classifies AI by consequence, autonomy level, system access, write authority, oversight, reversibility, and operating context. Low-consequence productivity use requires lighter controls; operationally influential, OT-connected, reliability-adjacent, or safety-critical use requires stronger validation, oversight, monitoring, and assurance.</p></div>
          </details>
          <details class="faq-item" data-category="assurance">
            <summary>How does the framework govern autonomy?</summary>
            <div class="faq-answer"><p>Autonomy is treated as a governed capability, not a feature toggle. Typical levels include Advisory, Supervised Action, Guarded Autonomy, and Autonomous. Higher autonomy requires stronger safeguards such as explicit approval, least privilege, hard constraints, kill switches, deterministic fallback, independent validation, and executive approval where consequences are high.</p></div>
          </details>
          <details class="faq-item" data-category="assurance">
            <summary>Are fully autonomous grid actions allowed?</summary>
            <div class="faq-answer"><p>They are presumed exceptional. SAFERai.Power should explicitly flag out-of-bounds or presumed unacceptable patterns such as AI becoming the sole protective or safety mechanism, or fully autonomous live switching, shedding, or protection-relevant action without deterministic guardrails and an approved safety and reliability case.</p></div>
          </details>
          <details class="faq-item" data-category="assurance">
            <summary>What happens after a system goes live?</summary>
            <div class="faq-answer"><p>Deployment is not the end of assessment. Monitoring should track performance, drift, incidents, exceptions, user behavior, version changes, supplier changes, complaints, and operating-condition changes. Significant changes or incidents should trigger reassessment, suspension, rollback, or retirement when needed.</p></div>
          </details>
          <details class="faq-item" data-category="assurance">
            <summary>What evidence would a high-consequence system need?</summary>
            <div class="faq-answer"><p>Higher-consequence systems may require formal validation, cyber/OT integration assessment, simulator or shadow-mode testing, safety and reliability cases, independent review, enhanced monitoring, manual override validation, incident drills, executive approval, and strict reassessment triggers.</p></div>
          </details>
          <details class="faq-item" data-category="membership">
            <summary>Who should participate?</summary>
            <div class="faq-answer"><p>Utilities, ISOs/RTOs, public power, cooperatives, technology providers, AI platform providers, hyperscalers, infrastructure companies, implementation partners, advisory firms, research organizations, and other stakeholders with a role in trusted AI adoption in the electric sector should consider participating.</p></div>
          </details>
          <details class="faq-item" data-category="membership">
            <summary>What are the participation tiers?</summary>
            <div class="faq-answer"><p>Lead Partner is $40,000 per year, Standard Partner is $25,000 per year, and Emerging Partner is $15,000 per year. Each reflects a two-year participation arc and may be paid annually or upfront.</p></div>
          </details>
          <details class="faq-item" data-category="membership">
            <summary>Does a higher tier buy more influence over the framework?</summary>
            <div class="faq-answer"><p>No. Participation fees support framework development; they do not buy commercial control over framework design. Across all paid tiers, founding members receive equivalent access to the substantive work, and all tiers participate as equals in the collaborative design process.</p></div>
          </details>
          <details class="faq-item" data-category="membership">
            <summary>What does the two-year commitment cover?</summary>
            <div class="faq-answer"><p>The two-year structure covers the foundational development arc for the risk framework, evidence-package templates, pilots, registry model, and tool components. It supports co-development, working group engagement, early artifacts, pilots, and transition toward enduring stewardship.</p></div>
          </details>
          <details class="faq-item" data-category="membership">
            <summary>Can participants join mid-cycle?</summary>
            <div class="faq-answer"><p>Yes. Participants joining mid-cycle are welcome, and fee structures are expected to be prorated.</p></div>
          </details>
          <details class="faq-item" data-category="membership">
            <summary>What if the Emerging Partner tier is still a barrier?</summary>
            <div class="faq-answer"><p>EPRI’s access principle is that no qualified utility, cooperative, or innovator should be excluded due to fee structure alone. Organizations should contact EPRI to discuss participation pathways, including potential fee adjustments supported by philanthropic or government grant funding.</p></div>
          </details>
          <details class="faq-item" data-category="membership">
            <summary>How much staff time is expected?</summary>
            <div class="faq-answer"><p>Every participating organization is expected to contribute skilled subject-matter expert time alongside funding. The planning estimate is approximately 80 hours of SME time per year, with the specific scope defined collaboratively with the EPRI project team.</p></div>
          </details>
          <details class="faq-item" data-category="membership">
            <summary>What kinds of SMEs should we involve?</summary>
            <div class="faq-answer"><p>Useful expertise falls into two broad domains: operational domain expertise such as grid operations, planning, distribution operations, customer operations, asset management, vegetation management, field work, and OT environments; and digital/AI expertise such as AI/ML, MLOps, model registries, open-source tooling, assurance, testing, and agentic systems.</p></div>
          </details>
          <details class="faq-item" data-category="membership">
            <summary>Do participants have to be strong in both utility operations and AI?</summary>
            <div class="faq-answer"><p>No. Many participants will be stronger in one domain. The value of the initiative comes from combining operational expertise, AI expertise, cyber expertise, implementation experience, and regulatory perspective across the founding membership.</p></div>
          </details>
          <details class="faq-item" data-category="membership">
            <summary>What exactly do founding members receive?</summary>
            <div class="faq-answer"><p>Founding members receive working group participation, early access to risk assessment artifacts, pilot participation opportunities, dedicated roadmap and pilot reviews, structured engagement with technology providers and APEX stakeholders, and recognition as founding members at major milestones.</p></div>
          </details>
          <details class="faq-item" data-category="membership">
            <summary>Can we publicly say we are a founding member?</summary>
            <div class="faq-answer"><p>The participation materials anticipate recognition as a founding member upon v1.0 publication and at major framework milestones. Specific public communications, logo use, and press language should be coordinated with EPRI.</p></div>
          </details>
          <details class="faq-item" data-category="membership">
            <summary>How do we start?</summary>
            <div class="faq-answer"><p>Send an email to bsooter@epri.com requesting an initial briefing. The next steps are usually an exploratory conversation, participation tier selection, fee structure confirmation, SME contribution scoping, and working group onboarding.</p></div>
          </details>
          <details class="faq-item" data-category="data">
            <summary>Do we have to share sensitive operational or customer data?</summary>
            <div class="faq-answer"><p>The initiative should support multiple collaboration patterns and does not require unrestricted sharing of sensitive data. Possible mechanisms include de-identification, aggregation, privacy-preserving analysis, synthetic data, reference schemas, metadata, and controlled pilot evidence. Data rights, restrictions, and confidentiality are core framework topics.</p></div>
          </details>
          <details class="faq-item" data-category="data">
            <summary>How does SAFERai.Power handle cyber and OT boundaries?</summary>
            <div class="faq-answer"><p>The framework explicitly accounts for least privilege, zones and segmentation, controlled interfaces, secure access, credential hygiene, supply-chain evidence, logging, monitoring, change approval, rollback discipline, and regulated or BES-sensitive operational data. It adds AI-specific evidence on top of existing OT and reliability practices.</p></div>
          </details>
          <details class="faq-item" data-category="data">
            <summary>How are privacy and confidentiality handled?</summary>
            <div class="faq-answer"><p>Privacy and confidentiality are enabling disciplines across all layers. Data sheets and provenance records should document data sources, rights, restrictions, retention, sensitivity, quality, limitations, access controls, and lawful-use constraints.</p></div>
          </details>
          <details class="faq-item" data-category="data">
            <summary>Will the framework address export-controlled, nuclear, or legally restricted information?</summary>
            <div class="faq-answer"><p>Yes. Restricted statutory data is a distinct data class in the framework concept and should be treated with hard legal gating, strong access controls, and no uncontrolled external model exposure.</p></div>
          </details>
          <details class="faq-item" data-category="data">
            <summary>How does SAFERai.Power handle model drift?</summary>
            <div class="faq-answer"><p>Drift is handled through monitoring plans, key performance and risk indicators, thresholds, revalidation triggers, incident signals, and change records. Reassessment should be triggered by major model changes, data changes, prompt or orchestration changes, expanded intended use, increased autonomy, new integrations, OT boundary changes, supplier changes, incidents, or persistent degradation.</p></div>
          </details>
          <details class="faq-item" data-category="technology">
            <summary>Why should technology providers join?</summary>
            <div class="faq-answer"><p>Technology providers gain a credible path into the electric-sector market by helping define what “power-sector-ready” AI evidence looks like. They can shape provider-side evidence packages and learn how utilities evaluate product assurance, deployment constraints, and operational risk.</p></div>
          </details>
          <details class="faq-item" data-category="technology">
            <summary>Can implementation and advisory partners participate?</summary>
            <div class="faq-answer"><p>Yes. Implementation and advisory partners can help define adoption methods, training curricula, deployment assurance practices, and services the sector will need to operationalize SAFERai.Power at scale.</p></div>
          </details>
          <details class="faq-item" data-category="technology">
            <summary>What supplier evidence will utilities likely request?</summary>
            <div class="faq-answer"><p>Expected evidence may include a system card, declared intended and out-of-scope uses, model or dependency inventory, evaluation summaries, version and update notification discipline, incident support, security evidence, known limitations, and documentation of major third-party dependencies.</p></div>
          </details>
          <details class="faq-item" data-category="technology">
            <summary>Does participation give a vendor preferred commercial status?</summary>
            <div class="faq-answer"><p>No. Participation supports framework development and engagement. It does not buy commercial advantage over framework design, does not create blanket product approval, and should not be represented as a substitute for scoped product or deployment evidence.</p></div>
          </details>
          <details class="faq-item" data-category="technology">
            <summary>Will the toolkit be open source?</summary>
            <div class="faq-answer"><p>The full toolkit is intended to be released as open source after the framework, evidence templates, pilots, and registry-backed assessment workflows are developed and validated. Founding members get early access to artifacts and reference components as they are developed before public release.</p></div>
          </details>
          <details class="faq-item" data-category="technology">
            <summary>Will SAFERai.Power include an AI system registry?</summary>
            <div class="faq-answer"><p>Yes. The framework and tools emphasize an AI System Registry rather than only a model registry because many deployments include products, embedded platform features, prompts, orchestration, agents, RAG pipelines, APIs, local permissions, human review steps, and external model dependencies.</p></div>
          </details>
          <details class="faq-item" data-category="regulatory">
            <summary>How can regulators, reliability organizations, and standards bodies participate?</summary>
            <div class="faq-answer"><p>Regulatory, reliability, standards, and policy organizations can participate through EPRI’s APEX platform at no cost under Chatham House Rules. This route is intended for organizations such as NERC, NARUC, NIST, FERC, DOE, state PUCs, and international counterparts.</p></div>
          </details>
          <details class="faq-item" data-category="regulatory">
            <summary>What is APEX?</summary>
            <div class="faq-answer"><p>APEX is EPRI’s AI and Power Exchange platform. For SAFERai.Power, it provides a no-fee stakeholder engagement pathway for policy, regulatory, reliability, and standards organizations to observe, shape assurance evidence expectations, and support cross-jurisdictional dialogue.</p></div>
          </details>
          <details class="faq-item" data-category="regulatory">
            <summary>Will regulators influence the framework?</summary>
            <div class="faq-answer"><p>The participation model encourages early engagement with regulators and standards stakeholders so the sector can shape practical expectations before fragmented requirements are imposed reactively. Paid tiers still participate through the collaborative working group process, while APEX provides structured visibility for public bodies.</p></div>
          </details>
          <details class="faq-item" data-category="regulatory">
            <summary>Is SAFERai.Power a regulatory requirement?</summary>
            <div class="faq-answer"><p>No. It is not a law or regulatory regime. It is intended to become a practical sector framework that utilities, technology partners, auditors, and regulators can use as a common language for risk assessment, evidence, assurance, lifecycle monitoring, and responsible AI deployment.</p></div>
          </details>
          <details class="faq-item" data-category="roadmap">
            <summary>What starts first?</summary>
            <div class="faq-answer"><p>The first step is founding-member mobilization: confirming participants, aligning on scope, selecting priority use cases, and organizing domain and technology working groups.</p></div>
          </details>
          <details class="faq-item" data-category="roadmap">
            <summary>What is delivered in the first six months?</summary>
            <div class="faq-answer"><p>The Foundation phase is expected to produce the working group charter, common glossary and data classes, draft AI System File schema, initial risk classification and autonomy guidance, founding member onboarding, APEX listening sessions, and technology-provider working group launch.</p></div>
          </details>
          <details class="faq-item" data-category="roadmap">
            <summary>What happens during Build and Pilot?</summary>
            <div class="faq-answer"><p>Months 7–12 focus on tiered test protocols, an AI System Registry prototype, monitoring and incident runbooks, pilot evaluations on representative use cases, and working group review cycles.</p></div>
          </details>
          <details class="faq-item" data-category="roadmap">
            <summary>When is the full toolkit released?</summary>
            <div class="faq-answer"><p>The full open-source SAFERai.Power toolkit is targeted for release after the framework and evidence templates have been piloted, validated, and converted into practical registry-backed assessment workflows.</p></div>
          </details>
          <details class="faq-item" data-category="roadmap">
            <summary>Do founding members get value before 2028?</summary>
            <div class="faq-answer"><p>Yes. The initiative is built as a learn-and-do cycle. Founding members help shape artifacts as they emerge, apply them to live use cases, join pilots, and feed lessons into the next iteration before the full tool suite is released.</p></div>
          </details>
          <details class="faq-item" data-category="roadmap">
            <summary>What pilot use cases are likely?</summary>
            <div class="faq-answer"><p>Initial candidates include customer-service copilots, vegetation and asset analytics, outage prediction and restoration prioritization support, planning models, and selected agentic workflows in business or customer operations. Higher-tier OT-connected use cases should follow once the evidence architecture and assurance pathways are ready.</p></div>
          </details>
          <details class="faq-item" data-category="roadmap">
            <summary>What happens after 2028?</summary>
            <div class="faq-answer"><p>The initiative is expected to transition to an enduring stewardship model for the risk framework, evidence package templates, registry model, and tool components, supported by philanthropic and government grant funding where appropriate.</p></div>
          </details>
          <details class="faq-item" data-category="membership">
            <summary>Who should we contact to join?</summary>
            <div class="faq-answer"><p>Contact EPRI at bsooter@epri.com. The fastest next step is to request an initial briefing.</p></div>
          </details>
        </div>
      </div>
    </section>

    <section style="background: #fff;">
      <div class="wrap">
        <div class="final-cta">
          <div class="kicker" style="color: #fff;">Join the founding cohort</div>
          <h2>Help define the practical risk framework and tools for trusted AI in the electric power industry.</h2>
          <p>Founding members shape the assessment methods, evidence templates, risk tiers, operating-boundary guidance, pilots, registry model, and open-source toolkit before fragmented approaches harden across the market.</p>
          <div class="contact-panel">
            <div>
              <strong>Contact Us</strong>
              <span>SAFERai.Power founding member inquiries</span>
              <span>bsooter@epri.com</span>
            </div>
            <a class="btn btn-primary" href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Founding%20Member%20Interest&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.Power.%0A%0AOrganization%3A%0ARole%3A%0APotential%20participation%20tier%3A%0AQuestions%3A%0A">Email Us →</a>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="wrap">
      <p><strong>SAFERai.Power</strong> | Electric Power Research Institute</p>
      <p>© 2026 Electric Power Research Institute (EPRI), Inc. All rights reserved.</p>
      <p><a href="mailto:bsooter@epri.com">bsooter@epri.com</a></p>
    </div>
  </footer>

  <a class="sticky-mobile-cta" href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Founding%20Member%20Interest&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.Power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us to Join</a>

  <script>
    const menuToggle = document.querySelector('.menu-toggle');
    const nav = document.getElementById('site-nav');
    menuToggle?.addEventListener('click', () => {
      const isOpen = nav.classList.toggle('open');
      menuToggle.setAttribute('aria-expanded', String(isOpen));
    });
    nav?.querySelectorAll('a').forEach(link => link.addEventListener('click', () => {
      nav.classList.remove('open');
      menuToggle?.setAttribute('aria-expanded', 'false');
    }));

    const search = document.getElementById('faqSearch');
    const items = Array.from(document.querySelectorAll('.faq-item'));
    const buttons = Array.from(document.querySelectorAll('.filter-btn'));
    const count = document.getElementById('faqCount');
    let activeFilter = 'all';

    function updateFaq() {
      const query = (search?.value || '').toLowerCase().trim();
      let visible = 0;
      items.forEach(item => {
        const category = item.dataset.category;
        const text = item.innerText.toLowerCase();
        const matchesCategory = activeFilter === 'all' || category === activeFilter;
        const matchesSearch = !query || text.includes(query);
        const show = matchesCategory && matchesSearch;
        item.hidden = !show;
        if (show) visible += 1;
      });
      count.textContent = visible === items.length ? 'Showing all FAQs' : `Showing ${visible} of ${items.length} FAQs`;
    }
    buttons.forEach(button => {
      button.addEventListener('click', () => {
        buttons.forEach(b => b.classList.remove('active'));
        button.classList.add('active');
        activeFilter = button.dataset.filter;
        updateFaq();
      });
    });
    search?.addEventListener('input', updateFaq);
    updateFaq();
  </script>
</body>
</html>
