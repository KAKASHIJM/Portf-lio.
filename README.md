# Portf-lio.
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<meta name="description"
content="DevSites — Desenvolvimento de sites, sistemas web, dashboards e lojas virtuais.">

<title>DevSites | Desenvolvimento Web</title>

<style>

:root {
    --bg: #050914;
    --bg2: #08111f;
    --card: #0c1627;
    --card2: #101c30;
    --line: #1b304c;

    --blue: #1495ff;
    --blue-light: #55c1ff;

    --text: #f5f8fc;
    --muted: #9aaac0;

    --green: #25d366;

    --radius: 20px;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Arial, Helvetica, sans-serif;

    background:
        radial-gradient(
            circle at 15% 0%,
            #0d2b4d 0,
            transparent 35%
        ),
        radial-gradient(
            circle at 90% 20%,
            #08264a 0,
            transparent 30%
        ),
        var(--bg);

    color: var(--text);
    line-height: 1.6;
}

a {
    text-decoration: none;
    color: inherit;
}

.container {
    width: min(1180px, 92%);
    margin: auto;
}

/* =========================
   HEADER
========================= */

header {
    position: sticky;
    top: 0;
    z-index: 100;

    background: rgba(5, 9, 20, .88);
    backdrop-filter: blur(15px);

    border-bottom: 1px solid var(--line);
}

.navbar {
    min-height: 75px;

    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 25px;
}

.logo {
    font-size: 23px;
    font-weight: 900;
}

.logo span {
    color: var(--blue);
}

.logo small {
    display: block;

    font-size: 8px;
    letter-spacing: 2px;

    color: var(--muted);
}

nav {
    display: flex;
    gap: 25px;
}

nav a {
    color: #d9e4f0;
    font-size: 14px;

    transition: .3s;
}

nav a:hover {
    color: var(--blue-light);
}

/* =========================
   BUTTON
========================= */

.btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;

    padding: 13px 20px;

    border-radius: 10px;

    background: var(--blue);

    border: 1px solid #42b3ff;

    color: white;

    font-weight: bold;

    cursor: pointer;

    transition: .3s;
}

.btn:hover {
    transform: translateY(-2px);

    box-shadow:
        0 10px 30px rgba(20,149,255,.25);
}

.btn-outline {
    background: transparent;

    border-color: #38506d;
}

/* =========================
   HERO
========================= */

.hero {
    padding: 110px 0 80px;

    text-align: center;
}

.badge {
    display: inline-block;

    padding: 7px 14px;

    border-radius: 50px;

    background: #092b49;

    border: 1px solid #15547e;

    color: #64c6ff;

    font-size: 12px;

    font-weight: bold;

    letter-spacing: 1px;
}

.hero h1 {
    max-width: 900px;

    margin: 22px auto;

    font-size: clamp(42px, 7vw, 75px);

    line-height: 1.05;
}

.hero h1 span {
    color: var(--blue-light);
}

.hero p {
    max-width: 720px;

    margin: auto;

    color: var(--muted);

    font-size: 18px;
}

.hero-buttons {
    margin-top: 30px;

    display: flex;

    justify-content: center;

    gap: 12px;

    flex-wrap: wrap;
}

/* =========================
   STATS
========================= */

.stats {
    margin-top: 60px;

    display: grid;

    grid-template-columns:
        repeat(3, 1fr);

    gap: 15px;
}

.stat {
    padding: 22px;

    background:
        linear-gradient(
            145deg,
            #0c182a,
            #07101d
        );

    border: 1px solid var(--line);

    border-radius: 16px;
}

.stat strong {
    display: block;

    font-size: 30px;

    color: var(--blue-light);
}

.stat span {
    color: var(--muted);

    font-size: 13px;
}

/* =========================
   SECTION
========================= */

section {
    padding: 75px 0;
}

.section-title {
    text-align: center;

    margin-bottom: 40px;
}

.kicker {
    color: var(--blue-light);

    font-size: 12px;

    font-weight: 900;

    letter-spacing: 2px;

    text-transform: uppercase;
}

.section-title h2 {
    font-size: 38px;

    margin: 7px 0;
}

.section-title p {
    color: var(--muted);
}

/* =========================
   SERVICES
========================= */

.services {
    display: grid;

    grid-template-columns:
        repeat(4, 1fr);

    gap: 18px;
}

.service {
    padding: 27px;

    background:
        linear-gradient(
            145deg,
            #0d1829,
            #08111f
        );

    border: 1px solid var(--line);

    border-radius: 18px;

    transition: .3s;
}

.service:hover {
    transform: translateY(-6px);

    border-color: #166aa5;
}

.service-icon {
    font-size: 32px;

    margin-bottom: 15px;
}

.service h3 {
    margin-bottom: 8px;
}

.service p {
    color: var(--muted);

    font-size: 14px;
}

/* =========================
   FILTERS
========================= */

.filters {
    display: flex;

    justify-content: center;

    flex-wrap: wrap;

    gap: 10px;

    margin-bottom: 30px;
}

.filter {
    padding: 9px 16px;

    border-radius: 50px;

    border: 1px solid var(--line);

    background: #0a1423;

    color: #cbd8e7;

    cursor: pointer;
}

.filter:hover,
.filter.active {
    background: #0866a8;

    border-color: var(--blue);

    color: white;
}

/* =========================
   PROJECTS
========================= */

.projects {
    display: grid;

    grid-template-columns:
        repeat(3, 1fr);

    gap: 20px;
}

.project {
    overflow: hidden;

    display: flex;

    flex-direction: column;

    background:
        linear-gradient(
            150deg,
            #0c1728,
            #07101c
        );

    border: 1px solid var(--line);

    border-radius: var(--radius);

    transition: .3s;
}

.project:hover {
    transform: translateY(-6px);

    border-color: #1672ae;

    box-shadow:
        0 20px 50px rgba(0,0,0,.5);
}

.project-image {
    height: 225px;

    overflow: hidden;

    cursor: pointer;

    background: #02060b;
}

.project-image img {
    width: 100%;
    height: 100%;

    object-fit: cover;

    transition: .4s;
}

.project:hover img {
    transform: scale(1.05);
}

.project-content {
    padding: 20px;
}

.project-category {
    color: var(--blue-light);

    font-size: 10px;

    font-weight: bold;

    letter-spacing: 1px;

    text-transform: uppercase;
}

.project h3 {
    margin: 7px 0;

    font-size: 21px;
}

.project p {
    color: var(--muted);

    font-size: 14px;
}

.tags {
    display: flex;

    flex-wrap: wrap;

    gap: 7px;

    margin: 15px 0;
}

.tags span {
    padding: 5px 9px;

    border-radius: 6px;

    border: 1px solid #263c57;

    color: #b9c8da;

    font-size: 11px;
}

.project-button {
    color: #63c7ff;

    font-weight: bold;

    font-size: 13px;
}

/* =========================
   TECHNOLOGIES
========================= */

.technologies {
    display: flex;

    justify-content: center;

    flex-wrap: wrap;

    gap: 12px;
}

.tech {
    padding: 15px 20px;

    background: #0a1423;

    border: 1px solid var(--line);

    border-radius: 12px;

    font-weight: bold;

    color: #dce8f5;

    transition: .3s;
}

.tech:hover {
    border-color: var(--blue);

    transform: translateY(-3px);
}

/* =========================
   CTA
========================= */

.cta {
    padding: 60px 30px;

    text-align: center;

    border-radius: 25px;

    background:
        linear-gradient(
            135deg,
            #07375f,
            #071324
        );

    border: 1px solid #145884;
}

.cta h2 {
    font-size: 38px;

    margin: 8px 0;
}

.cta p {
    max-width: 650px;

    margin: 10px auto 25px;

    color: var(--muted);
}

/* =========================
   FOOTER
========================= */

footer {
    padding: 30px 0;

    border-top: 1px solid var(--line);

    color: var(--muted);

    font-size: 13px;
}

.footer {
    display: flex;

    justify-content: space-between;

    flex-wrap: wrap;

    gap: 20px;
}

/* =========================
   MODAL
========================= */

.modal {
    position: fixed;

    inset: 0;

    z-index: 500;

    display: none;

    align-items: center;

    justify-content: center;

    padding: 20px;

    background: rgba(0,0,0,.85);
}

.modal.active {
    display: flex;
}

.modal-box {
    width: min(1100px, 95vw);

    max-height: 92vh;

    overflow: auto;

    background: #07101c;

    border: 1px solid #294766;

    border-radius: 20px;

    position: relative;
}

.modal-box img {
    width: 100%;

    max-height: 75vh;

    object-fit: contain;

    background: #02050a;

    display: block;
}

.close {
    position: absolute;

    right: 15px;
    top: 15px;

    width: 40px;
    height: 40px;

    border-radius: 50%;

    border: 1px solid #5c7188;

    background: #081321;

    color: white;

    font-size: 22px;

    cursor: pointer;

    z-index: 2;
}

.modal-info {
    padding: 20px;
}

.modal-info p {
    color: var(--muted);
}

/* =========================
   WHATSAPP
========================= */

.whatsapp {
    position: fixed;

    right: 22px;
    bottom: 22px;

    width: 58px;
    height: 58px;

    display: flex;

    align-items: center;
    justify-content: center;

    border-radius: 50%;

    background: var(--green);

    color: white;

    font-size: 27px;

    box-shadow:
        0 8px 30px rgba(37,211,102,.3);

    z-index: 100;
}

/* =========================
   RESPONSIVE
========================= */

@media(max-width: 950px) {

    nav {
        display: none;
    }

    .services {
        grid-template-columns:
            repeat(2, 1fr);
    }

    .projects {
        grid-template-columns:
            repeat(2, 1fr);
    }

}

@media(max-width: 650px) {

    .hero {
        padding-top: 75px;
    }

    .stats,
    .services,
    .projects {
        grid-template-columns: 1fr;
    }

    .section-title h2 {
        font-size: 30px;
    }

    .cta h2 {
        font-size: 30px;
    }

    .navbar > .btn {
        display: none;
    }

}

</style>
</head>

<body>

<!-- =========================
     HEADER
========================= -->

<header>

<div class="container navbar">

<a href="#inicio" class="logo">

&lt;/&gt; DEV<span>SITES</span>

<small>
SISTEMAS WEB PROFISSIONAIS
</small>

</a>

<nav>

<a href="#sobre">Sobre</a>

<a href="#servicos">Serviços</a>

<a href="#projetos">Projetos</a>

<a href="#tecnologias">Tecnologias</a>

<a href="#contato">Contato</a>

</nav>

<a
href="https://wa.me/"
target="_blank"
class="btn">

💬 WhatsApp

</a>

</div>

</header>


<main>

<!-- =========================
     HERO
========================= -->

<section class="hero" id="inicio">

<div class="container">

<span class="badge">
DESENVOLVIMENTO WEB • FULL-STACK
</span>

<h1>

Transformo ideias em

<span>
sistemas digitais
</span>

profissionais.

</h1>

<p>

Sites, landing pages, dashboards,
sistemas administrativos e lojas virtuais
criados para empresas que querem crescer
no digital.

</p>

<div class="hero-buttons">

<a href="#projetos" class="btn">
🖥️ Ver projetos
</a>

<a href="#contato" class="btn btn-outline">
🚀 Solicitar orçamento
</a>

</div>


<div class="stats">

<div class="stat">

<strong>
9+
</strong>

<span>
Projetos no portfólio
</span>

</div>


<div class="stat">

<strong>
100%
</strong>

<span>
Responsivo
</span>

</div>


<div class="stat">

<strong>
∞
</strong>

<span>
Soluções personalizadas
</span>

</div>

</div>

</div>

</section>


<!-- =========================
     SOBRE
========================= -->

<section id="sobre">

<div class="container">

<div class="section-title">

<span class="kicker">
Sobre a DevSites
</span>

<h2>
Código com objetivo.
</h2>

<p>

Desenvolvimento pensado para transformar
necessidades reais em soluções digitais
modernas e profissionais.

</p>

</div>

</div>

</section>


<!-- =========================
     SERVIÇOS
========================= -->

<section id="servicos">

<div class="container">

<div class="section-title">

<span class="kicker">
Serviços
</span>

<h2>
Soluções para o seu negócio
</h2>

</div>


<div class="services">


<div class="service">

<div class="service-icon">
🌐
</div>

<h3>
Criação de Sites
</h3>

<p>

Sites institucionais modernos,
rápidos e adaptados para celulares,
tablets e computadores.

</p>

</div>


<div class="service">

<div class="service-icon">
🚀
</div>

<h3>
Landing Pages
</h3>

<p>

Páginas profissionais focadas em
divulgação, captação de clientes
e conversão.

</p>

</div>


<div class="service">

<div class="service-icon">
⚙️
</div>

<h3>
Sistemas Web
</h3>

<p>

Dashboards, painéis administrativos
e sistemas personalizados para
empresas.

</p>

</div>


<div class="service">

<div class="service-icon">
🛒
</div>

<h3>
Lojas Virtuais
</h3>

<p>

Catálogos, carrinho, pedidos e
estruturas preparadas para vendas
online.

</p>

</div>

</div>

</div>

</section>


<!-- =========================
     PROJETOS
========================= -->

<section id="projetos">

<div class="container">

<div class="section-title">

<span class="kicker">
Portfólio
</span>

<h2>
Projetos selecionados
</h2>

<p>
Alguns dos projetos desenvolvidos pela DevSites.
</p>

</div>


<div class="filters">

<button class="filter active" data-filter="all">
Todos
</button>

<button class="filter" data-filter="site">
Sites
</button>

<button class="filter" data-filter="sistema">
Sistemas
</button>

<button class="filter" data-filter="dashboard">
Dashboards
</button>

</div>


<div class="projects">


<!-- HOUSE PIZZARIA -->

<article class="project" data-category="site">

<div
class="project-image"
onclick="openProject(
'assets/house-pizzaria-home.jpeg',
'House Pizzaria',
'Site profissional para pizzaria com cardápio e apresentação da marca.'
)"
>

<img
src="assets/house-pizzaria-home.jpeg"
alt="House Pizzaria"
>

</div>

<div class="project-content">

<span class="project-category">
SITE
</span>

<h3>
House Pizzaria
</h3>

<p>

Site completo com apresentação,
cardápio, promoções, depoimentos
e pedidos.

</p>

<div class="tags">

<span>HTML</span>
<span>CSS</span>
<span>JavaScript</span>

</div>

<a
href="#"
class="project-button"
onclick="openProject(
'assets/house-pizzaria-home.jpeg',
'House Pizzaria',
'Site profissional para pizzaria.'
);return false"
>

Ver projeto →

</a>

</div>

</article>


<!-- BELLA NAILS -->

<article class="project" data-category="site">

<div
class="project-image"
onclick="openProject(
'assets/studio-bella-nails.jpeg',
'Studio Bella Nails',
'Site de beleza com serviços e sistema de agendamento.'
)"
>

<img
src="assets/studio-bella-nails.jpeg"
alt="Studio Bella Nails"
>

</div>

<div class="project-content">

<span class="project-category">
SITE
</span>

<h3>
Studio Bella Nails
</h3>

<p>

Site para apresentação dos serviços,
agendamento e atendimento.

</p>

<div class="tags">

<span>HTML</span>
<span>CSS</span>
<span>JavaScript</span>

</div>

<a
href="#"
class="project-button"
onclick="openProject(
'assets/studio-bella-nails.jpeg',
'Studio Bella Nails',
'Site de serviços e agendamento.'
);return false"
>

Ver projeto →

</a>

</div>

</article>


<!-- HOUSE ADMIN -->

<article class="project" data-category="sistema">

<div
class="project-image"
onclick="openProject(
'assets/house-pizzaria-admin.jpeg',
'House Pizzaria — Painel Admin',
'Painel administrativo para gerenciamento de produtos, promoções e pedidos.'
)"
>

<img
src="assets/house-pizzaria-admin.jpeg"
alt="House Pizzaria Admin"
>

</div>

<div class="project-content">

<span class="project-category">
SISTEMA
</span>

<h3>
House Pizzaria — Admin
</h3>

<p>

Painel administrativo para
gerenciamento da pizzaria.

</p>

<div class="tags">

<span>Dashboard</span>
<span>Admin</span>
<span>CRUD</span>

</div>

<a
href="#"
class="project-button"
onclick="openProject(
'assets/house-pizzaria-admin.jpeg',
'House Pizzaria — Admin',
'Painel administrativo.'
);return false"
>

Ver projeto →

</a>

</div>

</article>


<!-- BARBEARIA -->

<article class="project" data-category="site">

<div
class="project-image"
onclick="openProject(
'assets/barbearia-style.png',
'Barbearia Style',
'Site de barbearia com serviços e agendamento.'
)"
>

<img
src="assets/barbearia-style.png"
alt="Barbearia Style"
>

</div>

<div class="project-content">

<span class="project-category">
SITE
</span>

<h3>
Barbearia Style
</h3>

<p>

Apresentação de serviços,
escolha de cortes e agendamento.

</p>

<div class="tags">

<span>HTML</span>
<span>CSS</span>
<span>JavaScript</span>

</div>

<a
href="#"
class="project-button"
onclick="openProject(
'assets/barbearia-style.png',
'Barbearia Style',
'Site com serviços e agendamento.'
);return false"
>

Ver projeto →

</a>

</div>

</article>


<!-- GESTÃO INTERNA -->

<article class="project" data-category="dashboard">

<div
class="project-image"
onclick="openProject(
'assets/gestao-interna-dashboard.jpeg',
'Gestão Interna',
'Dashboard administrativo com indicadores, usuários, alertas e relatórios.'
)"
>

<img
src="assets/gestao-interna-dashboard.jpeg"
alt="Gestão Interna"
>

</div>

<div class="project-content">

<span class="project-category">
DASHBOARD
</span>

<h3>
Gestão Interna
</h3>

<p>

Painel administrativo com
indicadores e acompanhamento
de atividades.

</p>

<div class="tags">

<span>Dashboard</span>
<span>KPI</span>
<span>Relatórios</span>

</div>

<a
href="#"
class="project-button"
onclick="openProject(
'assets/gestao-interna-dashboard.jpeg',
'Gestão Interna',
'Dashboard administrativo.'
);return false"
>

Ver projeto →

</a>

</div>

</article>


<!-- DISTRIBUIDORA -->

<article class="project" data-category="sistema">

<div
class="project-image"
onclick="openProject(
'assets/distribuidora-gestao.jpeg',
'Distribuidora — Gestão Inteligente',
'Sistema completo para estoque, vendas, pedidos, financeiro e relatórios.'
)"
>

<img
src="assets/distribuidora-gestao.jpeg"
alt="Distribuidora"
>

</div>

<div class="project-content">

<span class="project-category">
SISTEMA
</span>

<h3>
Distribuidora
</h3>

<p>

Sistema completo para gestão
de estoque, vendas e financeiro.

</p>

<div class="tags">

<span>React</span>
<span>Node.js</span>
<span>PostgreSQL</span>

</div>

<a
href="#"
class="project-button"
onclick="openProject(
'assets/distribuidora-gestao.jpeg',
'Distribuidora — Gestão Inteligente',
'Sistema de gestão empresarial.'
);return false"
>

Ver projeto →

</a>

</div>

</article>


<!-- RIFA -->

<article class="project" data-category="sistema">

<div
class="project-image"
onclick="openProject(
'assets/rifa-premium.jpeg',
'Rifa Premium',
'Sistema de seleção de números, pedidos e painel administrativo.'
)"
>

<img
src="assets/rifa-premium.jpeg"
alt="Rifa Premium"
>

</div>

<div class="project-content">

<span class="project-category">
SISTEMA
</span>

<h3>
Rifa Premium
</h3>

<p>

Interface de seleção de números,
pedido, pagamento e administração.

</p>

<div class="tags">

<span>JavaScript</span>
<span>PIX</span>
<span>Admin</span>

</div>

<a
href="#"
class="project-button"
onclick="openProject(
'assets/rifa-premium.jpeg',
'Rifa Premium',
'Sistema de rifas e painel administrativo.'
);return false"
>

Ver projeto →

</a>

</div>

</article>


<!-- DEV SITES -->

<article class="project" data-category="site">

<div
class="project-image"
onclick="openProject(
'assets/devsites-portfolio.jpeg',
'DevSites',
'Portfólio profissional da DevSites.'
)"
>

<img
src="assets/devsites-portfolio.jpeg"
alt="DevSites"
>

</div>

<div class="project-content">

<span class="project-category">
PORTFÓLIO
</span>

<h3>
DevSites
</h3>

<p>

Portfólio profissional com
serviços, projetos e tecnologias.

</p>

<div class="tags">

<span>Frontend</span>
<span>UI/UX</span>
<span>Responsivo</span>

</div>

<a
href="#"
class="project-button"
onclick="openProject(
'assets/devsites-portfolio.jpeg',
'DevSites',
'Portfólio profissional.'
);return false"
>

Ver projeto →

</a>

</div>

</article>


<!-- HOUSE SISTEMA -->

<article class="project" data-category="sistema">

<div
class="project-image"
onclick="openProject(
'assets/house-pizzaria-sistema.jpeg',
'House Pizzaria — Sistema',
'Cardápio digital, carrinho, pedidos e painel administrativo.'
)"
>

<img
src="assets/house-pizzaria-sistema.jpeg"
alt="House Pizzaria Sistema"
>

</div>

<div class="project-content">

<span class="project-category">
SISTEMA
</span>

<h3>
House Pizzaria — Sistema
</h3>

<p>

Sistema com cardápio,
carrinho, pedidos e administração.

</p>

<div class="tags">

<span>JavaScript</span>
<span>Pedidos</span>
<span>Admin</span>

</div>

<a
href="#"
class="project-button"
onclick="openProject(
'assets/house-pizzaria-sistema.jpeg',
'House Pizzaria — Sistema',
'Cardápio, carrinho e painel administrativo.'
);return false"
>

Ver projeto →

</a>

</div>

</article>


</div>

</div>

</section>


<!-- =========================
     TECNOLOGIAS
========================= -->

<section id="tecnologias">

<div class="container">

<div class="section-title">

<span class="kicker">
Tecnologias
</span>

<h2>
Ferramentas que utilizo
</h2>

</div>


<div class="technologies">

<div class="tech">
HTML5
</div>

<div class="tech">
CSS3
</div>

<div class="tech">
JavaScript
</div>

<div class="tech">
Python
</div>

<div class="tech">
C
</div>

<div class="tech">
Java
</div>

<div class="tech">
React
</div>

<div class="tech">
Node.js
</div>

<div class="tech">
PostgreSQL
</div>

<div class="tech">
Git
</div>

<div class="tech">
GitHub
</div>

</div>

</div>

</section>


<!-- =========================
     CONTATO
========================= -->

<section id="contato">

<div class="container">

<div class="cta">

<span class="kicker">
Vamos conversar?
</span>

<h2>
Seu próximo projeto começa aqui.
</h2>

<p>

Conte sua ideia, necessidade ou projeto.
A DevSites transforma conceitos em
soluções digitais profissionais.

</p>

<a
href="https://wa.me/"
target="_blank"
class="btn"
>

💬 Falar no WhatsApp

</a>

</div>

</div>

</section>

</main>


<!-- =========================
     FOOTER
========================= -->

<footer>

<div class="container footer">

<span>
© 2026 DevSites — Sistemas Web Profissionais.
</span>

<span>
Desenvolvimento • Design • Tecnologia
</span>

</div>

</footer>


<!-- =========================
     WHATSAPP
========================= -->

<a
href="https://wa.me/"
target="_blank"
class="whatsapp"
aria-label="WhatsApp"
>

☏

</a>


<!-- =========================
     MODAL PROJETO
========================= -->

<div
class="modal"
id="projectModal"
onclick="closeModalOutside(event)"
>

<div class="modal-box">

<button
class="close"
onclick="closeProject()"
>
×
</button>

<img
id="modalImage"
src=""
alt=""
>

<div class="modal-info">

<h3 id="modalTitle">
</h3>

<p id="modalDescription">
</p>

</div>

</div>

</div>


<script>

/* =========================
   FILTRO DOS PROJETOS
========================= */

const filterButtons =
document.querySelectorAll(".filter");

const projects =
document.querySelectorAll(".project");


filterButtons.forEach(button => {

    button.addEventListener("click", () => {

        filterButtons.forEach(btn => {
            btn.classList.remove("active");
        });

        button.classList.add("active");

        const filter =
            button.dataset.filter;

        projects.forEach(project => {

            if (
                filter === "all" ||
                project.dataset.category === filter
            ) {

                project.style.display = "flex";

            } else {

                project.style.display = "none";

            }

        });

    });

});


/* =========================
   MODAL
========================= */

function openProject(
    image,
    title,
    description
) {

    document.getElementById(
        "modalImage"
    ).src = image;

    document.getElementById(
        "modalTitle"
    ).textContent = title;

    document.getElementById(
        "modalDescription"
    ).textContent = description;

    document.getElementById(
        "projectModal"
    ).classList.add("active");

    document.body.style.overflow = "hidden";
}


function closeProject() {

    document.getElementById(
        "projectModal"
    ).classList.remove("active");

    document.body.style.overflow = "";

}


function closeModalOutside(event) {

    if (
        event.target.id === "projectModal"
    ) {

        closeProject();

    }

}


document.addEventListener(
    "keydown",
    function(event) {

        if (event.key === "Escape") {

            closeProject();

        }

    }
);

</script>

</body>
</html>