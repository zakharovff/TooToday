<html lang="ru" dir="ltr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Tootoday - музыкальный коллектив из Москвы, создающий уникальный электронный звук. Слушайте нашу музыку на всех популярных стриминговых платформах.">
    <meta name="keywords" content="Tootoday, музыкальная группа, электронная музыка, Ambient, Dubstep, D'n'B, Drum, Bass, Hardcore">
    <meta name="author" content="Tootoday">
    <meta property="og:title" content="Tootoday - Музыкальный коллектив">
    <meta property="og:description" content="Tootoday - музыкальный коллектив из Москвы, создающий уникальный электронный звук">
    <meta property="og:type" content="website">
    
    <title>Tootoday - Музыкальный коллектив из Москвы</title>

    <link rel="icon" href="favicon.ico">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
    
    <style>
        /* Базовые стили и CSS переменные */
        :root {
            --primary-color: #8a2be2;
            --secondary-color: #4a00e0;
            --accent-color: #ff6b6b;
            --dark-color: #1a1a2e;
            --light-color: #f8f9fa;
            --gray-color: #6c757d;
            --text-dark: #212529;
            --text-light: #f8f9fa;
            --shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
            --border-radius: 10px;
            --container-width: 1200px;
        }

        /* Сброс и базовые стили */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Open Sans', sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            background-color: var(--light-color);
            overflow-x: hidden;
        }

        h1, h2, h3, h4, h5, h6 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            line-height: 1.3;
            margin-bottom: 1rem;
        }

        h1 {
            font-size: 3rem;
        }

        h2 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
        }

        h2:after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            border-radius: 2px;
        }

        p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
        }

        a {
            text-decoration: none;
            color: inherit;
            transition: var(--transition);
        }

        ul {
            list-style: none;
        }

        img {
            max-width: 100%;
            height: auto;
            display: block;
        }

        .container {
            width: 100%;
            max-width: var(--container-width);
            margin: 0 auto;
            padding: 0 20px;
        }

        .section {
            padding: 100px 0;
        }

        .btn {
            display: inline-block;
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            font-weight: 600;
            border: none;
            cursor: pointer;
            transition: var(--transition);
            font-size: 1rem;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: var(--shadow);
        }

        /* Хедер и навигация */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: rgba(26, 26, 46, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            display: flex;
            align-items: center;
        }

        .logo i {
            color: var(--primary-color);
            margin-right: 10px;
            font-size: 2rem;
        }

        .logo span {
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        nav ul {
            display: flex;
            gap: 30px;
        }

        nav a {
            color: white;
            font-weight: 500;
            font-size: 1.1rem;
            position: relative;
        }

        nav a:hover {
            color: var(--primary-color);
        }

        nav a:after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            transition: var(--transition);
        }

        nav a:hover:after {
            width: 100%;
        }

        /* Кнопка переключения языка */
        .language-switcher {
            display: flex;
            align-items: center;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50px;
            padding: 5px;
            cursor: pointer;
            margin-left: 20px;
        }

        .language-btn {
            padding: 8px 20px;
            border-radius: 50px;
            font-weight: 600;
            transition: var(--transition);
            background: transparent;
            border: none;
            color: white;
            cursor: pointer;
            font-size: 0.9rem;
        }

        .language-btn.active {
            background-color: var(--primary-color);
            color: white;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
            margin-left: 20px;
        }

        /* Герой секция - ИСПРАВЛЕНА И ВОССТАНОВЛЕНА */
        .hero {
            position: relative;
            padding: 200px 0 100px;
            background: linear-gradient(135deg, 
                rgba(138, 43, 226, 0.9) 0%, 
                rgba(74, 0, 224, 0.9) 50%, 
                rgba(26, 26, 46, 0.9) 100%),
                url('https://images.unsplash.com/photo-1511379938547-c1f69419868d?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80');                
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            text-align: center;
            min-height: 100vh;
            display: flex;
            align-items: center;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at 30% 30%, rgba(255, 255, 255, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 70% 70%, rgba(255, 107, 107, 0.1) 0%, transparent 50%);
            z-index: 1;
        }

        .hero .container {
            position: relative;
            z-index: 2;
            max-width: 800px;
        }

        .hero h1 {
            font-size: 4.5rem;
            margin-bottom: 25px;
            background: linear-gradient(to right, #ffffff, #ffccff);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            animation: fadeInUp 1s ease-out;
        }

        .hero p {
            font-size: 1.5rem;
            max-width: 700px;
            margin: 0 auto 50px;
            color: rgba(255, 255, 255, 0.95);
            text-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
            animation: fadeInUp 1s ease-out 0.2s both;
        }

        .hero .btn {
            font-size: 1.2rem;
            padding: 16px 45px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            animation: fadeInUp 1s ease-out 0.4s both;
            position: relative;
            overflow: hidden;
        }

        .hero .btn::after {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: 0.5s;
        }

        .hero .btn:hover::after {
            left: 100%;
        }

        /* Анимация для героя */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* О группе секция */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-text {
            font-size: 1.1rem;
        }

        .about-image {
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: var(--shadow);
        }

        .about-image img {
            width: 100%;
            height: auto;
            transition: var(--transition);
        }

        .about-image:hover img {
            transform: scale(1.05);
        }

        /* Музыка секция */
        .music {
            background-color: #f8f9fa;
        }

        .platforms-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        .platform-card {
            background-color: white;
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .platform-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }

        .platform-icon {
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 30px;
            text-align: center;
            font-size: 3rem;
        }

        .platform-content {
            padding: 25px;
        }

        .platform-content h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }

        /* Контакты секция */
        .contact-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .contact-info {
            background-color: white;
            padding: 40px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 30px;
        }

        .contact-icon {
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 20px;
            font-size: 1.5rem;
        }

        .contact-text h4 {
            margin-bottom: 5px;
            font-size: 1.2rem;
        }

        .contact-text a {
            color: var(--primary-color);
            font-weight: 600;
        }

        .contact-text a:hover {
            text-decoration: underline;
        }

        /* Футер */
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 70px 0 30px;
        }

        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }

        .footer-logo {
            font-size: 2rem;
            margin-bottom: 20px;
        }

        .social-links {
            display: flex;
            gap: 20px;
            margin: 30px 0;
        }

        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            color: white;
            font-size: 1.3rem;
            transition: var(--transition);
        }

        .social-link:hover {
            background-color: var(--primary-color);
            transform: translateY(-5px);
        }

        .copyright {
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            width: 100%;
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
        }

        /* Адаптивность */
        @media (max-width: 992px) {
            h1 {
                font-size: 3rem;
            }
            
            h2 {
                font-size: 2.2rem;
            }
            
            .hero h1 {
                font-size: 3.5rem;
            }
            
            .about-content {
                grid-template-columns: 1fr;
            }
            
            .platforms-grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }

        @media (max-width: 768px) {
            .header-container {
                flex-wrap: wrap;
            }
            
            .mobile-menu-btn {
                display: block;
                order: 2;
            }
            
            nav {
                width: 100%;
                max-height: 0;
                overflow: hidden;
                transition: max-height 0.5s ease;
                order: 4;
            }
            
            nav.active {
                max-height: 300px;
                margin-top: 20px;
            }
            
            nav ul {
                flex-direction: column;
                gap: 15px;
            }
            
            .language-switcher {
                order: 3;
                margin-left: auto;
            }
            
            .hero {
                padding: 150px 0 80px;
                min-height: 90vh;
                background-attachment: scroll;
            }
            
            .hero h1 {
                font-size: 2.8rem;
            }
            
            .hero p {
                font-size: 1.3rem;
            }
            
            .section {
                padding: 80px 0;
            }
        }

        @media (max-width: 576px) {
            h1 {
                font-size: 2.5rem;
            }
            
            h2 {
                font-size: 2rem;
            }
            
            .hero {
                padding: 130px 0 70px;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .platforms-grid {
                grid-template-columns: 1fr;
            }
            
            .contact-info {
                padding: 25px;
            }
            
            .header-container {
                justify-content: space-between;
            }
            
            .language-switcher {
                margin-left: 10px;
            }
            
            .language-btn {
                padding: 6px 15px;
                font-size: 0.8rem;
            }
        }
    </style>
</head>
<body>
    <!-- Хедер -->
    <header>
        <div class="container header-container">
            <a href="#" class="logo">
                <i class="fas fa-music"></i>
                <span>Tootoday</span>
            </a>
            
            <nav id="mainNav">
                <ul>
                    <li><a href="#about" class="nav-link">О группе</a></li>
                    <li><a href="#music" class="nav-link">Наша музыка</a></li>
                    <li><a href="#contacts" class="nav-link">Контакты</a></li>
                </ul>
            </nav>
            
            <div class="language-switcher" id="languageSwitcher">
                <button class="language-btn active" data-lang="ru">RU</button>
                <button class="language-btn" data-lang="en">EN</button>
            </div>
            
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </header>

    <!-- Главный контент -->
    <main>
        <!-- Герой секция - ИСПРАВЛЕНА И ВОССТАНОВЛЕНА -->
        <section class="hero">
            <div class="container">
                <h1 id="heroTitle">Tootoday</h1>
                <p id="heroSubtitle">Музыкальный коллектив, создающий уникальный электронный звук</p>
                <a href="#music" class="btn" id="listenMusic">Слушать музыку</a>
            </div>
        </section>

        <!-- О группе -->
        <section id="about" class="section">
            <div class="container">
                <h2 id="aboutTitle">О группе</h2>
                <div class="about-content">
                    <div class="about-text">
                        <p id="aboutText1">Tootoday — музыкальный коллектив, основанный в 2017 году в Москве. Изначально это была инструментальная группа, основными инструментами являлись баян и фортепиано. Постепенно фокус сместился в сторону электронной музыки.</p>
                        <p id="aboutText2">Группа объединяет в своём творчестве различные оттенки электронной музыки от легкого Ambient до более тяжелых Dubstep и D'n'B, создавая уникальный стиль, который быстро завоевал популярность среди слушателей.</p>
                        <p id="aboutText3">За время своего существования Tootoday выпустили два студийных альбома и несколько успешных синглов. Участники являются призерами различных музыкальных конкурсов и концертов. Наша музыка звучит на крупнейших стриминговых платформах страны и мира.</p>
                    </div>
                    <div class="about-image">
                        <img src="https://images.unsplash.com/photo-1519281682544-5f37c4b14c47?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80" alt="Группа Tootoday в студии" loading="lazy">
                    </div>
                </div>
            </div>
        </section>

        <!-- Наша музыка -->
        <section id="music" class="section music">
            <div class="container">
                <h2 id="musicTitle">Наша музыка</h2>
                <div class="platforms-grid" id="platformsContainer">
                    <!-- Платформы будут загружены через JavaScript -->
                </div>
            </div>
        </section>

        <!-- Контакты -->
        <section id="contacts" class="section">
            <div class="container">
                <h2 id="contactsTitle">Контакты</h2>
                <div class="contact-content">
                    <div class="contact-info">
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div class="contact-text">
                                <h4 id="emailLabel">Электронная почта</h4>
                                <a href="mailto:tootoday.band@gmail.com">tootoday.band@gmail.com</a>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fab fa-telegram"></i>
                            </div>
                            <div class="contact-text">
                                <h4 id="telegramLabel">Telegram канал</h4>
                                <a href="https://t.me/ToOtOdAy" target="_blank" rel="noopener noreferrer">@ToOtOdAy</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Футер -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">
                    <i class="fas fa-music"></i>
                    <span>Tootoday</span>
                </div>
                <p id="footerText">Слушайте нашу музыку на всех популярных платформах</p>
                <div class="social-links">
                    <a href="https://t.me/Curlykin" class="social-link" target="_blank" rel="noopener noreferrer" aria-label="Telegram">
                        <i class="fab fa-telegram"></i>
                    </a>
                    <a href="https://vk.com/artist/5233716049124375436" class="social-link" target="_blank" rel="noopener noreferrer" aria-label="VKontakte">
                        <i class="fab fa-vk"></i>
                    </a>
                    <a href="https://open.spotify.com/artist/0qLM7oVOVfvIkdBwQnOdO8" class="social-link" target="_blank" rel="noopener noreferrer" aria-label="Spotify">
                        <i class="fab fa-spotify"></i>
                    </a>
                </div>
                <div class="copyright">
                    <p id="copyrightText">© 2023 Tootoday. Все права защищены.</p>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Данные для перевода
        const translations = {
            ru: {
                heroTitle: "Tootoday",
                heroSubtitle: "Музыкальный коллектив, создающий уникальный электронный звук",
                listenMusic: "Слушать музыку",
                aboutTitle: "О группе",
                aboutText1: "Tootoday — музыкальный коллектив, основанный в 2017 году в Москве. Изначально это была инструментальная группа, основными инструментами являлись баян и фортепиано. Постепенно фокус сместился в сторону электронной музыки.",
                aboutText2: "Группа объединяет в своём творчестве различные оттенки электронной музыки от легкого Ambient до более тяжелых Dubstep и D'n'B, создавая уникальный стиль, который быстро завоевал популярность среди слушателей.",
                aboutText3: "За время своего существования Tootoday выпустили два студийных альбома и несколько успешных синглов. Участники являются призерами различных музыкальных конкурсов и концертов. Наша музыка звучит на крупнейших стриминговых платформах страны и мира.",
                musicTitle: "Наша музыка",
                contactsTitle: "Контакты",
                emailLabel: "Электронная почта",
                telegramLabel: "Telegram канал",
                footerText: "Слушайте нашу музыку на всех популярных платформах",
                copyrightText: "© 2023 Tootoday. Все права защищены.",
                navAbout: "О группе",
                navMusic: "Наша музыка",
                navContacts: "Контакты"
            },
            en: {
                heroTitle: "Tootoday",
                heroSubtitle: "Music band creating unique electronic sound",
                listenMusic: "Listen to music",
                aboutTitle: "About Us",
                aboutText1: "Tootoday is a music band founded in 2017 in Moscow. Initially, it was an instrumental group with bayan and piano as the main instruments. Gradually, the focus shifted towards electronic music.",
                aboutText2: "The band combines various shades of electronic music from light Ambient to heavier Dubstep and D'n'B, creating a unique style that quickly gained popularity among listeners.",
                aboutText3: "During its existence, Tootoday has released two studio albums and several successful singles. The members are winners of various music competitions and concerts. Our music is available on the largest streaming platforms in the country and worldwide.",
                musicTitle: "Our Music",
                contactsTitle: "Contacts",
                emailLabel: "Email",
                telegramLabel: "Telegram channel",
                footerText: "Listen to our music on all popular platforms",
                copyrightText: "© 2023 Tootoday. All rights reserved.",
                navAbout: "About",
                navMusic: "Music",
                navContacts: "Contacts"
            }
        };

        // Данные о стриминговых платформах
        const platforms = [
            {
                name: "Яндекс Музыка",
                nameEn: "Yandex Music",
                icon: "fas fa-music",
                url: "https://music.yandex.com/artist/25201658?utm_medium=copy_link&ref_id=ca7872c1-e376-4cdc-8226-7ad588dd86c2",
                color: "#ffcc00"
            },
            {
                name: "Звук",
                nameEn: "Zvuk",
                icon: "fas fa-headphones",
                url: "https://zvuk.com/artist/214040541",
                color: "#00a2ff"
            },
            {
                name: "ВКонтакте",
                nameEn: "VKontakte",
                icon: "fab fa-vk",
                url: "https://vk.com/artist/5233716049124375436",
                color: "#4c75a3"
            },
            {
                name: "МТС Музыка",
                nameEn: "MTS Music",
                icon: "fas fa-signal",
                url: "https://mts-music-spo.onelink.me/sKFX/vkyuavzp",
                color: "#e30613"
            },
            {
                name: "Одноклассники",
                nameEn: "Odnoklassniki",
                icon: "fab fa-odnoklassniki",
                url: "https://m.ok.ru/music/artist/122909431251668?ysclid=mjhi82rvg6276337956",
                color: "#f7931e"
            },
            {
                name: "Spotify",
                nameEn: "Spotify",
                icon: "fab fa-spotify",
                url: "https://open.spotify.com/artist/0qLM7oVOVfvIkdBwQnOdO8?si=zNlUGOTNTHOY0wKfX6-wcg",
                color: "#1db954"
            },
            {
                name: "Amazon Музыка",
                nameEn: "Amazon Music",
                icon: "fab fa-amazon",
                url: "https://music.amazon.com/artists/B0G9MZ5L1D/tootoday?marketplaceId=ART4WZ8MWBX2Y&musicTerritory=MX&ref=dm_sh_XYOF0r1mrtMbG8e14MlaVzdQn",
                color: "#ff9900"
            },
{
                name: "Apple Музыка",
                nameEn: "Apple Music",
                icon: "fab fa-apple",
                url: "https://music.apple.com/us/artist/tootoday/1866143169",
                color: "#000000"
            },
{
  "name": "Band.Link",
  "nameEn": "Band.Link",
  "icon": "fas fa-link",
  "url": "https://band.link/2WkW9",
  "color": "#3d5afe"
}
        ];

        // Текущий язык
        let currentLanguage = 'ru';

        // DOM элементы
        const languageSwitcher = document.getElementById('languageSwitcher');
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const mainNav = document.getElementById('mainNav');
        const platformsContainer = document.getElementById('platformsContainer');
        const navLinks = document.querySelectorAll('.nav-link');

        // Функция инициализации страницы
        function initPage() {
            // Проверяем сохраненный язык в localStorage
            const savedLanguage = localStorage.getItem('tootoday_language');
            if (savedLanguage && (savedLanguage === 'ru' || savedLanguage === 'en')) {
                currentLanguage = savedLanguage;
                updateLanguageButtons();
            }
            
            // Загружаем платформы
            renderPlatforms();
            
            // Применяем текущий язык
            applyLanguage();
            
            // Настраиваем обработчики событий
            setupEventListeners();
        }

        // Функция отрисовки платформ
        function renderPlatforms() {
            platformsContainer.innerHTML = '';
            
            platforms.forEach(platform => {
                const platformCard = document.createElement('div');
                platformCard.className = 'platform-card';
                
                const platformName = currentLanguage === 'ru' ? platform.name : platform.nameEn;
                const buttonText = currentLanguage === 'ru' ? 'Слушать' : 'Listen';
                
                platformCard.innerHTML = `
                    <div class="platform-icon" style="background: ${platform.color || 'linear-gradient(to right, var(--primary-color), var(--secondary-color))'}">
                        <i class="${platform.icon}"></i>
                    </div>
                    <div class="platform-content">
                        <h3>${platformName}</h3>
                        <a href="${platform.url}" target="_blank" rel="noopener noreferrer" class="btn">
                            ${buttonText}
                        </a>
                    </div>
                `;
                
                platformsContainer.appendChild(platformCard);
            });
        }

        // Функция обновления кнопок языка
        function updateLanguageButtons() {
            const buttons = document.querySelectorAll('.language-btn');
            buttons.forEach(button => {
                button.classList.remove('active');
                if (button.getAttribute('data-lang') === currentLanguage) {
                    button.classList.add('active');
                }
            });
        }

        // Функция применения языка
        function applyLanguage() {
            // Обновляем тексты на странице
            document.getElementById('heroTitle').textContent = translations[currentLanguage].heroTitle;
            document.getElementById('heroSubtitle').textContent = translations[currentLanguage].heroSubtitle;
            document.getElementById('listenMusic').textContent = translations[currentLanguage].listenMusic;
            document.getElementById('aboutTitle').textContent = translations[currentLanguage].aboutTitle;
            document.getElementById('aboutText1').textContent = translations[currentLanguage].aboutText1;
            document.getElementById('aboutText2').textContent = translations[currentLanguage].aboutText2;
            document.getElementById('aboutText3').textContent = translations[currentLanguage].aboutText3;
            document.getElementById('musicTitle').textContent = translations[currentLanguage].musicTitle;
            document.getElementById('contactsTitle').textContent = translations[currentLanguage].contactsTitle;
            document.getElementById('emailLabel').textContent = translations[currentLanguage].emailLabel;
            document.getElementById('telegramLabel').textContent = translations[currentLanguage].telegramLabel;
            document.getElementById('footerText').textContent = translations[currentLanguage].footerText;
            document.getElementById('copyrightText').textContent = translations[currentLanguage].copyrightText;
            
            // Обновляем навигацию
            if (navLinks.length >= 3) {
                navLinks[0].textContent = translations[currentLanguage].navAbout;
                navLinks[1].textContent = translations[currentLanguage].navMusic;
                navLinks[2].textContent = translations[currentLanguage].navContacts;
            }
            
            // Обновляем язык HTML элемента
            document.documentElement.lang = currentLanguage;
            
            // Обновляем кнопки языка
            updateLanguageButtons();
            
            // Перерисовываем платформы
            renderPlatforms();
        }

        // Функция переключения языка
        function switchLanguage(lang) {
            if (lang === currentLanguage) return;
            
            currentLanguage = lang;
            localStorage.setItem('tootoday_language', lang);
            applyLanguage();
        }

        // Настройка обработчиков событий
        function setupEventListeners() {
            // Переключатель языка
            document.querySelectorAll('.language-btn').forEach(button => {
                button.addEventListener('click', function() {
                    const lang = this.getAttribute('data-lang');
                    switchLanguage(lang);
                });
            });
            
            // Мобильное меню
            mobileMenuBtn.addEventListener('click', function() {
                mainNav.classList.toggle('active');
                this.innerHTML = mainNav.classList.contains('active') 
                    ? '<i class="fas fa-times"></i>' 
                    : '<i class="fas fa-bars"></i>';
            });
            
            // Закрытие меню при клике на ссылку
            document.querySelectorAll('.nav-link').forEach(link => {
                link.addEventListener('click', function() {
                    mainNav.classList.remove('active');
                    mobileMenuBtn.innerHTML = '<i class="fas fa-bars"></i>';
                });
            });
            
            // Плавная прокрутка для ссылок
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    if (targetId === '#') return;
                    
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                });
            });
        }

        // Инициализация при загрузке страницы
        document.addEventListener('DOMContentLoaded', initPage);
    </script>


<!-- Yandex.Metrika counter -->
<script type="text/javascript">
    (function(m,e,t,r,i,k,a){
        m[i]=m[i]||function(){(m[i].a=m[i].a||[]).push(arguments)};
        m[i].l=1*new Date();
        for (var j = 0; j < document.scripts.length; j++) {if (document.scripts[j].src === r) { return; }}
        k=e.createElement(t),a=e.getElementsByTagName(t)[0],k.async=1,k.src=r,a.parentNode.insertBefore(k,a)
    })(window, document,'script','https://mc.yandex.ru/metrika/tag.js?id=106071419', 'ym');

    ym(106071419, 'init', {ssr:true, webvisor:true, clickmap:true, ecommerce:"dataLayer", accurateTrackBounce:true, trackLinks:true});
</script>
<noscript><div><img src="https://mc.yandex.ru/watch/106071419" style="position:absolute; left:-9999px;" alt="" /></div></noscript>
<!-- /Yandex.Metrika counter -->


    <!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-C4JTXR5M3S"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-C4JTXR5M3S');
</script>

</body>
</html>
