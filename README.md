<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Borges Tech Solution - Aplicativos, Sites e Soluções Digitais</title>
<meta name="description" content="Desenvolvemos aplicativos, sites e soluções digitais sob medida para empresas em Ribeirão Preto e região.">
<meta property="og:title" content="Borges Tech Solution - Aplicativos e Sites">
<meta property="og:description" content="Soluções digitais personalizadas para sua empresa.">
<meta property="og:image" content="Borges Tech Solution_logo.jpg">
<meta property="og:type" content="website">

<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<style>
:root {
    --primary-color: #0a1a2f;
    --secondary-color: #00ff99;
    --bg-color: #f8f9fa;
    --text-color: #333;
    --card-bg: #fff;
    --card-shadow: rgba(0,0,0,0.1);
}

* { box-sizing: border-box; }

body {
    margin: 0;
    font-family: 'Roboto', sans-serif;
    background-color: var(--bg-color);
    color: var(--text-color);
    scroll-behavior: smooth;
}

header {
    background: var(--primary-color);
    color: #fff;
    padding: 15px 40px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
}

header img { height: 60px; }

nav ul {
    list-style: none;
    display: flex;
    gap: 25px;
    margin: 0;
    padding: 0;
    flex-wrap: wrap;
}

nav ul li a {
    color: #fff;
    text-decoration: none;
    font-weight: 500;
    transition: color 0.3s;
}

nav ul li a:hover,
nav ul li a:focus { color: var(--secondary-color); }

.whatsapp-header a { font-size: 22px; color: #25d366; }
.whatsapp-mobile a { font-size: 24px; color: #25d366; }

/* Hero com partículas */
.hero {
    position: relative;
    color: #fff;
    text-align: center;
    padding: 120px 20px;
    overflow: hidden;
    background: linear-gradient(-45deg, #00ff99, #0a1a2f, #00ffe5, #0055cc);
    background-size: 400% 400%;
    animation: gradientAnimation 15s ease infinite;
}

.hero::before {
    content: "";
    position: absolute;
    inset: 0;
    background: rgba(10,26,47,0.5);
}

.hero-content {
    position: relative;
    z-index: 2;
    opacity: 0;
    transform: translateY(40px);
    transition: all 1s ease;
}

.hero-content.active { opacity: 1; transform: translateY(0); }

.hero h1 { font-size: 48px; margin-bottom: 15px; }
.hero p { font-size: 20px; margin-bottom: 30px; }

.hero a {
    background: var(--secondary-color);
    color: var(--primary-color);
    padding: 15px 30px;
    border-radius: 30px;
    text-decoration: none;
    font-weight: bold;
    transition: all 0.4s ease;
}

.hero a:hover {
    background: #00cc7a;
    transform: scale(1.05);
    box-shadow: 0 0 20px rgba(0,255,153,0.6);
}

@keyframes gradientAnimation {
    0%{background-position:0% 50%}
    50%{background-position:100% 50%}
    100%{background-position:0% 50%}
}

/* Seções */
section {
    padding: 60px 20px;
    opacity: 0;
    transform: translateY(40px);
    filter: blur(4px);
    transition: all 0.8s ease;
    color: #fff;
    background: linear-gradient(-45deg, #0055cc, #00ffe5, #0a1a2f, #00ff99);
    background-size: 400% 400%;
    animation: gradientAnimation 20s ease infinite;
}

section.active { opacity: 1; transform: translateY(0); filter: blur(0); }

.services h2 { font-size: 32px; text-align: center; margin-bottom: 40px; }

.service-cards, .portfolio-cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 25px;
    max-width: 1100px;
    margin: auto;
}

.card {
    background: var(--card-bg);
    padding: 25px;
    border-radius: 12px;
    box-shadow: 0 4px 10px var(--card-shadow);
    opacity: 0;
    transform: translateY(40px);
    transition: all 0.8s ease, transform 0.3s;
    text-align: center;
    color: var(--primary-color);
}

.card.active { opacity: 1; transform: translateY(0); }

.card i {
    font-size: 40px;
    color: var(--primary-color);
    margin-bottom: 15px;
    transition: transform 0.3s, color 0.3s;
}

.card:hover i {
    transform: scale(1.3) rotate(10deg);
    color: var(--secondary-color);
}

.card:hover {
    transform: translateY(-8px);
    box-shadow: 0 6px 15px var(--card-shadow);
}

/* Formulário */
form {
    max-width: 600px;
    margin: auto;
    display: flex;
    flex-direction: column;
    gap: 15px;
    background: rgba(255,255,255,0.9);
    padding: 25px;
    border-radius: 12px;
    color: #0a1a2f;
}

form input, form textarea {
    padding: 12px;
    border-radius: 6px;
    border: 1px solid #ccc;
    font-size: 16px;
    width: 100%;
}

form button {
    background: var(--secondary-color);
    border: none;
    color: var(--primary-color);
    font-weight: bold;
    padding: 15px;
    border-radius: 30px;
    cursor: pointer;
    transition: all 0.3s;
}

form button:hover { background: #00cc7a; transform: scale(1.05); }

/* Footer */
footer { background: var(--primary-color); color: #fff; text-align: center; padding: 25px 10px; margin-top: 50px; }

/* WhatsApp flutuante */
.whatsapp-float {
    position: fixed;
    width: 60px;
    height: 60px;
    bottom: 20px;
    right: 20px;
    background-color: #25d366;
    color: #fff;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 28px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.2);
    z-index: 1000;
    transition: transform 0.3s, box-shadow 0.3s;
    animation: pulse 2s infinite;
}

.whatsapp-float:hover {
    transform: scale(1.2);
    box-shadow: 0 0 20px rgba(37,211,102,0.8);
}

@keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.1); }
    100% { transform: scale(1); }
}

/* Ícone WhatsApp mobile */
.whatsapp-mobile { display: none; }

@media (max-width: 768px) {
    .hero h1 { font-size: 32px; }
    .hero p { font-size: 16px; }
    nav ul { flex-direction: column; gap: 10px; align-items: center; }
    header { justify-content: center; gap: 15px; }

    .whatsapp-header { display: none; }
    .whatsapp-mobile { display: inline-block; margin-top: 10px; }
    .whatsapp-mobile a:hover { color: #00cc7a; }
}
</style>
</head>
<body>

<header>
    <img src="Borges Tech Solution_logo.jpg" alt="Logo Borges Tech Solution">
    <nav>
        <ul>
            <li><a href="#home">Início</a></li>
            <li><a href="#servicos">Serviços</a></li>
            <li><a href="#portfolio">Portfólio</a></li>
            <li><a href="#contato">Contato</a></li>
            <!-- WhatsApp desktop -->
            <li class="whatsapp-header">
                <a href="https://wa.me/5516981848846?text=Ol%C3%A1%2C%20gostaria%20de%20mais%20informa%C3%A7%C3%B5es%20sobre%20seus%20softwares." target="_blank" aria-label="WhatsApp">
                    <i class="fab fa-whatsapp"></i>
                </a>
            </li>
            <!-- WhatsApp mobile -->
            <li class="whatsapp-mobile">
                <a href="https://wa.me/5516981848846?text=Ol%C3%A1%2C%20gostaria%20de%20mais%20informa%C3%A7%C3%B5es%20sobre%20seus%20softwares." target="_blank" aria-label="WhatsApp">
                    <i class="fab fa-whatsapp"></i>
                </a>
            </li>
        </ul>
    </nav>
</header>

<section class="hero" id="home">
    <canvas id="particles"></canvas>
    <div class="hero-content">
        <h1>Criação de Aplicativos e Sites Profissionais</h1>
        <p>Desenvolvemos soluções digitais sob medida para empresas em Ribeirão Preto e região.</p>
        <a href="#servicos">Nossos Serviços</a>
    </div>
</section>

<section class="services" id="servicos">
    <h2>O que fazemos</h2>
    <div class="service-cards">
        <div class="card"><i class="fas fa-mobile-alt"></i><h3>Desenvolvimento de Aplicativos</h3><p>Aplicativos modernos para Android e iOS, feitos para potencializar o seu negócio.</p></div>
        <div class="card"><i class="fas fa-laptop-code"></i><h3>Criação de Sites Profissionais</h3><p>Sites responsivos, rápidos e com design atual para empresas de todos os portes.</p></div>
        <div class="card"><i class="fas fa-briefcase"></i><h3>Soluções Empresariais Digitais</h3><p>Sistemas sob medida para gestão, automação e inovação nos processos do seu negócio.</p></div>
    </div>
</section>

<section class="services" id="portfolio">
    <h2>Cases de Sucesso</h2>
    <div class="portfolio-cards">
        <div class="card"><i class="fas fa-store"></i><h3>E-commerce Local</h3><p>Desenvolvemos uma loja virtual para uma rede de comércio regional, aumentando suas vendas em 60%.</p></div>
        <div class="card"><i class="fas fa-hospital"></i><h3>Aplicativo de Saúde</h3><p>Aplicativo móvel para clínicas, permitindo agendamento online e melhorando a experiência do paciente.</p></div>
        <div class="card"><i class="fas fa-building"></i><h3>Site Corporativo</h3><p>Website institucional moderno para uma empresa de engenharia, fortalecendo sua presença digital.</p></div>
    </div>
</section>

<section id="contato">
    <h2>Contato</h2>
    <form id="contactForm">
        <input type="text" name="name" placeholder="Seu nome" required>
        <input type="email" name="email" placeholder="Seu e-mail" required>
        <textarea name="message" rows="5" placeholder="Sua mensagem" required></textarea>
        <button type="submit">Enviar</button>
    </form>
</section>

<footer>
    <p>&copy; 2025 Borges Tech Solution - Ribeirão Preto. Todos os direitos reservados.</p>
</footer>

<!-- WhatsApp flutuante -->
<a href="https://wa.me/5516981848846?text=Ol%C3%A1%2C%20gostaria%20de%20mais%20informa%C3%A7%C3%B5es%20sobre%20seus%20softwares." class="whatsapp-float" target="_blank" aria-label="WhatsApp">
    <i class="fab fa-whatsapp"></i>
</a>

<script>
// Observer para fade in seções, hero e cards
const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if(entry.isIntersecting){ entry.target.classList.add('active'); }
    });
}, { threshold: 0.1 });
document.querySelectorAll('section, .hero-content, .card').forEach(el => observer.observe(el));

// Formulário envia para WhatsApp e email
document.getElementById('contactForm').addEventListener('submit', function(e){
    e.preventDefault();
    const name = this.name.value;
    const email = this.email.value;
    const message = this.message.value;

    // Link WhatsApp
    const waLink = `https://wa.me/5516981848846?text=Nome:%20${encodeURIComponent(name)}%0AEmail:%20${encodeURIComponent(email)}%0AMensagem:%20${encodeURIComponent(message)}`;
    window.open(waLink, '_blank');

    // Email
    const mailLink = `mailto:seuemail@dominio.com?subject=Contato%20via%20Site&body=Nome:%20${encodeURIComponent(name)}%0AEmail:%20${encodeURIComponent(email)}%0AMensagem:%20${encodeURIComponent(message)}`;
    window.open(mailLink, '_blank');

    alert("Mensagem enviada com sucesso!");
    this.reset();
});

// Partículas simples no hero
const canvas = document.getElementById('particles');
const ctx = canvas.getContext('2d');
let w, h;
function resize(){ w=canvas.width=window.innerWidth; h=canvas.height=400; }
window.addEventListener('resize', resize);
resize();

const particles = [];
for(let i=0;i<50;i++){ particles.push({x:Math.random()*w, y:Math.random()*h, r:Math.random()*3+1, dx:(Math.random()-0.5)*0.5, dy:(Math.random()-0.5)*0.5}); }

function animate(){
    ctx.clearRect(0,0,w,h);
    particles.forEach(p=>{
        p.x+=p.dx; p.y+=p.dy;
        if(p.x> w)p.x=0; if(p.x<0)p.x=w;
        if(p.y>h)p.y=0; if(p.y<0)p.y=h;
        ctx.beginPath();
        ctx.arc(p.x,p.y,p.r,0,Math.PI*2);
        ctx.fillStyle='rgba(255,255,255,0.7)';
        ctx.fill();
    });
    requestAnimationFrame(animate);
}
animate();
</script>

</body>
</html>
