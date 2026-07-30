<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adauto Rodrigues | Advocacia Trabalhista Especializada</title>
    <!-- Google Fonts & Font Awesome Icons -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@500;700;900&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        /* ==========================================================================
           1. VARIÁVEIS GLOBAIS E RESET
           ========================================================================== */
        :root {
            --primary-navy: #0B132B;
            --secondary-navy: #1C2541;
            --accent-gold: #C5A059;
            --accent-gold-hover: #D4AF37;
            --text-dark: #1E293B;
            --text-muted: #64748B;
            --bg-light: #F8FAFC;
            --white: #FFFFFF;
            --border-color: #E2E8F0;
            --success-color: #10B981;
            --font-serif: 'Cinzel', serif;
            --font-sans: 'Plus Jakarta Sans', sans-serif;
            --shadow-sm: 0 2px 4px rgba(0,0,0,0.05);
            --shadow-md: 0 10px 25px rgba(0,0,0,0.08);
            --shadow-lg: 0 20px 40px rgba(0,0,0,0.15);
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            font-size: 16px;
        }

        body {
            font-family: var(--font-sans);
            color: var(--text-dark);
            background-color: var(--bg-light);
            line-height: 1.6;
            overflow-x: hidden;
        }

        a {
            text-decoration: none;
            color: inherit;
            transition: var(--transition);
        }

        ul {
            list-style: none;
        }

        /* ==========================================================================
           2. COMPONENTES UTILITÁRIOS
           ========================================================================== */
        .container {
            width: 90%;
            max-width: 1280px;
            margin: 0 auto;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            padding: 14px 28px;
            font-size: 0.95rem;
            font-weight: 600;
            border-radius: 6px;
            cursor: pointer;
            transition: var(--transition);
            border: none;
            outline: none;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .btn-gold {
            background: linear-gradient(135deg, var(--accent-gold), #B38E46);
            color: var(--white);
            box-shadow: 0 4px 15px rgba(197, 160, 89, 0.3);
        }

        .btn-gold:hover {
            background: linear-gradient(135deg, #D4AF37, var(--accent-gold));
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(197, 160, 89, 0.4);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--accent-gold);
            color: var(--accent-gold);
        }

        .btn-outline:hover {
            background: var(--accent-gold);
            color: var(--white);
            transform: translateY(-2px);
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-subtitle {
            color: var(--accent-gold);
            font-weight: 700;
            text-transform: uppercase;
            font-size: 0.85rem;
            letter-spacing: 2px;
            display: block;
            margin-bottom: 8px;
        }

        .section-title {
            font-family: var(--font-serif);
            font-size: 2.3rem;
            color: var(--primary-navy);
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 3px;
            background-color: var(--accent-gold);
            margin: 12px auto 0 auto;
            border-radius: 2px;
        }

        /* ==========================================================================
           3. NAVBAR & CABEÇALHO
           ========================================================================== */
        .top-bar {
            background-color: var(--primary-navy);
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.85rem;
            padding: 8px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.08);
        }

        .top-bar-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .top-info {
            display: flex;
            gap: 20px;
        }

        .top-info i {
            color: var(--accent-gold);
            margin-right: 5px;
        }

        .navbar {
            background-color: var(--secondary-navy);
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: var(--shadow-md);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            color: var(--white);
        }

        .logo i {
            font-size: 2rem;
            color: var(--accent-gold);
        }

        .logo-text h1 {
            font-family: var(--font-serif);
            font-size: 1.4rem;
            letter-spacing: 1px;
            line-height: 1.1;
        }

        .logo-text span {
            font-size: 0.75rem;
            color: var(--accent-gold);
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .nav-links {
            display: flex;
            gap: 25px;
            align-items: center;
        }

        .nav-links a {
            color: var(--white);
            font-weight: 500;
            font-size: 0.95rem;
            position: relative;
        }

        .nav-links a:hover {
            color: var(--accent-gold);
        }

        .nav-auth-btn {
            background-color: rgba(197, 160, 89, 0.15);
            border: 1px solid var(--accent-gold);
            color: var(--accent-gold) !important;
            padding: 8px 18px;
            border-radius: 4px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .nav-auth-btn:hover {
            background-color: var(--accent-gold);
            color: var(--white) !important;
        }

        .mobile-menu-btn {
            display: none;
            color: var(--white);
            font-size: 1.5rem;
            background: none;
            border: none;
            cursor: pointer;
        }

        /* ==========================================================================
           4. HERO SECTION
           ========================================================================== */
        .hero {
            background: linear-gradient(135deg, rgba(11, 19, 43, 0.92) 0%, rgba(28, 37, 65, 0.88) 100%), 
                        url('https://images.unsplash.com/photo-1589829545856-d10d557cf95f?auto=format&fit=crop&w=1920&q=80') center/cover no-repeat;
            color: var(--white);
            padding: 120px 0 100px 0;
            position: relative;
        }

        .hero-grid {
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 50px;
            align-items: center;
        }

        .hero-badge {
            display: inline-block;
            background: rgba(197, 160, 89, 0.2);
            border: 1px solid var(--accent-gold);
            color: var(--accent-gold);
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 20px;
            text-transform: uppercase;
        }

        .hero-title {
            font-family: var(--font-serif);
            font-size: 3.2rem;
            line-height: 1.2;
            margin-bottom: 20px;
        }

        .hero-title span {
            color: var(--accent-gold);
        }

        .hero-description {
            font-size: 1.1rem;
            color: rgba(255, 255, 255, 0.85);
            margin-bottom: 35px;
            max-width: 600px;
        }

        .hero-actions {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .hero-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 12px;
            box-shadow: var(--shadow-lg);
        }

        .hero-card h3 {
            font-family: var(--font-serif);
            color: var(--accent-gold);
            font-size: 1.4rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .quick-features-list {
            margin-top: 20px;
        }

        .quick-features-list li {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 12px;
            font-size: 0.95rem;
            color: rgba(255, 255, 255, 0.9);
        }

        .quick-features-list i {
            color: var(--accent-gold);
        }

        /* ==========================================================================
           5. FERRAMENTA INTERATIVA: CALCULADORA TRABALHISTA
           ========================================================================== */
        .calculator-section {
            padding: 80px 0;
            background-color: var(--white);
        }

        .calc-wrapper {
            background: var(--bg-light);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 40px;
            box-shadow: var(--shadow-md);
        }

        .calc-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            font-weight: 600;
            margin-bottom: 8px;
            color: var(--primary-navy);
            font-size: 0.9rem;
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid var(--border-color);
            border-radius: 6px;
            font-size: 1rem;
            font-family: var(--font-sans);
            transition: var(--transition);
        }

        .form-control:focus {
            outline: none;
            border-color: var(--accent-gold);
            box-shadow: 0 0 0 3px rgba(197, 160, 89, 0.15);
        }

        .calc-results {
            background: var(--primary-navy);
            color: var(--white);
            padding: 30px;
            border-radius: 8px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .calc-results h4 {
            font-family: var(--font-serif);
            color: var(--accent-gold);
            font-size: 1.3rem;
            margin-bottom: 20px;
            border-bottom: 1px solid rgba(255,255,255,0.1);
            padding-bottom: 10px;
        }

        .result-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 12px;
            font-size: 0.95rem;
            border-bottom: 1px dashed rgba(255,255,255,0.1);
            padding-bottom: 8px;
        }

        .result-total {
            margin-top: 20px;
            padding-top: 15px;
            border-top: 2px solid var(--accent-gold);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .result-total span {
            font-size: 1.2rem;
            font-weight: 700;
        }

        .result-total .total-value {
            font-size: 1.8rem;
            color: var(--accent-gold);
            font-family: var(--font-serif);
        }

        /* ==========================================================================
           6. ÁREAS DE ATUAÇÃO (SERVIÇOS TRABALHISTAS)
           ========================================================================== */
        .services-section {
            padding: 100px 0;
            background-color: var(--bg-light);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }

        .service-card {
            background: var(--white);
            border-radius: 10px;
            padding: 35px;
            border: 1px solid var(--border-color);
            transition: var(--transition);
            position: relative;
            top: 0;
        }

        .service-card:hover {
            top: -8px;
            box-shadow: var(--shadow-md);
            border-color: var(--accent-gold);
        }

        .service-icon {
            width: 60px;
            height: 60px;
            background: rgba(197, 160, 89, 0.1);
            color: var(--accent-gold);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.6rem;
            margin-bottom: 25px;
        }

        .service-card h3 {
            font-family: var(--font-serif);
            font-size: 1.35rem;
            color: var(--primary-navy);
            margin-bottom: 12px;
        }

        .service-card p {
            color: var(--text-muted);
            font-size: 0.95rem;
            margin-bottom: 20px;
        }

        .service-list {
            list-style: none;
            padding-top: 15px;
            border-top: 1px solid var(--border-color);
        }

        .service-list li {
            font-size: 0.88rem;
            color: var(--text-dark);
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .service-list i {
            color: var(--accent-gold);
            font-size: 0.75rem;
        }

        /* ==========================================================================
           7. SOBRE O ADVOGADO
           ========================================================================== */
        .about-section {
            padding: 100px 0;
            background-color: var(--white);
        }

        .about-grid {
            display: grid;
            grid-template-columns: 0.9fr 1.1fr;
            gap: 60px;
            align-items: center;
        }

        .about-image-wrapper {
            position: relative;
        }

        .about-image-wrapper img {
            width: 100%;
            border-radius: 10px;
            box-shadow: var(--shadow-lg);
            display: block;
        }

        .experience-badge {
            position: absolute;
            bottom: -20px;
            right: -20px;
            background: var(--primary-navy);
            color: var(--white);
            padding: 25px;
            border-radius: 8px;
            border-left: 5px solid var(--accent-gold);
            box-shadow: var(--shadow-md);
            text-align: center;
        }

        .experience-badge .number {
            font-family: var(--font-serif);
            font-size: 2.2rem;
            color: var(--accent-gold);
            font-weight: 700;
            line-height: 1;
        }

        .experience-badge .text {
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-top: 5px;
        }

        .about-content h2 {
            font-family: var(--font-serif);
            font-size: 2.2rem;
            color: var(--primary-navy);
            margin-bottom: 15px;
        }

        .about-content .oab-number {
            color: var(--accent-gold);
            font-weight: 700;
            margin-bottom: 20px;
            display: block;
            letter-spacing: 1px;
        }

        .about-content p {
            color: var(--text-muted);
            margin-bottom: 20px;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin-top: 30px;
            padding-top: 30px;
            border-top: 1px solid var(--border-color);
        }

        .stat-item h4 {
            font-family: var(--font-serif);
            font-size: 1.8rem;
            color: var(--primary-navy);
        }

        .stat-item p {
            font-size: 0.85rem;
            margin-bottom: 0;
        }

        /* ==========================================================================
           8. ARTIGOS / BLOG TRABALHISTA
           ========================================================================== */
        .blog-section {
            padding: 100px 0;
            background-color: var(--bg-light);
        }

        .blog-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }

        .blog-card {
            background: var(--white);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: var(--shadow-sm);
            border: 1px solid var(--border-color);
            transition: var(--transition);
        }

        .blog-card:hover {
            box-shadow: var(--shadow-md);
            transform: translateY(-5px);
        }

        .blog-img {
            height: 200px;
            background-size: cover;
            background-position: center;
        }

        .blog-content {
            padding: 25px;
        }

        .blog-date {
            font-size: 0.8rem;
            color: var(--accent-gold);
            font-weight: 600;
            text-transform: uppercase;
            margin-bottom: 8px;
            display: block;
        }

        .blog-title {
            font-family: var(--font-serif);
            font-size: 1.2rem;
            color: var(--primary-navy);
            margin-bottom: 12px;
            line-height: 1.4;
        }

        .blog-excerpt {
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-bottom: 20px;
        }

        .blog-link {
            color: var(--primary-navy);
            font-weight: 700;
            font-size: 0.85rem;
            display: flex;
            align-items: center;
            gap: 8px;
            cursor: pointer;
        }

        .blog-link:hover {
            color: var(--accent-gold);
        }

        /* ==========================================================================
           9. PERGUNTAS FREQUENTES (FAQ ACCORDION)
           ========================================================================== */
        .faq-section {
            padding: 100px 0;
            background-color: var(--white);
        }

        .faq-container {
            max-width: 800px;
            margin: 0 auto;
        }

        .faq-item {
            border: 1px solid var(--border-color);
            border-radius: 8px;
            margin-bottom: 15px;
            overflow: hidden;
        }

        .faq-question {
            width: 100%;
            padding: 20px;
            text-align: left;
            background: var(--white);
            border: none;
            outline: none;
            font-family: var(--font-sans);
            font-weight: 600;
            font-size: 1.05rem;
            color: var(--primary-navy);
            display: flex;
            justify-content: space-between;
            align-items: center;
            cursor: pointer;
            transition: var(--transition);
        }

        .faq-question:hover {
            background-color: var(--bg-light);
        }

        .faq-answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-out;
            background-color: var(--bg-light);
        }

        .faq-answer-content {
            padding: 20px;
            color: var(--text-muted);
            font-size: 0.95rem;
            border-top: 1px solid var(--border-color);
        }

        .faq-icon {
            transition: transform 0.3s ease;
            color: var(--accent-gold);
        }

        .faq-item.active .faq-icon {
            transform: rotate(180deg);
        }

        /* ==========================================================================
           10. MODAL DE LOGIN (CPF, GMAIL, NOME) & PORTAL DO CLIENTE
           ========================================================================== */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(11, 19, 43, 0.85);
            backdrop-filter: blur(5px);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 2000;
            opacity: 0;
            visibility: hidden;
            transition: var(--transition);
        }

        .modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .modal-box {
            background: var(--white);
            width: 90%;
            max-width: 480px;
            border-radius: 12px;
            box-shadow: var(--shadow-lg);
            overflow: hidden;
            position: relative;
            transform: translateY(-20px);
            transition: var(--transition);
        }

        .modal-overlay.active .modal-box {
            transform: translateY(0);
        }

        .modal-close {
            position: absolute;
            top: 15px;
            right: 20px;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--text-muted);
            cursor: pointer;
            z-index: 10;
        }

        .modal-header {
            background: var(--primary-navy);
            color: var(--white);
            padding: 30px 20px 20px 20px;
            text-align: center;
        }

        .modal-header h3 {
            font-family: var(--font-serif);
            color: var(--accent-gold);
            font-size: 1.5rem;
        }

        .modal-header p {
            font-size: 0.85rem;
            color: rgba(255,255,255,0.7);
            margin-top: 5px;
        }

        .modal-body {
            padding: 30px;
        }

        .login-tabs {
            display: flex;
            border-bottom: 2px solid var(--border-color);
            margin-bottom: 25px;
        }

        .tab-btn {
            flex: 1;
            padding: 10px;
            background: none;
            border: none;
            font-family: var(--font-sans);
            font-weight: 600;
            font-size: 0.9rem;
            color: var(--text-muted);
            cursor: pointer;
            border-bottom: 2px solid transparent;
            margin-bottom: -2px;
            transition: var(--transition);
        }

        .tab-btn.active {
            color: var(--accent-gold);
            border-bottom-color: var(--accent-gold);
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        .btn-google {
            width: 100%;
            background: var(--white);
            border: 1px solid var(--border-color);
            color: var(--text-dark);
            padding: 12px;
            border-radius: 6px;
            font-weight: 600;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            cursor: pointer;
            transition: var(--transition);
            margin-bottom: 15px;
        }

        .btn-google:hover {
            background-color: #F1F5F9;
        }

        .divider {
            text-align: center;
            margin: 20px 0;
            position: relative;
        }

        .divider::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 0;
            width: 100%;
            height: 1px;
            background: var(--border-color);
        }

        .divider span {
            background: var(--white);
            padding: 0 10px;
            position: relative;
            font-size: 0.8rem;
            color: var(--text-muted);
        }

        /* PAINEL DO CLIENTE LOGADO (DASHBOARD SIMULADO) */
        .client-dashboard {
            display: none;
            padding: 30px;
        }

        .client-dashboard.active {
            display: block;
        }

        .user-welcome {
            background: var(--bg-light);
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
            border-left: 4px solid var(--accent-gold);
        }

        .process-status-tracker {
            margin-top: 20px;
        }

        .status-step {
            display: flex;
            gap: 15px;
            margin-bottom: 15px;
            position: relative;
        }

        .status-step::before {
            content: '';
            position: absolute;
            left: 12px;
            top: 25px;
            width: 2px;
            height: calc(100% + 5px);
            background: var(--border-color);
        }

        .status-step:last-child::before {
            display: none;
        }

        .step-icon {
            width: 26px;
            height: 26px;
            border-radius: 50%;
            background: var(--border-color);
            color: var(--white);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.75rem;
            z-index: 1;
        }

        .status-step.completed .step-icon {
            background: var(--success-color);
        }

        .status-step.current .step-icon {
            background: var(--accent-gold);
        }

        .step-info h5 {
            font-size: 0.95rem;
            color: var(--primary-navy);
        }

        .step-info p {
            font-size: 0.8rem;
            color: var(--text-muted);
        }

        /* ==========================================================================
           11. SEÇÃO DE CONTATO E AGENDAMENTO
           ========================================================================== */
        .contact-section {
            padding: 100px 0;
            background-color: var(--primary-navy);
            color: var(--white);
        }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
        }

        .contact-info-side h2 {
            font-family: var(--font-serif);
            font-size: 2.2rem;
            color: var(--accent-gold);
            margin-bottom: 20px;
        }

        .contact-detail-item {
            display: flex;
            align-items: flex-start;
            gap: 20px;
            margin-bottom: 25px;
        }

        .contact-detail-item i {
            width: 45px;
            height: 45px;
            background: rgba(197, 160, 89, 0.15);
            border: 1px solid var(--accent-gold);
            color: var(--accent-gold);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            flex-shrink: 0;
        }

        .contact-detail-item h4 {
            font-size: 1.1rem;
            margin-bottom: 4px;
        }

        .contact-detail-item p {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.95rem;
        }

        .contact-form-side {
            background: var(--white);
            padding: 40px;
            border-radius: 12px;
            color: var(--text-dark);
        }

        .contact-form-side h3 {
            font-family: var(--font-serif);
            color: var(--primary-navy);
            font-size: 1.5rem;
            margin-bottom: 20px;
        }

        /* ==========================================================================
           12. RODAPÉ (FOOTER)
           ========================================================================== */
        footer {
            background-color: #060B18;
            color: rgba(255, 255, 255, 0.6);
            padding: 70px 0 30px 0;
            font-size: 0.9rem;
            border-top: 1px solid rgba(255,255,255,0.05);
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 1.5fr 1fr 1fr 1.2fr;
            gap: 40px;
            margin-bottom: 50px;
        }

        .footer-col h4 {
            color: var(--white);
            font-family: var(--font-serif);
            font-size: 1.1rem;
            margin-bottom: 20px;
            position: relative;
        }

        .footer-col h4::after {
            content: '';
            display: block;
            width: 30px;
            height: 2px;
            background: var(--accent-gold);
            margin-top: 8px;
        }

        .footer-col ul li {
            margin-bottom: 10px;
        }

        .footer-col ul li a:hover {
            color: var(--accent-gold);
        }

        .social-links {
            display: flex;
            gap: 12px;
            margin-top: 20px;
        }

        .social-links a {
            width: 38px;
            height: 38px;
            background: rgba(255,255,255,0.08);
            color: var(--white);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }

        .social-links a:hover {
            background: var(--accent-gold);
            color: var(--white);
        }

        .footer-bottom {
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.08);
            text-align: center;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
        }

        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 60px;
            height: 60px;
            background-color: #25D366;
            color: var(--white);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            box-shadow: var(--shadow-lg);
            z-index: 999;
            transition: var(--transition);
        }

        .whatsapp-float:hover {
            transform: scale(1.1);
        }

        /* ==========================================================================
           13. RESPONSIVIDADE (MEDIA QUERIES)
           ========================================================================== */
        @media (max-width: 992px) {
            .hero-grid, .calc-grid, .about-grid, .contact-grid {
                grid-template-columns: 1fr;
            }

            .hero-title {
                font-size: 2.5rem;
            }

            .footer-grid {
                grid-template-columns: 1fr 1fr;
            }

            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: var(--secondary-navy);
                flex-direction: column;
                padding: 20px;
                box-shadow: var(--shadow-md);
            }

            .nav-links.active {
                display: flex;
            }

            .mobile-menu-btn {
                display: block;
            }
        }

        @media (max-width: 576px) {
            .top-bar {
                display: none;
            }

            .hero-title {
                font-size: 2rem;
            }

            .footer-grid {
                grid-template-columns: 1fr;
            }

            .footer-bottom {
                flex-direction: column;
                text-align: center;
            }
        }
    </style>
</head>
<body>

    <!-- TOP BAR DE INFORMAÇÕES -->
    <div class="top-bar">
        <div class="container top-bar-content">
            <div class="top-info">
                <span><i class="fa-solid fa-phone"></i> (11) 98765-4321</span>
                <span><i class="fa-solid fa-envelope"></i> contato@adautorodrigues.adv.br</span>
                <span><i class="fa-solid fa-location-dot"></i> Av. Paulista, 1000 - São Paulo/SP</span>
            </div>
            <div>
                <span><i class="fa-solid fa-clock"></i> Segunda a Sexta: 08h às 18h</span>
            </div>
        </div>
    </div>

    <!-- NAVBAR PRINCIPAL -->
    <nav class="navbar">
        <div class="container nav-container">
            <a href="#" class="logo">
                <i class="fa-solid fa-scale-balanced"></i>
                <div class="logo-text">
                    <h1>ADAUTO RODRIGUES</h1>
                    <span>Advocacia Trabalhista</span>
                </div>
            </a>

            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fa-solid fa-bars"></i>
            </button>

            <ul class="nav-links" id="navLinks">
                <li><a href="#inicio">Início</a></li>
                <li><a href="#calculadora">Simulador</a></li>
                <li><a href="#servicos">Áreas de Atuação</a></li>
                <li><a href="#sobre">O Advogado</a></li>
                <li><a href="#artigos">Direitos</a></li>
                <li><a href="#faq">FAQ</a></li>
                <li><a href="#contato">Contato</a></li>
                <li>
                    <a href="javascript:void(0)" class="nav-auth-btn" id="openAuthModalBtn">
                        <i class="fa-solid fa-user-lock"></i> Área do Cliente
                    </a>
                </li>
            </ul>
        </div>
    </nav>

    <!-- HERO SECTION -->
    <section class="hero" id="inicio">
        <div class="container hero-grid">
            <div class="hero-text-side">
                <span class="hero-badge"><i class="fa-solid fa-award"></i> Defesa Especializada do Trabalhador</span>
                <h1 class="hero-title">Protegendo seus <span>Direitos Trabalhistas</span> com Excelência e Agilidade.</h1>
                <p class="hero-description">
                    Atuação focada na garantia integral das suas verbas rescisórias, horas extras, insalubridade, reparação por acidentes e assédio no ambiente de trabalho.
                </p>
                <div class="hero-actions">
                    <a href="#calculadora" class="btn btn-gold"><i class="fa-solid fa-calculator"></i> Simular Rescisão</a>
                    <a href="#contato" class="btn btn-outline"><i class="fa-solid fa-comments"></i> Falar com Especialista</a>
                </div>
            </div>

            <div class="hero-card">
                <h3><i class="fa-solid fa-shield-halved"></i> Como podemos ajudar hoje?</h3>
                <p style="color: rgba(255,255,255,0.8); font-size: 0.95rem;">
                    Se você foi demitido, sofreu abusos na empresa ou não recebeu seus direitos corretamente, conte com uma análise técnica minuciosa.
                </p>
                <ul class="quick-features-list">
                    <li><i class="fa-solid fa-circle-check"></i> Análise de demissão sem justa causa</li>
                    <li><i class="fa-solid fa-circle-check"></i> Pedido de Rescisão Indireta</li>
                    <li><i class="fa-solid fa-circle-check"></i> Cobrança de Horas Extras e FGTS</li>
                    <li><i class="fa-solid fa-circle-check"></i> Atendimento 100% Online e Presencial</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- CALCULADORA TRABALHISTA INTERATIVA -->
    <section class="calculator-section" id="calculadora">
        <div class="container">
            <div class="section-header">
                <span class="section-subtitle">Simulador Gratuito</span>
                <h2 class="section-title">Calcule Estimativa das Suas Verbas</h2>
            </div>

            <div class="calc-wrapper">
                <div class="calc-grid">
                    <div class="calc-inputs">
                        <div class="form-group">
                            <label for="salarioBruto">Último Salário Bruto (R$)</label>
                            <input type="number" id="salarioBruto" class="form-control" placeholder="Ex: 3500.00" value="3000">
                        </div>

                        <div class="form-group">
                            <label for="mesesTrabalhados">Tempo Trabalhado (em meses)</label>
                            <input type="number" id="mesesTrabalhados" class="form-control" placeholder="Ex: 24" value="12">
                        </div>

                        <div class="form-group">
                            <label for="motivoSaida">Motivo do Desligamento</label>
                            <select id="motivoSaida" class="form-control">
                                <option value="semJustaCausa">Demissão Sem Justa Causa</option>
                                <option value="rescisaoIndireta">Rescisão Indireta (Culpa do Empregador)</option>
                                <option value="pedidoDemissao">Pedido de Demissão</option>
                                <option value="justaCausa">Demissão Por Justa Causa</option>
                            </select>
                        </div>

                        <div class="form-group">
                            <label for="avisoPrevio">Aviso Prévio</label>
                            <select id="avisoPrevio" class="form-control">
                                <option value="indenizado">Indenizado pela Empresa</option>
                                <option value="trabalhado">Trabalhado</option>
                            </select>
                        </div>

                        <button type="button" class="btn btn-gold" style="width: 100%;" onclick="calcularRescisao()">
                            <i class="fa-solid fa-calculator"></i> Calcular Agora
                        </button>
                    </div>

                    <div class="calc-results">
                        <div>
                            <h4><i class="fa-solid fa-receipt"></i> Estimativa do Resultado</h4>
                            <div class="result-item">
                                <span>Aviso Prévio Indenizado:</span>
                                <strong id="resAviso">R$ 0,00</strong>
                            </div>
                            <div class="result-item">
                                <span>13º Salário Proporcional:</span>
                                <strong id="res13">R$ 0,00</strong>
                            </div>
                            <div class="result-item">
                                <span>Férias Proporcionais + 1/3:</span>
                                <strong id="resFerias">R$ 0,00</strong>
                            </div>
                            <div class="result-item">
                                <span>Multa de 40% do FGTS (Est.):</span>
                                <strong id="resFGTS">R$ 0,00</strong>
                            </div>
                        </div>

                        <div class="result-total">
                            <span>Total Estimado:</span>
                            <div class="total-value" id="resTotal">R$ 0,00</div>
                        </div>
                        <p style="font-size: 0.75rem; color: rgba(255,255,255,0.5); margin-top: 10px;">
                            *Esta simulação possui caráter meramente ilustrativo. Para valores exatos com reflexos e horas extras, agende uma consulta formal.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ÁREAS DE ATUAÇÃO -->
    <section class="services-section" id="servicos">
        <div class="container">
            <div class="section-header">
                <span class="section-subtitle">Nossas Especialidades</span>
                <h2 class="section-title">Soluções para Conflitos Trabalhistas</h2>
            </div>

            <div class="services-grid">
                <!-- Serviço 1 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fa-solid fa-clock-rotate-left"></i>
                    </div>
                    <h3>Horas Extras e Adicionais</h3>
                    <p>Recuperação de horas trabalhadas além do limite legal sem o devido pagamento, supressão de intervalos de refeição e adicional noturno.</p>
                    <ul class="service-list">
                        <li><i class="fa-solid fa-check"></i> Intervalo Intrajornada</li>
                        <li><i class="fa-solid fa-check"></i> Banco de horas irregular</li>
                        <li><i class="fa-solid fa-check"></i> Prorrogação de jornada noturna</li>
                    </ul>
                </div>

                <!-- Serviço 2 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fa-solid fa-skull-crossbones"></i>
                    </div>
                    <h3>Insalubridade e Periculosidade</h3>
                    <p>Cobrança de adicionais para trabalhadores expostos a agentes nocivos à saúde (químicos, ruídos) ou riscos de vida (eletricidade, inflamáveis).</p>
                    <ul class="service-list">
                        <li><i class="fa-solid fa-check"></i> Perícia técnica especializada</li>
                        <li><i class="fa-solid fa-check"></i> Adicional de 10%, 20% ou 40%</li>
                        <li><i class="fa-solid fa-check"></i> Falta de fornecimento de EPI</li>
                    </ul>
                </div>

                <!-- Serviço 3 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fa-solid fa-file-contract"></i>
                    </div>
                    <h3>Rescisão Indireta do Contrato</h3>
                    <p>Ação legal para quando a empresa comete faltas graves (atraso de salário, falta de depósito do FGTS, assédio), garantindo os mesmos direitos da demissão sem justa causa.</p>
                    <ul class="service-list">
                        <li><i class="fa-solid fa-check"></i> Desligamento com direitos integrais</li>
                        <li><i class="fa-solid fa-check"></i> Liberação imediata de FGTS</li>
                        <li><i class="fa-solid fa-check"></i> Habilitação no Seguro-Desemprego</li>
                    </ul>
                </div>

                <!-- Serviço 4 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fa-solid fa-user-injured"></i>
                    </div>
                    <h3>Acidente de Trabalho e Doença Profissional</h3>
                    <p>Indemnizações por danos morais, estéticos e materiais resultantes de lesões ocorridas na empresa ou adquiridas por conta do trabalho desempenhado.</p>
                    <ul class="service-list">
                        <li><i class="fa-solid fa-check"></i> Pedido de Estabilidade Provisória</li>
                        <li><i class="fa-solid fa-check"></i> Indenização por Burnout / LER</li>
                        <li><i class="fa-solid fa-check"></i> Pensão vitalícia ou temporária</li>
                    </ul>
                </div>

                <!-- Serviço 5 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fa-solid fa-gavel"></i>
                    </div>
                    <h3>Reversão de Justa Causa</h3>
                    <p>Anulação na Justiça Trabalhista de demissões injustas por justa causa aplicadas de maneira desproporcional ou sem provas substanciais.</p>
                    <ul class="service-list">
                        <li><i class="fa-solid fa-check"></i> Restabelecimento das verbas completas</li>
                        <li><i class="fa-solid fa-check"></i> Retirada da penalidade injusta</li>
                        <li><i class="fa-solid fa-check"></i> Danos morais por acusação infundada</li>
                    </ul>
                </div>

                <!-- Serviço 6 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fa-solid fa-handshake-slash"></i>
                    </div>
                    <h3>Assédio Moral e Discriminação</h3>
                    <p>Combate rigoroso a situações de humilhação, rigor excessivo, metas inalcançáveis, discriminação ou isolamento do empregado no ambiente corporativo.</p>
                    <ul class="service-list">
                        <li><i class="fa-solid fa-check"></i> Produção e preservação de provas</li>
                        <li><i class="fa-solid fa-check"></i> Compensação financeira por danos à honra</li>
                        <li><i class="fa-solid fa-check"></i> Proteção da dignidade do trabalhador</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- SOBRE O ADVOGADO -->
    <section class="about-section" id="sobre">
        <div class="container">
            <div class="about-grid">
                <div class="about-image-wrapper">
                    <img src="https://images.unsplash.com/photo-1560250097-0b93528c311a?auto=format&fit=crop&w=800&q=80" alt="Dr. Adauto Rodrigues">
                    <div class="experience-badge">
                        <div class="number">15+</div>
                        <div class="text">Anos de Experiência</div>
                    </div>
                </div>

                <div class="about-content">
                    <span class="section-subtitle">Conheça o Especialista</span>
                    <h2>Dr. Adauto Rodrigues</h2>
                    <span class="oab-number">OAB/SP nº 345.890 | Advogado Trabalhista</span>

                    <p>
                        Fundador do escritório Adauto Rodrigues Advocacia, é graduado em Direito com pós-graduação em Direito e Processo do Trabalho pela USP. Dedica sua carreira exclusivamente à defesa dos direitos dos trabalhadores do setor privado e corporativo.
                    </p>
                    <p>
                        Com uma visão humanizada e focada em resultados rápidos, tem atuado decisivamente na recuperação de créditos trabalhistas sonegados e na restauração da dignidade de profissionais lesados.
                    </p>

                    <div class="stats-grid">
                        <div class="stat-item">
                            <h4>+2.500</h4>
                            <p>Processos Concluídos</p>
                        </div>
                        <div class="stat-item">
                            <h4>98%</h4>
                            <p>Clientes Satisfeitos</p>
                        </div>
                        <div class="stat-item">
                            <h4>R$ 15M+</h4>
                            <p>Recuperados aos Clientes</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ARTIGOS E ORIENTAÇÕES TRABALHISTAS -->
    <section class="blog-section" id="artigos">
        <div class="container">
            <div class="section-header">
                <span class="section-subtitle">Informativo Jurídico</span>
                <h2 class="section-title">Fique Por Dentro dos Seus Direitos</h2>
            </div>

            <div class="blog-grid">
                <article class="blog-card">
                    <div class="blog-img" style="background-image: url('https://images.unsplash.com/photo-1450133064473-71024230f91b?auto=format&fit=crop&w=600&q=80');"></div>
                    <div class="blog-content">
                        <span class="blog-date">15 de Maio, 2026</span>
                        <h3 class="blog-title">Fui demitido e a empresa não pagou a rescisão: o que fazer?</h3>
                        <p class="blog-excerpt">Saiba qual é o prazo legal para pagamento das verbas rescisórias e as multas aplicáveis pelo atraso (Art. 477 da CLT).</p>
                        <a href="javascript:void(0)" class="blog-link" onclick="alert('Artigo completo: O prazo legal para pagamento da rescisão é de até 10 dias corridos após o término do contrato. Se não pago, incide multa equivalente a um salário do empregado.')">Ler Artigo Completo <i class="fa-solid fa-arrow-right"></i></a>
                    </div>
                </article>

                <article class="blog-card">
                    <div class="blog-img" style="background-image: url('https://images.unsplash.com/photo-1521791136064-7986c2920216?auto=format&fit=crop&w=600&q=80');"></div>
                    <div class="blog-content">
                        <span class="blog-date">02 de Abril, 2026</span>
                        <h3 class="blog-title">Como comprovar as Horas Extras na Justiça do Trabalho?</h3>
                        <p class="blog-excerpt">Descubra as provas mais valiosas para comprovar trabalho em jornada extraordinária: testemunhas, registros e mensagens.</p>
                        <a href="javascript:void(0)" class="blog-link" onclick="alert('Artigo completo: Fotos, e-mails, registros de GPS, conversas no WhatsApp e depoimentos de colegas de trabalho são aceitos como prova idônea.')">Ler Artigo Completo <i class="fa-solid fa-arrow-right"></i></a>
                    </div>
                </article>

                <article class="blog-card">
                    <div class="blog-img" style="background-image: url('https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?auto=format&fit=crop&w=600&q=80');"></div>
                    <div class="blog-content">
                        <span class="blog-date">20 de Março, 2026</span>
                        <h3 class="blog-title">Rescisão Indireta: quando você pode "demitir" o seu patrão?</h3>
                        <p class="blog-excerpt">Entenda os motivos legais que autorizam o empregado a sair da empresa sem perder nenhum dos seus direitos.</p>
                        <a href="javascript:void(0)" class="blog-link" onclick="alert('Artigo completo: Atraso recorrente de salários, não recolhimento de FGTS e tratamento com rigor excessivo/assédio são motivos claros para pedir Rescisão Indireta.')">Ler Artigo Completo <i class="fa-solid fa-arrow-right"></i></a>
                    </div>
                </article>
            </div>
        </div>
    </section>

    <!-- FAQ SECTION -->
    <section class="faq-section" id="faq">
        <div class="container">
            <div class="section-header">
                <span class="section-subtitle">Dúvidas Frequentes</span>
                <h2 class="section-title">Perguntas Mais Comuns</h2>
            </div>

            <div class="faq-container">
                <div class="faq-item">
                    <button class="faq-question">
                        <span>Quanto custa para entrar com um processo trabalhista?</span>
                        <i class="fa-solid fa-chevron-down faq-icon"></i>
                    </button>
                    <div class="faq-answer">
                        <div class="faq-answer-content">
                            Geralmente, atuamos com honorários *Ad Exitum*, o que significa que os honorários advocatícios são quitados apenas no final do processo, sobre o valor efetivamente ganho/recuperado pelo trabalhador.
                        </div>
                    </div>
                </div>

                <div class="faq-item">
                    <button class="faq-question">
                        <span>Qual é o prazo para eu entrar na Justiça contra a empresa?</span>
                        <i class="fa-solid fa-chevron-down faq-icon"></i>
                    </button>
                    <div class="faq-answer">
                        <div class="faq-answer-content">
                            O trabalhador tem o prazo de até **2 (dois) anos** após a data de rescisão/saída da empresa para ingressar com a Ação Trabalhista. Nesse processo, poderá cobrar os últimos 5 (cinco) anos de direitos retroativos.
                        </div>
                    </div>
                </div>

                <div class="faq-item">
                    <button class="faq-question">
                        <span>O que acontece se a empresa onde eu trabalhava fechar?</span>
                        <i class="fa-solid fa-chevron-down faq-icon"></i>
                    </button>
                    <div class="faq-answer">
                        <div class="faq-answer-content">
                            Se a empresa fechar ou falir, o processo pode redirecionar a cobrança diretamente para os bens pessoais dos sócios (Desconsideração da Personalidade Jurídica) ou para o grupo econômico do qual a empresa fazia parte.
                        </div>
                    </div>
                </div>

                <div class="faq-item">
                    <button class="faq-question">
                        <span>Preciso comparecer presencialmente a alguma audiência?</span>
                        <i class="fa-solid fa-chevron-down faq-icon"></i>
                    </button>
                    <div class="faq-answer">
                        <div class="faq-answer-content">
                            Atualmente, a maioria das audiências e atendimentos ocorrem na modalidade telepresencial (online por videoconferência). Caso haja audiência presencial, nós o acompanharemos integralmente.
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SEÇÃO DE CONTATO E AGENDAMENTO -->
    <section class="contact-section" id="contato">
        <div class="container">
            <div class="contact-grid">
                <div class="contact-info-side">
                    <h2>Entre em Contato Conosco</h2>
                    <p style="color: rgba(255,255,255,0.8); margin-bottom: 40px;">
                        Envie o resumo da sua situação e agende uma consulta especializada para avaliar seus direitos trabalhistas.
                    </p>

                    <div class="contact-detail-item">
                        <i class="fa-solid fa-phone"></i>
                        <div>
                            <h4>Telefone e WhatsApp</h4>
                            <p>(11) 98765-4321 / (11) 3333-4444</p>
                        </div>
                    </div>

                    <div class="contact-detail-item">
                        <i class="fa-solid fa-envelope"></i>
                        <div>
                            <h4>E-mail</h4>
                            <p>atendimento@adautorodrigues.adv.br</p>
                        </div>
                    </div>

                    <div class="contact-detail-item">
                        <i class="fa-solid fa-location-dot"></i>
                        <div>
                            <h4>Endereço do Escritório</h4>
                            <p>Av. Paulista, 1000, Cj. 1201 - Bela Vista, São Paulo - SP, CEP 01310-100</p>
                        </div>
                    </div>
                </div>

                <div class="contact-form-side">
                    <h3>Agendar Consulta</h3>
                    <form id="contactForm" onsubmit="event.preventDefault(); handleFormSubmit();">
                        <div class="form-group">
                            <label for="cNome">Nome Completo</label>
                            <input type="text" id="cNome" class="form-control" placeholder="Seu nome" required>
                        </div>

                        <div class="form-group">
                            <label for="cTelefone">WhatsApp / Telefone</label>
                            <input type="tel" id="cTelefone" class="form-control" placeholder="(11) 99999-9999" required>
                        </div>

                        <div class="form-group">
                            <label for="cAssunto">Principal Assunto</label>
                            <select id="cAssunto" class="form-control">
                                <option>Demissão / Rescisão de Contrato</option>
                                <option>Horas Extras / Adicionais</option>
                                <option>Insalubridade / Periculosidade</option>
                                <option>Acidente do Trabalho / Doença</option>
                                <option>Assédio Moral / Outros</option>
                            </select>
                        </div>

                        <div class="form-group">
                            <label for="cMensagem">Resumo da sua situação</label>
                            <textarea id="cMensagem" class="form-control" rows="4" placeholder="Descreva brevemente o que aconteceu no seu trabalho..." required></textarea>
                        </div>

                        <button type="submit" class="btn btn-gold" style="width: 100%;">
                            <i class="fa-solid fa-paper-plane"></i> Enviar Solicitação
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <a href="#" class="logo" style="margin-bottom: 20px;">
                        <i class="fa-solid fa-scale-balanced"></i>
                        <div class="logo-text">
                            <h1 style="font-size: 1.2rem;">ADAUTO RODRIGUES</h1>
                            <span>Advocacia Trabalhista</span>
                        </div>
                    </a>
                    <p style="margin-bottom: 15px;">
                        Escritório especializado em Direito do Trabalho, dedicado à defesa dos trabalhadores com ética, responsabilidade e rapidez.
                    </p>
                    <div class="social-links">
                        <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                        <a href="#"><i class="fa-brands fa-instagram"></i></a>
                        <a href="#"><i class="fa-brands fa-linkedin-in"></i></a>
                        <a href="#"><i class="fa-brands fa-whatsapp"></i></a>
                    </div>
                </div>

                <div class="footer-col">
                    <h4>Links Rápidos</h4>
                    <ul>
                        <li><a href="#inicio">Início</a></li>
                        <li><a href="#calculadora">Calculadora</a></li>
                        <li><a href="#servicos">Áreas de Atuação</a></li>
                        <li><a href="#sobre">Dr. Adauto Rodrigues</a></li>
                        <li><a href="#faq">Perguntas Frequentes</a></li>
                    </ul>
                </div>

                <div class="footer-col">
                    <h4>Serviços</h4>
                    <ul>
                        <li><a href="#servicos">Cálculo de Rescisão</a></li>
                        <li><a href="#servicos">Cobrança de Horas Extras</a></li>
                        <li><a href="#servicos">Rescisão Indireta</a></li>
                        <li><a href="#servicos">Insalubridade/Periculosidade</a></li>
                        <li><a href="#servicos">Acidentes de Trabalho</a></li>
                    </ul>
                </div>

                <div class="footer-col">
                    <h4>Horário de Funcionamento</h4>
                    <p><i class="fa-solid fa-clock" style="color: var(--accent-gold);"></i> Seg - Sex: 08:00 - 18:00</p>
                    <p><i class="fa-solid fa-calendar-check" style="color: var(--accent-gold);"></i> Plantão via WhatsApp aos sábados</p>
                    <div style="margin-top: 15px;">
                        <span style="display: inline-block; background: rgba(197, 160, 89, 0.1); padding: 5px 10px; border-radius: 4px; border: 1px solid var(--accent-gold); color: var(--accent-gold); font-size: 0.8rem;">
                            Inscrição OAB/SP 345.890
                        </span>
                    </div>
                </div>
            </div>

            <div class="footer-bottom">
                <p>&copy; <span id="currentYear"></span> Adauto Rodrigues Advocacia. Todos os direitos reservados.</p>
                <p>Termos de Uso | Política de Privacidade</p>
            </div>
        </div>
    </footer>

    <!-- BOTÃO FLUTUANTE DO WHATSAPP -->
    <a href="https://wa.me/5511987654321?text=Olá,%20gostaria%20de%20agendar%20uma%20consulta%20trabalhista" class="whatsapp-float" target="_blank" title="Fale no WhatsApp">
        <i class="fa-brands fa-whatsapp"></i>
    </a>

    <!-- MODAL DE LOGIN / ÁREA DO CLIENTE -->
    <div class="modal-overlay" id="authModal">
        <div class="modal-box">
            <button class="modal-close" id="closeModalBtn">&times;</button>
            
            <div class="modal-header">
                <h3>Área do Cliente</h3>
                <p>Acompanhe o andamento do seu processo</p>
            </div>

            <!-- TELA DE LOGIN -->
            <div class="modal-body" id="modalLoginForm">
                <div class="login-tabs">
                    <button class="tab-btn active" onclick="switchTab('cpfTab')">Entrar por CPF/Nome</button>
                    <button class="tab-btn" onclick="switchTab('gmailTab')">Login com Google</button>
                </div>

                <!-- ABA 1: LOGIN POR CPF / NOME -->
                <div class="tab-content active" id="cpfTab">
                    <form onsubmit="event.preventDefault(); processLogin('cpf');">
                        <div class="form-group">
                            <label for="loginIdentifier">Nome Completo ou CPF</label>
                            <input type="text" id="loginIdentifier" class="form-control" placeholder="Digite seu Nome ou CPF" required>
                        </div>

                        <div class="form-group">
                            <label for="loginPassword">Senha de Acesso</label>
                            <input type="password" id="loginPassword" class="form-control" placeholder="••••••••" required>
                        </div>

                        <button type="submit" class="btn btn-gold" style="width: 100%;">
                            <i class="fa-solid fa-right-to-bracket"></i> Acessar Meu Processo
                        </button>
                    </form>
                </div>

                <!-- ABA 2: LOGIN VIA GMAIL / GOOGLE -->
                <div class="tab-content" id="gmailTab">
                    <p style="font-size: 0.85rem; color: var(--text-muted); margin-bottom: 15px; text-align: center;">
                        Acesse rapidamente com sua conta Google vinculada ao cadastro do escritório:
                    </p>
                    
                    <button class="btn-google" onclick="processLogin('gmail')">
                        <svg width="18" height="18" viewBox="0 0 24 24">
                            <path fill="#4285F4" d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z"/>
                            <path fill="#34A853" d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z"/>
                            <path fill="#FBBC05" d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.06H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.94l2.85-2.22.81-.63z"/>
                            <path fill="#EA4335" d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.06l3.66 2.84c.87-2.6 3.3-4.52 6.16-4.52z"/>
                        </svg>
                        Entrar com o Gmail
                    </button>

                    <div class="divider">
                        <span>OU</span>
                    </div>

                    <form onsubmit="event.preventDefault(); processLogin('gmail');">
                        <div class="form-group">
                            <label for="gmailEmail">Seu E-mail Gmail</label>
                            <input type="email" id="gmailEmail" class="form-control" placeholder="seuemail@gmail.com" required>
                        </div>
                        <button type="submit" class="btn btn-gold" style="width: 100%;">
                            Acessar via E-mail
                        </button>
                    </form>
                </div>
            </div>

            <!-- PAINEL DE CLIENTE LOGADO (EXIBIDO APÓS O LOGIN) -->
            <div class="client-dashboard" id="clientDashboard">
                <div class="user-welcome">
                    <h4 id="userNameDisplay">Olá, Cliente!</h4>
                    <p style="font-size: 0.85rem; color: var(--text-muted);">Processo nº: 0001234-88.2026.5.02.0001</p>
                </div>

                <h5 style="margin-bottom: 15px; color: var(--primary-navy);">Status do Seu Processo:</h5>

                <div class="process-status-tracker">
                    <div class="status-step completed">
                        <div class="step-icon"><i class="fa-solid fa-check"></i></div>
                        <div class="step-info">
                            <h5>Ação Protocolada</h5>
                            <p>Peticiamento inicial realizado com sucesso.</p>
                        </div>
                    </div>

                    <div class="status-step completed">
                        <div class="step-icon"><i class="fa-solid fa-check"></i></div>
                        <div class="step-info">
                            <h5>Audiência de Conciliação</h5>
                            <p>Realizada em 10/04/2026.</p>
                        </div>
                    </div>

                    <div class="status-step current">
                        <div class="step-icon"><i class="fa-solid fa-spinner fa-spin"></i></div>
                        <div class="step-info">
                            <h5>Perícia Técnica em Andamento</h5>
                            <p>Aguardando laudo do perito judicial.</p>
                        </div>
                    </div>

                    <div class="status-step">
                        <div class="step-icon"><i class="fa-solid fa-gavel"></i></div>
                        <div class="step-info">
                            <h5>Sentença</h5>
                            <p>Aguardando publicação do juiz.</p>
                        </div>
                    </div>
                </div>

                <button class="btn btn-outline" style="width: 100%; margin-top: 25px;" onclick="logoutUser()">
                    <i class="fa-solid fa-right-from-bracket"></i> Sair do Painel
                </button>
            </div>
        </div>
    </div>

    <!-- ==========================================================================
       JAVASCRIPT
       ========================================================================== -->
    <script>
        // Set dynamic current year in footer
        document.getElementById('currentYear').textContent = new Date().getFullYear();

        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const navLinks = document.getElementById('navLinks');

        mobileMenuBtn.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Close mobile menu on link click
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });

        // FAQ Accordion Toggle
        const faqItems = document.querySelectorAll('.faq-item');

        faqItems.forEach(item => {
            const questionBtn = item.querySelector('.faq-question');
            questionBtn.addEventListener('click', () => {
                const isActive = item.classList.contains('active');
                
                // Fechar todos os outros
                faqItems.forEach(otherItem => {
                    otherItem.classList.remove('active');
                    otherItem.querySelector('.faq-answer').style.maxHeight = null;
                });

                if (!isActive) {
                    item.classList.add('active');
                    const answer = item.querySelector('.faq-answer');
                    answer.style.maxHeight = answer.scrollHeight + "px";
                }
            });
        });

        // Calculadora Trabalhista
        function calcularRescisao() {
            const salario = parseFloat(document.getElementById('salarioBruto').value) || 0;
            const meses = parseInt(document.getElementById('mesesTrabalhados').value) || 0;
            const motivo = document.getElementById('motivoSaida').value;
            const aviso = document.getElementById('avisoPrevio').value;

            let avisoValue = 0;
            let decimoTerceiro = 0;
            let ferias = 0;
            let fgtsMulta = 0;

            if (motivo === 'semJustaCausa' || motivo === 'rescisaoIndireta') {
                if (aviso === 'indenizado') {
                    avisoValue = salario;
                }
                decimoTerceiro = (salario / 12) * (meses % 12 || 12);
                ferias = ((salario / 12) * (meses % 12 || 12)) * 1.333;
                fgtsMulta = (salario * 0.08 * meses) * 0.40;
            } else if (motivo === 'pedidoDemissao') {
                decimoTerceiro = (salario / 12) * (meses % 12 || 12);
                ferias = ((salario / 12) * (meses % 12 || 12)) * 1.333;
            } else if (motivo === 'justaCausa') {
                // Em justa causa só recebe saldos de dias trabalhados
                decimoTerceiro = 0;
                ferias = 0;
            }

            const total = avisoValue + decimoTerceiro + ferias + fgtsMulta;

            // Formatação Monetária
            const formatMoney = (val) => val.toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' });

            document.getElementById('resAviso').textContent = formatMoney(avisoValue);
            document.getElementById('res13').textContent = formatMoney(decimoTerceiro);
            document.getElementById('resFerias').textContent = formatMoney(ferias);
            document.getElementById('resFGTS').textContent = formatMoney(fgtsMulta);
            document.getElementById('resTotal').textContent = formatMoney(total);
        }

        // Executa o cálculo inicial
        calcularRescisao();

        // Controle dos Modais e Autenticação
        const authModal = document.getElementById('authModal');
        const openAuthModalBtn = document.getElementById('openAuthModalBtn');
        const closeModalBtn = document.getElementById('closeModalBtn');

        openAuthModalBtn.addEventListener('click', () => {
            authModal.classList.add('active');
        });

        closeModalBtn.addEventListener('click', () => {
            authModal.classList.remove('active');
        });

        window.addEventListener('click', (e) => {
            if (e.target === authModal) {
                authModal.classList.remove('active');
            }
        });

        // Alternar entre abas do modal
        function switchTab(tabId) {
            document.querySelectorAll('.tab-btn').forEach(btn => btn.classList.remove('active'));
            document.querySelectorAll('.tab-content').forEach(content => content.classList.remove('active'));

            if (tabId === 'cpfTab') {
                document.querySelectorAll('.tab-btn')[0].classList.add('active');
                document.getElementById('cpfTab').classList.add('active');
            } else {
                document.querySelectorAll('.tab-btn')[1].classList.add('active');
                document.getElementById('gmailTab').classList.add('active');
            }
        }

        // Processar Login Simulado
        function processLogin(type) {
            let name = "Usuário Cliente";

            if (type === 'cpf') {
                const inputVal = document.getElementById('loginIdentifier').value;
                if (inputVal) name = inputVal;
            } else if (type === 'gmail') {
                const gmailVal = document.getElementById('gmailEmail').value;
                if (gmailVal) name = gmailVal.split('@')[0];
            }

            document.getElementById('userNameDisplay').textContent = "Olá, " + name + "!";
            document.getElementById('modalLoginForm').style.display = 'none';
            document.getElementById('clientDashboard').classList.add('active');
        }

        // Logout
        function logoutUser() {
            document.getElementById('clientDashboard').classList.remove('active');
            document.getElementById('modalLoginForm').style.display = 'block';
        }

        // Envio do formulário de contato
        function handleFormSubmit() {
            const nome = document.getElementById('cNome').value;
            alert(`Obrigado, ${nome}! Sua mensagem foi recebida com sucesso. A equipe do Dr. Adauto Rodrigues entrará em contato em até 24 horas.`);
            document.getElementById('contactForm').reset();
        }
    </script>
</body>
</html>