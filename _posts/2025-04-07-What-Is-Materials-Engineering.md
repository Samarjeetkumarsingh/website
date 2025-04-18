<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Materials Engineering | GATE MT Preparation & Career Guide</title>
    <meta name="description" content="Comprehensive guide to Materials Engineering, GATE MT exam preparation, career opportunities in metallurgy, and future technologies.">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        'satoshi': ['Satoshi', 'sans-serif'],
                        'clash': ['Clash Display', 'sans-serif'],
                        'techno': ['Rajdhani', 'sans-serif']
                    },
                    colors: {
                        'neon-blue': '#00f0ff',
                        'neon-pink': '#ff00f0',
                        'neon-green': '#00ff7a',
                        'neon-purple': '#a600ff',
                        'deep-space': '#0a0e17',
                        'star-dust': '#e0e0e0',
                        'gate-orange': '#FF6B00'
                    },
                    animation: {
                        'float': 'float 8s ease-in-out infinite',
                        'spin-slow': 'spin 20s linear infinite',
                        'pulse-slow': 'pulse 6s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                        'diffuse': 'diffuse 8s linear infinite',
                        'atom-spin': 'atomSpin 30s linear infinite',
                        'neon-glow': 'neonGlow 2s ease-in-out infinite alternate',
                        'bounce-slow': 'bounceSlow 3s infinite',
                        'wave': 'wave 5s ease-in-out infinite',
                        'particle-float': 'particleFloat 15s linear infinite'
                    },
                    keyframes: {
                        diffuse: {
                            '0%': { transform: 'translateX(0) translateY(0)', opacity: '1' },
                            '100%': { transform: 'translateX(var(--tx)) translateY(var(--ty))', opacity: '0' }
                        },
                        atomSpin: {
                            '0%': { transform: 'rotate(0deg)' },
                            '100%': { transform: 'rotate(360deg)' }
                        },
                        neonGlow: {
                            '0%': { 'text-shadow': '0 0 5px #fff, 0 0 10px #fff, 0 0 15px currentColor, 0 0 20px currentColor' },
                            '100%': { 'text-shadow': '0 0 10px #fff, 0 0 20px #fff, 0 0 30px currentColor, 0 0 40px currentColor' }
                        },
                        bounceSlow: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-20px)' }
                        },
                        wave: {
                            '0%, 100%': { transform: 'rotate(-3deg)' },
                            '50%': { transform: 'rotate(3deg)' }
                        },
                        particleFloat: {
                            '0%': { transform: 'translateX(0) translateY(0)', opacity: '1' },
                            '100%': { transform: 'translateX(calc(100vw + 100px)) translateY(var(--ty))', opacity: '0' }
                        }
                    }
                }
            }
        }
    </script>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Satoshi:wght@300;400;500;700;900&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Clash+Display:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@500;600;700&display=swap" rel="stylesheet">
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- AOS Animation -->
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    
    <style>
        :root {
            --neon-blue: #00f0ff;
            --neon-pink: #ff00f0;
            --neon-green: #00ff7a;
            --neon-purple: #a600ff;
            --deep-space: #0a0e17;
            --star-dust: #e0e0e0;
            --gate-orange: #FF6B00;
        }
        
        body {
            font-family: 'Satoshi', sans-serif;
            scroll-behavior: smooth;
            background-color: var(--deep-space);
            color: var(--star-dust);
            overflow-x: hidden;
            margin:0 auto;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Clash Display', sans-serif;
            font-weight: 600;
        }
        
        .tech-font {
            font-family: 'Rajdhani', sans-serif;
            font-weight: 600;
        }
        
        .hero-gradient {
            background: linear-gradient(135deg, rgba(0, 240, 255, 0.15) 0%, rgba(166, 0, 255, 0.15) 100%);
        }
        
        .hover-scale {
            transition: all 0.3s ease;
        }
        
        .hover-scale:hover {
            transform: scale(1.03);
        }
        
        .glass-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.36);
        }
        
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        
        ::-webkit-scrollbar-track {
            background: #0f172a;
        }
        
        ::-webkit-scrollbar-thumb {
            background: var(--neon-blue);
            border-radius: 4px;
        }
        
        ::-webkit-scrollbar-thumb:hover {
            background: var(--neon-green);
        }
        
        /* Diffusion Animation Container */
        .diffusion-container {
            position: relative;
            width: 100%;
            height: 300px;
            overflow: hidden;
            background: linear-gradient(90deg, rgba(0,0,0,0) 0%, rgba(0,240,255,0.1) 50%, rgba(0,0,0,0) 100%);
            display: flex;
            justify-content: space-between;
        }
        
        .concentration-zone {
            position: relative;
            width: 45%;
            height: 100%;
            display: flex;
            flex-wrap: wrap;
            align-content: flex-start;
        }
        
        .high-concentration {
            background: linear-gradient(90deg, rgba(166,0,255,0.1) 0%, rgba(0,0,0,0) 100%);
        }
        
        .low-concentration {
            background: linear-gradient(90deg, rgba(0,0,0,0) 0%, rgba(0,240,255,0.1) 100%);
        }
        
        .particle {
            position: absolute;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            animation: particleFloat 15s linear infinite;
            opacity: 0;
        }
        
        .particle-blue {
            background-color: var(--neon-blue);
            box-shadow: 0 0 10px var(--neon-blue), 0 0 20px var(--neon-blue);
        }
        
        .particle-green {
            background-color: var(--neon-green);
            box-shadow: 0 0 10px var(--neon-green), 0 0 20px var(--neon-green);
        }
        
        .particle-purple {
            background-color: var(--neon-purple);
            box-shadow: 0 0 10px var(--neon-purple), 0 0 20px var(--neon-purple);
        }
        
        .atom {
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            width: 150px;
            height: 150px;
        }
        
        .nucleus {
            width: 20px;
            height: 20px;
            background-color: var(--neon-pink);
            border-radius: 50%;
            box-shadow: 0 0 10px var(--neon-pink), 0 0 20px var(--neon-pink);
            z-index: 2;
        }
        
        .electron {
            position: absolute;
            width: 100%;
            height: 100%;
            border: 2px dashed rgba(0, 240, 255, 0.5);
            border-radius: 50%;
            animation: atomSpin 30s linear infinite;
        }
        
        .electron::before {
            content: '';
            position: absolute;
            top: -5px;
            left: 50%;
            transform: translateX(-50%);
            width: 10px;
            height: 10px;
            background-color: var(--neon-blue);
            border-radius: 50%;
            box-shadow: 0 0 10px var(--neon-blue), 0 0 20px var(--neon-blue);
        }
        
        .electron:nth-child(2) {
            width: 80%;
            height: 80%;
            animation-direction: reverse;
            animation-duration: 25s;
        }
        
        .electron:nth-child(2)::before {
            background-color: var(--neon-green);
            box-shadow: 0 0 10px var(--neon-green), 0 0 20px var(--neon-green);
        }
        
        .electron:nth-child(3) {
            width: 60%;
            height: 60%;
            animation-duration: 20s;
        }
        
        .electron:nth-child(3)::before {
            background-color: var(--neon-purple);
            box-shadow: 0 0 10px var(--neon-purple), 0 0 20px var(--neon-purple);
        }
        
        .neon-text {
            animation: neonGlow 2s ease-in-out infinite alternate;
        }
        
        .neon-blue {
            color: var(--neon-blue);
        }
        
        .neon-pink {
            color: var(--neon-pink);
        }
        
        .neon-green {
            color: var(--neon-green);
        }
        
        .neon-purple {
            color: var(--neon-purple);
        }
        
        .gate-orange {
            color: var(--gate-orange);
        }
        
        .gradient-border {
            position: relative;
            border-radius: 12px;
            overflow: hidden;
        }
        
        .gradient-border::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            border-radius: 12px;
            padding: 2px;
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-purple));
            -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
            -webkit-mask-composite: xor;
            mask-composite: exclude;
            pointer-events: none;
        }
        
        .grid-pattern {
            background-image: 
                linear-gradient(rgba(0, 240, 255, 0.1) 1px, transparent 1px),
                linear-gradient(90deg, rgba(0, 240, 255, 0.1) 1px, transparent 1px);
            background-size: 40px 40px;
        }
        
        /* GATE Exam Card */
        .gate-card {
            background: linear-gradient(135deg, rgba(255,107,0,0.1) 0%, rgba(10,14,23,0.8) 100%);
            border: 1px solid rgba(255,107,0,0.3);
        }
        
        /* Floating particles background */
        .particles-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: 0;
        }
        
        .particle-bg {
            position: absolute;
            width: 4px;
            height: 4px;
            border-radius: 50%;
            opacity: 0;
            animation: particleFloat 60s linear infinite;
        }
        
        /* Interactive crystal lattice */
        .crystal-lattice {
            display: grid;
            grid-template-columns: repeat(8, 1fr);
            grid-template-rows: repeat(8, 1fr);
            gap: 4px;
            width: 300px;
            height: 300px;
        }
        
        .lattice-point {
            width: 6px;
            height: 6px;
            background-color: var(--neon-blue);
            border-radius: 50%;
            transition: all 0.3s ease;
        }
        
        .lattice-point:hover {
            transform: scale(2);
            background-color: var(--neon-pink);
            box-shadow: 0 0 10px var(--neon-pink);
        }
        
        /* Interactive periodic table element */
        .element-card {
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .element-card:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 10px 20px rgba(0, 240, 255, 0.2);
        }
        
        /* 3D rotating material structure */
        .material-structure {
            transform-style: preserve-3d;
            animation: spin-slow 20s linear infinite;
        }
        
        /* Dynamic progress bars for GATE syllabus */
        .progress-bar {
            height: 8px;
            border-radius: 4px;
            background: rgba(255,255,255,0.1);
            overflow: hidden;
        }
        
        .progress-fill {
            height: 100%;
            border-radius: 4px;
            background: linear-gradient(90deg, var(--neon-blue), var(--neon-purple));
            transition: width 1s ease-in-out;
        }
    </style>
</head>
<body class="antialiased">
    <!-- Floating background particles -->
    <div class="particles-bg" id="particles-bg"></div>
    
    <!-- Sticky Navigation -->
    <nav class="sticky top-0 z-50 bg-deep-space/80 backdrop-blur-md shadow-sm border-b border-neon-blue/20">
        <div class="w-full px-6 py-4">
            <div class="flex justify-between items-center">
                <a href="#" class="text-2xl font-bold neon-blue neon-text">Material<span class="neon-green">Science</span></a>
                
                <!-- Mobile Menu Button -->
                <button id="menu-toggle" class="md:hidden text-star-dust focus:outline-none">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                    </svg>
                </button>
                
                <!-- Desktop Menu -->
                <div class="hidden md:flex space-x-8">
                    <a href="#introduction" class="text-star-dust hover:text-neon-blue font-medium transition-colors">Introduction</a>
                    <a href="#gate" class="text-star-dust hover:text-gate-orange font-medium transition-colors">GATE MT</a>
                    <a href="#diffusion" class="text-star-dust hover:text-neon-pink font-medium transition-colors">Diffusion</a>
                    <a href="#careers" class="text-star-dust hover:text-neon-purple font-medium transition-colors">Careers</a>
                    <a href="#future" class="text-star-dust hover:text-neon-blue font-medium transition-colors">Future</a>
                </div>
            </div>
            
            <!-- Mobile Menu -->
            <div id="mobile-menu" class="hidden md:hidden mt-4 pb-4">
                <a href="#introduction" class="block py-2 text-star-dust hover:text-neon-blue transition-colors">Introduction</a>
                <a href="#gate" class="block py-2 text-star-dust hover:text-gate-orange transition-colors">GATE MT</a>
                <a href="#diffusion" class="block py-2 text-star-dust hover:text-neon-pink transition-colors">Diffusion</a>
                <a href="#careers" class="block py-2 text-star-dust hover:text-neon-purple transition-colors">Careers</a>
                <a href="#future" class="block py-2 text-star-dust hover:text-neon-blue transition-colors">Future</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <header class="relative h-screen flex items-center justify-center overflow-hidden grid-pattern">
        <!-- Background Video -->
        <video autoplay muted loop class="absolute inset-0 w-full h-full object-cover z-0 opacity-30">
            <source src="https://assets.mixkit.co/videos/preview/mixkit-close-up-of-a-blue-circuit-board-12206-large.mp4" type="video/mp4">
        </video>
        <div class="absolute inset-0 bg-gradient-to-b from-deep-space/0 via-deep-space/80 to-deep-space z-1"></div>
        
        <!-- Animated atom -->
        <div class="absolute top-1/4 left-1/4 z-0 hidden lg:block">
            <div class="atom">
                <div class="nucleus"></div>
                <div class="electron"></div>
                <div class="electron"></div>
                <div class="electron"></div>
            </div>
        </div>
        
        <!-- Floating crystal structure -->
        <div class="absolute top-1/3 right-1/4 z-0 hidden lg:block" style="transform: rotate(45deg);">
            <div class="crystal-lattice">
                <!-- Generate lattice points -->
                <script>
                    document.addEventListener('DOMContentLoaded', function() {
                        const lattice = document.createElement('div');
                        lattice.className = 'crystal-lattice';
                        
                        for (let i = 0; i < 64; i++) {
                            const point = document.createElement('div');
                            point.className = 'lattice-point';
                            lattice.appendChild(point);
                        }
                        
                        document.querySelector('.absolute.top-1\\/3.right-1\\/4').appendChild(lattice);
                    });
                </script>
            </div>
        </div>
        
        <div class="relative z-10 px-6 text-center text-white w-full" data-aos="fade-up">
            <div class="max-w-6xl mx-auto">
                <h1 class="text-5xl md:text-7xl font-bold mb-6 leading-tight">
                    <span class="neon-blue neon-text">Materials</span> 
                    <span class="neon-green neon-text">Engineering</span>
                </h1>
                <p class="text-xl md:text-2xl mb-8 max-w-2xl mx-auto tech-font">Master the GATE MT exam and build the atomic foundations of tomorrow's technology</p>
                <div class="flex flex-col sm:flex-row justify-center gap-4">
                    <a href="#gate" class="bg-neon-blue text-deep-space font-semibold px-8 py-3 rounded-full hover:bg-neon-blue/90 transition duration-300 transform hover:scale-105 shadow-lg shadow-neon-blue/30">
                        GATE MT Guide
                    </a>
                    <a href="#careers" class="bg-transparent border-2 border-neon-green text-neon-green font-semibold px-8 py-3 rounded-full hover:bg-neon-green hover:text-deep-space transition duration-300 transform hover:scale-105 shadow-lg shadow-neon-green/20">
                        Career Paths
                    </a>
                </div>
            </div>
        </div>
        
        <a href="#introduction" class="absolute bottom-10 left-1/2 transform -translate-x-1/2 animate-bounce z-10 text-neon-blue">
            <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
            </svg>
        </a>
    </header>

    <!-- Introduction Section -->
    <section id="introduction" class="py-20 w-full relative overflow-hidden grid-pattern">
        <div class="w-full px-6">
            <div class="text-center mb-16" data-aos="fade-up">
                <span class="neon-blue font-semibold tech-font tracking-widest">THE SCIENCE OF MATERIALS</span>
                <h2 class="text-3xl md:text-4xl font-bold mb-4 mt-2">What is Materials Engineering?</h2>
                <div class="w-20 h-1 bg-gradient-to-r from-neon-blue to-neon-green mx-auto mb-6"></div>
                <p class="text-star-dust/80 max-w-3xl mx-auto">Materials Engineering is the interdisciplinary field that combines physics, chemistry, and engineering to design, develop, and optimize materials for real-world applications.</p>
            </div>
            
            <div class="grid md:grid-cols-3 gap-8 max-w-6xl mx-auto">
                <div class="glass-card p-8 rounded-xl hover-scale" data-aos="fade-up">
                    <div class="neon-blue text-4xl mb-4">
                        <i class="fas fa-atom"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 neon-blue">Atomic-Level Design</h3>
                    <p class="text-star-dust/80">Manipulating materials at the nanoscale to achieve desired properties like strength, conductivity, or flexibility.</p>
                    <div class="mt-4 h-1 bg-gradient-to-r from-neon-blue to-transparent w-full"></div>
                </div>
                
                <div class="glass-card p-8 rounded-xl hover-scale" data-aos="fade-up" data-aos-delay="100">
                    <div class="neon-green text-4xl mb-4">
                        <i class="fas fa-microscope"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 neon-green">Microstructure Analysis</h3>
                    <p class="text-star-dust/80">Studying crystal structures, grain boundaries, and defects to predict material behavior.</p>
                    <div class="mt-4 h-1 bg-gradient-to-r from-neon-green to-transparent w-full"></div>
                </div>
                
                <div class="glass-card p-8 rounded-xl hover-scale" data-aos="fade-up" data-aos-delay="200">
                    <div class="neon-purple text-4xl mb-4">
                        <i class="fas fa-industry"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 neon-purple">Industrial Application</h3>
                    <p class="text-star-dust/80">From aerospace alloys to biomedical implants, materials engineering powers modern industry.</p>
                    <div class="mt-4 h-1 bg-gradient-to-r from-neon-purple to-transparent w-full"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- GATE MT Exam Section -->
    <section id="gate" class="py-20 w-full relative overflow-hidden bg-gradient-to-br from-deep-space to-gate-orange/10">
        <div class="w-full px-6">
            <div class="text-center mb-16" data-aos="fade-up">
                <span class="gate-orange font-semibold tech-font tracking-widest">GATE EXAMINATION</span>
                <h2 class="text-3xl md:text-4xl font-bold mb-4 mt-2">GATE Metallurgical Engineering (MT)</h2>
                <div class="w-20 h-1 bg-gradient-to-r from-gate-orange to-neon-blue mx-auto mb-6"></div>
                <p class="text-star-dust/80 max-w-3xl mx-auto">Your gateway to PSUs jobs, higher education, and research opportunities in materials science.</p>
            </div>
            
            <div class="grid md:grid-cols-2 gap-10 items-center max-w-6xl mx-auto">
                <div class="space-y-8" data-aos="fade-right">
                    <div class="gate-card glass-card p-6 rounded-xl hover-scale">
                        <div class="flex items-start">
                            <div class="bg-gate-orange/10 p-3 rounded-full mr-4 border border-gate-orange/30">
                                <i class="fas fa-calendar-alt gate-orange"></i>
                            </div>
                            <div>
                                <h3 class="text-xl font-semibold mb-2 gate-orange">Exam Overview</h3>
                                <ul class="text-star-dust/80 space-y-2 text-sm">
                                    <li class="flex items-start">
                                        <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                                        <span><strong>Conducted by:</strong> 7 IITs and IISc on rotational basis (IIT Roorkee for GATE 2025)</span>
                                    </li>
                                    <li class="flex items-start">
                                        <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                                        <span><strong>Exam Mode:</strong> Computer Based Test (CBT)</span>
                                    </li>
                                    <li class="flex items-start">
                                        <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                                        <span><strong>Duration:</strong> 3 hours</span>
                                    </li>
                                    <li class="flex items-start">
                                        <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                                        <span><strong>Total Marks:</strong> 100 (55 - Metallurgical Engineering, 10 - General Aptitude)</span>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                    
                    <div class="gate-card glass-card p-6 rounded-xl hover-scale">
                        <div class="flex items-start">
                            <div class="bg-gate-orange/10 p-3 rounded-full mr-4 border border-gate-orange/30">
                                <i class="fas fa-book gate-orange"></i>
                            </div>
                            <div>
                                <h3 class="text-xl font-semibold mb-2 gate-orange">Syllabus Breakdown</h3>
                                <div class="space-y-4">
                                    <div>
                                        <div class="flex justify-between mb-1">
                                            <span class="text-sm text-star-dust/80">Thermodynamics & Rate Processes</span>
                                            <span class="text-sm text-star-dust/80">25%</span>
                                        </div>
                                        <div class="progress-bar">
                                            <div class="progress-fill" style="width: 25%"></div>
                                        </div>
                                    </div>
                                    <div>
                                        <div class="flex justify-between mb-1">
                                            <span class="text-sm text-star-dust/80">Extractive Metallurgy</span>
                                            <span class="text-sm text-star-dust/80">8%</span>
                                        </div>
                                        <div class="progress-bar">
                                            <div class="progress-fill" style="width: 8%"></div>
                                        </div>
                                    </div>
                                    <div>
                                        <div class="flex justify-between mb-1">
                                            <span class="text-sm text-star-dust/80">Physical Metallurgy</span>
                                            <span class="text-sm text-star-dust/80">15%</span>
                                        </div>
                                        <div class="progress-bar">
                                            <div class="progress-fill" style="width: 15%"></div>
                                        </div>
                                    </div>
                                    <div>
                                        <div class="flex justify-between mb-1">
                                            <span class="text-sm text-star-dust/80">Mechanical Metallurgy</span>
                                            <span class="text-sm text-star-dust/80">18%</span>
                                        </div>
                                        <div class="progress-bar">
                                            <div class="progress-fill" style="width: 18%"></div>
                                        </div>
                                    </div>
                                    <div>
                                        <div class="flex justify-between mb-1">
                                            <span class="text-sm text-star-dust/80">Manufacturing Processes</span>
                                            <span class="text-sm text-star-dust/80">9%</span>
                                        </div>
                                        <div class="progress-bar">
                                            <div class="progress-fill" style="width: 9%"></div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div data-aos="fade-left">
                    <div class="gate-card glass-card p-8 rounded-xl">
                        <h3 class="text-2xl font-bold mb-6 gate-orange text-center">GATE MT Preparation Strategy</h3>
                        
                        <div class="space-y-6">
                            <div class="flex items-start">
                                <div class="bg-gate-orange/10 p-2 rounded-full mr-4 border border-gate-orange/30">
                                    <i class="fas fa-check gate-orange"></i>
                                </div>
                                <div>
                                    <h4 class="font-semibold mb-1">Understand the Syllabus</h4>
                                    <p class="text-star-dust/80 text-sm">Thoroughly analyze the GATE MT syllabus and weightage of topics.</p>
                                </div>
                            </div>
                            
                            <div class="flex items-start">
                                <div class="bg-gate-orange/10 p-2 rounded-full mr-4 border border-gate-orange/30">
                                    <i class="fas fa-check gate-orange"></i>
                                </div>
                                <div>
                                    <h4 class="font-semibold mb-1">Standard Reference Books and Materials</h4>
                                    <p class="text-star-dust/80 text-sm">Use recommended books like "Physical Metallurgy" by Avner, "Extractive Metallurgy" by Ghosh and TestUrSelf's Study Materials.</p>
                                </div>
                            </div>
                            
                            <div class="flex items-start">
                                <div class="bg-gate-orange/10 p-2 rounded-full mr-4 border border-gate-orange/30">
                                    <i class="fas fa-check gate-orange"></i>
                                </div>
                                <div>
                                    <h4 class="font-semibold mb-1">Previous Year Papers</h4>
                                    <p class="text-star-dust/80 text-sm">Solve at least last 20 years' GATE MT papers to understand pattern. You must take PYQ's from TestUrSelf</p>
                                </div>
                            </div>
                            
                            <div class="flex items-start">
                                <div class="bg-gate-orange/10 p-2 rounded-full mr-4 border border-gate-orange/30">
                                    <i class="fas fa-check gate-orange"></i>
                                </div>
                                <div>
                                    <h4 class="font-semibold mb-1">Mock Tests of TestUrSelf</h4>
                                    <p class="text-star-dust/80 text-sm">Regularly take Sections, Partial & full-length mock tests under timed conditions.</p>
                                </div>
                            </div>
                            
                            <div class="flex items-start">
                                <div class="bg-gate-orange/10 p-2 rounded-full mr-4 border border-gate-orange/30">
                                    <i class="fas fa-check gate-orange"></i>
                                </div>
                                <div>
                                    <h4 class="font-semibold mb-1">Focus on Core Concepts</h4>
                                    <p class="text-star-dust/80 text-sm">Master thermodynamics, phase diagrams, heat treatment, extraction processes, mechanical metallurgy thoroughly.</p>
                                </div>
                            </div>
                            
                            <div class="mt-8 text-center">
                                <a href="https://www.testurself.in/gate-metallurgical-engineering-syllabus-2025/" class="bg-gate-orange text-deep-space font-semibold px-6 py-2 rounded-full hover:bg-gate-orange/90 transition duration-300 inline-block">
                                    Download Syllabus PDF
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Periodic Table Visualization -->
            <div class="mt-20" data-aos="fade-up">
                <h3 class="text-2xl font-bold mb-6 text-center neon-blue">Key Elements in Metallurgy</h3>
                <div class="flex flex-wrap justify-center gap-2 max-w-4xl mx-auto">
                    <!-- Transition Metals -->
                    <div class="element-card glass-card w-16 h-16 flex flex-col items-center justify-center rounded-lg neon-blue border border-neon-blue/30">
                        <div class="text-xs">26</div>
                        <div class="font-bold">Fe</div>
                        <div class="text-xs">Iron</div>
                    </div>
                    <div class="element-card glass-card w-16 h-16 flex flex-col items-center justify-center rounded-lg neon-blue border border-neon-blue/30">
                        <div class="text-xs">24</div>
                        <div class="font-bold">Cr</div>
                        <div class="text-xs">Chromium</div>
                    </div>
                    <div class="element-card glass-card w-16 h-16 flex flex-col items-center justify-center rounded-lg neon-blue border border-neon-blue/30">
                        <div class="text-xs">28</div>
                        <div class="font-bold">Ni</div>
                        <div class="text-xs">Nickel</div>
                    </div>
                    <div class="element-card glass-card w-16 h-16 flex flex-col items-center justify-center rounded-lg neon-blue border border-neon-blue/30">
                        <div class="text-xs">29</div>
                        <div class="font-bold">Cu</div>
                        <div class="text-xs">Copper</div>
                    </div>
                    <div class="element-card glass-card w-16 h-16 flex flex-col items-center justify-center rounded-lg neon-blue border border-neon-blue/30">
                        <div class="text-xs">13</div>
                        <div class="font-bold">Al</div>
                        <div class="text-xs">Aluminum</div>
                    </div>
                    <div class="element-card glass-card w-16 h-16 flex flex-col items-center justify-center rounded-lg neon-blue border border-neon-blue/30">
                        <div class="text-xs">22</div>
                        <div class="font-bold">Ti</div>
                        <div class="text-xs">Titanium</div>
                    </div>
                    <div class="element-card glass-card w-16 h-16 flex flex-col items-center justify-center rounded-lg neon-blue border border-neon-blue/30">
                        <div class="text-xs">74</div>
                        <div class="font-bold">W</div>
                        <div class="text-xs">Tungsten</div>
                    </div>
                    <div class="element-card glass-card w-16 h-16 flex flex-col items-center justify-center rounded-lg neon-blue border border-neon-blue/30">
                        <div class="text-xs">6</div>
                        <div class="font-bold">C</div>
                        <div class="text-xs">Carbon</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Why It Matters Section -->
    <section id="importance" class="py-20 w-full relative overflow-hidden bg-gradient-to-br from-deep-space to-neon-blue/10">
        <div class="w-full px-6">
            <div class="text-center mb-16" data-aos="fade-up">
                <span class="neon-green font-semibold tech-font tracking-widest">THE IMPACT</span>
                <h2 class="text-3xl md:text-4xl font-bold mb-4 mt-2">Why Materials Engineering Matters</h2>
                <div class="w-20 h-1 bg-gradient-to-r from-neon-green to-neon-blue mx-auto mb-6"></div>
                <p class="text-star-dust/80 max-w-3xl mx-auto">Materials innovation drives technological progress across every industry.</p>
            </div>
            
            <div class="grid md:grid-cols-2 gap-10 items-center max-w-6xl mx-auto">
                <div class="space-y-6" data-aos="fade-right">
                    <div class="flex items-start glass-card p-5 rounded-xl hover-scale">
                        <div class="bg-neon-blue/10 p-3 rounded-full mr-4 border border-neon-blue/30">
                            <i class="fas fa-space-shuttle neon-blue"></i>
                        </div>
                        <div>
                            <h3 class="text-xl font-semibold mb-2 neon-blue">Space Exploration</h3>
                            <p class="text-star-dust/80">Heat-resistant ceramics and lightweight alloys enable spacecraft to survive extreme conditions.</p>
                        </div>
                    </div>
                    
                    <div class="flex items-start glass-card p-5 rounded-xl hover-scale">
                        <div class="bg-neon-green/10 p-3 rounded-full mr-4 border border-neon-green/30">
                            <i class="fas fa-heartbeat neon-green"></i>
                        </div>
                        <div>
                            <h3 class="text-xl font-semibold mb-2 neon-green">Medical Breakthroughs</h3>
                            <p class="text-star-dust/80">Biocompatible materials for implants, prosthetics, and drug delivery systems.</p>
                        </div>
                    </div>
                    
                    <div class="flex items-start glass-card p-5 rounded-xl hover-scale">
                        <div class="bg-neon-purple/10 p-3 rounded-full mr-4 border border-neon-purple/30">
                            <i class="fas fa-bolt neon-purple"></i>
                        </div>
                        <div>
                            <h3 class="text-xl font-semibold mb-2 neon-purple">Renewable Energy</h3>
                            <p class="text-star-dust/80">High-efficiency solar cells, advanced batteries, and durable wind turbine blades.</p>
                        </div>
                    </div>
                </div>
                
                <div data-aos="fade-left">
                    <div class="gradient-border rounded-xl overflow-hidden">
                        <img src="https://images-website-testurself.s3.us-east-1.amazonaws.com/Designer.png" 
                             alt="Materials in aerospace" 
                             class="rounded-xl w-full h-auto object-cover">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Diffusion Animation Section -->
    <section id="diffusion" class="py-20 w-full relative overflow-hidden bg-gradient-to-br from-deep-space to-neon-purple/10">
        <div class="w-full px-6">
            <div class="text-center mb-16" data-aos="fade-up">
                <span class="neon-pink font-semibold tech-font tracking-widest">MATERIALS SCIENCE</span>
                <h2 class="text-3xl md:text-4xl font-bold mb-4 mt-2">Diffusion in Solids</h2>
                <div class="w-20 h-1 bg-gradient-to-r from-neon-pink to-neon-blue mx-auto mb-6"></div>
                <p class="text-star-dust/80 max-w-3xl mx-auto">The process by which atoms move from an area of high concentration to low concentration.</p>
            </div>
            
            <div class="max-w-6xl mx-auto grid md:grid-cols-2 gap-10 items-center">
                <div data-aos="fade-right">
                    <h3 class="text-2xl font-bold mb-4 neon-pink">Understanding Diffusion</h3>
                    <p class="text-star-dust/80 mb-6">Diffusion is a fundamental process in materials science that governs how atoms move through solids. This atomic-scale movement is crucial for processes like alloy formation, heat treatment, and semiconductor doping.</p>
                    
                    <div class="space-y-4">
                        <div class="flex items-start">
                            <div class="bg-neon-pink/10 p-2 rounded-full mr-4 border border-neon-pink/30">
                                <i class="fas fa-arrow-right neon-pink text-sm"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold mb-1">Fick's First Law</h4>
                                <p class="text-star-dust/80 text-sm">J = -D(dC/dx) where J is diffusion flux, D is diffusivity, and dC/dx is concentration gradient.</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-neon-pink/10 p-2 rounded-full mr-4 border border-neon-pink/30">
                                <i class="fas fa-arrow-right neon-pink text-sm"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold mb-1">Activation Energy</h4>
                                <p class="text-star-dust/80 text-sm">The energy barrier atoms must overcome to move through the crystal lattice.</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="bg-neon-pink/10 p-2 rounded-full mr-4 border border-neon-pink/30">
                                <i class="fas fa-arrow-right neon-pink text-sm"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold mb-1">Temperature Dependence</h4>
                                <p class="text-star-dust/80 text-sm">D = D₀ exp(-Q/RT) where Q is activation energy, R is gas constant, T is temperature.</p>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Interactive Diffusion Controls -->
                    <div class="mt-8 glass-card p-6 rounded-xl">
                        <h4 class="font-semibold mb-3 neon-blue">Diffusion Simulation Controls</h4>
                        <div class="space-y-4">
                            <div>
                                <label class="block text-sm text-star-dust/80 mb-1">Temperature (K)</label>
                                <input type="range" id="temp-slider" min="300" max="1200" value="600" class="w-full h-2 bg-deep-space rounded-lg appearance-none cursor-pointer">
                                <div class="flex justify-between text-xs text-star-dust/60">
                                    <span>300K</span>
                                    <span id="temp-value">600K</span>
                                    <span>1200K</span>
                                </div>
                            </div>
                            <div>
                                <label class="block text-sm text-star-dust/80 mb-1">Concentration Gradient</label>
                                <input type="range" id="gradient-slider" min="1" max="10" value="5" class="w-full h-2 bg-deep-space rounded-lg appearance-none cursor-pointer">
                                <div class="flex justify-between text-xs text-star-dust/60">
                                    <span>Low</span>
                                    <span id="gradient-value">Medium</span>
                                    <span>High</span>
                                </div>
                            </div>
                            <button id="restart-diffusion" class="bg-neon-blue/10 text-neon-blue px-4 py-2 rounded-full text-sm hover:bg-neon-blue/20 transition">
                                <i class="fas fa-sync-alt mr-2"></i> Restart Simulation
                            </button>
                        </div>
                    </div>
                </div>
                
                <div data-aos="fade-left">
                    <div class="diffusion-container rounded-xl" id="diffusion-simulator">
                        <div class="concentration-zone high-concentration" id="high-concentration">
                            <!-- Particles will be added here by JavaScript -->
                        </div>
                        <div class="concentration-zone low-concentration" id="low-concentration">
                            <!-- Particles will diffuse here -->
                        </div>
                    </div>
                    <div class="mt-6 flex justify-between text-xs text-star-dust/60">
                        <span>High Concentration</span>
                        <span>Low Concentration</span>
                    </div>
                    <div class="mt-8 glass-card p-6 rounded-xl">
                        <h4 class="font-semibold mb-3 neon-blue">Diffusion Mechanisms</h4>
                        <div class="flex flex-wrap gap-3">
                            <span class="px-3 py-1 bg-neon-blue/10 text-neon-blue rounded-full text-sm">Vacancy Diffusion</span>
                            <span class="px-3 py-1 bg-neon-green/10 text-neon-green rounded-full text-sm">Interstitial Diffusion</span>
                            <span class="px-3 py-1 bg-neon-purple/10 text-neon-purple rounded-full text-sm">Grain Boundary</span>
                            <span class="px-3 py-1 bg-neon-pink/10 text-neon-pink rounded-full text-sm">Surface Diffusion</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Career Opportunities Section -->
    <section id="careers" class="py-20 w-full relative overflow-hidden grid-pattern">
        <div class="w-full px-6">
            <div class="text-center mb-16" data-aos="fade-up">
                <span class="neon-purple font-semibold tech-font tracking-widest">CAREER PATHS</span>
                <h2 class="text-3xl md:text-4xl font-bold mb-4 mt-2">Where Materials Engineers Work</h2>
                <div class="w-20 h-1 bg-gradient-to-r from-neon-purple to-neon-blue mx-auto mb-6"></div>
                <p class="text-star-dust/80 max-w-3xl mx-auto">Diverse industries rely on materials expertise for innovation.</p>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6 max-w-6xl mx-auto">
                <div class="glass-card rounded-xl p-6 hover-scale" data-aos="flip-left">
                    <div class="bg-neon-blue/10 w-16 h-16 rounded-xl flex items-center justify-center mb-4 mx-auto border border-neon-blue/30">
                        <i class="fas fa-industry neon-blue text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2 neon-blue">PSUs through GATE (MT)</h3>
                    <p class="text-star-dust/80 text-center mb-4">Top Public Sector Undertakings recruiting Metallurgical Engineers:</p>
                    <ul class="text-sm text-star-dust/80 space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                            <span>Steel Authority of India (SAIL)</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                            <span>National Aluminium Company (NALCO)</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                            <span>Hindustan Copper Limited (HCL)</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                            <span>Mishra Dhatu Nigam (MIDHANI)</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                            <span>Hindustan Zinc Limited (HZL)</span>
                        </li>
                    </ul>
                    <div class="mt-4 text-center">
                        <a href="#" class="text-neon-blue text-sm font-medium hover:underline">View Salary Packages →</a>
                    </div>
                </div>
                
                <div class="glass-card rounded-xl p-6 hover-scale" data-aos="flip-left" data-aos-delay="100">
                    <div class="bg-neon-green/10 w-16 h-16 rounded-xl flex items-center justify-center mb-4 mx-auto border border-neon-green/30">
                        <i class="fas fa-graduation-cap neon-green text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2 neon-green">Higher Education</h3>
                    <p class="text-star-dust/80 text-center mb-4">Top institutes for Metallurgical Engineering in India:</p>
                    <ul class="text-sm text-star-dust/80 space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                            <span>IIT Bombay, Madras, Kharagpur, BHU</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                            <span>NIT Trichy, Rourkela, Warangal</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                            <span>Indian Institute of Science (IISc)</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                            <span>Institute of Chemical Technology (ICT)</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                            <span>IISERs, NISER, CEBS</span>
                        </li>
                    </ul>
                    <div class="mt-4 text-center">
                        <a href="#" class="text-neon-green text-sm font-medium hover:underline">View Cutoff Trends →</a>
                    </div>
                </div>
                
                <div class="glass-card rounded-xl p-6 hover-scale" data-aos="flip-left" data-aos-delay="200">
                    <div class="bg-neon-purple/10 w-16 h-16 rounded-xl flex items-center justify-center mb-4 mx-auto border border-neon-purple/30">
                        <i class="fas fa-flask neon-purple text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2 neon-purple">Research & Development</h3>
                    <p class="text-star-dust/80 text-center mb-4">Premier research organizations for Metallurgical Engineers:</p>
                    <ul class="text-sm text-star-dust/80 space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                            <span>Defense Metallurgical Research Lab (DMRL)</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                            <span>Bhabha Atomic Research Centre (BARC)</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                            <span>CSIR - National Metallurgical Laboratory</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                            <span>DRDO Laboratories</span>
                        </li>
                        <li class="flex items-start">
                            <i class="fas fa-check-circle text-neon-green mr-2 mt-1"></i>
                            <span>Vikram Sarabhai Space Centre (VSSC)</span>
                        </li>
                    </ul>
                    <div class="mt-4 text-center">
                        <a href="#" class="text-neon-purple text-sm font-medium hover:underline">Explore Research Areas →</a>
                    </div>
                </div>
            </div>
            
            <!-- Salary Comparison Chart -->
            <div class="mt-20 glass-card p-6 rounded-xl max-w-6xl mx-auto" data-aos="fade-up">
                <h3 class="text-2xl font-bold mb-6 text-center neon-blue">Career Progression & Salary Trends</h3>
                <div class="overflow-x-auto">
                    <table class="w-full text-sm text-star-dust/80">
                        <thead>
                            <tr class="border-b border-neon-blue/20">
                                <th class="text-left py-3 px-4">Position</th>
                                <th class="text-right py-3 px-4">Starting Salary (₹)</th>
                                <th class="text-right py-3 px-4">Mid-Career (₹)</th>
                                <th class="text-right py-3 px-4">Senior (₹)</th>
                                <th class="text-right py-3 px-4">Growth Potential</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr class="border-b border-neon-blue/10">
                                <td class="py-3 px-4">PSU Engineer (SAIL/NALCO)</td>
                                <td class="text-right py-3 px-4">8-12 LPA</td>
                                <td class="text-right py-3 px-4">15-20 LPA</td>
                                <td class="text-right py-3 px-4">25-35 LPA</td>
                                <td class="text-right py-3 px-4">
                                    <div class="inline-flex items-center">
                                        <span class="mr-2">High</span>
                                        <i class="fas fa-arrow-up text-neon-green"></i>
                                    </div>
                                </td>
                            </tr>
                            <tr class="border-b border-neon-blue/10">
                                <td class="py-3 px-4">Research Scientist (CSIR/DRDO)</td>
                                <td class="text-right py-3 px-4">6-9 LPA</td>
                                <td class="text-right py-3 px-4">12-18 LPA</td>
                                <td class="text-right py-3 px-4">20-30 LPA</td>
                                <td class="text-right py-3 px-4">
                                    <div class="inline-flex items-center">
                                        <span class="mr-2">Medium</span>
                                        <i class="fas fa-arrow-up text-neon-green"></i>
                                    </div>
                                </td>
                            </tr>
                            <tr class="border-b border-neon-blue/10">
                                <td class="py-3 px-4">Ph.D. Researcher (Abroad)</td>
                                <td class="text-right py-3 px-4">$30-50k</td>
                                <td class="text-right py-3 px-4">$70-90k</td>
                                <td class="text-right py-3 px-4">$100-150k</td>
                                <td class="text-right py-3 px-4">
                                    <div class="inline-flex items-center">
                                        <span class="mr-2">High</span>
                                        <i class="fas fa-arrow-up text-neon-green"></i>
                                    </div>
                                </td>
                            </tr>
                            <tr>
                                <td class="py-3 px-4">Academic Professor</td>
                                <td class="text-right py-3 px-4">8-10 LPA</td>
                                <td class="text-right py-3 px-4">12-15 LPA</td>
                                <td class="text-right py-3 px-4">18-25 LPA</td>
                                <td class="text-right py-3 px-4">
                                    <div class="inline-flex items-center">
                                        <span class="mr-2">Medium</span>
                                        <i class="fas fa-arrow-up text-neon-green"></i>
                                    </div>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                </div>
                <div class="mt-4 text-xs text-star-dust/60">
                    *LPA = Lakhs Per Annum | Figures are approximate and vary by organization
                </div>
            </div>
        </div>
    </section>
<!-- Testimonials Section -->
    <section class="py-20 w-full relative overflow-hidden bg-gradient-to-br from-deep-space to-neon-pink/10">
        <div class="w-full px-6">
            <div class="text-center mb-16" data-aos="fade-up">
                <span class="neon-blue font-semibold tech-font tracking-widest">INDUSTRY INSIGHTS</span>
                <h2 class="text-3xl md:text-4xl font-bold mb-4 mt-2">What Leaders Say</h2>
                <div class="w-20 h-1 bg-gradient-to-r from-neon-blue to-neon-pink mx-auto mb-6"></div>
                <p class="text-star-dust/80 max-w-3xl mx-auto">Industry leaders on the critical role of materials engineering.</p>
            </div>
            
            <div class="grid md:grid-cols-2 gap-8 max-w-5xl mx-auto">
                <!-- Elon Musk Tweet 1 -->
                <div class="glass-card rounded-xl overflow-hidden hover-scale" data-aos="zoom-in">
                    <div class="p-6">
                        <div class="flex items-start">
                            <img src="https://pbs.twimg.com/profile_images/1683325380441128960/yRsRRjGO_400x400.jpg" 
                                 alt="Elon Musk" 
                                 class="w-14 h-14 rounded-full mr-4">
                            <div>
                                <div class="flex items-center mb-2">
                                    <h3 class="text-lg font-bold mr-2">Elon Musk</h3>
                                    <span class="text-star-dust/60 text-sm">@elonmusk</span>
                                </div>
                                <p class="text-star-dust mb-4">"Take Materials Science 101. You won’t regret it."</p>
                                <div class="flex items-center text-star-dust/60 text-sm">
                                    <i class="fas fa-retweet mr-2"></i>
                                    <span class="mr-4">24.5K</span>
                                    <i class="fas fa-heart mr-2"></i>
                                    <span>128.7K</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="bg-deep-space/80 px-6 py-3 flex items-center text-sm border-t border-neon-blue/20">
                        <i class="fab fa-twitter text-neon-blue mr-2"></i>
                        <span>June 15, 2022</span>
                    </div>
                </div>
                
                <!-- Elon Musk Tweet 2 -->
                <div class="glass-card rounded-xl overflow-hidden hover-scale" data-aos="zoom-in" data-aos-delay="100">
                    <div class="p-6">
                        <div class="flex items-start">
                            <img src="https://pbs.twimg.com/profile_images/1683325380441128960/yRsRRjGO_400x400.jpg" 
                                 alt="Elon Musk" 
                                 class="w-14 h-14 rounded-full mr-4">
                            <div>
                                <div class="flex items-center mb-2">
                                    <h3 class="text-lg font-bold mr-2">Elon Musk</h3>
                                    <span class="text-star-dust/60 text-sm">@elonmusk</span>
                                </div>
                                <p class="text-star-dust mb-4">"The fundamental limitation in rocket design is materials science. If we had materials that could withstand higher temperatures, we could make rockets dramatically more efficient."</p>
                                <div class="flex items-center text-star-dust/60 text-sm">
                                    <i class="fas fa-retweet mr-2"></i>
                                    <span class="mr-4">18.2K</span>
                                    <i class="fas fa-heart mr-2"></i>
                                    <span>95.3K</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="bg-deep-space/80 px-6 py-3 flex items-center text-sm border-t border-neon-blue/20">
                        <i class="fab fa-twitter text-neon-blue mr-2"></i>
                        <span>March 8, 2023</span>
                    </div>
                </div>
                
                <!-- Industry Expert Testimonial -->
                <div class="glass-card rounded-xl overflow-hidden hover-scale" data-aos="zoom-in" data-aos-delay="200">
                    <div class="p-6">
                        <div class="flex items-start">
                            <img src="https://images.unsplash.com/photo-1560250097-0b93528c311a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=987&q=80" 
                                 alt="Dr. Anil Kumar" 
                                 class="w-14 h-14 rounded-full mr-4">
                            <div>
                                <div class="flex items-center mb-2">
                                    <h3 class="text-lg font-bold mr-2">Dr. Anil Kumar</h3>
                                    <span class="text-star-dust/60 text-sm">Ex-Director, NML Jamshedpur</span>
                                </div>
                                <p class="text-star-dust mb-4">"Metallurgical engineering is the backbone of India's industrial growth. With GATE (MT) as the gateway, our graduates are leading innovations in steel, aluminum, and advanced materials sectors."</p>
                                <div class="flex items-center text-star-dust/60 text-sm">
                                    <i class="fas fa-building mr-2"></i>
                                    <span>National Metallurgical Laboratory</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="bg-deep-space/80 px-6 py-3 flex items-center text-sm border-t border-neon-blue/20">
                        <i class="fas fa-quote-left text-neon-green mr-2"></i>
                        <span>Materials Today Conference, 2023</span>
                    </div>
                </div>
                
                <!-- Student Testimonial -->
                <div class="glass-card rounded-xl overflow-hidden hover-scale" data-aos="zoom-in" data-aos-delay="300">
                    <div class="p-6">
                        <div class="flex items-start">
                            <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=988&q=80" 
                                 alt="Priya Sharma" 
                                 class="w-14 h-14 rounded-full mr-4">
                            <div>
                                <div class="flex items-center mb-2">
                                    <h3 class="text-lg font-bold mr-2">Priya Sharma</h3>
                                    <span class="text-star-dust/60 text-sm">GATE Topper (MT), 2022</span>
                                </div>
                                <p class="text-star-dust mb-4">"Clearing GATE in Metallurgical Engineering opened doors to IISc Bangalore and then to SAIL. The depth of materials knowledge we gain is unparalleled and highly valued in core industries."</p>
                                <div class="flex items-center text-star-dust/60 text-sm">
                                    <i class="fas fa-university mr-2"></i>
                                    <span>IISc Bangalore → SAIL</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="bg-deep-space/80 px-6 py-3 flex items-center text-sm border-t border-neon-blue/20">
                        <i class="fas fa-quote-left text-neon-green mr-2"></i>
                        <span>GATE Success Story, 2023</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Future Trends Section -->
    <section id="future" class="py-20 w-full relative overflow-hidden bg-gradient-to-br from-deep-space to-neon-green/10">
        <div class="w-full px-6">
            <div class="text-center mb-16" data-aos="fade-up">
                <span class="neon-blue font-semibold tech-font tracking-widest">TOMORROW'S MATERIALS</span>
                <h2 class="text-3xl md:text-4xl font-bold mb-4 mt-2">The Future of Materials Engineering</h2>
                <div class="w-20 h-1 bg-gradient-to-r from-neon-blue to-neon-green mx-auto mb-6"></div>
                <p class="text-star-dust/80 max-w-3xl mx-auto">Cutting-edge innovations that will redefine industries.</p>
            </div>
            
            <div class="grid md:grid-cols-3 gap-8 max-w-6xl mx-auto">
                <div class="glass-card p-6 rounded-xl hover-scale" data-aos="fade-up">
                    <div class="gradient-border rounded-lg overflow-hidden mb-4">
                        <img src="https://images.unsplash.com/photo-1581094794329-c8112a89af12?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
                             alt="Nanomaterials" 
                             class="w-full h-48 object-cover">
                    </div>
                    <h3 class="text-xl font-semibold mb-2 neon-blue">Nanomaterials</h3>
                    <p class="text-star-dust/80 mb-4">Graphene, quantum dots, and carbon nanotubes enabling breakthroughs in electronics and medicine.</p>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-2 py-1 bg-neon-blue/10 text-neon-blue rounded-full text-xs">Graphene</span>
                        <span class="px-2 py-1 bg-neon-blue/10 text-neon-blue rounded-full text-xs">Quantum Dots</span>
                        <span class="px-2 py-1 bg-neon-blue/10 text-neon-blue rounded-full text-xs">CNTs</span>
                    </div>
                </div>
                
                <div class="glass-card p-6 rounded-xl hover-scale" data-aos="fade-up" data-aos-delay="100">
                    <div class="gradient-border rounded-lg overflow-hidden mb-4">
                        <img src="https://images.unsplash.com/photo-1575505586569-646b2ca898fc?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2086&q=80" 
                             alt="Biomaterials" 
                             class="w-full h-48 object-cover">
                    </div>
                    <h3 class="text-xl font-semibold mb-2 neon-green">Biomaterials</h3>
                    <p class="text-star-dust/80 mb-4">3D-printed organs, bioabsorbable implants, and smart drug delivery systems.</p>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-2 py-1 bg-neon-green/10 text-neon-green rounded-full text-xs">3D Bioprinting</span>
                        <span class="px-2 py-1 bg-neon-green/10 text-neon-green rounded-full text-xs">Hydrogels</span>
                        <span class="px-2 py-1 bg-neon-green/10 text-neon-green rounded-full text-xs">Scaffolds</span>
                    </div>
                </div>
                
                <div class="glass-card p-6 rounded-xl hover-scale" data-aos="fade-up" data-aos-delay="200">
                    <div class="gradient-border rounded-lg overflow-hidden mb-4">
                        <img src="https://images.unsplash.com/photo-1508514177221-188b1cf16e9d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2072&q=80" 
                             alt="Sustainable materials" 
                             class="w-full h-48 object-cover">
                    </div>
                    <h3 class="text-xl font-semibold mb-2 neon-purple">Sustainable Materials</h3>
                    <p class="text-star-dust/80 mb-4">Self-healing concrete, biodegradable plastics, and energy-efficient phase-change materials.</p>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-2 py-1 bg-neon-purple/10 text-neon-purple rounded-full text-xs">Green Steel</span>
                        <span class="px-2 py-1 bg-neon-purple/10 text-neon-purple rounded-full text-xs">Biodegradables</span>
                        <span class="px-2 py-1 bg-neon-purple/10 text-neon-purple rounded-full text-xs">Recyclables</span>
                    </div>
                </div>
            </div>
            
            <!-- Emerging Technologies Timeline -->
            <div class="mt-20 glass-card p-8 rounded-xl max-w-6xl mx-auto" data-aos="fade-up">
                <h3 class="text-2xl font-bold mb-8 text-center neon-pink">Materials Innovation Timeline</h3>
                <div class="relative">
                    <!-- Timeline line -->
                    <div class="absolute left-1/2 h-full w-1 bg-gradient-to-b from-neon-pink to-neon-blue transform -translate-x-1/2"></div>
                    
                    <!-- Timeline items -->
                    <div class="mb-8 flex justify-between items-center w-full">
                        <div class="w-5/12" data-aos="fade-right">
                            <div class="p-4 glass-card rounded-lg">
                                <h4 class="font-bold mb-2 neon-blue">2023-2025</h4>
                                <p class="text-sm text-star-dust/80">Commercialization of solid-state batteries with ceramic electrolytes</p>
                            </div>
                        </div>
                        <div class="w-1/12 flex justify-center">
                            <div class="w-6 h-6 rounded-full bg-neon-pink border-4 border-deep-space"></div>
                        </div>
                        <div class="w-5/12"></div>
                    </div>
                    
                    <div class="mb-8 flex justify-between items-center w-full">
                        <div class="w-5/12"></div>
                        <div class="w-1/12 flex justify-center">
                            <div class="w-6 h-6 rounded-full bg-neon-green border-4 border-deep-space"></div>
                        </div>
                        <div class="w-5/12" data-aos="fade-left">
                            <div class="p-4 glass-card rounded-lg">
                                <h4 class="font-bold mb-2 neon-green">2025-2028</h4>
                                <p class="text-sm text-star-dust/80">Widespread use of self-healing materials in infrastructure</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="mb-8 flex justify-between items-center w-full">
                        <div class="w-5/12" data-aos="fade-right">
                            <div class="p-4 glass-card rounded-lg">
                                <h4 class="font-bold mb-2 neon-purple">2028-2030</h4>
                                <p class="text-sm text-star-dust/80">Metamaterials for practical invisibility cloaking applications</p>
                            </div>
                        </div>
                        <div class="w-1/12 flex justify-center">
                            <div class="w-6 h-6 rounded-full bg-neon-purple border-4 border-deep-space"></div>
                        </div>
                        <div class="w-5/12"></div>
                    </div>
                    
                    <div class="flex justify-between items-center w-full">
                        <div class="w-5/12"></div>
                        <div class="w-1/12 flex justify-center">
                            <div class="w-6 h-6 rounded-full bg-neon-blue border-4 border-deep-space"></div>
                        </div>
                        <div class="w-5/12" data-aos="fade-left">
                            <div class="p-4 glass-card rounded-lg">
                                <h4 class="font-bold mb-2 neon-blue">2030+</h4>
                                <p class="text-sm text-star-dust/80">Room-temperature superconductors in power transmission</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Call to Action -->
    <section class="py-20 bg-gradient-to-r from-neon-blue to-neon-purple text-deep-space w-full">
        <div class="w-full px-6 text-center">
            <div class="max-w-4xl mx-auto" data-aos="zoom-in">
                <h2 class="text-3xl md:text-4xl font-bold mb-6">Ready to Master Materials Engineering?</h2>
                <p class="text-xl mb-8">Get our free GATE MT preparation kit with syllabus, previous papers, and study plan.</p>
                
                <div class="flex flex-col sm:flex-row justify-center gap-4">
                    <a href="#" class="bg-deep-space text-neon-blue font-semibold px-8 py-3 rounded-full hover:bg-deep-space/90 transition duration-300 transform hover:scale-105 shadow-lg shadow-deep-space/30">
                        Download Free Kit
                    </a>
                    <a href="#" class="bg-transparent border-2 border-deep-space text-deep-space font-semibold px-8 py-3 rounded-full hover:bg-deep-space hover:text-neon-blue transition duration-300 transform hover:scale-105 shadow-lg shadow-deep-space/20">
                        Join Webinar
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-deep-space/90 text-star-dust/60 py-12 w-full border-t border-neon-blue/20">
        <div class="w-full px-6">
            <div class="grid md:grid-cols-4 gap-10 max-w-6xl mx-auto">
                <div>
                    <h3 class="text-white text-lg font-semibold mb-4">Material<span class="neon-green">Science</span></h3>
                    <p class="mb-4">Empowering future materials engineers through education and innovation.</p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-star-dust/60 hover:text-neon-blue transition-colors">
                            <i class="fab fa-twitter text-xl"></i>
                        </a>
                        <a href="#" class="text-star-dust/60 hover:text-neon-blue transition-colors">
                            <i class="fab fa-linkedin text-xl"></i>
                        </a>
                        <a href="#" class="text-star-dust/60 hover:text-neon-blue transition-colors">
                            <i class="fab fa-youtube text-xl"></i>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h3 class="text-white text-lg font-semibold mb-4">Quick Links</h3>
                    <ul class="space-y-2">
                        <li><a href="#introduction" class="hover:text-neon-blue transition-colors">Introduction</a></li>
                        <li><a href="#gate" class="hover:text-gate-orange transition-colors">GATE MT</a></li>
                        <li><a href="#diffusion" class="hover:text-neon-pink transition-colors">Diffusion</a></li>
                        <li><a href="#careers" class="hover:text-neon-purple transition-colors">Careers</a></li>
                        <li><a href="#future" class="hover:text-neon-blue transition-colors">Future</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-white text-lg font-semibold mb-4">Resources</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="hover:text-neon-green transition-colors">Blog</a></li>
                        <li><a href="#" class="hover:text-neon-green transition-colors">Research Papers</a></li>
                        <li><a href="#" class="hover:text-neon-green transition-colors">Webinars</a></li>
                        <li><a href="#" class="hover:text-neon-green transition-colors">FAQ</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-white text-lg font-semibold mb-4">Contact</h3>
                    <ul class="space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-map-marker-alt mt-1 mr-3 neon-blue"></i>
                            <span>Patna, Bihar, IN 800013</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-envelope mr-3 neon-green"></i>
                            <span>info@testurself.in</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-phone-alt mr-3 neon-purple"></i>
                            <span>+91 8709271314</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-neon-blue/20 mt-10 pt-6 flex flex-col md:flex-row justify-between items-center max-w-6xl mx-auto">
                <p>&copy; TestUrSelf. All rights reserved.</p>
                <div class="mt-4 md:mt-0">
                    <a href="#" class="text-sm hover:text-neon-blue transition-colors mr-4">Privacy Policy</a>
                    <a href="#" class="text-sm hover:text-neon-blue transition-colors">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- Back to Top Button -->
    <button id="back-to-top" class="fixed bottom-8 right-8 bg-neon-blue text-deep-space w-12 h-12 rounded-full shadow-lg shadow-neon-blue/30 hidden items-center justify-center hover:bg-neon-blue/90 transition duration-300">
        <i class="fas fa-arrow-up text-xl"></i>
    </button>

    <!-- Scripts -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/js/all.min.js"></script>
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        // Initialize AOS animation library
        AOS.init({
            duration: 800,
            easing: 'ease-in-out',
            once: true
        });
        
        // Mobile menu toggle
        document.getElementById('menu-toggle').addEventListener('click', function() {
            document.getElementById('mobile-menu').classList.toggle('hidden');
        });
        
        // Back to top button
        const backToTopButton = document.getElementById('back-to-top');
        window.addEventListener('scroll', function() {
            if (window.pageYOffset > 300) {
                backToTopButton.classList.remove('hidden');
                backToTopButton.classList.add('flex');
            } else {
                backToTopButton.classList.add('hidden');
                backToTopButton.classList.remove('flex');
            }
        });
        
        backToTopButton.addEventListener('click', function() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });
        
        // Smooth scrolling for navigation links
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
                    document.getElementById('mobile-menu').classList.add('hidden');
                }
            });
        });

        // Create background particles
        function createBackgroundParticles() {
            const container = document.getElementById('particles-bg');
            const particleCount = 50;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle-bg';
                
                // Random position
                const left = Math.random() * 100;
                const top = Math.random() * 100;
                
                // Random movement
                const ty = (Math.random() - 0.5) * 100;
                
                // Random size
                const size = 2 + Math.random() * 3;
                
                // Random color
                const colors = ['neon-blue', 'neon-green', 'neon-purple', 'neon-pink'];
                const color = colors[Math.floor(Math.random() * colors.length)];
                
                particle.style.left = `${left}%`;
                particle.style.top = `${top}%`;
                particle.style.setProperty('--ty', `${ty}vh`);
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                particle.style.animationDelay = `${Math.random() * 30}s`;
                particle.style.animationDuration = `${30 + Math.random() * 60}s`;
                
                // Add color class
                particle.classList.add(`particle-${color}`);
                
                container.appendChild(particle);
            }
        }
        
        // Create diffusion animation particles
        function createDiffusionParticles() {
            const highZone = document.getElementById('high-concentration');
            const lowZone = document.getElementById('low-concentration');
            
            // Clear existing particles
            highZone.innerHTML = '';
            lowZone.innerHTML = '';
            
            // Get current temperature and gradient values
            const tempValue = parseInt(document.getElementById('temp-slider').value);
            const gradientValue = parseInt(document.getElementById('gradient-slider').value);
            
            // Calculate particle count based on gradient
            const particleCount = 20 + gradientValue * 5;
            
            // Calculate speed factor based on temperature (300-1200K)
            const speedFactor = tempValue / 600; // Normalized to 600K baseline
            
            // Create particles in high concentration zone
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle particle-blue';
                
                // Random position in high concentration zone
                const left = Math.random() * 80 + 10; // 10-90% of container
                const top = Math.random() * 80 + 10;  // 10-90% of container
                
                // Random movement towards low concentration
                const tx = 100 + Math.random() * 50; // 100-150% movement right
                const ty = (Math.random() - 0.5) * 60; // -30 to +30 vertical movement
                
                particle.style.left = `${left}%`;
                particle.style.top = `${top}%`;
                particle.style.setProperty('--tx', `${tx}%`);
                particle.style.setProperty('--ty', `${ty}%`);
                
                // Adjust animation based on temperature
                particle.style.animationDuration = `${8 / speedFactor}s`;
                
                // Random delay for staggered animation
                particle.style.animationDelay = `${Math.random() * 5}s`;
                
                highZone.appendChild(particle);
            }
            
            // Create some particles in low concentration zone (fewer)
            for (let i = 0; i < particleCount / 4; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle particle-blue';
                
                // Position in low concentration zone
                const left = Math.random() * 80 + 10;
                const top = Math.random() * 80 + 10;
                
                // Slight random movement
                const tx = Math.random() * 40 - 20; // -20 to +20
                const ty = (Math.random() - 0.5) * 40; // -20 to +20
                
                particle.style.left = `${left}%`;
                particle.style.top = `${top}%`;
                particle.style.setProperty('--tx', `${tx}%`);
                particle.style.setProperty('--ty', `${ty}%`);
                particle.style.animationDuration = `${8 / speedFactor}s`;
                particle.style.animationDelay = `${Math.random() * 5}s`;
                
                lowZone.appendChild(particle);
            }
        }
        
        // Update temperature value display
        document.getElementById('temp-slider').addEventListener('input', function() {
            document.getElementById('temp-value').textContent = `${this.value}K`;
            createDiffusionParticles();
        });
        
        // Update gradient value display
        document.getElementById('gradient-slider').addEventListener('input', function() {
            const gradientText = ['Low', 'Medium', 'High'][Math.floor(this.value / 3.34)];
            document.getElementById('gradient-value').textContent = gradientText;
            createDiffusionParticles();
        });
        
        // Restart diffusion button
        document.getElementById('restart-diffusion').addEventListener('click', createDiffusionParticles);
        
        // Initialize particles when page loads
        window.addEventListener('load', function() {
            createBackgroundParticles();
            createDiffusionParticles();
            
            // Set initial values for displays
            document.getElementById('temp-value').textContent = `${document.getElementById('temp-slider').value}K`;
            const gradientValue = parseInt(document.getElementById('gradient-slider').value);
            const gradientText = ['Low', 'Medium', 'High'][Math.floor(gradientValue / 3.34)];
            document.getElementById('gradient-value').textContent = gradientText;
        });
        
        // Interactive crystal lattice
        document.addEventListener('DOMContentLoaded', function() {
            const latticeContainer = document.querySelector('.absolute.top-1\\/3.right-1\\/4');
            if (latticeContainer) {
                const lattice = document.createElement('div');
                lattice.className = 'crystal-lattice';
                
                for (let i = 0; i < 64; i++) {
                    const point = document.createElement('div');
                    point.className = 'lattice-point';
                    
                    // Add slight animation delay for each point
                    point.style.transitionDelay = `${i * 0.05}s`;
                    
                    lattice.appendChild(point);
                }
                
                latticeContainer.appendChild(lattice);
            }
        });
    </script>
</body>
</html>
