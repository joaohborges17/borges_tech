<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Borges Tech Solution - Criação de Aplicativos e Sites</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        body {
            margin: 0;
            font-family: 'Roboto', sans-serif;
            background-color: #f8f9fa;
            color: #333;
        }
        header {
            background: #0a1a2f;
            color: #fff;
            padding: 15px 40px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        header img {
            height: 60px;
        }
        nav ul {
            list-style: none;
            display: flex;
            gap: 25px;
            margin: 0;
            padding: 0;
        }
        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        nav ul li a:hover {
            color: #00ff99;
        }
        .whatsapp-header {
            margin-left: 20px;
            font-size: 22px;
        }
        .whatsapp-header a {
            color: #25d366;
            text-decoration: none;
        }
        .hero {
            background: linear-gradient(rgba(10, 26, 47, 0.8), rgba(10, 26, 47, 0.8)), url('https://images.unsplash.com/photo-1526378722484-bd91ca387e72') center/cover;
            color: #fff;
            text-align: center;
            padding: 120px 20px;
        }
        .hero h1 {
            font-size: 48px;
            margin-bottom: 15px;
        }
        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
        }
        .hero a {
            background: #00ff99;
            color: #0a1a2f;
            padding: 15px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: 0.3s;
        }
        .hero a:hover {
            background: #00cc7a;
        }
        .services {
            padding: 60px 20px;
            text-align: center;
        }
        .services h2 {
            font-size: 32px;
            margin-bottom: 40px;
        }
        .service-cards, .portfolio-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            max-width: 1100px;
            margin: auto;
        }
        .card {
            background: #fff;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        .card:hover {
            transform: translateY(-8px);
        }
        .card i {
            font-size: 40px;
            color: #0a1a2f;
            margin-bottom: 15px;
        }
        footer {
            background: #0a1a2f;
            color: #fff;
            text-align: center;
            padding: 25px 10px;
            margin-top: 50px;
        }
        /* Botão WhatsApp flutuante */
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
            transition: transform 0.3s;
        }
        .whatsapp-float:hover {
            transform: scale(1.1);
        }
        @media (max-width: 768px) {
            .hero h1 { font-size: 32px; }
            .hero p { font-size: 16px; }
            nav ul { flex-direction: column; gap: 10px; }
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
                <li class="whatsapp-header">
                    <a href="https://wa.me/55169818488461?text=Ol%C3%A1%2C%20gostaria%20de%20mais%20informa%C3%A7%C3%B5es%20sobre%20seus%20softwares." target="_blank">
                        <i class="fab fa-whatsapp"></i>
                    </a>
                </li>
            </ul>
        </nav>
    </header>

    <section class="hero" id="home">
        <h1>Criação de Aplicativos e Sites Profissionais</h1>
        <p>Desenvolvemos soluções digitais sob medida para empresas em Ribeirão Preto e região.</p>
        <a href="#servicos">Nossos Serviços</a>
    </section>

    <section class="services" id="servicos">
        <h2>O que fazemos</h2>
        <div class="service-cards">
            <div class="card">
                <i class="fas fa-mobile-alt"></i>
                <h3>Desenvolvimento de Aplicativos</h3>
                <p>Aplicativos modernos para Android e iOS, feitos para potencializar o seu negócio.</p>
            </div>
            <div class="card">
                <i class="fas fa-laptop-code"></i>
                <h3>Criação de Sites Profissionais</h3>
                <p>Sites responsivos, rápidos e com design atual para empresas de todos os portes.</p>
            </div>
            <div class="card">
                <i class="fas fa-briefcase"></i>
                <h3>Soluções Empresariais Digitais</h3>
                <p>Sistemas sob medida para gestão, automação e inovação nos processos do seu negócio.</p>
            </div>
        </div>
    </section>

    <section class="services" id="portfolio">
        <h2>Cases de Sucesso</h2>
        <div class="portfolio-cards">
            <div class="card">
                <i class="fas fa-store"></i>
                <h3>E-commerce Local</h3>
                <p>Desenvolvemos uma loja virtual para uma rede de comércio regional, aumentando suas vendas em 60%.</p>
            </div>
            <div class="card">
                <i class="fas fa-hospital"></i>
                <h3>Aplicativo de Saúde</h3>
                <p>Aplicativo móvel para clínicas, permitindo agendamento online e melhorando a experiência do paciente.</p>
            </div>
            <div class="card">
                <i class="fas fa-building"></i>
                <h3>Site Corporativo</h3>
                <p>Website institucional moderno para uma empresa de engenharia, fortalecendo sua presença digital.</p>
            </div>
        </div>
    </section>

    <footer id="contato">
        <p>&copy; 2025 Borges Tech Solution - Ribeirão Preto. Todos os direitos reservados.</p>
    </footer>

    <!-- WhatsApp flutuante -->
    <a href="https://wa.me/55169818488461?text=Ol%C3%A1%2C%20gostaria%20de%20mais%20informa%C3%A7%C3%B5es%20sobre%20seus%20softwares." class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>
</body>
</html>
