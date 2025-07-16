<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LUXE ESTATES - Ultra-Premium Real Estate</title>
    <style>
    <link rel="stylesheet" href="luxe-estates.css">
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@300;400;500;600&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-gold: #D4AF37;
            --dark-gold: #B8941F;
            --charcoal: #1A1A1A;
            --dark-grey: #2C2C2C;
            --light-grey: #F8F8F8;
            --white: #FFFFFF;
            --accent-blue: #0F4C75;
            --text-light: #666666;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: var(--charcoal);
            scroll-behavior: smooth;
            background: var(--white);
        }

        /* Luxury Header */
        header {
            background: rgba(26, 26, 26, 0.95);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            color: var(--white);
            padding: 1.5rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
            transition: all 0.3s ease;
        }

        nav {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 3rem;
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 2.2rem;
            font-weight: 700;
            color: var(--primary-gold);
            text-decoration: none;
            letter-spacing: 2px;
            position: relative;
        }

        .logo::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 100%;
            height: 2px;
            background: linear-gradient(90deg, var(--primary-gold), transparent);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 3rem;
        }

        .nav-links a {
            color: var(--white);
            text-decoration: none;
            font-weight: 400;
            font-size: 1rem;
            position: relative;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .nav-links a::before {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 50%;
            width: 0;
            height: 2px;
            background: var(--primary-gold);
            transition: all 0.3s ease;
            transform: translateX(-50%);
        }

        .nav-links a:hover::before {
            width: 100%;
        }

        .nav-links a:hover {
            color: var(--primary-gold);
        }

        /* Luxury Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, rgba(0,0,0,0.7), rgba(15,76,117,0.4)), 
                        url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1920 1080"><defs><linearGradient id="skyGrad" x1="0%" y1="0%" x2="0%" y2="100%"><stop offset="0%" style="stop-color:%23001122;stop-opacity:1" /><stop offset="100%" style="stop-color:%23004488;stop-opacity:1" /></linearGradient></defs><rect fill="url(%23skyGrad)" width="1920" height="1080"/><g opacity="0.8"><rect fill="%23333" x="200" y="600" width="300" height="400"/><rect fill="%23444" x="220" y="620" width="50" height="80"/><rect fill="%23444" x="290" y="620" width="50" height="80"/><rect fill="%23444" x="370" y="620" width="50" height="80"/><rect fill="%23444" x="450" y="620" width="50" height="80"/><rect fill="%23D4AF37" x="240" y="750" width="200" height="250"/><rect fill="%23222" x="600" y="500" width="400" height="500"/><rect fill="%23444" x="620" y="520" width="60" height="100"/><rect fill="%23444" x="700" y="520" width="60" height="100"/><rect fill="%23444" x="780" y="520" width="60" height="100"/><rect fill="%23444" x="860" y="520" width="60" height="100"/><rect fill="%23D4AF37" x="640" y="700" width="320" height="300"/><circle fill="%23FFD700" cx="200" cy="150" r="60" opacity="0.6"/></g></svg>');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: var(--white);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at center, transparent 0%, rgba(0,0,0,0.3) 100%);
            pointer-events: none;
        }

        .hero-content {
            max-width: 800px;
            padding: 0 2rem;
            position: relative;
            z-index: 2;
            animation: fadeInUp 1s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero-content h1 {
            font-family: 'Playfair Display', serif;
            font-size: 4.5rem;
            font-weight: 700;
            margin-bottom: 1.5rem;
            text-shadow: 2px 2px 10px rgba(0,0,0,0.5);
            letter-spacing: 2px;
            line-height: 1.2;
        }

        .hero-content .subtitle {
            font-size: 1.4rem;
            margin-bottom: 3rem;
            color: var(--primary-gold);
            font-weight: 300;
            letter-spacing: 1px;
            text-shadow: 1px 1px 5px rgba(0,0,0,0.5);
        }

        .luxury-cta {
            background: linear-gradient(135deg, var(--primary-gold), var(--dark-gold));
            color: var(--charcoal);
            padding: 1.2rem 3rem;
            font-size: 1.1rem;
            font-weight: 600;
            border: 2px solid var(--primary-gold);
            border-radius: 0;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            transition: all 0.4s ease;
            text-transform: uppercase;
            letter-spacing: 2px;
            position: relative;
            overflow: hidden;
        }

        .luxury-cta::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
            transition: left 0.6s ease;
        }

        .luxury-cta:hover::before {
            left: 100%;
        }

        .luxury-cta:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.4);
            background: var(--white);
            color: var(--charcoal);
        }

        /* Premium Section Styling */
        .section {
            padding: 8rem 0;
            max-width: 1400px;
            margin: 0 auto;
            padding-left: 3rem;
            padding-right: 3rem;
        }

        .section h2 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            font-weight: 600;
            margin-bottom: 3rem;
            text-align: center;
            color: var(--charcoal);
            position: relative;
            letter-spacing: 1px;
        }

        .section h2::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: linear-gradient(90deg, var(--primary-gold), var(--dark-gold));
        }

        /* Luxury About Section */
        .about {
            background: linear-gradient(135deg, var(--light-grey), var(--white));
            position: relative;
        }

        .about::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="50" cy="50" r="1" fill="%23D4AF37" opacity="0.1"/></svg>');
            background-size: 50px 50px;
            pointer-events: none;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 5rem;
            align-items: center;
            position: relative;
            z-index: 1;
        }

        .about-text {
            padding: 2rem;
        }

        .about-text p {
            font-size: 1.2rem;
            line-height: 1.8;
            margin-bottom: 2rem;
            color: var(--text-light);
            font-weight: 300;
        }

        .about-text p:first-child {
            font-size: 1.3rem;
            color: var(--charcoal);
        }

        .luxury-stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .stat {
            text-align: center;
            padding: 2rem 1rem;
            background: var(--white);
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .stat:hover {
            transform: translateY(-5px);
        }

        .stat-number {
            font-family: 'Playfair Display', serif;
            font-size: 3rem;
            font-weight: 700;
            color: var(--primary-gold);
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: 1rem;
            color: var(--text-light);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .about-image {
            background: linear-gradient(135deg, var(--charcoal), var(--dark-grey));
            height: 500px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary-gold);
            position: relative;
            overflow: hidden;
            box-shadow: 0 20px 50px rgba(0,0,0,0.2);
        }

        .about-image::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(45deg, transparent, rgba(212, 175, 55, 0.1), transparent);
            animation: shimmer 3s infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        .about-image-content {
            text-align: center;
            z-index: 1;
        }

        .about-image-content h3 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .about-image-content p {
            font-size: 1.2rem;
            font-weight: 300;
        }

        /* Premium Location Cards */
        .location-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 3rem;
            margin-top: 4rem;
        }

        .location-card {
            background: var(--white);
            border-radius: 20px;
            padding: 3rem;
            box-shadow: 0 20px 50px rgba(0,0,0,0.1);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(212, 175, 55, 0.2);
        }

        .location-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(90deg, var(--primary-gold), var(--dark-gold));
        }

        .location-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 30px 60px rgba(0,0,0,0.15);
        }

        .location-card h3 {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            color: var(--charcoal);
            margin-bottom: 1.5rem;
            font-weight: 600;
        }

        .location-card p {
            font-size: 1.1rem;
            line-height: 1.7;
            color: var(--text-light);
            margin-bottom: 1.5rem;
        }

        .price-tag {
            background: linear-gradient(135deg, var(--primary-gold), var(--dark-gold));
            color: var(--charcoal);
            padding: 1rem 2rem;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1.1rem;
            display: inline-block;
            letter-spacing: 1px;
        }

        /* Luxury Planning Section */
        .planning {
            background: var(--charcoal);
            color: var(--white);
            position: relative;
        }

        .planning::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, transparent, rgba(212, 175, 55, 0.05), transparent);
            pointer-events: none;
        }

        .planning h2 {
            color: var(--white);
        }

        .planning-steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
            margin-top: 4rem;
            position: relative;
            z-index: 1;
        }

        .step {
            background: linear-gradient(135deg, var(--dark-grey), var(--charcoal));
            padding: 3rem;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 20px 50px rgba(0,0,0,0.3);
            transition: all 0.4s ease;
            position: relative;
            border: 1px solid rgba(212, 175, 55, 0.2);
        }

        .step:hover {
            transform: translateY(-10px);
            box-shadow: 0 30px 60px rgba(0,0,0,0.4);
        }

        .step-number {
            background: linear-gradient(135deg, var(--primary-gold), var(--dark-gold));
            color: var(--charcoal);
            width: 80px;
            height: 80px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 2rem;
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            font-weight: 700;
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.3);
        }

        .step h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            color: var(--primary-gold);
            margin-bottom: 1.5rem;
            font-weight: 600;
        }

        .step p {
            font-size: 1.1rem;
            line-height: 1.7;
            color: #CCCCCC;
            font-weight: 300;
        }

        /* Luxury Footer */
        footer {
            background: linear-gradient(135deg, var(--charcoal), #0A0A0A);
            color: var(--white);
            padding: 5rem 0 2rem;
            position: relative;
        }

        footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 1px;
            background: linear-gradient(90deg, transparent, var(--primary-gold), transparent);
        }

        .footer-content {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 3rem;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 3rem;
        }

        .footer-section h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            margin-bottom: 2rem;
            color: var(--primary-gold);
            font-weight: 600;
        }

        .footer-section p, .footer-section a {
            color: #CCCCCC;
            text-decoration: none;
            margin-bottom: 1rem;
            display: block;
            font-size: 1rem;
            transition: color 0.3s ease;
        }

        .footer-section a:hover {
            color: var(--primary-gold);
        }

        .footer-bottom {
            border-top: 1px solid rgba(212, 175, 55, 0.2);
            margin-top: 3rem;
            padding-top: 2rem;
            text-align: center;
            color: #999999;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero-content h1 {
                font-size: 3rem;
            }

            .about-content {
                grid-template-columns: 1fr;
                gap: 3rem;
            }

            .luxury-stats {
                grid-template-columns: 1fr;
            }

            .section {
                padding: 4rem 2rem;
            }

            .section h2 {
                font-size: 2.5rem;
            }

            nav {
                padding: 0 2rem;
            }

            .footer-content {
                padding: 0 2rem;
            }
        }

        /* Scroll animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Luxury Header -->
    <header>
        <nav>
            <a href="#home" class="logo">LUXE ESTATES</a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#location">Locations</a></li>
                <li><a href="#planning">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Luxury Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>ULTRA-PREMIUM ESTATES</h1>
            <p class="subtitle">Where Luxury Meets Perfection</p>
            <a href="#about" class="luxury-cta">Discover Excellence</a>
        </div>
    </section>

    <!-- Premium About Section -->
    <section id="about" class="section about fade-in">
        <h2>Redefining Luxury Living</h2>
        <div class="about-content">
            <div class="about-text">
                <p>For over two decades, LUXE ESTATES has been the epitome of ultra-premium real estate, curating the world's most exclusive properties for discerning clientele.</p>
                <p>Our portfolio features architectural masterpieces, waterfront sanctuaries, and private estates that represent the pinnacle of sophisticated living. Each property is meticulously selected to offer unparalleled luxury, privacy, and prestige.</p>
                <p>We don't just sell properties – we craft lifestyle experiences that exceed the expectations of the world's most successful individuals.</p>
                
                <div class="luxury-stats">
                    <div class="stat">
                        <div class="stat-number">$2.8B</div>
                        <div class="stat-label">Sales Volume</div>
                 
