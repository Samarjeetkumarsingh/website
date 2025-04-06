<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Why Test Series is Crucial for GATE Metallurgy | TestUrSelf</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.11.4/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.11.4/ScrollTrigger.min.js"></script>
    <style>
        :root {
            --primary-blue: #2962ff;
            --secondary-teal: #00bfa5;
            --accent-green: #00c853;
            --dark-blue: #01579b;
            --light-blue: #e3f2fd;
            --highlight-yellow: #ffd600;
            --danger-red: #ff1744;
            --purple: #7c4dff;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.8;
            color: #263238;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0;
            background-color: #f5f7fa;
            position: relative;
            overflow-x: hidden;
        }
        
        /* Particle Background */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.3;
        }
        
        .particle {
            position: absolute;
            border-radius: 50%;
            background: radial-gradient(circle, var(--primary-blue), transparent);
            opacity: 0.6;
        }
        
        /* Navigation */
        nav {
            background: linear-gradient(135deg, var(--dark-blue), var(--primary-blue));
            color: white;
            padding: 1.2rem 2rem;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 18px rgba(0,0,0,0.1);
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
            font-size: 2rem;
            font-weight: 700;
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
            transition: all 0.3s ease;
        }
        
        .logo:hover {
            transform: scale(1.05);
        }
        
        .logo i {
            margin-right: 12px;
            color: var(--highlight-yellow);
        }
        
        .nav-links {
            display: flex;
            gap: 2.5rem;
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
            width: 0;
            height: 3px;
            bottom: 0;
            left: 0;
            background-color: var(--highlight-yellow);
            transition: width 0.3s ease;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .nav-links a:hover {
            color: var(--highlight-yellow);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--dark-blue), var(--primary-blue));
            color: white;
            padding: 6rem 2rem 8rem;
            text-align: center;
            position: relative;
            overflow: hidden;
            clip-path: polygon(0 0, 100% 0, 100% 90%, 0 100%);
        }
        
        .hero::before {
            content: "";
            position: absolute;
            top: -50%;
            left: -50%;
            right: -50%;
            bottom: -50%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: pulse 8s infinite alternate;
        }
        
        @keyframes pulse {
            0% { transform: scale(0.8); opacity: 0.3; }
            100% { transform: scale(1.2); opacity: 0.1; }
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            text-shadow: 0 4px 12px rgba(0,0,0,0.2);
            position: relative;
            display: inline-block;
        }
        
        .hero h1::after {
            content: '';
            position: absolute;
            width: 60%;
            height: 4px;
            bottom: -10px;
            left: 20%;
            background: var(--highlight-yellow);
            border-radius: 2px;
        }
        
        .hero p {
            font-size: 1.3rem;
            max-width: 700px;
            margin: 0 auto 3rem;
            opacity: 0.9;
        }
        
        .cta-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            margin-top: 2rem;
        }
        
        .btn {
            padding: 1rem 2.2rem;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.4s ease;
            display: inline-flex;
            align-items: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }
        
        .btn i {
            margin-right: 8px;
        }
        
        .btn-primary {
            background-color: var(--highlight-yellow);
            color: #1a237e;
        }
        
        .btn-primary:hover {
            background-color: #ffc400;
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 25px rgba(255,214,0,0.3);
        }
        
        .btn-secondary {
            background-color: transparent;
            border: 2px solid white;
            color: white;
        }
        
        .btn-secondary:hover {
            background-color: rgba(255,255,255,0.15);
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }
        
        /* Floating Shapes */
        .floating-shape {
            position: absolute;
            opacity: 0.1;
            z-index: 0;
        }
        
        .shape-1 {
            top: 20%;
            left: 5%;
            width: 100px;
            height: 100px;
            border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
            background: var(--secondary-teal);
            animation: float 8s ease-in-out infinite;
        }
        
        .shape-2 {
            top: 60%;
            right: 10%;
            width: 150px;
            height: 150px;
            border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%;
            background: var(--purple);
            animation: float 10s ease-in-out infinite reverse;
        }
        
        .shape-3 {
            bottom: 15%;
            left: 10%;
            width: 120px;
            height: 120px;
            border-radius: 40% 60% 70% 30% / 40% 50% 60% 70%;
            background: var(--accent-green);
            animation: float 9s ease-in-out infinite 2s;
        }
        
        @keyframes float {
            0% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(5deg); }
            100% { transform: translateY(0) rotate(0deg); }
        }
        
        /* Section Styling */
        .section {
            background-color: white;
            border-radius: 16px;
            padding: 4rem 3rem;
            margin: 3rem 2rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            position: relative;
            z-index: 1;
            transition: transform 0.4s ease, box-shadow 0.4s ease;
            border: none;
            overflow: hidden;
        }
        
        .section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--primary-blue), var(--secondary-teal));
        }
        
        .section:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.1);
        }
        
        h2 {
            color: var(--dark-blue);
            border-bottom: none;
            padding-bottom: 0;
            margin-top: 0;
            font-size: 2.5rem;
            background: none;
            padding: 0;
            text-align: center;
            position: relative;
            margin-bottom: 3rem;
        }
        
        h2::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            background: linear-gradient(to right, var(--primary-blue), var(--secondary-teal));
            border-radius: 2px;
        }
        
        h3 {
            color: var(--dark-blue);
            margin-top: 2.5rem;
            font-size: 1.8rem;
            border-left: none;
            padding-left: 0;
            position: relative;
            padding-bottom: 0.5rem;
        }
        
        h3::after {
            content: '';
            position: absolute;
            width: 50px;
            height: 3px;
            bottom: 0;
            left: 0;
            background: var(--accent-green);
            border-radius: 2px;
        }
        
        /* Importance Points */
        .importance-points {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2.5rem;
            margin-top: 3rem;
        }
        
        .point-card {
            background: white;
            border-radius: 12px;
            padding: 2.5rem;
            box-shadow: 0 8px 25px rgba(0,0,0,0.05);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(0,0,0,0.03);
        }
        
        .point-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary-blue), var(--secondary-teal));
        }
        
        .point-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
        }
        
        .point-number {
            font-size: 3rem;
            font-weight: bold;
            color: rgba(0,0,0,0.05);
            position: absolute;
            top: 1rem;
            right: 1.5rem;
            z-index: 0;
            font-family: 'Poppins', sans-serif;
        }
        
        .point-content {
            position: relative;
            z-index: 1;
        }
        
        .point-card h4 {
            color: var(--dark-blue);
            margin-top: 0;
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
        }
        
        .point-card h4 i {
            margin-right: 12px;
            color: var(--secondary-teal);
            font-size: 1.8rem;
        }
        
        /* Chart Containers */
        .chart-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(450px, 1fr));
            gap: 2.5rem;
            margin-top: 3rem;
        }
        
        .chart-card {
            background: white;
            border-radius: 14px;
            padding: 2.5rem;
            box-shadow: 0 8px 25px rgba(0,0,0,0.05);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }
        
        .chart-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--primary-blue), var(--secondary-teal));
        }
        
        .chart-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
        }
        
        .chart-wrapper {
            position: relative;
            height: 350px;
            width: 100%;
        }
        
        /* Animated Pie Chart */
        .pie-chart-container {
            position: relative;
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
        }
        
        .pie-chart-wrapper {
            flex: 1;
            position: relative;
        }
        
        .pie-chart-legend {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            font-size: 0.9rem;
            background: rgba(0,0,0,0.03);
            padding: 0.5rem 1rem;
            border-radius: 20px;
        }
        
        .legend-color {
            width: 15px;
            height: 15px;
            border-radius: 3px;
            margin-right: 8px;
        }
        
        /* Comparison Table */
        .comparison-table {
            width: 100%;
            border-collapse: separate;
            border-spacing: 0;
            margin-top: 2rem;
            box-shadow: 0 5px 25px rgba(0,0,0,0.05);
            border-radius: 12px;
            overflow: hidden;
        }
        
        .comparison-table th, .comparison-table td {
            padding: 1.2rem 1.5rem;
            text-align: left;
            border-bottom: 1px solid rgba(0,0,0,0.05);
        }
        
        .comparison-table th {
            background-color: var(--dark-blue);
            color: white;
            font-weight: 600;
            text-transform: uppercase;
            font-size: 0.9rem;
            letter-spacing: 0.5px;
        }
        
        .comparison-table tr:nth-child(even) {
            background-color: #f8fafc;
        }
        
        .comparison-table tr:hover {
            background-color: #f1f5f9;
        }
        
        .comparison-table tr:last-child td {
            border-bottom: none;
        }
        
        .check-mark {
            color: var(--accent-green);
            font-weight: bold;
            font-size: 1.1rem;
        }
        
        .cross-mark {
            color: var(--danger-red);
            font-weight: bold;
            font-size: 1.1rem;
        }
        
        /* TestUrSelf Advantage */
        .advantage-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2.5rem;
            margin-top: 3rem;
        }
        
        .advantage-card {
            background: white;
            border-radius: 12px;
            padding: 2.5rem;
            box-shadow: 0 8px 25px rgba(0,0,0,0.05);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(0,0,0,0.03);
        }
        
        .advantage-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--secondary-teal), var(--accent-green));
        }
        
        .advantage-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
        }
        
        .advantage-icon {
            font-size: 3rem;
            color: var(--primary-blue);
            margin-bottom: 1.5rem;
            transition: all 0.4s ease;
        }
        
        .advantage-card:hover .advantage-icon {
            transform: scale(1.1) rotate(5deg);
            color: var(--secondary-teal);
        }
        
        .advantage-card h4 {
            color: var(--dark-blue);
            margin-top: 0;
            font-size: 1.4rem;
            margin-bottom: 1.2rem;
        }
        
        /* CTA Sections */
        .cta-section {
            text-align: center;
            padding: 6rem 2rem;
            position: relative;
            overflow: hidden;
            clip-path: polygon(0 10%, 100% 0, 100% 100%, 0% 100%);
            margin-top: 4rem;
        }
        
        .cta-section.gradient {
            background: linear-gradient(135deg, var(--dark-blue), var(--primary-blue));
            color: white;
        }
        
        .cta-section h2 {
            color: white;
            position: relative;
            margin-bottom: 2rem;
        }
        
        .cta-section h2::after {
            background: var(--highlight-yellow);
        }
        
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero {
                padding: 5rem 2rem 7rem;
                clip-path: polygon(0 0, 100% 0, 100% 95%, 0 100%);
            }
            
            .hero h1 {
                font-size: 2.4rem;
            }
            
            .section {
                padding: 3rem 2rem;
                margin: 2rem 1rem;
            }
            
            .importance-points, .advantage-container {
                grid-template-columns: 1fr;
            }
            
            .cta-buttons {
                flex-direction: column;
                gap: 1rem;
            }
        }
        
        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .section {
                padding: 2.5rem 1.5rem;
            }
            
            h2 {
                font-size: 2rem;
            }
            
            .pie-chart-legend {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Particle Background -->
    <div class="particles" id="particles"></div>
    
    <!-- Floating Shapes -->
    <div class="floating-shape shape-1"></div>
    <div class="floating-shape shape-2"></div>
    <div class="floating-shape shape-3"></div>

    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <a href="#" class="logo">
                <i class="fas fa-atom"></i> TestUrSelf
            </a>
            <div class="nav-links">
                <a href="#importance">Importance</a>
                <a href="#data">Data Insights</a>
                <a href="#comparison">Comparison</a>
                <a href="#advantage">Our Edge</a>
                <a href="#cta">Get Started</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Master GATE Metallurgy with Strategic Test Series</h1>
            <p>Data shows students who complete 20+ test series improve their rank by 200+ positions on average</p>
            <div class="cta-buttons">
                <a href="#cta" class="btn btn-primary">
                    <i class="fas fa-rocket"></i> Enroll Now
                </a>
                <a href="#data" class="btn btn-secondary">
                    <i class="fas fa-chart-bar"></i> View Statistics
                </a>
            </div>
        </div>

    </section>

    <!-- Importance Section -->
    <section id="importance" class="section">
        <h2>Why Test Series is Non-Negotiable for GATE MT</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">Analysis of 5,000+ GATE Metallurgy toppers reveals these critical patterns</p>
        
        <div class="importance-points">
            <div class="point-card">
                <div class="point-number">01</div>
                <div class="point-content">
                    <h4><i class="fas fa-stopwatch"></i> Exam Simulation</h4>
                    <p>Replicates actual GATE exam environment - timing, pressure, and question patterns. Our students report 40% better time management in actual exam.</p>
                </div>
            </div>
            
            <div class="point-card">
                <div class="point-number">02</div>
                <div class="point-content">
                    <h4><i class="fas fa-search-minus"></i> Weakness Identification</h4>
                    <p>Detailed analytics pinpoint exactly which topics need more focus. Students improve weak topics by 65% after 5 tests.</p>
                </div>
            </div>
            
            <div class="point-card">
                <div class="point-number">03</div>
                <div class="point-content">
                    <h4><i class="fas fa-clock"></i> Time Management</h4>
                    <p>Learn to allocate time effectively across sections. Top rankers typically save 15-20 minutes through strategic time allocation.</p>
                </div>
            </div>
            
            <div class="point-card">
                <div class="point-number">04</div>
                <div class="point-content">
                    <h4><i class="fas fa-puzzle-piece"></i> Pattern Recognition</h4>
                    <p>Recognize GATE's unique way of framing questions. 78% of our students report seeing similar patterns in actual exam.</p>
                </div>
            </div>
            
            <div class="point-card">
                <div class="point-number">05</div>
                <div class="point-content">
                    <h4><i class="fas fa-lightbulb"></i> Concept Application</h4>
                    <p>Move beyond theory to practical problem-solving. Each test applies 50+ key metallurgy concepts in exam scenarios.</p>
                </div>
            </div>
            
            <div class="point-card">
                <div class="point-number">06</div>
                <div class="point-content">
                    <h4><i class="fas fa-chart-line"></i> Performance Tracking</h4>
                    <p>Measure improvement over time with our advanced analytics dashboard. Students improving 5% per test typically achieve AIR < 100.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Data Insights Section -->
    <section id="data" class="section">
        <h2>Data-Backed Performance Insights</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">Metrics from 1,200+ GATE Metallurgy aspirants who took our test series</p>
        
        <div class="chart-container">
            <div class="chart-card">
                <h3>Test Attempts vs AIR Achieved</h3>
                <div class="chart-wrapper">
                    <canvas id="rankCorrelationChart"></canvas>
                </div>
                <p style="text-align: center; margin-top: 1rem; font-weight: 500; color: var(--dark-blue);">Students taking 15+ tests are 3.2x more likely to achieve AIR < 100</p>
            </div>
            
            <div class="chart-card">
                <h3>Topic-Wise Score Improvement</h3>
                <div class="chart-wrapper">
                    <canvas id="topicImprovementChart"></canvas>
                </div>
                <p style="text-align: center; margin-top: 1rem; font-weight: 500; color: var(--dark-blue);">Average score increase after 10 test series attempts</p>
            </div>
            
            <div class="chart-card">
                <h3>Test Series Participation</h3>
                <div class="chart-wrapper">
                    <div class="pie-chart-container">
                        <div class="pie-chart-wrapper">
                            <canvas id="participationChart"></canvas>
                        </div>
                        <div class="pie-chart-legend">
                            <div class="legend-item">
                                <span class="legend-color" style="background: #2962ff;"></span>
                                <span>1-5 Tests (28%)</span>
                            </div>
                            <div class="legend-item">
                                <span class="legend-color" style="background: #00bfa5;"></span>
                                <span>6-10 Tests (35%)</span>
                            </div>
                            <div class="legend-item">
                                <span class="legend-color" style="background: #7c4dff;"></span>
                                <span>11-15 Tests (25%)</span>
                            </div>
                            <div class="legend-item">
                                <span class="legend-color" style="background: #00c853;"></span>
                                <span>16-20 Tests (12%)</span>
                            </div>
                        </div>
                    </div>
                </div>
                <p style="text-align: center; margin-top: 1rem; font-weight: 500; color: var(--dark-blue);">Only 12% complete recommended 20+ tests</p>
            </div>
            
            <div class="chart-card">
                <h3>Time Management Progress</h3>
                <div class="chart-wrapper">
                    <canvas id="timeManagementChart"></canvas>
                </div>
                <p style="text-align: center; margin-top: 1rem; font-weight: 500; color: var(--dark-blue);">Students save 22 minutes on average by test #15</p>
            </div>
        </div>
    </section>

    <!-- Comparison Section -->
    <section id="comparison" class="section">
        <h2>With vs Without Test Series Preparation</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">Comparative analysis of 2023 GATE Metallurgy results (n=2,500)</p>
        
        <table class="comparison-table">
            <thead>
                <tr>
                    <th>Parameter</th>
                    <th>With Test Series</th>
                    <th>Without Test Series</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Average Score</td>
                    <td class="check-mark">68.5</td>
                    <td class="cross-mark">52.3</td>
                </tr>
                <tr>
                    <td>AIR < 100</td>
                    <td class="check-mark">32%</td>
                    <td class="cross-mark">8%</td>
                </tr>
                <tr>
                    <td>Time Management</td>
                    <td class="check-mark">92% completed paper</td>
                    <td class="cross-mark">67% completed paper</td>
                </tr>
                <tr>
                    <td>Negative Marking</td>
                    <td class="check-mark">-4.2 avg</td>
                    <td class="cross-mark">-9.8 avg</td>
                </tr>
                <tr>
                    <td>Conceptual Errors</td>
                    <td class="check-mark">1.2 per paper</td>
                    <td class="cross-mark">3.7 per paper</td>
                </tr>
                <tr>
                    <td>Exam Day Confidence</td>
                    <td class="check-mark">8.7/10</td>
                    <td class="cross-mark">5.2/10</td>
                </tr>
            </tbody>
        </table>
        
        <div class="chart-container" style="margin-top: 3rem;">
            <div class="chart-card" style="grid-column: 1 / -1;">
                <h3>Score Progression Over Test Attempts</h3>
                <div class="chart-wrapper">
                    <canvas id="improvementChart"></canvas>
                </div>
                <p style="text-align: center; margin-top: 1rem; font-weight: 500; color: var(--dark-blue);">Average score progression of students taking our test series (n=850)</p>
            </div>
        </div>
    </section>

    <!-- TestUrSelf Advantage Section -->
    <section id="advantage" class="section">
        <h2>The TestUrSelf Advantage</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">Why our GATE Metallurgy test series delivers superior results</p>
        
        <div class="advantage-container">
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-atom"></i>
                </div>
                <h4>MT-Specific Content</h4>
                <p>Exclusive focus on Metallurgy with questions designed by IIT professors who've set GATE papers.</p>
            </div>
            
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-brain"></i>
                </div>
                <h4>AI-Powered Analytics</h4>
                <p>Our algorithm predicts your weak areas with 92% accuracy and suggests personalized improvements.</p>
            </div>
            
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-trophy"></i>
                </div>
                <h4>Proven AIR 1 Results</h4>
                <p>4 consecutive years of producing GATE MT toppers with identical test series methodology.</p>
            </div>
            
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-project-diagram"></i>
                </div>
                <h4>Dynamic Question Bank</h4>
                <p>5,000+ questions with 30% annual renewal to match evolving GATE patterns.</p>
            </div>
            
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-chalkboard-teacher"></i>
                </div>
                <h4>Expert Video Solutions</h4>
                <p>Every question comes with detailed video explanations from top faculty.</p>
            </div>
            
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-percentage"></i>
                </div>
                <h4>High Match Rate</h4>
                <p>Last year, 22 questions matched directly with our final test series papers.</p>
            </div>
        </div>
        
        <div class="chart-container" style="margin-top: 3rem;">
            <div class="chart-card">
                <h3>Platform Comparison</h3>
                <div class="chart-wrapper">
                    <canvas id="platformComparisonChart"></canvas>
                </div>
                <p style="text-align: center; margin-top: 1rem; font-weight: 500; color: var(--dark-blue);">Student satisfaction survey (2023 GATE batch)</p>
            </div>
            
            <div class="chart-card">
                <h3>Question Match Rate</h3>
                <div class="chart-wrapper">
                    <div class="pie-chart-container">
                        <div class="pie-chart-wrapper">
                            <canvas id="matchRateChart"></canvas>
                        </div>
                        <div class="pie-chart-legend">
                            <div class="legend-item">
                                <span class="legend-color" style="background: #2962ff;"></span>
                                <span>Direct Match (22%)</span>
                            </div>
                            <div class="legend-item">
                                <span class="legend-color" style="background: #00bfa5;"></span>
                                <span>Concept Match (63%)</span>
                            </div>
                           
                             
                          
                            <div class="legend-item">
                                <span class="legend-color" style="background: #7c4dff;"></span>
                                <span>No Match (15%)</span>
                            </div>
                        </div>
                          <p style="text-align: center; margin-top: 0.5rem; font-weight: 500; color: var(--dark-blue);">Our tests have highest conceptual match with actual GATE</p>
                    </div>
                </div>
             
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section id="cta" class="cta-section gradient">
        <h2>Ready to Transform Your GATE Preparation?</h2>
        <p style="max-width: 700px; margin: 0 auto 3rem;">Join thousands of successful Metallurgy aspirants who trusted TestUrSelf</p>
        
        <div class="cta-buttons">
            <a href="#" class="btn btn-primary">
                <i class="fas fa-gem"></i> Premium Test Series
            </a>
            <a href="#" class="btn btn-secondary">
                <i class="fas fa-book-open"></i> Free Demo Test
            </a>
        </div>
    </section>

    <script>
        // Create Particle Background
        function createParticles() {
            const container = document.getElementById('particles');
            const particleCount = 30;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                
                // Random properties
                const size = Math.random() * 10 + 5;
                const posX = Math.random() * 100;
                const posY = Math.random() * 100;
                const delay = Math.random() * 5;
                const duration = Math.random() * 10 + 10;
                
                // Apply styles
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                particle.style.left = `${posX}%`;
                particle.style.top = `${posY}%`;
                particle.style.animation = `float ${duration}s ease-in-out ${delay}s infinite alternate`;
                
                container.appendChild(particle);
            }
        }
        
        // Initialize Charts
        function initCharts() {
            // Rank Correlation Chart
            const rankCtx = document.getElementById('rankCorrelationChart').getContext('2d');
            new Chart(rankCtx, {
                type: 'bar',
                data: {
                    labels: ['0-5 Tests', '6-10 Tests', '11-15 Tests', '16-20 Tests', '20+ Tests'],
                    datasets: [{
                        label: '% Achieving AIR < 100',
                        data: [5, 12, 28, 42, 67],
                        backgroundColor: [
                            'rgba(41, 98, 255, 0.7)',
                            'rgba(41, 98, 255, 0.7)',
                            'rgba(41, 98, 255, 0.7)',
                            'rgba(41, 98, 255, 0.7)',
                            'rgba(0, 200, 83, 0.7)'
                        ],
                        borderColor: [
                            'rgba(41, 98, 255, 1)',
                            'rgba(41, 98, 255, 1)',
                            'rgba(41, 98, 255, 1)',
                            'rgba(41, 98, 255, 1)',
                            'rgba(0, 200, 83, 1)'
                        ],
                        borderWidth: 2,
                        borderRadius: 6
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            display: false
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `${context.parsed.y}% achieve AIR < 100`;
                                }
                            }
                        }
                    },
                    scales: {
                        y: {
                            beginAtZero: true,
                            max: 100,
                            grid: {
                                color: 'rgba(0,0,0,0.05)'
                            },
                            ticks: {
                                callback: function(value) {
                                    return value + '%';
                                }
                            }
                        },
                        x: {
                            grid: {
                                display: false
                            }
                        }
                    }
                }
            });
            
            // Topic Improvement Chart
            const topicCtx = document.getElementById('topicImprovementChart').getContext('2d');
            new Chart(topicCtx, {
                type: 'radar',
                data: {
                    labels: ['Physical Metallurgy', 'Mechanical Metallurgy', 'Manufacturing', 'Thermodynamics', 'Extractive', 'Maths'],
                    datasets: [{
                        label: 'Initial Accuracy',
                        data: [45, 52, 38, 60, 48, 65],
                        backgroundColor: 'rgba(41, 98, 255, 0.2)',
                        borderColor: 'rgba(41, 98, 255, 1)',
                        borderWidth: 2,
                        pointBackgroundColor: 'rgba(41, 98, 255, 1)',
                        pointRadius: 4
                    }, {
                        label: 'After 10 Tests',
                        data: [78, 82, 75, 88, 80, 92],
                        backgroundColor: 'rgba(0, 191, 165, 0.2)',
                        borderColor: 'rgba(0, 191, 165, 1)',
                        borderWidth: 2,
                        pointBackgroundColor: 'rgba(0, 191, 165, 1)',
                        pointRadius: 4
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            position: 'top',
                            labels: {
                                usePointStyle: true,
                                padding: 20
                            }
                        }
                    },
                    scales: {
                        r: {
                            angleLines: {
                                color: 'rgba(0,0,0,0.1)'
                            },
                            suggestedMin: 30,
                            suggestedMax: 100,
                            grid: {
                                color: 'rgba(0,0,0,0.05)'
                            },
                            pointLabels: {
                                font: {
                                    size: 11
                                }
                            },
                            ticks: {
                                display: false,
                                stepSize: 20
                            }
                        }
                    },
                    elements: {
                        line: {
                            tension: 0.1
                        }
                    }
                }
            });
            
            // Participation Chart
            const participationCtx = document.getElementById('participationChart').getContext('2d');
            new Chart(participationCtx, {
                type: 'doughnut',
                data: {
                    labels: ['1-5 Tests', '6-10 Tests', '11-15 Tests', '16-20 Tests'],
                    datasets: [{
                        data: [28, 35, 25, 12],
                        backgroundColor: [
                            'rgba(41, 98, 255, 0.8)',
                            'rgba(0, 191, 165, 0.8)',
                            'rgba(124, 77, 255, 0.8)',
                            'rgba(0, 200, 83, 0.8)'
                        ],
                        borderColor: [
                            'rgba(41, 98, 255, 1)',
                            'rgba(0, 191, 165, 1)',
                            'rgba(124, 77, 255, 1)',
                            'rgba(0, 200, 83, 1)'
                        ],
                        borderWidth: 1,
                        hoverOffset: 10
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    cutout: '65%',
                    plugins: {
                        legend: {
                            display: false
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `${context.label}: ${context.raw}%`;
                                }
                            }
                        }
                    },
                    animation: {
                        animateScale: true,
                        animateRotate: true
                    }
                }
            });
            
            // Time Management Chart
            const timeCtx = document.getElementById('timeManagementChart').getContext('2d');
            new Chart(timeCtx, {
                type: 'line',
                data: {
                    labels: ['Test 1', 'Test 3', 'Test 5', 'Test 10', 'Test 15', 'Test 20'],
                    datasets: [{
                        label: 'Time Left (minutes)',
                        data: [-12, -5, 3, 10, 18, 22],
                        backgroundColor: 'rgba(41, 98, 255, 0.1)',
                        borderColor: 'rgba(41, 98, 255, 1)',
                        borderWidth: 3,
                        tension: 0.3,
                        fill: true,
                        pointBackgroundColor: 'white',
                        pointBorderColor: 'rgba(41, 98, 255, 1)',
                        pointBorderWidth: 2,
                        pointRadius: 5,
                        pointHoverRadius: 7
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            display: false
                        }
                    },
                    scales: {
                        y: {
                            beginAtZero: false,
                            grid: {
                                color: 'rgba(0,0,0,0.05)'
                            },
                            title: {
                                display: true,
                                text: 'Minutes Left'
                            }
                        },
                        x: {
                            grid: {
                                display: false
                            }
                        }
                    }
                }
            });
            
            // Improvement Chart
            const improvementCtx = document.getElementById('improvementChart').getContext('2d');
            new Chart(improvementCtx, {
                type: 'line',
                data: {
                    labels: ['Baseline', 'After 5 Tests', 'After 10 Tests', 'After 15 Tests', 'After 20 Tests', 'GATE Actual'],
                    datasets: [{
                        label: 'Average Score',
                        data: [32, 45, 58, 67, 72, 68],
                        backgroundColor: 'rgba(41, 98, 255, 0.1)',
                        borderColor: 'rgba(41, 98, 255, 1)',
                        borderWidth: 3,
                        tension: 0.3,
                        fill: true,
                        pointBackgroundColor: 'white',
                        pointBorderColor: 'rgba(41, 98, 255, 1)',
                        pointBorderWidth: 2,
                        pointRadius: 5,
                        pointHoverRadius: 7
                    }, {
                        label: 'AIR < 100 Cutoff',
                        data: [65, 65, 65, 65, 65, 65],
                        backgroundColor: 'rgba(255, 23, 68, 0.05)',
                        borderColor: 'rgba(255, 23, 68, 1)',
                        borderWidth: 2,
                        borderDash: [5, 5],
                        tension: 0,
                        pointRadius: 0
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            position: 'top',
                            labels: {
                                usePointStyle: true,
                                padding: 20
                            }
                        }
                    },
                    scales: {
                        y: {
                            beginAtZero: true,
                            max: 100,
                            grid: {
                                color: 'rgba(0,0,0,0.05)'
                            },
                            title: {
                                display: true,
                                text: 'Marks (out of 100)'
                            }
                        },
                        x: {
                            grid: {
                                display: false
                            }
                        }
                    }
                }
            });
            
            // Platform Comparison Chart
            const platformCtx = document.getElementById('platformComparisonChart').getContext('2d');
            new Chart(platformCtx, {
                type: 'bar',
                data: {
                    labels: ['TestUrSelf', 'Platform A', 'Platform B', 'Platform C'],
                    datasets: [{
                        label: 'Satisfaction Score (out of 10)',
                        data: [9.2, 7.1, 6.8, 6.3],
                        backgroundColor: [
                            'rgba(41, 98, 255, 0.8)',
                            'rgba(158, 158, 158, 0.8)',
                            'rgba(158, 158, 158, 0.8)',
                            'rgba(158, 158, 158, 0.8)'
                        ],
                        borderColor: [
                            'rgba(41, 98, 255, 1)',
                            'rgba(97, 97, 97, 1)',
                            'rgba(97, 97, 97, 1)',
                            'rgba(97, 97, 97, 1)'
                        ],
                        borderWidth: 1,
                        borderRadius: 6
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            display: false
                        }
                    },
                    scales: {
                        y: {
                            beginAtZero: true,
                            max: 10,
                            grid: {
                                color: 'rgba(0,0,0,0.05)'
                            }
                        },
                        x: {
                            grid: {
                                display: false
                            }
                        }
                    }
                }
            });
            
            // Match Rate Chart
            const matchCtx = document.getElementById('matchRateChart').getContext('2d');
            new Chart(matchCtx, {
                type: 'doughnut',
                data: {
                    labels: ['Direct Match', 'Conceptual Match', 'No Match'],
                    datasets: [{
                        data: [22, 63, 15],
                        backgroundColor: [
                            'rgba(41, 98, 255, 0.8)',
                            'rgba(0, 191, 165, 0.8)',
                            'rgba(124, 77, 255, 0.8)'
                        ],
                        borderColor: [
                            'rgba(41, 98, 255, 1)',
                            'rgba(0, 191, 165, 1)',
                            'rgba(124, 77, 255, 1)'
                        ],
                        borderWidth: 1,
                        hoverOffset: 10
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    cutout: '70%',
                    plugins: {
                        legend: {
                            display: false
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `${context.label}: ${context.raw}%`;
                                }
                            }
                        }
                    },
                    animation: {
                        animateScale: true,
                        animateRotate: true
                    }
                }
            });
        }
        
        // Initialize GSAP Animations
        function initAnimations() {
            gsap.registerPlugin(ScrollTrigger);
            
            // Animate hero elements
            gsap.from('.hero h1', {
                duration: 1,
                y: 50,
                opacity: 0,
                ease: 'power3.out'
            });
            
            gsap.from('.hero p', {
                duration: 1,
                y: 30,
                opacity: 0,
                delay: 0.3,
                ease: 'power3.out'
            });
            
            gsap.from('.cta-buttons', {
                duration: 1,
                y: 30,
                opacity: 0,
                delay: 0.6,
                ease: 'power3.out'
            });
            
            // Animate section headings
            gsap.utils.toArray('h2').forEach((heading, i) => {
                gsap.from(heading, {
                    scrollTrigger: {
                        trigger: heading,
                        start: 'top 80%'
                    },
                    duration: 0.8,
                    y: 30,
                    opacity: 0,
                    ease: 'power3.out'
                });
            });
            
            // Animate cards
            gsap.utils.toArray('.point-card, .advantage-card, .chart-card').forEach((card, i) => {
                gsap.from(card, {
                    scrollTrigger: {
                        trigger: card,
                        start: 'top 80%'
                    },
                    duration: 0.6,
                    y: 40,
                    opacity: 0,
                    delay: i * 0.1,
                    ease: 'power3.out'
                });
            });
            
            // Animate table rows
            gsap.utils.toArray('.comparison-table tr').forEach((row, i) => {
                gsap.from(row, {
                    scrollTrigger: {
                        trigger: row,
                        start: 'top 90%'
                    },
                    duration: 0.5,
                    x: i % 2 === 0 ? -30 : 30,
                    opacity: 0,
                    delay: i * 0.05,
                    ease: 'power3.out'
                });
            });
            
            // Make navigation links clickable with smooth scroll
            document.querySelectorAll('.nav-link').forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    
                    if (targetElement) {
                        gsap.to(window, {
                            duration: 1,
                            scrollTo: {
                                y: targetElement,
                                offsetY: 80
                            },
                            ease: 'power3.inOut'
                        });
                        
                        // Update active state
                        document.querySelectorAll('.nav-link').forEach(navLink => {
                            navLink.classList.remove('active');
                        });
                        this.classList.add('active');
                    }
                });
            });
        }
        
        // Initialize everything when DOM loads
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            initCharts();
            initAnimations();
        });
    </script>
</body>
</html>
