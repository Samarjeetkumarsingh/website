<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hall of Fame | GATE Champions | TestUrSelf</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
     <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        :root {
            --electric-blue: #0061ff;
            --neon-pink: #ff00aa;
            --cyber-purple: #8a2be2;
            --holographic-teal: #00f5d4;
            --matrix-green: #00ff41;
            --dark-matter: #121212;
            --carbon-fiber: #1e1e1e;
            --plasma-glow: rgba(0, 255, 209, 0.15);
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--dark-matter);
            color: white;
            margin: 0 auto;
            padding: 0rem;
            overflow-x: hidden;
            width: 100% !important;
            max-width: 96% !important
        }
        
        /* Cyberpunk Glow Effect */
        @keyframes cyber-glow {
            0% { text-shadow: 0 0 5px var(--holographic-teal), 0 0 10px var(--holographic-teal); }
            50% { text-shadow: 0 0 20px var(--neon-pink), 0 0 30px var(--neon-pink); }
            100% { text-shadow: 0 0 5px var(--holographic-teal), 0 0 10px var(--holographic-teal); }
        }
        
        /* Grid Background */
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                linear-gradient(rgba(18, 18, 18, 0.9), rgba(18, 18, 18, 0.9)),
                url('data:image/svg+xml;utf8,<svg width="100" height="100" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><path d="M0 0h100v100H0z" fill="none"/><path d="M0 0v100M20 0v100M40 0v100M60 0v100M80 0v100M100 0v100M0 0h100M0 20h100M0 40h100M0 60h100M0 80h100M0 100h100" stroke="rgba(255,255,255,0.05)" stroke-width="0.5"/></svg>');
            z-index: -2;
        }
        
        /* Holographic Scanline Effect */
        @keyframes scanline {
            0% { background-position: 0 0; }
            100% { background-position: 0 100vh; }
        }
        
        .scanlines {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                linear-gradient(to bottom, 
                    transparent 0%, 
                    rgba(0, 245, 212, 0.03) 50%, 
                    transparent 100%);
            background-size: 100% 8px;
            animation: scanline 1s linear infinite;
            pointer-events: none;
            z-index: -1;
            opacity: 0.3;
            width:100%
        }
        
        /* Main Container */
        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        /* Hero Section */
        .hero {
            text-align: center;
            padding: 6rem 2rem;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: "";
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle at center, var(--plasma-glow) 0%, transparent 70%);
            animation: rotate 20s linear infinite;
            z-index: -1;
        }
        
        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        .hero h1 {
            font-size: 4.5rem;
            font-weight: 800;
            margin: 0;
            background: linear-gradient(to right, var(--holographic-teal), var(--neon-pink));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-transform: uppercase;
            letter-spacing: 2px;
            animation: cyber-glow 3s infinite;
        }
        
        .hero p {
            font-size: 1.5rem;
            width:100%
            margin: 1.5rem auto;
            color: rgba(255,255,255,0.8);
        }
        
        .hero-stats {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 3rem;
            flex-wrap: wrap;
        }
        
        .stat-bubble {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 50px;
            padding: 1rem 2rem;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .stat-bubble i {
            color: var(--holographic-teal);
        }
        
        /* Champions Wall Section */
        .champions-wall {
            position: relative;
            padding: 4rem 0;
        }
        
        .section-header {
            text-align: center;
            margin-bottom: 4rem;
            position: relative;
        }
        
        .section-header h2 {
            font-size: 3rem;
            font-weight: 800;
            margin: 0;
            text-transform: uppercase;
            letter-spacing: 3px;
            background: linear-gradient(to right, var(--electric-blue), var(--cyber-purple));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            display: inline-block;
        }
        
        .section-header h2::after {
            content: "";
            display: block;
            width: 100px;
            height: 5px;
            background: linear-gradient(to right, var(--electric-blue), var(--cyber-purple));
            margin: 1rem auto;
            border-radius: 5px;
        }
        
        .section-header p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 1rem auto 0;
            color: rgba(255,255,255,0.7);
        }
        
        /* Champions Grid */
        .champions-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
            position: relative;
        }
        
        .champion-card {
            background: rgba(30, 30, 30, 0.7);
            border-radius: 15px;
            overflow: hidden;
            border: 1px solid rgba(255,255,255,0.1);
            transition: all 0.3s ease;
            position: relative;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }
        
        .champion-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(to right, var(--electric-blue), var(--cyber-purple));
        }
        
        .champion-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 97, 255, 0.2);
            border-color: rgba(0, 245, 212, 0.3);
        }
        
        .champion-header {
            padding: 1.5rem;
            text-align: center;
            position: relative;
        }
        
        .champion-year {
            font-size: 1rem;
            font-weight: 600;
            color: var(--holographic-teal);
            margin-bottom: 0.5rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .champion-rank {
            display: inline-block;
            background: rgba(0, 255, 209, 0.1);
            color: var(--holographic-teal);
            padding: 0.3rem 1.2rem;
            border-radius: 50px;
            font-weight: 700;
            font-size: 0.9rem;
            margin-bottom: 1rem;
            border: 1px solid var(--holographic-teal);
        }
        
        .champion-photo {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            margin: 0 auto;
            overflow: hidden;
            border: 3px solid rgba(255,255,255,0.1);
            box-shadow: 0 5px 20px rgba(0,0,0,0.3);
            position: relative;
        }
        
        .champion-photo::before {
            content: "";
            position: absolute;
            top: -3px;
            left: -3px;
            right: -3px;
            bottom: -3px;
            border-radius: 50%;
            background: linear-gradient(45deg, var(--electric-blue), var(--neon-pink));
            z-index: -1;
            opacity: 0.7;
        }
        
        .champion-photo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .champion-body {
            padding: 1.5rem;
            background: rgba(0,0,0,0.3);
            text-align: center;
        }
        
        .champion-name {
            font-size: 1.5rem;
            font-weight: 700;
            margin: 0 0 0.5rem;
            color: white;
        }
        
        .champion-branch {
            font-size: 1rem;
            color: rgba(255,255,255,0.7);
            margin-bottom: 1.5rem;
        }
        
        .champion-stats {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-bottom: 1.5rem;
        }
        
        .stat-item {
            text-align: center;
        }
        
        .stat-value {
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--holographic-teal);
        }
        
        .stat-label {
            font-size: 0.8rem;
            color: rgba(255,255,255,0.6);
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .champion-score {
            background: rgba(0, 255, 209, 0.1);
            color: var(--holographic-teal);
            padding: 0.8rem;
            border-radius: 6px;
            font-weight: 600;
            display: inline-block;
            border: 1px solid rgba(0, 255, 209, 0.3);
        }
        
        /* Performance Milestones Section */
        .performance-milestones {
            padding: 6rem 0;
            background: rgba(0,0,0,0.3);
            position: relative;
            overflow: hidden;
        }
        
        .performance-container {
            display: flex;
            align-items: center;
            gap: 4rem;
            flex-wrap: wrap;
        }
        
        .performance-content {
            flex: 1;
            min-width: 300px;
        }
        
        .performance-stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .performance-stat {
            background: rgba(255,255,255,0.05);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 10px;
            padding: 1.5rem;
            transition: all 0.3s ease;
        }
        
        .performance-stat:hover {
            background: rgba(0, 97, 255, 0.1);
            border-color: var(--electric-blue);
            transform: translateY(-5px);
        }
        
        .performance-stat h3 {
            font-size: 1.2rem;
            margin: 0 0 0.5rem;
            color: var(--holographic-teal);
        }
        
        .performance-stat p {
            margin: 0;
            color: rgba(255,255,255,0.8);
        }
        
        .chart-container {
            flex: 1;
            min-width: 300px;
            position: relative;
        }
        
        .chart-wrapper {
            background: rgba(30, 30, 30, 0.7);
            border-radius: 15px;
            padding: 2rem;
            border: 1px solid rgba(255,255,255,0.1);
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            position: relative;
            overflow: hidden;
        }
        
        .chart-wrapper::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(to right, var(--neon-pink), var(--cyber-purple));
        }
        
        /* Winning Programs Section */
        .winning-programs {
            padding: 6rem 0;
            position: relative;
        }
        
        .programs-tabs {
            display: flex;
            justify-content: center;
            margin-bottom: 2rem;
            flex-wrap: wrap;
            gap: 1rem;
        }
        
        .tab-button {
            background: rgba(255,255,255,0.05);
            border: none;
            border-radius: 50px;
            padding: 0.8rem 1.8rem;
            font-family: 'Poppins', sans-serif;
            font-weight: 600;
            color: rgba(255,255,255,0.8);
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .tab-button::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(0, 97, 255, 0.2), rgba(138, 43, 226, 0.2));
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .tab-button:hover {
            color: white;
            background: rgba(255,255,255,0.1);
        }
        
        .tab-button.active {
            background: linear-gradient(135deg, var(--electric-blue), var(--cyber-purple));
            color: white;
            box-shadow: 0 5px 15px rgba(138, 43, 226, 0.3);
        }
        
        .tab-button.active::before {
            opacity: 1;
        }
        
        .programs-content {
            display: none;
        }
        
        .programs-content.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .programs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2rem;
        }
        
        .program-card {
            background: rgba(30, 30, 30, 0.7);
            border-radius: 15px;
            overflow: hidden;
            border: 1px solid rgba(255,255,255,0.1);
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }
        
        .program-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(255, 0, 170, 0.2);
            border-color: rgba(255, 0, 170, 0.3);
        }
        
        .program-header {
            padding: 1.5rem;
            background: linear-gradient(135deg, rgba(0, 97, 255, 0.2), rgba(138, 43, 226, 0.2));
            position: relative;
        }
        
        .program-header h3 {
            font-size: 1.5rem;
            margin: 0;
            color: white;
        }
        
        .program-header p {
            margin: 0.5rem 0 0;
            color: rgba(255,255,255,0.7);
        }
        
        .program-body {
            padding: 1.5rem;
        }
        
        .program-features {
            list-style: none;
            padding: 0;
            margin: 0 0 1.5rem;
        }
        
        .program-features li {
            padding: 0.5rem 0;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .program-features i {
            color: var(--holographic-teal);
        }
        
        .program-stats {
            display: flex;
            justify-content: space-between;
            margin-top: 1.5rem;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255,255,255,0.1);
        }
        
        .program-stat {
            text-align: center;
        }
        
        .program-stat-value {
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--neon-pink);
        }
        
        .program-stat-label {
            font-size: 0.8rem;
            color: rgba(255,255,255,0.6);
            text-transform: uppercase;
        }
        
        .enrollment-form {
            background: rgba(30, 30, 30, 0.7);
            border-radius: 15px;
            padding: 2rem;
            border: 1px solid rgba(255,255,255,0.1);
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            width:100%
            margin: 0 auto;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--holographic-teal);
            font-weight: 500;
        }
        
        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem 1rem;
            background: rgba(255,255,255,0.05);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 8px;
            color: white;
            font-family: 'Poppins', sans-serif;
            transition: all 0.3s ease;
        }
        
        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--holographic-teal);
            box-shadow: 0 0 0 2px rgba(0, 245, 212, 0.2);
        }
        
        .form-row {
            display: flex;
            gap: 1.5rem;
        }
        
        .form-row .form-group {
            flex: 1;
        }
        
        .submit-btn {
            background: linear-gradient(135deg, var(--electric-blue), var(--cyber-purple));
            color: white;
            border: none;
            border-radius: 50px;
            padding: 1rem 2rem;
            font-family: 'Poppins', sans-serif;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: inline-block;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .submit-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(138, 43, 226, 0.3);
        }
        
        /* Floating Celebration Elements */
        .celebration-item {
            position: absolute;
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            color: var(--holographic-teal);
            z-index: -1;
            animation: floatCelebration 15s infinite ease-in-out;
            opacity: 0.7;
        }
        
        @keyframes floatCelebration {
            0%, 100% { transform: translate(0, 0) rotate(0deg); }
            25% { transform: translate(20px, -30px) rotate(10deg); }
            50% { transform: translate(-15px, -20px) rotate(-5deg); }
            75% { transform: translate(10px, 15px) rotate(5deg); }
        }
        
        /* Footer */
        .footer {
            background: rgba(0,0,0,0.7);
            padding: 4rem 0 2rem;
            position: relative;
            overflow: hidden;
        }
        
        .footer::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(to right, var(--electric-blue), var(--neon-pink), var(--cyber-purple));
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            margin-bottom: 3rem;
        }
        
        .footer-logo {
            font-size: 1.8rem;
            font-weight: 800;
            margin-bottom: 1rem;
            background: linear-gradient(to right, var(--holographic-teal), var(--neon-pink));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            display: inline-block;
        }
        
        .footer-about p {
            color: rgba(255,255,255,0.7);
            line-height: 1.6;
        }
        
        .footer-social {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .footer-social a {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255,255,255,0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            transition: all 0.3s ease;
        }
        
        .footer-social a:hover {
            background: var(--holographic-teal);
            transform: translateY(-3px);
        }
        
        .footer-links h3 {
            color: white;
            font-size: 1.2rem;
            margin-bottom: 1.5rem;
            position: relative;
        }
        
        .footer-links h3::after {
            content: "";
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--holographic-teal);
        }
        
        .footer-links ul {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        
        .footer-links li {
            margin-bottom: 0.8rem;
        }
        
        .footer-links a {
            color: rgba(255,255,255,0.7);
            text-decoration: none;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .footer-links a:hover {
            color: var(--holographic-teal);
            transform: translateX(5px);
        }
        
        .footer-links a i {
            font-size: 0.8rem;
        }
        
        .footer-contact p {
            display: flex;
            align-items: center;
            gap: 0.8rem;
            color: rgba(255,255,255,0.7);
            margin-bottom: 1rem;
        }
        
        .footer-contact i {
            color: var(--holographic-teal);
            width: 20px;
            text-align: center;
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: rgba(255,255,255,0.5);
            font-size: 0.9rem;
        }
        
        /* Responsive Adjustments */
        @media (max-width: 1024px) {
            .hero h1 {
                font-size: 3.5rem;
            }
            
            .section-header h2 {
                font-size: 2.5rem;
            }
            
            .performance-container {
                flex-direction: column;
            }
        }
        
        @media (max-width: 768px) {
            .hero {
                padding: 4rem 1rem;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            .champions-grid {
                grid-template-columns: 1fr 1fr;
            }
            
            .performance-stats {
                grid-template-columns: 1fr;
            }
            
            .form-row {
                flex-direction: column;
                gap: 0;
            }
        }
        
        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .champions-grid {
                grid-template-columns: 1fr;
            }
            
            .hero-stats {
                flex-direction: column;
                align-items: center;
            }
            
            .programs-grid {
                grid-template-columns: 1fr;
            }
            
            .footer-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body style="width:100%">
    <div class="scanlines"></div>
    <div class="floating-orb orb-1"></div>
    <div class="floating-orb orb-2"></div>
    <div class="floating-orb orb-3"></div>
    
    <!-- Celebration Elements -->
    <div class="celebration-item" style="top: 15%; left: 5%; animation-delay: 0s;"><i class="fas fa-trophy"></i></div>
    <div class="celebration-item" style="top: 25%; right: 8%; animation-delay: 2s;"><i class="fas fa-medal"></i></div>
    <div class="celebration-item" style="top: 60%; left: 10%; animation-delay: 4s;"><i class="fas fa-star"></i></div>
    <div class="celebration-item" style="top: 70%; right: 5%; animation-delay: 6s;"><i class="fas fa-award"></i></div>
    <div class="celebration-item" style="top: 40%; left: 15%; animation-delay: 1s;"><i class="fas fa-crown"></i></div>
    <div class="celebration-item" style="top: 50%; right: 15%; animation-delay: 3s;"><i class="fas fa-bolt"></i></div>
    
    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>HALL OF GATE CHAMPIONS</h1>
            <p>Celebrating our legacy of producing top rankers in GATE Metallurgical Engineering from 2018 to 2025</p>
            
            <div class="hero-stats">
                <div class="stat-bubble">
                    <i class="fas fa-trophy"></i>
                    <span>8 AIR-1 Rankers</span>
                </div>
                <div class="stat-bubble">
                    <i class="fas fa-medal"></i>
                    <span>460+ Top 100 Rankers</span>
                </div>
                <div class="stat-bubble">
                    <i class="fas fa-calendar-alt"></i>
                    <span>7 Years of Excellence</span>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Performance Milestones Section -->
    <section class="performance-milestones">
        <div class="container">
            <div class="section-header">
                <h2>PERFORMANCE MILESTONES</h2>
                <p>Our track record of excellence in GATE Metallurgical Engineering</p>
            </div>
            
            <div class="performance-container">
                <div class="performance-content">
                    <h3>Dominating GATE Metallurgy Since 2018</h3>
                    <p>We've consistently produced top rankers year after year, with our students achieving remarkable results across all categories. Our comprehensive approach ensures success for students from all backgrounds.</p>
                    
                    <div class="performance-stats">
                        <div class="performance-stat">
                            <h3>100%</h3>
                            <p>Success Rate in Last 5 Years</p>
                        </div>
                        <div class="performance-stat">
                            <h3>460+</h3>
                            <p>Top 100 Rankers</p>
                        </div>
                        <div class="performance-stat">
                            <h3>8</h3>
                            <p>Consecutive AIR-1 Rankers</p>
                        </div>
                        <div class="performance-stat">
                            <h3>95%</h3>
                            <p>Selection Rate in PSUs</p>
                        </div>
                    </div>
                </div>
                
                <div class="chart-container">
                    <div class="chart-wrapper">
                        <canvas id="performanceChart"></canvas>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Champions Wall -->
    <section class="champions-wall">
        <div class="container">
            <div class="section-header">
                <h2>OUR GATE CHAMPIONS</h2>
                <p>Meet the extraordinary students who achieved top ranks in GATE Metallurgy through our program</p>
            </div>
            
            <div class="champions-grid">
                <!-- Champion 2025 -->
                <div class="champion-card">
                    <div class="champion-header">
                        <div class="champion-year"> GATE 2025</div>
                        <div class="champion-rank">AIR-1</div>
                        <div class="champion-photo">
                            <img src="https://images-website-testurself.s3.us-east-1.amazonaws.com/AIR-1-2025.png" alt="Yogesh Sarma Sedai">
                        </div>
                    </div>
                    <div class="champion-body">
                        <h3 class="champion-name">Yogesh Sarma Sedai</h3>
                        <div class="champion-branch">Metallurgical Engineering</div>
                        
                        <div class="champion-stats">
                            <div class="stat-item">
                                <div class="stat-value">941</div>
                                <div class="stat-label">GATE Score</div>
                            </div>
                            <div class="stat-item">
                                <div class="stat-value">60+</div>
                                <div class="stat-label">Top 100</div>
                            </div>
                        </div>
                        
                        <div class="champion-score">New Ranker</div>
                    </div>
                </div>
                
                <!-- Champion 2024 -->
                <div class="champion-card">
                    <div class="champion-header">
                        <div class="champion-year">GATE 2024</div>
                        <div class="champion-rank">AIR-1</div>
                        <div class="champion-photo">
                            <img src="https://images-website-testurself.s3.us-east-1.amazonaws.com/AIR-1-2024.png" alt="Hrutidipan Pradhan">
                        </div>
                    </div>
                    <div class="champion-body">
                        <h3 class="champion-name">Hrutidipan Pradhan</h3>
                        <div class="champion-branch">Metallurgical Engineering</div>
                        
                        <div class="champion-stats">
                            <div class="stat-item">
                                <div class="stat-value">977</div>
                                <div class="stat-label">GATE Score</div>
                            </div>
                            <div class="stat-item">
                                <div class="stat-value">60+</div>
                                <div class="stat-label">Top 100</div>
                            </div>
                        </div>
                        
                        <div class="champion-score">Highest Score</div>
                    </div>
                </div>
                
                <!-- Champion 2023 -->
                <div class="champion-card">
                    <div class="champion-header">
                        <div class="champion-year">GATE 2023</div>
                        <div class="champion-rank">AIR-1</div>
                        <div class="champion-photo">
                            <img src="https://images-website-testurself.s3.us-east-1.amazonaws.com/AIR-1-2023.png" alt="Ashutosh Kumar">
                        </div>
                    </div>
                    <div class="champion-body">
                        <h3 class="champion-name">Ashutosh Kumar</h3>
                        <div class="champion-branch">Metallurgical Engineering</div>
                        
                        <div class="champion-stats">
                            <div class="stat-item">
                                <div class="stat-value">973</div>
                                <div class="stat-label">GATE Score</div>
                            </div>
                            <div class="stat-item">
                                <div class="stat-value">60+</div>
                                <div class="stat-label">Top 100</div>
                            </div>
                        </div>
                        
                        <div class="champion-score">Perfect Accuracy</div>
                    </div>
                </div>
                
                <!-- Champion 2022 -->
                <div class="champion-card">
                    <div class="champion-header">
                        <div class="champion-year">GATE 2022</div>
                        <div class="champion-rank">AIR-1</div>
                        <div class="champion-photo">
                            <img src="https://images-website-testurself.s3.us-east-1.amazonaws.com/AIR-1-2022.png" alt="Mohit Patidar">
                        </div>
                    </div>
                    <div class="champion-body">
                        <h3 class="champion-name">Mohit Patidar</h3>
                        <div class="champion-branch">Metallurgical Engineering</div>
                        
                        <div class="champion-stats">
                            <div class="stat-item">
                                <div class="stat-value">952</div>
                                <div class="stat-label">GATE Score</div>
                            </div>
                            <div class="stat-item">
                                <div class="stat-value">65+</div>
                                <div class="stat-label">Top 100</div>
                            </div>
                        </div>
                        
                        <div class="champion-score">Record Batch</div>
                    </div>
                </div>
                
                <!-- Champion 2021 -->
                <div class="champion-card">
                    <div class="champion-header">
                        <div class="champion-year">2021</div>
                        <div class="champion-rank">AIR-1</div>
                        <div class="champion-photo">
                            <img src="https://www.testurself.in/wp-content/uploads/2021/03/12.png" alt="D Laxman Rao">
                        </div>
                    </div>
                    <div class="champion-body">
                        <h3 class="champion-name">D Laxman Rao</h3>
                        <div class="champion-branch">Metallurgical Engineering</div>
                        
                        <div class="champion-stats">
                            <div class="stat-item">
                                <div class="stat-value">923</div>
                                <div class="stat-label">GATE Score</div>
                            </div>
                            <div class="stat-item">
                                <div class="stat-value">60+</div>
                                <div class="stat-label">Top 100</div>
                            </div>
                        </div>
                        
                        <div class="champion-score">Concept Master</div>
                    </div>
                </div>
                
                <!-- Champion 2020 -->
                <div class="champion-card">
                    <div class="champion-header">
                        <div class="champion-year">2020</div>
                        <div class="champion-rank">AIR-1</div>
                        <div class="champion-photo">
                            <img src="https://www.testurself.in/wp-content/uploads/2020/04/0752FA29-EA5B-4524-866B-4A8AB4398CFF.jpeg" alt="Jaya Gupta">
                        </div>
                    </div>
                    <div class="champion-body">
                        <h3 class="champion-name">Jaya Gupta</h3>
                        <div class="champion-branch">Metallurgical Engineering</div>
                        
                        <div class="champion-stats">
                            <div class="stat-item">
                                <div class="stat-value">-</div>
                                <div class="stat-label">GATE Score</div>
                            </div>
                            <div class="stat-item">
                                <div class="stat-value">60+</div>
                                <div class="stat-label">Top 100</div>
                            </div>
                        </div>
                        
                        <div class="champion-score">First Female Topper</div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Winning Programs Section -->
    <section class="winning-programs">
        <div class="container">
            <div class="section-header">
                <h2>OUR WINNING PROGRAMS</h2>
                <p>Specialized courses designed to produce GATE champions year after year</p>
            </div>
            
            <div class="programs-tabs">
                <button class="tab-button active" data-tab="programs">Programs</button>
                <button class="tab-button" data-tab="enrollment">Enrollment</button>
            </div>
            
            <div class="programs-content active" id="programs-tab">
                <div class="programs-grid">
                    <div class="program-card">
                        <div class="program-header">
                            <h3>GATE Topper's Batch</h3>
                            <p>For serious aspirants targeting AIR-1</p>
                        </div>
                        <div class="program-body">
                            <ul class="program-features">
                                <li><i class="fas fa-check-circle"></i> Comprehensive coverage of syllabus</li>
                                <li><i class="fas fa-check-circle"></i> Advanced problem solving sessions</li>
                                <li><i class="fas fa-check-circle"></i> Personalized mentoring</li>
                                <li><i class="fas fa-check-circle"></i> 50+ full-length mock tests</li>
                            </ul>
                            <div class="program-stats">
                                <div class="program-stat">
                                    <div class="program-stat-value">8</div>
                                    <div class="program-stat-label">AIR-1 Rankers</div>
                                </div>
                                <div class="program-stat">
                                    <div class="program-stat-value">100%</div>
                                    <div class="program-stat-label">Success Rate</div>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="program-card">
                        <div class="program-header">
                            <h3>PSU Aspirants Program</h3>
                            <p>Specialized training for PSU recruitment</p>
                        </div>
                        <div class="program-body">
                            <ul class="program-features">
                                <li><i class="fas fa-check-circle"></i> PSU-specific preparation</li>
                                <li><i class="fas fa-check-circle"></i> Interview preparation</li>
                                <li><i class="fas fa-check-circle"></i> Technical knowledge enhancement</li>
                                <li><i class="fas fa-check-circle"></i> Previous year question analysis</li>
                            </ul>
                            <div class="program-stats">
                                <div class="program-stat">
                                    <div class="program-stat-value">95%</div>
                                    <div class="program-stat-label">Selection Rate</div>
                                </div>
                                <div class="program-stat">
                                    <div class="program-stat-value">200+</div>
                                    <div class="program-stat-label">PSU Selections</div>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="program-card">
                        <div class="program-header">
                            <h3>Foundation Program</h3>
                            <p>For beginners starting their GATE journey</p>
                        </div>
                        <div class="program-body">
                            <ul class="program-features">
                                <li><i class="fas fa-check-circle"></i> Concept building modules</li>
                                <li><i class="fas fa-check-circle"></i> Basic to advanced progression</li>
                                <li><i class="fas fa-check-circle"></i> Regular doubt clearing</li>
                                <li><i class="fas fa-check-circle"></i> Weekly progress tests</li>
                            </ul>
                            <div class="program-stats">
                                <div class="program-stat">
                                    <div class="program-stat-value">80%</div>
                                    <div class="program-stat-label">Top 100 Rankers</div>
                                </div>
                                <div class="program-stat">
                                    <div class="program-stat-value">2x</div>
                                    <div class="program-stat-label">Performance Boost</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="programs-content" id="enrollment-tab">
                <div class="enrollment-form">
                    <h3 style="text-align: center; margin-bottom: 2rem; color: var(--holographic-teal);">Enroll in Our Winning Programs</h3>
                    <form id="enrollmentForm">
                        <div class="form-row">
                            <div class="form-group">
                                <label for="firstName">First Name</label>
                                <input type="text" id="firstName" name="firstName" required>
                            </div>
                            <div class="form-group">
                                <label for="lastName">Last Name</label>
                                <input type="text" id="lastName" name="lastName" required>
                            </div>
                        </div>
                        
                        <div class="form-row">
                            <div class="form-group">
                                <label for="email">Email Address</label>
                                <input type="email" id="email" name="email" required>
                            </div>
                            <div class="form-group">
                                <label for="phone">Phone Number</label>
                                <input type="tel" id="phone" name="phone" required>
                            </div>
                        </div>
                        
                        <div class="form-group">
                            <label for="program">Select Program</label>
                            <select id="program" name="program" required>
                                <option value="">Choose a program</option>
                                <option value="topper">GATE Topper's Batch</option>
                                <option value="psu">PSU Aspirants Program</option>
                                <option value="foundation">Foundation Program</option>
                                <option value="combo">Combo Program (All Access)</option>
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label for="message">Additional Information</label>
                            <textarea id="message" name="message" rows="4"></textarea>
                        </div>
                        
                        <div style="text-align: center; margin-top: 2rem;">
                            <button type="submit" class="submit-btn">Submit Enrollment</button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-container">
                <div class="footer-about">
                    <div class="footer-logo">TestUrSelf</div>
                    <p>Transforming GATE aspirants into top rankers since 2018. Our proven methodology and expert guidance have helped hundreds achieve their dreams in Metallurgical Engineering.</p>
                    <div class="footer-social">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                
                <div class="footer-links">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Home</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> About Us</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Programs</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Results</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Testimonials</a></li>
                    </ul>
                </div>
                
                <div class="footer-links">
                    <h3>Resources</h3>
                    <ul>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Study Materials</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Mock Tests</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Previous Papers</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Blog</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> FAQs</a></li>
                    </ul>
                </div>
                
                <div class="footer-contact">
                    <h3>Contact Us</h3>
                    <p><i class="fas fa-map-marker-alt"></i> 123 Education Street, Learning City, 560001</p>
                    <p><i class="fas fa-phone-alt"></i> +91 9876543210</p>
                    <p><i class="fas fa-envelope"></i> info@testurself.in</p>
                    <p><i class="fas fa-clock"></i> Mon-Sat: 9:00 AM - 6:00 PM</p>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2025 TestUrSelf. All Rights Reserved. | Designed with <i class="fas fa-heart" style="color: var(--neon-pink);"></i> for GATE Aspirants</p>
            </div>
        </div>
    </footer>
    
    <script>
        // Animation for champion cards
        const championCards = document.querySelectorAll('.champion-card');
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach((entry, index) => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = 1;
                    entry.target.style.transform = 'translateY(0)';
                    entry.target.style.transition = `all 0.5s ease ${index * 0.1}s`;
                }
            });
        }, { threshold: 0.1 });
        
        championCards.forEach(card => {
            card.style.opacity = 0;
            card.style.transform = 'translateY(30px)';
            observer.observe(card);
        });
        
        // Animation for program cards
        const programCards = document.querySelectorAll('.program-card');
        
        const programObserver = new IntersectionObserver((entries) => {
            entries.forEach((entry, index) => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = 1;
                    entry.target.style.transform = 'translateY(0)';
                    entry.target.style.transition = `all 0.5s ease ${index * 0.1}s`;
                }
            });
        }, { threshold: 0.1 });
        
        programCards.forEach(card => {
            card.style.opacity = 0;
            card.style.transform = 'translateY(30px)';
            programObserver.observe(card);
        });
        
        // Dynamic glow effect
        document.addEventListener('mousemove', (e) => {
            const orbs = document.querySelectorAll('.floating-orb');
            orbs.forEach(orb => {
                const x = e.clientX / window.innerWidth;
                const y = e.clientY / window.innerHeight;
                orb.style.transform = `translate(${x * 20}px, ${y * 20}px)`;
            });
        });
        
        // Performance Chart
        const ctx = document.getElementById('performanceChart').getContext('2d');
        const performanceChart = new Chart(ctx, {
            type: 'doughnut',
            data: {
                labels: ['AIR-1 Rankers', 'Top 10 Rankers', 'Top 100 Rankers', 'PSU Selections', 'IIT Admissions'],
                datasets: [{
                    data: [8, 42, 460, 200, 180],
                    backgroundColor: [
                        'rgba(0, 245, 212, 0.8)',
                        'rgba(0, 97, 255, 0.8)',
                        'rgba(138, 43, 226, 0.8)',
                        'rgba(255, 0, 170, 0.8)',
                        'rgba(0, 255, 65, 0.8)'
                    ],
                    borderColor: [
                        'rgba(0, 245, 212, 1)',
                        'rgba(0, 97, 255, 1)',
                        'rgba(138, 43, 226, 1)',
                        'rgba(255, 0, 170, 1)',
                        'rgba(0, 255, 65, 1)'
                    ],
                    borderWidth: 1,
                    hoverOffset: 20
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: true,
                plugins: {
                    legend: {
                        position: 'right',
                        labels: {
                            color: 'rgba(255, 255, 255, 0.8)',
                            font: {
                                family: 'Poppins',
                                size: 12
                            },
                            padding: 20
                        }
                    },
                    tooltip: {
                        backgroundColor: 'rgba(30, 30, 30, 0.9)',
                        titleColor: 'var(--holographic-teal)',
                        bodyColor: 'rgba(255, 255, 255, 0.8)',
                        borderColor: 'rgba(255, 255, 255, 0.1)',
                        borderWidth: 1,
                        padding: 15,
                        callbacks: {
                            label: function(context) {
                                let label = context.label || '';
                                if (label) {
                                    label += ': ';
                                }
                                label += context.raw;
                                return label;
                            }
                        }
                    }
                },
                cutout: '70%',
                animation: {
                    animateScale: true,
                    animateRotate: true
                }
            }
        });
        
        // Tab functionality
        const tabButtons = document.querySelectorAll('.tab-button');
        const tabContents = document.querySelectorAll('.programs-content');
        
        tabButtons.forEach(button => {
            button.addEventListener('click', () => {
                // Remove active class from all buttons and contents
                tabButtons.forEach(btn => btn.classList.remove('active'));
                tabContents.forEach(content => content.classList.remove('active'));
                
                // Add active class to clicked button
                button.classList.add('active');
                
                // Show corresponding content
                const tabId = button.getAttribute('data-tab');
                document.getElementById(`${tabId}-tab`).classList.add('active');
            });
        });
        
        // Form submission
        const enrollmentForm = document.getElementById('enrollmentForm');
        enrollmentForm.addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Thank you for your enrollment! We will contact you shortly.');
            enrollmentForm.reset();
        });
        
        // Animate celebration items
        const celebrationItems = document.querySelectorAll('.celebration-item');
        celebrationItems.forEach((item, index) => {
            item.style.animationDelay = `${index * 2}s`;
        });
    </script>
</body>
</html>
