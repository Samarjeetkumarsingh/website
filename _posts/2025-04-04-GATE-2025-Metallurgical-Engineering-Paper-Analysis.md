<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GATE 2025 Metallurgical Engineering Paper Analysis | TestUrSelf</title>
    <style>
        :root {
            --primary-color: #0a4d68;
            --secondary-color: #05bfdb;
            --accent-color: #00ffca;
            --light-color: #e8f9fd;
            --dark-color: #088395;
            --text-color: #1e1e1e;
            --highlight-color: #ffd700;
            --success-color: #4caf50;
            --thermal-color: #ff5722;
            --fluid-color: #2196f3;
            --mass-color: #8bc34a;
            --kinetics-color: #9c27b0;
            --vibrant-blue: #00a8ff;
            --vibrant-green: #00d2d3;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.8;
            color: var(--text-color);
            max-width: 1200px;
            margin: 0 auto;
            padding: 0;
            background-color: #f5f5f5;
            position: relative;
            overflow-x: hidden;
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
        
        /* Large Diagonal Watermark */
        body::after {
            content: "TestUrSelf";
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-30deg);
            font-size: 120px;
            font-weight: bold;
            color: rgba(10, 77, 104, 0.05);
            z-index: -1;
            pointer-events: none;
            white-space: nowrap;
            text-transform: uppercase;
            letter-spacing: 15px;
            width: 200%;
            text-align: center;
        }
        
        /* Navigation */
        nav {
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            color: white;
            padding: 1rem 2rem;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
            border-bottom: 3px solid var(--accent-color);
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
            font-weight: bold;
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 10px;
            color: var(--accent-color);
        }
        
        .nav-links {
            display: flex;
            gap: 2rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
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
            background-color: var(--accent-color);
            transition: width 0.3s ease;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .nav-links a:hover {
            color: var(--accent-color);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            color: white;
            padding: 5rem 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
            clip-path: polygon(0 0, 100% 0, 100% 90%, 0 100%);
            margin-bottom: -50px;
        }
        
        .hero::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('https://images.unsplash.com/photo-1635070041078-e363dbe005cb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80') center/cover;
            opacity: 0.2;
            z-index: 0;
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            background: linear-gradient(to right, var(--accent-color), var(--secondary-color));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            display: inline-block;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }
        
        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            margin-top: 2rem;
        }
        
        .btn {
            padding: 0.8rem 1.8rem;
            border-radius: 50px;
            font-weight: bold;
            text-decoration: none;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            justify-content: center;
        }
        
        .btn-primary {
            background-color: var(--accent-color);
            color: var(--primary-color);
            box-shadow: 0 4px 15px rgba(0, 255, 202, 0.4);
        }
        
        .btn-primary:hover {
            background-color: #00e5b7;
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0, 255, 202, 0.6);
        }
        
        .btn-secondary {
            background-color: transparent;
            border: 2px solid var(--accent-color);
            color: var(--accent-color);
        }
        
        .btn-secondary:hover {
            background-color: rgba(0, 255, 202, 0.1);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 255, 202, 0.3);
        }
        
        /* Floating Elements Animation */
        .floating-elements {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            overflow: hidden;
            z-index: 0;
        }
        
        .floating-element {
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: float 15s infinite linear;
        }
        
        @keyframes float {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-1000px) rotate(720deg);
                opacity: 0;
            }
        }
        
        /* Section Styling */
        .section {
            background-color: white;
            border-radius: 12px;
            padding: 3rem;
            margin: 2rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.08);
            position: relative;
            z-index: 1;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(0,0,0,0.05);
            overflow: hidden;
        }
        
        .section::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--accent-color), var(--secondary-color));
        }
        
        .section:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 35px rgba(0,0,0,0.12);
        }
        
        h2 {
            color: var(--primary-color);
            border-bottom: 3px solid var(--accent-color);
            padding-bottom: 0.8rem;
            margin-top: 0;
            font-size: 2.2rem;
            background: linear-gradient(to right, transparent, var(--light-color), transparent);
            padding: 1rem 0;
            text-align: center;
            border-radius: 8px;
            position: relative;
        }
        
        h2::after {
            content: "";
            position: absolute;
            bottom: -3px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: var(--accent-color);
        }
        
        h3 {
            color: var(--dark-color);
            margin-top: 2.5rem;
            font-size: 1.8rem;
            border-left: 5px solid var(--accent-color);
            padding-left: 1.5rem;
            position: relative;
        }
        
        h3::before {
            content: "";
            position: absolute;
            left: 0;
            bottom: -5px;
            width: 50%;
            height: 2px;
            background: linear-gradient(to right, var(--accent-color), transparent);
        }
        
        /* Paper Analysis Section */
        .analysis-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .subject-card {
            background: white;
            border-radius: 8px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            border-top: 4px solid var(--primary-color);
            position: relative;
            overflow: hidden;
        }
        
        .subject-card::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--accent-color), var(--secondary-color));
            transition: all 0.3s ease;
            transform: scaleX(0);
            transform-origin: left;
        }
        
        .subject-card:hover::after {
            transform: scaleX(1);
        }
        
        .subject-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }
        
        .subject-card h3 {
            color: var(--primary-color);
            margin-top: 0;
            border-left: none;
            padding-left: 0;
            font-size: 1.5rem;
            display: flex;
            align-items: center;
        }
        
        .subject-card h3 i {
            margin-right: 10px;
            color: var(--accent-color);
        }
        
        .marks-distribution {
            margin-top: 1.5rem;
        }
        
        .marks-distribution h4 {
            color: var(--dark-color);
            margin-bottom: 0.5rem;
        }
        
        .marks-bar {
            height: 20px;
            background-color: #f0f0f0;
            border-radius: 10px;
            margin-bottom: 1rem;
            overflow: hidden;
            box-shadow: inset 0 1px 3px rgba(0,0,0,0.1);
        }
        
        .marks-fill {
            height: 100%;
            background: linear-gradient(to right, var(--secondary-color), var(--accent-color));
            border-radius: 10px;
            transition: width 1s ease;
            position: relative;
            overflow: hidden;
        }
        
        .marks-fill::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(90deg, rgba(255,255,255,0) 0%, rgba(255,255,255,0.3) 50%, rgba(255,255,255,0) 100%);
            animation: shine 2s infinite;
        }
        
        @keyframes shine {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }
        
        /* Charts Section */
        .charts-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .chart-card {
            background: white;
            border-radius: 8px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            border: 1px solid rgba(0,0,0,0.05);
            position: relative;
            overflow: hidden;
        }
        
        .chart-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--accent-color), var(--secondary-color));
        }
        
        .chart-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }
        
        .chart-title {
            text-align: center;
            margin-bottom: 1.5rem;
            color: var(--primary-color);
            font-size: 1.5rem;
            position: relative;
            display: inline-block;
            width: 100%;
        }
        
        .chart-title::after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 3px;
            background: var(--accent-color);
        }
        
        /* TestUrSelf Advantage */
        .advantage-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .advantage-card {
            background: white;
            border-radius: 8px;
            padding: 2rem;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            border: 1px solid rgba(0,0,0,0.05);
            position: relative;
            overflow: hidden;
        }
        
        .advantage-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--accent-color), var(--secondary-color));
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.3s ease;
        }
        
        .advantage-card:hover::before {
            transform: scaleX(1);
        }
        
        .advantage-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }
        
        .advantage-icon {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 1.5rem;
            transition: all 0.3s ease;
            display: inline-block;
        }
        
        .advantage-card:hover .advantage-icon {
            transform: scale(1.2) rotate(5deg);
            color: var(--accent-color);
        }
        
        .advantage-card h4 {
            font-size: 1.4rem;
            margin-top: 0;
            margin-bottom: 1rem;
            color: var(--dark-color);
            position: relative;
            display: inline-block;
        }
        
        .advantage-card h4::after {
            content: "";
            position: absolute;
            bottom: -5px;
            left: 50%;
            transform: translateX(-50%);
            width: 30px;
            height: 2px;
            background: var(--accent-color);
            transition: width 0.3s ease;
        }
        
        .advantage-card:hover h4::after {
            width: 60px;
        }
        
        /* CTA Sections */
        .cta-section {
            text-align: center;
            padding: 4rem 2rem;
            position: relative;
            overflow: hidden;
        }
        
        .cta-section.dark {
            background-color: var(--dark-color);
            color: white;
        }
        
        .cta-section.gradient {
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            color: white;
            clip-path: polygon(0 10%, 100% 0, 100% 100%, 0% 100%);
            padding: 6rem 2rem 4rem;
        }
        
        /* Footer */
        footer {
            background-color: var(--primary-color);
            color: white;
            padding: 4rem 2rem;
            position: relative;
            clip-path: polygon(0 0, 100% 5%, 100% 100%, 0% 100%);
            margin-top: -50px;
            padding-top: 6rem;
        }
        
        footer::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 10px;
            background: linear-gradient(to right, var(--accent-color), var(--secondary-color));
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .footer-column h3 {
            color: white;
            border-left: none;
            padding-left: 0;
            font-size: 1.3rem;
            margin-bottom: 1.5rem;
            position: relative;
            display: inline-block;
        }
        
        .footer-column h3::after {
            content: "";
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 40px;
            height: 2px;
            background: var(--accent-color);
        }
        
        .footer-column h3::before {
            display: none;
        }
        
        .footer-column ul {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        
        .footer-column li {
            margin-bottom: 0.8rem;
            transition: all 0.3s ease;
            position: relative;
            padding-left: 15px;
        }
        
        .footer-column li::before {
            content: "→";
            position: absolute;
            left: 0;
            color: var(--accent-color);
            opacity: 0;
            transition: all 0.3s ease;
        }
        
        .footer-column li:hover {
            transform: translateX(5px);
        }
        
        .footer-column li:hover::before {
            opacity: 1;
            left: -5px;
        }
        
        .footer-column a {
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-column a:hover {
            color: var(--accent-color);
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .social-links a {
            color: white;
            font-size: 1.2rem;
            transition: all 0.3s ease;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255,255,255,0.1);
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .social-links a:hover {
            color: var(--accent-color);
            transform: translateY(-3px);
            background: rgba(255,255,255,0.2);
        }
        
        .footer-bottom {
            text-align: center;
            margin-top: 3rem;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
        }
        
        /* Floating Particles */
        .particles {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            overflow: hidden;
        }
        
        .particle {
            position: absolute;
            background: rgba(255, 255, 255, 0.5);
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
        
        /* Responsive Adjustments */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .section {
                padding: 2rem 1rem;
                margin: 1rem;
            }
            
            .charts-container {
                grid-template-columns: 1fr;
            }
            
            .footer-container {
                grid-template-columns: 1fr 1fr;
            }
            
            .cta-buttons {
                flex-direction: column;
            }
            
            .hero {
                clip-path: polygon(0 0, 100% 0, 100% 95%, 0 100%);
            }
            
            footer {
                clip-path: polygon(0 0, 100% 5%, 100% 100%, 0% 100%);
            }
        }
        
        @media (max-width: 480px) {
            .footer-container {
                grid-template-columns: 1fr;
            }
            
            .hero h1 {
                font-size: 1.8rem;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <a href="#" class="logo">
                <i class="fas fa-atom"></i> TestUrSelf
            </a>
            <div class="nav-links">
                <a href="#analysis">Paper Analysis</a>
                <a href="#charts">Visual Data</a>
                <a href="#advantage">Our Advantage</a>
                <a href="#cta">Resources</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="floating-elements">
            <div class="floating-element" style="width: 20px; height: 20px; left: 10%; animation-delay: 0s;"></div>
            <div class="floating-element" style="width: 30px; height: 30px; left: 25%; animation-delay: 2s;"></div>
            <div class="floating-element" style="width: 25px; height: 25px; left: 50%; animation-delay: 4s;"></div>
            <div class="floating-element" style="width: 40px; height: 40px; left: 70%; animation-delay: 6s;"></div>
            <div class="floating-element" style="width: 15px; height: 15px; left: 90%; animation-delay: 8s;"></div>
        </div>
        
        <div class="hero-content">
            <h1>GATE 2025 Metallurgical Engineering Paper Analysis</h1>
            <p>Detailed breakdown of expected question distribution and marks weightage based on previous patterns</p>
            <div class="cta-buttons">
                <a href="#analysis" class="btn btn-primary">
                    <i class="fas fa-chart-bar mr-2"></i> View Analysis
                </a>
                <a href="#cta" class="btn btn-secondary">
                    <i class="fas fa-download mr-2"></i> Get Preparation Kit
                </a>
            </div>
        </div>
    </section>

    <!-- Dynamic Countdown Section -->
    <section class="section" style="background: linear-gradient(135deg, var(--primary-color), var(--dark-color)); color: white;">
        <div class="countdown-container" style="display: flex; justify-content: space-around; text-align: center;">
            <div class="countdown-item">
                <div class="countdown-number" id="days" style="font-size: 3rem; font-weight: bold; color: var(--accent-color);">308</div>
                <div class="countdown-label" style="font-size: 1.2rem;">Days</div>
            </div>
            <div class="countdown-item">
                <div class="countdown-number" id="hours" style="font-size: 3rem; font-weight: bold; color: var(--accent-color);">7400</div>
                <div class="countdown-label" style="font-size: 1.2rem;">Hours</div>
            </div>
            <div class="countdown-item">
                <div class="countdown-number" id="minutes" style="font-size: 3rem; font-weight: bold; color: var(--accent-color);">444414</div>
                <div class="countdown-label" style="font-size: 1.2rem;">Minutes</div>
            </div>
            <div class="countdown-item">
                <div class="countdown-number" id="seconds" style="font-size: 3rem; font-weight: bold; color: var(--accent-color);">26664800</div>
                <div class="countdown-label" style="font-size: 1.2rem;">Seconds</div>
            </div>
        </div>
        <h3 style="text-align: center; margin-top: 2rem; color: white; border-left: none;">Until GATE 2026 Exam</h3>
    </section>

    <!-- Paper Analysis Section -->
    <section id="analysis" class="section">
        <h2>GATE 2026 Metallurgy Expected Paper Pattern</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">Based on analysis of previous years' papers and expert predictions</p>
        
        <div class="analysis-container">
            <div class="subject-card">
                <h3><i class="fas fa-brain"></i> General Aptitude</h3>
                <p>10 Marks (5 Questions × 1 Mark + 5 Questions × 2 Marks)</p>
                <div class="marks-distribution">
                    <h4>Marks Distribution:</h4>
                    <div class="marks-bar">
                        <div class="marks-fill" style="width: 100%"></div>
                    </div>
                    <p>1 Mark Questions: 5 | 2 Mark Questions: 5</p>
                </div>
            </div>
            
            <div class="subject-card">
                <h3><i class="fas fa-square-root-alt"></i> Engineering Mathematics</h3>
                <p>13 Marks (3 Questions × 1 Mark + 5 Questions × 2 Marks)</p>
                <div class="marks-distribution">
                    <h4>Marks Distribution:</h4>
                    <div class="marks-bar">
                        <div class="marks-fill" style="width: 65%"></div>
                    </div>
                    <p>1 Mark Questions: 3 | 2 Mark Questions: 5</p>
                </div>
            </div>
            
            <div class="subject-card">
                <h3><i class="fas fa-fire"></i> Metallurgical Thermodynamics</h3>
                <p>14-17 Marks (5 Questions × 1 Mark + 6 Questions × 2 Marks)</p>
                <div class="marks-distribution">
                    <h4>Marks Distribution:</h4>
                    <div class="marks-bar">
                        <div class="marks-fill" style="width: 85%"></div>
                    </div>
                    <p>1 Mark Questions: 5 | 2 Mark Questions: 6</p>
                </div>
            </div>
            
            <div class="subject-card">
                <h3><i class="fas fa-exchange-alt"></i> Transport Phenomena</h3>
                <p>9-12 Marks (3 Questions × 1 Mark + 4 Questions × 2 Marks)</p>
                <div class="marks-distribution">
                    <h4>Marks Distribution:</h4>
                    <div class="marks-bar">
                        <div class="marks-fill" style="width: 55%"></div>
                    </div>
                    <p>1 Mark Questions: 3 | 2 Mark Questions: 4</p>
                </div>
            </div>
            
            <div class="subject-card">
                <h3><i class="fas fa-flask"></i> Extractive Metallurgy</h3>
                <p>6-9 Marks (3 Questions × 1 Mark + 2 Questions × 2 Marks)</p>
                <div class="marks-distribution">
                    <h4>Marks Distribution:</h4>
                    <div class="marks-bar">
                        <div class="marks-fill" style="width: 45%"></div>
                    </div>
                    <p>1 Mark Questions: 3 | 2 Mark Questions: 2</p>
                </div>
            </div>
            
            <div class="subject-card">
                <h3><i class="fas fa-atom"></i> Physical Metallurgy</h3>
                <p>12-16 Marks (4 Questions × 1 Mark + 6 Questions × 2 Marks)</p>
                <div class="marks-distribution">
                    <h4>Marks Distribution:</h4>
                    <div class="marks-bar">
                        <div class="marks-fill" style="width: 80%"></div>
                    </div>
                    <p>1 Mark Questions: 4 | 2 Mark Questions: 6</p>
                </div>
            </div>
            
            <div class="subject-card">
                <h3><i class="fas fa-hard-hat"></i> Mechanical Metallurgy</h3>
                <p>15-20 Marks (4 Questions × 1 Mark + 7 Questions × 2 Marks)</p>
                <div class="marks-distribution">
                    <h4>Marks Distribution:</h4>
                    <div class="marks-bar">
                        <div class="marks-fill" style="width: 100%"></div>
                    </div>
                    <p>1 Mark Questions: 4 | 2 Mark Questions: 7</p>
                </div>
            </div>
            
            <div class="subject-card">
                <h3><i class="fas fa-industry"></i> Manufacturing Processes</h3>
                <p>7-10 Marks (2 Questions × 1 Mark + 3 Questions × 2 Marks)</p>
                <div class="marks-distribution">
                    <h4>Marks Distribution:</h4>
                    <div class="marks-bar">
                        <div class="marks-fill" style="width: 50%"></div>
                    </div>
                    <p>1 Mark Questions: 2 | 2 Mark Questions: 3</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Charts Section -->
    <section id="charts" class="section">
        <h2>Visual Representation of GATE 2025 Metallurgy Paper</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">Interactive charts showing subject-wise distribution and question types</p>
        
        <div class="charts-container">
            <div class="chart-card">
                <h3 class="chart-title">Subject-wise Marks Distribution</h3>
                <canvas id="marksDistributionChart"></canvas>
            </div>
            <div class="chart-card">
                <h3 class="chart-title">Question Type Distribution</h3>
                <canvas id="questionTypeChart"></canvas>
            </div>
            <div class="chart-card">
                <h3 class="chart-title">Expected Difficulty Level</h3>
                <canvas id="difficultyChart"></canvas>
            </div>
            <div class="chart-card">
                <h3 class="chart-title">Topic Priority for Preparation</h3>
                <canvas id="priorityChart"></canvas>
            </div>
        </div>
    </section>

    <!-- TestUrSelf Advantage -->
    <section id="advantage" class="section">
        <h2>Why TestUrSelf Covers Maximum GATE Questions</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">Our materials are designed to match the exact pattern of GATE Metallurgy papers</p>
        
        <div class="advantage-container">
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-chart-line"></i>
                </div>
                <h4>Pattern Analysis</h4>
                <p>Our team analyzes 25+ years of GATE papers to predict question patterns accurately.</p>
            </div>
            
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-book"></i>
                </div>
                <h4>Comprehensive Coverage</h4>
                <p>Study material covers all topics with exact depth required for GATE examination.</p>
            </div>
            
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-clipboard-check"></i>
                </div>
                <h4>PYQ Focus</h4>
                <p>Previous year questions with solutions help understand recurring concepts.</p>
            </div>
            
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-tasks"></i>
                </div>
                <h4>Mock Tests</h4>
                <p>25+ full-length tests designed by Top rankers matching GATE difficulty.</p>
            </div>
            
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-lightbulb"></i>
                </div>
                <h4>Concept Clarity</h4>
                <p>Focus on fundamental concepts that form the basis of most GATE questions.</p>
            </div>
            
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-award"></i>
                </div>
                <h4>Proven Results</h4>
                <p>Our students consistently score higher with many securing top ranks.</p>
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section id="cta" class="cta-section gradient">
        <div class="particles" id="particles-js"></div>
        <h2 style="color: white; border-bottom-color: var(--accent-color);">Start Your GATE 2026 Metallurgy Preparation Today!</h2>
        <p style="max-width: 700px; margin: 0 auto 2rem;">Get our specially designed study material that covers maximum GATE questions</p>
        
        <div class="cta-buttons">
            <a href="#" class="btn btn-primary">
                <i class="fas fa-book-open mr-2"></i> Download Study Plan
            </a>
            <a href="#" class="btn btn-secondary">
                <i class="fas fa-video mr-2"></i> Free Video Lectures
            </a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-container">
            <div class="footer-column">
                <h3>TestUrSelf</h3>
                <p>India's most trusted GATE Metallurgy preparation platform since 2018.</p>
                <div class="social-links">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    <a href="#"><i class="fab fa-youtube"></i></a>
                </div>
            </div>
            
            <div class="footer-column">
                <h3>Quick Links</h3>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">About Us</a></li>
                    <li><a href="#">Courses</a></li>
                    <li><a href="#">Test Series</a></li>
                    <li><a href="#">Results</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </div>
            
            <div class="footer-column">
                <h3>Resources</h3>
                <ul>
                    <li><a href="#">Blog</a></li>
                    <li><a href="#">Free Materials</a></li>
                    <li><a href="#">Video Lectures</a></li>
                    <li><a href="#">PYQ Solutions</a></li>
                    <li><a href="#">GATE Syllabus</a></li>
                    <li><a href="#">FAQs</a></li>
                </ul>
            </div>
            
            <div class="footer-column">
                <h3>Contact Us</h3>
                <ul>
                    <li><i class="fas fa-map-marker-alt mr-2"></i> Delhi, India</li>
                    <li><i class="fas fa-phone-alt mr-2"></i> +91 9876543210</li>
                    <li><i class="fas fa-envelope mr-2"></i> info@testurself.in</li>
                </ul>
            </div>
        </div>
        
        <div class="footer-bottom">
            <p>&copy; TestUrSelf. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        // Set the date we're counting down to (GATE 2025 exam date - assumed to be Feb 2, 2025)
        const countDownDate = new Date("Feb 2, 2025 09:00:00").getTime();

        // Update the countdown every 1 second
        const countdownFunction = setInterval(function() {
            // Get today's date and time
            const now = new Date().getTime();
            
            // Find the distance between now and the countdown date
            const distance = countDownDate - now;
            
            // Time calculations for days, hours, minutes and seconds
            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);
            
            // Output the result in elements with id="days", "hours", "minutes", "seconds"
            document.getElementById("days").innerHTML = days.toString().padStart(2, '0');
            document.getElementById("hours").innerHTML = hours.toString().padStart(2, '0');
            document.getElementById("minutes").innerHTML = minutes.toString().padStart(2, '0');
            document.getElementById("seconds").innerHTML = seconds.toString().padStart(2, '0');
            
            // If the countdown is finished, write some text 
            if (distance < 0) {
                clearInterval(countdownFunction);
                document.getElementById("days").innerHTML = "00";
                document.getElementById("hours").innerHTML = "00";
                document.getElementById("minutes").innerHTML = "00";
                document.getElementById("seconds").innerHTML = "00";
            }
        }, 1000);

        // Create floating particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles-js');
            const particleCount = 30;
            
            for (let i = 0; i < particleCount; i++) {
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
                particle.style.opacity = Math.random() * 0.5 + 0.1;
                
                particlesContainer.appendChild(particle);
            }
        }

        // Charts Data
        const marksDistributionData = {
            labels: [
                'General Aptitude',
                'Engineering Maths',
                'Metallurgical Thermodynamics',
                'Transport Phenomena',
                'Extractive Metallurgy',
                'Physical Metallurgy',
                'Mechanical Metallurgy',
                'Manufacturing Processes'
            ],
            datasets: [{
                data: [10, 13, 17, 11, 6, 13, 18, 8],
                backgroundColor: [
                    '#0a4d68',
                    '#05bfdb',
                    '#00ffca',
                    '#088395',
                    '#00d2d3',
                    '#00a8ff',
                    '#8bc34a',
                    '#9c27b0'
                ],
                borderWidth: 1
            }]
        };

        const questionTypeData = {
            labels: ['1 Mark Questions', '2 Mark Questions'],
            datasets: [{
                data: [29, 38],
                backgroundColor: ['#0a4d68', '#05bfdb'],
                borderWidth: 1
            }]
        };

        const difficultyData = {
            labels: ['Easy (30%)', 'Medium (50%)', 'Hard (20%)'],
            datasets: [{
                data: [30, 50, 20],
                backgroundColor: ['#00ffca', '#05bfdb', '#0a4d68'],
                borderWidth: 1
            }]
        };

        const priorityData = {
            labels: ['High Priority', 'Medium Priority', 'Low Priority'],
            datasets: [{
                data: [50, 30, 20],
                backgroundColor: ['#0a4d68', '#05bfdb', '#00ffca'],
                borderWidth: 1
            }]
        };

        // Initialize Charts
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            
            // Marks Distribution Chart
            const marksCtx = document.getElementById('marksDistributionChart').getContext('2d');
            new Chart(marksCtx, {
                type: 'bar',
                data: marksDistributionData,
                options: {
                    responsive: true,
                    plugins: {
                        legend: {
                            display: false
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `${context.label}: ${context.raw} Marks`;
                                }
                            }
                        }
                    },
                    scales: {
                        y: {
                            beginAtZero: true,
                            title: {
                                display: true,
                                text: 'Marks'
                            }
                        }
                    }
                }
            });

            // Question Type Chart
            const questionCtx = document.getElementById('questionTypeChart').getContext('2d');
            new Chart(questionCtx, {
                type: 'pie',
                data: questionTypeData,
                options: {
                    responsive: true,
                    plugins: {
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `${context.label}: ${context.raw} Questions`;
                                }
                            }
                        }
                    }
                }
            });

            // Difficulty Chart
            const difficultyCtx = document.getElementById('difficultyChart').getContext('2d');
            new Chart(difficultyCtx, {
                type: 'doughnut',
                data: difficultyData,
                options: {
                    responsive: true,
                    plugins: {
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `${context.label}: ${context.raw}% of paper`;
                                }
                            }
                        }
                    }
                }
            });

            // Priority Chart
            const priorityCtx = document.getElementById('priorityChart').getContext('2d');
            new Chart(priorityCtx, {
                type: 'polarArea',
                data: priorityData,
                options: {
                    responsive: true,
                    plugins: {
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `${context.label}: ${context.raw}% of syllabus`;
                                }
                            }
                        }
                    }
                }
            });

            // Animate marks bars on scroll
            const marksBars = document.querySelectorAll('.marks-fill');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        const width = entry.target.style.width;
                        entry.target.style.width = '0';
                        setTimeout(() => {
                            entry.target.style.width = width;
                        }, 100);
                    }
                });
            }, { threshold: 0.5 });
            
            marksBars.forEach(bar => {
                observer.observe(bar);
            });
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    targetElement.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>
