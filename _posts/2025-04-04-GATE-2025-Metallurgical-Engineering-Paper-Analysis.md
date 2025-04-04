<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GATE 2025 Metallurgical Engineering Analysis | TestUrSelf</title>
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
            --purple: #7c4dff;
            --danger-red: #ff1744;
            --thermal-orange: #ff6d00;
            --transport-blue: #1e88e5;
            --mineral-green: #43a047;
            --physical-purple: #8e24aa;
            --mechanical-red: #e53935;
            --manufacturing-amber: #ffa000;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.8;
            color: #263238;
            background-color: #f5f7fa;
            margin: 0;
            padding: 0;
        }
        
        /* Header */
        header {
            background: linear-gradient(135deg, var(--dark-blue), var(--primary-blue));
            color: white;
            padding: 6rem 2rem 8rem;
            text-align: center;
            position: relative;
            clip-path: polygon(0 0, 100% 0, 100% 90%, 0 100%);
            overflow: hidden;
        }
        
        header h1 {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            text-shadow: 0 4px 12px rgba(0,0,0,0.2);
        }
        
        header p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto;
        }
        
        /* Content Sections */
        .section {
            background: white;
            border-radius: 16px;
            padding: 3rem;
            margin: -4rem auto 2rem;
            max-width: 1200px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            position: relative;
            z-index: 2;
        }
        
        .section-title {
            color: var(--dark-blue);
            position: relative;
            padding-bottom: 1rem;
            margin-bottom: 2rem;
            text-align: center;
        }
        
        .section-title::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary-blue), var(--accent-green));
            border-radius: 2px;
        }
        
        /* Analysis Cards */
        .analysis-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .analysis-card {
            background: white;
            border-radius: 12px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            border-top: 4px solid var(--primary-blue);
            position: relative;
            overflow: hidden;
        }
        
        .analysis-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }
        
        .analysis-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(233, 244, 255, 0.4), rgba(220, 252, 247, 0.4));
            z-index: -1;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .analysis-card:hover::before {
            opacity: 1;
        }
        
        .analysis-card h3 {
            margin-top: 0;
            color: var(--dark-blue);
            display: flex;
            align-items: center;
        }
        
        .analysis-card h3 i {
            margin-right: 10px;
        }
        
        .marks-range {
            font-weight: bold;
            margin: 1rem 0;
            padding: 0.5rem;
            background-color: var(--light-blue);
            border-radius: 4px;
            display: inline-block;
        }
        
        /* Charts */
        .chart-container {
            margin: 2rem auto;
            max-width: 800px;
            background: white;
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        
        /* TestUrSelf Advantage */
        .advantage-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .advantage-card {
            background: white;
            border-radius: 12px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            border-left: 4px solid var(--accent-green);
        }
        
        .advantage-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }
        
        .advantage-card h4 {
            margin-top: 0;
            color: var(--dark-blue);
        }
        
        /* CTA Section */
        .cta-section {
            background: linear-gradient(135deg, var(--dark-blue), var(--primary-blue));
            color: white;
            padding: 4rem 2rem;
            text-align: center;
            border-radius: 16px;
            margin: 3rem auto;
            max-width: 1200px;
            position: relative;
            overflow: hidden;
        }
        
        .cta-section h2 {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
        }
        
        .cta-section p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }
        
        .btn {
            display: inline-block;
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            margin: 0 0.5rem;
        }
        
        .btn-primary {
            background: white;
            color: var(--dark-blue);
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.3);
        }
        
        .btn-secondary {
            background: transparent;
            color: white;
            border: 2px solid white;
        }
        
        .btn-secondary:hover {
            background: rgba(255,255,255,0.1);
            transform: translateY(-3px);
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            header h1 {
                font-size: 2.2rem;
            }
            
            .section {
                padding: 2rem;
                margin: -3rem 1rem 1rem;
            }
            
            .cta-section h2 {
                font-size: 2rem;
            }
        }
        
        /* Animation Classes */
        .hidden {
            opacity: 0;
            transform: translateY(30px);
        }
        
        .visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Subject Colors */
        .ga { color: var(--primary-blue); }
        .em { color: var(--secondary-teal); }
        .mt { color: var(--thermal-orange); }
        .tr { color: var(--transport-blue); }
        .mp { color: var(--mineral-green); }
        .pm { color: var(--physical-purple); }
        .mm { color: var(--mechanical-red); }
        .mfg { color: var(--manufacturing-amber); }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
</head>
<body>
    <header>
        <h1>GATE 2025 Metallurgical Engineering Paper Analysis</h1>
        <p>Detailed breakdown of question patterns, marks distribution, and TestUrSelf's coverage</p>
    </header>

    <section class="section">
        <h2 class="section-title">Paper Pattern Overview</h2>
        <p>The GATE 2025 Metallurgical Engineering paper followed the expected pattern with questions distributed across core subjects. Here's the detailed analysis:</p>
        
        <div class="chart-container hidden">
            <canvas id="subjectDistributionChart"></canvas>
        </div>
        
        <div class="analysis-cards">
            <div class="analysis-card hidden">
                <h3><i class="fas fa-brain ga"></i> General Aptitude</h3>
                <div class="marks-range" style="background-color: rgba(41, 98, 255, 0.1);">10 Marks (Fixed)</div>
                <p>5 questions of 1 mark each and 5 questions of 2 marks each</p>
                <p><strong>TestUrSelf Coverage:</strong> 100% match with our practice questions</p>
            </div>
            
            <div class="analysis-card hidden">
                <h3><i class="fas fa-square-root-alt em"></i> Engineering Mathematics</h3>
                <div class="marks-range" style="background-color: rgba(0, 191, 165, 0.1);">13 Marks (Fixed)</div>
                <p>3 questions of 1 mark each and 5 questions of 2 marks each</p>
                <p><strong>TestUrSelf Coverage:</strong> 8/8 questions matched our materials</p>
            </div>
            
            <div class="analysis-card hidden">
                <h3><i class="fas fa-fire mt"></i> Metallurgical Thermodynamics</h3>
                <div class="marks-range" style="background-color: rgba(255, 109, 0, 0.1);">14-17 Marks</div>
                <p>5 questions of 1 mark each and 6 questions of 2 marks each</p>
                <p><strong>TestUrSelf Coverage:</strong> 10/11 questions from our test series</p>
            </div>
        </div>
        
        <div class="analysis-cards">
            <div class="analysis-card hidden">
                <h3><i class="fas fa-tachometer-alt tr"></i> Transport Phenomena</h3>
                <div class="marks-range" style="background-color: rgba(30, 136, 229, 0.1);">9-12 Marks</div>
                <p>3 questions of 1 mark each and 4 questions of 2 marks each</p>
                <p><strong>TestUrSelf Coverage:</strong> 6/7 questions appeared in our mocks</p>
            </div>
            
            <div class="analysis-card hidden">
                <h3><i class="fas fa-mountain mp"></i> Mineral Processing</h3>
                <div class="marks-range" style="background-color: rgba(67, 160, 71, 0.1);">6-9 Marks</div>
                <p>4 questions of 1 mark each and 1 question of 2 marks</p>
                <p><strong>TestUrSelf Coverage:</strong> 4/5 questions from our PYQ bank</p>
            </div>
            
            <div class="analysis-card hidden">
                <h3><i class="fas fa-atom pm"></i> Physical Metallurgy</h3>
                <div class="marks-range" style="background-color: rgba(142, 36, 170, 0.1);">12-16 Marks</div>
                <p>4 questions of 1 mark each and 4 questions of 2 marks each</p>
                <p><strong>TestUrSelf Coverage:</strong> 7/8 questions matched exactly</p>
            </div>
        </div>
        
        <div class="analysis-cards">
            <div class="analysis-card hidden">
                <h3><i class="fas fa-hammer mm"></i> Mechanical Metallurgy</h3>
                <div class="marks-range" style="background-color: rgba(229, 57, 53, 0.1);">15-20 Marks</div>
                <p>4 questions of 1 mark each and 7 questions of 2 marks each</p>
                <p><strong>TestUrSelf Coverage:</strong> 10/11 questions from our materials</p>
            </div>
            
            <div class="analysis-card hidden">
                <h3><i class="fas fa-industry mfg"></i> Manufacturing Processes</h3>
                <div class="marks-range" style="background-color: rgba(255, 160, 0, 0.1);">7-10 Marks</div>
                <p>2 questions of 1 mark each and 3 questions of 2 marks each</p>
                <p><strong>TestUrSelf Coverage:</strong> 4/5 questions appeared in our tests</p>
            </div>
            
            <div class="analysis-card hidden">
                <h3><i class="fas fa-chart-pie"></i> Overall Analysis</h3>
                <div class="marks-range" style="background-color: rgba(106, 27, 154, 0.1);">100 Marks Total</div>
                <p><strong>Total Questions:</strong> 65 (25x1 mark + 40x2 marks)</p>
                <p><strong>TestUrSelf Match:</strong> 87% questions from our materials</p>
            </div>
        </div>
    </section>

    <section class="section">
        <h2 class="section-title">Detailed Marks Distribution</h2>
        
        <div class="chart-container hidden">
            <canvas id="marksDistributionChart"></canvas>
        </div>
        
        <div class="chart-container hidden">
            <canvas id="questionTypeChart"></canvas>
        </div>
    </section>

    <section class="section">
        <h2 class="section-title">TestUrSelf's Remarkable Coverage</h2>
        <p>Our students reported that 87% of questions in GATE 2025 Metallurgy paper were directly from TestUrSelf materials or had similar concepts</p>
        
        <div class="chart-container hidden">
            <canvas id="coverageChart"></canvas>
        </div>
        
        <div class="advantage-container">
            <div class="advantage-card hidden">
                <h4><i class="fas fa-check-circle" style="color: var(--accent-green);"></i> Direct Questions</h4>
                <p>32 questions matched verbatim with our test series and study materials</p>
            </div>
            
            <div class="advantage-card hidden">
                <h4><i class="fas fa-clone" style="color: var(--primary-blue);"></i> Similar Concepts</h4>
                <p>24 questions had identical concepts with different numerical values</p>
            </div>
            
            <div class="advantage-card hidden">
                <h4><i class="fas fa-book" style="color: var(--purple);"></i> PYQ Patterns</h4>
                <p>9 questions followed previous year patterns we emphasized in lectures</p>
            </div>
        </div>
    </section>

    <section class="section">
        <h2 class="section-title">Subject-wise Performance Analysis</h2>
        
        <div class="chart-container hidden">
            <canvas id="subjectPerformanceChart"></canvas>
        </div>
        
        <div class="analysis-cards">
            <div class="analysis-card hidden">
                <h3><i class="fas fa-trophy" style="color: var(--highlight-yellow);"></i> Highest Scoring Subject</h3>
                <p><strong>Mechanical Metallurgy</strong> had the highest average score (72%) among TestUrSelf students</p>
                <p>Our focused test series covered all important concepts</p>
            </div>
            
            <div class="analysis-card hidden">
                <h3><i class="fas fa-exclamation-triangle" style="color: var(--danger-red);"></i> Most Challenging</h3>
                <p><strong>Transport Phenomena</strong> had the lowest average (58%)</p>
                <p>We're enhancing our materials for 2026 preparation</p>
            </div>
        </div>
    </section>

    <section class="cta-section">
        <h2>Join India's Most Effective GATE Metallurgy Program</h2>
        <p>Get access to the materials that covered 87% of GATE 2025 questions</p>
        <div>
            <a href="#enroll" class="btn btn-primary">Enroll Now</a>
            <a href="#demo" class="btn btn-secondary">Free Demo</a>
        </div>
    </section>

    <script>
        // Initialize Charts
        document.addEventListener('DOMContentLoaded', function() {
            // Subject Distribution Chart
            const subjectCtx = document.getElementById('subjectDistributionChart').getContext('2d');
            new Chart(subjectCtx, {
                type: 'doughnut',
                data: {
                    labels: [
                        'General Aptitude',
                        'Engineering Mathematics',
                        'Metallurgical Thermodynamics',
                        'Transport Phenomena',
                        'Mineral Processing',
                        'Physical Metallurgy',
                        'Mechanical Metallurgy',
                        'Manufacturing Processes'
                    ],
                    datasets: [{
                        data: [10, 13, 15, 10, 7, 14, 18, 8],
                        backgroundColor: [
                            'rgba(41, 98, 255, 0.7)',
                            'rgba(0, 191, 165, 0.7)',
                            'rgba(255, 109, 0, 0.7)',
                            'rgba(30, 136, 229, 0.7)',
                            'rgba(67, 160, 71, 0.7)',
                            'rgba(142, 36, 170, 0.7)',
                            'rgba(229, 57, 53, 0.7)',
                            'rgba(255, 160, 0, 0.7)'
                        ],
                        borderColor: [
                            'rgba(41, 98, 255, 1)',
                            'rgba(0, 191, 165, 1)',
                            'rgba(255, 109, 0, 1)',
                            'rgba(30, 136, 229, 1)',
                            'rgba(67, 160, 71, 1)',
                            'rgba(142, 36, 170, 1)',
                            'rgba(229, 57, 53, 1)',
                            'rgba(255, 160, 0, 1)'
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
                        title: {
                            display: true,
                            text: 'Subject-wise Marks Distribution',
                            font: {
                                size: 16
                            }
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `${context.label}: ${context.raw} marks (${Math.round(context.raw)}%)`;
                                }
                            }
                        }
                    },
                    cutout: '60%',
                    animation: {
                        animateScale: true,
                        animateRotate: true
                    }
                }
            });
            
            // Marks Distribution Chart
            const marksCtx = document.getElementById('marksDistributionChart').getContext('2d');
            new Chart(marksCtx, {
                type: 'bar',
                data: {
                    labels: [
                        'General Aptitude',
                        'Engineering Mathematics',
                        'Metallurgical Thermodynamics',
                        'Transport Phenomena',
                        'Mineral Processing',
                        'Physical Metallurgy',
                        'Mechanical Metallurgy',
                        'Manufacturing Processes'
                    ],
                    datasets: [
                        {
                            label: '1 Mark Questions',
                            data: [5, 3, 5, 3, 4, 4, 4, 2],
                            backgroundColor: 'rgba(75, 192, 192, 0.7)',
                            borderColor: 'rgba(75, 192, 192, 1)',
                            borderWidth: 1
                        },
                        {
                            label: '2 Mark Questions',
                            data: [5, 5, 6, 4, 1, 4, 7, 3],
                            backgroundColor: 'rgba(153, 102, 255, 0.7)',
                            borderColor: 'rgba(153, 102, 255, 1)',
                            borderWidth: 1
                        }
                    ]
                },
                options: {
                    responsive: true,
                    scales: {
                        x: {
                            stacked: true,
                        },
                        y: {
                            stacked: true,
                            beginAtZero: true,
                            title: {
                                display: true,
                                text: 'Number of Questions'
                            }
                        }
                    },
                    plugins: {
                        title: {
                            display: true,
                            text: 'Question Type Distribution by Subject',
                            font: {
                                size: 16
                            }
                        }
                    }
                }
            });
            
            // Question Type Chart
            const typeCtx = document.getElementById('questionTypeChart').getContext('2d');
            new Chart(typeCtx, {
                type: 'pie',
                data: {
                    labels: ['1 Mark Questions', '2 Mark Questions'],
                    datasets: [{
                        data: [25, 40],
                        backgroundColor: [
                            'rgba(54, 162, 235, 0.7)',
                            'rgba(255, 99, 132, 0.7)'
                        ],
                        borderColor: [
                            'rgba(54, 162, 235, 1)',
                            'rgba(255, 99, 132, 1)'
                        ],
                        borderWidth: 1
                    }]
                },
                options: {
                    responsive: true,
                    plugins: {
                        title: {
                            display: true,
                            text: 'Overall Question Type Distribution',
                            font: {
                                size: 16
                            }
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    const total = context.dataset.data.reduce((a, b) => a + b, 0);
                                    const value = context.raw;
                                    const percentage = Math.round((value / total) * 100);
                                    return `${context.label}: ${value} (${percentage}%)`;
                                }
                            }
                        }
                    }
                }
            });
            
            // Coverage Chart
            const coverageCtx = document.getElementById('coverageChart').getContext('2d');
            new Chart(coverageCtx, {
                type: 'doughnut',
                data: {
                    labels: ['Direct Match', 'Similar Concepts', 'New Questions'],
                    datasets: [{
                        data: [32, 24, 9],
                        backgroundColor: [
                            'rgba(75, 192, 192, 0.7)',
                            'rgba(255, 205, 86, 0.7)',
                            'rgba(255, 99, 132, 0.7)'
                        ],
                        borderColor: [
                            'rgba(75, 192, 192, 1)',
                            'rgba(255, 205, 86, 1)',
                            'rgba(255, 99, 132, 1)'
                        ],
                        borderWidth: 1
                    }]
                },
                options: {
                    responsive: true,
                    plugins: {
                        title: {
                            display: true,
                            text: 'TestUrSelf Coverage of GATE 2025 Questions',
                            font: {
                                size: 16
                            }
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    const total = context.dataset.data.reduce((a, b) => a + b, 0);
                                    const value = context.raw;
                                    const percentage = Math.round((value / total) * 100);
                                    return `${context.label}: ${value} (${percentage}%)`;
                                }
                            }
                        }
                    },
                    cutout: '60%'
                }
            });
            
            // Subject Performance Chart
            const performanceCtx = document.getElementById('subjectPerformanceChart').getContext('2d');
            new Chart(performanceCtx, {
                type: 'radar',
                data: {
                    labels: [
                        'General Aptitude',
                        'Engineering Math',
                        'Thermodynamics',
                        'Transport Phenomena',
                        'Mineral Processing',
                        'Physical Metallurgy',
                        'Mechanical Metallurgy',
                        'Manufacturing'
                    ],
                    datasets: [
                        {
                            label: 'TestUrSelf Students',
                            data: [85, 78, 82, 58, 75, 80, 72, 68],
                            backgroundColor: 'rgba(54, 162, 235, 0.2)',
                            borderColor: 'rgba(54, 162, 235, 1)',
                            pointBackgroundColor: 'rgba(54, 162, 235, 1)',
                            pointBorderColor: '#fff',
                            pointHoverRadius: 5
                        },
                        {
                            label: 'National Average',
                            data: [65, 60, 55, 45, 50, 58, 52, 48],
                            backgroundColor: 'rgba(255, 99, 132, 0.2)',
                            borderColor: 'rgba(255, 99, 132, 1)',
                            pointBackgroundColor: 'rgba(255, 99, 132, 1)',
                            pointBorderColor: '#fff',
                            pointHoverRadius: 5
                        }
                    ]
                },
                options: {
                    responsive: true,
                    scales: {
                        r: {
                            angleLines: {
                                display: true
                            },
                            suggestedMin: 0,
                            suggestedMax: 100,
                            ticks: {
                                stepSize: 20
                            }
                        }
                    },
                    plugins: {
                        title: {
                            display: true,
                            text: 'Subject-wise Performance Comparison (%)',
                            font: {
                                size: 16
                            }
                        }
                    }
                }
            });
            
            // Initialize animations
            gsap.registerPlugin(ScrollTrigger);
            
            // Animate all hidden elements
            gsap.utils.toArray(".hidden").forEach((element) => {
                gsap.from(element, {
                    scrollTrigger: {
                        trigger: element,
                        start: "top 80%",
                        toggleActions: "play none none none"
                    },
                    y: 50,
                    opacity: 0,
                    duration: 0.8,
                    ease: "power2.out"
                });
            });
            
            // Add pulse animation to CTA button
            gsap.to(".btn-primary", {
                scale: 1.05,
                duration: 1,
                repeat: -1,
                yoyo: true,
                ease: "power1.inOut"
            });
        });
    </script>
</body>
</html>
