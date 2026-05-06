<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>SAFERai.Power | AI Risk Framework & Tools for Utility Operations</title>
  <meta name="description" content="SAFERai.Power is an EPRI-led initiative to build a practical AI risk assessment framework, evidence-package templates, and tools for trusted AI in electric utility operations." />
  <meta name="theme-color" content="#173f63" />
  <meta property="og:title" content="SAFERai.Power" />
  <meta property="og:description" content="A power-sector AI risk assessment framework, evidence-package templates, and practical tools for trusted utility AI." />
  <meta property="og:type" content="website" />
  <style>
    /* GitHub Pages-ready: critical CSS is inlined so the page still looks correct if only index.html is deployed. */
:root {
  --navy: #173f63;
  --navy-dark: #0d2943;
  --blue: #2e75b6;
  --blue-soft: #eaf4ff;
  --light-blue: #bdd7ee;
  --accent: #f4a01c;
  --accent-dark: #b85d00;
  --green: #2e7d52;
  --green-soft: #e9f7ef;
  --ink: #102033;
  --muted: #5d7088;
  --line: #d7e3ef;
  --paper: #ffffff;
  --wash: #f4f7fb;
  --danger: #b42318;
  --shadow: 0 22px 60px rgba(13, 41, 67, .14);
  --shadow-soft: 0 12px 32px rgba(13, 41, 67, .08);
  --radius-xl: 32px;
  --radius-lg: 24px;
  --radius-md: 18px;
  --max: 1180px;
}

* { box-sizing: border-box; }
html { scroll-behavior: smooth; }
body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
  background: var(--wash);
  color: var(--ink);
  line-height: 1.55;
  -webkit-font-smoothing: antialiased;
  text-rendering: optimizeLegibility;
}
body.menu-open { overflow: hidden; }
a { color: inherit; }
img, svg { max-width: 100%; display: block; }
.container { width: min(var(--max), calc(100% - 40px)); margin: 0 auto; }
.section-pad { padding: clamp(58px, 7vw, 96px) 0; }
.white-section { background: #fff; }
.skip-link {
  position: absolute;
  left: 16px;
  top: -100px;
  z-index: 100;
  background: var(--accent);
  color: #111827;
  border-radius: 999px;
  padding: 10px 14px;
  font-weight: 800;
}
.skip-link:focus { top: 14px; }

.topbar {
  background: var(--navy-dark);
  color: #dbeafe;
  font-size: 13px;
  border-bottom: 1px solid rgba(255,255,255,.1);
}
.topbar-inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 18px;
  min-height: 42px;
}
.topbar p { margin: 0; }
.topbar strong { color: #fff; }
.topbar a { color: #fff; text-decoration: none; font-weight: 800; white-space: nowrap; }

.site-header { position: sticky; top: 0; z-index: 50; }
.nav {
  background: rgba(255,255,255,.96);
  border-bottom: 1px solid rgba(23,63,99,.16);
  box-shadow: 0 8px 30px rgba(13,41,67,.05);
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
  box-shadow: 0 14px 30px rgba(23,63,99,.24);
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
  font-weight: 800;
  letter-spacing: .12em;
  text-transform: uppercase;
}
.menu {
  display: flex;
  align-items: center;
  gap: 4px;
}
.menu a {
  text-decoration: none;
  color: #29455e;
  font-weight: 800;
  font-size: 14px;
  padding: 10px 12px;
  border-radius: 999px;
  white-space: nowrap;
}
.menu a:hover { background: var(--blue-soft); color: var(--navy); }
.menu a.nav-cta {
  background: var(--accent);
  color: #1a1a1a;
  box-shadow: 0 12px 26px rgba(244,160,28,.24);
  border: 1px solid rgba(184,93,0,.22);
}
.menu a.nav-cta:hover { background: #ffb53f; color: #111; }
.menu-button {
  display: none;
  align-items: center;
  gap: 8px;
  border: 1px solid var(--line);
  background: #fff;
  color: var(--navy);
  border-radius: 12px;
  padding: 10px 12px;
  font-weight: 900;
}
.menu-button svg { width: 21px; height: 21px; }

.hero {
  position: relative;
  overflow: hidden;
  background:
    radial-gradient(circle at 8% 14%, rgba(244,160,28,.2), transparent 24%),
    radial-gradient(circle at 92% 18%, rgba(189,215,238,.2), transparent 28%),
    linear-gradient(135deg, #0b2138 0%, var(--navy) 48%, #2e75b6 100%);
  color: #fff;
  border-bottom: 5px solid var(--accent);
}
.hero-bg {
  position: absolute;
  inset: 0;
  opacity: .16;
  background-image:
    linear-gradient(rgba(255,255,255,.24) 1px, transparent 1px),
    linear-gradient(90deg, rgba(255,255,255,.24) 1px, transparent 1px);
  background-size: 46px 46px;
}
.hero-grid {
  position: relative;
  display: grid;
  grid-template-columns: minmax(0, 1.05fr) minmax(360px, .95fr);
  gap: clamp(28px, 5vw, 58px);
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
.eyebrow span, .kicker::before {
  content: "";
  width: 26px;
  height: 3px;
  border-radius: 999px;
  background: var(--accent);
}
h1, h2, h3 { margin: 0; line-height: 1.07; letter-spacing: -.045em; }
h1 {
  max-width: 840px;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: clamp(46px, 6.2vw, 82px);
  font-weight: 900;
}
h2 {
  font-family: Georgia, 'Times New Roman', serif;
  color: var(--navy);
  font-size: clamp(33px, 4.1vw, 56px);
}
h3 { color: var(--navy); font-size: 24px; }
.hero-lede {
  max-width: 720px;
  color: #e6f2ff;
  font-size: clamp(18px, 2vw, 23px);
  line-height: 1.45;
  margin: 24px 0 14px;
}
.hero-note {
  max-width: 690px;
  margin: 0 0 28px;
  color: #bdd7ee;
  font-weight: 700;
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
.button-primary { background: var(--accent); color: #111827; box-shadow: 0 16px 36px rgba(244,160,28,.3); }
.button-primary:hover { background: #ffb53f; }
.button-secondary { background: rgba(255,255,255,.12); color: #fff; border-color: rgba(255,255,255,.28); }
.button-secondary:hover { background: rgba(255,255,255,.2); }
.button-outline { background: #fff; color: var(--navy); border-color: var(--line); box-shadow: var(--shadow-soft); }
.button-outline:hover { background: var(--blue-soft); }

.hero-panel {
  background: rgba(255,255,255,.97);
  color: var(--ink);
  border-radius: var(--radius-xl);
  box-shadow: 0 28px 80px rgba(0,0,0,.26);
  border: 1px solid rgba(255,255,255,.36);
  padding: clamp(24px, 3.5vw, 34px);
}
.panel-label {
  display: inline-block;
  background: var(--blue-soft);
  color: var(--navy);
  border: 1px solid #cfe1f3;
  border-radius: 999px;
  padding: 7px 11px;
  font-size: 12px;
  font-weight: 950;
  letter-spacing: .1em;
  text-transform: uppercase;
  margin-bottom: 15px;
}
.hero-panel h2 { font-size: clamp(29px, 3.4vw, 42px); }
.build-list { display: grid; gap: 12px; margin-top: 22px; }
.build-list div {
  border: 1px solid var(--line);
  border-radius: 18px;
  padding: 16px;
  background: #fbfdff;
}
.build-list strong { display: block; color: var(--navy); font-size: 17px; }
.build-list span { display: block; color: var(--muted); margin-top: 4px; }

.trust-strip { background: #fff; border-bottom: 1px solid var(--line); }
.trust-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1px;
  background: var(--line);
  border-left: 1px solid var(--line);
  border-right: 1px solid var(--line);
}
.trust-grid div { background: #fff; padding: 22px 20px; }
.trust-grid strong { display: block; color: var(--navy); font-size: 16px; }
.trust-grid span { display: block; color: var(--muted); font-size: 14px; margin-top: 4px; }

.section-head { max-width: 840px; margin-bottom: 30px; }
.section-head.centered { margin-left: auto; margin-right: auto; text-align: center; }
.section-head.centered .kicker { justify-content: center; }
.section-head p:not(.kicker), .sticky-copy p:not(.kicker) { color: var(--muted); font-size: 18px; margin: 15px 0 0; }
.light-head h2, .light-head p:not(.kicker) { color: #fff; }
.light-head p:not(.kicker) { color: #d6eaff; }

.scope-grid { display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 22px; }
.scope-card {
  position: relative;
  overflow: hidden;
  background: #fff;
  border: 1px solid var(--line);
  border-radius: var(--radius-lg);
  padding: clamp(24px, 3vw, 34px);
  box-shadow: var(--shadow-soft);
}
.scope-card::after {
  content: "";
  position: absolute;
  right: -55px;
  bottom: -70px;
  width: 180px;
  height: 180px;
  border-radius: 50%;
  background: rgba(46,117,182,.08);
}
.scope-card.negative::after { background: rgba(244,160,28,.12); }
.card-icon {
  width: 44px;
  height: 44px;
  border-radius: 15px;
  display: grid;
  place-items: center;
  background: var(--green-soft);
  color: var(--green);
  font-size: 23px;
  font-weight: 950;
  margin-bottom: 15px;
}
.scope-card.negative .card-icon { background: #fff4df; color: var(--accent-dark); }
.scope-card h3 { font-size: 30px; margin-bottom: 16px; }
.scope-card ul { margin: 0; padding: 0; list-style: none; display: grid; gap: 12px; }
.scope-card li { position: relative; padding-left: 28px; color: #334b63; }
.scope-card li::before {
  content: "";
  position: absolute;
  left: 0;
  top: .55em;
  width: 9px;
  height: 9px;
  border-radius: 50%;
  background: var(--accent);
}

.two-col { display: grid; grid-template-columns: .92fr 1.08fr; gap: clamp(26px, 5vw, 58px); align-items: start; }
.sticky-copy { position: sticky; top: 128px; }
.problem-stack { display: grid; gap: 16px; }
.problem-card {
  background: #fff;
  border: 1px solid var(--line);
  border-radius: var(--radius-lg);
  padding: 26px;
  box-shadow: var(--shadow-soft);
}
.problem-card span {
  display: inline-grid;
  place-items: center;
  width: 42px;
  height: 42px;
  border-radius: 14px;
  background: var(--navy);
  color: #fff;
  font-weight: 950;
  margin-bottom: 15px;
}
.problem-card h3 { margin-bottom: 10px; }
.problem-card p { color: var(--muted); margin: 0; }

.navy-section {
  background:
    radial-gradient(circle at 12% 10%, rgba(244,160,28,.18), transparent 24%),
    linear-gradient(135deg, var(--navy-dark), var(--navy));
  color: #fff;
}
.tool-grid { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: 18px; }
.tool-card {
  background: rgba(255,255,255,.08);
  border: 1px solid rgba(255,255,255,.16);
  border-radius: var(--radius-lg);
  padding: 24px;
  box-shadow: 0 14px 36px rgba(0,0,0,.08);
}
.tool-card span {
  display: inline-flex;
  color: #111827;
  background: var(--accent);
  border-radius: 999px;
  padding: 5px 10px;
  font-weight: 950;
  font-size: 12px;
  margin-bottom: 16px;
}
.tool-card h3 { color: #fff; margin-bottom: 10px; }
.tool-card p { color: #d6eaff; margin: 0; }

.layer-grid { display: grid; grid-template-columns: repeat(4, minmax(0,1fr)); gap: 18px; }
.layer-card {
  background: #fff;
  border: 1px solid var(--line);
  border-radius: var(--radius-lg);
  padding: 24px;
  box-shadow: var(--shadow-soft);
}
.layer-card span {
  display: inline-block;
  color: var(--accent-dark);
  font-weight: 950;
  font-size: 12px;
  letter-spacing: .11em;
  text-transform: uppercase;
  margin-bottom: 12px;
}
.layer-card h3 { margin-bottom: 10px; }
.layer-card p { color: var(--muted); margin: 0; }

.system-file-card {
  display: grid;
  grid-template-columns: .95fr 1.05fr;
  gap: 0;
  margin-top: 24px;
  border-radius: var(--radius-xl);
  overflow: hidden;
  border: 1px solid var(--line);
  box-shadow: var(--shadow);
  background: #fff;
}
.system-file-copy {
  padding: clamp(28px, 4vw, 42px);
  background: var(--navy);
  color: #fff;
}
.system-file-copy h2 { color: #fff; font-size: clamp(30px, 3.8vw, 48px); }
.system-file-copy p:not(.kicker) { color: #dbeafe; font-size: 17px; }
.artifact-list {
  display: grid;
  grid-template-columns: repeat(2, minmax(0,1fr));
  gap: 12px;
  padding: clamp(24px, 3vw, 32px);
  background: linear-gradient(135deg, #ffffff, #f3f9ff);
}
.artifact-list span {
  background: #fff;
  border: 1px solid var(--line);
  border-radius: 15px;
  padding: 13px 14px;
  color: #2f4761;
  font-weight: 800;
  box-shadow: 0 8px 20px rgba(13,41,67,.05);
}

.tier-table {
  overflow: hidden;
  background: #fff;
  border: 1px solid var(--line);
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-soft);
}
.tier-row { display: grid; grid-template-columns: .45fr 1.1fr 1.3fr 1.4fr; }
.tier-row > div { padding: 16px 18px; border-bottom: 1px solid var(--line); }
.tier-row:last-child > div { border-bottom: 0; }
.tier-row > div + div { border-left: 1px solid var(--line); }
.tier-header { background: var(--navy); color: #fff; font-weight: 950; }
.tier-row:not(.tier-header) > div:first-child { color: var(--navy); background: var(--blue-soft); font-size: 20px; }
.autonomy-grid { display: grid; grid-template-columns: repeat(4, minmax(0,1fr)); gap: 18px; margin-top: 22px; }
.autonomy-grid article {
  background: #fff;
  border: 1px solid var(--line);
  border-radius: var(--radius-lg);
  padding: 22px;
  box-shadow: var(--shadow-soft);
}
.autonomy-grid p { color: var(--muted); margin: 8px 0 0; }

.pricing-grid { display: grid; grid-template-columns: repeat(3, minmax(0,1fr)); gap: 20px; align-items: stretch; }
.price-card {
  position: relative;
  display: flex;
  flex-direction: column;
  background: #fff;
  border: 1px solid var(--line);
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-soft);
  overflow: hidden;
}
.price-card.featured { border: 2px solid var(--accent); transform: translateY(-8px); }
.price-badge {
  position: absolute;
  top: 14px;
  right: 14px;
  background: var(--accent);
  color: #111827;
  border-radius: 999px;
  font-weight: 950;
  font-size: 12px;
  padding: 6px 10px;
  z-index: 2;
}
.price-head { background: var(--navy); color: #fff; padding: 26px 24px; }
.standard .price-head { background: var(--blue); }
.emerging .price-head { background: #5b9bd5; }
.price-head p { margin: 0 0 8px; font-weight: 950; letter-spacing: .1em; text-transform: uppercase; font-size: 12px; }
.price-head h3 { color: #fff; font-size: clamp(42px, 5vw, 56px); }
.price-head span { display: block; color: rgba(255,255,255,.84); font-weight: 800; margin-top: 4px; }
.price-body { padding: 24px; display: flex; flex-direction: column; flex: 1; gap: 18px; }
.price-body .who { color: #334b63; margin: 0; font-weight: 750; }
.price-body ul { margin: 0; padding-left: 20px; color: var(--muted); }
.price-body li { margin: 8px 0; }
.price-body .button { margin-top: auto; width: 100%; }
.access-card {
  display: grid;
  grid-template-columns: .9fr 1.1fr;
  gap: 24px;
  align-items: center;
  margin-top: 24px;
  padding: clamp(24px, 3vw, 32px);
  border-radius: var(--radius-lg);
  border: 1px dashed rgba(46,117,182,.55);
  background: #f7fbff;
}
.access-card h3 { font-size: clamp(24px, 3vw, 34px); }
.access-card p:last-child { color: var(--muted); margin: 0; }

.benefit-grid { display: grid; grid-template-columns: repeat(3, minmax(0,1fr)); gap: 18px; }
.benefit-grid article {
  background: #fff;
  border: 1px solid var(--line);
  border-radius: var(--radius-lg);
  padding: 24px;
  box-shadow: var(--shadow-soft);
}
.benefit-grid span { color: var(--accent-dark); font-weight: 950; letter-spacing: .12em; font-size: 12px; }
.benefit-grid h3 { margin: 10px 0; }
.benefit-grid p { color: var(--muted); margin: 0; }

.roadmap { display: grid; gap: 16px; max-width: 900px; margin: 0 auto; }
.road-item { display: grid; grid-template-columns: 58px 1fr; gap: 18px; align-items: start; }
.road-item > div {
  width: 58px;
  height: 58px;
  border-radius: 18px;
  background: var(--navy);
  color: #fff;
  display: grid;
  place-items: center;
  font-weight: 950;
  border: 5px solid #fff;
  box-shadow: 0 10px 22px rgba(23,63,99,.18);
}
.road-item section {
  background: #fff;
  border: 1px solid var(--line);
  border-radius: var(--radius-lg);
  padding: 22px 24px;
  box-shadow: var(--shadow-soft);
}
.road-item span { color: var(--accent-dark); font-size: 12px; font-weight: 950; letter-spacing: .12em; text-transform: uppercase; }
.road-item h3 { margin: 7px 0 8px; }
.road-item p { color: var(--muted); margin: 0; }

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
.cta-card p:not(.kicker) { color: #dbeafe; max-width: 760px; font-size: 18px; }
.cta-card .button { min-width: 180px; }

.faq-tools {
  display: grid;
  grid-template-columns: 1fr;
  gap: 14px;
  margin-bottom: 20px;
}
.search-label {
  position: absolute;
  width: 1px;
  height: 1px;
  overflow: hidden;
  clip: rect(0,0,0,0);
}
.faq-search {
  width: 100%;
  min-height: 56px;
  border: 1px solid var(--line);
  border-radius: 18px;
  padding: 0 18px;
  color: var(--ink);
  background: #fff;
  font-size: 16px;
  box-shadow: var(--shadow-soft);
}
.faq-search:focus { outline: 3px solid rgba(46,117,182,.18); border-color: var(--blue); }
.faq-filters { display: flex; justify-content: center; gap: 8px; flex-wrap: wrap; }
.filter {
  border: 1px solid var(--line);
  background: #fff;
  color: #314a64;
  border-radius: 999px;
  padding: 10px 13px;
  font-weight: 900;
  cursor: pointer;
}
.filter.active { background: var(--navy); color: #fff; border-color: var(--navy); }
.faq-count { margin: 0; text-align: center; color: var(--muted); font-size: 14px; font-weight: 800; }
.faq-list { display: grid; gap: 10px; max-width: 980px; margin: 0 auto; }
.faq-item {
  background: #fff;
  border: 1px solid var(--line);
  border-radius: 18px;
  overflow: hidden;
  box-shadow: 0 8px 20px rgba(13,41,67,.05);
}
.faq-item[hidden] { display: none; }
.faq-item summary {
  list-style: none;
  cursor: pointer;
  color: var(--navy);
  font-weight: 950;
  padding: 18px 20px;
  display: flex;
  justify-content: space-between;
  gap: 16px;
}
.faq-item summary::-webkit-details-marker { display: none; }
.faq-item summary::after { content: "+"; color: var(--blue); font-size: 24px; line-height: 1; }
.faq-item[open] summary::after { content: "−"; }
.faq-item div { padding: 0 20px 20px; color: #40566f; }
.faq-item p { margin: 0; }

.footer {
  background: #0b2138;
  color: #d8e4f0;
  padding: 32px 0;
}
.footer-grid { display: flex; align-items: center; justify-content: space-between; gap: 24px; flex-wrap: wrap; }
.footer-brand { color: #fff; font-family: Georgia, 'Times New Roman', serif; font-size: 26px; font-weight: 900; text-decoration: none; }
.footer p { margin: 8px 0 0; color: #b8c8d8; }
.footer-links { display: flex; gap: 14px; flex-wrap: wrap; }
.footer-links a { color: #fff; text-decoration: none; font-weight: 850; }
.mobile-contact { display: none; }

@media (max-width: 1060px) {
  .hero-grid, .two-col, .system-file-card, .access-card, .cta-card { grid-template-columns: 1fr; }
  .hero-panel { max-width: 760px; }
  .tool-grid, .benefit-grid { grid-template-columns: repeat(2, minmax(0,1fr)); }
  .layer-grid, .autonomy-grid { grid-template-columns: repeat(2, minmax(0,1fr)); }
  .pricing-grid { grid-template-columns: 1fr; max-width: 720px; margin: 0 auto; }
  .price-card.featured { transform: none; }
  .sticky-copy { position: static; }
}
@media (max-width: 820px) {
  .container { width: min(100% - 28px, var(--max)); }
  .topbar-inner { justify-content: center; text-align: center; }
  .topbar a { display: none; }
  .nav-inner { min-height: 68px; }
  .brand-mark { width: 42px; height: 42px; border-radius: 13px; }
  .brand-name { font-size: 21px; }
  .brand-sub { display: none; }
  .menu-button { display: inline-flex; }
  .menu {
    position: fixed;
    left: 0;
    right: 0;
    top: 109px;
    bottom: 0;
    display: none;
    flex-direction: column;
    align-items: stretch;
    gap: 8px;
    padding: 18px 16px 100px;
    background: #fff;
    overflow: auto;
    border-top: 1px solid var(--line);
  }
  .menu.open { display: flex; }
  .menu a { border-radius: 14px; padding: 14px 16px; }
  .menu a.nav-cta { text-align: center; }
  .scope-grid, .trust-grid, .tool-grid, .layer-grid, .artifact-list, .autonomy-grid, .benefit-grid { grid-template-columns: 1fr; }
  .tier-table { display: grid; gap: 12px; background: transparent; border: 0; box-shadow: none; }
  .tier-row { grid-template-columns: 1fr; border: 1px solid var(--line); border-radius: 18px; overflow: hidden; background: #fff; box-shadow: var(--shadow-soft); }
  .tier-header { display: none; }
  .tier-row > div { border: 0; border-bottom: 1px solid var(--line); }
  .tier-row > div + div { border-left: 0; }
  .tier-row > div:last-child { border-bottom: 0; }
  .hero-actions .button, .cta-card .button { width: 100%; }
  .mobile-contact {
    display: block;
    position: fixed;
    left: 14px;
    right: 14px;
    bottom: 12px;
    z-index: 60;
    background: var(--accent);
    color: #111827;
    text-align: center;
    text-decoration: none;
    font-weight: 950;
    padding: 14px 18px;
    border-radius: 999px;
    box-shadow: 0 18px 40px rgba(13,41,67,.24);
  }
  body { padding-bottom: 74px; }
}
@media (max-width: 520px) {
  .section-pad { padding: 50px 0; }
  h1 { font-size: 42px; }
  h2 { font-size: 32px; }
  .hero-panel, .scope-card, .problem-card, .tool-card, .layer-card, .price-body, .benefit-grid article, .road-item section { padding: 20px; }
  .road-item { grid-template-columns: 44px 1fr; gap: 12px; }
  .road-item > div { width: 44px; height: 44px; border-radius: 14px; border-width: 3px; }
  .topbar { font-size: 12px; }
  .menu { top: 110px; }
}
@media (prefers-reduced-motion: reduce) {
  html { scroll-behavior: auto; }
  .button { transition: none; }
  .button:hover { transform: none; }
}

  </style>
</head>
<body>
  <a class="skip-link" href="#main">Skip to content</a>

  <header class="site-header" id="top">
    <div class="topbar">
      <div class="container topbar-inner">
        <p><strong>Founding member engagement</strong> for electric utilities, ISOs/RTOs, technology partners, and sector stakeholders.</p>
        <a href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Participation%20Inquiry">Contact Us</a>
      </div>
    </div>

    <nav class="nav" aria-label="Primary navigation">
      <div class="container nav-inner">
        <a class="brand" href="#top" aria-label="SAFERai.Power home">
          <span class="brand-mark" aria-hidden="true">
            <svg viewBox="0 0 64 64" role="img" focusable="false">
              <path d="M32 4 56 16v16c0 15.6-9.9 24.6-24 28C17.9 56.6 8 47.6 8 32V16L32 4Z" fill="currentColor" opacity=".18"/>
              <path d="M32 9 51 18.5V32c0 12.1-7.4 19.2-19 22-11.6-2.8-19-9.9-19-22V18.5L32 9Z" fill="none" stroke="currentColor" stroke-width="4"/>
              <path d="M24 34h12l-4 13 12-19H32l4-11-12 17Z" fill="#f4a01c"/>
            </svg>
          </span>
          <span>
            <span class="brand-name">SAFERai.Power</span>
            <span class="brand-sub">Electric Power Research Institute</span>
          </span>
        </a>

        <button class="menu-button" type="button" aria-expanded="false" aria-controls="site-menu">
          <span>Menu</span>
          <svg viewBox="0 0 24 24" aria-hidden="true"><path d="M4 7h16M4 12h16M4 17h16" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"/></svg>
        </button>

        <div class="menu" id="site-menu">
          <a href="#scope">Scope</a>
          <a href="#tools">Tools</a>
          <a href="#framework">Framework</a>
          <a href="#participate">Participate</a>
          <a href="#faq">FAQ</a>
          <a class="nav-cta" href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Participation%20Inquiry&body=Hello%2C%0A%0AI%27d%20like%20to%20learn%20more%20about%20SAFERai.Power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us</a>
        </div>
      </div>
    </nav>
  </header>

  <main id="main">
    <section class="hero section-pad">
      <div class="hero-bg" aria-hidden="true"></div>
      <div class="container hero-grid">
        <div class="hero-copy">
          <p class="eyebrow"><span></span> Framework + evidence packages + tools</p>
          <h1>Make utility AI easier to approve, safer to deploy, and clearer to trust.</h1>
          <p class="hero-lede">SAFERai.Power is an EPRI-led nonprofit initiative to co-develop a harmonized AI risk assessment framework, reusable evidence-package templates, and practical tools for AI in electric utility operations.</p>
          <p class="hero-note">It is not another general AI governance model. It is the power-sector operational risk assessment layer that governance, procurement, assurance, and regulatory conversations need.</p>
          <div class="hero-actions">
            <a class="button button-primary" href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Participation%20Inquiry&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.Power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us</a>
            <a class="button button-secondary" href="#participate">View participation options</a>
          </div>
        </div>

        <aside class="hero-panel" aria-label="What SAFERai.Power is building">
          <div class="panel-label">What we are building</div>
          <h2>One consistent way to assess operational AI risk across the sector.</h2>
          <div class="build-list">
            <div>
              <strong>Risk framework</strong>
              <span>Use-case tiers, autonomy levels, escalation modifiers, and power-sector operating boundaries.</span>
            </div>
            <div>
              <strong>Evidence packages</strong>
              <span>AI System File templates for providers, deployers, reviewers, and auditors.</span>
            </div>
            <div>
              <strong>Practical tools</strong>
              <span>Assessment workflow, AI System Registry model, evidence generator, and open-source components.</span>
            </div>
          </div>
        </aside>
      </div>
    </section>

    <section class="trust-strip" aria-label="Audience">
      <div class="container trust-grid">
        <div><strong>For utilities</strong><span>Common diligence before deployment</span></div>
        <div><strong>For ISOs/RTOs</strong><span>Risk language for reliability-sensitive use cases</span></div>
        <div><strong>For technology partners</strong><span>Clearer product evidence expectations</span></div>
        <div><strong>For public stakeholders</strong><span>Structured engagement through APEX</span></div>
      </div>
    </section>

    <section class="section-pad white-section" id="scope">
      <div class="container">
        <div class="section-head centered">
          <p class="kicker">Clarifying the scope</p>
          <h2>Not another governance document. A risk framework and toolset utilities can actually use.</h2>
          <p>Broad AI governance work already exists. SAFERai.Power focuses on the operational assessment gap for AI in utility functions such as asset management, grid operations, planning, restoration, vegetation management, customer and DER integration, and OT-adjacent workflows.</p>
        </div>

        <div class="scope-grid">
          <article class="scope-card positive">
            <div class="card-icon">✓</div>
            <h3>What SAFERai.Power is</h3>
            <ul>
              <li>A harmonized AI risk assessment framework for electric-sector operating contexts.</li>
              <li>Reusable evidence-package templates for utilities, ISOs/RTOs, and technology partners.</li>
              <li>A practical tool-building effort: assessment workflow, AI System Registry model, evidence generator, playbooks, pilots, and open-source components.</li>
              <li>A way to feed stronger operational evidence into existing governance, procurement, assurance, and regulatory processes.</li>
            </ul>
          </article>
          <article class="scope-card negative">
            <div class="card-icon">—</div>
            <h3>What SAFERai.Power is not</h3>
            <ul>
              <li>Not a general AI governance model competing with NIST, ISO/IEC, or internal utility programs.</li>
              <li>Not a new law, regulatory regime, or one-size-fits-all compliance checklist.</li>
              <li>Not a blanket approval of any vendor, platform, model, product, or deployment.</li>
              <li>Not a paper-only exercise. The intended output is a usable framework, templates, pilots, and tools.</li>
            </ul>
          </article>
        </div>
      </div>
    </section>

    <section class="section-pad" id="why">
      <div class="container two-col">
        <div class="section-head sticky-copy">
          <p class="kicker">Why now</p>
          <h2>AI is moving from pilots into live utility workflows.</h2>
          <p>Today, every utility makes AI risk judgments in isolation, every solution provider makes different claims, and every reviewer asks different questions. The result is duplicated effort, inconsistent diligence, slower adoption, and avoidable risk.</p>
          <p>SAFERai.Power creates a shared operating basis: faster where risk is low, more rigorous where safety, reliability, customer treatment, cyber, or regulatory consequence is real.</p>
        </div>
        <div class="problem-stack">
          <article class="problem-card">
            <span>01</span>
            <h3>Generic AI guidance is not enough for utility operations.</h3>
            <p>Power-sector AI can touch OT-adjacent systems, outage communications, asset integrity, restoration prioritization, field work, DER coordination, planning assumptions, and reliability-sensitive workflows.</p>
          </article>
          <article class="problem-card">
            <span>02</span>
            <h3>The missing layer is operational evidence.</h3>
            <p>Teams need consistent records of intended purpose, data provenance, limitations, autonomy, testing, monitoring, ownership, incident handling, and reassessment triggers.</p>
          </article>
          <article class="problem-card">
            <span>03</span>
            <h3>Product assurance and deployment assurance both matter.</h3>
            <p>A strong product can still be deployed unsafely if permissions, integrations, local procedures, oversight, or monitoring are weak. SAFERai.Power separates both evidence tracks.</p>
          </article>
        </div>
      </div>
    </section>

    <section class="section-pad navy-section" id="tools">
      <div class="container">
        <div class="section-head light-head">
          <p class="kicker">Tools, not just text</p>
          <h2>The framework becomes useful when it produces artifacts.</h2>
          <p>SAFERai.Power is designed to turn sector principles into working templates, assessment workflows, registry fields, pilot playbooks, and evidence packages.</p>
        </div>
        <div class="tool-grid">
          <article class="tool-card">
            <span>01</span>
            <h3>U-SAFER assessment workflow</h3>
            <p>A reusable question skeleton that adapts by use case, consequence domain, autonomy level, system access, and deployment context.</p>
          </article>
          <article class="tool-card">
            <span>02</span>
            <h3>AI System Registry model</h3>
            <p>A system of record for AI system identity, owner, intended purpose, risk tier, autonomy level, dependencies, evidence status, and change triggers.</p>
          </article>
          <article class="tool-card">
            <span>03</span>
            <h3>AI System File templates</h3>
            <p>Standardized evidence packages covering intended use, data provenance, system cards, TEVV, oversight, cyber/OT review, deployment profile, monitoring, and incidents.</p>
          </article>
          <article class="tool-card">
            <span>04</span>
            <h3>Provider evidence requests</h3>
            <p>Common expectations for technology partners: product scope, version, dependencies, limits, validation evidence, security discipline, and update obligations.</p>
          </article>
          <article class="tool-card">
            <span>05</span>
            <h3>Deployment assurance playbooks</h3>
            <p>Guidance for local utility implementation: permissions, integrations, role-based oversight, training, procedures, monitoring, escalation, and rollback.</p>
          </article>
          <article class="tool-card">
            <span>06</span>
            <h3>LLM-assisted toolkit components</h3>
            <p>Reference open-source components for conversational intake, evidence generation, registry-backed reassessment, and human review queues.</p>
          </article>
        </div>
      </div>
    </section>

    <section class="section-pad white-section" id="framework">
      <div class="container">
        <div class="section-head centered">
          <p class="kicker">Framework architecture</p>
          <h2>A four-layer operating model for utility AI evidence.</h2>
          <p>The framework scales by risk. Low-consequence uses should not carry the same burden as safety-critical, reliability-adjacent, or OT-connected systems.</p>
        </div>

        <div class="layer-grid">
          <article class="layer-card">
            <span>Layer 1</span>
            <h3>Data and system context</h3>
            <p>Intended purpose, data classification, provenance, rights, quality, stakeholder impact, operating environment, and restrictions.</p>
          </article>
          <article class="layer-card">
            <span>Layer 2</span>
            <h3>AI System Registry</h3>
            <p>System ownership, provider/deployer roles, versioning, dependencies, autonomy level, risk tier, approval state, and change triggers.</p>
          </article>
          <article class="layer-card">
            <span>Layer 3</span>
            <h3>TEVV and monitoring</h3>
            <p>Testing, evaluation, verification, validation, benchmarking, stress testing, drift monitoring, incident signals, and revalidation.</p>
          </article>
          <article class="layer-card">
            <span>Layer 4</span>
            <h3>Evidence review and assurance</h3>
            <p>Scope-bound evidence review, attestation pathways, independent review for higher-consequence systems, surveillance, and corrective action.</p>
          </article>
        </div>

        <div class="system-file-card">
          <div class="system-file-copy">
            <p class="kicker">The AI System File</p>
            <h2>The minimum common evidence package for material utility AI systems.</h2>
            <p>The AI System File helps teams answer the questions that matter before and after deployment: what the system is for, what it can influence, what data it uses, what evidence supports it, who owns it, what happens when it is wrong, and when it must be reassessed.</p>
          </div>
          <div class="artifact-list" aria-label="AI System File contents">
            <span>Impact assessment / intended-use review</span>
            <span>AI Use-Case Dossier</span>
            <span>Data Sheet and Provenance Record</span>
            <span>AI System Card</span>
            <span>Autonomy and Human Oversight Plan</span>
            <span>TEVV Report</span>
            <span>Cyber / OT Integration Assessment</span>
            <span>Deployment Profile</span>
            <span>Monitoring and Incident Plan</span>
            <span>Change and Reassessment Record</span>
          </div>
        </div>
      </div>
    </section>

    <section class="section-pad" id="risk">
      <div class="container">
        <div class="section-head">
          <p class="kicker">Risk and autonomy</p>
          <h2>Utility AI risk depends on consequence, autonomy, access, oversight, and reversibility.</h2>
          <p>SAFERai.Power treats autonomy as a governed capability, not a feature toggle. AI may assist consequential work, but it should not become the single point of failure for safety- or reliability-critical functions.</p>
        </div>

        <div class="tier-table" role="table" aria-label="Illustrative risk tier model">
          <div class="tier-row tier-header" role="row">
            <div role="columnheader">Tier</div>
            <div role="columnheader">Use case posture</div>
            <div role="columnheader">Examples</div>
            <div role="columnheader">Minimum control posture</div>
          </div>
          <div class="tier-row" role="row">
            <div role="cell"><strong>T1</strong></div>
            <div role="cell">Low-consequence assistance</div>
            <div role="cell">Summaries, internal drafting, personal productivity</div>
            <div role="cell">Acceptable use, data guardrails, human review</div>
          </div>
          <div class="tier-row" role="row">
            <div role="cell"><strong>T2</strong></div>
            <div role="cell">Business support and planning</div>
            <div role="cell">Internal analytics, planning forecasts, low-consequence customer support</div>
            <div role="cell">Use-case dossier, system card, data record, baseline validation</div>
          </div>
          <div class="tier-row" role="row">
            <div role="cell"><strong>T3</strong></div>
            <div role="cell">Operationally influential</div>
            <div role="cell">Vegetation analytics, predictive maintenance, outage prioritization support</div>
            <div role="cell">Formal validation, approval points, monitoring, management attestation</div>
          </div>
          <div class="tier-row" role="row">
            <div role="cell"><strong>T4</strong></div>
            <div role="cell">Reliability-adjacent / OT-connected support</div>
            <div role="cell">Operator advisory, DER dispatch recommendation, simulator switching support</div>
            <div role="cell">Independent validation, cyber/OT review, safety and reliability case</div>
          </div>
          <div class="tier-row" role="row">
            <div role="cell"><strong>T5</strong></div>
            <div role="cell">Grid-critical, safety-critical, or actuation-capable</div>
            <div role="cell">Live write-enabled OT automation, protection-adjacent decision support</div>
            <div role="cell">Executive approval, independent assurance, deterministic fallback, surveillance</div>
          </div>
        </div>

        <div class="autonomy-grid">
          <article><h3>Advisory</h3><p>Recommends or drafts; no direct execution. Human decision required.</p></article>
          <article><h3>Supervised action</h3><p>Limited action after explicit approval, with least privilege and rollback.</p></article>
          <article><h3>Guarded autonomy</h3><p>Bounded action within deterministic constraints, escalation logic, and validated operating limits.</p></article>
          <article><h3>Autonomous</h3><p>Exceptional for critical workflows; requires enhanced evidence, deterministic fallback, and executive approval.</p></article>
        </div>
      </div>
    </section>

    <section class="section-pad white-section" id="participate">
      <div class="container">
        <div class="section-head centered">
          <p class="kicker">Participation</p>
          <h2>Founding members help shape the framework and tools before expectations harden without them.</h2>
          <p>Participation is not a license fee. It is a two-year commitment to co-develop the risk framework, evidence templates, pilot playbooks, registry model, and tool components the sector needs.</p>
        </div>

        <div class="pricing-grid" aria-label="Participation tiers">
          <article class="price-card lead">
            <div class="price-head"><p>Lead Partner</p><h3>$40,000</h3><span>per year · $80,000 over two years</span></div>
            <div class="price-body">
              <p class="who">Large utilities, major IPPs, ISOs/RTOs, hyperscalers, AI platform providers, and infrastructure companies.</p>
              <ul>
                <li>Equal access to working groups and framework artifacts</li>
                <li>Early access to templates, registry model, U-SAFER protocols, and playbooks</li>
                <li>Pilot use case participation and roadmap reviews</li>
              </ul>
              <a class="button button-outline" href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Lead%20Partner%20Interest">Contact Us</a>
            </div>
          </article>
          <article class="price-card standard featured">
            <div class="price-badge">Core option</div>
            <div class="price-head"><p>Standard Partner</p><h3>$25,000</h3><span>per year · $50,000 over two years</span></div>
            <div class="price-body">
              <p class="who">Mid-size utilities, regional operators, established AI vendors, implementation partners, and advisory firms.</p>
              <ul>
                <li>Equal participation in collaborative design decisions</li>
                <li>Early access to AI System File and deployment assurance templates</li>
                <li>Structured engagement with utilities and technology partners</li>
              </ul>
              <a class="button button-outline" href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Standard%20Partner%20Interest">Contact Us</a>
            </div>
          </article>
          <article class="price-card emerging">
            <div class="price-head"><p>Emerging Partner</p><h3>$15,000</h3><span>per year · $30,000 over two years</span></div>
            <div class="price-body">
              <p class="who">Smaller utilities, cooperatives, public power districts, municipal utilities, and early-stage technology companies.</p>
              <ul>
                <li>Same substantive access to the initiative as larger participants</li>
                <li>Templates and practices usable by teams without large internal AI programs</li>
                <li>Participation pathways available where fees are a barrier</li>
              </ul>
              <a class="button button-outline" href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Emerging%20Partner%20Interest">Contact Us</a>
            </div>
          </article>
        </div>

        <div class="access-card">
          <div>
            <p class="kicker">Access principle</p>
            <h3>No qualified utility, cooperative, or innovator should be excluded because of fee structure alone.</h3>
          </div>
          <p>Participation fees fund framework and tool development; they do not buy commercial control over the framework. All tiers participate as equals in the collaborative working process. Participants should expect to contribute skilled subject-matter-expert time in addition to funding, with scope defined with the project team.</p>
        </div>
      </div>
    </section>

    <section class="section-pad" id="receive">
      <div class="container">
        <div class="section-head">
          <p class="kicker">What participants receive</p>
          <h2>Substantive access is equal across tiers.</h2>
          <p>Tier differences reflect organizational scale and capacity to contribute, not depth of engagement.</p>
        </div>
        <div class="benefit-grid">
          <article><span>01</span><h3>Working group seats</h3><p>Voting input on framework decisions, with all tiers participating as equals in the collaborative design process.</p></article>
          <article><span>02</span><h3>Early artifacts</h3><p>AI System File templates, registry schema, assessment protocols, autonomy guidance, and evidence packages as they are developed.</p></article>
          <article><span>03</span><h3>Pilot participation</h3><p>Opportunities to shape pilot use cases, test the methodology, and feed lessons into the next iteration.</p></article>
          <article><span>04</span><h3>Technology partner engagement</h3><p>Structured collaboration across model developers, platform providers, tooling firms, integrators, and utility deployers.</p></article>
          <article><span>05</span><h3>APEX stakeholder visibility</h3><p>Regulatory, reliability, standards, and policy organizations can engage through EPRI’s APEX pathway at no fee.</p></article>
          <article><span>06</span><h3>Founding member recognition</h3><p>Recognition at major milestones and upon publication of the framework and toolkit deliverables.</p></article>
        </div>
      </div>
    </section>

    <section class="section-pad white-section" id="roadmap">
      <div class="container">
        <div class="section-head centered">
          <p class="kicker">Development roadmap</p>
          <h2>A learn-and-do cycle that produces usable artifacts as the project progresses.</h2>
          <p>Founding members do not wait until the end for value. The project is structured to collect good practices, apply them to live use cases, and iterate templates and tools through pilots.</p>
        </div>
        <div class="roadmap">
          <article class="road-item"><div>1</div><section><span>Months 1–4</span><h3>Harvest and synthesize</h3><p>Map existing standards, utility policies, technology partner inputs, and sector needs into a structured gap analysis.</p></section></article>
          <article class="road-item"><div>2</div><section><span>Months 3–6</span><h3>Domain decomposition</h3><p>Build the real Use Case Matrix by consequence domain, autonomy level, access, write authority, and reversibility.</p></section></article>
          <article class="road-item"><div>3</div><section><span>Months 5–12</span><h3>SAFER document and template suite</h3><p>Create the principles, glossary, assessment methodology, playbooks, assurance guide, and evidence templates.</p></section></article>
          <article class="road-item"><div>4</div><section><span>Months 8–18</span><h3>Pilot and validate</h3><p>Apply the draft methodology to representative utility, ISO/RTO, and technology-partner use cases and refine based on evidence.</p></section></article>
          <article class="road-item"><div>5</div><section><span>Months 12–24</span><h3>Open-source toolkit components</h3><p>Build the LLM-assisted assessment interface, registry model, evidence package generator, reassessment workflow, and reference implementation.</p></section></article>
        </div>
      </div>
    </section>

    <section class="section-pad cta-section" id="contact">
      <div class="container cta-card">
        <div>
          <p class="kicker">Next step</p>
          <h2>Ready to help define trusted AI adoption for the electric sector?</h2>
          <p>Start with an initial briefing to discuss the project, participation track, contribution profile, and fit for your organization.</p>
        </div>
        <a class="button button-primary" href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Participation%20Inquiry&body=Hello%2C%0A%0AI%27d%20like%20to%20schedule%20an%20initial%20briefing%20about%20SAFERai.Power.%0A%0AOrganization%3A%0ARole%3A%0AQuestions%3A%0A">Contact Us</a>
      </div>
    </section>

    <section class="section-pad white-section" id="faq">
      <div class="container">
        <div class="section-head centered">
          <p class="kicker">FAQ</p>
          <h2>Questions potential participants are likely to ask.</h2>
          <p>Use the filters or search box to find answers by topic.</p>
        </div>

        <div class="faq-tools" aria-label="FAQ filters">
          <label class="search-label" for="faq-search">Search FAQ</label>
          <input id="faq-search" class="faq-search" type="search" placeholder="Search by keyword, topic, tier, evidence, tooling…" />
          <div class="faq-filters" role="group" aria-label="FAQ categories">
            <button class="filter active" type="button" data-filter="all">All</button>
            <button class="filter" type="button" data-filter="scope">Scope</button>
            <button class="filter" type="button" data-filter="tools">Tools</button>
            <button class="filter" type="button" data-filter="participation">Participation</button>
            <button class="filter" type="button" data-filter="assurance">Assurance</button>
            <button class="filter" type="button" data-filter="technical">Technical</button>
          </div>
          <p class="faq-count" aria-live="polite"><span id="faq-count">0</span> questions shown</p>
        </div>

        <div class="faq-list" id="faq-list">
          <details class="faq-item" data-category="scope" open>
            <summary>Is SAFERai.Power an AI governance framework?</summary>
            <div><p>Not in the broad, general sense. SAFERai.Power is a power-sector AI risk assessment framework, evidence-package model, and tool-building initiative. It supports governance programs by supplying the operational evidence and assessment rigor those programs need.</p></div>
          </details>
          <details class="faq-item" data-category="scope">
            <summary>How is this different from NIST AI RMF, ISO/IEC 42001, IEC 62443, NERC CIP, or the EU AI Act?</summary>
            <div><p>Those frameworks and requirements are important reference points. SAFERai.Power does not replace them. It translates broad lifecycle, safety, cybersecurity, reliability, and management-system concepts into power-sector use cases, evidence templates, assessment methods, and operating boundaries.</p></div>
          </details>
          <details class="faq-item" data-category="scope">
            <summary>Why does the electric sector need its own AI risk assessment layer?</summary>
            <div><p>Utility AI can affect public and worker safety, asset health, restoration, customer treatment, DER coordination, planning assumptions, cyber posture, and reliability-sensitive operations. General AI guidance does not define the operational evidence needed for those contexts.</p></div>
          </details>
          <details class="faq-item" data-category="scope">
            <summary>Does this slow down AI adoption?</summary>
            <div><p>The intent is the opposite. A shared risk framework should help organizations move faster where risk is low and more carefully where consequence is real. Clear expectations reduce rework, duplicated diligence, and late-stage objections.</p></div>
          </details>
          <details class="faq-item" data-category="scope">
            <summary>What kinds of utility functions are in scope?</summary>
            <div><p>Initial focus areas include asset management, grid operations, system planning, outage and restoration support, vegetation management, customer operations, DER integration, cybersecurity operations, field work, and OT-adjacent environments.</p></div>
          </details>
          <details class="faq-item" data-category="scope">
            <summary>Is customer-service AI in scope, or only grid operations?</summary>
            <div><p>Both can be in scope. Customer-facing AI can create fairness, legal, reputational, privacy, and customer-trust risk. Grid-adjacent AI can create safety, reliability, cyber, and operational risk. The framework scales controls based on consequence.</p></div>
          </details>
          <details class="faq-item" data-category="scope">
            <summary>Does SAFERai.Power assume AI should be used in all utility functions?</summary>
            <div><p>No. The framework is designed to help teams decide where AI is appropriate, what evidence is required, what boundaries apply, and where autonomy or system access should be limited or prohibited.</p></div>
          </details>
          <details class="faq-item" data-category="scope">
            <summary>Will this replace an internal utility AI review board or center of excellence?</summary>
            <div><p>No. SAFERai.Power should map onto existing AI review boards, centers of excellence, data governance, cybersecurity, legal, reliability, and audit functions. It gives those groups sector-specific questions, artifacts, and evidence expectations.</p></div>
          </details>

          <details class="faq-item" data-category="tools">
            <summary>What actual deliverables will come out of the project?</summary>
            <div><p>Expected deliverables include SAFER principles and glossary, U-SAFER assessment methodology, Use Case Matrix, AI System File templates, AI System Registry schema, product evidence request templates, deployment assurance templates, monitoring and incident playbooks, pilot case studies, and open-source toolkit components.</p></div>
          </details>
          <details class="faq-item" data-category="tools">
            <summary>What is the AI System File?</summary>
            <div><p>The AI System File is the structured evidence package for a material AI system. It captures intended purpose, data provenance, system capabilities and limits, autonomy and oversight, TEVV results, cyber/OT considerations, deployment profile, monitoring, incidents, and reassessment triggers.</p></div>
          </details>
          <details class="faq-item" data-category="tools">
            <summary>What is the AI System Registry?</summary>
            <div><p>The registry is a system of record for governed AI systems. It should capture system name, owner, provider, deployer, intended purpose, out-of-scope uses, data sources, risk tier, autonomy level, dependencies, validation status, deployment environment, monitoring status, incident history, and approval state.</p></div>
          </details>
          <details class="faq-item" data-category="tools">
            <summary>Why a system registry instead of only a model registry?</summary>
            <div><p>Many utility AI deployments are not just a model. They include vendor applications, embedded platform features, prompts, retrieval pipelines, agents, APIs, permissions, integrations, human review steps, and external model dependencies. The governed object is the AI system.</p></div>
          </details>
          <details class="faq-item" data-category="tools">
            <summary>What is U-SAFER?</summary>
            <div><p>U-SAFER is the working name for the utility/electric-sector assessment method. It uses stable question categories while allowing thresholds, metrics, and evidence depth to vary by use case, consequence, autonomy, and deployment context.</p></div>
          </details>
          <details class="faq-item" data-category="tools">
            <summary>Will there be software, or only templates?</summary>
            <div><p>The project is intended to produce both. Templates and playbooks are early deliverables. The longer-term goal is a practical open-source toolkit with LLM-assisted intake, registry-backed evidence management, reassessment workflows, and human approval gates.</p></div>
          </details>
          <details class="faq-item" data-category="tools">
            <summary>Will the toolkit make final risk decisions automatically?</summary>
            <div><p>No. The toolkit can help collect evidence, route questions, draft documentation, and trigger deterministic checks. Human owners, domain experts, and reviewers retain authority for consequential decisions.</p></div>
          </details>
          <details class="faq-item" data-category="tools">
            <summary>Can smaller utilities use the tools without a large AI governance staff?</summary>
            <div><p>Yes. A major goal is to give smaller or less mature organizations practical templates, checklists, registry fields, and workflows they can adopt without building a large internal program from scratch.</p></div>
          </details>

          <details class="faq-item" data-category="assurance">
            <summary>What is product assurance?</summary>
            <div><p>Product assurance asks whether a provider’s product, version, dependencies, intended purpose, documented limits, security evidence, and validation results are appropriate for defined electric-sector use cases.</p></div>
          </details>
          <details class="faq-item" data-category="assurance">
            <summary>What is deployment assurance?</summary>
            <div><p>Deployment assurance asks whether a utility’s local implementation is safe in practice: permissions, integrations, procedures, training, oversight, monitoring, escalation, rollback, and incident response.</p></div>
          </details>
          <details class="faq-item" data-category="assurance">
            <summary>Can a product be acceptable but a deployment still be unsafe?</summary>
            <div><p>Yes. A product may be well-controlled in principle, but a local deployment can create risk through excessive permissions, weak human oversight, poor data quality, unsafe integrations, or missing monitoring.</p></div>
          </details>
          <details class="faq-item" data-category="assurance">
            <summary>Will SAFERai.Power certify products or utilities?</summary>
            <div><p>The framework may define assurance pathways, readiness reviews, or verification-like signals, but any meaningful assurance claim should be scope-bound to a defined product or deployment, version, intended purpose, operating boundary, and surveillance rules.</p></div>
          </details>
          <details class="faq-item" data-category="assurance">
            <summary>How will the framework handle vendor claims?</summary>
            <div><p>It will define common evidence requests so utilities can ask technology partners for product scope, model or dependency inventory, validation evidence, limitations, security and update discipline, support commitments, and out-of-scope uses.</p></div>
          </details>
          <details class="faq-item" data-category="assurance">
            <summary>What happens after deployment?</summary>
            <div><p>Deployment is not the end of validation. Higher-risk systems need monitoring for performance degradation, drift, incidents, overrides, supplier updates, autonomy changes, and conditions that trigger reassessment.</p></div>
          </details>
          <details class="faq-item" data-category="assurance">
            <summary>Will regulators be involved?</summary>
            <div><p>Regulatory, reliability, standards, and policy organizations are expected to engage through EPRI’s APEX pathway. That gives public stakeholders visibility and input without creating procurement complications tied to paid membership.</p></div>
          </details>
          <details class="faq-item" data-category="assurance">
            <summary>Does this create a new compliance obligation?</summary>
            <div><p>No. SAFERai.Power is not a law or regulatory regime. It is intended to provide a stronger, common evidence basis that can support internal reviews, procurement diligence, audits, and regulatory conversations.</p></div>
          </details>

          <details class="faq-item" data-category="technical">
            <summary>How does SAFERai.Power classify risk?</summary>
            <div><p>Risk classification considers consequence if wrong, autonomy level, system access and write authority, human oversight, reversibility, operating context, data sensitivity, cyber exposure, customer impact, and reliability or safety relevance.</p></div>
          </details>
          <details class="faq-item" data-category="technical">
            <summary>How does the framework handle autonomy?</summary>
            <div><p>Autonomy is classified separately from risk tier. Working levels include Advisory, Supervised Action, Guarded Autonomy, and Autonomous. Higher autonomy and write authority increase evidence and oversight expectations.</p></div>
          </details>
          <details class="faq-item" data-category="technical">
            <summary>Does SAFERai.Power allow autonomous grid operations?</summary>
            <div><p>The framework does not assume live autonomy is acceptable by default. Any critical or actuation-capable use would require strong safety and reliability evidence, deterministic guardrails, manual override, independent review, and explicit approval.</p></div>
          </details>
          <details class="faq-item" data-category="technical">
            <summary>What does TEVV mean?</summary>
            <div><p>TEVV means testing, evaluation, verification, and validation. In this context it includes benchmarking, scenario testing, stress testing, human factors review, cyber/OT evaluation, fairness review where relevant, monitoring, and revalidation.</p></div>
          </details>
          <details class="faq-item" data-category="technical">
            <summary>How will the framework address generative AI and agentic AI?</summary>
            <div><p>It will cover prompts, retrieval, tool use, model and provider updates, memory or state, permission boundaries, task decomposition, escalation behavior, action reversibility, and the limits of AI-generated explanations.</p></div>
          </details>
          <details class="faq-item" data-category="technical">
            <summary>How will cyber and OT boundaries be handled?</summary>
            <div><p>AI systems that touch OT or reliability-sensitive environments need evidence around interfaces, permissions, segmentation, secure access, logging, threat considerations, change management, rollback, and regulated operational data handling.</p></div>
          </details>
          <details class="faq-item" data-category="technical">
            <summary>Does the framework cover embedded AI features in existing enterprise software?</summary>
            <div><p>Yes. The framework treats build, buy, upgrade, and enable decisions explicitly. Embedded AI features need assessment when they influence material decisions, data exposure, automation, customer communications, or operational workflows.</p></div>
          </details>
          <details class="faq-item" data-category="technical">
            <summary>Will SAFERai.Power prescribe specific models, platforms, or architectures?</summary>
            <div><p>No. It standardizes evidence, assessment logic, and control expectations. It does not mandate one vendor stack, model architecture, cloud provider, or data strategy.</p></div>
          </details>
          <details class="faq-item" data-category="technical">
            <summary>How does the framework handle data that cannot be shared?</summary>
            <div><p>It should support multiple collaboration patterns, including metadata standards, de-identification, aggregation, privacy-preserving evaluation, synthetic data where appropriate, and local assessment without unrestricted data sharing.</p></div>
          </details>

          <details class="faq-item" data-category="participation">
            <summary>Who should participate?</summary>
            <div><p>Utilities, ISOs/RTOs, technology partners, AI solution providers, implementation and advisory firms, research organizations, and other stakeholders with a role in trustworthy AI deployment in the electric sector.</p></div>
          </details>
          <details class="faq-item" data-category="participation">
            <summary>What are the participation tiers?</summary>
            <div><p>The current structure includes Lead Partner at $40,000 per year, Standard Partner at $25,000 per year, and Emerging Partner at $15,000 per year, each structured as a two-year commitment.</p></div>
          </details>
          <details class="faq-item" data-category="participation">
            <summary>Do higher tiers get more control over the framework?</summary>
            <div><p>No. Tier differentiation reflects organizational scale and capacity to contribute, not control over the framework. Substantive access and participation in the collaborative design process are intended to be equal across tiers.</p></div>
          </details>
          <details class="faq-item" data-category="participation">
            <summary>Is SME time expected?</summary>
            <div><p>Yes. Participants are expected to contribute skilled subject-matter-expert time in addition to funding. The scope should be defined with the project team based on the participant’s expertise and project needs.</p></div>
          </details>
          <details class="faq-item" data-category="participation">
            <summary>What expertise is most useful?</summary>
            <div><p>Useful expertise includes grid operations, planning, asset management, distribution operations, customer operations, field work, OT/cyber, AI/ML, MLOps, model registry design, AI assurance, agentic systems, and open-source tool development.</p></div>
          </details>
          <details class="faq-item" data-category="participation">
            <summary>Can public agencies or standards bodies participate without a fee?</summary>
            <div><p>Regulatory, reliability, standards, and policy organizations are expected to participate through EPRI’s APEX platform at no cost, under appropriate engagement rules.</p></div>
          </details>
          <details class="faq-item" data-category="participation">
            <summary>What if the Emerging Partner fee is still a barrier?</summary>
            <div><p>The access principle is that no qualified utility, cooperative, or innovator should be excluded because of fee structure alone. Organizations should contact the project team to discuss possible pathways.</p></div>
          </details>
          <details class="faq-item" data-category="participation">
            <summary>How do we start?</summary>
            <div><p>Start with an initial briefing. The project team can discuss fit, participation track, contribution profile, potential use cases, SME involvement, and next steps.</p></div>
          </details>
          <details class="faq-item" data-category="participation">
            <summary>Who is the contact?</summary>
            <div><p>Use the Contact Us links on this site, which open an email to bsooter@epri.com.</p></div>
          </details>
          <details class="faq-item" data-category="participation">
            <summary>Can organizations join after the project begins?</summary>
            <div><p>Yes. Mid-cycle participation can be accommodated, with participation details and fee treatment handled by the project team.</p></div>
          </details>
          <details class="faq-item" data-category="participation">
            <summary>What do founding members get that later adopters may not?</summary>
            <div><p>Founding members help shape the framework, templates, tool requirements, pilots, and evidence expectations while they are still being designed, rather than adapting after the approach has hardened.</p></div>
          </details>
          <details class="faq-item" data-category="tools">
            <summary>Will outputs be open source?</summary>
            <div><p>The project is designed to produce open-source toolkit components and broadly usable framework artifacts, while sensitive pilot evidence, participant-specific records, and controlled assurance materials may remain appropriately protected.</p></div>
          </details>
          <details class="faq-item" data-category="assurance">
            <summary>How will SAFERai.Power avoid becoming a paperwork exercise?</summary>
            <div><p>The project is being framed around operational artifacts: registry fields, evidence templates, assessment workflows, pilots, monitoring triggers, and practical tool components. The document suite is the beginning of the framework, not the end state.</p></div>
          </details>
          <details class="faq-item" data-category="scope">
            <summary>Why is EPRI positioned to lead this?</summary>
            <div><p>The project depends on independence, sector convening power, and deep operational expertise across utility functions. EPRI can bring utilities, technology partners, researchers, reliability stakeholders, and policy observers into one harmonized effort.</p></div>
          </details>
        </div>
      </div>
    </section>
  </main>

  <footer class="footer">
    <div class="container footer-grid">
      <div>
        <a class="footer-brand" href="#top">SAFERai.Power</a>
        <p>Practical AI risk assessment, evidence packages, and tools for the electric sector.</p>
      </div>
      <div class="footer-links">
        <a href="#scope">Scope</a>
        <a href="#tools">Tools</a>
        <a href="#participate">Participate</a>
        <a href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Participation%20Inquiry">Contact Us</a>
      </div>
    </div>
  </footer>

  <a class="mobile-contact" href="mailto:bsooter@epri.com?subject=SAFERai.Power%20Participation%20Inquiry">Contact Us</a>
  <script>
(function () {
  const menuButton = document.querySelector('.menu-button');
  const menu = document.querySelector('.menu');

  if (menuButton && menu) {
    menuButton.addEventListener('click', () => {
      const open = menu.classList.toggle('open');
      document.body.classList.toggle('menu-open', open);
      menuButton.setAttribute('aria-expanded', String(open));
    });

    menu.querySelectorAll('a').forEach((link) => {
      link.addEventListener('click', () => {
        menu.classList.remove('open');
        document.body.classList.remove('menu-open');
        menuButton.setAttribute('aria-expanded', 'false');
      });
    });
  }

  const search = document.querySelector('#faq-search');
  const filters = Array.from(document.querySelectorAll('.filter'));
  const items = Array.from(document.querySelectorAll('.faq-item'));
  const count = document.querySelector('#faq-count');
  let activeFilter = 'all';

  function applyFaqFilters() {
    const query = (search ? search.value : '').trim().toLowerCase();
    let shown = 0;

    items.forEach((item) => {
      const category = item.dataset.category || '';
      const text = item.textContent.toLowerCase();
      const categoryMatch = activeFilter === 'all' || category === activeFilter;
      const queryMatch = !query || text.includes(query);
      const visible = categoryMatch && queryMatch;
      item.hidden = !visible;
      if (visible) shown += 1;
    });

    if (count) count.textContent = String(shown);
  }

  filters.forEach((button) => {
    button.addEventListener('click', () => {
      activeFilter = button.dataset.filter || 'all';
      filters.forEach((b) => b.classList.toggle('active', b === button));
      applyFaqFilters();
    });
  });

  if (search) search.addEventListener('input', applyFaqFilters);
  applyFaqFilters();
})();

  </script>
</body>
</html>
