<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, user-scalable=yes">
    <title>Tootoday - Официальный сайт музыкальной группы</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&family=Open+Sans:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #ff3366;
            --secondary: #6633ff;
            --dark: #121212;
            --light: #f8f9fa;
            --gray: #2d2d2d;
            --transition: all 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            --container-padding: clamp(1rem, 4vw, 2rem);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            font-size: 100%;
        }

        body {
            font-family: 'Open Sans', sans-serif;
            line-height: 1.6;
            color: var(--light);
            background-color: var(--dark);
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
            text-rendering: optimizeLegibility;
        }

        h1, h2, h3, h4 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: clamp(0.75rem, 2vw, 1rem);
        }

        h1 {
            font-size: clamp(2rem, 8vw, 3.5rem);
            text-transform: uppercase;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        h2 {
            font-size: clamp(1.75rem, 6vw, 2.5rem);
            position: relative;
            display: inline-block;
            margin-bottom: clamp(1.5rem, 4vw, 2.5rem);
        }

        h2:after {
            content: '';
            position: absolute;
            left: 0;
            bottom: -10px;
            width: min(70px, 20vw);
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            border-radius: 2px;
        }

        p {
            font-size: clamp(0.875rem, 1.1vw, 1rem);
            line-height: 1.7;
        }

        section {
            padding: clamp(3rem, 8vw, 5rem) var(--container-padding);
            position: relative;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            width: 100%;
            padding: 0 var(--container-padding);
        }

        .btn {
            display: inline-block;
            padding: clamp(0.7rem, 2vw, 0.8rem) clamp(1.5rem, 4vw, 2rem);
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            color: white;
            border: none;
            border-radius: 50px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: var(--transition);
            text-decoration: none;
            font-size: clamp(0.8rem, 1vw, 0.9rem);
            text-align: center;
            min-height: 44px;
            min-width: 44px;
        }

        .btn:hover, .btn:focus {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
            outline: none;
        }

        .btn:active {
            transform: translateY(-1px);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }

        .btn-outline:hover, .btn-outline:focus {
            background: var(--primary);
            color: white;
        }

        /* Touch-friendly targets */
        button, .btn, .nav-links a, .social-link, .track, .gallery-item {
            touch-action: manipulation;
        }

        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            padding: clamp(1rem, 3vw, 1.5rem) 0;
            transition: var(--transition);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
        }

        header.scrolled {
            background-color: rgba(18, 18, 18, 0.95);
            padding: 0.8rem 0;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 var(--container-padding);
            position: relative;
        }

        .logo {
            font-size: clamp(1.5rem, 4vw, 1.8rem);
            font-weight: 700;
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
            min-height: 44px;
        }

        .logo span {
            color: var(--primary);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: clamp(1rem, 2vw, 2rem);
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            text-transform: uppercase;
            font-size: clamp(0.75rem, 1vw, 0.9rem);
            letter-spacing: 1px;
            transition: var(--transition);
            padding: 0.5rem 0;
            position: relative;
            min-height: 44px;
            display: flex;
            align-items: center;
        }

        .nav-links a:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: width 0.3s ease;
        }

        .nav-links a:hover:after,
        .nav-links a:focus:after {
            width: 100%;
        }

        .nav-links a:hover,
        .nav-links a:focus {
            color: var(--primary);
            outline: none;
        }

        .hamburger {
            display: none;
            cursor: pointer;
            font-size: 1.5rem;
            color: white;
            min-height: 44px;
            min-width: 44px;
            align-items: center;
            justify-content: center;
            z-index: 1001;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            min-height: 100dvh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: 
                linear-gradient(rgba(18, 18, 18, 0.8), rgba(18, 18, 18, 0.9)), 
                url('https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            background-repeat: no-repeat;
            padding: 80px var(--container-padding) clamp(3rem, 8vw, 5rem);
        }

        @media (max-width: 768px) {
            .hero {
                background-attachment: scroll;
            }
        }

        .hero-content {
            max-width: min(800px, 90vw);
            padding: clamp(1rem, 3vw, 2rem);
            margin: 0 auto;
        }

        .hero p {
            font-size: clamp(1rem, 1.5vw, 1.2rem);
            margin-bottom: clamp(1.5rem, 4vw, 2rem);
            color: #ddd;
        }

        .hero-btns {
            display: flex;
            justify-content: center;
            gap: clamp(1rem, 2vw, 1.5rem);
            flex-wrap: wrap;
        }

        .hero-btns .btn {
            flex: 1;
            min-width: 200px;
            max-width: 300px;
        }

        /* About Section */
        .about {
            background-color: var(--gray);
        }

        .about-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(min(300px, 100%), 1fr));
            gap: clamp(2rem, 4vw, 4rem);
            align-items: center;
        }

        .about-text p {
            margin-bottom: clamp(1rem, 2vw, 1.5rem);
            color: #ccc;
        }

        .about-image {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            aspect-ratio: 4/3;
            max-height: 500px;
        }

        .about-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
            border-radius: 10px;
        }

        /* Music Section */
        .music {
            text-align: center;
        }

        .section-subtitle {
            color: #aaa;
            margin-bottom: clamp(2rem, 4vw, 3rem);
            font-size: clamp(1rem, 1.2vw, 1.1rem);
        }

        .album-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(min(280px, 100%), 1fr));
            gap: clamp(1.5rem, 3vw, 2rem);
            margin-bottom: clamp(2rem, 4vw, 3rem);
        }

        .album-card {
            background-color: var(--gray);
            border-radius: 10px;
            overflow: hidden;
            transition: var(--transition);
            display: flex;
            flex-direction: column;
            height: 100%;
        }

        .album-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4);
        }

        .album-img {
            height: clamp(200px, 40vw, 250px);
            overflow: hidden;
        }

        .album-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }

        .album-card:hover .album-img img {
            transform: scale(1.05);
        }

        .album-info {
            padding: clamp(1rem, 2vw, 1.5rem);
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

        .album-info h3 {
            color: white;
            margin-bottom: 0.5rem;
            font-size: clamp(1.1rem, 1.5vw, 1.3rem);
        }

        .album-info p {
            color: #aaa;
            font-size: clamp(0.8rem, 1vw, 0.9rem);
            margin-bottom: clamp(1rem, 2vw, 1.5rem);
        }

        .album-info .btn {
            margin-top: auto;
            align-self: flex-start;
        }

        .player {
            background-color: var(--gray);
            border-radius: 10px;
            padding: clamp(1.5rem, 3vw, 2rem);
            max-width: min(800px, 100%);
            margin: 0 auto;
            text-align: left;
        }

        .player h3 {
            margin-bottom: clamp(1rem, 2vw, 1.5rem);
            font-size: clamp(1.2rem, 2vw, 1.5rem);
        }

        .track {
            display: flex;
            align-items: center;
            padding: clamp(0.8rem, 1.5vw, 1rem);
            border-bottom: 1px solid #444;
            cursor: pointer;
            transition: var(--transition);
            min-height: 60px;
        }

        .track:hover {
            background-color: rgba(255, 255, 255, 0.05);
        }

        .track.active {
            background-color: rgba(255, 51, 102, 0.1);
            border-left: 4px solid var(--primary);
        }

        .track-number {
            font-weight: 600;
            margin-right: 1rem;
            color: var(--primary);
            min-width: 30px;
            font-size: clamp(0.9rem, 1.1vw, 1rem);
        }

        .track-title {
            flex-grow: 1;
            color: white;
            font-size: clamp(0.9rem, 1.1vw, 1rem);
        }

        .track-duration {
            color: #aaa;
            font-size: clamp(0.8rem, 1vw, 0.9rem);
        }

        /* Tour Section */
        .tour {
            background-color: var(--gray);
        }

        .tour-dates {
            max-width: min(800px, 100%);
            margin: 0 auto;
        }

        .tour-date {
            display: flex;
            background-color: var(--dark);
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: clamp(1rem, 2vw, 1.5rem);
            transition: var(--transition);
            flex-wrap: wrap;
        }

        .tour-date:hover {
            transform: translateX(10px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }

        .tour-date-info {
            padding: clamp(1rem, 2vw, 1.5rem);
            flex: 1;
            min-width: 250px;
        }

        .tour-date-info h3 {
            color: white;
            font-size: clamp(1rem, 1.5vw, 1.2rem);
        }

        .tour-date-info p {
            color: #aaa;
            margin-bottom: 0.5rem;
            font-size: clamp(0.85rem, 1vw, 0.95rem);
        }

        .tour-date-ticket {
            display: flex;
            align-items: center;
            justify-content: center;
            padding: clamp(1rem, 2vw, 1.5rem);
            background-color: var(--primary);
            min-width: 150px;
        }

        /* Gallery Section */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(min(250px, 100%), 1fr));
            gap: clamp(0.75rem, 1.5vw, 1rem);
            grid-auto-rows: 250px;
        }

        @media (max-width: 480px) {
            .gallery-grid {
                grid-template-columns: repeat(auto-fill, minmax(min(200px, 100%), 1fr));
                grid-auto-rows: 200px;
            }
        }

        .gallery-item {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            height: 100%;
            cursor: pointer;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
            will-change: transform;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .gallery-item-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(rgba(255, 51, 102, 0.7), rgba(102, 51, 255, 0.7));
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: var(--transition);
        }

        .gallery-item:hover .gallery-item-overlay {
            opacity: 1;
        }

        /* Contact Section */
        .contact {
            background-color: var(--gray);
        }

        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(min(300px, 100%), 1fr));
            gap: clamp(2rem, 4vw, 4rem);
        }

        .contact-info h3 {
            color: white;
            margin-bottom: clamp(0.75rem, 2vw, 1rem);
            font-size: clamp(1.2rem, 2vw, 1.5rem);
        }

        .contact-info p {
            color: #aaa;
            margin-bottom: clamp(1.5rem, 3vw, 2rem);
        }

        .contact-details p {
            margin-bottom: 0.75rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .social-links {
            display: flex;
            gap: clamp(0.5rem, 1vw, 1rem);
            flex-wrap: wrap;
        }

        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: clamp(40px, 5vw, 50px);
            height: clamp(40px, 5vw, 50px);
            background-color: var(--dark);
            border-radius: 50%;
            color: white;
            font-size: clamp(1rem, 1.5vw, 1.2rem);
            transition: var(--transition);
            text-decoration: none;
            min-height: 44px;
            min-width: 44px;
        }

        .social-link:hover {
            background-color: var(--primary);
            transform: translateY(-5px);
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: clamp(0.8rem, 1.5vw, 1rem);
            margin-bottom: clamp(1rem, 1.5vw, 1.5rem);
            background-color: var(--dark);
            border: 1px solid #444;
            border-radius: 5px;
            color: white;
            font-family: 'Open Sans', sans-serif;
            font-size: clamp(0.9rem, 1.1vw, 1rem);
            transition: var(--transition);
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 2px rgba(255, 51, 102, 0.2);
        }

        .contact-form textarea {
            height: 150px;
            resize: vertical;
            min-height: 120px;
        }

        /* Footer */
        footer {
            background-color: #0a0a0a;
            padding: clamp(2rem, 5vw, 3rem) 0;
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 var(--container-padding);
        }

        .footer-logo {
            font-size: clamp(1.5rem, 3vw, 2rem);
            font-weight: 700;
            color: white;
            margin-bottom: clamp(1rem, 2vw, 1.5rem);
        }

        .footer-logo span {
            color: var(--primary);
        }

        .copyright {
            color: #777;
            font-size: clamp(0.8rem, 1vw, 0.9rem);
            margin-top: clamp(1.5rem, 3vw, 2rem);
        }

        /* Responsive Styles */
        @media (max-width: 992px) {
            .nav-links {
                position: fixed;
                top: 0;
                right: -100%;
                width: min(300px, 80%);
                height: 100vh;
                height: 100dvh;
                background-color: var(--dark);
                flex-direction: column;
                align-items: center;
                justify-content: center;
                padding: 2rem;
                transition: right 0.4s cubic-bezier(0.68, -0.55, 0.27, 1.55);
                box-shadow: -5px 0 25px rgba(0, 0, 0, 0.3);
                z-index: 1000;
                gap: 1.5rem;
            }
            
            .nav-links.active {
                right: 0;
            }
            
            .hamburger {
                display: flex;
            }
            
            .hamburger.active i:before {
                content: '\f00d';
            }
            
            .hero-btns .btn {
                min-width: 180px;
            }
            
            .tour-date {
                flex-direction: column;
            }
            
            .tour-date-ticket {
                padding: 1rem;
                min-width: 100%;
            }
        }

        @media (max-width: 768px) {
            :root {
                --container-padding: 1.25rem;
            }
            
            .hero-btns {
                flex-direction: column;
                align-items: center;
            }
            
            .hero-btns .btn {
                max-width: 100%;
                width: min(300px, 100%);
            }
            
            .gallery-grid {
                grid-template-columns: repeat(auto-fill, minmax(min(180px, 100%), 1fr));
                grid-auto-rows: 180px;
            }
        }

        @media (max-width: 480px) {
            :root {
                --container-padding: 1rem;
            }
            
            h1 {
                font-size: clamp(1.8rem, 7vw, 2.2rem);
            }
            
            h2 {
                font-size: clamp(1.5rem, 5vw, 1.8rem);
            }
            
            .nav-links {
                width: 100%;
            }
            
            .hero p {
                font-size: clamp(0.95rem, 4vw, 1.1rem);
            }
            
            .track {
                padding: 0.75rem 0.5rem;
                min-height: 50px;
            }
            
            .track-number {
                margin-right: 0.75rem;
                min-width: 25px;
            }
            
            .contact-container {
                gap: 2rem;
            }
        }

        @media (max-width: 360px) {
            :root {
                --container-padding: 0.875rem;
            }
            
            .hero-btns .btn {
                min-width: 160px;
            }
            
            .album-info .btn,
            .tour-date-ticket .btn {
                width: 100%;
            }
        }

        /* High DPI Screens */
        @media (-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi) {
            body {
                -webkit-font-smoothing: antialiased;
                -moz-osx-font-smoothing: grayscale;
            }
        }

        /* Print Styles */
        @media print {
            .hero, footer, .btn, .hamburger, .social-links {
                display: none !important;
            }
            
            body {
                color: black;
                background: white;
            }
            
            section {
                padding: 1rem 0;
                break-inside: avoid;
            }
            
            h1, h2, h3 {
                color: black;
            }
            
            .about-content, .album-container, .gallery-grid {
                display: block;
            }
            
            .album-card, .tour-date, .gallery-item {
                break-inside: avoid;
                margin-bottom: 1rem;
            }
        }

        /* Reduced Motion */
        @media (prefers-reduced-motion: reduce) {
            *, *::before, *::after {
                animation-duration: 0.01ms !important;
                animation-iteration-count: 1 !important;
                transition-duration: 0.01ms !important;
                scroll-behavior: auto !important;
            }
            
            html {
                scroll-behavior: auto;
            }
        }

        /* Dark mode preference */
        @media (prefers-color-scheme: dark) {
            :root {
                --dark: #0a0a0a;
                --gray: #1a1a1a;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header id="header">
        <div class="nav-container">
            <a href="#" class="logo">TOO<span>TODAY</span></a>
            <div class="hamburger" id="hamburger" aria-label="Меню" aria-expanded="false">
                <i class="fas fa-bars"></i>
            </div>
            <ul class="nav-links" id="navLinks">
                <li><a href="#home">Главная</a></li>
                <li><a href="#about">О группе</a></li>
                <li><a href="#music">Музыка</a></li>
                <li><a href="#tour">Концерты</a></li>
                <li><a href="#gallery">Галерея</a></li>
                <li><a href="#contact">Контакты</a></li>
            </ul>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Tootoday</h1>
            <p>Инновационное звучание, захватывающие выступления и энергия, которая заставляет сердца биться в унисон. Присоединяйтесь к нашему музыкальному путешествию.</p>
            <div class="hero-btns">
                <a href="#music" class="btn">Слушать музыку</a>
                <a href="#tour" class="btn btn-outline">Ближайшие концерты</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2>О группе</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Tootoday — музыкальный коллектив, основанный в 2018 году в Москве. Группа объединяет в своём творчестве элементы электронной музыки, инди-рока и альтернативного звучания, создавая уникальный стиль, который быстро завоевал популярность среди слушателей.</p>
                    <p>За время своего существования Tootoday выпустили два студийных альбома и несколько успешных синглов. Их музыка звучала на крупнейших радиостанциях страны, а клипы набирали миллионы просмотров на YouTube.</p>
                    <p>В 2022 году группа получила премию "Открытие года" на музыкальной церемонии "Звуковая дорожка" и была номинирована на "Лучший альтернативный проект".</p>
                    <a href="#contact" class="btn">Связаться с нами</a>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1516450360452-9312f5e86fc7?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Группа Tootoday">
                </div>
            </div>
        </div>
    </section>

    <!-- Music Section -->
    <section class="music" id="music">
        <div class="container">
            <h2>Наша музыка</h2>
            <p class="section-subtitle">Слушайте наши последние релизы и добавляйте в избранное</p>
            
            <div class="album-container">
                <div class="album-card">
                    <div class="album-img">
                        <img src="https://images.unsplash.com/photo-1493225457124-a3eb161ffa5f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Альбом Эхо времен" loading="lazy">
                    </div>
                    <div class="album-info">
                        <h3>Эхо времен</h3>
                        <p>2023 • Альбом</p>
                        <a href="#" class="btn">Слушать</a>
                    </div>
                </div>
                
                <div class="album-card">
                    <div class="album-img">
                        <img src="https://images.unsplash.com/photo-1571974599782-87624638275c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1632&q=80" alt="Альбом Без границ" loading="lazy">
                    </div>
                    <div class="album-info">
                        <h3>Без границ</h3>
                        <p>2021 • Альбом</p>
                        <a href="#" class="btn">Слушать</a>
                    </div>
                </div>
                
                <div class="album-card">
                    <div class="album-img">
                        <img src="https://images.unsplash.com/photo-1511379938547-c1f69419868d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Сингл Небесный свет" loading="lazy">
                    </div>
                    <div class="album-info">
                        <h3>Небесный свет</h3>
                        <p>2023 • Сингл</p>
                        <a href="#" class="btn">Слушать</a>
                    </div>
                </div>
            </div>
            
            <div class="player">
                <h3>Популярные треки</h3>
                <div class="track active" role="button" tabindex="0" aria-label="Воспроизвести Небесный свет">
                    <div class="track-number">01</div>
                    <div class="track-title">Небесный свет</div>
                    <div class="track-duration">3:45</div>
                </div>
                <div class="track" role="button" tabindex="0" aria-label="Воспроизвести Эхо">
                    <div class="track-number">02</div>
                    <div class="track-title">Эхо</div>
                    <div class="track-duration">4:12</div>
                </div>
                <div class="track" role="button" tabindex="0" aria-label="Воспроизвести За горизонтом">
                    <div class="track-number">03</div>
                    <div class="track-title">За горизонтом</div>
                    <div class="track-duration">3:58</div>
                </div>
                <div class="track" role="button" tabindex="0" aria-label="Воспроизвести Без границ">
                    <div class="track-number">04</div>
                    <div class="track-title">Без границ</div>
                    <div class="track-duration">4:30</div>
                </div>
                <div class="track" role="button" tabindex="0" aria-label="Воспроизвести Времена года">
                    <div class="track-number">05</div>
                    <div class="track-title">Времена года</div>
                    <div class="track-duration">3:20</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Tour Section -->
    <section class="tour" id="tour">
        <div class="container">
            <h2>Концерты</h2>
            <p class="section-subtitle">Приходите на наши живые выступления и почувствуйте энергию</p>
            
            <div class="tour-dates">
                <div class="tour-date">
                    <div class="tour-date-info">
                        <h3>Москва, Крокус Сити Холл</h3>
                        <p>15 октября 2023 • 19:00</p>
                        <p>Презентация нового альбома "Эхо времен"</p>
                    </div>
                    <div class="tour-date-ticket">
                        <a href="#" class="btn">Купить билет</a>
                    </div>
                </div>
                
                <div class="tour-date">
                    <div class="tour-date-info">
                        <h3>Санкт-Петербург, Ледовый дворец</h3>
                        <p>22 октября 2023 • 20:00</p>
                        <p>Специальный гость: группа "Созвездие"</p>
                    </div>
                    <div class="tour-date-ticket">
                        <a href="#" class="btn">Купить билет</a>
                    </div>
                </div>
                
                <div class="tour-date">
                    <div class="tour-date-info">
                        <h3>Екатеринбург, ДИВС</h3>
                        <p>5 ноября 2023 • 19:30</p>
                        <p>Часть всероссийского тура "Без границ"</p>
                    </div>
                    <div class="tour-date-ticket">
                        <a href="#" class="btn">Купить билет</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section class="gallery" id="gallery">
        <div class="container">
            <h2>Галерея</h2>
            <p class="section-subtitle">Моменты с концертов, репетиций и жизни группы</p>
            
            <div class="gallery-grid">
                <div class="gallery-item" role="button" tabindex="0" aria-label="Открыть изображение концерта">
                    <img src="https://images.unsplash.com/photo-1516280440614-37939bbacd81?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Концертное выступление" loading="lazy">
                    <div class="gallery-item-overlay">
                        <i class="fas fa-search-plus"></i>
                    </div>
                </div>
                
                <div class="gallery-item" role="button" tabindex="0" aria-label="Открыть изображение студии">
                    <img src="https://images.unsplash.com/photo-1470225620780-dba8ba36b745?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Студийная запись" loading="lazy">
                    <div class="gallery-item-overlay">
                        <i class="fas fa-search-plus"></i>
                    </div>
                </div>
                
                <div class="gallery-item" role="button" tabindex="0" aria-label="Открыть изображение репетиции">
                    <img src="https://images.unsplash.com/photo-1498038432885-c6f3f1b912ee?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Репетиция" loading="lazy">
                    <div class="gallery-item-overlay">
                        <i class="fas fa-search-plus"></i>
                    </div>
                </div>
                
                <div class="gallery-item" role="button" tabindex="0" aria-label="Открыть изображение встречи с фанатами">
                    <img src="https://images.unsplash.com/photo-1501612780327-45045538702b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Встреча с фанатами" loading="lazy">
                    <div class="gallery-item-overlay">
                        <i class="fas fa-search-plus"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <h2>Контакты</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Свяжитесь с нами</h3>
                    <p>По вопросам сотрудничества, организации концертов или просто чтобы сказать привет!</p>
                    
                    <div class="contact-details">
                        <p><i class="fas fa-envelope"></i> booking@tootoday.com</p>
                        <p><i class="fas fa-phone"></i> +7 (999) 123-45-67</p>
                        <p><i class="fas fa-map-marker-alt"></i> Москва, ул. Музыкальная, 15</p>
                    </div>
                    
                    <div class="social-links">
                        <a href="#" class="social-link" aria-label="Spotify"><i class="fab fa-spotify"></i></a>
                        <a href="#" class="social-link" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
                        <a href="#" class="social-link" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="social-link" aria-label="VK"><i class="fab fa-vk"></i></a>
                        <a href="#" class="social-link" aria-label="Telegram"><i class="fab fa-telegram"></i></a>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form id="contactForm">
                        <input type="text" placeholder="Ваше имя" required aria-label="Ваше имя">
                        <input type="email" placeholder="Ваш email" required aria-label="Ваш email">
                        <input type="text" placeholder="Тема" required aria-label="Тема сообщения">
                        <textarea placeholder="Ваше сообщение" required aria-label="Текст сообщения"></textarea>
                        <button type="submit" class="btn">Отправить сообщение</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-logo">TOO<span>TODAY</span></div>
            <p>Музыка, которая меняет мир. Присоединяйтесь к нашему сообществу.</p>
            
            <div class="social-links">
                <a href="#" class="social-link" aria-label="Spotify"><i class="fab fa-spotify"></i></a>
                <a href="#" class="social-link" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
                <a href="#" class="social-link" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
                <a href="#" class="social-link" aria-label="VK"><i class="fab fa-vk"></i></a>
                <a href="#" class="social-link" aria-label="Telegram"><i class="fab fa-telegram"></i></a>
            </div>
            
            <p class="copyright">&copy; 2023 Tootoday. Все права защищены.</p>
        </div>
    </footer>

    <script>
        // Mobile Navigation Toggle
        const hamburger = document.getElementById('hamburger');
        const navLinks = document.getElementById('navLinks');
        
        hamburger.addEventListener('click', () => {
            const isExpanded = hamburger.getAttribute('aria-expanded') === 'true';
            hamburger.setAttribute('aria-expanded', !isExpanded);
            navLinks.classList.toggle('active');
            hamburger.classList.toggle('active');
            
            // Prevent body scroll when menu is open
            document.body.style.overflow = navLinks.classList.contains('active') ? 'hidden' : '';
        });
        
        // Close mobile menu when clicking on a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
                hamburger.classList.remove('active');
                hamburger.setAttribute('aria-expanded', 'false');
                document.body.style.overflow = '';
            });
        });
        
        // Close menu when clicking outside
        document.addEventListener('click', (e) => {
            if (!navLinks.contains(e.target) && !hamburger.contains(e.target)) {
                navLinks.classList.remove('active');
                hamburger.classList.remove('active');
                hamburger.setAttribute('aria-expanded', 'false');
                document.body.style.overflow = '';
            }
        });
        
        // Header scroll effect
        let lastScroll = 0;
        const header = document.getElementById('header');
        
        window.addEventListener('scroll', () => {
            const currentScroll = window.pageYOffset;
            
            if (currentScroll > 100) {
                header.classList.add('scrolled');
                
                // Hide header on scroll down, show on scroll up
                if (currentScroll > lastScroll && currentScroll > 200) {
                    header.style.transform = 'translateY(-100%)';
                } else {
                    header.style.transform = 'translateY(0)';
                }
            } else {
                header.classList.remove('scrolled');
                header.style.transform = 'translateY(0)';
            }
            
            lastScroll = currentScroll;
        }, { passive: true });
        
        // Track player interaction
        document.querySelectorAll('.track').forEach(track => {
            track.addEventListener('click', () => {
                document.querySelectorAll('.track').forEach(t => t.classList.remove('active'));
                track.classList.add('active');
                
                // In a real implementation, this would play the selected track
                const trackTitle = track.querySelector('.track-title').textContent;
                console.log(`Воспроизведение: ${trackTitle}`);
                
                // Accessibility feedback
                track.setAttribute('aria-label', `Воспроизводится ${trackTitle}`);
            });
            
            // Keyboard navigation for tracks
            track.addEventListener('keydown', (e) => {
                if (e.key === 'Enter' || e.key === ' ') {
                    e.preventDefault();
                    track.click();
                }
            });
        });
        
        // Form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Simple validation
            const inputs = this.querySelectorAll('input, textarea');
            let isValid = true;
            
            inputs.forEach(input => {
                if (!input.value.trim()) {
                    isValid = false;
                    input.style.borderColor = 'var(--primary)';
                } else {
                    input.style.borderColor = '#444';
                }
            });
            
            if (isValid) {
                alert('Спасибо за ваше сообщение! Мы свяжемся с вами в ближайшее время.');
                this.reset();
            } else {
                alert('Пожалуйста, заполните все поля формы.');
            }
        });
        
        // Smooth scrolling for anchor links with offset
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    e.preventDefault();
                    
                    const headerHeight = document.getElementById('header').offsetHeight;
                    const targetPosition = targetElement.getBoundingClientRect().top + window.pageYOffset - headerHeight;
                    
                    window.scrollTo({
                        top: targetPosition,
                        behavior: 'smooth'
                    });
                    
                    // Update URL without jumping
                    history.pushState(null, null, targetId);
                }
            });
        });
        
        // Gallery image click
        document.querySelectorAll('.gallery-item').forEach(item => {
            item.addEventListener('click', () => {
                console.log('В реальном приложении здесь бы открылось модальное окно с увеличенным изображением.');
            });
            
            item.addEventListener('keydown', (e) => {
                if (e.key === 'Enter' || e.key === ' ') {
                    e.preventDefault();
                    item.click();
                }
            });
        });
        
        // Lazy loading for images
        if ('loading' in HTMLImageElement.prototype) {
            const images = document.querySelectorAll('img[loading="lazy"]');
            images.forEach(img => {
                img.src = img.dataset.src;
            });
        }
        
        // Detect touch device
        const isTouchDevice = 'ontouchstart' in window || navigator.maxTouchPoints > 0;
        if (isTouchDevice) {
            document.body.classList.add('touch-device');
        } else {
            document.body.classList.add('no-touch-device');
        }
        
        // Performance optimization - debounce scroll events
        let scrollTimeout;
        window.addEventListener('scroll', () => {
            clearTimeout(scrollTimeout);
            scrollTimeout = setTimeout(() => {
                // Performance cleanup or actions after scroll stops
            }, 100);
        }, { passive: true });
        
        // Initialize
        document.addEventListener('DOMContentLoaded', () => {
            // Set current year in footer if needed
            const yearElement = document.querySelector('.copyright');
            if (yearElement) {
                yearElement.innerHTML = yearElement.innerHTML.replace('2023', new Date().getFullYear());
            }
        });
    </script>
</body>
</html>
