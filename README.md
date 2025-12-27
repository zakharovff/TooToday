<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
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
            color: var(--light);
            background-color: var(--dark);
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 1rem;
        }

        h1 {
            font-size: 3.5rem;
            text-transform: uppercase;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        h2 {
            font-size: 2.5rem;
            position: relative;
            display: inline-block;
            margin-bottom: 2.5rem;
        }

        h2:after {
            content: '';
            position: absolute;
            left: 0;
            bottom: -10px;
            width: 70px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            border-radius: 2px;
        }

        section {
            padding: 5rem 1rem;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }

        .btn {
            display: inline-block;
            padding: 0.8rem 2rem;
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
            font-size: 0.9rem;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }

        .btn-outline:hover {
            background: var(--primary);
            color: white;
        }

        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            padding: 1.5rem 0;
            transition: var(--transition);
        }

        header.scrolled {
            background-color: rgba(18, 18, 18, 0.95);
            padding: 1rem 0;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            text-decoration: none;
        }

        .logo span {
            color: var(--primary);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            text-transform: uppercase;
            font-size: 0.9rem;
            letter-spacing: 1px;
            transition: var(--transition);
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .hamburger {
            display: none;
            cursor: pointer;
            font-size: 1.5rem;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: linear-gradient(rgba(18, 18, 18, 0.8), rgba(18, 18, 18, 0.9)), url('https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            padding-top: 80px;
        }

        .hero-content {
            max-width: 800px;
            padding: 2rem;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            color: #ddd;
        }

        .hero-btns {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
        }

        /* About Section */
        .about {
            background-color: var(--gray);
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-text p {
            margin-bottom: 1.5rem;
            color: #ccc;
        }

        .about-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }

        /* Music Section */
        .music {
            text-align: center;
        }

        .album-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .album-card {
            background-color: var(--gray);
            border-radius: 10px;
            overflow: hidden;
            transition: var(--transition);
        }

        .album-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4);
        }

        .album-img {
            height: 250px;
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
            padding: 1.5rem;
        }

        .album-info h3 {
            color: white;
            margin-bottom: 0.5rem;
        }

        .album-info p {
            color: #aaa;
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        .player {
            background-color: var(--gray);
            border-radius: 10px;
            padding: 2rem;
            max-width: 800px;
            margin: 0 auto;
            text-align: left;
        }

        .track {
            display: flex;
            align-items: center;
            padding: 1rem;
            border-bottom: 1px solid #444;
            cursor: pointer;
            transition: var(--transition);
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
        }

        .track-title {
            flex-grow: 1;
            color: white;
        }

        .track-duration {
            color: #aaa;
        }

        /* Tour Section */
        .tour {
            background-color: var(--gray);
        }

        .tour-dates {
            max-width: 800px;
            margin: 0 auto;
        }

        .tour-date {
            display: flex;
            background-color: var(--dark);
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 1.5rem;
            transition: var(--transition);
        }

        .tour-date:hover {
            transform: translateX(10px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }

        .tour-date-info {
            padding: 1.5rem;
            flex-grow: 1;
        }

        .tour-date-info h3 {
            color: white;
        }

        .tour-date-info p {
            color: #aaa;
            margin-bottom: 0.5rem;
        }

        .tour-date-ticket {
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 1.5rem;
            background-color: var(--primary);
        }

        /* Gallery Section */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1rem;
        }

        .gallery-item {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            height: 250px;
            cursor: pointer;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
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
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
        }

        .contact-info h3 {
            color: white;
            margin-bottom: 1rem;
        }

        .contact-info p {
            color: #aaa;
            margin-bottom: 2rem;
        }

        .social-links {
            display: flex;
            gap: 1rem;
        }

        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background-color: var(--dark);
            border-radius: 50%;
            color: white;
            font-size: 1.2rem;
            transition: var(--transition);
            text-decoration: none;
        }

        .social-link:hover {
            background-color: var(--primary);
            transform: translateY(-5px);
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 1rem;
            margin-bottom: 1.5rem;
            background-color: var(--dark);
            border: 1px solid #444;
            border-radius: 5px;
            color: white;
            font-family: 'Open Sans', sans-serif;
        }

        .contact-form textarea {
            height: 150px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background-color: #0a0a0a;
            padding: 3rem 0;
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }

        .footer-logo {
            font-size: 2rem;
            font-weight: 700;
            color: white;
            margin-bottom: 1.5rem;
        }

        .footer-logo span {
            color: var(--primary);
        }

        .copyright {
            color: #777;
            font-size: 0.9rem;
            margin-top: 2rem;
        }

        /* Responsive Styles */
        @media (max-width: 992px) {
            h1 {
                font-size: 2.8rem;
            }
            
            h2 {
                font-size: 2.2rem;
            }
            
            .about-content,
            .contact-container {
                grid-template-columns: 1fr;
                gap: 3rem;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                position: fixed;
                top: 80px;
                left: 0;
                width: 100%;
                background-color: var(--dark);
                flex-direction: column;
                align-items: center;
                padding: 2rem 0;
                transform: translateY(-100%);
                opacity: 0;
                transition: var(--transition);
                box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            }
            
            .nav-links.active {
                transform: translateY(0);
                opacity: 1;
            }
            
            .nav-links li {
                margin: 1rem 0;
            }
            
            .hamburger {
                display: block;
                color: white;
            }
            
            .hero-btns {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 80%;
                margin-bottom: 1rem;
            }
            
            .tour-date {
                flex-direction: column;
            }
            
            .tour-date-ticket {
                padding: 1rem;
            }
        }

        @media (max-width: 576px) {
            h1 {
                font-size: 2.2rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            section {
                padding: 3rem 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header id="header">
        <div class="nav-container">
            <a href="#" class="logo">TOO<span>TODAY</span></a>
            <div class="hamburger" id="hamburger">
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
                        <img src="https://images.unsplash.com/photo-1493225457124-a3eb161ffa5f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Альбом Эхо времен">
                    </div>
                    <div class="album-info">
                        <h3>Эхо времен</h3>
                        <p>2023 • Альбом</p>
                        <a href="#" class="btn">Слушать</a>
                    </div>
                </div>
                
                <div class="album-card">
                    <div class="album-img">
                        <img src="https://images.unsplash.com/photo-1571974599782-87624638275c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1632&q=80" alt="Альбом Без границ">
                    </div>
                    <div class="album-info">
                        <h3>Без границ</h3>
                        <p>2021 • Альбом</p>
                        <a href="#" class="btn">Слушать</a>
                    </div>
                </div>
                
                <div class="album-card">
                    <div class="album-img">
                        <img src="https://images.unsplash.com/photo-1511379938547-c1f69419868d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Сингл Небесный свет">
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
                <div class="track active">
                    <div class="track-number">01</div>
                    <div class="track-title">Небесный свет</div>
                    <div class="track-duration">3:45</div>
                </div>
                <div class="track">
                    <div class="track-number">02</div>
                    <div class="track-title">Эхо</div>
                    <div class="track-duration">4:12</div>
                </div>
                <div class="track">
                    <div class="track-number">03</div>
                    <div class="track-title">За горизонтом</div>
                    <div class="track-duration">3:58</div>
                </div>
                <div class="track">
                    <div class="track-number">04</div>
                    <div class="track-title">Без границ</div>
                    <div class="track-duration">4:30</div>
                </div>
                <div class="track">
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
                
                <div class="tour-date">
                    <div class="tour-date-info">
                        <h3>Новосибирск, Арена</h3>
                        <p>18 ноября 2023 • 19:00</p>
                        <p>Заключительный концерт тура</p>
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
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1516280440614-37939bbacd81?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Концертное выступление">
                    <div class="gallery-item-overlay">
                        <i class="fas fa-search-plus fa-2x"></i>
                    </div>
                </div>
                
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1470225620780-dba8ba36b745?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Студийная запись">
                    <div class="gallery-item-overlay">
                        <i class="fas fa-search-plus fa-2x"></i>
                    </div>
                </div>
                
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1498038432885-c6f3f1b912ee?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Репетиция">
                    <div class="gallery-item-overlay">
                        <i class="fas fa-search-plus fa-2x"></i>
                    </div>
                </div>
                
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1501612780327-45045538702b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Встреча с фанатами">
                    <div class="gallery-item-overlay">
                        <i class="fas fa-search-plus fa-2x"></i>
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
                        <a href="#" class="social-link"><i class="fab fa-spotify"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-youtube"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-vk"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-telegram"></i></a>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form id="contactForm">
                        <input type="text" placeholder="Ваше имя" required>
                        <input type="email" placeholder="Ваш email" required>
                        <input type="text" placeholder="Тема" required>
                        <textarea placeholder="Ваше сообщение" required></textarea>
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
                <a href="#" class="social-link"><i class="fab fa-spotify"></i></a>
                <a href="#" class="social-link"><i class="fab fa-youtube"></i></a>
                <a href="#" class="social-link"><i class="fab fa-instagram"></i></a>
                <a href="#" class="social-link"><i class="fab fa-vk"></i></a>
                <a href="#" class="social-link"><i class="fab fa-telegram"></i></a>
            </div>
            
            <p class="copyright">&copy; 2023 Tootoday. Все права защищены.</p>
        </div>
    </footer>

    <script>
        // Mobile Navigation Toggle
        const hamburger = document.getElementById('hamburger');
        const navLinks = document.getElementById('navLinks');
        
        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            hamburger.innerHTML = navLinks.classList.contains('active') 
                ? '<i class="fas fa-times"></i>' 
                : '<i class="fas fa-bars"></i>';
        });
        
        // Close mobile menu when clicking on a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
                hamburger.innerHTML = '<i class="fas fa-bars"></i>';
            });
        });
        
        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
        
        // Track player interaction
        document.querySelectorAll('.track').forEach(track => {
            track.addEventListener('click', () => {
                document.querySelectorAll('.track').forEach(t => t.classList.remove('active'));
                track.classList.add('active');
                
                // In a real implementation, this would play the selected track
                // For demo purposes, we'll just show an alert
                const trackTitle = track.querySelector('.track-title').textContent;
                alert(`Воспроизведение: ${trackTitle}\n\nВ реальном приложении здесь бы запустился аудиоплеер.`);
            });
        });
        
        // Form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Спасибо за ваше сообщение! Мы свяжемся с вами в ближайшее время.');
            this.reset();
        });
        
        // Smooth scrolling for anchor links
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
        
        // Gallery image click
        document.querySelectorAll('.gallery-item').forEach(item => {
            item.addEventListener('click', () => {
                alert('В реальном приложении здесь бы открылось модальное окно с увеличенным изображением.');
            });
        });
    </script>
</body>
</html>
