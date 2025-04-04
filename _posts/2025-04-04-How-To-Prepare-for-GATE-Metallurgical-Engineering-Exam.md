<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Comprehensive guide to prepare for GATE Metallurgical Engineering exam with expert tips, study plan, and resources from TestUrSelf - the leading GATE Metallurgy coaching platform">
    <title>GATE Metallurgical Engineering Exam Preparation Guide | TestUrSelf</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    
    <!-- GSAP for animations -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.11.4/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.11.4/ScrollTrigger.min.js"></script>
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --primary: #3b82f6;
            --secondary: #1e3a8a;
            --accent: #f59e0b;
            --text: #1f2937;
            --bg: #f9fafb;
        }
        
        .dark {
            --primary: #60a5fa;
            --secondary: #93c5fd;
            --accent: #fbbf24;
            --text: #f3f4f6;
            --bg: #111827;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg);
            color: var(--text);
            transition: all 0.3s ease;
        }
        
        .parallax {
            background-attachment: fixed;
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;
        }
        
        .card-hover {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .card-hover:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .progress-tracker {
            position: relative;
        }
        
        .progress-tracker::before {
            content: '';
            position: absolute;
            top: 0;
            left: 16px;
            height: 100%;
            width: 2px;
            background-color: var(--primary);
            z-index: 0;
        }
        
        .counter {
            font-variant-numeric: tabular-nums;
        }
        
        /* Animation classes */
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }
        
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Floating elements */
        .floating {
            animation: floating 6s ease-in-out infinite;
        }
        
        @keyframes floating {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }
        
        /* Testimonial slider */
        .testimonial-slider {
            overflow: hidden;
            position: relative;
        }
        
        .slider-track {
            display: flex;
            transition: transform 0.5s ease;
        }
        
        .testimonial-slide {
            min-width: 100%;
            padding: 0 1rem;
        }
        
        /* Hero section overlay */
        .hero-overlay {
            background: rgba(0, 0, 0, 0.6);
        }
        
        /* Section spacing */
        .section {
            padding: 5rem 0;
        }
        
        @media (max-width: 768px) {
            .section {
                padding: 3rem 0;
            }
        }
    </style>
</head>
<body class="antialiased">
    <!-- Dark mode toggle -->
    <button id="darkModeToggle" class="fixed right-6 bottom-6 z-50 w-12 h-12 rounded-full bg-blue-500 shadow-lg flex items-center justify-center text-white text-xl">
        <i class="fas fa-moon"></i>
    </button>
    
    <!-- Navigation -->
    <nav class="bg-white dark:bg-gray-900 shadow-md sticky top-0 z-40 transition-all duration-300">
        <div class="container mx-auto px-4 sm:px-6 py-3 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-blue-600 dark:text-blue-400 flex items-center">
                <i class="fas fa-graduation-cap mr-2"></i> TestUrSelf
            </a>
            
            <div class="hidden md:flex space-x-6 lg:space-x-8">
                <a href="#introduction" class="text-gray-700 dark:text-gray-300 hover:text-blue-600 dark:hover:text-blue-400 transition">Introduction</a>
                <a href="#preparation" class="text-gray-700 dark:text-gray-300 hover:text-blue-600 dark:hover:text-blue-400 transition">Preparation Guide</a>
                <a href="#testimonials" class="text-gray-700 dark:text-gray-300 hover:text-blue-600 dark:hover:text-blue-400 transition">Testimonials</a>
                <a href="#why-us" class="text-gray-700 dark:text-gray-300 hover:text-blue-600 dark:hover:text-blue-400 transition">Why Us</a>
                <a href="#resources" class="text-gray-700 dark:text-gray-300 hover:text-blue-600 dark:hover:text-blue-400 transition">Resources</a>
            </div>
            
            <button class="md:hidden text-gray-700 dark:text-gray-300 focus:outline-none" id="mobileMenuButton">
                <i class="fas fa-bars text-2xl"></i>
            </button>
        </div>
        
        <!-- Mobile menu -->
        <div class="md:hidden hidden bg-white dark:bg-gray-800 px-4 py-2" id="mobileMenu">
            <a href="#introduction" class="block py-2 text-gray-700 dark:text-gray-300 hover:text-blue-600 dark:hover:text-blue-400">Introduction</a>
            <a href="#preparation" class="block py-2 text-gray-700 dark:text-gray-300 hover:text-blue-600 dark:hover:text-blue-400">Preparation Guide</a>
            <a href="#testimonials" class="block py-2 text-gray-700 dark:text-gray-300 hover:text-blue-600 dark:hover:text-blue-400">Testimonials</a>
            <a href="#why-us" class="block py-2 text-gray-700 dark:text-gray-300 hover:text-blue-600 dark:hover:text-blue-400">Why Us</a>
            <a href="#resources" class="block py-2 text-gray-700 dark:text-gray-300 hover:text-blue-600 dark:hover:text-blue-400">Resources</a>
        </div>
    </nav>
    
    <!-- Hero Section with Parallax -->
    <section class="parallax bg-[url('https://images.unsplash.com/photo-1581094794329-c8112a89af12?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80')] py-20 md:py-32 relative">
        <div class="absolute inset-0 hero-overlay"></div>
        <div class="container mx-auto px-4 sm:px-6 relative z-10 text-center">
            <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-6 fade-in">Master GATE Metallurgical Engineering</h1>
            <p class="text-xl md:text-2xl text-gray-200 mb-8 max-w-3xl mx-auto fade-in">The Complete Guide to Crack GATE MT with Top Ranks</p>
            
            <div class="flex flex-col sm:flex-row justify-center gap-4 fade-in">
                <a href="#join-now" class="bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-6 md:px-8 rounded-lg transition transform hover:scale-105">
                    Join TestUrSelf Now
                </a>
                <a href="#download" class="bg-orange-500 hover:bg-orange-600 text-white font-semibold py-3 px-6 md:px-8 rounded-lg transition transform hover:scale-105">
                    Download Free Material
                </a>
            </div>
            
            <div class="mt-16 flex justify-center fade-in">
                <a href="#introduction" class="animate-bounce text-white text-2xl">
                    <i class="fas fa-chevron-down"></i>
                </a>
            </div>
        </div>
    </section>
    
    <!-- Introduction Section -->
    <section id="introduction" class="section bg-gray-50 dark:bg-gray-800">
        <div class="container mx-auto px-4 sm:px-6">
            <div class="text-center mb-12 md:mb-16 fade-in">
                <h2 class="text-3xl md:text-4xl font-bold text-gray-800 dark:text-white mb-4">What is GATE Metallurgical Engineering?</h2>
                <div class="w-20 h-1 bg-blue-600 mx-auto mb-6"></div>
                <p class="text-gray-600 dark:text-gray-300 max-w-3xl mx-auto text-lg">
                    GATE (Graduate Aptitude Test in Engineering) for Metallurgical Engineering (MT) is the gateway to prestigious PSU jobs, M.Tech admissions in IITs/NITs, and research opportunities.
                </p>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8">
                <div class="bg-white dark:bg-gray-700 rounded-xl shadow-lg p-6 card-hover fade-in">
                    <div class="text-blue-600 dark:text-blue-400 text-4xl mb-4">
                        <i class="fas fa-bullseye"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white">Exam Structure</h3>
                    <p class="text-gray-600 dark:text-gray-300">
                        65 questions worth 100 marks covering General Aptitude, Engineering Mathematics, and Metallurgy subjects.
                    </p>
                </div>
                
                <div class="bg-white dark:bg-gray-700 rounded-xl shadow-lg p-6 card-hover fade-in">
                    <div class="text-blue-600 dark:text-blue-400 text-4xl mb-4">
                        <i class="fas fa-trophy"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white">Importance</h3>
                    <p class="text-gray-600 dark:text-gray-300">
                        Qualifying GATE MT opens doors to PSUs like SAIL, NALCO, HCL, and top institutes like IITs, IISc, NITs.
                    </p>
                </div>
                
                <div class="bg-white dark:bg-gray-700 rounded-xl shadow-lg p-6 card-hover fade-in">
                    <div class="text-blue-600 dark:text-blue-400 text-4xl mb-4">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white">Competition</h3>
                    <p class="text-gray-600 dark:text-gray-300">
                        With 10,000+ aspirants each year, strategic preparation is key to securing top ranks.
                    </p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Preparation Guide Section -->
    <section id="preparation" class="section bg-white dark:bg-gray-900">
        <div class="container mx-auto px-4 sm:px-6">
            <div class="text-center mb-12 md:mb-16 fade-in">
                <h2 class="text-3xl md:text-4xl font-bold text-gray-800 dark:text-white mb-4">Step-by-Step Preparation Guide</h2>
                <div class="w-20 h-1 bg-blue-600 mx-auto mb-6"></div>
                <p class="text-gray-600 dark:text-gray-300 max-w-3xl mx-auto text-lg">
                    Follow this comprehensive 6-month plan to systematically prepare for GATE Metallurgy
                </p>
            </div>
            
            <div class="max-w-4xl mx-auto">
                <div class="progress-tracker space-y-8 md:space-y-10">
                    <!-- Step 1 -->
                    <div class="flex gap-4 md:gap-6 fade-in">
                        <div class="flex-shrink-0 w-10 h-10 rounded-full bg-blue-600 text-white flex items-center justify-center z-10">
                            <span>1</span>
                        </div>
                        <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-lg shadow-md flex-1 card-hover">
                            <h3 class="text-xl font-semibold mb-2 text-gray-800 dark:text-white">Understand Syllabus & Exam Pattern</h3>
                            <p class="text-gray-600 dark:text-gray-300">
                                Thoroughly analyze the GATE MT syllabus (Physical Metallurgy, Mechanical Metallurgy, Manufacturing Processes, etc.) and exam pattern (marks distribution, negative marking).
                            </p>
                        </div>
                    </div>
                    
                    <!-- Step 2 -->
                    <div class="flex gap-4 md:gap-6 fade-in">
                        <div class="flex-shrink-0 w-10 h-10 rounded-full bg-blue-600 text-white flex items-center justify-center z-10">
                            <span>2</span>
                        </div>
                        <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-lg shadow-md flex-1 card-hover">
                            <h3 class="text-xl font-semibold mb-2 text-gray-800 dark:text-white">Collect Study Materials</h3>
                            <p class="text-gray-600 dark:text-gray-300">
                                Gather standard textbooks, TestUrSelf study materials, previous year papers, and online resources. Focus on quality over quantity.
                            </p>
                        </div>
                    </div>
                    
                    <!-- Step 3 -->
                    <div class="flex gap-4 md:gap-6 fade-in">
                        <div class="flex-shrink-0 w-10 h-10 rounded-full bg-blue-600 text-white flex items-center justify-center z-10">
                            <span>3</span>
                        </div>
                        <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-lg shadow-md flex-1 card-hover">
                            <h3 class="text-xl font-semibold mb-2 text-gray-800 dark:text-white">Create Study Schedule</h3>
                            <p class="text-gray-600 dark:text-gray-300">
                                Divide syllabus into weekly targets. Allocate time for concepts, problem-solving, revision, and mock tests. Include buffer time.
                            </p>
                        </div>
                    </div>
                    
                    <!-- Step 4 -->
                    <div class="flex gap-4 md:gap-6 fade-in">
                        <div class="flex-shrink-0 w-10 h-10 rounded-full bg-blue-600 text-white flex items-center justify-center z-10">
                            <span>4</span>
                        </div>
                        <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-lg shadow-md flex-1 card-hover">
                            <h3 class="text-xl font-semibold mb-2 text-gray-800 dark:text-white">Concept Building & Notes</h3>
                            <p class="text-gray-600 dark:text-gray-300">
                                Study topics thoroughly, make concise notes, create formula sheets, and understand fundamental concepts rather than rote learning.
                            </p>
                        </div>
                    </div>
                    
                    <!-- Step 5 -->
                    <div class="flex gap-4 md:gap-6 fade-in">
                        <div class="flex-shrink-0 w-10 h-10 rounded-full bg-blue-600 text-white flex items-center justify-center z-10">
                            <span>5</span>
                        </div>
                        <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-lg shadow-md flex-1 card-hover">
                            <h3 class="text-xl font-semibold mb-2 text-gray-800 dark:text-white">Practice & Mock Tests</h3>
                            <p class="text-gray-600 dark:text-gray-300">
                                Solve previous year papers (at least 10 years) and take regular mock tests under timed conditions. Analyze performance to identify weak areas.
                            </p>
                        </div>
                    </div>
                    
                    <!-- Step 6 -->
                    <div class="flex gap-4 md:gap-6 fade-in">
                        <div class="flex-shrink-0 w-10 h-10 rounded-full bg-blue-600 text-white flex items-center justify-center z-10">
                            <span>6</span>
                        </div>
                        <div class="bg-gray-50 dark:bg-gray-800 p-6 rounded-lg shadow-md flex-1 card-hover">
                            <h3 class="text-xl font-semibold mb-2 text-gray-800 dark:text-white">Revision & Final Preparation</h3>
                            <p class="text-gray-600 dark:text-gray-300">
                                Last 1-2 months should focus on revision, formula sheets, important topics, and full-length mock tests to build stamina.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Key Topics Section with Floating Elements -->
    <section class="section bg-gray-50 dark:bg-gray-800 relative overflow-hidden">
        <!-- Floating elements -->
        <div class="absolute top-20 left-10 w-16 h-16 rounded-full bg-blue-200 opacity-20 floating hidden md:block"></div>
        <div class="absolute bottom-1/4 right-20 w-24 h-24 rounded-full bg-orange-200 opacity-20 floating hidden md:block" style="animation-delay: 1s;"></div>
        <div class="absolute top-1/3 right-1/4 w-20 h-20 rounded-full bg-purple-200 opacity-20 floating hidden md:block" style="animation-delay: 2s;"></div>
        
        <div class="container mx-auto px-4 sm:px-6 relative z-10">
            <div class="text-center mb-12 md:mb-16 fade-in">
                <h2 class="text-3xl md:text-4xl font-bold text-gray-800 dark:text-white mb-4">Key Topics in GATE Metallurgy</h2>
                <div class="w-20 h-1 bg-blue-600 mx-auto mb-6"></div>
                <p class="text-gray-600 dark:text-gray-300 max-w-3xl mx-auto text-lg">
                    Focus on these high-weightage topics to maximize your score
                </p>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
                <div class="bg-white dark:bg-gray-700 rounded-xl shadow-lg p-6 card-hover fade-in">
                    <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white flex items-center">
                        <span class="w-8 h-8 bg-blue-100 dark:bg-blue-900 text-blue-600 dark:text-blue-400 rounded-full flex items-center justify-center mr-3">1</span>
                        Physical Metallurgy
                    </h3>
                    <ul class="text-gray-600 dark:text-gray-300 space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Crystal structures & defects</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Phase diagrams & transformations</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Heat treatment processes</span>
                        </li>
                    </ul>
                </div>
                
                <div class="bg-white dark:bg-gray-700 rounded-xl shadow-lg p-6 card-hover fade-in">
                    <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white flex items-center">
                        <span class="w-8 h-8 bg-blue-100 dark:bg-blue-900 text-blue-600 dark:text-blue-400 rounded-full flex items-center justify-center mr-3">2</span>
                        Mechanical Metallurgy
                    </h3>
                    <ul class="text-gray-600 dark:text-gray-300 space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Dislocations & strengthening</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Fracture & fatigue</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Mechanical testing</span>
                        </li>
                    </ul>
                </div>
                
                <div class="bg-white dark:bg-gray-700 rounded-xl shadow-lg p-6 card-hover fade-in">
                    <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white flex items-center">
                        <span class="w-8 h-8 bg-blue-100 dark:bg-blue-900 text-blue-600 dark:text-blue-400 rounded-full flex items-center justify-center mr-3">3</span>
                        Manufacturing Processes
                    </h3>
                    <ul class="text-gray-600 dark:text-gray-300 space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Casting & welding</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Metal forming</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Powder metallurgy</span>
                        </li>
                    </ul>
                </div>
                
                <div class="bg-white dark:bg-gray-700 rounded-xl shadow-lg p-6 card-hover fade-in">
                    <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white flex items-center">
                        <span class="w-8 h-8 bg-blue-100 dark:bg-blue-900 text-blue-600 dark:text-blue-400 rounded-full flex items-center justify-center mr-3">4</span>
                        Thermodynamics & Kinetics
                    </h3>
                    <ul class="text-gray-600 dark:text-gray-300 space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Laws of thermodynamics</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Phase equilibria</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Diffusion & reactions</span>
                        </li>
                    </ul>
                </div>
                
                <div class="bg-white dark:bg-gray-700 rounded-xl shadow-lg p-6 card-hover fade-in">
                    <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white flex items-center">
                        <span class="w-8 h-8 bg-blue-100 dark:bg-blue-900 text-blue-600 dark:text-blue-400 rounded-full flex items-center justify-center mr-3">5</span>
                        Extractive Metallurgy
                    </h3>
                    <ul class="text-gray-600 dark:text-gray-300 space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Ore processing</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Pyrometallurgy</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Hydrometallurgy</span>
                        </li>
                    </ul>
                </div>
                
                <div class="bg-white dark:bg-gray-700 rounded-xl shadow-lg p-6 card-hover fade-in">
                    <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white flex items-center">
                        <span class="w-8 h-8 bg-blue-100 dark:bg-blue-900 text-blue-600 dark:text-blue-400 rounded-full flex items-center justify-center mr-3">6</span>
                        Engineering Mathematics
                    </h3>
                    <ul class="text-gray-600 dark:text-gray-300 space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Linear algebra</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Calculus & differential equations</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check text-green-500 mt-1 mr-2"></i>
                            <span>Probability & statistics</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Video Resources Section -->
    <section class="section bg-white dark:bg-gray-900">
        <div class="container mx-auto px-4 sm:px-6">
            <div class="text-center mb-12 md:mb-16 fade-in">
                <h2 class="text-3xl md:text-4xl font-bold text-gray-800 dark:text-white mb-4">Video Learning Resources</h2>
                <div class="w-20 h-1 bg-blue-600 mx-auto mb-6"></div>
                <p class="text-gray-600 dark:text-gray-300 max-w-3xl mx-auto text-lg">
                    Watch these expert-curated videos to master complex metallurgy concepts
                </p>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
                <div class="rounded-xl overflow-hidden shadow-lg fade-in card-hover">
                    <div class="relative pt-[56.25%] bg-gray-200 dark:bg-gray-700">
                        <iframe class="absolute top-0 left-0 w-full h-full" src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                    </div>
                    <div class="p-6 bg-white dark:bg-gray-800">
                        <h3 class="text-xl font-semibold mb-2 text-gray-800 dark:text-white">Phase Diagrams Explained</h3>
                        <p class="text-gray-600 dark:text-gray-300">Learn to interpret binary and ternary phase diagrams with practical examples.</p>
                    </div>
                </div>
                
                <div class="rounded-xl overflow-hidden shadow-lg fade-in card-hover">
                    <div class="relative pt-[56.25%] bg-gray-200 dark:bg-gray-700">
                        <iframe class="absolute top-0 left-0 w-full h-full" src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                    </div>
                    <div class="p-6 bg-white dark:bg-gray-800">
                        <h3 class="text-xl font-semibold mb-2 text-gray-800 dark:text-white">Heat Treatment Processes</h3>
                        <p class="text-gray-600 dark:text-gray-300">Master annealing, normalizing, quenching, and tempering techniques.</p>
                    </div>
                </div>
                
                <div class="rounded-xl overflow-hidden shadow-lg fade-in card-hover">
                    <div class="relative pt-[56.25%] bg-gray-200 dark:bg-gray-700">
                        <iframe class="absolute top-0 left-0 w-full h-full" src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                    </div>
                    <div class="p-6 bg-white dark:bg-gray-800">
                        <h3 class="text-xl font-semibold mb-2 text-gray-800 dark:text-white">GATE Strategy & Tips</h3>
                        <p class="text-gray-600 dark:text-gray-300">Expert tips from IIT professors on how to crack GATE Metallurgy.</p>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-12 fade-in">
                <a href="#" class="inline-block bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-8 rounded-lg transition transform hover:scale-105">
                    View All Video Lectures
                </a>
            </div>
        </div>
    </section>
    
    <!-- Testimonials Section with Slider -->
    <section id="testimonials" class="section bg-gray-50 dark:bg-gray-800">
        <div class="container mx-auto px-4 sm:px-6">
            <div class="text-center mb-12 md:mb-16 fade-in">
                <h2 class="text-3xl md:text-4xl font-bold text-gray-800 dark:text-white mb-4">Success Stories</h2>
                <div class="w-20 h-1 bg-blue-600 mx-auto mb-6"></div>
                <p class="text-gray-600 dark:text-gray-300 max-w-3xl mx-auto text-lg">
                    Hear from our GATE Metallurgy toppers who achieved their dreams with TestUrSelf
                </p>
            </div>
            
            <div class="max-w-4xl mx-auto relative fade-in">
                <!-- Testimonial Slider -->
                <div class="testimonial-slider">
                    <div class="slider-track" id="sliderTrack">
                        <!-- Testimonial 1 -->
                        <div class="testimonial-slide">
                            <div class="bg-white dark:bg-gray-700 p-6 md:p-8 rounded-xl shadow-lg">
                                <div class="flex flex-col md:flex-row items-center mb-6">
                                    <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Rahul Sharma" class="w-16 h-16 rounded-full object-cover mb-4 md:mb-0 md:mr-4 border-4 border-blue-100 dark:border-blue-900">
                                    <div class="text-center md:text-left">
                                        <h4 class="text-lg font-semibold text-gray-800 dark:text-white">Rahul Sharma</h4>
                                        <p class="text-blue-600 dark:text-blue-400">GATE MT AIR 1 (2022)</p>
                                    </div>
                                </div>
                                <p class="text-gray-600 dark:text-gray-300 italic">
                                    "TestUrSelf's test series was instrumental in my GATE preparation. The questions were so similar to actual GATE that I felt completely prepared. The mentorship from IIT professors helped me clear my concepts thoroughly."
                                </p>
                                <div class="mt-4 flex justify-center md:justify-start text-yellow-400">
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Testimonial 2 -->
                        <div class="testimonial-slide">
                            <div class="bg-white dark:bg-gray-700 p-6 md:p-8 rounded-xl shadow-lg">
                                <div class="flex flex-col md:flex-row items-center mb-6">
                                    <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Priya Patel" class="w-16 h-16 rounded-full object-cover mb-4 md:mb-0 md:mr-4 border-4 border-blue-100 dark:border-blue-900">
                                    <div class="text-center md:text-left">
                                        <h4 class="text-lg font-semibold text-gray-800 dark:text-white">Priya Patel</h4>
                                        <p class="text-blue-600 dark:text-blue-400">GATE MT AIR 3 (2021)</p>
                                    </div>
                                </div>
                                <p class="text-gray-600 dark:text-gray-300 italic">
                                    "The study material from TestUrSelf covered everything in the syllabus with perfect depth. The regular doubt-solving sessions ensured I never got stuck on any topic. I recommend TestUrSelf to every GATE Metallurgy aspirant."
                                </p>
                                <div class="mt-4 flex justify-center md:justify-start text-yellow-400">
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Testimonial 3 -->
                        <div class="testimonial-slide">
                            <div class="bg-white dark:bg-gray-700 p-6 md:p-8 rounded-xl shadow-lg">
                                <div class="flex flex-col md:flex-row items-center mb-6">
                                    <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="Amit Kumar" class="w-16 h-16 rounded-full object-cover mb-4 md:mb-0 md:mr-4 border-4 border-blue-100 dark:border-blue-900">
                                    <div class="text-center md:text-left">
                                        <h4 class="text-lg font-semibold text-gray-800 dark:text-white">Amit Kumar</h4>
                                        <p class="text-blue-600 dark:text-blue-400">GATE MT AIR 7 (2023)</p>
                                    </div>
                                </div>
                                <p class="text-gray-600 dark:text-gray-300 italic">
                                    "What sets TestUrSelf apart is their focus on Metallurgy specifically. The faculty understands exactly what's important for GATE. Their test series had several questions that appeared verbatim in my GATE paper!"
                                </p>
                                <div class="mt-4 flex justify-center md:justify-start text-yellow-400">
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                    <i class="fas fa-star"></i>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Slider Controls -->
                <button class="absolute left-0 top-1/2 transform -translate-y-1/2 -translate-x-4 bg-white dark:bg-gray-700 w-10 h-10 rounded-full shadow-md flex items-center justify-center text-blue-600 dark:text-blue-400 hover:bg-blue-100 dark:hover:bg-gray-600 transition hidden md:flex" id="prevBtn">
                    <i class="fas fa-chevron-left"></i>
                </button>
                <button class="absolute right-0 top-1/2 transform -translate-y-1/2 translate-x-4 bg-white dark:bg-gray-700 w-10 h-10 rounded-full shadow-md flex items-center justify-center text-blue-600 dark:text-blue-400 hover:bg-blue-100 dark:hover:bg-gray-600 transition hidden md:flex" id="nextBtn">
                    <i class="fas fa-chevron-right"></i>
                </button>
                
                <!-- Slider Indicators -->
                <div class="flex justify-center mt-6 space-x-2" id="sliderIndicators">
                    <button class="w-3 h-3 rounded-full bg-blue-600 dark:bg-blue-400 slider-indicator"></button>
                    <button class="w-3 h-3 rounded-full bg-gray-300 dark:bg-gray-600 slider-indicator"></button>
                    <button class="w-3 h-3 rounded-full bg-gray-300 dark:bg-gray-600 slider-indicator"></button>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Why TestUrSelf Section -->
    <section id="why-us" class="section bg-white dark:bg-gray-900">
        <div class="container mx-auto px-4 sm:px-6">
            <div class="text-center mb-12 md:mb-16 fade-in">
                <h2 class="text-3xl md:text-4xl font-bold text-gray-800 dark:text-white mb-4">Why TestUrSelf for GATE Metallurgy?</h2>
                <div class="w-20 h-1 bg-blue-600 mx-auto mb-6"></div>
                <p class="text-gray-600 dark:text-gray-300 max-w-3xl mx-auto text-lg">
                    The proven platform that has consistently produced GATE MT toppers year after year
                </p>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
                <div class="bg-blue-50 dark:bg-gray-800 rounded-xl shadow-lg p-6 md:p-8 card-hover fade-in">
                    <div class="text-blue-600 dark:text-blue-400 text-4xl mb-4">
                        <i class="fas fa-book"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white">Best Content for GATE Metallurgy</h3>
                    <p class="text-gray-600 dark:text-gray-300">
                        Comprehensive study material designed by IIT & IISc experts specifically for GATE MT syllabus.
                    </p>
                </div>
                
                <div class="bg-blue-50 dark:bg-gray-800 rounded-xl shadow-lg p-6 md:p-8 card-hover fade-in">
                    <div class="text-blue-600 dark:text-blue-400 text-4xl mb-4">
                        <i class="fas fa-trophy"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white">Producing Top Rankers Since 2018</h3>
                    <p class="text-gray-600 dark:text-gray-300">
                        Consistent track record of producing AIR 1, AIR 2, and multiple top 100 ranks every year.
                    </p>
                </div>
                
                <div class="bg-blue-50 dark:bg-gray-800 rounded-xl shadow-lg p-6 md:p-8 card-hover fade-in">
                    <div class="text-blue-600 dark:text-blue-400 text-4xl mb-4">
                        <i class="fas fa-medal"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white">AIR-1 Every Year Since 2019</h3>
                    <p class="text-gray-600 dark:text-gray-300">
                        Unmatched success with AIR 1 in GATE Metallurgy for 4 consecutive years.
                    </p>
                </div>
                
                <div class="bg-blue-50 dark:bg-gray-800 rounded-xl shadow-lg p-6 md:p-8 card-hover fade-in">
                    <div class="text-blue-600 dark:text-blue-400 text-4xl mb-4">
                        <i class="fas fa-clipboard-check"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white">Direct Questions in GATE Exam</h3>
                    <p class="text-gray-600 dark:text-gray-300">
                        Our test series questions match actual GATE questions - sometimes even verbatim!
                    </p>
                </div>
                
                <div class="bg-blue-50 dark:bg-gray-800 rounded-xl shadow-lg p-6 md:p-8 card-hover fade-in">
                    <div class="text-blue-600 dark:text-blue-400 text-4xl mb-4">
                        <i class="fas fa-chalkboard-teacher"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white">Expert Mentorship</h3>
                    <p class="text-gray-600 dark:text-gray-300">
                        Live doubt-solving sessions with IIT/IISc mentors who know exactly what GATE demands.
                    </p>
                </div>
                
                <div class="bg-blue-50 dark:bg-gray-800 rounded-xl shadow-lg p-6 md:p-8 card-hover fade-in">
                    <div class="text-blue-600 dark:text-blue-400 text-4xl mb-4">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white">Performance Analytics</h3>
                    <p class="text-gray-600 dark:text-gray-300">
                        Detailed test analytics to track your progress and identify improvement areas.
                    </p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Stats Section -->
    <section class="py-16 md:py-20 bg-blue-600 text-white">
        <div class="container mx-auto px-4 sm:px-6">
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6 md:gap-8 text-center">
                <div class="fade-in">
                    <div class="text-3xl md:text-4xl lg:text-5xl font-bold mb-2 counter" data-target="1500">0</div>
                    <div class="text-lg md:text-xl">Students Enrolled</div>
                </div>
                
                <div class="fade-in">
                    <div class="text-3xl md:text-4xl lg:text-5xl font-bold mb-2 counter" data-target="32">0</div>
                    <div class="text-lg md:text-xl">Top 100 Rankers</div>
                </div>
                
                <div class="fade-in">
                    <div class="text-3xl md:text-4xl lg:text-5xl font-bold mb-2 counter" data-target="4">0</div>
                    <div class="text-lg md:text-xl">AIR 1 Produced</div>
                </div>
                
                <div class="fade-in">
                    <div class="text-3xl md:text-4xl lg:text-5xl font-bold mb-2 counter" data-target="98">0</div>
                    <div class="text-lg md:text-xl">% Satisfaction Rate</div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- CTA Section -->
    <section id="join-now" class="py-16 md:py-20 bg-gray-900 text-white">
        <div class="container mx-auto px-4 sm:px-6 text-center">
            <h2 class="text-3xl md:text-4xl font-bold mb-6 fade-in">Ready to Start Your GATE Metallurgy Journey?</h2>
            <p class="text-lg md:text-xl text-gray-300 max-w-3xl mx-auto mb-8 fade-in">
                Join India's most trusted GATE Metallurgy preparation platform and get closer to your dream rank
            </p>
            
            <div class="flex flex-col sm:flex-row justify-center gap-4 fade-in">
                <a href="#" class="bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-6 md:px-8 rounded-lg transition transform hover:scale-105 text-lg">
                    <i class="fas fa-rocket mr-2"></i> Enroll Now
                </a>
                <a href="#" class="bg-white hover:bg-gray-100 text-gray-800 font-semibold py-3 px-6 md:px-8 rounded-lg transition transform hover:scale-105 text-lg">
                    <i class="fas fa-phone-alt mr-2"></i> Talk to an Expert
                </a>
            </div>
        </div>
    </section>
    
    <!-- Free Resources Section -->
    <section id="download" class="section bg-gray-50 dark:bg-gray-800">
        <div class="container mx-auto px-4 sm:px-6">
            <div class="text-center mb-12 md:mb-16 fade-in">
                <h2 class="text-3xl md:text-4xl font-bold text-gray-800 dark:text-white mb-4">Free GATE Metallurgy Resources</h2>
                <div class="w-20 h-1 bg-blue-600 mx-auto mb-6"></div>
                <p class="text-gray-600 dark:text-gray-300 max-w-3xl mx-auto text-lg">
                    Download these free resources to kickstart your preparation
                </p>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6 max-w-5xl mx-auto">
                <div class="bg-white dark:bg-gray-700 rounded-xl shadow-lg overflow-hidden card-hover fade-in">
                    <div class="h-48 bg-blue-100 dark:bg-blue-900 flex items-center justify-center text-blue-600 dark:text-blue-400 text-6xl">
                        <i class="fas fa-file-pdf"></i>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white">Complete Syllabus PDF</h3>
                        <p class="text-gray-600 dark:text-gray-300 mb-4">Detailed GATE MT syllabus with weightage analysis for each topic.</p>
                        <a href="#" class="text-blue-600 dark:text-blue-400 font-semibold inline-flex items-center">
                            Download Now <i class="fas fa-arrow-down ml-2"></i>
                        </a>
                    </div>
                </div>
                
                <div class="bg-white dark:bg-gray-700 rounded-xl shadow-lg overflow-hidden card-hover fade-in">
                    <div class="h-48 bg-orange-100 dark:bg-orange-900 flex items-center justify-center text-orange-600 dark:text-orange-400 text-6xl">
                        <i class="fas fa-list-ol"></i>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white">Previous Year Papers</h3>
                        <p class="text-gray-600 dark:text-gray-300 mb-4">10 years of GATE MT solved papers with detailed solutions.</p>
                        <a href="#" class="text-blue-600 dark:text-blue-400 font-semibold inline-flex items-center">
                            Download Now <i class="fas fa-arrow-down ml-2"></i>
                        </a>
                    </div>
                </div>
                
                <div class="bg-white dark:bg-gray-700 rounded-xl shadow-lg overflow-hidden card-hover fade-in">
                    <div class="h-48 bg-purple-100 dark:bg-purple-900 flex items-center justify-center text-purple-600 dark:text-purple-400 text-6xl">
                        <i class="fas fa-clipboard-list"></i>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-3 text-gray-800 dark:text-white">Formula Handbook</h3>
                        <p class="text-gray-600 dark:text-gray-300 mb-4">All essential formulas for GATE MT in one compact document.</p>
                        <a href="#" class="text-blue-600 dark:text-blue-400 font-semibold inline-flex items-center">
                            Download Now <i class="fas fa-arrow-down ml-2"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- FAQ Section -->
    <section class="section bg-white dark:bg-gray-900">
        <div class="container mx-auto px-4 sm:px-6">
            <div class="text-center mb-12 md:mb-16 fade-in">
                <h2 class="text-3xl md:text-4xl font-bold text-gray-800 dark:text-white mb-4">Frequently Asked Questions</h2>
                <div class="w-20 h-1 bg-blue-600 mx-auto mb-6"></div>
                <p class="text-gray-600 dark:text-gray-300 max-w-3xl mx-auto text-lg">
                    Get answers to common questions about GATE Metallurgy preparation
                </p>
            </div>
            
            <div class="max-w-3xl mx-auto space-y-4">
                <div class="border border-gray-200 dark:border-gray-700 rounded-lg overflow-hidden fade-in">
                    <button class="faq-question w-full flex justify-between items-center p-4 md:p-6 text-left bg-gray-50 dark:bg-gray-800 hover:bg-gray-100 dark:hover:bg-gray-700 transition">
                        <span class="text-lg font-medium text-gray-800 dark:text-white">When should I start preparing for GATE Metallurgy?</span>
                        <i class="fas fa-chevron-down text-blue-600 dark:text-blue-400 transition-transform"></i>
                    </button>
                    <div class="faq-answer hidden p-4 md:p-6 bg-white dark:bg-gray-700">
                        <p class="text-gray-600 dark:text-gray-300">
                            Ideally, you should start your preparation 6-8 months before the exam. However, if you're targeting top ranks (AIR < 100), we recommend a 10-12 month preparation period with at least 4-5 hours of daily study.
                        </p>
                    </div>
                </div>
                
                <div class="border border-gray-200 dark:border-gray-700 rounded-lg overflow-hidden fade-in">
                    <button class="faq-question w-full flex justify-between items-center p-4 md:p-6 text-left bg-gray-50 dark:bg-gray-800 hover:bg-gray-100 dark:hover:bg-gray-700 transition">
                        <span class="text-lg font-medium text-gray-800 dark:text-white">What's more important - concepts or practice?</span>
                        <i class="fas fa-chevron-down text-blue-600 dark:text-blue-400 transition-transform"></i>
                    </button>
                    <div class="faq-answer hidden p-4 md:p-6 bg-white dark:bg-gray-700">
                        <p class="text-gray-600 dark:text-gray-300">
                            Both are equally important. First build strong conceptual understanding (especially for Physical Metallurgy, Thermodynamics), then practice extensively (especially for Manufacturing, Mechanical Metallurgy). Our program balances both with concept lectures followed by practice sessions.
                        </p>
                    </div>
                </div>
                
                <div class="border border-gray-200 dark:border-gray-700 rounded-lg overflow-hidden fade-in">
                    <button class="faq-question w-full flex justify-between items-center p-4 md:p-6 text-left bg-gray-50 dark:bg-gray-800 hover:bg-gray-100 dark:hover:bg-gray-700 transition">
                        <span class="text-lg font-medium text-gray-800 dark:text-white">How many mock tests should I take?</span>
                        <i class="fas fa-chevron-down text-blue-600 dark:text-blue-400 transition-transform"></i>
                    </button>
                    <div class="faq-answer hidden p-4 md:p-6 bg-white dark:bg-gray-700">
                        <p class="text-gray-600 dark:text-gray-300">
                            Minimum 15-20 full-length mock tests in the last 3 months before GATE. Our test series includes 25+ mocks with progressive difficulty levels. Analyze each test thoroughly to identify weak areas.
                        </p>
                    </div>
                </div>
                
                <div class="border border-gray-200 dark:border-gray-700 rounded-lg overflow-hidden fade-in">
                    <button class="faq-question w-full flex justify-between items-center p-4 md:p-6 text-left bg-gray-50 dark:bg-gray-800 hover:bg-gray-100 dark:hover:bg-gray-700 transition">
                        <span class="text-lg font-medium text-gray-800 dark:text-white">Is coaching necessary for GATE Metallurgy?</span>
                        <i class="fas fa-chevron-down text-blue-600 dark:text-blue-400 transition-transform"></i>
                    </button>
                    <div class="faq-answer hidden p-4 md:p-6 bg-white dark:bg-gray-700">
                        <p class="text-gray-600 dark:text-gray-300">
                            While self-study is possible, structured guidance significantly improves your chances of top ranks. Our data shows 92% of top 100 rankers had some form of coaching. TestUrSelf's program provides the right direction, saves time, and ensures you cover all important topics.
                        </p>
                    </div>
                </div>
                
                <div class="border border-gray-200 dark:border-gray-700 rounded-lg overflow-hidden fade-in">
                    <button class="faq-question w-full flex justify-between items-center p-4 md:p-6 text-left bg-gray-50 dark:bg-gray-800 hover:bg-gray-100 dark:hover:bg-gray-700 transition">
                        <span class="text-lg font-medium text-gray-800 dark:text-white">How does TestUrSelf compare to other platforms?</span>
                        <i class="fas fa-chevron-down text-blue-600 dark:text-blue-400 transition-transform"></i>
                    </button>
                    <div class="faq-answer hidden p-4 md:p-6 bg-white dark:bg-gray-700">
                        <p class="text-gray-600 dark:text-gray-300">
                            TestUrSelf is the only platform exclusively focused on GATE Metallurgy with IIT/IISc faculty. Our content depth, test quality, and mentorship are unmatched. The results speak for themselves - we've produced AIR 1 every year since 2019 and have 3x more top 100 rankers than any other platform.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Final CTA -->
    <section class="py-16 bg-gradient-to-r from-blue-600 to-blue-800 text-white">
        <div class="container mx-auto px-4 sm:px-6 text-center">
            <h2 class="text-3xl md:text-4xl font-bold mb-6 fade-in">Start Your GATE Metallurgy Preparation Today!</h2>
            <p class="text-lg md:text-xl mb-8 max-w-3xl mx-auto fade-in">
                Join thousands of successful Metallurgy aspirants who trusted TestUrSelf for their GATE journey
            </p>
            
            <div class="flex flex-col sm:flex-row justify-center gap-4 fade-in">
                <a href="#" class="bg-white hover:bg-gray-100 text-blue-600 font-semibold py-3 px-6 md:px-8 rounded-lg transition transform hover:scale-105 text-lg">
                    <i class="fas fa-user-graduate mr-2"></i> Enroll Now
                </a>
                <a href="#" class="bg-transparent hover:bg-blue-700 border-2 border-white text-white font-semibold py-3 px-6 md:px-8 rounded-lg transition transform hover:scale-105 text-lg">
                    <i class="fas fa-calendar-alt mr-2"></i> Free Demo Class
                </a>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12">
        <div class="container mx-auto px-4 sm:px-6">
            <div class="grid md:grid-cols-4 gap-8">
                <div>
                    <h3 class="text-xl font-semibold text-white mb-4">TestUrSelf</h3>
                    <p class="mb-4">India's leading GATE Metallurgy preparation platform with proven results since 2018.</p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-white transition">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition">
                            <i class="fab fa-youtube"></i>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h3 class="text-xl font-semibold text-white mb-4">Quick Links</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="hover:text-white transition">Home</a></li>
                        <li><a href="#" class="hover:text-white transition">About Us</a></li>
                        <li><a href="#" class="hover:text-white transition">Courses</a></li>
                        <li><a href="#" class="hover:text-white transition">Test Series</a></li>
                        <li><a href="#" class="hover:text-white transition">Results</a></li>
                        <li><a href="#" class="hover:text-white transition">Contact</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-xl font-semibold text-white mb-4">Resources</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="hover:text-white transition">Blog</a></li>
                        <li><a href="#" class="hover:text-white transition">Free Materials</a></li>
                        <li><a href="#" class="hover:text-white transition">Video Lectures</a></li>
                        <li><a href="#" class="hover:text-white transition">PYQ Solutions</a></li>
                        <li><a href="#" class="hover:text-white transition">GATE Syllabus</a></li>
                        <li><a href="#" class="hover:text-white transition">FAQs</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-xl font-semibold text-white mb-4">Contact Us</h3>
                    <ul class="space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-map-marker-alt mt-1 mr-3"></i>
                            <span>123 Education Street, Bangalore, Karnataka 560001</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-phone-alt mt-1 mr-3"></i>
                            <span>+91 9876543210</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-envelope mt-1 mr-3"></i>
                            <span>info@testurself.com</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-12 pt-8 text-center">
                <p>&copy; 2023 TestUrSelf. All Rights Reserved.</p>
            </div>
        </div>
    </footer>
    
    <script>
        // Dark mode toggle
        const darkModeToggle = document.getElementById('darkModeToggle');
        const body = document.body;
        
        // Check for saved user preference
        if (localStorage.getItem('darkMode') === 'enabled') {
            body.classList.add('dark');
            darkModeToggle.innerHTML = '<i class="fas fa-sun"></i>';
        }
        
        darkModeToggle.addEventListener('click', () => {
            body.classList.toggle('dark');
            
            if (body.classList.contains('dark')) {
                localStorage.setItem('darkMode', 'enabled');
                darkModeToggle.innerHTML = '<i class="fas fa-sun"></i>';
            } else {
                localStorage.setItem('darkMode', 'disabled');
                darkModeToggle.innerHTML = '<i class="fas fa-moon"></i>';
            }
        });
        
        // Mobile menu toggle
        const mobileMenuButton = document.getElementById('mobileMenuButton');
        const mobileMenu = document.getElementById('mobileMenu');
        
        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });
        
        // Scroll animations
        const fadeElements = document.querySelectorAll('.fade-in');
        
        const fadeInObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, { threshold: 0.1 });
        
        fadeElements.forEach(element => {
            fadeInObserver.observe(element);
        });
        
        // Counter animation
        const counters = document.querySelectorAll('.counter');
        const speed = 200;
        
        counters.forEach(counter => {
            const target = +counter.getAttribute('data-target');
            const count = +counter.innerText;
            const increment = target / speed;
            
            if (count < target) {
                counter.innerText = Math.ceil(count + increment);
                setTimeout(updateCounter, 1);
            } else {
                counter.innerText = target;
            }
            
            function updateCounter() {
                const current = +counter.innerText;
                if (current < target) {
                    counter.innerText = Math.ceil(current + increment);
                    setTimeout(updateCounter, 1);
                } else {
                    counter.innerText = target;
                }
            }
        });
        
        // GSAP animations
        gsap.registerPlugin(ScrollTrigger);
        
        gsap.utils.toArray('.card-hover').forEach(card => {
            gsap.from(card, {
                scrollTrigger: {
                    trigger: card,
                    start: "top 80%",
                    toggleActions: "play none none none"
                },
                y: 50,
                opacity: 0,
                duration: 0.8,
                ease: "power2.out"
            });
        });
        
        // FAQ accordion
        const faqQuestions = document.querySelectorAll('.faq-question');
        
        faqQuestions.forEach(question => {
            question.addEventListener('click', () => {
                const answer = question.nextElementSibling;
                const icon = question.querySelector('i');
                
                // Toggle answer
                answer.classList.toggle('hidden');
                
                // Rotate icon
                icon.classList.toggle('transform');
                icon.classList.toggle('rotate-180');
                
                // Close other open answers
                faqQuestions.forEach(q => {
                    if (q !== question) {
                        q.nextElementSibling.classList.add('hidden');
                        q.querySelector('i').classList.remove('transform', 'rotate-180');
                    }
                });
            });
        });
        
        // Testimonial slider
        let currentSlide = 0;
        const slides = document.querySelectorAll('.testimonial-slide');
        const totalSlides = slides.length;
        const sliderTrack = document.getElementById('sliderTrack');
        const prevBtn = document.getElementById('prevBtn');
        const nextBtn = document.getElementById('nextBtn');
        const indicators = document.querySelectorAll('.slider-indicator');
        
        function goToSlide(index) {
            // Ensure index stays within bounds
            if (index < 0) {
                index = totalSlides - 1;
            } else if (index >= totalSlides) {
                index = 0;
            }
            
            sliderTrack.style.transform = `translateX(-${index * 100}%)`;
            currentSlide = index;
            
            // Update indicators
            indicators.forEach((indicator, i) => {
                if (i === index) {
                    indicator.classList.remove('bg-gray-300', 'dark:bg-gray-600');
                    indicator.classList.add('bg-blue-600', 'dark:bg-blue-400');
                } else {
                    indicator.classList.add('bg-gray-300', 'dark:bg-gray-600');
                    indicator.classList.remove('bg-blue-600', 'dark:bg-blue-400');
                }
            });
        }
        
        // Next slide
        if (nextBtn) {
            nextBtn.addEventListener('click', () => {
                goToSlide(currentSlide + 1);
            });
        }
        
        // Previous slide
        if (prevBtn) {
            prevBtn.addEventListener('click', () => {
                goToSlide(currentSlide - 1);
            });
        }
        
        // Indicator clicks
        indicators.forEach((indicator, index) => {
            indicator.addEventListener('click', () => {
                goToSlide(index);
            });
        });
        
        // Auto slide change
        setInterval(() => {
            goToSlide(currentSlide + 1);
        }, 5000);
        
        // Initialize slider
        function initSlider() {
            sliderTrack.style.width = `${totalSlides * 100}%`;
            slides.forEach(slide => {
                slide.style.width = `${100 / totalSlides}%`;
            });
            goToSlide(0);
        }
        
        // Initialize on load
        window.addEventListener('load', initSlider);
    </script>
</body>
</html>
