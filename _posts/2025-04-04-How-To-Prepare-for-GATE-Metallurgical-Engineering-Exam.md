<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Comprehensive guide to prepare for GATE Metallurgical Engineering exam with expert tips, study plan, and resources from TestUrSelf">
    <title>GATE Metallurgical Engineering Exam Preparation Guide | TestUrSelf</title>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&family=Poppins:wght@600;700&display=swap" rel="stylesheet">
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #6a1b9a;
            --secondary: #9c27b0;
            --accent: #ff9800;
            --light: #f3e5f5;
            --dark: #4a148c;
            --text: #333;
            --bg: #f9f9f9;
            --card-bg: #fff;
            --success: #4caf50;
            --warning: #ff9800;
            --info: #2196f3;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            line-height: 1.6;
            color: var(--text);
            background-color: var(--bg);
            margin: 0;
            padding: 0;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary), var(--dark));
            color: white;
            padding: 60px 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        header::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
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
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Poppins', sans-serif;
            margin-top: 0;
        }
        
        h1 {
            font-size: 2.8rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        h2 {
            font-size: 2.2rem;
            color: var(--primary);
            margin-bottom: 30px;
            position: relative;
            padding-bottom: 15px;
        }
        
        h2::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(to right, var(--primary), var(--accent));
            border-radius: 2px;
        }
        
        h3 {
            font-size: 1.8rem;
            color: var(--dark);
            margin-bottom: 20px;
        }
        
        /* Navigation */
        nav {
            background-color: var(--card-bg);
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 20px;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 10px;
        }
        
        .nav-links {
            display: flex;
            gap: 25px;
        }
        
        .nav-links a {
            color: var(--text);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--text);
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1581094794329-c8112a89af12?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80') no-repeat center center/cover;
            color: white;
            padding: 100px 0;
            text-align: center;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            border-radius: 50px;
            font-weight: 500;
            text-decoration: none;
            transition: all 0.3s;
            margin: 0 10px 10px 0;
        }
        
        .btn-primary {
            background-color: var(--primary);
            color: white;
        }
        
        .btn-primary:hover {
            background-color: var(--dark);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }
        
        .btn-secondary {
            background-color: var(--accent);
            color: white;
        }
        
        .btn-secondary:hover {
            background-color: #ffab00;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }
        
        /* Section Styles */
        .section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        /* Card Styles */
        .card {
            background-color: var(--card-bg);
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            padding: 30px;
            transition: transform 0.3s, box-shadow 0.3s;
            height: 100%;
        }
        
        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }
        
        .card-icon {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        /* Preparation Guide */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .timeline::before {
            content: '';
            position: absolute;
            top: 0;
            left: 50px;
            height: 100%;
            width: 3px;
            background: linear-gradient(to bottom, var(--primary), var(--accent));
        }
        
        .timeline-item {
            display: flex;
            margin-bottom: 40px;
            position: relative;
        }
        
        .timeline-number {
            width: 50px;
            height: 50px;
            background-color: var(--primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            margin-right: 30px;
            flex-shrink: 0;
            z-index: 1;
        }
        
        .timeline-content {
            background-color: var(--card-bg);
            border-radius: 10px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            flex-grow: 1;
        }
        
        /* Testimonials */
        .testimonial-slider {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
        }
        
        .testimonial {
            background-color: var(--card-bg);
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            text-align: center;
            margin: 0 15px;
        }
        
        .testimonial-img {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            object-fit: cover;
            margin: 0 auto 20px;
            border: 4px solid var(--light);
        }
        
        .testimonial-rating {
            color: var(--accent);
            margin: 15px 0;
        }
        
        /* Stats */
        .stats {
            background: linear-gradient(135deg, var(--primary), var(--dark));
            color: white;
            padding: 60px 0;
            text-align: center;
        }
        
        .stat-item {
            margin-bottom: 30px;
        }
        
        .stat-number {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 10px;
            color: var(--accent);
        }
        
        /* FAQ */
        .faq-item {
            margin-bottom: 20px;
            border: 1px solid #eee;
            border-radius: 8px;
            overflow: hidden;
        }
        
        .faq-question {
            width: 100%;
            padding: 20px;
            background-color: var(--card-bg);
            border: none;
            text-align: left;
            font-weight: 500;
            font-size: 1.1rem;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .faq-answer {
            padding: 0 20px;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s, padding 0.3s;
            background-color: #f9f9f9;
        }
        
        .faq-answer.active {
            padding: 20px;
            max-height: 500px;
        }
        
        /* CTA */
        .cta {
            background: linear-gradient(135deg, var(--primary), var(--dark));
            color: white;
            text-align: center;
            padding: 80px 0;
        }
        
        /* Footer */
        footer {
            background-color: #222;
            color: #ddd;
            padding: 60px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            color: white;
            margin-bottom: 20px;
            font-size: 1.3rem;
        }
        
        .footer-column ul {
            list-style: none;
            padding: 0;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #bbb;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: white;
        }
        
        .footer-social {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .footer-social a {
            color: white;
            font-size: 1.2rem;
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #444;
        }
        
        /* Responsive Styles */
        @media (max-width: 992px) {
            h1 {
                font-size: 2.4rem;
            }
            
            h2 {
                font-size: 2rem;
            }
            
            .nav-links {
                display: none;
            }
            
            .mobile-menu-btn {
                display: block;
            }
        }
        
        @media (max-width: 768px) {
            .section {
                padding: 60px 0;
            }
            
            .hero {
                padding: 80px 0;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            .btn {
                display: block;
                width: 100%;
                margin-bottom: 15px;
            }
            
            .timeline::before {
                left: 25px;
            }
            
            .timeline-number {
                width: 40px;
                height: 40px;
                margin-right: 20px;
            }
        }
        
        @media (max-width: 576px) {
            .hero {
                padding: 60px 0;
            }
            
            h1 {
                font-size: 1.8rem;
            }
            
            .section {
                padding: 40px 0;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="container nav-container">
            <a href="#" class="logo">
                <i class="fas fa-graduation-cap"></i> TestUrSelf
            </a>
            
            <div class="nav-links">
                <a href="#introduction">Introduction</a>
                <a href="#preparation">Preparation Guide</a>
                <a href="#testimonials">Testimonials</a>
                <a href="#why-us">Why Us</a>
                <a href="#resources">Resources</a>
            </div>
            
            <button class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </nav>
    
    <!-- Hero Section -->
    <header class="hero">
        <div class="container hero-content">
            <h1>Master GATE Metallurgical Engineering</h1>
            <p>The Complete Guide to Crack GATE MT with Top Ranks</p>
            <div>
                <a href="#join-now" class="btn btn-primary">Join TestUrSelf Now</a>
                <a href="#download" class="btn btn-secondary">Download Free Material</a>
            </div>
        </div>
    </header>
    
    <!-- Introduction Section -->
    <section id="introduction" class="section">
        <div class="container">
            <div class="section-title">
                <h2>What is GATE Metallurgical Engineering?</h2>
                <p>GATE (Graduate Aptitude Test in Engineering) for Metallurgical Engineering (MT) is the gateway to prestigious PSU jobs, M.Tech admissions in IITs/NITs, and research opportunities.</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div class="card">
                    <div class="card-icon">
                        <i class="fas fa-bullseye"></i>
                    </div>
                    <h3>Exam Structure</h3>
                    <p>65 questions worth 100 marks covering General Aptitude, Engineering Mathematics, and Metallurgy subjects.</p>
                </div>
                
                <div class="card">
                    <div class="card-icon">
                        <i class="fas fa-trophy"></i>
                    </div>
                    <h3>Importance</h3>
                    <p>Qualifying GATE MT opens doors to PSUs like SAIL, NALCO, HCL, and top institutes like IITs, IISc, NITs.</p>
                </div>
                
                <div class="card">
                    <div class="card-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>Competition</h3>
                    <p>With 10,000+ aspirants each year, strategic preparation is key to securing top ranks.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Preparation Guide Section -->
    <section id="preparation" class="section bg-gray-100">
        <div class="container">
            <div class="section-title">
                <h2>Step-by-Step Preparation Guide</h2>
                <p>Follow this comprehensive 6-month plan to systematically prepare for GATE Metallurgy</p>
            </div>
            
            <div class="timeline">
                <!-- Step 1 -->
                <div class="timeline-item">
                    <div class="timeline-number">1</div>
                    <div class="timeline-content">
                        <h3>Understand Syllabus & Exam Pattern</h3>
                        <p>Thoroughly analyze the GATE MT syllabus (Physical Metallurgy, Mechanical Metallurgy, Manufacturing Processes, etc.) and exam pattern (marks distribution, negative marking).</p>
                    </div>
                </div>
                
                <!-- Step 2 -->
                <div class="timeline-item">
                    <div class="timeline-number">2</div>
                    <div class="timeline-content">
                        <h3>Collect Study Materials</h3>
                        <p>Gather standard textbooks, TestUrSelf study materials, previous year papers, and online resources. Focus on quality over quantity.</p>
                    </div>
                </div>
                
                <!-- Step 3 -->
                <div class="timeline-item">
                    <div class="timeline-number">3</div>
                    <div class="timeline-content">
                        <h3>Create Study Schedule</h3>
                        <p>Divide syllabus into weekly targets. Allocate time for concepts, problem-solving, revision, and mock tests. Include buffer time.</p>
                    </div>
                </div>
                
                <!-- Step 4 -->
                <div class="timeline-item">
                    <div class="timeline-number">4</div>
                    <div class="timeline-content">
                        <h3>Concept Building & Notes</h3>
                        <p>Study topics thoroughly, make concise notes, create formula sheets, and understand fundamental concepts rather than rote learning.</p>
                    </div>
                </div>
                
                <!-- Step 5 -->
                <div class="timeline-item">
                    <div class="timeline-number">5</div>
                    <div class="timeline-content">
                        <h3>Practice & Mock Tests</h3>
                        <p>Solve previous year papers (at least 10 years) and take regular mock tests under timed conditions. Analyze performance to identify weak areas.</p>
                    </div>
                </div>
                
                <!-- Step 6 -->
                <div class="timeline-item">
                    <div class="timeline-number">6</div>
                    <div class="timeline-content">
                        <h3>Revision & Final Preparation</h3>
                        <p>Last 1-2 months should focus on revision, formula sheets, important topics, and full-length mock tests to build stamina.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Key Topics Section -->
    <section class="section">
        <div class="container">
            <div class="section-title">
                <h2>Key Topics in GATE Metallurgy</h2>
                <p>Focus on these high-weightage topics to maximize your score</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <div class="card">
                    <h3>Physical Metallurgy</h3>
                    <ul>
                        <li><i class="fas fa-check text-success mr-2"></i> Crystal structures & defects</li>
                        <li><i class="fas fa-check text-success mr-2"></i> Phase diagrams & transformations</li>
                        <li><i class="fas fa-check text-success mr-2"></i> Heat treatment processes</li>
                    </ul>
                </div>
                
                <div class="card">
                    <h3>Mechanical Metallurgy</h3>
                    <ul>
                        <li><i class="fas fa-check text-success mr-2"></i> Dislocations & strengthening</li>
                        <li><i class="fas fa-check text-success mr-2"></i> Fracture & fatigue</li>
                        <li><i class="fas fa-check text-success mr-2"></i> Mechanical testing</li>
                    </ul>
                </div>
                
                <div class="card">
                    <h3>Manufacturing Processes</h3>
                    <ul>
                        <li><i class="fas fa-check text-success mr-2"></i> Casting & welding</li>
                        <li><i class="fas fa-check text-success mr-2"></i> Metal forming</li>
                        <li><i class="fas fa-check text-success mr-2"></i> Powder metallurgy</li>
                    </ul>
                </div>
                
                <div class="card">
                    <h3>Thermodynamics & Kinetics</h3>
                    <ul>
                        <li><i class="fas fa-check text-success mr-2"></i> Laws of thermodynamics</li>
                        <li><i class="fas fa-check text-success mr-2"></i> Phase equilibria</li>
                        <li><i class="fas fa-check text-success mr-2"></i> Diffusion & reactions</li>
                    </ul>
                </div>
                
                <div class="card">
                    <h3>Extractive Metallurgy</h3>
                    <ul>
                        <li><i class="fas fa-check text-success mr-2"></i> Ore processing</li>
                        <li><i class="fas fa-check text-success mr-2"></i> Pyrometallurgy</li>
                        <li><i class="fas fa-check text-success mr-2"></i> Hydrometallurgy</li>
                    </ul>
                </div>
                
                <div class="card">
                    <h3>Engineering Mathematics</h3>
                    <ul>
                        <li><i class="fas fa-check text-success mr-2"></i> Linear algebra</li>
                        <li><i class="fas fa-check text-success mr-2"></i> Calculus & differential equations</li>
                        <li><i class="fas fa-check text-success mr-2"></i> Probability & statistics</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Video Resources Section -->
    <section class="section bg-gray-100">
        <div class="container">
            <div class="section-title">
                <h2>Video Learning Resources</h2>
                <p>Watch these expert-curated videos to master complex metallurgy concepts</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div class="card">
                    <div class="aspect-w-16 aspect-h-9 mb-4">
                        <iframe class="w-full h-full rounded-lg" src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                    </div>
                    <h3>Phase Diagrams Explained</h3>
                    <p>Learn to interpret binary and ternary phase diagrams with practical examples.</p>
                </div>
                
                <div class="card">
                    <div class="aspect-w-16 aspect-h-9 mb-4">
                        <iframe class="w-full h-full rounded-lg" src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                    </div>
                    <h3>Heat Treatment Processes</h3>
                    <p>Master annealing, normalizing, quenching, and tempering techniques.</p>
                </div>
                
                <div class="card">
                    <div class="aspect-w-16 aspect-h-9 mb-4">
                        <iframe class="w-full h-full rounded-lg" src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                    </div>
                    <h3>GATE Strategy & Tips</h3>
                    <p>Expert tips from IIT professors on how to crack GATE Metallurgy.</p>
                </div>
            </div>
            
            <div class="text-center mt-8">
                <a href="#" class="btn btn-primary">View All Video Lectures</a>
            </div>
        </div>
    </section>
    
    <!-- Testimonials Section -->
    <section id="testimonials" class="section">
        <div class="container">
            <div class="section-title">
                <h2>Success Stories</h2>
                <p>Hear from our GATE Metallurgy toppers who achieved their dreams with TestUrSelf</p>
            </div>
            
            <div class="testimonial-slider">
                <div class="testimonial">
                    <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Rahul Sharma" class="testimonial-img">
                    <h3>Rahul Sharma</h3>
                    <p class="text-primary font-medium">GATE MT AIR 1 (2022)</p>
                    <div class="testimonial-rating">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <p class="italic">"TestUrSelf's test series was instrumental in my GATE preparation. The questions were so similar to actual GATE that I felt completely prepared. The mentorship from IIT professors helped me clear my concepts thoroughly."</p>
                </div>
                
                <div class="testimonial">
                    <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Priya Patel" class="testimonial-img">
                    <h3>Priya Patel</h3>
                    <p class="text-primary font-medium">GATE MT AIR 3 (2021)</p>
                    <div class="testimonial-rating">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <p class="italic">"The study material from TestUrSelf covered everything in the syllabus with perfect depth. The regular doubt-solving sessions ensured I never got stuck on any topic. I recommend TestUrSelf to every GATE Metallurgy aspirant."</p>
                </div>
                
                <div class="testimonial">
                    <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="Amit Kumar" class="testimonial-img">
                    <h3>Amit Kumar</h3>
                    <p class="text-primary font-medium">GATE MT AIR 7 (2023)</p>
                    <div class="testimonial-rating">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <p class="italic">"What sets TestUrSelf apart is their focus on Metallurgy specifically. The faculty understands exactly what's important for GATE. Their test series had several questions that appeared verbatim in my GATE paper!"</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Why TestUrSelf Section -->
    <section id="why-us" class="section bg-gray-100">
        <div class="container">
            <div class="section-title">
                <h2>Why TestUrSelf for GATE Metallurgy?</h2>
                <p>The proven platform that has consistently produced GATE MT toppers year after year</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <div class="card">
                    <div class="card-icon">
                        <i class="fas fa-book"></i>
                    </div>
                    <h3>Best Content for GATE Metallurgy</h3>
                    <p>Comprehensive study material designed by IIT & IISc experts specifically for GATE MT syllabus.</p>
                </div>
                
                <div class="card">
                    <div class="card-icon">
                        <i class="fas fa-trophy"></i>
                    </div>
                    <h3>Producing Top Rankers Since 2018</h3>
                    <p>Consistent track record of producing AIR 1, AIR 2, and multiple top 100 ranks every year.</p>
                </div>
                
                <div class="card">
                    <div class="card-icon">
                        <i class="fas fa-medal"></i>
                    </div>
                    <h3>AIR-1 Every Year Since 2019</h3>
                    <p>Unmatched success with AIR 1 in GATE Metallurgy for 4 consecutive years.</p>
                </div>
                
                <div class="card">
                    <div class="card-icon">
                        <i class="fas fa-clipboard-check"></i>
                    </div>
                    <h3>Direct Questions in GATE Exam</h3>
                    <p>Our test series questions match actual GATE questions - sometimes even verbatim!</p>
                </div>
                
                <div class="card">
                    <div class="card-icon">
                        <i class="fas fa-chalkboard-teacher"></i>
                    </div>
                    <h3>Expert Mentorship</h3>
                    <p>Live doubt-solving sessions with IIT/IISc mentors who know exactly what GATE demands.</p>
                </div>
                
                <div class="card">
                    <div class="card-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>Performance Analytics</h3>
                    <p>Detailed test analytics to track your progress and identify improvement areas.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Stats Section -->
    <section class="stats">
        <div class="container">
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
                <div class="stat-item">
                    <div class="stat-number" data-count="1500">0</div>
                    <p>Students Enrolled</p>
                </div>
                
                <div class="stat-item">
                    <div class="stat-number" data-count="32">0</div>
                    <p>Top 100 Rankers</p>
                </div>
                
                <div class="stat-item">
                    <div class="stat-number" data-count="4">0</div>
                    <p>AIR 1 Produced</p>
                </div>
                
                <div class="stat-item">
                    <div class="stat-number" data-count="98">0</div>
                    <p>% Satisfaction Rate</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- CTA Section -->
    <section id="join-now" class="cta">
        <div class="container">
            <h2>Ready to Start Your GATE Metallurgy Journey?</h2>
            <p class="mb-8">Join India's most trusted GATE Metallurgy preparation platform and get closer to your dream rank</p>
            
            <div>
                <a href="#" class="btn btn-primary"><i class="fas fa-rocket mr-2"></i> Enroll Now</a>
                <a href="#" class="btn btn-secondary"><i class="fas fa-phone-alt mr-2"></i> Talk to an Expert</a>
            </div>
        </div>
    </section>
    
    <!-- Free Resources Section -->
    <section id="download" class="section">
        <div class="container">
            <div class="section-title">
                <h2>Free GATE Metallurgy Resources</h2>
                <p>Download these free resources to kickstart your preparation</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div class="card">
                    <div class="bg-purple-100 text-purple-600 text-6xl p-8 mb-4 rounded-lg flex justify-center">
                        <i class="fas fa-file-pdf"></i>
                    </div>
                    <h3>Complete Syllabus PDF</h3>
                    <p>Detailed GATE MT syllabus with weightage analysis for each topic.</p>
                    <a href="#" class="text-primary font-medium inline-flex items-center mt-4">
                        Download Now <i class="fas fa-arrow-down ml-2"></i>
                    </a>
                </div>
                
                <div class="card">
                    <div class="bg-orange-100 text-orange-600 text-6xl p-8 mb-4 rounded-lg flex justify-center">
                        <i class="fas fa-list-ol"></i>
                    </div>
                    <h3>Previous Year Papers</h3>
                    <p>10 years of GATE MT solved papers with detailed solutions.</p>
                    <a href="#" class="text-primary font-medium inline-flex items-center mt-4">
                        Download Now <i class="fas fa-arrow-down ml-2"></i>
                    </a>
                </div>
                
                <div class="card">
                    <div class="bg-blue-100 text-blue-600 text-6xl p-8 mb-4 rounded-lg flex justify-center">
                        <i class="fas fa-clipboard-list"></i>
                    </div>
                    <h3>Formula Handbook</h3>
                    <p>All essential formulas for GATE MT in one compact document.</p>
                    <a href="#" class="text-primary font-medium inline-flex items-center mt-4">
                        Download Now <i class="fas fa-arrow-down ml-2"></i>
                    </a>
                </div>
            </div>
        </div>
    </section>
    
    <!-- FAQ Section -->
    <section class="section bg-gray-100">
        <div class="container">
            <div class="section-title">
                <h2>Frequently Asked Questions</h2>
                <p>Get answers to common questions about GATE Metallurgy preparation</p>
            </div>
            
            <div class="max-w-3xl mx-auto">
                <div class="faq-item">
                    <button class="faq-question">
                        <span>When should I start preparing for GATE Metallurgy?</span>
                        <i class="fas fa-chevron-down"></i>
                    </button>
                    <div class="faq-answer">
                        <p>Ideally, you should start your preparation 6-8 months before the exam. However, if you're targeting top ranks (AIR < 100), we recommend a 10-12 month preparation period with at least 4-5 hours of daily study.</p>
                    </div>
                </div>
                
                <div class="faq-item">
                    <button class="faq-question">
                        <span>What's more important - concepts or practice?</span>
                        <i class="fas fa-chevron-down"></i>
                    </button>
                    <div class="faq-answer">
                        <p>Both are equally important. First build strong conceptual understanding (especially for Physical Metallurgy, Thermodynamics), then practice extensively (especially for Manufacturing, Mechanical Metallurgy). Our program balances both with concept lectures followed by practice sessions.</p>
                    </div>
                </div>
                
                <div class="faq-item">
                    <button class="faq-question">
                        <span>How many mock tests should I take?</span>
                        <i class="fas fa-chevron-down"></i>
                    </button>
                    <div class="faq-answer">
                        <p>Minimum 15-20 full-length mock tests in the last 3 months before GATE. Our test series includes 25+ mocks with progressive difficulty levels. Analyze each test thoroughly to identify weak areas.</p>
                    </div>
                </div>
                
                <div class="faq-item">
                    <button class="faq-question">
                        <span>Is coaching necessary for GATE Metallurgy?</span>
                        <i class="fas fa-chevron-down"></i>
                    </button>
                    <div class="faq-answer">
                        <p>While self-study is possible, structured guidance significantly improves your chances of top ranks. Our data shows 92% of top 100 rankers had some form of coaching. TestUrSelf's program provides the right direction, saves time, and ensures you cover all important topics.</p>
                    </div>
                </div>
                
                <div class="faq-item">
                    <button class="faq-question">
                        <span>How does TestUrSelf compare to other platforms?</span>
                        <i class="fas fa-chevron-down"></i>
                    </button>
                    <div class="faq-answer">
                        <p>TestUrSelf is the only platform exclusively focused on GATE Metallurgy with IIT/IISc faculty. Our content depth, test quality, and mentorship are unmatched. The results speak for themselves - we've produced AIR 1 every year since 2019 and have 3x more top 100 rankers than any other platform.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Final CTA -->
    <section class="cta">
        <div class="container">
            <h2>Start Your GATE Metallurgy Preparation Today!</h2>
            <p class="mb-8">Join thousands of successful Metallurgy aspirants who trusted TestUrSelf for their GATE journey</p>
            
            <div>
                <a href="#" class="btn btn-primary"><i class="fas fa-user-graduate mr-2"></i> Enroll Now</a>
                <a href="#" class="btn btn-secondary"><i class="fas fa-calendar-alt mr-2"></i> Free Demo Class</a>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>TestUrSelf</h3>
                    <p>India's leading GATE Metallurgy preparation platform with proven results since 2018.</p>
                    <div class="footer-social">
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
                        <li><i class="fas fa-map-marker-alt mr-2"></i> 123 Education Street, Bangalore, Karnataka 560001</li>
                        <li><i class="fas fa-phone-alt mr-2"></i> +91 9876543210</li>
                        <li><i class="fas fa-envelope mr-2"></i> info@testurself.com</li>
                    </ul>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2023 TestUrSelf. All Rights Reserved.</p>
            </div>
        </div>
    </footer>
    
    <script>
        // Mobile menu toggle
        const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
        const navLinks = document.querySelector('.nav-links');
        
        mobileMenuBtn.addEventListener('click', () => {
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
        });
        
        // FAQ accordion
        const faqQuestions = document.querySelectorAll('.faq-question');
        
        faqQuestions.forEach(question => {
            question.addEventListener('click', () => {
                const answer = question.nextElementSibling;
                const icon = question.querySelector('i');
                
                // Toggle current answer
                answer.classList.toggle('active');
                icon.classList.toggle('rotate-180');
                
                // Close other answers
                faqQuestions.forEach(q => {
                    if (q !== question) {
                        q.nextElementSibling.classList.remove('active');
                        q.querySelector('i').classList.remove('rotate-180');
                    }
                });
            });
        });
        
        // Counter animation
        const statNumbers = document.querySelectorAll('.stat-number');
        const speed = 200;
        
        statNumbers.forEach(stat => {
            const target = +stat.getAttribute('data-count');
            const count = +stat.innerText;
            const increment = target / speed;
            
            if (count < target) {
                stat.innerText = Math.ceil(count + increment);
                setTimeout(updateCounter, 1);
            } else {
                stat.innerText = target;
            }
            
            function updateCounter() {
                const current = +stat.innerText;
                if (current < target) {
                    stat.innerText = Math.ceil(current + increment);
                    setTimeout(updateCounter, 1);
                } else {
                    stat.innerText = target;
                }
            }
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
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
