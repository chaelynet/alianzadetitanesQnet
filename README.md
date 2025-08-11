<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>QNET Argentina | Líderes del Futuro en América</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Open+Sans:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #0056b3;
            --secondary: #00a859;
            --accent: #ff6b00;
            --light: #f8f9fa;
            --dark: #212529;
            --gray: #6c757d;
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Open Sans', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: #f5f7fa;
            overflow-x: hidden;
        }
        
        h1, h2, h3, h4, h5 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            line-height: 1.2;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary), #003d82);
            color: white;
            padding: 15px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo img {
            height: 50px;
            margin-right: 15px;
        }
        
        .logo h1 {
            font-size: 1.8rem;
            margin: 0;
        }
        
        .logo span {
            color: var(--secondary);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 25px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: var(--transition);
            padding: 8px 12px;
            border-radius: 4px;
        }
        
        nav ul li a:hover {
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 86, 179, 0.85), rgba(0, 86, 179, 0.9)), url('https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3') no-repeat center center/cover;
            height: 100vh;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
            padding-top: 80px;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .hero h2 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .hero p {
            font-size: 1.4rem;
            margin-bottom: 30px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .btn {
            display: inline-block;
            background: var(--secondary);
            color: white;
            padding: 15px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: var(--transition);
            border: 2px solid var(--secondary);
            cursor: pointer;
        }
        
        .btn:hover {
            background: transparent;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid white;
            margin-left: 15px;
        }
        
        .btn-outline:hover {
            background: white;
            color: var(--primary);
        }
        
        /* About Section */
        .section {
            padding: 100px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--secondary);
            border-radius: 2px;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: var(--dark);
        }
        
        .about-text p {
            margin-bottom: 20px;
            font-size: 1.1rem;
        }
        
        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
            transition: var(--transition);
        }
        
        .about-image img:hover {
            transform: scale(1.03);
        }
        
        /* Benefits Section */
        .benefits {
            background-color: var(--light);
        }
        
        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .benefit-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
            text-align: center;
            padding: 30px;
        }
        
        .benefit-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .benefit-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .benefit-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        /* History Section */
        .history-timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .history-timeline::before {
            content: '';
            position: absolute;
            top: 0;
            bottom: 0;
            width: 4px;
            background: var(--secondary);
            left: 50%;
            margin-left: -2px;
        }
        
        .timeline-item {
            position: relative;
            margin-bottom: 50px;
            width: 100%;
        }
        
        .timeline-item:nth-child(odd) {
            padding-right: calc(50% + 30px);
            text-align: right;
        }
        
        .timeline-item:nth-child(even) {
            padding-left: calc(50% + 30px);
        }
        
        .timeline-content {
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            position: relative;
        }
        
        .timeline-content::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background: white;
            top: 30px;
            transform: rotate(45deg);
        }
        
        .timeline-item:nth-child(odd) .timeline-content::after {
            right: -10px;
        }
        
        .timeline-item:nth-child(even) .timeline-content::after {
            left: -10px;
        }
        
        .timeline-year {
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 10px;
            font-size: 1.2rem;
        }
        
        .timeline-dot {
            position: absolute;
            width: 20px;
            height: 20px;
            background: var(--secondary);
            border-radius: 50%;
            top: 30px;
            left: 50%;
            transform: translateX(-50%);
        }
        
        /* Leadership Section */
        .leadership-form {
            max-width: 700px;
            margin: 0 auto;
            background: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--dark);
        }
        
        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: var(--transition);
        }
        
        .form-group input:focus,
        .form-group textarea:focus,
        .form-group select:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(0, 86, 179, 0.1);
        }
        
        .form-row {
            display: flex;
            gap: 20px;
        }
        
        .form-row .form-group {
            flex: 1;
        }
        
        /* Chatbot */
        .chatbot-container {
            position: fixed;
            bottom: 30px;
            right: 30px;
            z-index: 1000;
        }
        
        .chatbot-toggle {
            width: 60px;
            height: 60px;
            background: var(--primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            font-size: 1.5rem;
            transition: var(--transition);
        }
        
        .chatbot-toggle:hover {
            background: var(--secondary);
            transform: scale(1.1);
        }
        
        .chatbot {
            position: absolute;
            bottom: 80px;
            right: 0;
            width: 350px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            display: none;
            flex-direction: column;
            height: 500px;
            overflow: hidden;
        }
        
        .chatbot-header {
            background: var(--primary);
            color: white;
            padding: 20px;
            display: flex;
            align-items: center;
        }
        
        .chatbot-header h3 {
            margin: 0;
            font-size: 1.2rem;
        }
        
        .chatbot-header i {
            margin-right: 10px;
        }
        
        .chatbot-messages {
            flex: 1;
            padding: 20px;
            overflow-y: auto;
            display: flex;
            flex-direction: column;
        }
        
        .message {
            max-width: 80%;
            padding: 12px 15px;
            margin-bottom: 15px;
            border-radius: 18px;
            position: relative;
            animation: fadeIn 0.3s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .bot-message {
            background: #f1f5f9;
            align-self: flex-start;
            border-bottom-left-radius: 5px;
        }
        
        .user-message {
            background: var(--primary);
            color: white;
            align-self: flex-end;
            border-bottom-right-radius: 5px;
        }
        
        .chatbot-input {
            display: flex;
            padding: 15px;
            border-top: 1px solid #eee;
        }
        
        .chatbot-input input {
            flex: 1;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 30px;
            outline: none;
        }
        
        .chatbot-input button {
            background: var(--primary);
            color: white;
            border: none;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            margin-left: 10px;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .chatbot-input button:hover {
            background: var(--secondary);
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 60px 0 30px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            font-size: 1.4rem;
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--secondary);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 12px;
        }
        
        .footer-column ul li a {
            color: #ddd;
            text-decoration: none;
            transition: var(--transition);
        }
        
        .footer-column ul li a:hover {
            color: var(--secondary);
            padding-left: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            transition: var(--transition);
        }
        
        .social-links a:hover {
            background: var(--secondary);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            color: #aaa;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .about-content {
                flex-direction: column;
            }
            
            .timeline-item:nth-child(odd) {
                padding-right: 0;
                text-align: left;
                padding-left: calc(50% + 30px);
            }
        }
        
        @media (max-width: 768px) {
            .hero h2 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .btn {
                display: block;
                margin: 15px auto;
                width: 80%;
                max-width: 300px;
            }
            
            .btn-outline {
                margin-left: 0;
            }
            
            nav ul {
                display: none;
                position: absolute;
                top: 70px;
                left: 0;
                width: 100%;
                background: var(--primary);
                flex-direction: column;
                padding: 20px 0;
            }
            
            nav ul.show {
                display: flex;
            }
            
            nav ul li {
                margin: 10px 0;
                text-align: center;
            }
            
            .mobile-menu {
                display: block;
            }
            
            .form-row {
                flex-direction: column;
                gap: 0;
            }
            
            .chatbot {
                width: 300px;
                right: 15px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <h1>QNET <span>ARGENTINA</span></h1>
            </div>
            <div class="mobile-menu">
                <i class="fas fa-bars"></i>
            </div>
            <nav>
                <ul>
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#nosotros">Nosotros</a></li>
                    <li><a href="#beneficios">Beneficios</a></li>
                    <li><a href="#historia">Historia</a></li>
                    <li><a href="#liderazgo">Liderazgo</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="hero-content">
            <h2>Líderes del Futuro en América</h2>
            <p>QNET llega a Argentina como primera oficina oficial en América. Únete a nosotros y lidera el cambio en el mercado multinivel global.</p>
            <div class="hero-buttons">
                <a href="#liderazgo" class="btn">Conviértete en Líder</a>
                <a href="#nosotros" class="btn btn-outline">Descubre Más</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="section" id="nosotros">
        <div class="container">
            <div class="section-title">
                <h2>¿Qué es QNET?</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>La Empresa Multinivel Global</h3>
                    <p>QNET es una empresa multinivel fundada en 1998 por Vijay Eswaran y Joseph Bismark, con presencia en más de 100 países. Ofrecemos productos innovadores en salud, bienestar y estilo de vida.</p>
                    <p>Con más de 25 años de trayectoria, QNET ha generado ingresos estimados en $520 millones anuales y ha revolucionado el modelo de ventas directas a través de tecnología avanzada y productos de calidad.</p>
                    <p>En 2024, QNET ha iniciado oficialmente su expansión en América con Argentina como punto de entrada estratégico, buscando líderes visionarios para liderar esta transformación en el continente.</p>
                    <a href="#historia" class="btn">Nuestra Historia</a>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&h=400&q=80" alt="Equipo QNET">
                </div>
            </div>
        </div>
    </section>

    <!-- Benefits Section -->
    <section class="section benefits" id="beneficios">
        <div class="container">
            <div class="section-title">
                <h2>Beneficios de QNET</h2>
            </div>
            <div class="benefits-grid">
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-wallet"></i>
                    </div>
                    <h3>Ingresos Ilimitados</h3>
                    <p>Modelo de compensación que premia el liderazgo y el crecimiento de tu red con ingresos potencialmente ilimitados.</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-globe-americas"></i>
                    </div>
                    <h3>Expansión Global</h3>
                    <p>Accede a mercados internacionales y oportunidades de negocio en más de 100 países.</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3>Desarrollo de Liderazgo</h3>
                    <p>Programas de formación continua para desarrollar tus habilidades de liderazgo y emprendimiento.</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-calendar-alt"></i>
                    </div>
                    <h3>Eventos Exclusivos</h3>
                    <p>Participa en conferencias internacionales, convenciones y eventos de networking con líderes globales.</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-medal"></i>
                    </div>
                    <h3>Reconocimiento</h3>
                    <p>Oportunidades de viajar, recibir premios y ser reconocido por tu contribución al crecimiento de QNET.</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">
                        <i class="fas fa-hands-helping"></i>
                    </div>
                    <h3>Impacto Social</h3>
                    <p>Participa en iniciativas de responsabilidad social y sostenibilidad ambiental.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- History Section -->
    <section class="section" id="historia">
        <div class="container">
            <div class="section-title">
                <h2>Nuestra Trayectoria</h2>
            </div>
            <div class="history-timeline">
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <div class="timeline-year">1998</div>
                        <p>Fundación de QNET por Vijay Eswaran y Joseph Bismark bajo el grupo QI en Singapur.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <div class="timeline-year">2001</div>
                        <p>Primer V-Convention, evento anual que reúne a líderes de todo el mundo y se convierte en una tradición.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <div class="timeline-year">2014</div>
                        <p>Alianza estratégica con el Manchester City Football Club como patrocinador oficial.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <div class="timeline-year">2021</div>
                        <p>Lanzamiento del programa Green Legacy en colaboración con Ecomatcher para plantar bosques en múltiples países.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <div class="timeline-year">2024</div>
                        <p>Apertura oficial de la primera oficina en Argentina, marcando el inicio de la expansión en América.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Leadership Section -->
    <section class="section" id="liderazgo">
        <div class="container">
            <div class="section-title">
                <h2>¿Eres un Líder del Futuro?</h2>
            </div>
            <div class="leadership-form">
                <form id="leaderForm">
                    <div class="form-row">
                        <div class="form-group">
                            <label for="nombre">Nombre Completo</label>
                            <input type="text" id="nombre" required placeholder="Tu nombre completo">
                        </div>
                        <div class="form-group">
                            <label for="email">Correo Electrónico</label>
                            <input type="email" id="email" required placeholder="tu@email.com">
                        </div>
                    </div>
                    <div class="form-row">
                        <div class="form-group">
                            <label for="telefono">Teléfono</label>
                            <input type="tel" id="telefono" required placeholder="+54 11 1234 5678">
                        </div>
                        <div class="form-group">
                            <label for="ciudad">Ciudad</label>
                            <input type="text" id="ciudad" required placeholder="Buenos Aires">
                        </div>
                    </div>
                    <div class="form-group">
                        <label for="experiencia">Experiencia en Liderazgo</label>
                        <textarea id="experiencia" rows="4" required placeholder="Cuéntanos sobre tu experiencia como líder..."></textarea>
                    </div>
                    <div class="form-group">
                        <label for="motivacion">¿Por qué quieres liderar QNET en América?</label>
                        <textarea id="motivacion" rows="4" required placeholder="Tu motivación para unirte a QNET..."></textarea>
                    </div>
                    <button type="submit" class="btn">Enviar Solicitud</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Chatbot -->
    <div class="chatbot-container">
        <div class="chatbot-toggle" id="chatbotToggle">
            <i class="fas fa-comments"></i>
        </div>
        <div class="chatbot" id="chatbot">
            <div class="chatbot-header">
                <i class="fas fa-robot"></i>
                <h3>Asistente QNET</h3>
            </div>
            <div class="chatbot-messages" id="chatMessages">
                <div class="message bot-message">
                    ¡Hola! Soy tu asistente virtual de QNET Argentina. ¿En qué puedo ayudarte hoy?
                </div>
            </div>
            <div class="chatbot-input">
                <input type="text" id="userInput" placeholder="Escribe tu mensaje...">
                <button id="sendMessage"><i class="fas fa-paper-plane"></i></button>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>QNET Argentina</h3>
                    <p>Primera oficina oficial en América, liderando el futuro del negocio multinivel en el continente.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Enlaces Rápidos</h3>
                    <ul>
                        <li><a href="#inicio">Inicio</a></li>
                        <li><a href="#nosotros">Nosotros</a></li>
                        <li><a href="#beneficios">Beneficios</a></li>
                        <li><a href="#historia">Historia</a></li>
                        <li><a href="#liderazgo">Liderazgo</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Productos</h3>
                    <ul>
                        <li><a href="#">Bienestar y Salud</a></li>
                        <li><a href="#">Tecnología Cuántica</a></li>
                        <li><a href="#">Electrodomésticos</a></li>
                        <li><a href="#">Accesorios de Moda</a></li>
                        <li><a href="#">Lanzamientos 2024</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contacto</h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> Buenos Aires, Argentina</li>
                        <li><i class="fas fa-phone"></i> +54 11 1234 5678</li>
                        <li><i class="fas fa-envelope"></i> info@qnetargentina.com</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2024 QNET Argentina. Todos los derechos reservados. | Primera Oficina Oficial en América</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            document.querySelector('nav ul').classList.toggle('show');
        });

        // Smooth Scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
                
                // Close mobile menu if open
                document.querySelector('nav ul').classList.remove('show');
            });
        });

        // Form Submission
        document.getElementById('leaderForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const nombre = document.getElementById('nombre').value;
            
            // Show success message
            alert(`¡Gracias ${nombre}! Hemos recibido tu solicitud. Un representante de QNET se contactará contigo pronto.`);
            
            // Reset form
            this.reset();
        });

        // Chatbot Functionality
        const chatbotToggle = document.getElementById('chatbotToggle');
        const chatbot = document.getElementById('chatbot');
        const chatMessages = document.getElementById('chatMessages');
        const userInput = document.getElementById('userInput');
        const sendMessage = document.getElementById('sendMessage');

        chatbotToggle.addEventListener('click', () => {
            chatbot.style.display = chatbot.style.display === 'flex' ? 'none' : 'flex';
            if (chatbot.style.display === 'flex') {
                userInput.focus();
            }
        });

        function addMessage(message, isUser = false) {
            const messageDiv = document.createElement('div');
            messageDiv.classList.add('message');
            messageDiv.classList.add(isUser ? 'user-message' : 'bot-message');
            messageDiv.textContent = message;
            chatMessages.appendChild(messageDiv);
            chatMessages.scrollTop = chatMessages.scrollHeight;
        }

        function getBotResponse(userMessage) {
            const lowerMessage = userMessage.toLowerCase();
            
            if (lowerMessage.includes('hola') || lowerMessage.includes('buenos dias')) {
                return '¡Hola! Bienvenido a QNET Argentina. ¿En qué puedo ayudarte hoy?';
            } else if (lowerMessage.includes('beneficio') || lowerMessage.includes('ganar')) {
                return 'QNET ofrece ingresos ilimitados a través de nuestro modelo de compensación. Puedes ganar por tus ventas directas y por el crecimiento de tu red.';
            } else if (lowerMessage.includes('producto') || lowerMessage.includes('catalogo')) {
                return 'Tenemos productos innovadores en salud, bienestar, tecnología cuántica y accesorios de moda. ¿Te interesa algún tipo específico?';
            } else if (lowerMessage.includes('lider') || lowerMessage.includes('oportunidad')) {
                return '¡Perfecto! Estamos buscando líderes visionarios para liderar QNET en América. Puedes aplicar en la sección "Liderazgo" de nuestra página.';
            } else if (lowerMessage.includes('manchester') || lowerMessage.includes('futbol')) {
                return '¡Sí! QNET es patrocinador oficial del Manchester City desde 2014. Esta alianza nos ha dado gran visibilidad global.';
            } else if (lowerMessage.includes('argentina') || lowerMessage.includes('oficina')) {
                return 'QNET ha abierto oficialmente su primera oficina en Argentina en 2024, marcando el inicio de nuestra expansión en América.';
            } else if (lowerMessage.includes('gracias')) {
                return '¡De nada! ¿Hay algo más en lo que pueda ayudarte?';
            } else {
                const responses = [
                    'QNET tiene más de 25 años de trayectoria global con presencia en más de 100 países.',
                    'Nuestro modelo de negocio se basa en ventas directas y desarrollo de redes de distribuidores.',
                    '¿Te gustaría conocer más sobre nuestros productos innovadores?',
                    '¿Tienes alguna pregunta específica sobre oportunidades en QNET?',
                    'Puedes aplicar para ser líder en la sección "Liderazgo" de nuestra página.'
                ];
                return responses[Math.floor(Math.random() * responses.length)];
            }
        }

        sendMessage.addEventListener('click', () => {
            const message = userInput.value.trim();
            if (message) {
                addMessage(message, true);
                userInput.value = '';
                
                // Simulate bot thinking
                setTimeout(() => {
                    const botResponse = getBotResponse(message);
                    addMessage(botResponse);
                }, 1000);
            }
        });

        userInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') {
                sendMessage.click();
            }
        });

        // Initial bot message after a delay
        setTimeout(() => {
            addMessage('¡Bienvenido a QNET Argentina! ¿Te gustaría conocer más sobre oportunidades de liderazgo en América?');
        }, 2000);
    </script>
</body>
</html>
