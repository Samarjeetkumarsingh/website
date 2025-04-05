<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Master GATE Metallurgy | TestUrSelf - India's #1 GATE Coaching</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@9/swiper-bundle.min.css">
    <style>
        :root {
            --primary-blue: #176b87;
            --primary-green: #229954;
            --accent-yellow: #f8e71c;
            --dark-blue: #0d47a1;
            --dark-green: #2a7a52;
            --light-bg: #f0f7ff;
            --text-dark: #2d3436;
            --text-light: #e8f9fd;
            --vibrant-blue: #00a8ff;
            --vibrant-green: #00d2d3;
            --box-shadow: 0 15px 30px rgba(0,0,0,0.1);
            --transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.1);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            color: var(--text-dark);
            line-height: 1.7;
            background-color: #f5f5f5;
            overflow-x: hidden;
            position: relative;
        }
        
        /* Animated Gradient Background */
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, #e8f9fd 0%, #d1f5ff 50%, #e8f9fd 100%);
            background-size: 200% 200%;
            animation: gradientBG 15s ease infinite;
            z-index: -2;
        }
        
        @keyframes gradientBG {
            0% {background-position: 0% 50%;}
            50% {background-position: 100% 50%;}
            100% {background-position: 0% 50%;}
        }
        
        /* Watermark */
        body::after {
            content: "TestUrSelf";
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-30deg);
            font-size: 20vw;
            font-weight: bold;
            color: rgba(23, 107, 135, 0.03);
            z-index: -1;
            pointer-events: none;
            white-space: nowrap;
            text-transform: uppercase;
            letter-spacing: 15px;
            width: 200%;
            text-align: center;
        }
        
        /* Navigation */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: linear-gradient(135deg, var(--primary-blue), var(--dark-blue));
            color: white;
            padding: 1rem 2rem;
            z-index: 1000;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: var(--transition);
        }
        
        .navbar.scrolled {
            padding: 0.5rem 2rem;
            background: rgba(23, 107, 135, 0.98);
            backdrop-filter: blur(10px);
        }
        
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 800;
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 10px;
            color: var(--accent-yellow);
            transition: var(--transition);
        }
        
        .logo:hover i {
            transform: rotate(360deg);
        }
        
        .nav-links {
            display: flex;
            gap: 2rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            position: relative;
            padding: 0.5rem 0;
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent-yellow);
            transition: var(--transition);
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .nav-links a:hover {
            color: var(--accent-yellow);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero-section {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 120px 2rem 80px;
            position: relative;
            overflow: hidden;
        }
        
        .hero-content {
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
            position: relative;
            z-index: 2;
        }
        
        .hero-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(rgba(23, 107, 135, 0.85), rgba(34, 153, 84, 0.85)), 
                        url('https://images.unsplash.com/photo-1581094794329-c8112a89af12?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            z-index: -1;
        }
        
        .hero-bg::after {
            content: "";
            position: absolute;
            bottom: -5px;
            left: 0;
            right: 0;
            height: 20px;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none"><path d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z" opacity=".25" fill="%23f0f7ff"></path><path d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z" opacity=".5" fill="%23f0f7ff"></path><path d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z" fill="%23f0f7ff"></path></svg>') no-repeat center bottom;
            background-size: cover;
        }
        
        .hero-section h1 {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            font-weight: 800;
            line-height: 1.2;
            text-shadow: 0 2px 4px rgba(0,0,0,0.2);
            background: linear-gradient(to right, white, var(--accent-yellow));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: fadeInUp 1s ease;
        }
        
        .hero-section h1 span {
            color: var(--accent-yellow);
            background: transparent;
            -webkit-background-clip: initial;
            background-clip: initial;
        }
        
        .hero-section p {
            font-size: 1.4rem;
            opacity: 0.95;
            max-width: 800px;
            margin: 0 auto 2.5rem;
            text-shadow: 0 1px 3px rgba(0,0,0,0.2);
            animation: fadeInUp 1s ease 0.2s forwards;
            opacity: 0;
        }
        
        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 2rem;
            animation: fadeInUp 1s ease 0.4s forwards;
            opacity: 0;
        }
        
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 16px 40px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.1rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: var(--transition);
            min-width: 220px;
            text-align: center;
        }
        
        .btn-primary {
            background-color: var(--accent-yellow);
            color: var(--primary-blue);
        }
        
        .btn-primary:hover {
            background-color: #e6d41a;
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 30px rgba(248, 231, 28, 0.4);
        }
        
        .btn-secondary {
            background-color: rgba(255,255,255,0.15);
            color: white;
            border: 2px solid rgba(255,255,255,0.3);
        }
        
        .btn-secondary:hover {
            background-color: rgba(255,255,255,0.25);
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 30px rgba(255,255,255,0.2);
        }
        
        /* Stats Bar */
        .stats-section {
            padding: 4rem 2rem;
            background-color: white;
            position: relative;
            z-index: 1;
        }
        
        .stats-container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .stats-bar {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 2rem;
        }
        
        .stat-card {
            background: white;
            padding: 30px 25px;
            border-radius: 12px;
            box-shadow: var(--box-shadow);
            transition: var(--transition);
            position: relative;
            overflow: hidden;
            text-align: center;
            border: 1px solid rgba(0,0,0,0.05);
        }
        
        .stat-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--primary-blue), var(--primary-green));
            transition: var(--transition);
        }
        
        .stat-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }
        
        .stat-number {
            font-size: 3rem;
            font-weight: 800;
            color: var(--primary-blue);
            line-height: 1;
            margin-bottom: 0.5rem;
            transition: var(--transition);
        }
        
        .stat-card:hover .stat-number {
            color: var(--primary-green);
        }
        
        .stat-label {
            font-weight: 600;
            color: var(--primary-green);
            transition: var(--transition);
        }
        
        .stat-card:hover .stat-label {
            color: var(--primary-blue);
        }
        
        /* Methodology Section */
        .methodology-section {
            padding: 6rem 2rem;
            position: relative;
            background-color: white;
        }
        
        .section-header {
            text-align: center;
            max-width: 1200px;
            margin: 0 auto 4rem;
        }
        
        .section-header h2 {
            font-size: 2.8rem;
            color: var(--dark-blue);
            margin-bottom: 1rem;
            font-weight: 800;
            position: relative;
            display: inline-block;
        }
        
        .section-header h2 span {
            color: var(--dark-green);
        }
        
        .section-header p {
            font-size: 1.3rem;
            color: var(--text-dark);
            max-width: 800px;
            margin: 0 auto;
        }
        
        .features-container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .feature-card {
            background: white;
            padding: 2.5rem;
            border-radius: 16px;
            box-shadow: var(--box-shadow);
            position: relative;
            overflow: hidden;
            transition: var(--transition);
            border-top: 5px solid var(--dark-blue);
            border: 1px solid rgba(0,0,0,0.05);
        }
        
        .feature-card.green {
            border-top: 5px solid var(--dark-green);
        }
        
        .feature-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 25px 50px rgba(0,0,0,0.15);
        }
        
        .feature-header {
            display: flex;
            align-items: flex-start;
            margin-bottom: 1.5rem;
        }
        
        .feature-icon {
            background: #e3f2fd;
            width: 70px;
            height: 70px;
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 1.5rem;
            font-size: 2rem;
            color: var(--dark-blue);
            transition: var(--transition);
        }
        
        .feature-card:hover .feature-icon {
            transform: scale(1.1) rotate(10deg);
        }
        
        .feature-card.green .feature-icon {
            background: #e8f5e9;
            color: var(--dark-green);
        }
        
        .feature-title {
            color: var(--dark-blue);
            margin: 0;
            font-size: 1.6rem;
            font-weight: 700;
            transition: var(--transition);
        }
        
        .feature-card:hover .feature-title {
            color: var(--primary-blue);
        }
        
        .feature-card.green .feature-title {
            color: var(--dark-green);
        }
        
        .feature-card.green:hover .feature-title {
            color: var(--primary-green);
        }
        
        .feature-list {
            padding-left: 1.5rem;
            margin: 0;
            color: var(--text-dark);
        }
        
        .feature-list li {
            margin-bottom: 1rem;
            position: relative;
            padding-left: 1.5rem;
            font-size: 1.05rem;
        }
        
        .feature-list li::before {
            content: "";
            position: absolute;
            left: 0;
            top: 0.7rem;
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background-color: var(--dark-blue);
            transition: var(--transition);
        }
        
        .feature-card:hover .feature-list li::before {
            transform: scale(1.5);
        }
        
        .feature-card.green .feature-list li::before {
            background-color: var(--dark-green);
        }
        
        .feature-list strong {
            color: var(--dark-green);
            font-weight: 600;
        }
        
        .feature-card.green .feature-list strong {
            color: var(--dark-blue);
        }
        
        /* Testimonials Section */
        .testimonials-section {
            padding: 6rem 0;
            background: linear-gradient(135deg, var(--light-bg) 0%, #e8f5ee 100%);
            position: relative;
            overflow: hidden;
        }
        
        .testimonials-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        .testimonials-header {
            text-align: center;
            margin-bottom: 4rem;
        }
        
        .testimonials-header h3 {
            color: var(--primary-blue);
            font-size: 2.5rem;
            margin-bottom: 1rem;
            font-weight: 800;
        }
        
        .testimonials-header h3 span {
            color: var(--primary-green);
        }
        
        .testimonials-header p {
            text-align: center;
            max-width: 700px;
            margin: 0 auto;
            font-size: 1.2rem;
            color: var(--text-dark);
        }
        
        .swiper {
            width: 100%;
            padding: 2rem 0 4rem;
        }
        
        .testimonial-card {
            background: white;
            padding: 2.5rem;
            border-radius: 16px;
            box-shadow: var(--box-shadow);
            position: relative;
            transition: var(--transition);
            margin: 0 1rem;
            height: auto;
        }
        
        .testimonial-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--primary-blue), var(--primary-green));
            transition: var(--transition);
        }
        
        .testimonial-text {
            font-style: italic;
            color: var(--text-dark);
            font-size: 1.1rem;
            margin-bottom: 2rem;
            line-height: 1.8;
            position: relative;
            padding-left: 1.5rem;
        }
        
        .testimonial-text::before {
            content: """;
            position: absolute;
            left: 0;
            top: -0.5rem;
            font-size: 3rem;
            color: var(--primary-blue);
            opacity: 0.2;
            font-family: serif;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-avatar {
            width: 60px;
            height: 60px;
            background: var(--primary-blue);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            margin-right: 1.5rem;
            font-size: 1.5rem;
            flex-shrink: 0;
        }
        
        .author-info p {
            margin: 0;
        }
        
        .author-name {
            font-weight: 700;
            color: var(--primary-blue);
        }
        
        .author-rank {
            color: var(--primary-green);
            font-size: 0.95rem;
        }
        
        .swiper-pagination {
            position: relative;
            bottom: 0;
            margin-top: 2rem;
        }
        
        .swiper-pagination-bullet {
            width: 12px;
            height: 12px;
            background-color: var(--primary-blue);
            opacity: 0.3;
            transition: var(--transition);
        }
        
        .swiper-pagination-bullet-active {
            background-color: var(--primary-blue);
            opacity: 1;
            transform: scale(1.2);
        }
        
        /* Final CTA */
        .final-cta {
            padding: 8rem 2rem;
            background: linear-gradient(135deg, var(--primary-blue) 0%, var(--primary-green) 100%);
            color: white;
            text-align: center;
            position: relative;
            overflow: hidden;
            clip-path: polygon(0 10%, 100% 0, 100% 100%, 0% 100%);
        }
        
        .final-cta::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(to right, var(--accent-yellow), rgba(255,255,255,0.5));
        }
        
        .cta-container {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
            z-index: 2;
        }
        
        .final-cta h2 {
            font-size: 2.8rem;
            margin-bottom: 1.5rem;
            font-weight: 800;
            line-height: 1.3;
        }
        
        .final-cta p {
            font-size: 1.3rem;
            max-width: 700px;
            margin: 0 auto 2.5rem;
            opacity: 0.95;
        }
        
        .cta-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        
        /* Floating Particles */
        .particles {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
            overflow: hidden;
        }
        
        .particle {
            position: absolute;
            background: rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            animation: float-particle 15s infinite linear;
        }
        
        @keyframes float-particle {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-1000px) rotate(720deg);
                opacity: 0;
            }
        }
        
        /* Animations */
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
        
        @keyframes pulse {
            0% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.05);
            }
            100% {
                transform: scale(1);
            }
        }
        
        /* Responsive Adjustments */
        @media (max-width: 992px) {
            .hero-section h1 {
                font-size: 2.8rem;
            }
            
            .section-header h2 {
                font-size: 2.2rem;
            }
            
            .final-cta h2 {
                font-size: 2.2rem;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero-section {
                padding: 100px 1.5rem 60px;
            }
            
            .hero-section h1 {
                font-size: 2.2rem;
            }
            
            .hero-section p {
                font-size: 1.1rem;
            }
            
            .section-header h2 {
                font-size: 1.8rem;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
            
            .final-cta h2 {
                font-size: 1.8rem;
            }
            
            .final-cta p {
                font-size: 1.1rem;
            }
        }
        
        @media (max-width: 576px) {
            .hero-buttons, .cta-buttons {
                flex-direction: column;
                gap: 15px;
            }
            
            .btn {
                width: 100%;
            }
            
            .stats-bar {
                grid-template-columns: 1fr 1fr;
            }
            
            .hero-section h1 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar">
        <div class="nav-container">
            <a href="#" class="logo">
                <i class="fas fa-atom"></i> TestUrSelf
            </a>
            <div class="nav-links">
                <a href="#methodology">Methodology</a>
                <a href="#testimonials">Success Stories</a>
                <a href="https://online.testurself.in" target="_blank">Courses</a>
                <a href="#cta">Contact</a>
            </div>
            <button class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero-section">
        <div class="hero-bg"></div>
        <div class="particles" id="hero-particles"></div>
        
        <div class="hero-content">
            <h1>Master <span>GATE Metallurgy</span> with TestUrSelf's Proven System</h1>
            <p>7 Consecutive Years Producing AIR-1 | 5000+ Successful Students | India's Best Platform</p>
            
            <div class="hero-buttons">
                <a href="https://online.testurself.in" target="_blank" rel="noopener" class="btn btn-primary">
                    EXPLORE PROGRAM <i class="fas fa-arrow-right"></i>
                </a>
                <a href="#testimonials" class="btn btn-secondary">
                    SEE RESULTS <i class="fas fa-star"></i>
                </a>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats-section">
        <div class="stats-container">
            <div class="stats-bar">
                <div class="stat-card">
                    <div class="stat-number" data-count="7">0</div>
                    <div class="stat-label">Years of Excellence</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number" data-count="8">0</div>
                    <div class="stat-label">AIR-1 Produced</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number" data-count="5000">0+</div>
                    <div class="stat-label">Successful Students</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number" data-count="460">0+</div>
                    <div class="stat-label">in Top 100</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Methodology Section -->
    <section class="methodology-section" id="methodology">
        <div class="section-header">
            <h2>Our <span>Winning</span> Methodology</h2>
            <p>Proven strategies that have consistently produced top rankers in GATE Metallurgical Engineering</p>
        </div>
        
        <div class="features-container">
            <!-- Row 1 -->
            <div class="features-grid">
                <!-- Feature 1 -->
                <div class="feature-card">
                    <div class="feature-header">
                        <div class="feature-icon">
                            <i class="fas fa-book"></i>
                        </div>
                        <h3 class="feature-title">Concept-Driven Content</h3>
                    </div>
                    <ul class="feature-list">
                        <li>Complete <strong>GATE syllabus coverage</strong> with depth</li>
                        <li>Expert-designed <strong>study materials</strong> by GATE toppers</li>
                        <li>Regular <strong>content updates</strong> matching latest patterns</li>
                    </ul>
                </div>
                
                <!-- Feature 2 -->
                <div class="feature-card green">
                    <div class="feature-header">
                        <div class="feature-icon">
                            <i class="fas fa-mobile-alt"></i>
                        </div>
                        <h3 class="feature-title">Smart Learning Resources</h3>
                    </div>
                    <ul class="feature-list">
                        <li><strong>Mobile-friendly</strong> platform for learning anywhere</li>
                        <li>Optimized <strong>test schedules</strong> for maximum retention</li>
                        <li>Dedicated <strong>student support</strong> team available 24/7</li>
                    </ul>
                </div>
            </div>
            
            <!-- Row 2 -->
            <div class="features-grid">
                <!-- Feature 3 -->
                <div class="feature-card">
                    <div class="feature-header">
                        <div class="feature-icon">
                            <i class="fas fa-pen-fancy"></i>
                        </div>
                        <h3 class="feature-title">Real Exam Test Series</h3>
                    </div>
                    <ul class="feature-list">
                        <li>IIT/IISc designed <strong>mock tests</strong> with actual difficulty levels</li>
                        <li>Detailed <strong>solution analysis</strong> for every question</li>
                        <li>Advanced <strong>performance tracking</strong> with heatmaps</li>
                    </ul>
                </div>
                
                <!-- Feature 4 -->
                <div class="feature-card green">
                    <div class="feature-header">
                        <div class="feature-icon">
                            <i class="fas fa-chart-pie"></i>
                        </div>
                        <h3 class="feature-title">Performance Analytics</h3>
                    </div>
                    <ul class="feature-list">
                        <li>Compare with <strong>top rankers</strong> across India</li>
                        <li>Detailed <strong>strength analysis</strong> by topic</li>
                        <li>Personalized <strong>improvement plans</strong> generated weekly</li>
                    </ul>
                </div>
            </div>
            
            <!-- Row 3 -->
            <div class="features-grid">
                <!-- Feature 5 -->
                <div class="feature-card">
                    <div class="feature-header">
                        <div class="feature-icon">
                            <i class="fas fa-brain"></i>
                        </div>
                        <h3 class="feature-title">Expert Doubt Resolution</h3>
                    </div>
                    <ul class="feature-list">
                        <li>24/7 access to <strong>subject experts</strong> via chat</li>
                        <li>Personalized <strong>concept clarification</strong> sessions</li>
                    </ul>
                </div>
                
                <!-- Feature 6 -->
                <div class="feature-card green">
                    <div class="feature-header">
                        <div class="feature-icon">
                            <i class="fas fa-trophy"></i>
                        </div>
                        <h3 class="feature-title">PYQ Bank & Solutions</h3>
                    </div>
                    <ul class="feature-list">
                        <li>Complete <strong>previous year papers</strong> (2010-2024)</li>
                        <li>Detailed <strong>trend analysis</strong> of important topics</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="testimonials-section" id="testimonials">
        <div class="particles" id="testimonial-particles"></div>
        <div class="testimonials-container">
            <div class="testimonials-header">
                <h3>What Our <span>Top Rankers</span> Say</h3>
                <p>Hear from students who achieved AIR-1 using TestUrSelf's GATE Metallurgy program</p>
            </div>
            
            <!-- Swiper Testimonials -->
            <div class="swiper mySwiper">
                <div class="swiper-wrapper">
                    <div class="swiper-slide">
                        <div class="testimonial-card">
                            <p class="testimonial-text">The test series of TestUrSelf was very helpful as it helped in analysing my weak and strong topics. It provided a similar platform as the actual GATE exam and helped in clearing my doubts. The test series had a range of questions from easy to hard which made me mentally strong to tackle any sort of paper in the actual exam.</p>
                            
                            <div class="testimonial-author">
                                <div class="author-avatar">JG</div>
                                <div class="author-info">
                                    <p class="author-name">Jaya Gupta</p>
                                    <p class="author-rank">AIR-1 GATE Metallurgy 2020</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="swiper-slide">
                        <div class="testimonial-card">
                            <p class="testimonial-text">I had taken the test series and practise question series (PQS) of TestUrSelf. The quantity and quality of questions in both of these was very good. The test series and practise questions helped me to find out my weak and strong topics and thus helped me to decide which topic I need to focus more on.</p>
                            
                            <div class="testimonial-author">
                                <div class="author-avatar">HP</div>
                                <div class="author-info">
                                    <p class="author-name">Hrutidipan Pradhan</p>
                                    <p class="author-rank">AIR-1 GATE Metallurgy 2024</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="swiper-slide">
                        <div class="testimonial-card">
                            <p class="testimonial-text">The comprehensive study material provided by TestUrSelf covered all aspects of the syllabus. The regular doubt clearing sessions with faculty were extremely helpful. The mock tests were perfectly timed to help me build my exam temperament.</p>
                            
                            <div class="testimonial-author">
                                <div class="author-avatar">SK</div>
                                <div class="author-info">
                                    <p class="author-name">Sanjay Kumar</p>
                                    <p class="author-rank">AIR-3 GATE Metallurgy 2022</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="swiper-slide">
                        <div class="testimonial-card">
                            <p class="testimonial-text">What I loved most about TestUrSelf was the personalized attention. The performance analytics helped me identify my weak areas and the faculty provided targeted guidance. The previous year question bank was a goldmine for preparation.</p>
                            
                            <div class="testimonial-author">
                                <div class="author-avatar">PM</div>
                                <div class="author-info">
                                    <p class="author-name">Priya Mishra</p>
                                    <p class="author-rank">AIR-7 GATE Metallurgy 2023</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="swiper-pagination"></div>
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section class="final-cta" id="cta">
        <div class="particles" id="cta-particles"></div>
        <div class="cta-container">
            <h2>Ready to Transform Your GATE Preparation?</h2>
            <p>Join thousands of Metallurgy aspirants who achieved their dream ranks with TestUrSelf</p>
            <div class="cta-buttons">
                <a href="https://online.testurself.in" class="btn btn-primary">
                    START YOUR JOURNEY NOW <i class="fas fa-arrow-right"></i>
                </a>
                <a href="#testimonials" class="btn btn-secondary">
                    SEE MORE RESULTS <i class="fas fa-star"></i>
                </a>
            </div>
        </div>
    </section>

    <!-- Scripts -->
    <script src="https://cdn.jsdelivr.net/npm/swiper@9/swiper-bundle.min.js"></script>
    <script>
        // Initialize Swiper Testimonials
        const swiper = new Swiper(".mySwiper", {
            slidesPerView: 1,
            spaceBetween: 30,
            loop: true,
            autoplay: {
                delay: 5000,
                disableOnInteraction: false,
            },
            pagination: {
                el: ".swiper-pagination",
                clickable: true,
            },
            breakpoints: {
                768: {
                    slidesPerView: 2,
                }
            }
        });
        
        // Animated Counter for Stats
        function animateCounters() {
            const counters = document.querySelectorAll('.stat-number');
            const speed = 200;
            
            counters.forEach(counter => {
                const target = +counter.getAttribute('data-count');
                const count = +counter.innerText.replace('+', '');
                const increment = target / speed;
                
                if (count < target) {
                    counter.innerText = Math.ceil(count + increment);
                    if (counter.getAttribute('data-count').includes('+')) {
                        counter.innerText += '+';
                    }
                    setTimeout(animateCounters, 1);
                } else {
                    counter.innerText = target;
                    if (counter.getAttribute('data-count').includes('+')) {
                        counter.innerText += '+';
                    }
                }
            });
        }
        
        // Intersection Observer for Animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: "0px 0px -100px 0px"
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate');
                    if (entry.target.classList.contains('stats-bar')) {
                        animateCounters();
                    }
                }
            });
        }, observerOptions);
        
        // Observe sections
        document.querySelectorAll('.stats-bar, .section-header, .feature-card, .testimonials-header').forEach(section => {
            observer.observe(section);
        });
        
        // Create floating particles
        function createParticles(containerId, count) {
            const container = document.getElementById(containerId);
            if (!container) return;
            
            for (let i = 0; i < count; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                
                // Random size between 2px and 6px
                const size = Math.random() * 4 + 2;
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                
                // Random position
                particle.style.left = `${Math.random() * 100}%`;
                particle.style.top = `${Math.random() * 100}%`;
                
                // Random animation duration between 10s and 20s
                const duration = Math.random() * 10 + 10;
                particle.style.animationDuration = `${duration}s`;
                
                // Random delay
                particle.style.animationDelay = `${Math.random() * 5}s`;
                
                // Random opacity
                particle.style.opacity = Math.random() * 0.3 + 0.1;
                
                container.appendChild(particle);
            }
        }
        
        // Initialize particles when page loads
        window.addEventListener('load', () => {
            createParticles('hero-particles', 30);
            createParticles('testimonial-particles', 20);
            createParticles('cta-particles', 15);
            
            // Animate hero elements sequentially
            const heroElements = document.querySelectorAll('.hero-section h1, .hero-section p, .hero-buttons');
            heroElements.forEach((el, index) => {
                el.style.animation = `fadeInUp 1s ease ${index * 0.2}s forwards`;
            });
        });
        
        // Navbar scroll effect
        window.addEventListener('scroll', () => {
            const navbar = document.querySelector('.navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });
        
        // Mobile menu toggle
        const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
        const navLinks = document.querySelector('.nav-links');
        
        mobileMenuBtn.addEventListener('click', () => {
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    if (navLinks.style.display === 'flex') {
                        navLinks.style.display = 'none';
                    }
                }
            });
        });
    </script>
</body>
</html>
