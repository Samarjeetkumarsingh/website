<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Materials Engineering | The Atomic Frontier of Innovation</title>
    <meta name="description" content="Explore the fascinating world of Materials Engineering - from atomic structures to industrial applications and future technologies.">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        'satoshi': ['Satoshi', 'sans-serif'],
                        'clash': ['Clash Display', 'sans-serif'],
                        'techno': ['Orbitron', 'sans-serif']
                    },
                    colors: {
                        'neon-blue': '#00f5ff',
                        'electric-purple': '#bc13fe',
                        'acid-green': '#7fff00',
                        'hot-pink': '#ff28d1',
                        'vivid-orange': '#ff5e00',
                        'deep-space': '#0f0e17',
                        'cosmic-purple': '#4b0082',
                        'quantum-blue': '#0abdc6'
                    },
                    animation: {
                        'float': 'float 8s ease-in-out infinite',
                        'float-2': 'float2 10s ease-in-out infinite',
                        'float-3': 'float3 7s ease-in-out infinite',
                        'spin-slow': 'spin 20s linear infinite',
                        'pulse-glow': 'pulse-glow 4s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                        'pulse-glow-fast': 'pulse-glow 2s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                        'diffuse': 'diffuse 6s linear infinite',
                        'breathing': 'breathing 5s ease-out infinite',
                        'vibrate': 'vibrate 0.3s linear infinite',
                        'atom-spin': 'atom-spin 15s linear infinite',
                        'electron-orbit': 'electron-orbit 8s linear infinite',
                        'wave': 'wave 3s ease-in-out infinite',
                        'neon-flicker': 'neon-flicker 1.5s ease-in-out infinite alternate'
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0) rotate(0deg)' },
                            '50%': { transform: 'translateY(-30px) rotate(5deg)' },
                        },
                        float2: {
                            '0%, 100%': { transform: 'translateY(0) rotate(0deg)' },
                            '50%': { transform: 'translateY(-40px) rotate(-8deg)' },
                        },
                        float3: {
                            '0%, 100%': { transform: 'translateY(0) rotate(0deg)' },
                            '50%': { transform: 'translateY(-25px) rotate(3deg)' },
                        },
                        'pulse-glow': {
                            '0%, 100%': { opacity: '0.8', boxShadow: '0 0 5px currentColor' },
                            '50%': { opacity: '1', boxShadow: '0 0 20px currentColor' }
                        },
                        'diffuse': {
                            '0%': { transform: 'scale(0.5)', opacity: '1' },
                            '100%': { transform: 'scale(1.5)', opacity: '0' }
                        },
                        'breathing': {
                            '0%, 100%': { transform: 'scale(1)' },
                            '50%': { transform: 'scale(1.05)' }
                        },
                        'vibrate': {
                            '0%, 100%': { transform: 'translateX(0)' },
                            '20%, 60%': { transform: 'translateX(-2px)' },
                            '40%, 80%': { transform: 'translateX(2px)' }
                        },
                        'atom-spin': {
                            '0%': { transform: 'rotate(0deg)' },
                            '100%': { transform: 'rotate(360deg)' }
                        },
                        'electron-orbit': {
                            '0%': { transform: 'rotate(0deg) translateX(50px) rotate(0deg)' },
                            '100%': { transform: 'rotate(360deg) translateX(50px) rotate(-360deg)' }
                        },
                        'wave': {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-10px)' }
                        },
                        'neon-flicker': {
                            '0%': { opacity: '0.7', textShadow: '0 0 5px currentColor' },
                            '100%': { opacity: '1', textShadow: '0 0 15px currentColor' }
                        }
                    }
                }
            }
        }
    </script>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Satoshi:wght@300;400;500;700;900&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Clash+Display:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- AOS Animation -->
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    
    <style>
        body {
            font-family: 'Satoshi', sans-serif;
            scroll-behavior: smooth;
            background-color: #0f0e17;
            color: #fffffe;
            overflow-x: hidden;
            margin:0 auto;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Clash Display', sans-serif;
            font-weight: 600;
        }
        
        .tech-font {
            font-family: 'Orbitron', sans-serif;
        }
        
        .hero-gradient {
            background: linear-gradient(135deg, rgba(10, 189, 198, 0.8) 0%, rgba(188, 19, 254, 0.8) 100%);
        }
        
        .crystal {
            filter: drop-shadow(0 0 10px rgba(0, 245, 255, 0.5));
            opacity: 0.8;
        }
        
        .crystal-small {
            width: 60px;
            height: 60px;
            opacity: 0.6;
        }
        
        .crystal-medium {
            width: 100px;
            height: 100px;
        }
        
        .crystal-large {
            width: 150px;
            height: 150px;
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
        }
        
        .structure-tooltip {
            position: relative;
            cursor: pointer;
        }
        
        .structure-tooltip:hover .tooltip-content {
            visibility: visible;
            opacity: 1;
        }
        
        .tooltip-content {
            visibility: hidden;
            width: 200px;
            background-color: rgba(15, 14, 23, 0.9);
            color: #fff;
            text-align: center;
            border-radius: 6px;
            padding: 10px;
            position: absolute;
            z-index: 1;
            bottom: 125%;
            left: 50%;
            margin-left: -100px;
            opacity: 0;
            transition: opacity 0.3s;
            border: 1px solid rgba(0, 245, 255, 0.3);
            box-shadow: 0 0 15px rgba(0, 245, 255, 0.2);
        }
        
        .tooltip-content:after {
            content: "";
            position: absolute;
            top: 100%;
            left: 50%;
            margin-left: -5px;
            border-width: 5px;
            border-style: solid;
            border-color: rgba(15, 14, 23, 0.9) transparent transparent transparent;
        }
        
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        
        ::-webkit-scrollbar-track {
            background: #1e1b32;
        }
        
        ::-webkit-scrollbar-thumb {
            background: linear-gradient(#00f5ff, #bc13fe);
            border-radius: 4px;
        }
        
        ::-webkit-scrollbar-thumb:hover {
            background: linear-gradient(#00c5cc, #9a0fc5);
        }
        
        /* Diffusion Animation Elements */
        .diffusion-container {
            position: relative;
            width: 200px;
            height: 200px;
            margin: 0 auto;
        }
        
        .high-concentration {
            position: absolute;
            width: 60px;
            height: 60px;
            background: radial-gradient(circle, #ff28d1 0%, #bc13fe 70%, transparent 100%);
            border-radius: 50%;
            top: 50%;
            left: 20%;
            transform: translate(-50%, -50%);
            animation: pulse-glow 2s infinite;
        }
        
        .diffusion-particle {
            position: absolute;
            width: 8px;
            height: 8px;
            background-color: #00f5ff;
            border-radius: 50%;
            opacity: 0;
        }
        
        .particle-1 {
            top: 45%;
            left: 30%;
            animation: diffuse 6s infinite;
        }
        
        .particle-2 {
            top: 55%;
            left: 25%;
            animation: diffuse 5s infinite 0.5s;
        }
        
        .particle-3 {
            top: 40%;
            left: 35%;
            animation: diffuse 7s infinite 1s;
        }
        
        .particle-4 {
            top: 60%;
            left: 20%;
            animation: diffuse 5.5s infinite 1.5s;
        }
        
        .particle-5 {
            top: 50%;
            left: 40%;
            animation: diffuse 6.5s infinite 2s;
        }
        
        .low-concentration-area {
            position: absolute;
            width: 120px;
            height: 120px;
            border: 1px dashed rgba(0, 245, 255, 0.3);
            border-radius: 50%;
            top: 50%;
            left: 70%;
            transform: translate(-50%, -50%);
        }
        
        /* Atom Animation */
        .atom {
            position: relative;
            width: 150px;
            height: 150px;
            margin: 0 auto;
        }
        
        .nucleus {
            position: absolute;
            width: 30px;
            height: 30px;
            background: radial-gradient(circle, #ff5e00, #ff28d1);
            border-radius: 50%;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            box-shadow: 0 0 20px #ff28d1;
            z-index: 2;
        }
        
        .electron {
            position: absolute;
            width: 10px;
            height: 10px;
            background-color: #00f5ff;
            border-radius: 50%;
            box-shadow: 0 0 10px #00f5ff;
        }
        
        .orbit {
            position: absolute;
            border: 2px dashed rgba(0, 245, 255, 0.3);
            border-radius: 50%;
        }
        
        .orbit-1 {
            width: 100px;
            height: 100px;
            top: 25px;
            left: 25px;
            animation: atom-spin 15s linear infinite;
        }
        
        .orbit-2 {
            width: 150px;
            height: 80px;
            top: 35px;
            left: 0;
            animation: atom-spin 20s linear infinite reverse;
        }
        
        .electron-1 {
            top: 20px;
            left: 20px;
            animation: electron-orbit 8s linear infinite;
        }
        
        .electron-2 {
            top: 20px;
            right: 20px;
            animation: electron-orbit 8s linear infinite reverse;
        }
        
        .electron-3 {
            bottom: 35px;
            left: 0;
            animation: electron-orbit 10s linear infinite;
        }
        
        /* Animated Underline */
        .animated-underline {
            position: relative;
            display: inline-block;
        }
        
        .animated-underline:after {
            content: '';
            position: absolute;
            width: 100%;
            transform: scaleX(0);
            height: 2px;
            bottom: -4px;
            left: 0;
            background: linear-gradient(90deg, #00f5ff, #bc13fe);
            transform-origin: bottom right;
            transition: transform 0.4s cubic-bezier(0.86, 0, 0.07, 1);
        }
        
        .animated-underline:hover:after {
            transform: scaleX(1);
            transform-origin: bottom left;
        }
        
        /* Neon Text */
        .neon-text {
            text-shadow: 0 0 5px currentColor, 0 0 10px currentColor;
            animation: neon-flicker 1.5s ease-in-out infinite alternate;
        }
        
        /* Wave Animation */
        .wave-animation {
            display: inline-block;
            animation: wave 3s ease-in-out infinite;
            animation-delay: calc(0.1s * var(--i));
        }
        
        /* Body Part Animation */
        .body-part {
            transition: all 0.5s ease;
            cursor: pointer;
        }
        
        .body-part:hover {
            transform: scale(1.1);
            filter: drop-shadow(0 0 10px rgba(0, 245, 255, 0.7));
        }
        
        /* Cyberpunk Button */
        .cyber-button {
            position: relative;
            overflow: hidden;
            border: 2px solid;
            border-image: linear-gradient(45deg, #00f5ff, #bc13fe) 1;
            transition: all 0.3s;
        }
        
        .cyber-button:hover {
            box-shadow: 0 0 15px rgba(0, 245, 255, 0.5), 
                         0 0 30px rgba(188, 19, 254, 0.3);
            transform: translateY(-3px);
        }
        
        .cyber-button:before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 245, 255, 0.4), transparent);
            transition: 0.5s;
        }
        
        .cyber-button:hover:before {
            left: 100%;
        }
    </style>
</head>
<body class="antialiased">
    <!-- Floating Crystal Structures -->
    <div class="fixed top-20 left-10 z-0 animate-float hidden lg:block">
        <svg width="100" height="100" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="crystal text-neon-blue crystal-medium">
            <path d="M12 1L3 5V11C3 16.55 6.84 21.74 12 23C17.16 21.74 21 16.55 21 11V5L12 1Z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
    </div>
    
    <div class="fixed top-1/3 right-20 z-0 animate-float-2 hidden lg:block">
        <svg width="120" height="120" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="crystal text-electric-purple crystal-medium">
            <path d="M12 2L4 7L12 12L20 7L12 2Z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M4 12L12 17L20 12" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M4 17L12 22L20 17" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
    </div>
    
    <div class="fixed bottom-1/4 left-1/4 z-0 animate-float-3 hidden lg:block">
        <svg width="80" height="80" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="crystal text-acid-green crystal-small">
            <path d="M12 2L2 7L12 12L22 7L12 2Z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M2 12L12 17L22 12" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M2 17L12 22L22 17" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
    </div>

    <!-- Sticky Navigation -->
    <nav class="sticky top-0 z-50 bg-deep-space/80 backdrop-blur-md shadow-sm border-b border-electric-purple/30">
        <div class="w-full px-6 py-4">
            <div class="flex justify-between items-center">
                <a href="#" class="text-2xl font-bold text-neon-blue tech-font">MATERIAL<span class="text-hot-pink">X</span></a>
                
                <!-- Mobile Menu Button -->
                <button id="menu-toggle" class="md:hidden text-gray-400 hover:text-white focus:outline-none">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                    </svg>
                </button>
                
                <!-- Desktop Menu -->
                <div class="hidden md:flex space-x-8">
                    <a href="#introduction" class="text-gray-400 hover:text-neon-blue font-medium animated-underline">Introduction</a>
                    <a href="#importance" class="text-gray-400 hover:text-neon-blue font-medium animated-underline">Why It Matters</a>
                    <a href="#diffusion" class="text-gray-400 hover:text-neon-blue font-medium animated-underline">Diffusion</a>
                    <a href="#careers" class="text-gray-400 hover:text-neon-blue font-medium animated-underline">Careers</a>
                    <a href="#future" class="text-gray-400 hover:text-neon-blue font-medium animated-underline">Future</a>
                </div>
            </div>
            
            <!-- Mobile Menu -->
            <div id="mobile-menu" class="hidden md:hidden mt-4 pb-4 space-y-2">
                <a href="#introduction" class="block py-2 text-gray-400 hover:text-neon-blue">Introduction</a>
                <a href="#importance" class="block py-2 text-gray-400 hover:text-neon-blue">Why It Matters</a>
                <a href="#diffusion" class="block py-2 text-gray-400 hover:text-neon-blue">Diffusion</a>
                <a href="#careers" class="block py-2 text-gray-400 hover:text-neon-blue">Careers</a>
                <a href="#future" class="block py-2 text-gray-400 hover:text-neon-blue">Future</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <header class="relative h-screen flex items-center justify-center overflow-hidden">
        <!-- Background Video -->
        <video autoplay muted loop class="absolute inset-0 w-full h-full object-cover z-0">
            <source src="https://assets.mixkit.co/videos/preview/mixkit-close-up-of-a-blue-circuit-board-12206-large.mp4" type="video/mp4">
        </video>
        <div class="absolute inset-0 hero-gradient z-1"></div>
        
        <!-- Animated Atom -->
        <div class="absolute top-1/4 left-1/4 z-0 hidden lg:block">
            <div class="atom">
                <div class="nucleus animate-pulse-glow"></div>
                <div class="orbit orbit-1"></div>
                <div class="orbit orbit-2"></div>
                <div class="electron electron-1"></div>
                <div class="electron electron-2"></div>
                <div class="electron electron-3"></div>
            </div>
        </div>
        
        <div class="relative z-10 px-6 text-center text-white w-full" data-aos="fade-up">
            <div class="max-w-6xl mx-auto">
                <h1 class="text-5xl md:text-7xl font-bold mb-6 leading-tight">
                    <span class="text-neon-blue neon-text">MATERIALS</span> 
                    <span class="text-electric-purple neon-text">ENGINEERING</span>
                </h1>
                <p class="text-xl md:text-2xl mb-8 max-w-2xl mx-auto tech-font">DESIGNING THE ATOMIC FOUNDATIONS OF TOMORROW</p>
                <div class="flex flex-col sm:flex-row justify-center gap-4">
                    <a href="#introduction" class="cyber-button bg-transparent text-white font-semibold px-8 py-3 rounded-none">
                        EXPLORE NOW
                    </a>
                    <a href="#careers" class="cyber-button bg-transparent text-white font-semibold px-8 py-3 rounded-none border-electric-purple text-electric-purple">
                        CAREER PATHS
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
    <section id="introduction" class="py-20 bg-deep-space w-full relative overflow-hidden">
        <!-- Background crystal structures -->
        <div class="absolute top-20 right-10 z-0 animate-float hidden lg:block">
            <svg width="100" height="100" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="crystal text-neon-blue/20 crystal-medium">
                <path d="M12 1L3 5V11C3 16.55 6.84 21.74 12 23C17.16 21.74 21 16.55 21 11V5L12 1Z" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
        </div>
        
        <div class="w-full px-6">
            <div class="text-center mb-16" data-aos="fade-up">
                <span class="text-neon-blue font-semibold tech-font tracking-widest">THE SCIENCE OF MATERIALS</span>
                <h2 class="text-3xl md:text-4xl font-bold mb-4 mt-2">What is <span class="text-electric-purple">Materials Engineering</span>?</h2>
                <div class="w-20 h-1 bg-gradient-to-r from-neon-blue to-electric-purple mx-auto mb-6"></div>
                <p class="text-gray-400 max-w-3xl mx-auto">Materials Engineering is the interdisciplinary field that combines physics, chemistry, and engineering to design, develop, and optimize materials for real-world applications.</p>
            </div>
            
            <div class="grid md:grid-cols-3 gap-8 max-w-6xl mx-auto">
                <div class="glass-card p-8 rounded-xl hover-scale" data-aos="fade-up">
                    <div class="text-neon-blue text-4xl mb-4">
                        <i class="fas fa-atom animate-spin-slow"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-white">Atomic-Level Design</h3>
                    <p class="text-gray-400">Manipulating materials at the nanoscale to achieve desired properties like strength, conductivity, or flexibility.</p>
                </div>
                
                <div class="glass-card p-8 rounded-xl hover-scale" data-aos="fade-up" data-aos-delay="100">
                    <div class="text-electric-purple text-4xl mb-4">
                        <i class="fas fa-microscope animate-pulse-glow"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-white">Microstructure Analysis</h3>
                    <p class="text-gray-400">Studying crystal structures, grain boundaries, and defects to predict material behavior.</p>
                </div>
                
                <div class="glass-card p-8 rounded-xl hover-scale" data-aos="fade-up" data-aos-delay="200">
                    <div class="text-hot-pink text-4xl mb-4">
                        <i class="fas fa-industry animate-wave"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-white">Industrial Application</h3>
                    <p class="text-gray-400">From aerospace alloys to biomedical implants, materials engineering powers modern industry.</p>
                </div>
            </div>
            
            <!-- Crystal Structures Tooltips -->
            <div class="mt-16 flex justify-center space-x-8" data-aos="fade-up">
                <div class="structure-tooltip">
                    <svg width="80" height="80" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="crystal text-neon-blue hover:text-neon-blue transition-colors animate-pulse-glow">
                        <path d="M12 1L3 5V11C3 16.55 6.84 21.74 12 23C17.16 21.74 21 16.55 21 11V5L12 1Z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                    <div class="tooltip-content">
                        <h4 class="font-bold mb-1">FCC Structure</h4>
                        <p class="text-sm">Face-Centered Cubic (e.g., Aluminum, Copper)</p>
                    </div>
                </div>
                
                <div class="structure-tooltip">
                    <svg width="80" height="80" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="crystal text-electric-purple hover:text-electric-purple transition-colors animate-pulse-glow">
                        <path d="M12 2L4 7L12 12L20 7L12 2Z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                        <path d="M4 12L12 17L20 12" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                        <path d="M4 17L12 22L20 17" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                    <div class="tooltip-content">
                        <h4 class="font-bold mb-1">BCC Structure</h4>
                        <p class="text-sm">Body-Centered Cubic (e.g., Iron, Tungsten)</p>
                    </div>
                </div>
                
                <div class="structure-tooltip">
                    <svg width="80" height="80" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="crystal text-acid-green hover:text-acid-green transition-colors animate-pulse-glow">
                        <path d="M12 2L2 7L12 12L22 7L12 2Z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                        <path d="M2 12L12 17L22 12" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                        <path d="M2 17L12 22L22 17" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                    <div class="tooltip-content">
                        <h4 class="font-bold mb-1">HCP Structure</h4>
                        <p class="text-sm">Hexagonal Close-Packed (e.g., Titanium, Zinc)</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Why It Matters Section -->
    <section id="importance" class="py-20 bg-gradient-to-br from-cosmic-purple/30 to-deep-space w-full relative overflow-hidden">
        <!-- Background crystal -->
        <div class="absolute bottom-20 left-10 z-0 animate-float-3 hidden lg:block">
            <svg width="120" height="120" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="crystal text-neon-blue/20 crystal-medium">
                <path d="M12 2L4 7L12 12L20 7L12 2Z" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M4 12L12 17L20 12" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M4 17L12 22L20 17" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
        </div>
        
        <div class="w-full px-6">
            <div class="text-center mb-16" data-aos="fade-up">
                <span class="text-neon-blue font-semibold tech-font tracking-widest">THE IMPACT</span>
                <h2 class="text-3xl md:text-4xl font-bold mb-4 mt-2">Why Materials Engineering <span class="text-hot-pink">Matters</span></h2>
                <div class="w-20 h-1 bg-gradient-to-r from-neon-blue to-electric-purple mx-auto mb-6"></div>
                <p class="text-gray-400 max-w-3xl mx-auto">Materials innovation drives technological progress across every industry.</p>
            </div>
            
            <div class="grid md:grid-cols-2 gap-10 items-center max-w-6xl mx-auto">
                <div class="space-y-6" data-aos="fade-right">
                    <div class="flex items-start glass-card p-5 rounded-xl hover-scale">
                        <div class="bg-neon-blue/10 p-3 rounded-full mr-4 text-neon-blue animate-pulse-glow">
                            <i class="fas fa-space-shuttle"></i>
                        </div>
                        <div>
                            <h3 class="text-xl font-semibold mb-2 text-white">Space Exploration</h3>
                            <p class="text-gray-400">Heat-resistant ceramics and lightweight alloys enable spacecraft to survive extreme conditions.</p>
                        </div>
                    </div>
                    
                    <div class="flex items-start glass-card p-5 rounded-xl hover-scale">
                        <div class="bg-hot-pink/10 p-3 rounded-full mr-4 text-hot-pink animate-pulse-glow">
                            <i class="fas fa-heartbeat"></i>
                        </div>
                        <div>
                            <h3 class="text-xl font-semibold mb-2 text-white">Medical Breakthroughs</h3>
                            <p class="text-gray-400">Biocompatible materials for implants, prosthetics, and drug delivery systems.</p>
                        </div>
                    </div>
                    
                    <div class="flex items-start glass-card p-5 rounded-xl hover-scale">
                        <div class="bg-acid-green/10 p-3 rounded-full mr-4 text-acid-green animate-pulse-glow">
                            <i class="fas fa-bolt"></i>
                        </div>
                        <div>
                            <h3 class="text-xl font-semibold mb-2 text-white">Renewable Energy</h3>
                            <p class="text-gray-400">High-efficiency solar cells, advanced batteries, and durable wind turbine blades.</p>
                        </div>
                    </div>
                </div>
                
                <div data-aos="fade-left">
                    <img src="https://images.unsplash.com/photo-1581094795054-d5a3f1db2a9a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
                         alt="Materials in aerospace" 
                         class="rounded-xl shadow-lg w-full h-auto object-cover border-2 border-electric-purple/50">
                </div>
            </div>
        </div>
    </section>

    <!-- Diffusion Animation Section -->
    <section id="diffusion" class="py-20 bg-deep-space w-full relative overflow-hidden border-t border-electric-purple/30">
        <div class="w-full px-6">
            <div class="text-center mb-16" data-aos="fade-up">
                <span class="text-neon-blue font-semibold tech-font tracking-widest">MATERIALS SCIENCE</span>
                <h2 class="text-3xl md:text-4xl font-bold mb-4 mt-2">Diffusion in <span class="text-acid-green">Solids</span></h2>
                <div class="w-20 h-1 bg-gradient-to-r from-neon-blue to-electric-purple mx-auto mb-6"></div>
                <p class="text-gray-400 max-w-3xl mx-auto">The process of mass transport by atomic motion from high concentration to low concentration.</p>
            </div>
            
            <div class="grid md:grid-cols-2 gap-10 items-center max-w-6xl mx-auto">
                <div data-aos="fade-right">
                    <div class="diffusion-container">
                        <div class="high-concentration"></div>
                        <div class="diffusion-particle particle-1"></div>
                        <div class="diffusion-particle particle-2"></div>
                        <div class="diffusion-particle particle-3"></div>
                        <div class="diffusion-particle particle-4"></div>
                        <div class="diffusion-particle particle-5"></div>
                        <div class="low-concentration-area"></div>
                    </div>
                </div>
                
                <div class="space-y-6" data-aos="fade-left">
                    <div class="glass-card p-6 rounded-xl">
                        <h3 class="text-xl font-semibold mb-3 text-neon-blue">Fick's First Law</h3>
                        <p class="text-gray-400 mb-4">The diffusion flux is proportional to the concentration gradient:</p>
                        <div class="bg-deep-space border border-electric-purple/30 p-4 rounded-lg mb-4">
                            <p class="text-center text-white font-mono">J = -D (∂C/∂x)</p>
                        </div>
                        <p class="text-gray-400">Where J is the diffusion flux, D is the diffusion coefficient, and ∂C/∂x is the concentration gradient.</p>
                    </div>
                    
                    <div class="glass-card p-6 rounded-xl">
                        <h3 class="text-xl font-semibold mb-3 text-electric-purple">Applications</h3>
                        <ul class="space-y-3 text-gray-400">
                            <li class="flex items-start">
                                <span class="text-hot-pink mr-2">•</span>
                                <span>Carburization of steel surfaces</span>
                            </li>
                            <li class="flex items-start">
                                <span class="text-hot-pink mr-2">•</span>
                                <span>Doping in semiconductor fabrication</span>
                            </li>
                            <li class="flex items-start">
                                <span class="text-hot-pink mr-2">•</span>
                                <span>Fuel cell operation</span>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Career Opportunities Section -->
    <section id="careers" class="py-20 bg-gradient-to-br from-deep-space to-cosmic-purple/50 w-full relative overflow-hidden border-t border-electric-purple/30">
        <!-- Background crystal -->
        <div class="absolute top-1/3 right-20 z-0 animate-float-2 hidden lg:block">
            <svg width="100" height="100" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="crystal text-electric-purple/20 crystal-medium">
                <path d="M12 2L2 7L12 12L22 7L12 2Z" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M2 12L12 17L22 12" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M2 17L12 22L22 17" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
        </div>
        
        <div class="w-full px-6">
            <div class="text-center mb-16" data-aos="fade-up">
                <span class="text-neon-blue font-semibold tech-font tracking-widest">CAREER PATHS</span>
                <h2 class="text-3xl md:text-4xl font-bold mb-4 mt-2">Where Materials Engineers <span class="text-hot-pink">Work</span></h2>
                <div class="w-20 h-1 bg-gradient-to-r from-neon-blue to-electric-purple mx-auto mb-6"></div>
                <p class="text-gray-400 max-w-3xl mx-auto">Diverse industries rely on materials expertise for innovation.</p>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6 max-w-6xl mx-auto">
                <div class="glass-card rounded-xl p-6 hover-scale" data-aos="flip-left">
                    <div class="bg-neon-blue/10 w-16 h-16 rounded-xl flex items-center justify-center mb-4 mx-auto text-neon-blue animate-pulse-glow">
                        <i class="fas fa-plane text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2 text-white">Aerospace</h3>
                    <p class="text-gray-400 text-center">Lightweight alloys & heat shields for ISRO, NASA, and private space companies.</p>
                </div>
                
                <div class="glass-card rounded-xl p-6 hover-scale" data-aos="flip-left" data-aos-delay="100">
                    <div class="bg-electric-purple/10 w-16 h-16 rounded-xl flex items-center justify-center mb-4 mx-auto text-electric-purple animate-pulse-glow">
                        <i class="fas fa-car text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2 text-white">Automotive</h3>
                    <p class="text-gray-400 text-center">Advanced composites for electric vehicles at Tesla, Tata, and Mahindra.</p>
                </div>
                
                <div class="glass-card rounded-xl p-6 hover-scale" data-aos="flip-left" data-aos-delay="200">
                    <div class="bg-hot-pink/10 w-16 h-16 rounded-xl flex items-center justify-center mb-4 mx-auto text-hot-pink animate-pulse-glow">
                        <i class="fas fa-heart text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2 text-white">Biomedical</h3>
                    <p class="text-gray-400 text-center">Biocompatible implants and surgical tools for medical advancements.</p>
                </div>
                
                <div class="glass-card rounded-xl p-6 hover-scale" data-aos="flip-left" data-aos-delay="300">
                    <div class="bg-acid-green/10 w-16 h-16 rounded-xl flex items-center justify-center mb-4 mx-auto text-acid-green animate-pulse-glow">
                        <i class="fas fa-bolt text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2 text-white">Energy</h3>
                    <p class="text-gray-400 text-center">Solar cells, batteries, and nuclear materials for sustainable power.</p>
                </div>
            </div>
            
            <!-- Body Parts Animation Section -->
            <div class="mt-16 text-center" data-aos="fade-up">
                <h3 class="text-2xl font-semibold mb-8 text-white">Materials in the <span class="text-neon-blue">Human Body</span></h3>
                <div class="flex flex-wrap justify-center gap-8 max-w-4xl mx-auto">
                    <div class="body-part" data-aos="zoom-in">
                        <div class="bg-neon-blue/10 p-4 rounded-full w-24 h-24 flex items-center justify-center mx-auto mb-2">
                            <i class="fas fa-bone text-3xl text-neon-blue"></i>
                        </div>
                        <p class="text-gray-400">Bone Implants</p>
                    </div>
                    <div class="body-part" data-aos="zoom-in" data-aos-delay="100">
                        <div class="bg-electric-purple/10 p-4 rounded-full w-24 h-24 flex items-center justify-center mx-auto mb-2">
                            <i class="fas fa-heart text-3xl text-electric-purple"></i>
                        </div>
                        <p class="text-gray-400">Heart Valves</p>
                    </div>
                    <div class="body-part" data-aos="zoom-in" data-aos-delay="200">
                        <div class="bg-hot-pink/10 p-4 rounded-full w-24 h-24 flex items-center justify-center mx-auto mb-2">
                            <i class="fas fa-brain text-3xl text-hot-pink"></i>
                        </div>
                        <p class="text-gray-400">Neural Interfaces</p>
                    </div>
                    <div class="body-part" data-aos="zoom-in" data-aos-delay="300">
                        <div class="bg-acid-green/10 p-4 rounded-full w-24 h-24 flex items-center justify-center mx-auto mb-2">
                            <i class="fas fa-eye text-3xl text-acid-green"></i>
                        </div>
                        <p class="text-gray-400">Artificial Corneas</p>
                    </div>
                    <div class="body-part" data-aos="zoom-in" data-aos-delay="400">
                        <div class="bg-vivid-orange/10 p-4 rounded-full w-24 h-24 flex items-center justify-center mx-auto mb-2">
                            <i class="fas fa-tooth text-3xl text-vivid-orange"></i>
                        </div>
                        <p class="text-gray-400">Dental Implants</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Elon Musk Tweets Section -->
    <section class="py-20 bg-deep-space w-full border-t border-electric-purple/30">
        <div class="w-full px-6">
            <div class="text-center mb-16" data-aos="fade-up">
                <span class="text-neon-blue font-semibold tech-font tracking-widest">INDUSTRY INSIGHTS</span>
                <h2 class="text-3xl md:text-4xl font-bold mb-4 mt-2">What <span class="text-electric-purple">Leaders</span> Say</h2>
                <div class="w-20 h-1 bg-gradient-to-r from-neon-blue to-electric-purple mx-auto mb-6"></div>
                <p class="text-gray-400 max-w-3xl mx-auto">Elon Musk on the critical role of materials science in innovation.</p>
            </div>
            
            <div class="grid md:grid-cols-2 gap-8 max-w-5xl mx-auto">
                <!-- Tweet 1 -->
                <div class="glass-card rounded-xl overflow-hidden hover-scale" data-aos="zoom-in">
                    <div class="p-6">
                        <div class="flex items-start">
                            <img src="https://pbs.twimg.com/profile_images/1683325380441128960/yRsRRjGO_400x400.jpg" 
                                 alt="Elon Musk" 
                                 class="w-14 h-14 rounded-full mr-4 border-2 border-neon-blue">
                            <div>
                                <div class="flex items-center mb-2">
                                    <h3 class="text-lg font-bold mr-2 text-white">Elon Musk</h3>
                                    <span class="text-gray-400 text-sm">@elonmusk</span>
                                </div>
                                <p class="text-gray-200 mb-4">"The fundamental limitation in rocket design is materials science. If we had materials that could withstand higher temperatures, we could make rockets dramatically more efficient."</p>
                                <div class="flex items-center text-gray-400 text-sm">
                                    <i class="fas fa-retweet mr-2"></i>
                                    <span class="mr-4">24.5K</span>
                                    <i class="fas fa-heart mr-2 text-hot-pink"></i>
                                    <span>128.7K</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="bg-deep-space/50 px-6 py-3 flex items-center text-sm border-t border-electric-purple/30">
                        <i class="fab fa-twitter text-neon-blue mr-2"></i>
                        <span>June 15, 2022</span>
                    </div>
                </div>
                
                <!-- Tweet 2 -->
                <div class="glass-card rounded-xl overflow-hidden hover-scale" data-aos="zoom-in" data-aos-delay="100">
                    <div class="p-6">
                        <div class="flex items-start">
                            <img src="https://pbs.twimg.com/profile_images/1683325380441128960/yRsRRjGO_400x400.jpg" 
                                 alt="Elon Musk" 
                                 class="w-14 h-14 rounded-full mr-4 border-2 border-neon-blue">
                            <div>
                                <div class="flex items-center mb-2">
                                    <h3 class="text-lg font-bold mr-2 text-white">Elon Musk</h3>
                                    <span class="text-gray-400 text-sm">@elonmusk</span>
                                </div>
                                <p class="text-gray-200 mb-4">"Battery technology is fundamentally a materials science problem. The energy density improvements we need for sustainable transport depend on new cathode/anode materials."</p>
                                <div class="flex items-center text-gray-400 text-sm">
                                    <i class="fas fa-retweet mr-2"></i>
                                    <span class="mr-4">18.2K</span>
                                    <i class="fas fa-heart mr-2 text-hot-pink"></i>
                                    <span>95.3K</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="bg-deep-space/50 px-6 py-3 flex items-center text-sm border-t border-electric-purple/30">
                        <i class="fab fa-twitter text-neon-blue mr-2"></i>
                        <span>March 8, 2023</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Future Trends Section -->
    <section id="future" class="py-20 bg-gradient-to-br from-deep-space to-cosmic-purple/70 w-full relative overflow-hidden border-t border-electric-purple/30">
        <!-- Background crystal -->
        <div class="absolute bottom-20 right-20 z-0 animate-float hidden lg:block">
            <svg width="120" height="120" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="crystal text-electric-purple/20 crystal-medium">
                <path d="M12 2L2 7L12 12L22 7L12 2Z" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M2 12L12 17L22 12" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M2 17L12 22L22 17" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
        </div>
        
        <div class="w-full px-6">
            <div class="text-center mb-16" data-aos="fade-up">
                <span class="text-neon-blue font-semibold tech-font tracking-widest">TOMORROW'S MATERIALS</span>
                <h2 class="text-3xl md:text-4xl font-bold mb-4 mt-2">The <span class="text-acid-green">Future</span> of Materials Engineering</h2>
                <div class="w-20 h-1 bg-gradient-to-r from-neon-blue to-electric-purple mx-auto mb-6"></div>
                <p class="text-gray-400 max-w-3xl mx-auto">Cutting-edge innovations that will redefine industries.</p>
            </div>
            
            <div class="grid md:grid-cols-3 gap-8 max-w-6xl mx-auto">
                <div class="glass-card p-6 rounded-xl hover-scale" data-aos="fade-up">
                    <img src="https://images.unsplash.com/photo-1581094794329-c8112a89af12?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
                         alt="Nanomaterials" 
                         class="rounded-lg w-full h-48 object-cover mb-4 border border-neon-blue/30">
                    <h3 class="text-xl font-semibold mb-2 text-neon-blue">Nanomaterials</h3>
                    <p class="text-gray-400">Graphene, quantum dots, and carbon nanotubes enabling breakthroughs in electronics and medicine.</p>
                </div>
                
                <div class="glass-card p-6 rounded-xl hover-scale" data-aos="fade-up" data-aos-delay="100">
                    <img src="https://images.unsplash.com/photo-1575505586569-646b2ca898fc?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2086&q=80" 
                         alt="Biomaterials" 
                         class="rounded-lg w-full h-48 object-cover mb-4 border border-hot-pink/30">
                    <h3 class="text-xl font-semibold mb-2 text-hot-pink">Biomaterials</h3>
                    <p class="text-gray-400">3D-printed organs, bioabsorbable implants, and smart drug delivery systems.</p>
                </div>
                
                <div class="glass-card p-6 rounded-xl hover-scale" data-aos="fade-up" data-aos-delay="200">
                    <img src="https://images.unsplash.com/photo-1508514177221-188b1cf16e9d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2072&q=80" 
                         alt="Sustainable materials" 
                         class="rounded-lg w-full h-48 object-cover mb-4 border border-acid-green/30">
                    <h3 class="text-xl font-semibold mb-2 text-acid-green">Sustainable Materials</h3>
                    <p class="text-gray-400">Self-healing concrete, biodegradable plastics, and energy-efficient phase-change materials.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Call to Action -->
    <section class="py-20 bg-gradient-to-r from-neon-blue to-electric-purple text-white w-full">
        <div class="w-full px-6 text-center">
            <div class="max-w-4xl mx-auto" data-aos="zoom-in">
                <h2 class="text-3xl md:text-4xl font-bold mb-6">Ready to Explore <span class="text-deep-space">Materials Engineering</span>?</h2>
                <p class="text-xl mb-8 tech-font">JOIN THE NEXT GENERATION OF INNOVATORS</p>
                
                <div class="flex flex-col sm:flex-row justify-center gap-4">
                    <a href="#" class="cyber-button bg-deep-space text-white font-semibold px-8 py-3 rounded-none border-neon-blue">
                        DOWNLOAD CAREER GUIDE
                    </a>
                    <a href="#" class="cyber-button bg-deep-space text-white font-semibold px-8 py-3 rounded-none border-hot-pink text-hot-pink">
                        SPEAK TO AN ADVISOR
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-deep-space text-gray-400 py-12 w-full border-t border-electric-purple/30">
        <div class="w-full px-6">
            <div class="grid md:grid-cols-4 gap-10 max-w-6xl mx-auto">
                <div>
                    <h3 class="text-white text-lg font-semibold mb-4 tech-font">MATERIAL<span class="text-hot-pink">X</span></h3>
                    <p class="mb-4">Empowering future materials engineers through education and innovation.</p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-neon-blue">
                            <i class="fab fa-twitter text-xl"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-neon-blue">
                            <i class="fab fa-linkedin text-xl"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-neon-blue">
                            <i class="fab fa-youtube text-xl"></i>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h3 class="text-white text-lg font-semibold mb-4">Quick Links</h3>
                    <ul class="space-y-2">
                        <li><a href="#introduction" class="hover:text-neon-blue">Introduction</a></li>
                        <li><a href="#importance" class="hover:text-neon-blue">Why It Matters</a></li>
                        <li><a href="#diffusion" class="hover:text-neon-blue">Diffusion</a></li>
                        <li><a href="#careers" class="hover:text-neon-blue">Careers</a></li>
                        <li><a href="#future" class="hover:text-neon-blue">Future Trends</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-white text-lg font-semibold mb-4">Resources</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="hover:text-neon-blue">Blog</a></li>
                        <li><a href="#" class="hover:text-neon-blue">Research Papers</a></li>
                        <li><a href="#" class="hover:text-neon-blue">Webinars</a></li>
                        <li><a href="#" class="hover:text-neon-blue">FAQ</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-white text-lg font-semibold mb-4">Contact</h3>
                    <ul class="space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-map-marker-alt mt-1 mr-3 text-neon-blue"></i>
                            <span>123 Science Park, Bangalore, IN 560001</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-envelope mr-3 text-neon-blue"></i>
                            <span>contact@materialx.edu.in</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-phone-alt mr-3 text-neon-blue"></i>
                            <span>+91 9876543210</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-10 pt-6 flex flex-col md:flex-row justify-between items-center max-w-6xl mx-auto">
                <p>&copy; 2023 MATERIALX. All rights reserved.</p>
                <div class="mt-4 md:mt-0">
                    <a href="#" class="text-sm hover:text-neon-blue mr-4">Privacy Policy</a>
                    <a href="#" class="text-sm hover:text-neon-blue">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- Back to Top Button -->
    <button id="back-to-top" class="fixed bottom-8 right-8 bg-neon-blue text-deep-space w-12 h-12 rounded-full shadow-lg hidden items-center justify-center hover:bg-electric-purple transition duration-300">
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
        
        // Wave animation for text
        const waveText = document.querySelectorAll('.wave-animation');
        waveText.forEach((el, i) => {
            el.style.setProperty('--i', i);
        });
        
        // Body part hover animations
        const bodyParts = document.querySelectorAll('.body-part');
        bodyParts.forEach(part => {
            part.addEventListener('mouseenter', () => {
                const icon = part.querySelector('i');
                icon.classList.add('animate-vibrate');
            });
            
            part.addEventListener('mouseleave', () => {
                const icon = part.querySelector('i');
                icon.classList.remove('animate-vibrate');
            });
        });
    </script>
</body>
</html>
