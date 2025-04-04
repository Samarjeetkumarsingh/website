<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GATE Metallurgical Engineering Exam Preparation Guide | TestUrSelf</title>
    <style>
        :root {
            --primary-color: #6a1b9a;
            --secondary-color: #ff9800;
            --accent-color: #4a148c;
            --light-color: #f3e5f5;
            --dark-color: #4a148c;
            --text-color: #212121;
            --highlight-color: #ffeb3b;
            --success-color: #388e3c;
            --thermal-color: #e53935;
            --fluid-color: #1e88e5;
            --mass-color: #43a047;
            --kinetics-color: #8e24aa;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
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
            background: linear-gradient(135deg, #f5f5f5 0%, #e0e0e0 50%, #f5f5f5 100%);
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
            color: rgba(106, 27, 154, 0.05);
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
        }
        
        .nav-links a:hover {
            color: var(--secondary-color);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            color: white;
            padding: 5rem 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero::after {
            content: "";
            position: absolute;
            top: -50%;
            left: -50%;
            right: -50%;
            bottom: -50%;
            background: linear-gradient(
                to bottom right,
                rgba(255,255,255,0) 0%,
                rgba(255,255,255,0.1) 50%,
                rgba(255,255,255,0) 100%
            );
            transform: rotate(30deg);
            animation: shine 6s infinite;
        }
        
        @keyframes shine {
            0% {transform: rotate(30deg) translate(-30%, -30%);}
            100% {transform: rotate(30deg) translate(30%, 30%);}
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
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
            border-radius: 4px;
            font-weight: bold;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .btn-primary {
            background-color: var(--secondary-color);
            color: white;
        }
        
        .btn-primary:hover {
            background-color: #e68a00;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .btn-secondary {
            background-color: transparent;
            border: 2px solid white;
            color: white;
        }
        
        .btn-secondary:hover {
            background-color: rgba(255,255,255,0.1);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        /* Section Styling */
        .section {
            background-color: white;
            border-radius: 12px;
            padding: 3rem;
            margin: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
            z-index: 1;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(0,0,0,0.05);
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }
        
        h2 {
            color: var(--primary-color);
            border-bottom: 3px solid var(--accent-color);
            padding-bottom: 0.8rem;
            margin-top: 0;
            font-size: 2.2rem;
            background: linear-gradient(to right, transparent, #f3e5f5, transparent);
            padding: 1rem 0;
            text-align: center;
            border-radius: 8px;
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
        
        /* GATE Intro Section */
        .gate-intro {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }
        
        .intro-card {
            background: white;
            border-radius: 8px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            border-top: 4px solid var(--primary-color);
        }
        
        .intro-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }
        
        .intro-card h3 {
            color: var(--primary-color);
            margin-top: 0;
            border-left: none;
            padding-left: 0;
            font-size: 1.5rem;
        }
        
        .intro-card h3 i {
            margin-right: 10px;
            color: var(--secondary-color);
        }
        
        /* Key Topics Section */
        .topics-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .topic-card {
            background: linear-gradient(135deg, #f9f9f9, #f0f0f0);
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            border-left: 4px solid var(--primary-color);
        }
        
        .topic-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
        }
        
        .topic-card h4 {
            color: var(--primary-color);
            margin-top: 0;
            margin-bottom: 1rem;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
        }
        
        .topic-card h4 i {
            margin-right: 10px;
            font-size: 1.2rem;
        }
        
        .topic-card ul {
            margin: 0;
            padding-left: 1.5rem;
        }
        
        .topic-card li {
            margin-bottom: 0.5rem;
            position: relative;
        }
        
        .topic-card li::before {
            content: "•";
            color: var(--secondary-color);
            font-weight: bold;
            display: inline-block;
            width: 1em;
            margin-left: -1em;
        }
        
        /* Why Choose Us Section */
        .why-us-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .feature-card {
            background: white;
            border-radius: 8px;
            padding: 2rem;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            border: 1px solid rgba(0,0,0,0.05);
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }
        
        .feature-icon {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 1.5rem;
            transition: all 0.3s ease;
        }
        
        .feature-card:hover .feature-icon {
            transform: scale(1.1);
            color: var(--secondary-color);
        }
        
        .feature-card h4 {
            font-size: 1.4rem;
            margin-top: 0;
            margin-bottom: 1rem;
            color: var(--dark-color);
        }
        
        /* Preparation Guide */
        .preparation-steps {
            display: grid;
            gap: 2rem;
        }
        
        .step {
            display: flex;
            gap: 1.5rem;
            align-items: flex-start;
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.5s ease;
        }
        
        .step.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        .step-number {
            background-color: var(--primary-color);
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            flex-shrink: 0;
            transition: all 0.3s ease;
        }
        
        .step:hover .step-number {
            background-color: var(--secondary-color);
            transform: scale(1.1);
        }
        
        .step-content {
            background-color: var(--light-color);
            padding: 1.5rem;
            border-radius: 8px;
            flex-grow: 1;
            position: relative;
            transition: all 0.3s ease;
        }
        
        .step:hover .step-content {
            background-color: #e8d5f1;
        }
        
        .step-content::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--primary-color), var(--secondary-color));
        }
        
        /* Testimonials */
        .testimonials-container {
            position: relative;
            overflow: hidden;
        }
        
        .testimonials-slider {
            display: flex;
            transition: transform 0.5s ease;
        }
        
        .testimonial {
            min-width: 100%;
            padding: 0 1rem;
        }
        
        .testimonial-card {
            background-color: white;
            border-radius: 8px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
            border: 1px solid rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        
        .testimonial-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }
        
        .testimonial-header {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
        }
        
        .testimonial-img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: 1rem;
            border: 3px solid var(--light-color);
            transition: all 0.3s ease;
        }
        
        .testimonial-card:hover .testimonial-img {
            border-color: var(--secondary-color);
            transform: scale(1.05);
        }
        
        .testimonial-info h4 {
            margin: 0;
            font-size: 1.2rem;
        }
        
        .testimonial-info p {
            margin: 0;
            color: var(--secondary-color);
            font-weight: 500;
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 1.5rem;
        }
        
        .testimonial-rating {
            color: var(--highlight-color);
        }
        
        .slider-controls {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 2rem;
        }
        
        .slider-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background-color: #ccc;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .slider-dot.active {
            background-color: var(--primary-color);
            transform: scale(1.2);
        }
        
        /* Stats Section */
        .stats-section {
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            color: white;
            padding: 4rem 2rem;
            text-align: center;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 2rem;
            max-width: 1000px;
            margin: 0 auto;
        }
        
        .stat-item {
            padding: 1.5rem;
            transition: all 0.3s ease;
        }
        
        .stat-item:hover {
            transform: translateY(-5px);
        }
        
        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
            color: var(--secondary-color);
        }
        
        .stat-label {
            font-size: 1.1rem;
        }
        
        /* CTA Sections */
        .cta-section {
            text-align: center;
            padding: 4rem 2rem;
        }
        
        .cta-section.dark {
            background-color: var(--dark-color);
            color: white;
        }
        
        .cta-section.gradient {
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            color: white;
        }
        
        /* FAQ Section */
        .faq-item {
            margin-bottom: 1rem;
            border: 1px solid #e0e0e0;
            border-radius: 8px;
            overflow: hidden;
            transition: all 0.3s ease;
        }
        
        .faq-item:hover {
            border-color: var(--primary-color);
        }
        
        .faq-question {
            width: 100%;
            padding: 1.5rem;
            text-align: left;
            background-color: #f9f9f9;
            border: none;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-weight: 500;
            font-size: 1.1rem;
            transition: all 0.3s ease;
        }
        
        .faq-question:hover {
            background-color: #f0f0f0;
        }
        
        .faq-answer {
            padding: 0 1.5rem;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease, padding 0.3s ease;
        }
        
        .faq-answer.open {
            padding: 1.5rem;
            max-height: 500px;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 4rem 2rem;
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
        }
        
        .footer-column li:hover {
            transform: translateX(5px);
        }
        
        .footer-column a {
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-column a:hover {
            color: white;
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
        }
        
        .social-links a:hover {
            color: var(--secondary-color);
            transform: translateY(-3px);
        }
        
        .footer-bottom {
            text-align: center;
            margin-top: 3rem;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
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
            
            .stats-container {
                grid-template-columns: 1fr 1fr;
            }
            
            .footer-container {
                grid-template-columns: 1fr 1fr;
            }
            
            .cta-buttons {
                flex-direction: column;
            }
        }
        
        @media (max-width: 480px) {
            .stats-container {
                grid-template-columns: 1fr;
            }
            
            .footer-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <a href="#" class="logo">
                <i class="fas fa-graduation-cap"></i> TestUrSelf
            </a>
            <div class="nav-links">
                <a href="#preparation">Preparation</a>
                <a href="#testimonials">Success Stories</a>
                <a href="#stats">Our Results</a>
                <a href="#faq">FAQ</a>
                <a href="#cta">Join Now</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <h1>Master GATE Metallurgical Engineering</h1>
        <p>The Complete Guide to Crack GATE MT with Top Ranks</p>
        <div class="cta-buttons">
            <a href="#cta" class="btn btn-primary">Join TestUrSelf Now</a>
            <a href="#download" class="btn btn-secondary">Download Free Material</a>
        </div>
    </section>

    <!-- GATE Introduction Section -->
    <section class="section">
        <h2>What is GATE Metallurgical Engineering?</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">GATE (Graduate Aptitude Test in Engineering) for Metallurgical Engineering (MT) is the gateway to prestigious PSU jobs, M.Tech admissions in IITs/NITs, and research opportunities.</p>
        
        <div class="gate-intro">
            <div class="intro-card">
                <h3><i class="fas fa-clipboard-list"></i> Exam Structure</h3>
                <p>65 questions worth 100 marks covering General Aptitude, Engineering Mathematics, and Metallurgy subjects.</p>
            </div>
            
            <div class="intro-card">
                <h3><i class="fas fa-star"></i> Importance</h3>
                <p>Qualifying GATE MT opens doors to PSUs like SAIL, NALCO, IOCL, DRDO, BARC, and top institutes like IITs, IISc, NITs.</p>
            </div>
            
            <div class="intro-card">
                <h3><i class="fas fa-trophy"></i> Competition</h3>
                <p>With 3,500+ aspirants each year, strategic preparation is key to securing top ranks.</p>
            </div>
        </div>
    </section>

    <!-- Key Topics Section -->
    <section class="section">
        <h2>Key Topics in GATE Metallurgy</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">Focus on these high-weightage topics to maximize your score</p>
        
        <div class="topics-container">
            <div class="topic-card">
                <h4><i class="fas fa-atom" style="color: var(--thermal-color);"></i> Physical Metallurgy</h4>
                <ul>
                    <li>Crystal structures & defects</li>
                    <li>Phase diagrams & transformations</li>
                    <li>Heat treatment processes</li>
                </ul>
            </div>
            
            <div class="topic-card">
                <h4><i class="fas fa-hard-hat" style="color: var(--fluid-color);"></i> Mechanical Metallurgy</h4>
                <ul>
                    <li>Dislocations & strengthening</li>
                    <li>Fracture & fatigue</li>
                    <li>Mechanical testing</li>
                </ul>
            </div>
            
            <div class="topic-card">
                <h4><i class="fas fa-industry" style="color: var(--mass-color);"></i> Manufacturing Processes</h4>
                <ul>
                    <li>Casting & welding</li>
                    <li>Metal forming</li>
                    <li>Powder metallurgy</li>
                </ul>
            </div>
            
            <div class="topic-card">
                <h4><i class="fas fa-fire" style="color: var(--kinetics-color);"></i> Thermodynamics & Kinetics</h4>
                <ul>
                    <li>Laws of thermodynamics</li>
                    <li>Phase equilibria</li>
                    <li>Diffusion & reactions</li>
                </ul>
            </div>
            
            <div class="topic-card">
                <h4><i class="fas fa-flask" style="color: var(--thermal-color);"></i> Extractive Metallurgy</h4>
                <ul>
                    <li>Ore processing</li>
                    <li>Pyrometallurgy</li>
                    <li>Hydrometallurgy</li>
                </ul>
            </div>
            
            <div class="topic-card">
                <h4><i class="fas fa-square-root-alt" style="color: var(--fluid-color);"></i> Engineering Mathematics</h4>
                <ul>
                    <li>Linear algebra</li>
                    <li>Calculus & differential equations</li>
                    <li>Probability & statistics</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Preparation Guide Section -->
    <section id="preparation" class="section">
        <h2>Step-by-Step Preparation Guide</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">Follow this comprehensive 6-month plan to systematically prepare for GATE Metallurgy</p>
        
        <div class="preparation-steps">
            <!-- Step 1 -->
            <div class="step">
                <div class="step-number">1</div>
                <div class="step-content">
                    <h3>Understand Syllabus & Exam Pattern</h3>
                    <p>Thoroughly analyze the GATE MT syllabus (Physical Metallurgy, Mechanical Metallurgy, Manufacturing Processes, etc.) and exam pattern (marks distribution, negative marking).</p>
                </div>
            </div>
            
            <!-- Step 2 -->
            <div class="step">
                <div class="step-number">2</div>
                <div class="step-content">
                    <h3>Collect Study Materials</h3>
                    <p>Gather standard textbooks, TestUrSelf study materials, previous year papers, and Video courses. Focus on quality over quantity.</p>
                </div>
            </div>
            
            <!-- Step 3 -->
            <div class="step">
                <div class="step-number">3</div>
                <div class="step-content">
                    <h3>Create Study Schedule</h3>
                    <p>Divide syllabus into weekly targets. Allocate time for concepts, problem-solving, revision, and mock tests. Include buffer time.</p>
                </div>
            </div>
            
            <!-- Step 4 -->
            <div class="step">
                <div class="step-number">4</div>
                <div class="step-content">
                    <h3>Concept Building & Notes</h3>
                    <p>Study topics thoroughly, make concise notes, create formula sheets, and understand fundamental concepts rather than rote learning.</p>
                </div>
            </div>
            
            <!-- Step 5 -->
            <div class="step">
                <div class="step-number">5</div>
                <div class="step-content">
                    <h3>Practice & Mock Tests</h3>
                    <p>Solve previous year papers (at least 10 years) and take regular mock tests from TestUrSelf under timed conditions. Analyze performance to identify weak areas.</p>
                </div>
            </div>
            
            <!-- Step 6 -->
            <div class="step">
                <div class="step-number">6</div>
                <div class="step-content">
                    <h3>Revision & Final Preparation</h3>
                    <p>Last 1-2 months should focus on revision, formula sheets, important topics, and full-length mock tests to build stamina.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section id="testimonials" class="section">
        <h2>Success Stories</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">Hear from our GATE Metallurgy toppers who achieved their dreams with TestUrSelf</p>
        
        <div class="testimonials-container">
            <div class="testimonials-slider" id="testimonialSlider">
                <!-- Testimonial 1 -->
                <div class="testimonial">
                    <div class="testimonial-card">
                        <div class="testimonial-header">
                            <img src="https://drive.google.com/file/d/1grpAixEKbHslcsrrJ2NIWw2snHbN_ira/view?usp=sharing" alt="Rahul Sharma" class="testimonial-img">
                            <div class="testimonial-info">
                                <h4>Hrutidipan Pradhan</h4>
                                <p>GATE MT AIR 1 (2024)</p>
                            </div>
                        </div>
                        <div class="testimonial-text">
                            "TestUrSelf's test series was instrumental in my GATE preparation. The questions were so similar to actual GATE that I felt completely prepared. The mentorship from IIT professors helped me clear my concepts thoroughly."
                        </div>
                        <div class="testimonial-rating">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                        </div>
                    </div>
                </div>
                
                <!-- Testimonial 2 -->
                <div class="testimonial">
                    <div class="testimonial-card">
                        <div class="testimonial-header">
                            <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Priya Patel" class="testimonial-img">
                            <div class="testimonial-info">
                                <h4>Priya Patel</h4>
                                <p>GATE MT AIR 3 (2021)</p>
                            </div>
                        </div>
                        <div class="testimonial-text">
                            "The study material from TestUrSelf covered everything in the syllabus with perfect depth. The regular doubt-solving sessions ensured I never got stuck on any topic. I recommend TestUrSelf to every GATE Metallurgy aspirant."
                        </div>
                        <div class="testimonial-rating">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                        </div>
                    </div>
                </div>
                
                <!-- Testimonial 3 -->
                <div class="testimonial">
                    <div class="testimonial-card">
                        <div class="testimonial-header">
                            <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="Amit Kumar" class="testimonial-img">
                            <div class="testimonial-info">
                                <h4>Amit Kumar</h4>
                                <p>GATE MT AIR 7 (2023)</p>
                            </div>
                        </div>
                        <div class="testimonial-text">
                            "What sets TestUrSelf apart is their focus on Metallurgy specifically. The faculty understands exactly what's important for GATE. Their test series had several questions that appeared verbatim in my GATE paper!"
                        </div>
                        <div class="testimonial-rating">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="slider-controls">
                <div class="slider-dot active" data-index="0"></div>
                <div class="slider-dot" data-index="1"></div>
                <div class="slider-dot" data-index="2"></div>
            </div>
        </div>
    </section>

    <!-- Why Choose Us Section -->
    <section class="section">
        <h2>Why TestUrSelf for GATE Metallurgy?</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">The proven platform that has consistently produced GATE MT toppers year after year</p>
        
        <div class="why-us-container">
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-book-open"></i>
                </div>
                <h4>Best Content for GATE Metallurgy</h4>
                <p>Comprehensive study material designed by IIT & IISc experts specifically for GATE MT syllabus.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-medal"></i>
                </div>
                <h4>Producing Top Rankers Since 2018</h4>
                <p>Consistent track record of producing AIR 1, AIR 2, and multiple top 100 ranks every year.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-trophy"></i>
                </div>
                <h4>AIR-1 Every Year Since 2019</h4>
                <p>Unmatched success with AIR 1 in GATE Metallurgy for 4 consecutive years.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-check-circle"></i>
                </div>
                <h4>Direct Questions in GATE Exam</h4>
                <p>Our test series questions match actual GATE questions - sometimes even verbatim!</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-chalkboard-teacher"></i>
                </div>
                <h4>Expert Mentorship</h4>
                <p>Live doubt-solving sessions with IIT/IISc mentors who know exactly what GATE demands.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-chart-line"></i>
                </div>
                <h4>Performance Analytics</h4>
                <p>Detailed test analytics to track your progress and identify improvement areas.</p>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section id="stats" class="stats-section">
        <h2 style="color: white; border-bottom-color: var(--secondary-color);">Our Track Record</h2>
        
        <div class="stats-container">
            <div class="stat-item">
                <div class="stat-number" id="studentsCount">1500</div>
                <div class="stat-label">Students Enrolled</div>
            </div>
            
            <div class="stat-item">
                <div class="stat-number" id="rankersCount">32</div>
                <div class="stat-label">Top 100 Rankers</div>
            </div>
            
            <div class="stat-item">
                <div class="stat-number" id="air1Count">4</div>
                <div class="stat-label">AIR 1 Produced</div>
            </div>
            
            <div class="stat-item">
                <div class="stat-number" id="satisfactionCount">98</div>
                <div class="stat-label">% Satisfaction Rate</div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section id="cta" class="cta-section dark">
        <h2 style="color: white; border-bottom-color: var(--secondary-color);">Ready to Start Your GATE Metallurgy Journey?</h2>
        <p style="max-width: 700px; margin: 0 auto 2rem;">Join India's most trusted GATE Metallurgy preparation platform and get closer to your dream rank</p>
        
        <div class="cta-buttons">
            <a href="#" class="btn btn-primary">
                <i class="fas fa-rocket mr-2"></i> Enroll Now
            </a>
            <a href="#" class="btn btn-secondary">
                <i class="fas fa-phone-alt mr-2"></i> Talk to an Expert
            </a>
        </div>
    </section>

    <!-- FAQ Section -->
    <section id="faq" class="section">
        <h2>Frequently Asked Questions</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">Get answers to common questions about GATE Metallurgy preparation</p>
        
        <div class="faq-container">
            <div class="faq-item">
                <button class="faq-question">
                    When should I start preparing for GATE Metallurgy?
                    <i class="fas fa-chevron-down"></i>
                </button>
                <div class="faq-answer">
                    <p>Ideally, you should start your preparation 6-8 months before the exam. However, if you're targeting top ranks (AIR < 100), we recommend a 10-12 month preparation period with at least 4-5 hours of daily study.</p>
                </div>
            </div>
            
            <div class="faq-item">
                <button class="faq-question">
                    What's more important - concepts or practice?
                    <i class="fas fa-chevron-down"></i>
                </button>
                <div class="faq-answer">
                    <p>Both are equally important. First build strong conceptual understanding (especially for Physical Metallurgy, Thermodynamics), then practice extensively (especially for Manufacturing, Mechanical Metallurgy). Our program balances both with concept lectures followed by practice sessions.</p>
                </div>
            </div>
            
            <div class="faq-item">
                <button class="faq-question">
                    How many mock tests should I take?
                    <i class="fas fa-chevron-down"></i>
                </button>
                <div class="faq-answer">
                    <p>Minimum 15-20 full-length mock tests in the last 3 months before GATE. Our test series includes 25+ mocks with progressive difficulty levels. Analyze each test thoroughly to identify weak areas.</p>
                </div>
            </div>
            
            <div class="faq-item">
                <button class="faq-question">
                    Is coaching necessary for GATE Metallurgy?
                    <i class="fas fa-chevron-down"></i>
                </button>
                <div class="faq-answer">
                    <p>While self-study is possible, structured guidance significantly improves your chances of top ranks. Our data shows 92% of top 100 rankers had some form of coaching. TestUrSelf's program provides the right direction, saves time, and ensures you cover all important topics.</p>
                </div>
            </div>
            
            <div class="faq-item">
                <button class="faq-question">
                    How does TestUrSelf compare to other platforms?
                    <i class="fas fa-chevron-down"></i>
                </button>
                <div class="faq-answer">
                    <p>TestUrSelf is the only platform exclusively focused on GATE Metallurgy with IIT/IISc faculty. Our content depth, test quality, and mentorship are unmatched. The results speak for themselves - we've produced AIR 1 every year since 2019 and have 3x more top 100 rankers than any other platform.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section class="cta-section gradient">
        <h2 style="color: white; border-bottom-color: var(--secondary-color);">Start Your GATE Metallurgy Preparation Today!</h2>
        <p style="max-width: 700px; margin: 0 auto 2rem;">Join thousands of successful Metallurgy aspirants who trusted TestUrSelf for their GATE journey</p>
        
        <div class="cta-buttons">
            <a href="#" class="btn btn-primary">
                <i class="fas fa-user-graduate mr-2"></i> Enroll Now
            </a>
            <a href="#" class="btn btn-secondary">
                <i class="fas fa-calendar-alt mr-2"></i> Free Demo Class
            </a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-container">
            <div class="footer-column">
                <h3>TestUrSelf</h3>
                <p>India's leading GATE Metallurgy preparation platform with proven results since 2018.</p>
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
                    <li><i class="fas fa-map-marker-alt mr-2"></i> 123 Education Street, Bangalore</li>
                    <li><i class="fas fa-phone-alt mr-2"></i> +91 9876543210</li>
                    <li><i class="fas fa-envelope mr-2"></i> info@testurself.com</li>
                </ul>
            </div>
        </div>
        
        <div class="footer-bottom">
            <p>&copy; 2023 TestUrSelf. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        // Testimonial Slider
        const slider = document.getElementById('testimonialSlider');
        const dots = document.querySelectorAll('.slider-dot');
        let currentSlide = 0;
        const totalSlides = document.querySelectorAll('.testimonial').length;
        let slideInterval;
        
        function goToSlide(index) {
            currentSlide = (index + totalSlides) % totalSlides;
            slider.style.transform = `translateX(-${currentSlide * 100}%)`;
            
            // Update dots
            dots.forEach((dot, i) => {
                dot.classList.toggle('active', i === currentSlide);
            });
        }
        
        function nextSlide() {
            goToSlide(currentSlide + 1);
        }
        
        function startSlider() {
            slideInterval = setInterval(nextSlide, 5000);
        }
        
        function resetSlider() {
            clearInterval(slideInterval);
            startSlider();
        }
        
        // Dot click handlers
        dots.forEach(dot => {
            dot.addEventListener('click', function() {
                const index = parseInt(this.getAttribute('data-index'));
                goToSlide(index);
                resetSlider();
            });
        });
        
        // Start the slider
        startSlider();
        
        // FAQ Accordion
        const faqQuestions = document.querySelectorAll('.faq-question');
        
        faqQuestions.forEach(question => {
            question.addEventListener('click', function() {
                const answer = this.nextElementSibling;
                const icon = this.querySelector('i');
                
                // Toggle current answer
                answer.classList.toggle('open');
                icon.classList.toggle('fa-chevron-down');
                icon.classList.toggle('fa-chevron-up');
                
                // Close other answers
                faqQuestions.forEach(q => {
                    if (q !== question) {
                        q.nextElementSibling.classList.remove('open');
                        q.querySelector('i').classList.add('fa-chevron-down');
                        q.querySelector('i').classList.remove('fa-chevron-up');
                    }
                });
            });
        });
        
        // Counter Animation
        function animateCounter(element, target, duration = 2000) {
            const start = 0;
            const increment = target / (duration / 16); // 60fps
            let current = start;
            
            const updateCounter = () => {
                current += increment;
                if (current < target) {
                    element.textContent = Math.floor(current);
                    requestAnimationFrame(updateCounter);
                } else {
                    element.textContent = target;
                }
            };
            
            // Start when element is in view
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        updateCounter();
                        observer.unobserve(element);
                    }
                });
            }, { threshold: 0.5 });
            
            observer.observe(element);
        }
        
        // Initialize counters
        animateCounter(document.getElementById('studentsCount'), 1500);
        animateCounter(document.getElementById('rankersCount'), 32);
        animateCounter(document.getElementById('air1Count'), 4);
        animateCounter(document.getElementById('satisfactionCount'), 98);
        
        // Step Animation
        const steps = document.querySelectorAll('.step');
        
        const stepObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, { threshold: 0.1 });
        
        steps.forEach((step, index) => {
            // Add delay based on index
            step.style.transitionDelay = `${index * 100}ms`;
            stepObserver.observe(step);
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
