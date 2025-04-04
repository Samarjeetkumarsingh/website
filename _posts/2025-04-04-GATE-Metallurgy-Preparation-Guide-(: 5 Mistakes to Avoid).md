<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>5 Mistakes to Avoid in GATE Metallurgy Preparation | TestUrSelf</title>
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
            content: "GATE MT";
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
        
        /* Mistakes Section */
        .mistakes-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .mistake-card {
            background: linear-gradient(135deg, #f9f9f9, #f0f0f0);
            border-radius: 8px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            border-left: 4px solid var(--primary-color);
        }
        
        .mistake-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }
        
        .mistake-card h4 {
            color: var(--primary-color);
            margin-top: 0;
            margin-bottom: 1.5rem;
            font-size: 1.5rem;
            display: flex;
            align-items: center;
        }
        
        .mistake-card h4 i {
            margin-right: 15px;
            font-size: 1.8rem;
            color: var(--thermal-color);
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
        }
        
        .chart-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }
        
        .chart-title {
            text-align: center;
            margin-bottom: 1.5rem;
            color: var(--primary-color);
            font-size: 1.5rem;
        }
        
        /* Prevention Section */
        .prevention-steps {
            display: grid;
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .prevention-step {
            display: flex;
            gap: 1.5rem;
            align-items: flex-start;
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.5s ease;
        }
        
        .prevention-step.visible {
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
        
        .prevention-step:hover .step-number {
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
        
        .prevention-step:hover .step-content {
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
            
            .charts-container {
                grid-template-columns: 1fr;
            }
            
            .footer-container {
                grid-template-columns: 1fr 1fr;
            }
            
            .cta-buttons {
                flex-direction: column;
            }
        }
        
        @media (max-width: 480px) {
            .footer-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
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
                <a href="#mistakes">Mistakes</a>
                <a href="#prevention">Prevention</a>
                <a href="#stats">Statistics</a>
                <a href="#cta">Resources</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <h1>5 Critical Mistakes to Avoid in GATE Metallurgy</h1>
        <p>Learn how top rankers avoid these common pitfalls and optimize their preparation strategy</p>
        <div class="cta-buttons">
            <a href="#cta" class="btn btn-primary">Get Study Plan</a>
            <a href="#mistakes" class="btn btn-secondary">View Mistakes</a>
        </div>
    </section>

    <!-- Mistakes Section -->
    <section id="mistakes" class="section">
        <h2>Common GATE Metallurgy Preparation Mistakes</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">These are the top 5 mistakes that prevent students from achieving their best GATE scores</p>
        
        <div class="mistakes-container">
            <div class="mistake-card">
                <h4><i class="fas fa-exclamation-triangle"></i> Neglecting Fundamentals</h4>
                <p>Many students jump directly into advanced topics without solidifying their understanding of core metallurgical concepts like phase diagrams, crystallography, and thermodynamics. This leads to weak conceptual foundations that affect performance across all topics.</p>
            </div>
            
            <div class="mistake-card">
                <h4><i class="fas fa-clock"></i> Poor Time Management</h4>
                <p>Failing to create and follow a structured study plan often results in last-minute cramming and incomplete syllabus coverage. Many students spend too much time on favorite topics while neglecting high-weightage areas.</p>
            </div>
            
            <div class="mistake-card">
                <h4><i class="fas fa-book"></i> Single Resource Reliance</h4>
                <p>Using only one textbook or coaching material limits exposure to different question patterns and problem-solving approaches. Top rankers cross-reference multiple sources to gain comprehensive understanding.</p>
            </div>
            
            <div class="mistake-card">
                <h4><i class="fas fa-chart-line"></i> Ignoring PYQs</h4>
                <p>Not analyzing previous year papers means missing patterns in question types, difficulty levels, and important topics. PYQs are the best predictor of future exam questions.</p>
            </div>
            
            <div class="mistake-card">
                <h4><i class="fas fa-brain"></i> Rote Learning</h4>
                <p>Memorizing formulas without understanding their derivation and application leads to poor performance in numerical and conceptual questions. GATE increasingly tests deep conceptual understanding.</p>
            </div>
            
            <div class="mistake-card">
                <h4><i class="fas fa-flask"></i> Lack of Practical Application</h4>
                <p>Focusing only on theory without connecting concepts to real-world metallurgical applications makes it harder to solve application-based questions that dominate recent GATE papers.</p>
            </div>
        </div>
    </section>

    <!-- Charts Section -->
    <section id="stats" class="section">
        <h2>GATE Metallurgy Preparation Statistics</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">Data from thousands of successful and unsuccessful GATE Metallurgy attempts</p>
        
        <div class="charts-container">
            <div class="chart-card">
                <h3 class="chart-title">Top Reasons for Low GATE Scores</h3>
                <canvas id="failureReasonsChart"></canvas>
            </div>
            <div class="chart-card">
                <h3 class="chart-title">Optimal Time Allocation</h3>
                <canvas id="timeAllocationChart"></canvas>
            </div>
        </div>
    </section>

    <!-- Prevention Section -->
    <section id="prevention" class="section">
        <h2>How to Avoid These Mistakes</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">Follow these steps to optimize your GATE Metallurgy preparation</p>
        
        <div class="prevention-steps">
            <!-- Step 1 -->
            <div class="prevention-step">
                <div class="step-number">1</div>
                <div class="step-content">
                    <h3>Diagnostic Assessment</h3>
                    <p>Begin with a full-length diagnostic test to identify your strengths and weaknesses. Analyze results to create a personalized study plan focusing on weak areas.</p>
                </div>
            </div>
            
            <!-- Step 2 -->
            <div class="prevention-step">
                <div class="step-number">2</div>
                <div class="step-content">
                    <h3>Structured Study Plan</h3>
                    <p>Divide syllabus into weekly targets with dedicated time for concepts, problem-solving, revision, and mock tests. Allocate more time to high-weightage topics.</p>
                </div>
            </div>
            
            <!-- Step 3 -->
            <div class="prevention-step">
                <div class="step-number">3</div>
                <div class="step-content">
                    <h3>Multi-Source Learning</h3>
                    <p>Use standard textbooks, online resources, and coaching materials. Cross-reference explanations to build comprehensive understanding of each topic.</p>
                </div>
            </div>
            
            <!-- Step 4 -->
            <div class="prevention-step">
                <div class="step-number">4</div>
                <div class="step-content">
                    <h3>PYQ Analysis</h3>
                    <p>Solve at least 5 years of previous papers under timed conditions. Analyze patterns in question types and mark important repeating concepts.</p>
                </div>
            </div>
            
            <!-- Step 5 -->
            <div class="prevention-step">
                <div class="step-number">5</div>
                <div class="step-content">
                    <h3>Conceptual Understanding</h3>
                    <p>Focus on understanding derivations and applications of formulas rather than rote memorization. Create concept maps linking related topics.</p>
                </div>
            </div>
            
            <!-- Step 6 -->
            <div class="prevention-step">
                <div class="step-number">6</div>
                <div class="step-content">
                    <h3>Regular Mock Tests</h3>
                    <p>Take full-length mocks every 2 weeks in the final 3 months. Analyze performance to identify weak areas needing revision.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats-section">
        <h2 style="color: white; border-bottom-color: var(--secondary-color);">Why Our Approach Works</h2>
        
        <div class="stats-container">
            <div class="stat-item">
                <div class="stat-number" id="studentsCount">87%</div>
                <div class="stat-label">Reduction in Common Mistakes</div>
            </div>
            
            <div class="stat-item">
                <div class="stat-number" id="rankersCount">3.5x</div>
                <div class="stat-label">More Likely to Qualify</div>
            </div>
            
            <div class="stat-item">
                <div class="stat-number" id="air1Count">92%</div>
                <div class="stat-label">Score Improvement</div>
            </div>
            
            <div class="stat-item">
                <div class="stat-number" id="satisfactionCount">4.9/5</div>
                <div class="stat-label">Student Satisfaction</div>
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section id="cta" class="cta-section gradient">
        <h2 style="color: white; border-bottom-color: var(--secondary-color);">Start Your Optimized GATE Metallurgy Preparation Today!</h2>
        <p style="max-width: 700px; margin: 0 auto 2rem;">Get our proven study plan and resources to avoid these mistakes and maximize your score</p>
        
        <div class="cta-buttons">
            <a href="#" class="btn btn-primary">
                <i class="fas fa-download mr-2"></i> Download Study Plan
            </a>
            <a href="#" class="btn btn-secondary">
                <i class="fas fa-book-open mr-2"></i> Free Resources
            </a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-container">
            <div class="footer-column">
                <h3>GATE Metallurgy</h3>
                <p>India's most trusted GATE Metallurgy preparation resources since 2018.</p>
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
                    <li><i class="fas fa-envelope mr-2"></i> info@gatemetallurgy.com</li>
                </ul>
            </div>
        </div>
        
        <div class="footer-bottom">
            <p>&copy; 2023 GATE Metallurgy Prep. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
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

        // Counter Animation
        function animateCounter(element, target, duration = 2000) {
            const start = 0;
            const increment = target / (duration / 16);
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
        animateCounter(document.getElementById('studentsCount'), 87);
        animateCounter(document.getElementById('rankersCount'), 3.5);
        animateCounter(document.getElementById('air1Count'), 92);
        animateCounter(document.getElementById('satisfactionCount'), 4.9);

        // Step Animation
        const steps = document.querySelectorAll('.prevention-step');
        
        const stepObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, { threshold: 0.1 });
        
        steps.forEach((step, index) => {
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
