<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#050b14">
<meta name="description" content="DevSites — Sites profissionais para empresas que querem crescer.">
<meta name="keywords" content="criação de sites, sites profissionais, loja virtual, landing page, desenvolvimento web">
<meta property="og:title" content="DevSites — Sites profissionais">
<meta property="og:description" content="Escolha, personalize e solicite seu próximo site profissional.">
<title>DevSites — Sites Profissionais</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>
:root{
    --bg:#050912;
    --bg2:#08111f;
    --card:#0c1625;
    --card2:#101d30;
    --primary:#1683ff;
    --primary2:#00c6ff;
    --cyan:#35e7ff;
    --white:#f6f9ff;
    --muted:#8ea1b8;
    --border:rgba(255,255,255,.09);
    --success:#27d17f;
    --danger:#ff5364;
    --warning:#ffbd4a;
    --shadow:0 25px 70px rgba(0,0,0,.35);
    --radius:18px;
}

*{box-sizing:border-box;margin:0;padding:0}

html{
    scroll-behavior:smooth;
}

body{
    font-family:Inter,Arial,sans-serif;
    background:
        radial-gradient(circle at 10% 10%,rgba(22,131,255,.13),transparent 30%),
        radial-gradient(circle at 90% 30%,rgba(0,198,255,.08),transparent 28%),
        var(--bg);
    color:var(--white);
    overflow-x:hidden;
    padding-bottom:110px;
}

body.locked{
    overflow:hidden;
}

button,input,select,textarea{
    font:inherit;
}

button{
    cursor:pointer;
}

a{
    color:inherit;
    text-decoration:none;
}

img{
    max-width:100%;
    display:block;
}

.container{
    width:min(1180px,92%);
    margin:auto;
}

/* ================= HEADER ================= */

header{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    z-index:1000;
    border-bottom:1px solid transparent;
    transition:.3s;
}

header.scrolled{
    background:rgba(5,9,18,.88);
    backdrop-filter:blur(18px);
    border-color:var(--border);
}

.navbar{
    height:78px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:30px;
}

.logo{
    font-family:"Space Grotesk";
    font-size:25px;
    font-weight:800;
    letter-spacing:-1px;
}

.logo span{
    color:var(--primary2);
}

.nav-links{
    display:flex;
    align-items:center;
    gap:25px;
}

.nav-links a{
    color:#aebed1;
    font-size:14px;
    transition:.25s;
}

.nav-links a:hover{
    color:white;
}

.header-actions{
    display:flex;
    align-items:center;
    gap:10px;
}

.btn{
    border:0;
    padding:13px 20px;
    border-radius:12px;
    font-weight:700;
    transition:.25s;
    display:inline-flex;
    justify-content:center;
    align-items:center;
    gap:8px;
}

.btn:hover{
    transform:translateY(-2px);
}

.btn-primary{
    color:white;
    background:linear-gradient(135deg,var(--primary),var(--primary2));
    box-shadow:0 10px 30px rgba(22,131,255,.22);
}

.btn-outline{
    color:white;
    background:rgba(255,255,255,.04);
    border:1px solid var(--border);
}

.btn-danger{
    background:rgba(255,83,100,.12);
    color:#ff8794;
    border:1px solid rgba(255,83,100,.2);
}

.btn-success{
    background:rgba(39,209,127,.12);
    color:#65eaa3;
    border:1px solid rgba(39,209,127,.2);
}

.mobile-menu{
    display:none;
    border:0;
    background:none;
    color:white;
    font-size:27px;
}

/* ================= HERO ================= */

.hero{
    min-height:850px;
    padding:170px 0 90px;
    position:relative;
    overflow:hidden;
}

.hero::before{
    content:"";
    position:absolute;
    width:600px;
    height:600px;
    background:rgba(0,140,255,.12);
    filter:blur(100px);
    border-radius:50%;
    left:-250px;
    top:100px;
}

.hero-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    align-items:center;
    gap:70px;
}

.badge{
    display:inline-flex;
    padding:8px 13px;
    border-radius:30px;
    border:1px solid rgba(0,198,255,.2);
    background:rgba(0,198,255,.06);
    color:#69ddff;
    font-size:12px;
    font-weight:700;
    margin-bottom:20px;
}

.hero h1{
    font-family:"Space Grotesk";
    font-size:clamp(42px,5vw,70px);
    line-height:1.02;
    letter-spacing:-3px;
    max-width:700px;
}

.hero h1 span{
    background:linear-gradient(90deg,#fff,#50dfff);
    -webkit-background-clip:text;
    color:transparent;
}

.hero p{
    color:var(--muted);
    line-height:1.8;
    font-size:17px;
    max-width:610px;
    margin:25px 0 30px;
}

.hero-actions{
    display:flex;
    gap:12px;
    flex-wrap:wrap;
}

.hero-trust{
    display:flex;
    gap:25px;
    margin-top:35px;
    color:#8194aa;
    font-size:13px;
}

.hero-trust strong{
    color:white;
    display:block;
    font-size:19px;
    margin-bottom:4px;
}

/* mockups */

.hero-preview{
    position:relative;
    min-height:470px;
}

.browser{
    position:absolute;
    border-radius:18px;
    border:1px solid rgba(255,255,255,.15);
    overflow:hidden;
    box-shadow:var(--shadow);
    background:#101a28;
}

.browser.main{
    width:88%;
    right:0;
    top:35px;
    transform:perspective(1000px) rotateY(-5deg) rotateX(2deg);
}

.browser.small{
    width:38%;
    left:0;
    bottom:0;
    z-index:4;
    transform:rotate(-5deg);
}

.browser-top{
    height:30px;
    background:#0b111b;
    display:flex;
    align-items:center;
    gap:5px;
    padding:0 10px;
}

.dot{
    width:7px;
    height:7px;
    border-radius:50%;
    background:#4f5d70;
}

.browser img{
    width:100%;
    height:300px;
    object-fit:cover;
}

.browser.small img{
    height:210px;
}

/* ================= SECTION ================= */

section{
    padding:100px 0;
}

.section-head{
    text-align:center;
    margin-bottom:45px;
}

.section-head span{
    color:var(--primary2);
    font-size:12px;
    text-transform:uppercase;
    letter-spacing:2px;
    font-weight:800;
}

.section-head h2{
    font-family:"Space Grotesk";
    font-size:clamp(32px,4vw,48px);
    margin:12px 0;
}

.section-head p{
    color:var(--muted);
    max-width:650px;
    margin:auto;
    line-height:1.7;
}

/* ================= STATS ================= */

.stats{
    border-top:1px solid var(--border);
    border-bottom:1px solid var(--border);
    background:rgba(255,255,255,.015);
}

.stats-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
}

.stat{
    padding:35px;
    text-align:center;
    border-right:1px solid var(--border);
}

.stat:last-child{
    border-right:0;
}

.stat strong{
    display:block;
    font-family:"Space Grotesk";
    font-size:35px;
}

.stat span{
    color:var(--muted);
    font-size:13px;
}

/* ================= CATALOG & FLIP CARD ================= */

.filters{
    display:flex;
    gap:9px;
    flex-wrap:wrap;
    justify-content:center;
    margin-bottom:35px;
}

.filter{
    background:rgba(255,255,255,.04);
    border:1px solid var(--border);
    color:#a9b8ca;
    padding:10px 15px;
    border-radius:30px;
    transition:.2s;
}

.filter:hover,
.filter.active{
    color:white;
    border-color:rgba(0,198,255,.45);
    background:rgba(0,198,255,.08);
}

.products-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:28px;
}

.flip-card {
    --fc-w: 100%;
    --fc-h: 460px;
    --fc-radius: 20px;
    --fc-bg: #0c1625;
    --fc-ink: #f5f5f5;
    --fc-shadow: #000000;
    --fc-shadow-o: 0.45;
    --fc-glare: 0.22;

    position: relative;
    display: block;
    width: var(--fc-w);
    height: var(--fc-h);
    border-radius: var(--fc-radius);
    outline: none;
    cursor: grab;
    user-select: none;
    -webkit-user-select: none;
    -webkit-touch-callout: none;
    -webkit-tap-highlight-color: transparent;
    touch-action: pan-y;
}

.flip-card[data-dragging="true"] {
    cursor: grabbing;
}

.flip-card__shadow {
    position: absolute;
    inset: 10% 8% -4%;
    border-radius: var(--fc-radius);
    background: color-mix(in srgb, var(--fc-shadow) calc(var(--fc-shadow-o) * 100%), transparent);
    filter: blur(20px);
    pointer-events: none;
}

.flip-card__rotor {
    position: absolute;
    inset: 0;
    transform-style: preserve-3d;
    transition: transform 0.1s cubic-bezier(0.1, 0.9, 0.2, 1);
}

.flip-card__face {
    position: absolute;
    inset: 0;
    overflow: hidden;
    border-radius: var(--fc-radius);
    background: linear-gradient(145deg, rgba(255,255,255,.06), rgba(255,255,255,.015));
    border: 1px solid var(--border);
    color: var(--fc-ink);
    backface-visibility: hidden;
    -webkit-backface-visibility: hidden;
    display: flex;
    flex-direction: column;
}

.flip-card__face img {
    -webkit-user-drag: none;
}

.flip-card__face--front {
    z-index: 2;
}

.flip-card__face--back {
    transform: rotateY(180deg);
    background: #0b1524;
    padding: 24px;
    justify-content: space-between;
}

.flip-card__glare {
    position: absolute;
    inset: 0;
    background: radial-gradient(
        circle farthest-side at var(--fc-gx, 50%) var(--fc-gy, 50%),
        rgba(255, 255, 255, var(--fc-glare)) 0%,
        rgba(255, 255, 255, calc(var(--fc-glare) * 0.5)) 35%,
        rgba(255, 255, 255, 0) 100%
    );
    opacity: var(--fc-sheen, 0);
    pointer-events: none;
    transition: opacity 0.2s ease;
}

.flip-hint {
    font-size: 11px;
    color: var(--primary2);
    text-align: center;
    margin-top: 6px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 4px;
}

.product-image{
    height:210px;
    overflow:hidden;
    position:relative;
    background:#0a111c;
}

.product-image img{
    width:100%;
    height:100%;
    object-fit:cover;
}

.product-badge{
    position:absolute;
    top:13px;
    left:13px;
    background:#0c1827dd;
    border:1px solid rgba(255,255,255,.13);
    backdrop-filter:blur(10px);
    border-radius:8px;
    padding:7px 9px;
    font-size:10px;
    font-weight:800;
}

.product-info{
    padding:20px;
    display: flex;
    flex-direction: column;
    flex: 1;
    justify-content: space-between;
}

.product-category{
    color:var(--primary2);
    text-transform:uppercase;
    letter-spacing:1px;
    font-size:10px;
    font-weight:800;
}

.product-info h3{
    margin:6px 0;
    font-size:20px;
}

.product-info p{
    color:var(--muted);
    line-height:1.6;
    font-size:13px;
}

.techs{
    display:flex;
    gap:5px;
    flex-wrap:wrap;
    margin:10px 0;
}

.techs span{
    font-size:10px;
    padding:4px 8px;
    border-radius:6px;
    background:rgba(255,255,255,.05);
    color:#9fb0c4;
}

.card-actions{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:8px;
    margin-top: 15px;
}

/* ================= SERVICES ================= */

.services-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:15px;
}

.service{
    padding:25px;
    border:1px solid var(--border);
    border-radius:16px;
    background:rgba(255,255,255,.025);
    transition:.25s;
}

.service:hover{
    transform:translateY(-4px);
    background:rgba(22,131,255,.07);
}

.service-icon{
    width:42px;
    height:42px;
    border-radius:12px;
    display:grid;
    place-items:center;
    background:rgba(0,198,255,.1);
    color:var(--cyan);
    margin-bottom:18px;
    font-size:20px;
}

.service h3{
    margin-bottom:8px;
    font-size:16px;
}

.service p{
    color:var(--muted);
    font-size:12px;
    line-height:1.6;
}

/* ================= PROCESS ================= */

.process{
    background:#07101d;
}

.process-grid{
    display:grid;
    grid-template-columns:repeat(6,1fr);
    gap:10px;
}

.step{
    position:relative;
    text-align:center;
}

.step-number{
    width:50px;
    height:50px;
    border-radius:50%;
    display:grid;
    place-items:center;
    margin:0 auto 15px;
    background:linear-gradient(135deg,var(--primary),var(--primary2));
    font-weight:800;
    box-shadow:0 10px 25px rgba(22,131,255,.2);
}

.step h3{
    font-size:14px;
}

.step p{
    font-size:11px;
    color:var(--muted);
    margin-top:7px;
}

/* ================= PLANS ================= */

.plans-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:18px;
}

.plan{
    border:1px solid var(--border);
    border-radius:18px;
    padding:27px;
    background:rgba(255,255,255,.025);
}

.plan.featured{
    border-color:rgba(0,198,255,.45);
    background:linear-gradient(160deg,rgba(0,198,255,.09),rgba(255,255,255,.02));
}

.plan-name{
    color:var(--cyan);
    font-size:12px;
    font-weight:800;
}

.plan h3{
    font-size:24px;
    margin:8px 0;
}

.plan-price{
    font-size:21px;
    font-weight:700;
    color:var(--primary2);
    margin:20px 0;
}

.plan ul{
    list-style:none;
    margin-bottom:22px;
}

.plan li{
    padding:8px 0;
    color:#9fb0c4;
    font-size:13px;
    border-bottom:1px solid rgba(255,255,255,.04);
}

/* ================= FAQ ================= */

.faq{
    max-width:850px;
    margin:auto;
}

.faq-item{
    border:1px solid var(--border);
    border-radius:14px;
    margin-bottom:10px;
    overflow:hidden;
    background:rgba(255,255,255,.025);
}

.faq-question{
    padding:20px;
    display:flex;
    justify-content:space-between;
    gap:20px;
    cursor:pointer;
    font-weight:700;
}

.faq-answer{
    max-height:0;
    overflow:hidden;
    transition:.3s;
    color:var(--muted);
    line-height:1.7;
    font-size:14px;
}

.faq-item.open .faq-answer{
    max-height:200px;
    padding:0 20px 20px;
}

/* ================= TESTIMONIALS ================= */

.testimonials{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:18px;
}

.testimonial{
    padding:25px;
    border:1px solid var(--border);
    border-radius:18px;
    background:rgba(255,255,255,.025);
}

.stars{
    color:#ffc34d;
    margin-bottom:15px;
}

.testimonial p{
    color:#a7b5c6;
    line-height:1.7;
    font-size:13px;
}

.client{
    display:flex;
    align-items:center;
    gap:12px;
    margin-top:20px;
}

.avatar{
    width:42px;
    height:42px;
    border-radius:50%;
    object-fit:cover;
}

.client small{
    display:block;
    color:var(--muted);
    margin-top:3px;
}

/* ================= FOLDER FLOAT ================= */

.folder-float-section {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 80px 0;
    background: radial-gradient(circle at center, rgba(0, 198, 255, 0.05), transparent 70%);
}

.folder-float {
  --ff-w: 220px;
  --ff-h: 155px;
  --ff-r: 16px;
  --ff-tab: 16px;
  --ff-back: #121f33;
  --ff-front: #182a45;
  --ff-paper: #f5f5f5;
  --ff-item-ink: #050912;
  --ff-label: #f5f5f5;
  --ff-spread: 200px;
  --ff-lift: 30px;
  --ff-angle: 34deg;
  --ff-rest: 16deg;
  --ff-open: 520ms;
  --ff-close: 312ms;
  --ff-stagger: 45ms;
  --ff-n: 4;
  --ff-spring: cubic-bezier(0.34, 1.57, 0.64, 1);
  --ff-ease-out: cubic-bezier(0.23, 1, 0.32, 1);

  position: relative;
  display: inline-block;
  width: var(--ff-w);
  padding-top: var(--ff-tab);
  font-family: inherit;
  font-size: 13px;
  font-weight: 600;
  line-height: 1;
  margin-top: 120px;
}

.folder-float__folder {
  position: relative;
  width: var(--ff-w);
  height: var(--ff-h);
}

.folder-float__back {
  position: absolute;
  inset: 0;
  z-index: 0;
  border-radius: var(--ff-r);
  background: var(--ff-back);
  transform: perspective(600px) rotateX(8deg);
  transform-origin: 50% 100%;
}

.folder-float__back::before {
  content: '';
  position: absolute;
  top: calc(-1 * var(--ff-tab));
  left: 0;
  width: 42%;
  height: calc(var(--ff-tab) + var(--ff-r));
  border-radius: var(--ff-r) var(--ff-r) 0 0;
  background: inherit;
}

.folder-float__paper {
  position: absolute;
  top: 10%;
  z-index: 1;
  right: 8%;
  left: 8%;
  height: 50%;
  border-radius: 6px;
  background: var(--ff-paper);
  opacity: 0;
  transform: translateY(10px);
  transition: transform var(--ff-close) var(--ff-ease-out), opacity var(--ff-close) ease;
}

.folder-float__front {
  position: absolute;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 2;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  gap: 6px;
  height: 78%;
  padding: 16px 18px;
  box-sizing: border-box;
  border-radius: var(--ff-r);
  border: 1px solid var(--border);
  background: linear-gradient(180deg, #1d3354, #12223a);
  color: var(--ff-label);
  box-shadow: 0 -10px 24px rgba(0, 0, 0, 0.4);
  transform: perspective(600px) rotateX(calc(-1 * var(--ff-rest)));
  transform-origin: 50% 100%;
  transition: transform var(--ff-open) var(--ff-ease-out);
}

.folder-float__label {
  font-size: 14px;
  font-weight: 700;
}

.folder-float__sub {
  font-size: 11px;
  opacity: 0.65;
}

.folder-float__trigger {
  position: absolute;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 3;
  height: 78%;
  margin: 0;
  padding: 0;
  border: 0;
  border-radius: var(--ff-r);
  background: transparent;
  cursor: pointer;
  outline: none;
  -webkit-tap-highlight-color: transparent;
}

.folder-float[data-open] .folder-float__front {
  transform: perspective(600px) rotateX(calc(-1 * var(--ff-angle)));
}

.folder-float[data-open] .folder-float__paper {
  opacity: 1;
  transform: translateY(0);
  transition: transform var(--ff-open) var(--ff-ease-out), opacity 200ms ease;
}

.folder-float__items {
  position: absolute;
  top: var(--ff-tab);
  left: 50%;
  z-index: 1;
  width: 0;
  height: 0;
}

.folder-float[data-open] .folder-float__items::before {
  content: '';
  position: absolute;
  top: calc(-1 * (var(--ff-lift) + 120px));
  left: calc(-1 * (var(--ff-spread) + 100px));
  width: calc(2 * var(--ff-spread) + 200px);
  height: calc(var(--ff-lift) + 120px);
}

.folder-float__item {
  position: absolute;
  top: 0;
  left: 50%;
  margin: 0;
  padding: 0 16px;
  height: 36px;
  border: 0;
  border-radius: 18px;
  background: linear-gradient(135deg, #35e7ff, #00c6ff);
  color: var(--ff-item-ink);
  font: inherit;
  font-weight: 700;
  white-space: nowrap;
  box-shadow: 0 6px 20px rgba(0, 198, 255, 0.35);
  cursor: pointer;
  outline: none;
  opacity: 0;
  transform: translate(-50%, 44px) scale(0.6);
  transform-origin: 50% 50%;
  pointer-events: none;
  -webkit-tap-highlight-color: transparent;
  transition: transform var(--ff-close) var(--ff-ease-out) calc((var(--ff-n) - 1 - var(--i)) * var(--ff-stagger) * 0.5), opacity 160ms ease;
}

.folder-float[data-open] .folder-float__item {
  opacity: 1;
  transform: translate(calc(-50% + var(--x, 0px)), var(--y, 0px)) rotate(var(--r, 0deg)) scale(1);
  pointer-events: auto;
  transition: transform var(--ff-open) var(--ff-spring) calc(var(--i) * var(--ff-stagger)), opacity 160ms ease;
}

.folder-float__drift {
  display: block;
  animation: folder-float-drift 3.2s ease-in-out infinite;
  animation-delay: calc(var(--i) * -0.7s);
  animation-play-state: paused;
}

.folder-float[data-open] .folder-float__drift {
  animation-play-state: running;
}

@keyframes folder-float-drift {
  0%, 100% { translate: 0 0; }
  50% { translate: 0 -4px; }
}

/* ================= DOCK MENU ================= */
.dock-outer {
    position: fixed;
    bottom: 20px;
    left: 0;
    width: 100%;
    display: flex;
    justify-content: center;
    z-index: 1200;
    pointer-events: none;
}

.dock-panel {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 10px 14px;
    background: rgba(12, 22, 37, 0.85);
    backdrop-filter: blur(18px);
    border: 1px solid var(--border);
    border-radius: 24px;
    box-shadow: var(--shadow);
    pointer-events: auto;
}

.dock-item {
    position: relative;
    width: 48px;
    height: 48px;
    border-radius: 14px;
    background: rgba(255, 255, 255, 0.04);
    border: 1px solid var(--border);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    transition: width 0.2s cubic-bezier(0.1, 0.9, 0.2, 1), height 0.2s cubic-bezier(0.1, 0.9, 0.2, 1), background 0.2s;
}

.dock-item:hover {
    background: rgba(0, 198, 255, 0.12);
    border-color: rgba(0, 198, 255, 0.35);
}

.dock-icon {
    font-size: 20px;
    line-height: 1;
}

.dock-label {
    position: absolute;
    bottom: -22px;
    background: rgba(5, 9, 18, 0.9);
    border: 1px solid var(--border);
    padding: 3px 8px;
    border-radius: 6px;
    font-size: 10px;
    font-weight: 600;
    color: var(--white);
    white-space: nowrap;
    opacity: 0;
    pointer-events: none;
    transform: translateY(4px);
    transition: 0.2s ease;
}

.dock-item:hover .dock-label {
    opacity: 1;
    transform: translateY(0);
}

/* ================= FOOTER ================= */

footer{
    border-top:1px solid var(--border);
    padding:60px 0 25px;
    background:#030711;
}

.footer-grid{
    display:grid;
    grid-template-columns:2fr repeat(3,1fr);
    gap:40px;
}

.footer-brand p{
    color:var(--muted);
    max-width:350px;
    line-height:1.7;
    margin-top:15px;
    font-size:13px;
}

footer h4{
    margin-bottom:15px;
}

footer ul{
    list-style:none;
}

footer li{
    color:#8292a6;
    margin:9px 0;
    font-size:13px;
}

.copyright{
    border-top:1px solid var(--border);
    margin-top:40px;
    padding-top:20px;
    color:#657487;
    font-size:12px;
    text-align:center;
}

/* ================= FLOATING WHATSAPP ================= */

.whatsapp{
    position:fixed;
    right:22px;
    bottom:140px;
    z-index:900;
    width:58px;
    height:58px;
    border-radius:50%;
    display:grid;
    place-items:center;
    background:#25d366;
    color:white;
    font-size:26px;
    box-shadow:0 12px 35px rgba(37,211,102,.25);
    transition:transform .2s ease, box-shadow .2s ease;
}

.whatsapp svg{
    width:30px;
    height:30px;
}

.whatsapp:hover{
    transform:translateY(-3px) scale(1.04);
    box-shadow:0 16px 40px rgba(37,211,102,.35);
}


/* ================= WHATSAPP SEND STATUS ================= */
.whatsapp-send-btn{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    gap:9px;
    min-width:210px;
}
.status-mark{
    width:20px;
    height:20px;
    display:inline-grid;
    place-items:center;
    flex:0 0 20px;
    color:currentColor;
}
.status-mark-svg{width:20px;height:20px;overflow:visible}
.status-track,.status-progress{
    fill:none;
    stroke:currentColor;
    stroke-width:2;
    transform:rotate(-90deg);
    transform-origin:50% 50%;
}
.status-track{opacity:.18}
.status-progress{
    stroke-linecap:round;
    stroke-dasharray:56.55;
    stroke-dashoffset:56.55;
    transition:stroke-dashoffset .24s ease;
}
.status-check{
    fill:none;
    stroke:#22c55e;
    stroke-width:2;
    stroke-linecap:round;
    stroke-linejoin:round;
    opacity:0;
    stroke-dasharray:14;
    stroke-dashoffset:14;
    transition:opacity .18s ease,stroke-dashoffset .24s ease;
}
.status-mark[data-status="running"] .status-progress{
    animation:statusSpin 1.1s linear infinite;
}
.status-mark[data-status="done"] .status-progress{
    stroke:#22c55e;
    stroke-dashoffset:0;
    animation:none;
}
.status-mark[data-status="done"] .status-check{
    opacity:1;
    stroke-dashoffset:0;
}
@keyframes statusSpin{to{transform:rotate(270deg)}}
.whatsapp-send-btn[data-sending="true"]{opacity:.9;cursor:wait}

/* ================= MODALS ================= */

.modal-overlay{
    position:fixed;
    inset:0;
    background:rgba(0,0,0,.72);
    backdrop-filter:blur(10px);
    z-index:2000;
    display:none;
    align-items:center;
    justify-content:center;
    padding:20px;
}

.modal-overlay.show{
    display:flex;
}

.modal{
    width:min(900px,100%);
    max-height:92vh;
    overflow:auto;
    background:#091321;
    border:1px solid var(--border);
    border-radius:22px;
    box-shadow:var(--shadow);
    animation:modalIn .25s ease;
}

@keyframes modalIn{
    from{opacity:0;transform:translateY(20px) scale(.98)}
    to{opacity:1;transform:none}
}

.modal-head{
    padding:20px 24px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    border-bottom:1px solid var(--border);
}

.close{
    border:0;
    background:rgba(255,255,255,.06);
    color:white;
    width:36px;
    height:36px;
    border-radius:10px;
    font-size:20px;
}

.modal-body{
    padding:25px;
}

/* product detail */

.detail-grid{
    display:grid;
    grid-template-columns:1.1fr .9fr;
    gap:25px;
}

.detail-main-image{
    height:330px;
    width:100%;
    object-fit:cover;
    border-radius:16px;
    border:1px solid var(--border);
}

.gallery{
    display:flex;
    gap:8px;
    margin-top:10px;
    overflow:auto;
}

.gallery img{
    width:75px;
    height:55px;
    object-fit:cover;
    border-radius:8px;
    cursor:pointer;
    border:2px solid transparent;
}

.gallery img.active{
    border-color:var(--primary2);
}

.feature-list{
    list-style:none;
    margin:18px 0;
}

.feature-list li{
    padding:9px 0;
    border-bottom:1px solid var(--border);
    color:#a6b6c9;
    font-size:13px;
}

.feature-list li::before{
    content:"✓";
    color:var(--success);
    margin-right:8px;
}

/* forms */

.form-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:14px;
}

.field{
    margin-bottom:14px;
}

.field.full{
    grid-column:1/-1;
}

.field label{
    display:block;
    margin-bottom:7px;
    font-size:12px;
    color:#aab8ca;
}

.field input,
.field select,
.field textarea{
    width:100%;
    border:1px solid var(--border);
    background:#07101c;
    color:white;
    border-radius:10px;
    padding:12px;
    outline:none;
}

.field textarea{
    min-height:100px;
    resize:vertical;
}

.field input:focus,
.field select:focus,
.field textarea:focus{
    border-color:rgba(0,198,255,.55);
}

.modal-actions{
    display:flex;
    justify-content:flex-end;
    gap:10px;
    margin-top:20px;
}

/* ================= CART / SOLICITAÇÃO ================= */

.cart-list{
    display:flex;
    flex-direction:column;
    gap:10px;
}

.cart-item{
    display:grid;
    grid-template-columns:70px 1fr auto;
    gap:13px;
    align-items:center;
    padding:12px;
    border:1px solid var(--border);
    border-radius:12px;
}

.cart-item img{
    width:70px;
    height:50px;
    object-fit:cover;
    border-radius:8px;
}

.cart-item h4{
    font-size:14px;
}

.cart-item small{
    color:var(--muted);
}

.cart-summary{
    margin-top:20px;
    border-top:1px solid var(--border);
    padding-top:20px;
}

/* ================= ADMIN ================= */

.admin-overlay{
    position:fixed;
    inset:0;
    background:#050a12;
    z-index:5000;
    display:none;
}

.admin-overlay.show{
    display:block;
}

.admin-login{
    position:absolute;
    inset:0;
    display:grid;
    place-items:center;
    background:
        radial-gradient(circle at 50% 20%,rgba(22,131,255,.16),transparent 35%),
        #050a12;
}

.login-box{
    width:min(420px,92%);
    padding:35px;
    border:1px solid var(--border);
    border-radius:22px;
    background:rgba(10,20,34,.85);
    box-shadow:var(--shadow);
}

.login-box h2{
    font-family:"Space Grotesk";
    font-size:30px;
    margin-bottom:8px;
}

.login-box p{
    color:var(--muted);
    font-size:13px;
    line-height:1.6;
    margin-bottom:25px;
}

.admin-layout{
    display:grid;
    grid-template-columns:245px 1fr;
    height:100%;
}

.admin-sidebar{
    background:#07101b;
    border-right:1px solid var(--border);
    padding:20px;
    overflow:auto;
}

.admin-brand{
    font-family:"Space Grotesk";
    font-size:22px;
    font-weight:800;
    margin-bottom:25px;
}

.admin-brand span{
    color:var(--primary2);
}

.admin-menu{
    display:flex;
    flex-direction:column;
    gap:5px;
}

.admin-menu button{
    width:100%;
    text-align:left;
    border:0;
    background:transparent;
    color:#8fa2b7;
    padding:12px;
    border-radius:9px;
}

.admin-menu button:hover,
.admin-menu button.active{
    background:rgba(22,131,255,.12);
    color:white;
}

.admin-main{
    overflow:auto;
}

.admin-topbar{
    height:70px;
    border-bottom:1px solid var(--border);
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:0 25px;
    background:rgba(5,9,18,.8);
    backdrop-filter:blur(15px);
}

.admin-content{
    padding:25px;
}

.admin-section{
    display:none;
}

.admin-section.active{
    display:block;
}

.admin-title{
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:15px;
    margin-bottom:22px;
}

.admin-title h2{
    font-family:"Space Grotesk";
}

.dashboard-cards{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:15px;
    margin-bottom:25px;
}

.dashboard-card{
    padding:20px;
    border:1px solid var(--border);
    border-radius:15px;
    background:rgba(255,255,255,.025);
}

.dashboard-card span{
    color:var(--muted);
    font-size:12px;
}

.dashboard-card strong{
    display:block;
    font-size:28px;
    margin-top:7px;
}

.admin-table{
    width:100%;
    border-collapse:collapse;
    background:rgba(255,255,255,.02);
    border:1px solid var(--border);
    border-radius:15px;
    overflow:hidden;
}

.admin-table th,
.admin-table td{
    padding:13px;
    border-bottom:1px solid var(--border);
    text-align:left;
    font-size:12px;
}

.admin-table th{
    color:#8fa2b7;
    font-weight:600;
}

.admin-table td{
    color:#d9e3ef;
}

.table-product{
    display:flex;
    align-items:center;
    gap:10px;
}

.table-product img{
    width:45px;
    height:32px;
    border-radius:6px;
    object-fit:cover;
}

.status{
    display:inline-block;
    padding:5px 8px;
    border-radius:7px;
    font-size:10px;
    background:rgba(255,255,255,.06);
}

.status.ativo{
    color:#65eaa3;
    background:rgba(39,209,127,.1);
}

.status.pendente{
    color:#ffd074;
    background:rgba(255,189,74,.1);
}

.admin-actions{
    display:flex;
    gap:5px;
    flex-wrap:wrap;
}

.small-btn{
    padding:7px 9px;
    font-size:10px;
    border-radius:7px;
    border:1px solid var(--border);
    background:rgba(255,255,255,.04);
    color:white;
}

.admin-empty{
    text-align:center;
    padding:40px;
    color:var(--muted);
}

/* ================= TOAST ================= */

.toast-container{
    position:fixed;
    right:20px;
    top:90px;
    z-index:7000;
    display:flex;
    flex-direction:column;
    gap:10px;
}

.toast{
    min-width:270px;
    max-width:380px;
    padding:14px 17px;
    border-radius:12px;
    background:#101c2c;
    border:1px solid var(--border);
    box-shadow:var(--shadow);
    animation:toastIn .25s ease;
    font-size:13px;
}

@keyframes toastIn{
    from{opacity:0;transform:translateX(20px)}
    to{opacity:1;transform:none}
}

/* ================= RESPONSIVE ================= */

@media(max-width:1000px){
    .nav-links{display:none}
    .mobile-menu{display:block}
    .hero-grid{grid-template-columns:1fr}
    .hero{padding-top:130px}
    .hero-preview{max-width:700px;margin:auto;width:100%}
    .products-grid{grid-template-columns:repeat(2,1fr)}
    .services-grid{grid-template-columns:repeat(2,1fr)}
    .plans-grid{grid-template-columns:repeat(2,1fr)}
    .process-grid{grid-template-columns:repeat(3,1fr);gap:30px}
    .admin-layout{grid-template-columns:80px 1fr}
    .admin-brand{font-size:0;text-align:center}
    .admin-brand::before{content:"D";font-size:25px;color:var(--cyan)}
    .admin-menu button{font-size:0;text-align:center}
    .admin-menu button::first-letter{font-size:20px}
    .dashboard-cards{grid-template-columns:repeat(2,1fr)}
}

@media(max-width:650px){
    .navbar{height:68px}
    .header-actions .btn-outline{display:none}
    .hero h1{letter-spacing:-2px}
    .hero-trust{gap:15px;flex-wrap:wrap}
    .browser.main{width:94%}
    .browser.small{width:45%}
    .browser img{height:220px}
    .browser.small img{height:150px}
    .stats-grid{grid-template-columns:1fr 1fr}
    .stat{padding:25px 10px;border-bottom:1px solid var(--border)}
    .products-grid,
    .services-grid,
    .plans-grid,
    .testimonials{
        grid-template-columns:1fr;
    }
    .process-grid{grid-template-columns:1fr 1fr}
    .detail-grid{grid-template-columns:1fr}
    .form-grid{grid-template-columns:1fr}
    .field.full{grid-column:auto}
    .admin-topbar{padding:0 12px}
    .admin-content{padding:15px}
    .admin-title{align-items:flex-start;flex-direction:column}
    .admin-table{display:block;overflow-x:auto;white-space:nowrap}
    .admin-sidebar{padding:10px}
    .admin-layout{grid-template-columns:65px 1fr}
}

/* ================= AERO SHARDS HERO ================= */
.aero-shards-bg{position:absolute;inset:0;overflow:hidden;pointer-events:none;z-index:0;background:#120F17}
.hero{position:relative;isolation:isolate;overflow:hidden}
.hero>.container{position:relative;z-index:2}
.aero-shards-canvas{width:100%;height:100%;display:block}
.aero-shard{position:absolute;left:50%;top:50%;width:clamp(22px,4vw,70px);height:clamp(7px,1.2vw,18px);border-radius:999px;transform-origin:center;opacity:.65;will-change:transform}
@media (prefers-reduced-motion:reduce){.aero-shard{animation:none!important;transition:none!important}}
</style>
</head>

<body>

<!-- ================= HEADER ================= -->

<header id="header">
<div class="container navbar">

<a href="#inicio" class="logo">Dev<span>Sites</span></a>

<nav class="nav-links">
<a href="#inicio">Início</a>
<a href="#sites">Sites</a>
<a href="#categorias">Categorias</a>
<a href="#processo">Como Funciona</a>
<a href="#planos">Planos</a>
<a href="#depoimentos">Depoimentos</a>
<a href="#faq">FAQ</a>
<a href="#contato">Contato</a>
</nav>

<div class="header-actions">
<button class="btn btn-outline" onclick="openCart()">📋 <span id="cartCount">0</span></button>
<button class="btn btn-primary" onclick="scrollToSites()">Ver Sites</button>
</div>

<button class="mobile-menu" onclick="toggleMobileMenu()">☰</button>

</div>
</header>

<!-- ================= HERO ================= -->

<main>

<section class="hero" id="inicio">
<div id="aeroShardsHero" class="aero-shards-bg" aria-hidden="true"></div>
<div class="container hero-grid">

<div>
<div class="badge">● PLATAFORMA DE SITES PROFISSIONAIS</div>

<h1>
Sites profissionais para <span>transformar</span> sua presença digital.
</h1>

<p>
Escolha um modelo pronto, personalize sua identidade ou solicite um projeto desenvolvido especialmente para sua empresa.
</p>

<div class="hero-actions">
<button class="btn btn-primary" onclick="scrollToSites()">Explorar Sites →</button>
<button class="btn btn-outline" onclick="openContact()">Quero meu Site</button>
</div>

<div class="hero-trust">
<div>
<strong>+100</strong>
Sites desenvolvidos
</div>

<div>
<strong>+50</strong>
Empresas atendidas
</div>

<div>
<strong>98%</strong>
Clientes satisfeitos
</div>
</div>
</div>

<div class="hero-preview">

<div class="browser main">
<div class="browser-top">
<i class="dot"></i><i class="dot"></i><i class="dot"></i>
</div>
<img src="https://images.unsplash.com/photo-1556742049-0cfed4f6a45d?auto=format&fit=crop&w=1200&q=85" alt="Loja virtual DevSites">
</div>

<div class="browser small">
<div class="browser-top">
<i class="dot"></i><i class="dot"></i><i class="dot"></i>
</div>
<img src="https://images.unsplash.com/photo-1497366754035-f200968a6e72?auto=format&fit=crop&w=700&q=85" alt="Site empresarial DevSites">
</div>

</div>
</div>
</section>

<!-- ================= STATS ================= -->

<section class="stats">
<div class="container stats-grid">

<div class="stat">
<strong data-count="100">0</strong>
<span>Sites desenvolvidos</span>
</div>

<div class="stat">
<strong data-count="50">0</strong>
<span>Empresas atendidas</span>
</div>

<div class="stat">
<strong data-count="30">0</strong>
<span>Modelos disponíveis</span>
</div>

<div class="stat">
<strong data-count="98">0</strong>
<span>Clientes satisfeitos</span>
</div>

</div>
</section>

<!-- ================= SITES ================= -->

<section id="sites">
<div class="container">

<div class="section-head">
<span>CATÁLOGO</span>
<h2>Escolha o site ideal para seu negócio</h2>
<p>
Clique ou arraste o card para ver os detalhes do projeto no verso.
</p>
</div>

<div class="filters" id="filters"></div>

<div class="products-grid" id="productsGrid"></div>

</div>
</section>

<!-- ================= SERVICES ================= -->

<section id="categorias">
<div class="container">

<div class="section-head">
<span>SERVIÇOS</span>
<h2>Mais do que um site</h2>
<p>
Soluções digitais para diferentes necessidades.
</p>
</div>

<div class="services-grid">

<div class="service">
<div class="service-icon">⌘</div>
<h3>Criação de Sites</h3>
<p>Sites modernos, rápidos e responsivos.</p>
</div>

<div class="service">
<div class="service-icon">↗</div>
<h3>Landing Pages</h3>
<p>Páginas focadas em conversão.</p>
</div>

<div class="service">
<div class="service-icon">▣</div>
<h3>Lojas Virtuais</h3>
<p>Estruturas preparadas para vendas online.</p>
</div>

<div class="service">
<div class="service-icon">⌘</div>
<h3>Sistemas Web</h3>
<p>Sistemas personalizados para empresas.</p>
</div>

<div class="service">
<div class="service-icon">▤</div>
<h3>Painéis Administrativos</h3>
<p>Controle seus dados através de dashboards.</p>
</div>

<div class="service">
<div class="service-icon">◈</div>
<h3>SEO</h3>
<p>Estrutura preparada para mecanismos de busca.</p>
</div>

<div class="service">
<div class="service-icon">⚡</div>
<h3>Performance</h3>
<p>Otimização para carregamento rápido.</p>
</div>

<div class="service">
<div class="service-icon">◉</div>
<h3>Integrações</h3>
<p>WhatsApp, APIs e ferramentas externas.</p>
</div>

</div>
</div>
</section>

<!-- ================= PROCESS ================= -->

<section class="process" id="processo">
<div class="container">

<div class="section-head">
<span>PROCESSO</span>
<h2>Como funciona</h2>
<p>Um processo simples para colocar seu projeto no ar.</p>
</div>

<div class="process-grid">

<div class="step">
<div class="step-number">01</div>
<h3>Escolha</h3>
<p>Escolha seu site.</p>
</div>

<div class="step">
<div class="step-number">02</div>
<h3>Envie seus dados</h3>
<p>Logo, textos e informações.</p>
</div>

<div class="step">
<div class="step-number">03</div>
<h3>Personalizamos</h3>
<p>Aplicamos sua identidade.</p>
</div>

<div class="step">
<div class="step-number">04</div>
<h3>Aprovação</h3>
<p>Você revisa o projeto.</p>
</div>

<div class="step">
<div class="step-number">05</div>
<h3>Publicação</h3>
<p>Colocamos seu site no ar.</p>
</div>

<div class="step">
<div class="step-number">06</div>
<h3>Comece</h3>
<p>Seu negócio online.</p>
</div>

</div>
</div>
</section>

<!-- ================= PLANS ================= -->

<section id="planos">
<div class="container">

<div class="section-head">
<span>PLANOS</span>
<h2>Escolha o nível do seu projeto</h2>
<p>Estruturas para diferentes necessidades.</p>
</div>

<div class="plans-grid">

<div class="plan">
<div class="plan-name">STARTER</div>
<h3>Pequenos negócios</h3>
<div class="plan-price">Sob consulta</div>
<ul>
<li>✓ Site responsivo</li>
<li>✓ Até 5 páginas</li>
<li>✓ WhatsApp</li>
<li>✓ Formulário</li>
<li>✓ SEO básico</li>
</ul>
<button class="btn btn-outline" style="width:100%" onclick="openContact('Starter')">Solicitar Projeto</button>
</div>

<div class="plan featured">
<div class="plan-name">PROFISSIONAL</div>
<h3>Empresas</h3>
<div class="plan-price">Sob consulta</div>
<ul>
<li>✓ Até 10 páginas</li>
<li>✓ Design personalizado</li>
<li>✓ WhatsApp</li>
<li>✓ SEO</li>
<li>✓ Otimização</li>
</ul>
<button class="btn btn-primary" style="width:100%" onclick="openContact('Profissional')">Solicitar Projeto</button>
</div>

<div class="plan">
<div class="plan-name">PREMIUM</div>
<h3>Projetos completos</h3>
<div class="plan-price">Sob consulta</div>
<ul>
<li>✓ Design premium</li>
<li>✓ Painel administrativo</li>
<li>✓ Integrações</li>
<li>✓ SEO avançado</li>
<li>✓ Suporte</li>
</ul>
<button class="btn btn-outline" style="width:100%" onclick="openContact('Premium')">Solicitar Projeto</button>
</div>

<div class="plan">
<div class="plan-name">CUSTOM</div>
<h3>Projeto exclusivo</h3>
<div class="plan-price">Sob consulta</div>
<ul>
<li>✓ Sistema personalizado</li>
<li>✓ Banco de dados</li>
<li>✓ APIs</li>
<li>✓ Painel completo</li>
<li>✓ Arquitetura escalável</li>
</ul>
<button class="btn btn-outline" style="width:100%" onclick="openContact('Custom')">Solicitar</button>
</div>

</div>
</div>
</section>

<!-- ================= TESTIMONIALS ================= -->

<section id="depoimentos">
<div class="container">

<div class="section-head">
<span>CLIENTES</span>
<h2>O que nossos clientes dizem</h2>
</div>

<div class="testimonials">

<div class="testimonial">
<div class="stars">★★★★★</div>
<p>
"Precisávamos de uma presença digital mais profissional e a estrutura do site facilitou muito nosso atendimento."
</p>
<div class="client">
<img class="avatar" src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=100&q=80" alt="Rafael Martins">
<div>
<strong>Rafael Martins</strong>
<small>Empresa Alpha</small>
</div>
</div>
</div>

<div class="testimonial">
<div class="stars">★★★★★</div>
<p>
"O catálogo de modelos ajudou nossa equipe a escolher rapidamente o estilo que queríamos."
</p>
<div class="client">
<img class="avatar" src="https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=100&q=80" alt="Juliana Costa">
<div>
<strong>Juliana Costa</strong>
<small>Studio Prime</small>
</div>
</div>
</div>

<div class="testimonial">
<div class="stars">★★★★★</div>
<p>
"O projeto ficou responsivo e com uma aparência muito mais profissional para nossa empresa."
</p>
<div class="client">
<img class="avatar" src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&w=100&q=80" alt="Lucas Almeida">
<div>
<strong>Lucas Almeida</strong>
<small>Tech Company</small>
</div>
</div>
</div>

</div>
</div>
</section>

<!-- ================= FOLDER FLOAT SECTION ================= -->

<section class="folder-float-section">
<div class="container" style="text-align:center">
<div class="section-head">
<span>FEEDBACK RÁPIDO</span>
<h2>O que dizem sobre nossas entregas</h2>
<p>Passe o mouse ou clique na pasta abaixo para ver os destaques dos nossos projetos.</p>
</div>

<div class="folder-float" id="folderFloatApp">
<div class="folder-float__items" id="folderItems"></div>
<div class="folder-float__folder">
    <span class="folder-float__back" aria-hidden="true"></span>
    <span class="folder-float__paper" aria-hidden="true"></span>
    <span class="folder-float__front" aria-hidden="true">
        <span class="folder-float__label">DevSites Feedback</span>
        <span class="folder-float__sub">4 notas exclusivas</span>
    </span>
    <button type="button" class="folder-float__trigger" id="folderTrigger" aria-label="Abrir pasta de feedbacks"></button>
</div>
</div>

</div>
</section>

<!-- ================= FAQ ================= -->

<section id="faq">
<div class="container">

<div class="section-head">
<span>FAQ</span>
<h2>Perguntas frequentes</h2>
</div>

<div class="faq">

<div class="faq-item">
<div class="faq-question">Como funciona a solicitação de um site? <span>+</span></div>
<div class="faq-answer">Você pode escolher um modelo no catálogo ou solicitar um orçamento sob medida. Nossa equipe entrará em contato para alinhar os detalhes.</div>
</div>

<div class="faq-item">
<div class="faq-question">Quanto tempo demora? <span>+</span></div>
<div class="faq-answer">O prazo varia conforme a complexidade, quantidade de páginas e nível de personalização.</div>
</div>

<div class="faq-item">
<div class="faq-question">O site funciona no celular? <span>+</span></div>
<div class="faq-answer">Sim. Os modelos desta plataforma são estruturados para desktop, tablet e celular.</div>
</div>

<div class="faq-item">
<div class="faq-question">Posso alterar as cores? <span>+</span></div>
<div class="faq-answer">Sim. A personalização pode incluir cores, fontes, textos, imagens, logo e identidade visual.</div>
</div>

<div class="faq-item">
<div class="faq-question">Vocês criam lojas virtuais? <span>+</span></div>
<div class="faq-answer">Sim. Existem modelos específicos para lojas e estruturas que podem ser ampliadas para e-commerce.</div>
</div>

<div class="faq-item">
<div class="faq-question">O site possui painel administrativo? <span>+</span></div>
<div class="faq-answer">Alguns projetos possuem painel administrativo. Recursos específicos podem ser adicionados conforme o projeto.</div>
</div>

<div class="faq-item">
<div class="faq-question">Posso colocar meu domínio? <span>+</span></div>
<div class="faq-answer">Sim. O projeto pode ser publicado em um domínio próprio após a configuração da hospedagem.</div>
</div>

<div class="faq-item">
<div class="faq-question">Vocês fazem manutenção? <span>+</span></div>
<div class="faq-answer">Sim. Serviços de manutenção e evolução podem ser contratados separadamente.</div>
</div>

<div class="faq-item">
<div class="faq-question">Posso solicitar um projeto personalizado? <span>+</span></div>
<div class="faq-answer">Sim. Utilize a opção "Quero meu Site" para enviar as informações do projeto.</div>
</div>

</div>
</div>
</section>

</main>

<!-- ================= DOCK MENU ================= -->

<div class="dock-outer" id="dockOuter">
  <div class="dock-panel" id="dockPanel" role="toolbar" aria-label="Navegação rápida">
    <div class="dock-item" role="button" tabindex="0" aria-label="Início" onclick="document.getElementById('inicio').scrollIntoView({behavior:'smooth'})">
      <div class="dock-icon">🏠</div>
      <div class="dock-label">Início</div>
    </div>
    <div class="dock-item" role="button" tabindex="0" aria-label="Sites" onclick="scrollToSites()">
      <div class="dock-icon">🖥️</div>
      <div class="dock-label">Sites</div>
    </div>
    <div class="dock-item" role="button" tabindex="0" aria-label="Planos" onclick="document.getElementById('planos').scrollIntoView({behavior:'smooth'})">
      <div class="dock-icon">💎</div>
      <div class="dock-label">Planos</div>
    </div>
    <div class="dock-item" role="button" tabindex="0" aria-label="Solicitações" onclick="openCart()">
      <div class="dock-icon">📋</div>
      <div class="dock-label">Solicitações</div>
    </div>
    <div class="dock-item" role="button" tabindex="0" aria-label="Painel Admin" onclick="openAdmin()">
      <div class="dock-icon">⚙️</div>
      <div class="dock-label">Admin</div>
    </div>
  </div>
</div>

<!-- ================= FOOTER ================= -->

<footer id="contato">
<div class="container">

<div class="footer-grid">

<div class="footer-brand">
<a class="logo">Dev<span>Sites</span></a>
<p>
Sites profissionais para empresas que querem crescer.
</p>
</div>

<div>
<h4>Empresa</h4>
<ul>
<li><a href="#sites">Sites</a></li>
<li><a href="#planos">Planos</a></li>
<li><a href="#processo">Como funciona</a></li>
<li><a href="#faq">FAQ</a></li>
</ul>
</div>

<div>
<h4>Serviços</h4>
<ul>
<li>Sites profissionais</li>
<li>Lojas virtuais</li>
<li>Sistemas Web</li>
<li>SEO</li>
<li>Manutenção</li>
</ul>
</div>

<div>
<h4>Contato</h4>
<ul>
<li>WhatsApp</li>
<li>Instagram</li>
<li>Facebook</li>
<li>LinkedIn</li>
</ul>
</div>

</div>

<div class="copyright">
© 2026 DevSites. Todos os direitos reservados.
</div>

</div>
</footer>

<a class="whatsapp" href="https://wa.me/5547992170175?text=Olá!%20Gostaria%20de%20conhecer%20os%20sites%20disponíveis%20da%20DevSites." target="_blank" aria-label="WhatsApp"><svg viewBox="0 0 24 24" aria-hidden="true"><path d="M20.52 3.48A11.86 11.86 0 0 0 12.06 0C5.5 0 .16 5.34.16 11.9c0 2.1.55 4.15 1.6 5.96L.06 24l6.28-1.65a11.9 11.9 0 0 0 5.72 1.46h.01c6.56 0 11.9-5.34 11.9-11.9 0-3.18-1.24-6.16-3.45-8.43ZM12.07 21.8h-.01a9.9 9.9 0 0 1-5.05-1.38l-.36-.21-3.73.98 1-3.64-.23-.37a9.88 9.88 0 0 1-1.52-5.28C2.17 6.44 6.61 2 12.07 2a9.84 9.84 0 0 1 7 2.9 9.84 9.84 0 0 1 2.9 7c0 5.46-4.44 9.9-9.9 9.9Zm5.43-7.42c-.3-.15-1.77-.87-2.04-.97-.27-.1-.47-.15-.67.15-.2.3-.77.97-.95 1.17-.17.2-.35.22-.65.07-.3-.15-1.25-.46-2.38-1.47-.88-.78-1.47-1.74-1.64-2.04-.17-.3-.02-.46.13-.61.13-.13.3-.35.45-.52.15-.17.2-.3.3-.5.1-.2.05-.37-.02-.52-.07-.15-.67-1.62-.92-2.22-.24-.58-.49-.5-.67-.51h-.57c-.2 0-.52.07-.79.37-.27.3-1.04 1.02-1.04 2.49s1.07 2.89 1.22 3.09c.15.2 2.1 3.2 5.08 4.49.71.31 1.26.5 1.69.64.71.23 1.36.2 1.87.12.57-.08 1.77-.72 2.02-1.42.25-.7.25-1.3.17-1.42-.07-.12-.27-.2-.57-.35Z" fill="currentColor"/></svg></a>

<!-- ================= PRODUCT MODAL ================= -->

<div class="modal-overlay" id="productModal">
<div class="modal">

<div class="modal-head">
<h2 id="detailTitle">Site</h2>
<button class="close" onclick="closeModal('productModal')">×</button>
</div>

<div class="modal-body">
<div class="detail-grid">

<div>
<img id="detailMainImage" class="detail-main-image" src="" alt="">
<div id="detailGallery" class="gallery"></div>
</div>

<div>
<div id="detailCategory" class="product-category"></div>
<h2 id="detailName"></h2>
<p id="detailDescription" style="color:var(--muted);line-height:1.7;margin-top:12px"></p>

<ul id="detailFeatures" class="feature-list"></ul>

<div class="techs" id="detailTechs"></div>

<div class="modal-actions">
<button class="btn btn-outline" onclick="requestCustomization()">Personalizar</button>
<button class="btn btn-primary" onclick="requestCurrentProduct()">Solicitar Projeto</button>
</div>

</div>

</div>
</div>

</div>
</div>

<!-- ================= CART / SOLICITAÇÕES MODAL ================= -->

<div class="modal-overlay" id="cartModal">
<div class="modal" style="max-width:650px">

<div class="modal-head">
<h2>Projetos Selecionados</h2>
<button class="close" onclick="closeModal('cartModal')">×</button>
</div>

<div class="modal-body">

<div id="cartItems" class="cart-list"></div>

<div class="cart-summary">
<p style="color:var(--muted);font-size:13px;line-height:1.6;margin-bottom:15px">
Envie sua seleção para receber uma proposta personalizada sem compromisso.
</p>
<div class="modal-actions">
<button class="btn btn-primary" onclick="openCheckout()">Solicitar Proposta</button>
</div>
</div>

</div>
</div>
</div>

<!-- ================= CHECKOUT / SOLICITAÇÃO ================= -->

<div class="modal-overlay" id="checkoutModal">
<div class="modal" style="max-width:700px">

<div class="modal-head">
<h2>Enviar Solicitação de Projeto</h2>
<button class="close" onclick="closeModal('checkoutModal')">×</button>
</div>

<div class="modal-body">

<div class="form-grid">

<div class="field">
<label>Nome *</label>
<input id="checkoutName" required>
</div>

<div class="field">
<label>E-mail *</label>
<input id="checkoutEmail" type="email" required>
</div>

<div class="field">
<label>WhatsApp *</label>
<input id="checkoutWhatsapp">
</div>

<div class="field">
<label>Empresa / Negócio</label>
<input id="checkoutDocument">
</div>

<div class="field full">
<label>Observações / Requisitos</label>
<input id="checkoutObservation">
</div>

</div>

<div class="modal-actions">
<button class="btn btn-primary" onclick="createOrder()">Enviar Solicitação</button>
</div>

</div>
</div>
</div>

<!-- ================= CONTACT ================= -->

<div class="modal-overlay" id="contactModal">
<div class="modal" style="max-width:600px">

<div class="modal-head">
<h2>Solicitar projeto</h2>
<button class="close" onclick="closeModal('contactModal')">×</button>
</div>

<div class="modal-body">

<div class="form-grid">

<div class="field">
<label>Nome</label>
<input id="contactName">
</div>

<div class="field">
<label>WhatsApp</label>
<input id="contactWhatsapp">
</div>

<div class="field">
<label>E-mail</label>
<input id="contactEmail">
</div>

<div class="field">
<label>Tipo de projeto</label>
<select id="contactType">
<option>Site institucional</option>
<option>Loja virtual</option>
<option>Landing Page</option>
<option>Sistema Web</option>
<option>Projeto personalizado</option>
</select>
</div>

<div class="field full">
<label>Conte sobre seu projeto</label>
<textarea id="contactMessage"></textarea>
</div>

</div>

<div class="modal-actions">
<button id="sendWhatsappBtn" class="btn btn-primary whatsapp-send-btn" onclick="sendContact()" aria-label="Enviar solicitação pelo WhatsApp">
    <span class="status-mark" id="whatsappStatusMark" data-status="idle" aria-hidden="true">
        <svg viewBox="0 0 24 24" class="status-mark-svg">
            <circle class="status-track" cx="12" cy="12" r="9"></circle>
            <circle class="status-progress" cx="12" cy="12" r="9"></circle>
            <path class="status-check" d="M7.5 12.5l3 3 6-7"></path>
        </svg>
    </span>
    <span id="sendWhatsappLabel">Enviar pelo WhatsApp</span>
</button>
</div>

</div>
</div>
</div>

<!-- ================= ADMIN ================= -->

<div class="admin-overlay" id="adminOverlay">

<div id="adminLogin" class="admin-login">

<div class="login-box">

<div class="logo">Dev<span>Sites</span></div>

<h2>Painel Administrativo</h2>

<p>
Acesse o painel para gerenciar produtos, pedidos, clientes e conteúdo da plataforma.
</p>

<div class="field">
<label>E-mail</label>
<input id="adminEmail" value="admin@devsites.com">
</div>

<div class="field">
<label>Senha</label>
<input id="adminPassword" type="password" value="junior17JM">
</div>

<button class="btn btn-primary" style="width:100%" onclick="adminLogin()">
Entrar no painel
</button>

<button class="btn btn-outline" style="width:100%;margin-top:10px" onclick="closeAdmin()">
Voltar para loja
</button>

</div>

</div>

<div id="adminPanel" style="display:none;height:100%">

<div class="admin-layout">

<aside class="admin-sidebar">

<div class="admin-brand">Dev<span>Sites</span></div>

<div class="admin-menu">

<button class="active" onclick="showAdminSection('dashboard',this)">📊 Dashboard</button>
<button onclick="showAdminSection('products',this)">🖥️ Produtos</button>
<button onclick="showAdminSection('categories',this)">▦ Categorias</button>
<button onclick="showAdminSection('orders',this)">📦 Solicitações</button>
<button onclick="showAdminSection('clients',this)">👥 Clientes</button>
<button onclick="showAdminSection('banners',this)">🖼️ Banners</button>
<button onclick="showAdminSection('testimonials',this)">💬 Depoimentos</button>
<button onclick="showAdminSection('plans',this)">💎 Planos</button>
<button onclick="showAdminSection('settings',this)">⚙️ Configurações</button>

</div>

</aside>

<main class="admin-main">

<div class="admin-topbar">
<strong>Painel Administrativo</strong>

<div style="display:flex;gap:8px">
<button class="btn btn-outline" onclick="closeAdmin()">← Loja</button>
<button class="btn btn-danger" onclick="adminLogout()">Sair</button>
</div>
</div>

<div class="admin-content">

<!-- DASHBOARD -->

<section class="admin-section active" id="admin-dashboard">

<div class="admin-title">
<div>
<h2>Dashboard</h2>
<p style="color:var(--muted);font-size:12px">Visão geral da plataforma.</p>
</div>
</div>

<div class="dashboard-cards">

<div class="dashboard-card">
<span>Total de sites</span>
<strong id="dashProducts">0</strong>
</div>

<div class="dashboard-card">
<span>Solicitações</span>
<strong id="dashOrders">0</strong>
</div>

<div class="dashboard-card">
<span>Clientes</span>
<strong id="dashClients">0</strong>
</div>

</div>

<div style="border:1px solid var(--border);border-radius:15px;padding:20px">
<h3 style="margin-bottom:15px">Últimas solicitações</h3>
<div id="dashboardOrders"></div>
</div>

</section>

<!-- PRODUCTS -->

<section class="admin-section" id="admin-products">

<div class="admin-title">
<div>
<h2>Produtos / Sites</h2>
<p style="color:var(--muted);font-size:12px">Gerencie os sites disponíveis no catálogo.</p>
</div>

<button class="btn btn-primary" onclick="openProductEditor()">+ Adicionar site</button>
</div>

<div id="adminProductsTable"></div>

</section>

<!-- CATEGORIES -->

<section class="admin-section" id="admin-categories">

<div class="admin-title">
<h2>Categorias</h2>
<button class="btn btn-primary" onclick="addCategory()">+ Nova categoria</button>
</div>

<div id="adminCategories"></div>

</section>

<!-- ORDERS -->

<section class="admin-section" id="admin-orders">

<div class="admin-title">
<h2>Solicitações de Projetos</h2>
</div>

<div id="adminOrdersTable"></div>

</section>

<!-- CLIENTS -->

<section class="admin-section" id="admin-clients">

<div class="admin-title">
<h2>Clientes</h2>
</div>

<div id="adminClientsTable"></div>

</section>

<!-- BANNERS -->

<section class="admin-section" id="admin-banners">

<div class="admin-title">
<h2>Banners</h2>
<button class="btn btn-primary" onclick="addBanner()">+ Novo banner</button>
</div>

<div id="adminBanners"></div>

</section>

<!-- TESTIMONIALS -->

<section class="admin-section" id="admin-testimonials">

<div class="admin-title">
<h2>Depoimentos</h2>
<button class="btn btn-primary" onclick="addTestimonial()">+ Novo depoimento</button>
</div>

<div id="adminTestimonials"></div>

</section>

<!-- PLANS -->

<section class="admin-section" id="admin-plans">

<div class="admin-title">
<h2>Planos</h2>
</div>

<div id="adminPlans"></div>

</section>

<!-- SETTINGS -->

<section class="admin-section" id="admin-settings">

<div class="admin-title">
<h2>Configurações</h2>
</div>

<div style="max-width:700px">

<div class="field">
<label>Nome da empresa</label>
<input id="settingCompany">
</div>

<div class="field">
<label>Slogan</label>
<input id="settingSlogan">
</div>

<div class="field">
<label>WhatsApp</label>
<input id="settingWhatsapp">
</div>

<div class="field">
<label>Instagram</label>
<input id="settingInstagram">
</div>

<button class="btn btn-primary" onclick="saveSettings()">Salvar configurações</button>

</div>

</section>

</div>
</main>

</div>

</div>

</div>

<!-- PRODUCT EDITOR -->

<div class="modal-overlay" id="productEditorModal">
<div class="modal" style="max-width:900px">

<div class="modal-head">
<h2 id="productEditorTitle">Adicionar site</h2>
<button class="close" onclick="closeModal('productEditorModal')">×</button>
</div>

<div class="modal-body">

<input type="hidden" id="editProductId">

<div class="form-grid">

<div class="field">
<label>Nome do site *</label>
<input id="prodName">
</div>

<div class="field">
<label>Categoria *</label>
<select id="prodCategory"></select>
</div>

<div class="field full">
<label>Descrição</label>
<textarea id="prodDescription"></textarea>
</div>

<div class="field full">
<label>Imagem principal — URL</label>
<input id="prodImage" placeholder="https://...">
</div>

<div class="field">
<label>Link da demonstração</label>
<input id="prodDemo" placeholder="https://...">
</div>

<div class="field full">
<label>Galeria — URLs separadas por vírgula</label>
<textarea id="prodGallery" placeholder="https://imagem1.jpg, https://imagem2.jpg"></textarea>
</div>

<div class="field full">
<label>Tecnologias — separadas por vírgula</label>
<input id="prodTechs" placeholder="HTML5, CSS3, JavaScript">
</div>

<div class="field full">
<label>Recursos — separados por vírgula</label>
<textarea id="prodFeatures" placeholder="Responsivo, WhatsApp, SEO, Formulário"></textarea>
</div>

<div class="field">
<label>☑ Destaque</label>
<select id="prodFeatured">
<option value="false">Não</option>
<option value="true">Sim</option>
</select>
</div>

<div class="field">
<label>☑ Mais vendido</label>
<select id="prodBest">
<option value="false">Não</option>
<option value="true">Sim</option>
</select>
</div>

<div class="field">
<label>Status</label>
<select id="prodStatus">
<option value="ativo">Ativo</option>
<option value="inativo">Inativo</option>
</select>
</div>

</div>

<div class="modal-actions">
<button class="btn btn-outline" onclick="closeModal('productEditorModal')">Cancelar</button>
<button class="btn btn-primary" onclick="saveProduct()">Salvar site</button>
</div>

</div>
</div>
</div>

<div id="toastContainer" class="toast-container"></div>

<script>
/* =========================================================
   DEVSITES - SEM VALORES
   SISTEMA FRONTEND + LOCALSTORAGE + REAL-TIME SYNC
========================================================= */

const STORAGE_KEY = "devsites_database_novals_v1";
const syncChannel = new BroadcastChannel("devsites_realtime_sync_nv");

const defaultProducts = [
{
id:1,
name:"TechNova",
category:"Empresas",
description:"Site tecnológico premium para empresas de tecnologia, startups e negócios digitais.",
image:"https://images.unsplash.com/photo-1558655146-d09347e92766?auto=format&fit=crop&w=1000&q=85",
gallery:[
"https://images.unsplash.com/photo-1558655146-d09347e92766?auto=format&fit=crop&w=1000&q=85",
"https://images.unsplash.com/photo-1460925895917-afdab827c52f?auto=format&fit=crop&w=1000&q=85"
],
demo:"#",
techs:["HTML5","CSS3","JavaScript"],
features:["Design responsivo","SEO básico","Formulário de contato","Integração WhatsApp"],
featured:true,
best:true,
status:"ativo"
},
{
id:2,
name:"House Pizzaria",
category:"Pizzarias",
description:"Experiência digital premium para pizzarias e restaurantes.",
image:"https://images.unsplash.com/photo-1579751626657-72bc17010498?auto=format&fit=crop&w=1000&q=85",
gallery:[
"https://images.unsplash.com/photo-1579751626657-72bc17010498?auto=format&fit=crop&w=1000&q=85",
"https://images.unsplash.com/photo-1513104890138-7c749659a591?auto=format&fit=crop&w=1000&q=85"
],
demo:"#",
techs:["HTML5","CSS3","JavaScript"],
features:["Cardápio digital","Carrinho","WhatsApp","Responsivo"],
featured:true,
best:true,
status:"ativo"
},
{
id:3,
name:"Urban Barber",
category:"Barbearias",
description:"Site elegante para barbearias modernas com apresentação de serviços.",
image:"https://images.unsplash.com/photo-1503951914875-452162b0f3f1?auto=format&fit=crop&w=1000&q=85",
gallery:[
"https://images.unsplash.com/photo-1503951914875-452162b0f3f1?auto=format&fit=crop&w=1000&q=85",
"https://images.unsplash.com/photo-1621605815971-fbc98d665033?auto=format&fit=crop&w=1000&q=85"
],
demo:"#",
techs:["HTML5","CSS3","JavaScript"],
features:["Serviços","Agendamento","WhatsApp","Galeria"],
featured:false,
best:false,
status:"ativo"
},
{
id:4,
name:"Prime Imóveis",
category:"Imobiliárias",
description:"Portal imobiliário moderno para apresentação de imóveis e captação de clientes.",
image:"https://images.unsplash.com/photo-1560518883-ce09059eeffa?auto=format&fit=crop&w=1000&q=85",
gallery:[
"https://images.unsplash.com/photo-1560518883-ce09059eeffa?auto=format&fit=crop&w=1000&q=85",
"https://images.unsplash.com/photo-1600607687920-4e2a09cf159d?auto=format&fit=crop&w=1000&q=85"
],
demo:"#",
techs:["HTML5","CSS3","JavaScript"],
features:["Catálogo de imóveis","Filtros","Formulário","WhatsApp"],
featured:false,
best:false,
status:"ativo"
},
{
id:5,
name:"Moda Store",
category:"Lojas",
description:"Loja virtual moderna para marcas de moda e comércio online.",
image:"https://images.unsplash.com/photo-1441986300917-64674bd600d8?auto=format&fit=crop&w=1000&q=85",
gallery:[
"https://images.unsplash.com/photo-1441986300917-64674bd600d8?auto=format&fit=crop&w=1000&q=85",
"https://images.unsplash.com/photo-1555529669-e69e7aa0ba9a?auto=format&fit=crop&w=1000&q=85"
],
demo:"#",
techs:["HTML5","CSS3","JavaScript"],
features:["Produtos","Carrinho","Categorias","Checkout preparado"],
featured:true,
best:false,
status:"ativo"
},
{
id:6,
name:"Clinic Pro",
category:"Clínicas",
description:"Presença digital profissional para clínicas e consultórios.",
image:"https://images.unsplash.com/photo-1519494026892-80bbd2d6fd0d?auto=format&fit=crop&w=1000&q=85",
gallery:[
"https://images.unsplash.com/photo-1519494026892-80bbd2d6fd0d?auto=format&fit=crop&w=1000&q=85",
"https://images.unsplash.com/photo-1576091160399-112ba8d25d1d?auto=format&fit=crop&w=1000&q=85"
],
demo:"#",
techs:["HTML5","CSS3","JavaScript"],
features:["Serviços","Equipe","Agendamento","Contato"],
featured:false,
best:false,
status:"ativo"
}
];

const defaultCategories = [
"Todos", "Empresas", "Lojas", "Restaurantes", "Pizzarias", "Barbearias", "Clínicas", "Imobiliárias", "Portfólios", "Advocacia", "Academias", "Hotéis", "Eventos", "Landing Pages", "Sistemas"
];

let db = loadDB();
let currentCategory = "Todos";
let currentProduct = null;
let cart = [];

function loadDB(){
    const saved = localStorage.getItem(STORAGE_KEY);
    if(saved){
        try{ return JSON.parse(saved); }catch(e){}
    }
    const initial = {
        products:defaultProducts,
        categories:defaultCategories,
        orders:[],
        clients:[],
        banners:[],
        testimonials:[],
        settings:{
            company:"DevSites",
            slogan:"Seu negócio merece um site profissional.",
            whatsapp:"5547992170175",
            instagram:""
        }
    };
    localStorage.setItem(STORAGE_KEY,JSON.stringify(initial));
    return initial;
}

function saveDB(){
    localStorage.setItem(STORAGE_KEY,JSON.stringify(db));
    syncChannel.postMessage({ type: "DB_CHANGED" });
}

syncChannel.onmessage = (event) => {
    if(event.data && event.data.type === "DB_CHANGED"){
        db = loadDB();
        renderFilters();
        renderProducts();
        if(document.getElementById("adminOverlay").classList.contains("show")){
            renderAdmin();
        }
    }
};

function escapeHTML(value){
    return String(value ?? "")
        .replaceAll("&","&amp;").replaceAll("<","&lt;").replaceAll(">","&gt;")
        .replaceAll('"',"&quot;").replaceAll("'","&#039;");
}

function toast(message){
    const box=document.getElementById("toastContainer");
    const item=document.createElement("div");
    item.className="toast";
    item.textContent=message;
    box.appendChild(item);
    setTimeout(()=>{
        item.style.opacity="0";
        item.style.transform="translateX(20px)";
        setTimeout(()=>item.remove(),300);
    },3000);
}

function closeModal(id){ document.getElementById(id).classList.remove("show"); }
function openModal(id){ document.getElementById(id).classList.add("show"); }
function scrollToSites(){ document.getElementById("sites").scrollIntoView({behavior:"smooth"}); }

window.addEventListener("scroll",()=>{
    document.getElementById("header").classList.toggle("scrolled",window.scrollY>30);
});

function toggleMobileMenu(){
    const nav=document.querySelector(".nav-links");
    if(nav.style.display==="flex"){
        nav.style.display="";
    }else{
        nav.style.display="flex";
        nav.style.position="absolute";
        nav.style.top="68px";
        nav.style.left="0";
        nav.style.right="0";
        nav.style.padding="20px";
        nav.style.flexDirection="column";
        nav.style.background="#07101b";
        nav.style.borderBottom="1px solid var(--border)";
    }
}

function renderFilters(){
    const container=document.getElementById("filters");
    container.innerHTML=db.categories.map(category=>`
        <button class="filter ${category===currentCategory?"active":""}" onclick="filterProducts('${escapeHTML(category)}')">
            ${escapeHTML(category)}
        </button>
    `).join("");
}

function filterProducts(category){
    currentCategory=category;
    renderFilters();
    renderProducts();
    document.getElementById("sites").scrollIntoView({behavior:"smooth",block:"start"});
}

function renderProducts(){
    const container=document.getElementById("productsGrid");
    let products=db.products.filter(p=>p.status==="ativo");

    if(currentCategory!=="Todos"){
        products=products.filter(p=>p.category===currentCategory);
    }

    if(!products.length){
        container.innerHTML=`<div class="admin-empty" style="grid-column:1/-1">Nenhum site encontrado nesta categoria.</div>`;
        return;
    }

    container.innerHTML=products.map(product=>{
        return `
        <div class="flip-card" data-card-id="${product.id}" tabindex="0" role="button" aria-label="${escapeHTML(product.name)}">
            <span class="flip-card__shadow" aria-hidden="true"></span>
            <div class="flip-card__rotor">
                <div class="flip-card__face flip-card__face--front">
                    <div class="product-image">
                        <img src="${escapeHTML(product.image)}" alt="${escapeHTML(product.name)}" loading="lazy" onerror="this.src='https://images.unsplash.com/photo-1558655146-d09347e92766?auto=format&fit=crop&w=1000&q=80'">
                        ${product.best ? `<div class="product-badge">★ MAIS VENDIDO</div>` : product.featured ? `<div class="product-badge">DESTAQUE</div>` : ""}
                    </div>
                    <div class="product-info">
                        <div>
                            <div class="product-category">${escapeHTML(product.category)}</div>
                            <h3>${escapeHTML(product.name)}</h3>
                            <p>${escapeHTML(product.description)}</p>
                        </div>
                        <div>
                            <div class="techs">
                                ${(product.techs||[]).slice(0,4).map(t=>`<span>${escapeHTML(t)}</span>`).join("")}
                            </div>
                            <div class="flip-hint">🔄 Clique ou arraste para ver recursos</div>
                        </div>
                    </div>
                    <span class="flip-card__glare" aria-hidden="true"></span>
                </div>
                <div class="flip-card__face flip-card__face--back">
                    <div>
                        <div class="product-category">${escapeHTML(product.category)}</div>
                        <h3 style="margin: 8px 0;">Recursos Inclusos</h3>
                        <ul class="feature-list">
                            ${(product.features||[]).map(f=>`<li>${escapeHTML(f)}</li>`).join("")}
                        </ul>
                    </div>
                    <div>
                        <div class="card-actions" onclick="event.stopPropagation()">
                            <button class="btn btn-outline" onclick="openProduct(${product.id})">Detalhes</button>
                            <button class="btn btn-primary" onclick="addToCart(${product.id})">Solicitar</button>
                        </div>
                        <div class="flip-hint" style="margin-top:12px;">🔄 Clique para virar a frente</div>
                    </div>
                    <span class="flip-card__glare" aria-hidden="true"></span>
                </div>
            </div>
        </div>
        `;
    }).join("");

    initFlipCards();
}

function openProduct(id){
    const product=db.products.find(p=>p.id===Number(id));
    if(!product) return;
    currentProduct=product;

    document.getElementById("detailTitle").textContent=product.name;
    document.getElementById("detailName").textContent=product.name;
    document.getElementById("detailCategory").textContent=product.category;
    document.getElementById("detailDescription").textContent=product.description;
    document.getElementById("detailMainImage").src=product.image;

    document.getElementById("detailTechs").innerHTML=(product.techs||[]).map(t=>`<span>${escapeHTML(t)}</span>`).join("");
    document.getElementById("detailFeatures").innerHTML=(product.features||[]).map(f=>`<li>${escapeHTML(f)}</li>`).join("");

    const gallery=document.getElementById("detailGallery");
    const images=[product.image,...(product.gallery||[])];
    gallery.innerHTML=images.map((img,index)=>`
        <img src="${escapeHTML(img)}" class="${index===0?"active":""}" onclick="changeDetailImage(this,'${escapeHTML(img)}')" alt="">
    `).join("");

    openModal("productModal");
}

function changeDetailImage(element,image){
    document.getElementById("detailMainImage").src=image;
    document.querySelectorAll("#detailGallery img").forEach(img=>img.classList.remove("active"));
    element.classList.add("active");
}

function requestCurrentProduct(){
    if(!currentProduct) return;
    addToCart(currentProduct.id);
    closeModal("productModal");
    openCart();
}

function requestCustomization(){
    closeModal("productModal");
    openContact(currentProduct ? currentProduct.name : "");
}

function addToCart(id){
    const product=db.products.find(p=>p.id===Number(id));
    if(!product) return;
    const existing=cart.find(item=>item.id===product.id);
    if(existing){ existing.quantity++; } else { cart.push({ id:product.id, quantity:1 }); }
    updateCartCount();
    toast(product.name+" foi adicionado aos projetos solicitados.");
}

function removeCartItem(id){
    cart=cart.filter(item=>item.id!==Number(id));
    updateCartCount();
    renderCart();
}

function changeQuantity(id,change){
    const item=cart.find(i=>i.id===Number(id));
    if(!item) return;
    item.quantity+=change;
    if(item.quantity<=0){ removeCartItem(id); return; }
    renderCart();
}

function updateCartCount(){
    const count=cart.reduce((total,item)=>total+item.quantity,0);
    document.getElementById("cartCount").textContent=count;
}

function renderCart(){
    const container=document.getElementById("cartItems");
    if(!cart.length){
        container.innerHTML=`<div class="admin-empty">Nenhum projeto selecionado.</div>`;
        return;
    }

    container.innerHTML=cart.map(item=>{
        const product=db.products.find(p=>p.id===item.id);
        if(!product) return "";
        return `
        <div class="cart-item">
            <img src="${escapeHTML(product.image)}" alt="">
            <div>
                <h4>${escapeHTML(product.name)}</h4>
                <small>Projeto para orçamento</small>
                <div style="display:flex;gap:6px;margin-top:7px">
                    <button class="small-btn" onclick="changeQuantity(${product.id},-1)">−</button>
                    <span style="padding:6px">${item.quantity}</span>
                    <button class="small-btn" onclick="changeQuantity(${product.id},1)">+</button>
                </div>
            </div>
            <button class="small-btn" onclick="removeCartItem(${product.id})">×</button>
        </div>
        `;
    }).join("");
}

function openCart(){ renderCart(); openModal("cartModal"); }

function openCheckout(){
    if(!cart.length){ toast("Selecione pelo menos um site."); return; }
    closeModal("cartModal");
    openModal("checkoutModal");
}

function createOrder(){
    const name=document.getElementById("checkoutName").value.trim();
    const email=document.getElementById("checkoutEmail").value.trim();
    const whatsapp=document.getElementById("checkoutWhatsapp").value.trim();
    if(!name || !email || !whatsapp){ toast("Preencha nome, e-mail e WhatsApp."); return; }

    const order={
        id:Date.now(),
        client:name, email, whatsapp,
        document:document.getElementById("checkoutDocument").value,
        observation:document.getElementById("checkoutObservation").value,
        products:cart.map(item=>{
            const product=db.products.find(p=>p.id===item.id);
            return { id:product.id, name:product.name, quantity:item.quantity };
        }),
        date:new Date().toLocaleString("pt-BR"),
        status:"Pendente"
    };

    db.orders.unshift(order);
    const existingClient=db.clients.find(c=>c.email===email);
    if(!existingClient){
        db.clients.unshift({ id:Date.now()+1, name, email, whatsapp, orders:1 });
    }else{
        existingClient.orders++;
    }
    saveDB();
    cart=[];
    updateCartCount();
    closeModal("checkoutModal");
    toast("Solicitação #"+order.id+" enviada com sucesso.");
    document.getElementById("checkoutName").value="";
    document.getElementById("checkoutEmail").value="";
    document.getElementById("checkoutWhatsapp").value="";
}

function openContact(type=""){
    openModal("contactModal");
    if(type){ document.getElementById("contactMessage").value="Tenho interesse no projeto: "+type; }
}

function sendContact(){
    const name=document.getElementById("contactName").value.trim();
    const whatsapp=document.getElementById("contactWhatsapp").value.trim();
    const message=document.getElementById("contactMessage").value.trim();
    if(!name || !whatsapp){ toast("Preencha nome e WhatsApp."); return; }

    const btn=document.getElementById("sendWhatsappBtn");
    const mark=document.getElementById("whatsappStatusMark");
    const label=document.getElementById("sendWhatsappLabel");
    const progress=document.querySelector("#whatsappStatusMark .status-progress");
    const phone=db.settings.whatsapp || "5547992170175";
    const text="Olá! Sou "+name+". WhatsApp: "+whatsapp+". "+message;

    if(btn.dataset.sending === "true") return;
    btn.dataset.sending="true";
    btn.disabled=true;
    mark.dataset.status="running";
    label.textContent="Abrindo WhatsApp...";

    /* Equivalente visual ao StatusMark: running + progresso de 62%. */
    requestAnimationFrame(()=>{
        progress.style.strokeDashoffset = String(56.55 * (1 - 0.62));
    });

    const whatsappUrl="https://wa.me/"+phone+"?text="+encodeURIComponent(text);
    window.open(whatsappUrl,"_blank");

    setTimeout(()=>{
        mark.dataset.status="done";
        label.textContent="WhatsApp aberto";
        btn.dataset.sending="false";
        btn.disabled=false;
        setTimeout(()=>{
            mark.dataset.status="idle";
            progress.style.strokeDashoffset="56.55";
            label.textContent="Enviar pelo WhatsApp";
        },1400);
    },700);
}

document.querySelectorAll(".faq-question").forEach(q=>{
    q.addEventListener("click",()=>{ q.parentElement.classList.toggle("open"); });
});

const observer=new IntersectionObserver(entries=>{
    entries.forEach(entry=>{
        if(!entry.isIntersecting) return;
        const el=entry.target;
        const target=Number(el.dataset.count);
        let current=0;
        const step=Math.max(1,Math.ceil(target/50));
        const interval=setInterval(()=>{
            current+=step;
            if(current>=target){ current=target; clearInterval(interval); }
            el.textContent="+"+current;
        },25);
        observer.unobserve(el);
    });
},{threshold:.5});

document.querySelectorAll("[data-count]").forEach(el=>observer.observe(el));

function openAdmin(){
    document.getElementById("adminOverlay").classList.add("show");
    document.body.classList.add("locked");
    document.getElementById("adminLogin").style.display="grid";
    document.getElementById("adminPanel").style.display="none";
}

function closeAdmin(){
    document.getElementById("adminOverlay").classList.remove("show");
    document.body.classList.remove("locked");
}

function adminLogin(){
    const email=document.getElementById("adminEmail").value.trim();
    const password=document.getElementById("adminPassword").value;
    if(email==="admin@devsites.com" && password==="junior17JM"){
        sessionStorage.setItem("devsites_admin","true");
        document.getElementById("adminLogin").style.display="none";
        document.getElementById("adminPanel").style.display="block";
        renderAdmin();
        toast("Login realizado com sucesso.");
    }else{
        toast("E-mail ou senha incorretos.");
    }
}

function adminLogout(){
    sessionStorage.removeItem("devsites_admin");
    document.getElementById("adminPanel").style.display="none";
    document.getElementById("adminLogin").style.display="grid";
}

function showAdminSection(section,button){
    document.querySelectorAll(".admin-section").forEach(s=>s.classList.remove("active"));
    const target=document.getElementById("admin-"+section);
    if(target){ target.classList.add("active"); }
    document.querySelectorAll(".admin-menu button").forEach(b=>b.classList.remove("active"));
    if(button){ button.classList.add("active"); }
    renderAdmin();
}

function renderDashboard(){
    document.getElementById("dashProducts").textContent=db.products.length;
    document.getElementById("dashOrders").textContent=db.orders.length;
    document.getElementById("dashClients").textContent=db.clients.length;
    const box=document.getElementById("dashboardOrders");
    if(!db.orders.length){
        box.innerHTML=`<div class="admin-empty">Nenhuma solicitação registrada.</div>`;
        return;
    }
    box.innerHTML=`
        <table class="admin-table">
            <thead>
                <tr>
                    <th>Solicitação</th>
                    <th>Cliente</th>
                    <th>Status</th>
                </tr>
            </thead>
            <tbody>
                ${db.orders.slice(0,6).map(order=>`
                    <tr>
                        <td>#${order.id}</td>
                        <td>${escapeHTML(order.client)}</td>
                        <td><span class="status">${escapeHTML(order.status)}</span></td>
                    </tr>
                `).join("")}
            </tbody>
        </table>
    `;
}

function renderAdminProducts(){
    const container=document.getElementById("adminProductsTable");
    container.innerHTML=`
    <table class="admin-table">
        <thead>
            <tr>
                <th>Produto</th>
                <th>Categoria</th>
                <th>Status</th>
                <th>Ações</th>
            </tr>
        </thead>
        <tbody>
        ${db.products.map(product=>`
            <tr>
                <td>
                    <div class="table-product">
                        <img src="${escapeHTML(product.image)}">
                        <span>${escapeHTML(product.name)}</span>
                    </div>
                </td>
                <td>${escapeHTML(product.category)}</td>
                <td><span class="status ${product.status}">${product.status}</span></td>
                <td>
                    <div class="admin-actions">
                        <button class="small-btn" onclick="openProductEditor(${product.id})">Editar</button>
                        <button class="small-btn" onclick="duplicateProduct(${product.id})">Duplicar</button>
                        <button class="small-btn" onclick="toggleProduct(${product.id})">${product.status==="ativo"?"Desativar":"Ativar"}</button>
                        <button class="small-btn" onclick="deleteProduct(${product.id})">Excluir</button>
                    </div>
                </td>
            </tr>
        `).join("")}
        </tbody>
    </table>
    `;
}

function openProductEditor(id=null){
    document.getElementById("prodCategory").innerHTML=db.categories.filter(c=>c!=="Todos").map(c=>`<option>${escapeHTML(c)}</option>`).join("");
    document.getElementById("editProductId").value="";
    document.getElementById("prodName").value="";
    document.getElementById("prodDescription").value="";
    document.getElementById("prodImage").value="";
    document.getElementById("prodDemo").value="";
    document.getElementById("prodGallery").value="";
    document.getElementById("prodTechs").value="";
    document.getElementById("prodFeatures").value="";
    document.getElementById("prodFeatured").value="false";
    document.getElementById("prodBest").value="false";
    document.getElementById("prodStatus").value="ativo";
    document.getElementById("productEditorTitle").textContent=id ? "Editar site" : "Adicionar site";

    if(id){
        const product=db.products.find(p=>p.id===Number(id));
        if(!product) return;
        document.getElementById("editProductId").value=product.id;
        document.getElementById("prodName").value=product.name;
        document.getElementById("prodCategory").value=product.category;
        document.getElementById("prodDescription").value=product.description;
        document.getElementById("prodImage").value=product.image;
        document.getElementById("prodDemo").value=product.demo || "";
        document.getElementById("prodGallery").value=(product.gallery||[]).join(", ");
        document.getElementById("prodTechs").value=(product.techs||[]).join(", ");
        document.getElementById("prodFeatures").value=(product.features||[]).join(", ");
        document.getElementById("prodFeatured").value=String(!!product.featured);
        document.getElementById("prodBest").value=String(!!product.best);
        document.getElementById("prodStatus").value=product.status;
    }
    openModal("productEditorModal");
}

function saveProduct(){
    const id=document.getElementById("editProductId").value;
    const name=document.getElementById("prodName").value.trim();
    if(!name){ toast("Informe o nome do site."); return; }
    const data={
        name,
        category:document.getElementById("prodCategory").value,
        description:document.getElementById("prodDescription").value.trim(),
        image:document.getElementById("prodImage").value.trim() || "https://images.unsplash.com/photo-1558655146-d09347e92766?auto=format&fit=crop&w=1000&q=80",
        demo:document.getElementById("prodDemo").value.trim(),
        gallery:document.getElementById("prodGallery").value.split(",").map(x=>x.trim()).filter(Boolean),
        techs:document.getElementById("prodTechs").value.split(",").map(x=>x.trim()).filter(Boolean),
        features:document.getElementById("prodFeatures").value.split(",").map(x=>x.trim()).filter(Boolean),
        featured:document.getElementById("prodFeatured").value==="true",
        best:document.getElementById("prodBest").value==="true",
        status:document.getElementById("prodStatus").value
    };

    if(id){
        const index=db.products.findIndex(p=>p.id===Number(id));
        if(index!==-1){ db.products[index]={ ...db.products[index], ...data }; }
        toast("Site atualizado.");
    }else{
        db.products.unshift({ id:Date.now(), ...data });
        toast("Site adicionado.");
    }
    saveDB();
    closeModal("productEditorModal");
    renderProducts();
    renderAdmin();
}

function deleteProduct(id){
    if(!confirm("Excluir este site?")) return;
    db.products=db.products.filter(p=>p.id!==Number(id));
    saveDB();
    renderProducts();
    renderAdminProducts();
    toast("Site excluído.");
}

function duplicateProduct(id){
    const product=db.products.find(p=>p.id===Number(id));
    if(!product) return;
    db.products.unshift({
        ...JSON.parse(JSON.stringify(product)),
        id:Date.now(),
        name:product.name+" — Cópia"
    });
    saveDB();
    renderProducts();
    renderAdminProducts();
    toast("Produto duplicado.");
}

function toggleProduct(id){
    const product=db.products.find(p=>p.id===Number(id));
    if(!product) return;
    product.status=product.status==="ativo" ? "inativo" : "ativo";
    saveDB();
    renderProducts();
    renderAdminProducts();
}

function addCategory(){
    const name=prompt("Nome da nova categoria:");
    if(!name) return;
    if(db.categories.includes(name)){ toast("Essa categoria já existe."); return; }
    db.categories.push(name);
    saveDB();
    renderFilters();
    renderAdminCategories();
    toast("Categoria adicionada.");
}

function deleteCategory(category){
    if(category==="Todos") return;
    if(!confirm("Excluir categoria?")) return;
    db.categories=db.categories.filter(c=>c!==category);
    saveDB();
    renderFilters();
    renderAdminCategories();
    toast("Categoria excluída.");
}

function renderAdminCategories(){
    const box=document.getElementById("adminCategories");
    box.innerHTML=`
    <table class="admin-table">
        <thead>
            <tr>
                <th>Categoria</th>
                <th>Produtos</th>
                <th>Ações</th>
            </tr>
        </thead>
        <tbody>
        ${db.categories.map(category=>{
            const count=db.products.filter(p=>p.category===category).length;
            return `
            <tr>
                <td>${escapeHTML(category)}</td>
                <td>${count}</td>
                <td>
                    ${category!=="Todos" ? `<button class="small-btn" onclick="deleteCategory('${escapeHTML(category)}')">Excluir</button>` : "Sistema"}
                </td>
            </tr>
            `;
        }).join("")}
        </tbody>
    </table>
    `;
}

function renderAdminOrders(){
    const box=document.getElementById("adminOrdersTable");
    if(!db.orders.length){
        box.innerHTML=`<div class="admin-empty">Nenhuma solicitação cadastrada.</div>`;
        return;
    }
    box.innerHTML=`
    <table class="admin-table">
    <thead>
    <tr>
        <th>Solicitação</th>
        <th>Cliente</th>
        <th>Projeto(s)</th>
        <th>Status</th>
        <th>Ação</th>
    </tr>
    </thead>
    <tbody>
    ${db.orders.map(order=>`
        <tr>
            <td>#${order.id}</td>
            <td>${escapeHTML(order.client)}<br><small style="color:#6f8195">${escapeHTML(order.email)}</small></td>
            <td>${order.products.map(p=>`${escapeHTML(p.name)} (${p.quantity})`).join("<br>")}</td>
            <td>
                <select onchange="updateOrderStatus(${order.id},this.value)" style="background:#07101b;color:white;border:1px solid var(--border);padding:7px;border-radius:7px">
                    ${["Pendente","Em análise","Em desenvolvimento","Concluído","Cancelado"].map(status=>`
                        <option ${order.status===status?"selected":""}>${status}</option>
                    `).join("")}
                </select>
            </td>
            <td><button class="small-btn" onclick="deleteOrder(${order.id})">Excluir</button></td>
        </tr>
    `).join("")}
    </tbody>
    </table>
    `;
}

function updateOrderStatus(id,status){
    const order=db.orders.find(o=>o.id===Number(id));
    if(!order) return;
    order.status=status;
    saveDB();
    renderDashboard();
    toast("Status atualizado.");
}

function deleteOrder(id){
    if(!confirm("Excluir solicitação?")) return;
    db.orders=db.orders.filter(o=>o.id!==Number(id));
    saveDB();
    renderAdminOrders();
    renderDashboard();
    toast("Solicitação excluída.");
}

function renderAdminClients(){
    const box=document.getElementById("adminClientsTable");
    if(!db.clients.length){
        box.innerHTML=`<div class="admin-empty">Nenhum cliente cadastrado.</div>`;
        return;
    }
    box.innerHTML=`
    <table class="admin-table">
    <thead>
    <tr>
        <th>Cliente</th>
        <th>E-mail</th>
        <th>WhatsApp</th>
        <th>Solicitações</th>
    </tr>
    </thead>
    <tbody>
    ${db.clients.map(client=>`
        <tr>
            <td>${escapeHTML(client.name)}</td>
            <td>${escapeHTML(client.email)}</td>
            <td>${escapeHTML(client.whatsapp)}</td>
            <td>${client.orders||0}</td>
        </tr>
    `).join("")}
    </tbody>
    </table>
    `;
}

function addBanner(){
    const title=prompt("Título do banner:");
    if(!title) return;
    const image=prompt("URL da imagem do banner:");
    db.banners.push({ id:Date.now(), title, image:image||"", status:"ativo" });
    saveDB();
    renderAdminBanners();
    toast("Banner adicionado.");
}

function deleteBanner(id){
    db.banners=db.banners.filter(b=>b.id!==Number(id));
    saveDB();
    renderAdminBanners();
}

function renderAdminBanners(){
    const box=document.getElementById("adminBanners");
    if(!db.banners.length){
        box.innerHTML=`<div class="admin-empty">Nenhum banner cadastrado.</div>`;
        return;
    }
    box.innerHTML=`
    <table class="admin-table">
    <thead>
    <tr>
        <th>Banner</th>
        <th>Imagem</th>
        <th>Status</th>
        <th>Ação</th>
    </tr>
    </thead>
    <tbody>
    ${db.banners.map(b=>`
        <tr>
            <td>${escapeHTML(b.title)}</td>
            <td>${b.image ? `<img src="${escapeHTML(b.image)}" style="width:100px;height:45px;object-fit:cover;border-radius:7px">` : "-"}</td>
            <td>${b.status}</td>
            <td><button class="small-btn" onclick="deleteBanner(${b.id})">Excluir</button></td>
        </tr>
    `).join("")}
    </tbody>
    </table>
    `;
}

function addTestimonial(){
    const name=prompt("Nome do cliente:");
    if(!name) return;
    const company=prompt("Empresa:");
    const text=prompt("Depoimento:");
    db.testimonials.push({ id:Date.now(), name, company:company||"", text:text||"", stars:5 });
    saveDB();
    renderAdminTestimonials();
    toast("Depoimento adicionado.");
}

function deleteTestimonial(id){
    db.testimonials=db.testimonials.filter(t=>t.id!==Number(id));
    saveDB();
    renderAdminTestimonials();
}

function renderAdminTestimonials(){
    const box=document.getElementById("adminTestimonials");
    if(!db.testimonials.length){
        box.innerHTML=`<div class="admin-empty">Nenhum depoimento cadastrado no painel.</div>`;
        return;
    }
    box.innerHTML=`
    <table class="admin-table">
    <thead>
    <tr>
        <th>Cliente</th>
        <th>Empresa</th>
        <th>Depoimento</th>
        <th>Ação</th>
    </tr>
    </thead>
    <tbody>
    ${db.testimonials.map(t=>`
        <tr>
            <td>${escapeHTML(t.name)}</td>
            <td>${escapeHTML(t.company)}</td>
            <td>${escapeHTML(t.text)}</td>
            <td><button class="small-btn" onclick="deleteTestimonial(${t.id})">Excluir</button></td>
        </tr>
    `).join("")}
    </tbody>
    </table>
    `;
}

function renderAdminPlans(){
    const plans=[["Starter","Sob consulta"],["Profissional","Sob consulta"],["Premium","Sob consulta"],["Custom","Sob consulta"]];
    document.getElementById("adminPlans").innerHTML=`
    <table class="admin-table">
    <thead>
        <tr>
            <th>Plano</th>
            <th>Tipo</th>
            <th>Status</th>
        </tr>
    </thead>
    <tbody>
    ${plans.map(p=>`
        <tr>
            <td>${p[0]}</td>
            <td>${p[1]}</td>
            <td><span class="status ativo">Ativo</span></td>
        </tr>
    `).join("")}
    </tbody>
    </table>
    `;
}

function renderSettings(){
    document.getElementById("settingCompany").value=db.settings.company||"";
    document.getElementById("settingSlogan").value=db.settings.slogan||"";
    document.getElementById("settingWhatsapp").value=db.settings.whatsapp||"";
    document.getElementById("settingInstagram").value=db.settings.instagram||"";
}

function saveSettings(){
    db.settings.company=document.getElementById("settingCompany").value;
    db.settings.slogan=document.getElementById("settingSlogan").value;
    db.settings.whatsapp=document.getElementById("settingWhatsapp").value;
    db.settings.instagram=document.getElementById("settingInstagram").value;
    saveDB();
    toast("Configurações salvas.");
}

function renderAdmin(){
    renderDashboard();
    renderAdminProducts();
    renderAdminCategories();
    renderAdminOrders();
    renderAdminClients();
    renderAdminBanners();
    renderAdminTestimonials();
    renderAdminPlans();
    renderSettings();
}

document.addEventListener("keydown",e=>{
    if(e.key==="Escape"){
        document.querySelectorAll(".modal-overlay.show").forEach(modal=>modal.classList.remove("show"));
    }
});

/* ================= FLIP CARD LOGIC ================= */
function initFlipCards() {
    const cards = document.querySelectorAll('.flip-card');
    cards.forEach(card => {
        const rotor = card.querySelector('.flip-card__rotor');
        const glares = card.querySelectorAll('.flip-card__glare');
        let isFlipped = false;
        let isDragging = false;
        let startX = 0;
        let currentRotation = 0;
        let dragDistance = 0;

        card.addEventListener('pointerdown', (e) => {
            if (e.target.closest('.card-actions')) return;
            isDragging = false;
            startX = e.clientX;
            dragDistance = 0;
            card.setPointerCapture(e.pointerId);
            card.setAttribute('data-dragging', 'true');
        });

        card.addEventListener('pointermove', (e) => {
            const rect = card.getBoundingClientRect();
            const px = Math.min(Math.max((e.clientX - rect.left) / rect.width, 0), 1);
            const py = Math.min(Math.max((e.clientY - rect.top) / rect.height, 0), 1);

            if (!isDragging) {
                const tiltX = (0.5 - py) * 16;
                const tiltY = (px - 0.5) * 16;
                const baseRot = isFlipped ? 180 : 0;
                rotor.style.transform = `perspective(1100px) scale(1.02) rotateX(${tiltX}deg) rotateY(${baseRot + tiltY}deg)`;

                glares.forEach(glare => {
                    glare.style.setProperty('--fc-gx', `${px * 100}%`);
                    glare.style.setProperty('--fc-gy', `${py * 100}%`);
                    glare.style.setProperty('--fc-sheen', '1');
                });
            }

            if (card.hasPointerCapture(e.pointerId)) {
                const diffX = e.clientX - startX;
                if (Math.abs(diffX) > 5) {
                    isDragging = true;
                    dragDistance = diffX;
                    const baseRot = isFlipped ? 180 : 0;
                    currentRotation = baseRot + (diffX / rect.width) * 180;
                    rotor.style.transform = `perspective(1100px) rotateY(${currentRotation}deg)`;
                }
            }
        });

        const releasePointer = (e) => {
            if (card.hasPointerCapture(e.pointerId)) {
                card.releasePointerCapture(e.pointerId);
            }
            card.removeAttribute('data-dragging');

            if (isDragging) {
                if (Math.abs(dragDistance) > 40) {
                    isFlipped = !isFlipped;
                }
            } else if (!e.target.closest('.card-actions')) {
                isFlipped = !isFlipped;
            }

            const targetRot = isFlipped ? 180 : 0;
            rotor.style.transform = `perspective(1100px) scale(1) rotateX(0deg) rotateY(${targetRot}deg)`;

            glares.forEach(glare => {
                glare.style.setProperty('--fc-sheen', '0');
            });

            isDragging = false;
        };

        card.addEventListener('pointerup', releasePointer);
        card.addEventListener('pointercancel', releasePointer);

        card.addEventListener('mouseleave', () => {
            if (!isDragging) {
                const targetRot = isFlipped ? 180 : 0;
                rotor.style.transform = `perspective(1100px) scale(1) rotateX(0deg) rotateY(${targetRot}deg)`;
                glares.forEach(glare => {
                    glare.style.setProperty('--fc-sheen', '0');
                });
            }
        });

        card.addEventListener('keydown', (e) => {
            if (e.key === 'Enter' || e.key === ' ') {
                if (e.target.closest('.card-actions')) return;
                e.preventDefault();
                isFlipped = !isFlipped;
                const targetRot = isFlipped ? 180 : 0;
                rotor.style.transform = `perspective(1100px) rotateY(${targetRot}deg)`;
            }
        });
    });
}

/* ================= FOLDER FLOAT LOGIC ================= */
(function initFolderFloat(){
    const app = document.getElementById('folderFloatApp');
    const itemsBox = document.getElementById('folderItems');
    const trigger = document.getElementById('folderTrigger');
    if(!app || !itemsBox || !trigger) return;

    const feedbackNotes = [
        "Velocidade impressionante!",
        "Design limpo e moderno",
        "Atendimento nota 10",
        "Suporte super atencioso"
    ];

    let isOpen = false;

    itemsBox.innerHTML = feedbackNotes.map((note, i) => {
        const offsets = [
            { x: -120, y: -90, r: -6 },
            { x: 40, y: -110, r: 4 },
            { x: -90, y: -45, r: 2 },
            { x: 70, y: -55, r: -5 }
        ];
        const pos = offsets[i] || { x: 0, y: -50, r: 0 };
        return `
            <button class="folder-float__item" style="--i:${i}; --x:${pos.x}px; --y:${pos.y}px; --r:${pos.r}deg;">
                <span class="folder-float__drift">${escapeHTML(note)}</span>
            </button>
        `;
    }).join('');

    function toggleOpen(state){
        isOpen = state !== undefined ? state : !isOpen;
        if(isOpen){
            app.setAttribute('data-open', '');
        } else {
            app.removeAttribute('data-open');
        }
    }

    trigger.addEventListener('click', () => toggleOpen());
    app.addEventListener('mouseenter', () => toggleOpen(true));
    app.addEventListener('mouseleave', () => toggleOpen(false));
})();

/* ================= DOCK LOGIC ================= */
(function(){
  const panel = document.getElementById('dockPanel');
  if(!panel) return;
  const items = panel.querySelectorAll('.dock-item');
  const baseSize = 48;
  const magnification = 70;
  const distance = 140;

  panel.addEventListener('mousemove', (e) => {
    const mouseX = e.clientX;
    items.forEach(item => {
      const rect = item.getBoundingClientRect();
      const center = rect.left + rect.width / 2;
      const dist = Math.abs(mouseX - center);
      
      if (dist < distance) {
        const factor = 1 - Math.cos((dist / distance) * (Math.PI / 2));
        const targetSize = baseSize + (magnification - baseSize) * (1 - factor);
        item.style.width = `${targetSize}px`;
        item.style.height = `${targetSize}px`;
      } else {
        item.style.width = `${baseSize}px`;
        item.style.height = `${baseSize}px`;
      }
    });
  });

  panel.addEventListener('mouseleave', () => {
    items.forEach(item => {
      item.style.width = `${baseSize}px`;
      item.style.height = `${baseSize}px`;
    });
  });
})();

/* ================= AERO SHARDS - JS/CSS ================= */
(function(){
  const host=document.getElementById('aeroShardsHero');
  if(!host) return;
  const reduced=window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  const count=Math.min(90,Math.max(36,Math.floor(window.innerWidth*1.5/14)));
  const frag=document.createDocumentFragment();
  for(let i=0;i<count;i++){
    const el=document.createElement('span');
    el.className='aero-shard';
    const angle=Math.random()*Math.PI*2;
    const radius=80+Math.random()*55;
    const x=Math.cos(angle)*radius; const y=Math.sin(angle)*radius;
    const scale=.45+Math.random()*1.15;
    const rot=Math.random()*360;
    el.style.width=(20+Math.random()*58)+'px';
    el.style.height=(5+Math.random()*14)+'px';
    el.style.background=`linear-gradient(90deg,rgba(137,106,189,.08),rgba(168,85,247,${.18+Math.random()*.38}),rgba(255,255,255,.12))`;
    el.style.boxShadow='0 0 '+(5+Math.random()*18)+'px rgba(168,85,247,.18)';
    el.style.filter='blur('+Math.random()*1.1+'px)';
    el.dataset.x=x; el.dataset.y=y; el.dataset.r=rot; el.dataset.s=scale;
    el.dataset.depth=.35+Math.random()*.9; el.dataset.speed=.35+Math.random()*.9;
    frag.appendChild(el);
  }
  host.appendChild(frag);
  let raf=0,start=performance.now(),mx=0,my=0;
  host.addEventListener('pointermove',e=>{const r=host.getBoundingClientRect();mx=(e.clientX-r.left)/r.width-.5;my=(e.clientY-r.top)/r.height-.5},{passive:true});
  function frame(now){
    const t=(now-start)/1000;
    host.querySelectorAll('.aero-shard').forEach((el,i)=>{
      const d=+el.dataset.depth, sp=+el.dataset.speed;
      const baseX=+el.dataset.x,baseY=+el.dataset.y;
      const drift=Math.sin(t*sp+i*.73)*7;
      const repelX=mx*28*d, repelY=my*22*d;
      const x=baseX+drift+repelX, y=baseY+Math.cos(t*sp+i*.41)*5+repelY;
      el.style.transform=`translate(-50%,-50%) translate(${x}%,${y}%) rotate(${+el.dataset.r+t*sp*8}deg) scale(${+el.dataset.s})`;
    });
    if(!reduced) raf=requestAnimationFrame(frame);
  }
  frame(start);
})();

/* ================= INITIALIZE ================= */
renderFilters();
renderProducts();
updateCartCount();
</script>

</body>
</html>
