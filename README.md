<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Borges Tech Solutions - Desenvolvimento de sistemas e sites personalizados para transformar seu negócio com soluções digitais inovadoras.">
    <meta name="keywords" content="desenvolvimento de sites, desenvolvimento de sistemas, aplicativos mobile, web development, software development, Borges Tech">
    <meta name="author" content="Borges Tech Solutions">
    <meta name="robots" content="index, follow">
    <meta property="og:title" content="Borges Tech Solutions - Soluções Digitais Personalizadas">
    <meta property="og:description" content="Especialistas em criar sites, sistemas e aplicativos mobile sob medida para impulsionar o seu negócio.">
    <meta property="og:image" content="https://seusite.com/logo_borgestech.png">
    <meta property="og:url" content="https://seusite.com">
    <meta property="og:type" content="website">
    <title>Borges Tech Solutions</title>
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    <link rel="preload" href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" as="style" onload="this.rel='stylesheet'">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" integrity="sha512-Avb2QiuDEEvB4bZJYdft2mNjVShBftLdPG8FJ0V7irTLQ8Uo0qcPxh4Plq7G5tGm0rU+1SPhVotteLpBERwTkw==" crossorigin="anonymous" referrerpolicy="no-referrer">
    <style>
        :root {
            --primary-color: #6A1B9A; /* Purple */
            --secondary-color: #FFD700; /* Gold */
            --text-color: #333;
            --white: #fff;
            --background: #F3E5F5; /* Light Purple */
            --footer-bg: #4A0072; /* Darker Purple */
            --whatsapp-color: #25D366; /* WhatsApp Green */
            --chatbot-color: #0288D1; /* Blue for Chatbot */
            --gradient-bg: linear-gradient(135deg, #F3E5F5 0%, #E1BEE7 100%); /* Subtle gradient */
        }

        * { box-sizing: border-box; margin: 0; padding: 0; scroll-behavior: smooth; }
        body { font-family: 'Roboto', sans-serif; background: var(--background); color: var(--text-color); line-height: 1.7; }
        a { text-decoration: none; color: var(--primary-color); transition: color 0.3s, outline 0.2s; }
        a:hover { color: var(--secondary-color); }
        a:focus, button:focus { outline: 2px solid var(--secondary-color); outline-offset: 3px; }

        /* Header */
        header {
            background: var(--primary-color);
            color: var(--white);
            padding: 15px 30px;
            position: fixed;
            width: 100%;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
            transition: background 0.3s;
        }
        header.scrolled { background: var(--footer-bg); }
        header h1 { font-size: 1.9rem; font-weight: 700; }
        nav { display: flex; gap: 25px; }
        nav a { color: var(--white); font-weight: bold; font-size: 1.1rem; transition: color 0.3s, transform 0.3s; }
        nav a:hover { color: var(--secondary-color); transform: scale(1.05); }
        #menu-toggle { display: none; font-size: 28px; background: none; border: none; color: var(--white); cursor: pointer; }
        nav.active { 
            display: flex; 
            flex-direction: column; 
            position: absolute; 
            top: 70px; 
            left: 0; 
            width: 100%; 
            background: var(--primary-color); 
            padding: 20px; 
        }

        /* Hero */
        .hero {
            background: linear-gradient(rgba(106, 27, 154, 0.85), rgba(106, 27, 154, 0.85)), url('hero-bg.jpg') center/cover;
            color: var(--white);
            text-align: center;
            padding: 160px 20px 100px;
            animation: fadeIn 1s ease-in;
        }
        .hero h2 { font-size: 3.2rem; margin-bottom: 25px; animation: slideInUp 0.5s ease; }
        .hero p { font-size: 1.6rem; margin-bottom: 25px; animation: slideInUp 0.7s ease; max-width: 800px; margin-left: auto; margin-right: auto; }
        .hero .cta-group { display: flex; gap: 20px; justify-content: center; flex-wrap: wrap; animation: slideInUp 0.9s ease; }
        .cta-btn { 
            background: var(--secondary-color); 
            color: var(--text-color); 
            padding: 14px 28px; 
            border-radius: 10px; 
            font-weight: bold; 
            font-size: 1.1rem;
            transition: transform 0.3s, box-shadow 0.3s, background 0.3s; 
        }
        .cta-btn:hover { transform: scale(1.08); box-shadow: 0 6px 12px rgba(0,0,0,0.3); background: #E6C200; }
        .cta-btn.whatsapp { background: var(--whatsapp-color); color: var(--white); }
        .cta-btn.whatsapp:hover { background: #20B858; }

        /* Sections */
        section { padding: 90px 20px; text-align: center; background: var(--gradient-bg); }
        section h2 { font-size: 2.8rem; margin-bottom: 50px; color: var(--primary-color); font-weight: 700; }
        .services .service, .portfolio .project, .blog .article { 
            margin: 25px; 
            display: inline-block; 
            width: 320px; 
            background: var(--white); 
            padding: 25px; 
            border-radius: 12px; 
            box-shadow: 0 6px 15px rgba(0,0,0,0.1); 
            transition: transform 0.3s, box-shadow 0.3s; 
        }
        .services .service:hover, .portfolio .project:hover, .blog .article:hover { 
            transform: translateY(-12px); 
            box-shadow: 0 10px 25px rgba(0,0,0,0.2); 
        }
        .services .service i { font-size: 3rem; color: var(--primary-color); margin-bottom: 20px; }
        .portfolio .project img, .services .service img { 
            width: 100%; 
            border-radius: 10px; 
            transition: transform 0.3s; 
            loading: lazy; 
        }
        .portfolio .project:hover img, .services .service:hover img { transform: scale(1.08); }
        .about p, .support .faq p { max-width: 900px; margin: 0 auto 40px; font-size: 1.1rem; }
        .team { display: flex; justify-content: center; gap: 30px; flex-wrap: wrap; }
        .team-member { width: 220px; text-align: center; }
        .team-member img { width: 100%; border-radius: 50%; margin-bottom: 15px; loading: lazy; }
        .testimonials { margin-top: 50px; }
        .testimonials blockquote { font-style: italic; margin: 25px 0; max-width: 700px; margin-left: auto; margin-right: auto; font-size: 1.1rem; }
        .blog .article { text-align: left; }
        .support .faq { max-width: 900px; margin: 0 auto; }
        .support .faq details { margin-bottom: 25px; }
        .support .faq summary { font-weight: bold; cursor: pointer; font-size: 1.2rem; }

        /* Contact */
        .contact .contact-info { max-width: 700px; margin: 30px auto; text-align: left; }
        .contact .contact-info p { margin-bottom: 15px; font-size: 1.1rem; }
        .contact .cta-btn { 
            background: var(--whatsapp-color); 
            color: var(--white); 
            padding: 14px 28px; 
            border-radius: 10px; 
            font-weight: bold; 
            display: inline-block; 
            margin-top: 25px; 
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            align-items: center;
            justify-content: center;
        }
        .modal.show { display: flex; }
        .modal-content {
            background: var(--white);
            padding: 25px;
            border-radius: 14px;
            max-width: 550px;
            width: 90%;
            box-shadow: 0 6px 25px rgba(0,0,0,0.3);
            position: relative;
            animation: slideIn 0.4s ease;
        }
        .modal-content h3 { font-size: 1.7rem; color: var(--primary-color); margin-bottom: 25px; text-align: center; }
        .modal-content label { display: block; font-weight: bold; margin-bottom: 8px; font-size: 1.1rem; }
        .modal-content input, .modal-content textarea { 
            width: 100%; 
            padding: 12px; 
            margin-bottom: 20px; 
            border: 1px solid #ccc; 
            border-radius: 8px; 
            font-family: 'Roboto', sans-serif; 
            font-size: 1rem; 
        }
        .modal-content textarea { resize: vertical; min-height: 120px; }
        .modal-content input:focus, .modal-content textarea:focus { 
            border-color: var(--secondary-color); 
            outline: none; 
            box-shadow: 0 0 6px rgba(255, 215, 0, 0.5); 
        }
        .modal-content button[type="submit"] { 
            background: var(--whatsapp-color); 
            color: var(--white); 
            padding: 14px 28px; 
            border: none; 
            border-radius: 10px; 
            font-weight: bold; 
            cursor: pointer; 
            width: 100%; 
            transition: transform 0.3s, opacity 0.3s; 
        }
        .modal-content button[type="submit"]:hover { transform: scale(1.05); opacity: 0.95; }
        .close-btn { 
            position: absolute; 
            top: 15px; 
            right: 20px; 
            font-size: 28px; 
            color: var(--text-color); 
            cursor: pointer; 
            transition: color 0.3s; 
        }
        .close-btn:hover { color: var(--secondary-color); }

        /* Chatbot */
        .chatbot-modal {
            display: none;
            position: fixed;
            bottom: 80px;
            left: 20px; /* Moved to left side */
            width: 360px;
            height: 520px;
            background: var(--white);
            border-radius: 14px;
            box-shadow: 0 6px 25px rgba(0,0,0,0.3);
            z-index: 1000;
            flex-direction: column;
            overflow: hidden;
        }
        .chatbot-modal.show { display: flex; }
        .chatbot-header {
            background: var(--chatbot-color);
            color: var(--white);
            padding: 12px;
            text-align: center;
            font-size: 1.3rem;
            font-weight: bold;
        }
        .chatbot-body {
            flex: 1;
            padding: 20px;
            overflow-y: auto;
            background: #f9f9f9;
        }
        .chatbot-message {
            margin-bottom: 12px;
            padding: 12px;
            border-radius: 10px;
            max-width: 80%;
            line-height: 1.5;
            font-size: 0.95rem;
        }
        .chatbot-message.bot { background: var(--chatbot-color); color: var(--white); margin-left: auto; }
        .chatbot-message.user { background: var(--secondary-color); color: var(--text-color); margin-right: auto; }
        .chatbot-message.loading::after {
            content: '';
            display: inline-block;
            width: 22px;
            height: 22px;
            border: 2px solid var(--white);
            border-top-color: transparent;
            border-radius: 50%;
            animation: spin 1s linear infinite;
            margin-left: 12px;
            vertical-align: middle;
        }
        .chatbot-options {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 12px;
        }
        .chatbot-option-btn {
            background: var(--secondary-color);
            color: var(--text-color);
            border: none;
            padding: 10px 14px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 0.95rem;
            transition: opacity 0.3s, transform 0.3s;
        }
        .chatbot-option-btn:hover { opacity: 0.95; transform: scale(1.05); }
        .chatbot-input {
            display: flex;
            padding: 12px;
            background: var(--white);
            border-top: 1px solid #ccc;
        }
        .chatbot-input input {
            flex: 1;
            padding: 12px;
            border: 1px solid #ccc;
            border-radius: 8px;
            font-size: 1rem;
            margin-right: 12px;
        }
        .chatbot-input button {
            background: var(--whatsapp-color);
            color: var(--white);
            border: none;
            padding: 12px 18px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1rem;
        }
        .chatbot-input button:hover { opacity: 0.95; }

        /* Floating Buttons */
        .floating-buttons {
            position: fixed;
            bottom: 20px;
            right: 20px;
            display: flex;
            flex-direction: column;
            gap: 20px;
            z-index: 1000;
            opacity: 0;
            transition: opacity 0.6s ease-in-out;
        }
        .floating-buttons.show { opacity: 1; }
        .floating-btn {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 30px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.3);
            transition: transform 0.3s, box-shadow 0.3s;
            animation: pulse 2s infinite;
        }
        .floating-btn:hover { transform: scale(1.2); box-shadow: 0 12px 24px rgba(0,0,0,0.4); }
        .whatsapp-btn-floating { background-color: var(--whatsapp-color); }
        .whatsapp-btn-floating:hover::after {
            content: "Abrir Formulário de Contato";
            position: absolute;
            bottom: 70px;
            right: 50%;
            transform: translateX(50%);
            background-color: #333;
            color: var(--white);
            padding: 8px 12px;
            border-radius: 8px;
            font-size: 0.95rem;
            box-shadow: 0 2px 8px rgba(0,0,0,0.3);
            max-width: 160px;
            line-height: 1.5;
        }
        .contact-btn-floating { background-color: var(--secondary-color); }
        .contact-btn-floating:hover::after {
            content: "Solicitar Orçamento";
            position: absolute;
            bottom: 70px;
            right: 50%;
            transform: translateX(50%);
            background-color: #333;
            color: var(--white);
            padding: 8px 12px;
            border-radius: 8px;
            font-size: 0.95rem;
            box-shadow: 0 2px 8px rgba(0,0,0,0.3);
            max-width: 160px;
            line-height: 1.5;
        }
        .chatbot-btn-floating { background-color: var(--chatbot-color); }
        .chatbot-btn-floating:hover::after {
            content: "Chatbot de Suporte";
            position: absolute;
            bottom: 70px;
            right: 50%;
            transform: translateX(50%);
            background-color: #333;
            color: var(--white);
            padding: 8px 12px;
            border-radius: 8px;
            font-size: 0.95rem;
            box-shadow: 0 2px 8px rgba(0,0,0,0.3);
            max-width: 160px;
            line-height: 1.5;
        }

        /* Footer */
        footer { background: var(--footer-bg); color: var(--white); text-align: center; padding: 25px; }
        footer a { color: var(--secondary-color); font-size: 1.1rem; }
        footer a:hover { text-decoration: underline; transform: scale(1.05); }

        /* Animations */
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
        @keyframes slideIn { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }
        @keyframes slideInUp { from { opacity: 0; transform: translateY(50px); } to { opacity: 1; transform: translateY(0); } }
        @keyframes pulse { 0%, 100% { transform: scale(1); } 50% { transform: scale(1.1); } }
        @keyframes spin { to { transform: rotate(360deg); } }

        /* Responsive */
        @media (max-width: 768px) {
            header { flex-direction: column; align-items: flex-start; padding: 12px 25px; }
            #menu-toggle { display: block; }
            nav { display: none; }
            nav.active { display: flex; }
            .hero h2 { font-size: 2.2rem; }
            .hero p { font-size: 1.3rem; }
            .team { flex-direction: column; }
            .floating-buttons { bottom: 15px; right: 15px; gap: 15px; }
            .floating-btn { width: 50px; height: 50px; font-size: 26px; }
            .chatbot-modal { width: 90%; height: 400px; left: 15px; }
            .modal-content { width: 95%; }
            .whatsapp-btn-floating:hover::after, .contact-btn-floating:hover::after, .chatbot-btn-floating:hover::after { font-size: 0.85rem; padding: 6px 10px; max-width: 130px; }
            .hero .cta-group { flex-direction: column; }
            .services .service, .portfolio .project, .blog .article { width: 100%; max-width: 350px; }
        }
        @media (max-width: 480px) {
            .hero { padding: 120px 15px; }
            .hero h2 { font-size: 1.9rem; }
            .hero p { font-size: 1.1rem; }
            .modal-content { padding: 20px; }
            .chatbot-modal { width: 95%; height: 360px; left: 10px; }
            section { padding: 60px 15px; }
        }
    </style>
</head>
<body>
    <header id="header" role="banner">
        <h1>Borges Tech Solutions</h1>
        <button id="menu-toggle" aria-label="Alternar menu de navegação" aria-expanded="false"><i class="fas fa-bars" aria-hidden="true"></i></button>
        <nav role="navigation" aria-label="Menu principal">
            <a href="#home" aria-current="page">Home</a>
            <a href="#about">Sobre</a>
            <a href="#services">Serviços</a>
            <a href="#portfolio">Portfólio</a>
            <a href="#blog">Blog</a>
            <a href="#contact">Contato</a>
            <a href="#support">Suporte</a>
        </nav>
    </header>

    <section class="hero" id="home" role="region" aria-labelledby="hero-title">
        <h2 id="hero-title">Soluções Digitais que Impulsionam o seu Negócio</h2>
        <p>Desenvolvemos sistemas e sites personalizados que transformam ideias em soluções digitais eficientes, otimizadas e escaláveis.</p>
        <p><strong>Por que nos escolher?</strong> Expertise em projetos sob medida, entrega ágil e suporte contínuo com tecnologia de ponta.</p>
        <div class="cta-group">
            <button class="cta-btn" id="open-demo-form" aria-label="Solicitar demonstração">Solicitar Demonstração</button>
            <button class="cta-btn whatsapp" id="open-contact-form-hero" aria-label="Fale conosco">Fale Conosco</button>
            <button class="cta-btn" id="open-budget-form" aria-label="Peça um orçamento">Peça um Orçamento</button>
        </div>
    </section>

    <section id="about" role="region" aria-labelledby="about-title">
        <h2 id="about-title">Sobre a Empresa</h2>
        <p><strong>História:</strong> Fundada em 2023, a Borges Tech Solutions nasceu com o propósito de entregar tecnologia inovadora para empresas de todos os tamanhos.</p>
        <p><strong>Missão:</strong> Impulsionar o crescimento de nossos clientes com soluções digitais personalizadas.</p>
        <p><strong>Visão:</strong> Ser referência em desenvolvimento de software na América Latina até 2030.</p>
        <p><strong>Valores:</strong> Inovação, qualidade, transparência e compromisso com o cliente.</p>
        <h3>Nossa Equipe</h3>
        <div class="team">
            <div class="team-member">
                <img src="joao_henrique.jpg" alt="João Henrique Borges, CEO & Desenvolvedor">
                <h4>João Henrique Borges</h4>
                <p>CEO & Desenvolvedor</p>
            </div>
        </div>
        <h3>Certificações e Parcerias</h3>
        <p>Parceiros AWS Certified, certificados ISO 9001 e membros do programa Google for Startups.</p>
    </section>

    <section id="services" role="region" aria-labelledby="services-title">
        <h2 id="services-title">Nossos Serviços</h2>
        <div class="services">
            <div class="service">
                <i class="fas fa-code fa-3x"></i>
                <h3>Desenvolvimento de Sites</h3>
                <p>Criamos sites responsivos, otimizados para SEO e com interfaces intuitivas.</p>
                <p><strong>Benefícios:</strong> Aumente sua visibilidade online e engaje seus clientes.</p>
                <img src="site-screenshot.jpg" alt="Exemplo de site desenvolvido" loading="lazy">
            </div>
            <div class="service">
                <i class="fas fa-laptop-code fa-3x"></i>
                <h3>Desenvolvimento de Sistemas</h3>
                <p>Sistemas sob medida para automação de processos e gestão empresarial.</p>
                <p><strong>Benefícios:</strong> Reduza custos operacionais e melhore a eficiência.</p>
                <img src="system-screenshot.jpg" alt="Exemplo de sistema desenvolvido" loading="lazy">
            </div>
            <div class="service">
                <i class="fas fa-mobile-alt fa-3x"></i>
                <h3>Aplicativos Mobile</h3>
                <p>Apps para iOS e Android com foco em usabilidade e integração.</p>
                <p><strong>Benefícios:</strong> Conecte-se com seus clientes em qualquer lugar.</p>
                <img src="app-screenshot.jpg" alt="Exemplo de aplicativo mobile" loading="lazy">
            </div>
        </div>
    </section>

    <section id="portfolio" role="region" aria-labelledby="portfolio-title">
        <h2 id="portfolio-title">Portfólio e Cases de Sucesso</h2>
        <div class="portfolio">
            <div class="project">
                <img src="project1.jpg" alt="Site E-commerce" loading="lazy">
                <h3>Site E-commerce</h3>
                <p>Loja online com integração de pagamentos para uma varejista.</p>
                <p><strong>Resultado:</strong> Aumento de 30% nas vendas online em 6 meses.</p>
            </div>
            <div class="project">
                <img src="project2.jpg" alt="Sistema de Gestão" loading="lazy">
                <h3>Sistema de Gestão</h3>
                <p>ERP personalizado para uma empresa de logística.</p>
                <p><strong>Resultado:</strong> Redução de 20% no tempo de processamento de pedidos.</p>
            </div>
            <div class="project">
                <img src="project3.jpg" alt="App de Delivery" loading="lazy">
                <h3>App de Delivery</h3>
                <p>Aplicativo para entrega de alimentos com rastreamento em tempo real.</p>
                <p><strong>Resultado:</strong> 95% de satisfação dos usuários.</p>
            </div>
        </div>
        <div class="testimonials">
            <h3>Depoimentos</h3>
            <blockquote>"A Borges Tech entregou um site incrível que aumentou nosso alcance online!" – Ana Costa, CEO de Loja Virtual</blockquote>
            <blockquote>"O sistema de gestão transformou nossa operação. Excelente suporte!" – Carlos Mendes, Logística Express</blockquote>
        </div>
    </section>

    <section id="blog" role="region" aria-labelledby="blog-title">
        <h2 id="blog-title">Blog</h2>
        <div class="blog">
            <div class="article">
                <h3>Como a Automação Pode Transformar Sua Empresa</h3>
                <p>Descubra como sistemas personalizados reduzem custos e aumentam a eficiência.</p>
                <a href="#" aria-label="Leia mais sobre automação">Leia mais</a>
            </div>
            <div class="article">
                <h3>5 Tendências em Desenvolvimento Web para 2025</h3>
                <p>Fique por dentro das inovações que estão moldando o futuro digital.</p>
                <a href="#" aria-label="Leia mais sobre tendências em desenvolvimento web">Leia mais</a>
            </div>
            <div class="article">
                <h3>Dicas para Criar um App Mobile de Sucesso</h3>
                <p>Os segredos para desenvolver aplicativos que engajam usuários.</p>
                <a href="#" aria-label="Leia mais sobre desenvolvimento de apps">Leia mais</a>
            </div>
        </div>
        <a href="#" class="cta-btn" aria-label="Ver todos os artigos do blog">Ver Todos os Artigos</a>
    </section>

    <section id="contact" role="region" aria-labelledby="contact-title">
        <h2 id="contact-title">Contato</h2>
        <div class="contact-info">
            <p><strong>Telefone/WhatsApp:</strong> <a href="https://wa.me/5516981848861" target="_blank" rel="noopener noreferrer">+55 (16) 98184-8861</a></p>
            <p><strong>E-mail:</strong> <a href="mailto:contato@borgestech.com">contato@borgestech.com</a></p>
            <p><strong>Endereço:</strong> Rua Exemplo, 123, São Paulo, SP, Brasil</p>
            <p><strong>Redes Sociais:</strong> 
                <a href="#" aria-label="Siga-nos no Facebook"><i class="fab fa-facebook"></i></a>
                <a href="#" aria-label="Siga-nos no LinkedIn"><i class="fab fa-linkedin"></i></a>
                <a href="#" aria-label="Siga-nos no Instagram"><i class="fab fa-instagram"></i></a>
            </p>
        </div>
        <button class="cta-btn" id="open-contact-form" aria-label="Abrir formulário de contato">Fale Conosco</button>
    </section>

    <section id="support" role="region" aria-labelledby="support-title">
        <h2 id="support-title">Suporte ao Cliente</h2>
        <div class="faq">
            <h3>Perguntas Frequentes</h3>
            <details>
                <summary>Quanto tempo leva para desenvolver um site?</summary>
                <p>Depende do projeto, mas sites simples levam de 2 a 4 semanas, enquanto projetos complexos podem levar de 2 a 6 meses.</p>
            </details>
            <details>
                <summary>Vocês oferecem suporte após a entrega?</summary>
                <p>Sim, oferecemos suporte contínuo para todos os nossos projetos, com planos de manutenção personalizados.</p>
            </details>
            <details>
                <summary>Como funciona o processo de desenvolvimento?</summary>
                <p>Nosso processo inclui análise de requisitos, prototipagem, desenvolvimento, testes e entrega, com revisões constantes com o cliente.</p>
            </details>
        </div>
        <p><a href="#" aria-label="Acessar área do cliente">Área do Cliente</a> (para projetos em andamento)</p>
        <button class="cta-btn" id="open-support-form" aria-label="Abrir chatbot de suporte">Chat de Suporte</button>
    </section>

    <div class="modal" id="contact-modal" role="dialog" aria-labelledby="form-title">
        <div class="modal-content">
            <span class="close-btn" id="close-form" aria-label="Fechar formulário">&times;</span>
            <h3 id="form-title">Solicitar Orçamento</h3>
            <form id="whatsapp-form">
                <label for="name">Nome:</label>
                <input type="text" id="name" name="name" required aria-required="true" placeholder="Digite seu nome">
                <label for="phone">Telefone:</label>
                <input type="tel" id="phone" name="phone" required aria-required="true" placeholder="Digite seu telefone (com DDD)">
                <label for="message">Mensagem:</label>
                <textarea id="message" name="message" required aria-required="true" placeholder="Descreva sua solicitação"></textarea>
                <button type="submit" aria-label="Enviar mensagem via WhatsApp">Enviar via WhatsApp</button>
            </form>
        </div>
    </div>

    <div class="chatbot-modal" id="chatbot-modal" role="dialog" aria-labelledby="chatbot-title">
        <div class="chatbot-header" id="chatbot-title">Assistente Borges Tech</div>
        <div class="chatbot-body" id="chatbot-messages"></div>
        <div class="chatbot-input">
            <input type="text" id="chatbot-input" placeholder="Digite sua mensagem..." aria-label="Digite sua mensagem para o chatbot">
            <button id="chatbot-send" aria-label="Enviar mensagem no chatbot">Enviar</button>
        </div>
    </div>

    <div class="floating-buttons" id="floating-buttons" role="region" aria-label="Botões de contato rápidos">
        <button class="floating-btn contact-btn-floating" id="open-contact-form-floating" aria-label="Abrir formulário de contato"><i class="fas fa-envelope" aria-hidden="true"></i></button>
        <button class="floating-btn chatbot-btn-floating" id="open-chatbot" aria-label="Abrir chatbot de suporte"><i class="fas fa-robot" aria-hidden="true"></i></button>
        <button class="floating-btn whatsapp-btn-floating" id="open-whatsapp-form" aria-label="Abrir formulário de contato via WhatsApp"><i class="fab fa-whatsapp" aria-hidden="true"></i></button>
    </div>

    <footer role="contentinfo">
        <p>&copy; 2025 Borges Tech Solutions. Todos os direitos reservados.</p>
        <p>Siga-nos: 
            <a href="#" aria-label="Siga-nos no Facebook"><i class="fab fa-facebook"></i></a> 
            <a href="#" aria-label="Siga-nos no LinkedIn"><i class="fab fa-linkedin"></i></a> 
            <a href="#" aria-label="Siga-nos no Instagram"><i class="fab fa-instagram"></i></a>
        </p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const menuToggle = document.getElementById('menu-toggle');
            const nav = document.querySelector('nav');
            const floatingButtons = document.getElementById('floating-buttons');
            const openContactForm = document.getElementById('open-contact-form');
            const openContactFormFloating = document.getElementById('open-contact-form-floating');
            const openWhatsAppForm = document.getElementById('open-whatsapp-form');
            const openDemoForm = document.getElementById('open-demo-form');
            const openBudgetForm = document.getElementById('open-budget-form');
            const openSupportForm = document.getElementById('open-support-form');
            const closeForm = document.getElementById('close-form');
            const contactModal = document.getElementById('contact-modal');
            const form = document.getElementById('whatsapp-form');
            const openChatbot = document.getElementById('open-chatbot');
            const chatbotModal = document.getElementById('chatbot-modal');
            const chatbotInput = document.getElementById('chatbot-input');
            const chatbotSend = document.getElementById('chatbot-send');
            const chatbotMessages = document.getElementById('chatbot-messages');

            // Menu hamburguer
            menuToggle.addEventListener('click', () => {
                const isExpanded = menuToggle.getAttribute('aria-expanded') === 'true';
                menuToggle.setAttribute('aria-expanded', !isExpanded);
                nav.classList.toggle('active');
            });

            // Mostrar botões flutuantes
            setTimeout(() => floatingButtons.classList.add('show'), 500);

            // Efeito de scroll no header
            window.addEventListener('scroll', () => {
                document.getElementById('header').classList.toggle('scrolled', window.scrollY > 50);
            });

            // Abrir modal de contato
            [openContactForm, openContactFormFloating, openWhatsAppForm, openDemoForm, openBudgetForm].forEach(btn => {
                btn.addEventListener('click', () => {
                    contactModal.classList.add('show');
                    chatbotModal.classList.remove('show');
                    document.getElementById('name').focus();
                });
            });

            // Abrir chatbot para suporte
            openSupportForm.addEventListener('click', () => {
                chatbotModal.classList.toggle('show');
                contactModal.classList.remove('show');
                if (chatbotModal.classList.contains('show') && chatState === 'initial') {
                    addMessage('Olá! Bem-vindo ao Assistente Borges Tech. Como posso ajudar você hoje?', 'bot', [
                        { label: 'Solicitar Orçamento', value: 'Solicitar Orçamento' },
                        { label: 'Solicitar Suporte', value: 'Solicitar Suporte' }
                    ]);
                }
            });

            // Fechar modal
            closeForm.addEventListener('click', () => contactModal.classList.remove('show'));

            // Fechar modal ao clicar fora
            contactModal.addEventListener('click', (e) => {
                if (e.target === contactModal) contactModal.classList.remove('show');
            });

            // Enviar formulário via WhatsApp
            form.addEventListener('submit', (e) => {
                e.preventDefault();
                const name = document.getElementById('name').value.trim();
                const phone = document.getElementById('phone').value.trim();
                const message = document.getElementById('message').value.trim();
                const whatsappMessage = `Olá, meu nome é ${encodeURIComponent(name)}. Meu telefone é ${encodeURIComponent(phone)}. Mensagem: ${encodeURIComponent(message)}`;
                const whatsappUrl = `https://wa.me/5516981848861?text=${whatsappMessage}`;
                window.open(whatsappUrl, '_blank', 'noopener,noreferrer');
                form.reset();
                contactModal.classList.remove('show');
            });

            // Chatbot logic
            let chatState = 'initial';
            let projectData = {};
            let isBotResponding = false;

            const addMessage = (message, sender, options = []) => {
                const msgDiv = document.createElement('div');
                msgDiv.classList.add('chatbot-message', sender);
                if (sender === 'bot' && isBotResponding) msgDiv.classList.add('loading');
                msgDiv.textContent = message;
                chatbotMessages.appendChild(msgDiv);

                if (options.length > 0) {
                    const optionsDiv = document.createElement('div');
                    optionsDiv.classList.add('chatbot-options');
                    options.forEach(opt => {
                        const btn = document.createElement('button');
                        btn.classList.add('chatbot-option-btn');
                        btn.textContent = opt.label;
                        btn.addEventListener('click', () => handleChatbotInput(opt.value));
                        optionsDiv.appendChild(btn);
                    });
                    chatbotMessages.appendChild(optionsDiv);
                }

                chatbotMessages.scrollTop = chatbotMessages.scrollHeight;
                if (sender === 'bot' && isBotResponding) {
                    setTimeout(() => msgDiv.classList.remove('loading'), 1000);
                }
            };

            const handleChatbotInput = (input) => {
                if (isBotResponding) return;
                addMessage(input, 'user');
                isBotResponding = true;

                let response = '';
                let options = [];

                if (chatState === 'initial') {
                    if (input.toLowerCase().includes('projeto') || input === 'Solicitar Orçamento') {
                        chatState = 'project_type';
                        response = 'Ótimo! Que tipo de projeto você deseja?';
                        options = [
                            { label: 'Site', value: 'Site' },
                            { label: 'Sistema', value: 'Sistema' },
                            { label: 'Aplicativo Mobile', value: 'Aplicativo Mobile' }
                        ];
                    } else if (input.toLowerCase().includes('suporte') || input === 'Solicitar Suporte') {
                        chatState = 'support_name';
                        response = 'Entendido! Para solicitar suporte, informe seu nome.';
                    } else if (input.toLowerCase().includes('reiniciar') || input === 'Reiniciar') {
                        chatState = 'initial';
                        projectData = {};
                        response = 'Conversa reiniciada! Como posso ajudar? Escolha uma opção:';
                        options = [
                            { label: 'Solicitar Orçamento', value: 'Solicitar Orçamento' },
                            { label: 'Solicitar Suporte', value: 'Solicitar Suporte' }
                        ];
                    } else {
                        response = 'Desculpe, não entendi. Escolha uma opção para continuar:';
                        options = [
                            { label: 'Solicitar Orçamento', value: 'Solicitar Orçamento' },
                            { label: 'Solicitar Suporte', value: 'Solicitar Suporte' }
                        ];
                    }
                } else if (chatState === 'project_type') {
                    projectData.type = input;
                    if (!['Site', 'Sistema', 'Aplicativo Mobile'].includes(input)) {
                        response = 'Por favor, escolha uma opção válida: Site, Sistema ou Aplicativo Mobile.';
                        options = [
                            { label: 'Site', value: 'Site' },
                            { label: 'Sistema', value: 'Sistema' },
                            { label: 'Aplicativo Mobile', value: 'Aplicativo Mobile' }
                        ];
                    } else {
                        chatState = 'project_details';
                        response = 'Por favor, descreva brevemente o que você precisa para o projeto.';
                    }
                } else if (chatState === 'project_details') {
                    projectData.details = input;
                    chatState = 'project_name';
                    response = 'Ótimo! Qual é o seu nome?';
                } else if (chatState === 'project_name') {
                    projectData.name = input;
                    chatState = 'project_phone';
                    response = 'Qual é o seu número de telefone (com DDD)?';
                } else if (chatState === 'project_phone') {
                    projectData.phone = input;
                    if (!/^\d{10,11}$/.test(projectData.phone.replace(/\D/g, ''))) {
                        response = 'Por favor, insira um número de telefone válido com DDD (ex.: 16987654321).';
                    } else {
                        chatState = 'initial';
                        const whatsappMessage = `Solicitação de Orçamento\nNome: ${encodeURIComponent(projectData.name)}\nTelefone: ${encodeURIComponent(projectData.phone)}\nTipo de Projeto: ${encodeURIComponent(projectData.type)}\nDetalhes: ${encodeURIComponent(projectData.details)}`;
                        const whatsappUrl = `https://wa.me/5516981848861?text=${whatsappMessage}`;
                        window.open(whatsappUrl, '_blank', 'noopener,noreferrer');
                        response = 'Sua solicitação foi enviada via WhatsApp! Nossa equipe entrará em contato em breve. Deseja reiniciar a conversa?';
                        options = [
                            { label: 'Reiniciar', value: 'Reiniciar' },
                            { label: 'Fechar', value: 'Fechar' }
                        ];
                        projectData = {};
                    }
                } else if (chatState === 'support_name') {
                    projectData.name = input;
                    chatState = 'support_phone';
                    response = `Obrigado, ${projectData.name}! Qual é o seu número de telefone (com DDD)?`;
                } else if (chatState === 'support_phone') {
                    projectData.phone = input;
                    if (!/^\d{10,11}$/.test(projectData.phone.replace(/\D/g, ''))) {
                        response = 'Por favor, insira um número de telefone válido com DDD (ex.: 16987654321).';
                    } else {
                        chatState = 'support_issue';
                        response = 'Descreva o problema que você está enfrentando.';
                    }
                } else if (chatState === 'support_issue') {
                    projectData.issue = input;
                    chatState = 'initial';
                    const whatsappMessage = `Solicitação de Suporte\nNome: ${encodeURIComponent(projectData.name)}\nTelefone: ${encodeURIComponent(projectData.phone)}\nProblema: ${encodeURIComponent(projectData.issue)}`;
                    const whatsappUrl = `https://wa.me/5516981848861?text=${whatsappMessage}`;
                    window.open(whatsappUrl, '_blank', 'noopener,noreferrer');
                    response = 'Sua solicitação de suporte foi enviada via WhatsApp. Nossa equipe entrará em contato em breve! Deseja reiniciar a conversa?';
                    options = [
                        { label: 'Reiniciar', value: 'Reiniciar' },
                        { label: 'Fechar', value: 'Fechar' }
                    ];
                    projectData = {};
                } else if (input === 'Fechar') {
                    chatbotModal.classList.remove('show');
                    response = '';
                } else if (input === 'Reiniciar') {
                    chatState = 'initial';
                    projectData = {};
                    response = 'Conversa reiniciada! Como posso ajudar? Escolha uma opção:';
                    options = [
                        { label: 'Solicitar Orçamento', value: 'Solicitar Orçamento' },
                        { label: 'Solicitar Suporte', value: 'Solicitar Suporte' }
                    ];
                }

                if (response) {
                    setTimeout(() => {
                        addMessage(response, 'bot', options);
                        isBotResponding = false;
                    }, 1000);
                } else {
                    isBotResponding = false;
                }
            };

            openChatbot.addEventListener('click', () => {
                chatbotModal.classList.toggle('show');
                contactModal.classList.remove('show');
                if (chatbotModal.classList.contains('show') && chatState === 'initial') {
                    addMessage('Olá! Bem-vindo ao Assistente Borges Tech. Como posso ajudar você hoje?', 'bot', [
                        { label: 'Solicitar Orçamento', value: 'Solicitar Orçamento' },
                        { label: 'Solicitar Suporte', value: 'Solicitar Suporte' }
                    ]);
                }
            });

            chatbotSend.addEventListener('click', () => {
                const input = chatbotInput.value.trim();
                if (input) {
                    handleChatbotInput(input);
                    chatbotInput.value = '';
                }
            });

            chatbotInput.addEventListener('keypress', (e) => {
                if (e.key === 'Enter' && chatbotInput.value.trim()) {
                    handleChatbotInput(chatbotInput.value.trim());
                    chatbotInput.value = '';
                }
            });

            chatbotModal.addEventListener('click', (e) => {
                if (e.target === chatbotModal) chatbotModal.classList.remove('show');
            });
        });
    </script>
</body>
</html>
