<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>5 Mistakes to Avoid While Preparing for GATE Metallurgy</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        :root {
            --primary-blue: #1e88e5;
            --sky-blue: #87CEEB;
            --light-blue: #e3f2fd;
            --dark-blue: #1565c0;
            --primary-green: #43a047;
            --light-green: #90EE90;
            --dark-green: #2e7d32;
            --accent-color: #ff9800;
            --text-color: #212121;
            --light-gray: #f5f5f5;
            --gradient-bg: linear-gradient(135deg, var(--sky-blue), var(--light-green));
            --shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--light-gray);
            color: var(--text-color);
            line-height: 1.8;
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
            content: "GATE MT";
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-30deg);
            font-size: 120px;
            font-weight: bold;
            color: rgba(30, 136, 229, 0.05);
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
            background: linear-gradient(135deg, var(--primary-blue), var(--dark-blue));
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
            color: var(--light-green);
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
        }

        .nav-links a:hover {
            color: var(--light-green);
            transform: translateY(-2px);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, rgba(30, 136, 229, 0.9), rgba(67, 160, 71, 0.9)), 
                        url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-blend-mode: overlay;
            height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
            color: white;
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

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
        }

        .hero h1 {
            font-size: 3.2rem;
            margin-bottom: 1.5rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            animation: fadeInDown 1s ease-out;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2.5rem;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
            animation: fadeIn 1.5s ease-out;
        }

        .cta-button {
            display: inline-block;
            background-color: var(--primary-green);
            color: white;
            padding: 14px 32px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.2rem;
            transition: var(--transition);
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            animation: pulse 2s infinite;
            border: 2px solid transparent;
        }

        .cta-button:hover {
            background-color: var(--dark-green);
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.3);
            border-color: white;
        }

        /* Main Content */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        .section {
            background-color: white;
            border-radius: 12px;
            padding: 3rem;
            margin: 2rem 0;
            box-shadow: var(--shadow);
            position: relative;
            z-index: 1;
            transition: var(--transition);
            border: 1px solid rgba(0,0,0,0.05);
        }

        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--primary-blue);
            font-size: 2.4rem;
            position: relative;
            padding-bottom: 1rem;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 100px;
            height: 5px;
            background: linear-gradient(to right, var(--sky-blue), var(--light-green));
            margin: 1rem auto 0;
            border-radius: 5px;
        }

        /* Mistakes List */
        .mistakes-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }

        .mistake-item {
            background: white;
            border-radius: 12px;
            padding: 30px;
            box-shadow: var(--shadow);
            transition: var(--transition);
            opacity: 0;
            transform: translateY(30px);
            border-top: 4px solid var(--primary-blue);
        }

        .mistake-item.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .mistake-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
            border-top-color: var(--primary-green);
        }

        .mistake-icon {
            font-size: 2.8rem;
            color: var(--accent-color);
            margin-bottom: 20px;
            transition: var(--transition);
        }

        .mistake-item:hover .mistake-icon {
            transform: scale(1.1);
            color: var(--primary-green);
        }

        .mistake-title {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--dark-blue);
            position: relative;
            padding-bottom: 10px;
        }

        .mistake-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: linear-gradient(to right, var(--sky-blue), transparent);
            border-radius: 3px;
        }

        /* Charts Section */
        .charts-section {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }

        .chart-container {
            background: white;
            border-radius: 12px;
            padding: 30px;
            box-shadow: var(--shadow);
            transition: var(--transition);
            border: 1px solid rgba(0,0,0,0.05);
        }

        .chart-container:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }

        .chart-title {
            text-align: center;
            margin-bottom: 25px;
            color: var(--primary-blue);
            font-size: 1.5rem;
            position: relative;
            padding-bottom: 10px;
        }

        .chart-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: linear-gradient(to right, var(--sky-blue), var(--light-green));
            border-radius: 3px;
        }

        /* Infographics */
        .infographics {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }

        .info-card {
            background: white;
            border-radius: 12px;
            padding: 30px;
            box-shadow: var(--shadow);
            text-align: center;
            transition: var(--transition);
            border: 1px solid rgba(0,0,0,0.05);
        }

        .info-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
            background: linear-gradient(135deg, #f9f9f9, #f0f0f0);
        }

        .info-icon {
            font-size: 3rem;
            color: var(--primary-blue);
            margin-bottom: 20px;
            transition: var(--transition);
        }

        .info-card:hover .info-icon {
            transform: scale(1.2);
            color: var(--primary-green);
        }

        .info-title {
            font-size: 1.4rem;
            margin-bottom: 20px;
            color: var(--dark-blue);
            position: relative;
            padding-bottom: 10px;
        }

        .info-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 3px;
            background: var(--primary-green);
            border-radius: 3px;
        }

        /* CTA Section */
        .cta-section {
            background: linear-gradient(135deg, var(--primary-blue), var(--dark-blue));
            padding: 5rem 2rem;
            text-align: center;
            border-radius: 12px;
            margin-bottom: 60px;
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
        }

        .cta-section::after {
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

        .cta-section h2 {
            color: white;
            font-size: 2.2rem;
            margin-bottom: 1.5rem;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.3);
            position: relative;
            z-index: 1;
        }

        .cta-section p {
            color: white;
            font-size: 1.2rem;
            margin-bottom: 2.5rem;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
            position: relative;
            z-index: 1;
        }

        /* Footer */
        footer {
            background: linear-gradient(135deg, var(--dark-blue), #0d47a1);
            color: white;
            padding: 4rem 2rem 2rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .footer-column h3 {
            font-size: 1.4rem;
            margin-bottom: 1.5rem;
            color: var(--light-green);
            position: relative;
            padding-bottom: 10px;
        }

        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--light-green);
            border-radius: 3px;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 12px;
            transition: var(--transition);
        }

        .footer-column ul li:hover {
            transform: translateX(5px);
        }

        .footer-column ul li a {
            color: #e0e0e0;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-column ul li a:hover {
            color: white;
            text-decoration: underline;
        }

        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-icons a {
            color: white;
            font-size: 1.5rem;
            transition: var(--transition);
        }

        .social-icons a:hover {
            color: var(--light-green);
            transform: translateY(-5px);
        }

        .copyright {
            text-align: center;
            margin-top: 50px;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #bdbdbd;
            font-size: 0.9rem;
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 2.8rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero {
                height: 70vh;
            }
            
            .hero h1 {
                font-size: 2.4rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .section {
                padding: 2rem;
            }
            
            .charts-section {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 576px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .section {
                padding: 1.5rem;
                margin: 1rem 0;
            }
            
            .section-title {
                font-size: 1.8rem;
                margin-bottom: 2rem;
            }
            
            .mistake-item, .chart-container, .info-card {
                padding: 20px;
            }
            
            .cta-section {
                padding: 3rem 1.5rem;
            }
            
            .cta-section h2 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <a href="#" class="logo">
                <i class="fas fa-atom"></i> GATE Metallurgy Guide
            </a>
            <div class="nav-links">
                <a href="#mistakes">Mistakes</a>
                <a href="#strategies">Strategies</a>
                <a href="#resources">Resources</a>
                <a href="#download">Study Plan</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Top 5 Mistakes to Avoid While Preparing for GATE Metallurgy</h1>
            <p>Learn how to optimize your preparation strategy and maximize your score by avoiding these common pitfalls</p>
            <a href="#resources" class="cta-button">Start Your Preparation Now</a>
        </div>
    </section>

    <!-- Main Content -->
    <div class="container">
        <!-- Mistakes List -->
        <section id="mistakes" class="section">
            <h2 class="section-title">Common Preparation Mistakes</h2>
            <div class="mistakes-list">
                <div class="mistake-item">
                    <div class="mistake-icon">
                        <i class="fas fa-exclamation-triangle"></i>
                    </div>
                    <h3 class="mistake-title">Neglecting Fundamentals</h3>
                    <p>Many students jump directly into advanced topics without solidifying their understanding of core metallurgical concepts like phase diagrams, crystallography, and thermodynamics.</p>
                </div>
                
                <div class="mistake-item">
                    <div class="mistake-icon">
                        <i class="fas fa-clock"></i>
                    </div>
                    <h3 class="mistake-title">Poor Time Management</h3>
                    <p>Failing to create and follow a structured study plan often leads to last-minute cramming and incomplete syllabus coverage.</p>
                </div>
                
                <div class="mistake-item">
                    <div class="mistake-icon">
                        <i class="fas fa-book"></i>
                    </div>
                    <h3 class="mistake-title">Over-reliance on Single Resource</h3>
                    <p>Using only one textbook or coaching material limits exposure to different question patterns and problem-solving approaches.</p>
                </div>
                
                <div class="mistake-item">
                    <div class="mistake-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3 class="mistake-title">Ignoring Previous Year Papers</h3>
                    <p>Not analyzing past GATE papers means missing out on understanding question patterns, difficulty levels, and important topics.</p>
                </div>
                
                <div class="mistake-item">
                    <div class="mistake-icon">
                        <i class="fas fa-brain"></i>
                    </div>
                    <h3 class="mistake-title">Lack of Conceptual Clarity</h3>
                    <p>Memorizing formulas without understanding their derivation and application leads to poor performance in numerical and conceptual questions.</p>
                </div>
            </div>
        </section>

        <!-- Charts Section -->
        <section id="stats" class="section">
            <h2 class="section-title">Preparation Insights</h2>
            <div class="charts-section">
                <div class="chart-container">
                    <h3 class="chart-title">Top Reasons Students Fail GATE Metallurgy</h3>
                    <canvas id="failureReasonsChart"></canvas>
                </div>
                <div class="chart-container">
                    <h3 class="chart-title">Time Allocation Among Subjects</h3>
                    <canvas id="timeAllocationChart"></canvas>
                </div>
            </div>
        </section>

        <!-- Infographics -->
        <section id="strategies" class="section">
            <h2 class="section-title">Key Preparation Strategies</h2>
            <div class="infographics">
                <div class="info-card">
                    <div class="info-icon">
                        <i class="fas fa-bullseye"></i>
                    </div>
                    <h3 class="info-title">Focused Study</h3>
                    <p>Prioritize high-weightage topics like Physical Metallurgy, Mechanical Metallurgy, and Thermodynamics which typically account for 60% of the paper.</p>
                </div>
                
                <div class="info-card">
                    <div class="info-icon">
                        <i class="fas fa-calendar-alt"></i>
                    </div>
                    <h3 class="info-title">Time Management</h3>
                    <p>Allocate 40% of time to core subjects, 30% to practice, 20% to revision, and 10% to mock tests for optimal preparation.</p>
                </div>
                
                <div class="info-card">
                    <div class="info-icon">
                        <i class="fas fa-sync-alt"></i>
                    </div>
                    <h3 class="info-title">Revision Techniques</h3>
                    <p>Use spaced repetition with weekly revisions, concept maps for metallurgical processes, and formula sheets for quick review.</p>
                </div>
                
                <div class="info-card">
                    <div class="info-icon">
                        <i class="fas fa-question-circle"></i>
                    </div>
                    <h3 class="info-title">Question Analysis</h3>
                    <p>Analyze 5 years of previous papers to identify patterns - typically 30% conceptual, 50% numerical, and 20% application questions.</p>
                </div>
            </div>
        </section>

        <!-- CTA Section -->
        <div id="download" class="cta-section">
            <h2>Ready to Optimize Your GATE Metallurgy Preparation?</h2>
            <p>Download our comprehensive study plan tailored specifically for Metallurgy students, including topic-wise weightage, monthly targets, and revision schedules.</p>
            <a href="#" class="cta-button">Download Your GATE Metallurgy Study Plan</a>
        </div>
    </div>

    <!-- Footer -->
    <footer id="resources">
        <div class="footer-content">
            <div class="footer-column">
                <h3>GATE Metallurgy Resources</h3>
                <ul>
                    <li><a href="#">Syllabus Breakdown</a></li>
                    <li><a href="#">Recommended Books</a></li>
                    <li><a href="#">Online Courses</a></li>
                    <li><a href="#">Practice Questions</a></li>
                </ul>
            </div>
            
            <div class="footer-column">
                <h3>Study Tips</h3>
                <ul>
                    <li><a href="#">Effective Note-taking</a></li>
                    <li><a href="#">Memory Techniques</a></li>
                    <li><a href="#">Stress Management</a></li>
                    <li><a href="#">Exam Strategies</a></li>
                </ul>
            </div>
            
            <div class="footer-column">
                <h3>Contact Us</h3>
                <ul>
                    <li><a href="#">Email Support</a></li>
                    <li><a href="#">FAQ</a></li>
                    <li><a href="#">Feedback</a></li>
                    <li><a href="#">Consultation</a></li>
                </ul>
            </div>
            
            <div class="footer-column">
                <h3>Join the Community</h3>
                <div class="social-icons">
                    <a href="#"><i class="fab fa-facebook"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-linkedin"></i></a>
                    <a href="#"><i class="fab fa-youtube"></i></a>
                </div>
            </div>
        </div>
        
        <div class="copyright">
            <p>&copy; 2023 GATE Metallurgy Prep Guide. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Scroll animation for mistake items
        document.addEventListener('DOMContentLoaded', function() {
            const mistakeItems = document.querySelectorAll('.mistake-item');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach((entry, index) => {
                    if (entry.isIntersecting) {
                        setTimeout(() => {
                            entry.target.classList.add('visible');
                        }, 150 * index);
                    }
                });
            }, { threshold: 0.1 });
            
            mistakeItems.forEach(item => {
                observer.observe(item);
            });

            // Charts
            const failureReasonsCtx = document.getElementById('failureReasonsChart').getContext('2d');
            const failureReasonsChart = new Chart(failureReasonsCtx, {
                type: 'pie',
                data: {
                    labels: ['Incomplete Syllabus', 'Weak Fundamentals', 'Poor Time Mgmt', 'Lack of Practice', 'Exam Anxiety'],
                    datasets: [{
                        data: [35, 25, 20, 15, 5],
                        backgroundColor: [
                            '#e53935',
                            '#1e88e5',
                            '#43a047',
                            '#fb8c00',
                            '#8e24aa'
                        ],
                        borderWidth: 1
                    }]
                },
                options: {
                    responsive: true,
                    plugins: {
                        legend: {
                            position: 'right',
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `${context.label}: ${context.raw}%`;
                                }
                            }
                        }
                    }
                }
            });

            const timeAllocationCtx = document.getElementById('timeAllocationChart').getContext('2d');
            const timeAllocationChart = new Chart(timeAllocationCtx, {
                type: 'doughnut',
                data: {
                    labels: ['Physical Metallurgy', 'Mechanical Metallurgy', 'Thermodynamics', 'Extractive Metallurgy', 'Other Topics'],
                    datasets: [{
                        data: [30, 25, 20, 15, 10],
                        backgroundColor: [
                            '#1e88e5',
                            '#43a047',
                            '#e53935',
                            '#fb8c00',
                            '#8e24aa'
                        ],
                        borderWidth: 1
                    }]
                },
                options: {
                    responsive: true,
                    plugins: {
                        legend: {
                            position: 'right',
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `${context.label}: ${context.raw}%`;
                                }
                            }
                        }
                    }
                }
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
        });
    </script>
</body>
</html>
