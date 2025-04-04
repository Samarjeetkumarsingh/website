<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>5 Mistakes to Avoid in GATE Metallurgy Preparation</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        :root {
            --sky-blue: #87CEEB;
            --light-green: #90EE90;
            --dark-green: #228B22;
            --gradient-bg: linear-gradient(135deg, var(--sky-blue), var(--light-green));
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f9f9f9;
            color: #333;
            line-height: 1.6;
        }

        /* Hero Section */
        .hero {
            background: var(--gradient-bg), url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
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

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.3);
            z-index: 0;
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            animation: fadeInDown 1s ease-out;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
            animation: fadeIn 1.5s ease-out;
        }

        .cta-button {
            display: inline-block;
            background-color: var(--dark-green);
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            animation: pulse 2s infinite;
        }

        .cta-button:hover {
            background-color: #1e7a1e;
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
        }

        /* Main Content */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
            color: var(--dark-green);
            font-size: 2.2rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--gradient-bg);
            margin: 15px auto 0;
            border-radius: 2px;
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
            border-radius: 10px;
            padding: 25px;
            box-shadow: var(--shadow);
            transition: all 0.3s ease;
            opacity: 0;
            transform: translateY(20px);
        }

        .mistake-item.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .mistake-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
        }

        .mistake-icon {
            font-size: 2.5rem;
            color: #e74c3c;
            margin-bottom: 15px;
        }

        .mistake-title {
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: var(--dark-green);
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
            border-radius: 10px;
            padding: 25px;
            box-shadow: var(--shadow);
        }

        .chart-title {
            text-align: center;
            margin-bottom: 20px;
            color: var(--dark-green);
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
            border-radius: 10px;
            padding: 25px;
            box-shadow: var(--shadow);
            text-align: center;
            transition: all 0.3s ease;
        }

        .info-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
        }

        .info-icon {
            font-size: 2.5rem;
            color: var(--sky-blue);
            margin-bottom: 15px;
        }

        .info-title {
            font-size: 1.3rem;
            margin-bottom: 15px;
            color: var(--dark-green);
        }

        /* CTA Section */
        .cta-section {
            background: var(--gradient-bg);
            padding: 60px 20px;
            text-align: center;
            border-radius: 10px;
            margin-bottom: 60px;
            box-shadow: var(--shadow);
        }

        .cta-section h2 {
            color: white;
            font-size: 2rem;
            margin-bottom: 20px;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
        }

        .cta-section p {
            color: white;
            font-size: 1.1rem;
            margin-bottom: 30px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        /* Footer */
        footer {
            background-color: #333;
            color: white;
            padding: 50px 20px 20px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            color: var(--sky-blue);
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 10px;
        }

        .footer-column ul li a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-column ul li a:hover {
            color: white;
        }

        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-icons a {
            color: white;
            font-size: 1.5rem;
            transition: transform 0.3s ease;
        }

        .social-icons a:hover {
            transform: translateY(-5px);
        }

        .copyright {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid #555;
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
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
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
            
            .charts-section {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 1.8rem;
            }
            
            .cta-button {
                padding: 10px 20px;
                font-size: 1rem;
            }
            
            .mistake-title, .info-title {
                font-size: 1.2rem;
            }
        }
    </style>
</head>
<body>
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

        <!-- Charts Section -->
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

        <!-- Infographics -->
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

        <!-- CTA Section -->
        <div class="cta-section">
            <h2>Ready to Optimize Your GATE Metallurgy Preparation?</h2>
            <p>Download our comprehensive study plan tailored specifically for Metallurgy students, including topic-wise weightage, monthly targets, and revision schedules.</p>
            <a href="#" class="cta-button">Download Your GATE Metallurgy Study Plan</a>
        </div>
    </div>

    <!-- Footer -->
    <footer>
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
                    labels: ['Incomplete Syllabus', 'Weak Fundamentals', 'Poor Time Management', 'Lack of Practice', 'Exam Anxiety'],
                    datasets: [{
                        data: [35, 25, 20, 15, 5],
                        backgroundColor: [
                            '#e74c3c',
                            '#3498db',
                            '#2ecc71',
                            '#f39c12',
                            '#9b59b6'
                        ],
                        borderWidth: 1
                    }]
                },
                options: {
                    responsive: true,
                    plugins: {
                        legend: {
                            position: 'right',
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
                            '#3498db',
                            '#2ecc71',
                            '#e74c3c',
                            '#f39c12',
                            '#9b59b6'
                        ],
                        borderWidth: 1
                    }]
                },
                options: {
                    responsive: true,
                    plugins: {
                        legend: {
                            position: 'right',
                        }
                    }
                }
            });
        });
    </script>
</body>
</html>
