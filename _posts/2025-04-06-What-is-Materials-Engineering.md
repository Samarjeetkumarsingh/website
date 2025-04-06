<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>What is Materials Engineering? | Future of Innovation</title>
    <meta name="description" content="Discover the fascinating world of Materials Engineering - its importance, career opportunities, and future trends shaping our world.">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- AOS Animation Library -->
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    
    <style>
        :root {
            --primary: #3b82f6;
            --secondary: #10b981;
            --dark: #1e293b;
            --light: #f8fafc;
        }
        
        body {
         width: 100%;
  margin: 0;
  padding: 0;
            font-family: 'Inter', sans-serif;
            scroll-behavior: smooth;
        }
        
        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
        }
        
        .hero-gradient {
            background: linear-gradient(135deg, rgba(59,130,246,0.8) 0%, rgba(16,185,129,0.8) 100%);
        }
        
        .card-hover {
            transition: all 0.3s ease;
        }
        
        .card-hover:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .testimonial-carousel {
            scroll-snap-type: x mandatory;
        }
        
        .testimonial-slide {
            scroll-snap-align: start;
        }
        
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        
        ::-webkit-scrollbar-track {
            background: #f1f1f1;
        }
        
        ::-webkit-scrollbar-thumb {
            background: var(--primary);
            border-radius: 4px;
        }
        
        ::-webkit-scrollbar-thumb:hover {
            background: #2563eb;
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800">
    <!-- Sticky Navigation -->
    <nav class="sticky top-0 z-50 bg-white shadow-md">
        <div style="width: 100%; margin: 0; padding: 0;">
            <div class="flex justify-between items-center">
                <a href="#" class="text-2xl font-bold text-blue-500">Material<span class="text-emerald-500">Science</span></a>
                
                <!-- Mobile menu button -->
                <div class="md:hidden">
                    <button id="menu-toggle" class="text-gray-600 hover:text-blue-500 focus:outline-none">
                        <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                        </svg>
                    </button>
                </div>
                
                <!-- Desktop Menu -->
                <div class="hidden md:flex space-x-8">
                    <a href="#introduction" class="text-gray-700 hover:text-blue-500 font-medium">Introduction</a>
                    <a href="#importance" class="text-gray-700 hover:text-blue-500 font-medium">Why It Matters</a>
                    <a href="#benefits" class="text-gray-700 hover:text-blue-500 font-medium">Benefits</a>
                    <a href="#careers" class="text-gray-700 hover:text-blue-500 font-medium">Careers</a>
                    <a href="#gate" class="text-gray-700 hover:text-blue-500 font-medium">GATE (MT)</a>
                    <a href="#future" class="text-gray-700 hover:text-blue-500 font-medium">Future</a>
                </div>
            </div>
            
            <!-- Mobile Menu -->
            <div id="mobile-menu" class="hidden md:hidden mt-4 pb-4">
                <a href="#introduction" class="block py-2 text-gray-700 hover:text-blue-500">Introduction</a>
                <a href="#importance" class="block py-2 text-gray-700 hover:text-blue-500">Why It Matters</a>
                <a href="#benefits" class="block py-2 text-gray-700 hover:text-blue-500">Benefits</a>
                <a href="#careers" class="block py-2 text-gray-700 hover:text-blue-500">Careers</a>
                <a href="#gate" class="block py-2 text-gray-700 hover:text-blue-500">GATE (MT)</a>
                <a href="#future" class="block py-2 text-gray-700 hover:text-blue-500">Future</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <header class="relative h-screen flex items-center justify-center overflow-hidden">
        <div class="absolute inset-0">
            <img src="https://images.unsplash.com/photo-1635070041078-e363dbe005cb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
                 alt="Materials Engineering" 
                 class="w-full h-full object-cover">
            <div class="absolute inset-0 hero-gradient"></div>
        </div>
        
        <div class="relative z-10 px-6 text-center text-white max-w-4xl" data-aos="fade-up">
            <h1 class="text-4xl md:text-6xl font-bold mb-6">Materials Engineering</h1>
            <p class="text-xl md:text-2xl mb-8">The Foundation of Modern Innovation</p>
            <a href="#introduction" class="inline-block bg-white text-blue-600 font-semibold px-8 py-3 rounded-full hover:bg-gray-100 transition duration-300 transform hover:scale-105">
                Explore More
            </a>
        </div>
        
        <a href="#introduction" class="absolute bottom-10 left-1/2 transform -translate-x-1/2 animate-bounce">
            <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
            </svg>
        </a>
    </header>

    <!-- Introduction Section -->
    <section id="introduction" class="py-20 bg-white">
        <div style="width: 100%; margin: 0; padding: 0;">
            <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">What is Materials Engineering?</h2>
                <div class="w-20 h-1 bg-blue-500 mx-auto mb-6"></div>
                <p class="text-gray-600 max-w-3xl mx-auto">Materials Engineering is the interdisciplinary field that combines principles from physics, chemistry, and engineering to design, develop, and improve materials that shape our modern world.</p>
            </div>
            
            <div class="grid md:grid-cols-3 gap-10">
                <div class="bg-gray-50 p-8 rounded-lg shadow-md card-hover" data-aos="fade-up" data-aos-delay="100">
                    <div class="text-blue-500 text-4xl mb-4">
                        <i class="fas fa-atom"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3">Atomic Understanding</h3>
                    <p class="text-gray-600">Materials engineers study materials at atomic and molecular levels to understand their properties and behavior.</p>
                </div>
                
                <div class="bg-gray-50 p-8 rounded-lg shadow-md card-hover" data-aos="fade-up" data-aos-delay="200">
                    <div class="text-blue-500 text-4xl mb-4">
                        <i class="fas fa-cogs"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3">Application Focused</h3>
                    <p class="text-gray-600">They apply this knowledge to develop new materials and improve existing ones for specific applications.</p>
                </div>
                
                <div class="bg-gray-50 p-8 rounded-lg shadow-md card-hover" data-aos="fade-up" data-aos-delay="300">
                    <div class="text-blue-500 text-4xl mb-4">
                        <i class="fas fa-industry"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3">Industry Impact</h3>
                    <p class="text-gray-600">From aerospace to biomedical devices, materials engineering touches nearly every industry.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Why It Matters Section -->
    <section id="importance" class="py-20 bg-gray-50">
        <div style="width: 100%; margin: 0; padding: 0;">
            <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">Why Materials Engineering Matters</h2>
                <div class="w-20 h-1 bg-emerald-500 mx-auto mb-6"></div>
                <p class="text-gray-600 max-w-3xl mx-auto">Materials engineering drives innovation across industries and solves some of humanity's most pressing challenges.</p>
            </div>
            
            <div class="grid md:grid-cols-2 gap-10 items-center">
                <div class="space-y-6" data-aos="fade-right">
                    <div class="flex items-start">
                        <div class="bg-emerald-100 p-3 rounded-full mr-4">
                            <i class="fas fa-space-shuttle text-emerald-600"></i>
                        </div>
                        <div>
                            <h3 class="text-xl font-semibold mb-2">Space Exploration</h3>
                            <p class="text-gray-600">Lightweight, heat-resistant materials enable spacecraft to withstand extreme conditions.</p>
                        </div>
                    </div>
                    
                    <div class="flex items-start">
                        <div class="bg-blue-100 p-3 rounded-full mr-4">
                            <i class="fas fa-heartbeat text-blue-600"></i>
                        </div>
                        <div>
                            <h3 class="text-xl font-semibold mb-2">Medical Breakthroughs</h3>
                            <p class="text-gray-600">Biocompatible materials revolutionize implants, prosthetics, and drug delivery systems.</p>
                        </div>
                    </div>
                    
                    <div class="flex items-start">
                        <div class="bg-purple-100 p-3 rounded-full mr-4">
                            <i class="fas fa-bolt text-purple-600"></i>
                        </div>
                        <div>
                            <h3 class="text-xl font-semibold mb-2">Renewable Energy</h3>
                            <p class="text-gray-600">Advanced materials improve solar cells, batteries, and wind turbine efficiency.</p>
                        </div>
                    </div>
                    
                    <div class="flex items-start">
                        <div class="bg-yellow-100 p-3 rounded-full mr-4">
                            <i class="fas fa-car text-yellow-600"></i>
                        </div>
                        <div>
                            <h3 class="text-xl font-semibold mb-2">Transportation</h3>
                            <p class="text-gray-600">Stronger, lighter materials make vehicles more fuel-efficient and safer.</p>
                        </div>
                    </div>
                </div>
                
                <div data-aos="fade-left">
                    <img src="https://images.unsplash.com/photo-1451187580459-43490279c0fa?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2072&q=80" 
                         alt="Materials applications" 
                         class="rounded-lg shadow-xl w-full">
                </div>
            </div>
        </div>
    </section>

    <!-- Benefits Section -->
    <section id="benefits" class="py-20 bg-white">
        <div style="width: 100%; margin: 0; padding: 0;">
            <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">Benefits of Studying Materials Engineering</h2>
                <div class="w-20 h-1 bg-blue-500 mx-auto mb-6"></div>
                <p class="text-gray-600 max-w-3xl mx-auto">A degree in Materials Engineering opens doors to diverse opportunities across multiple sectors.</p>
            </div>
            
            <div class="grid md:grid-cols-3 gap-8">
                <div class="relative group" data-aos="zoom-in">
                    <div class="absolute -inset-1 bg-gradient-to-r from-blue-500 to-emerald-500 rounded-lg blur opacity-25 group-hover:opacity-100 transition duration-200"></div>
                    <div class="relative bg-white h-full p-6 rounded-lg shadow-md">
                        <h3 class="text-xl font-semibold mb-3 text-blue-600">Interdisciplinary Knowledge</h3>
                        <p class="text-gray-600">Gain expertise that bridges physics, chemistry, and engineering, making you versatile in solving complex problems.</p>
                    </div>
                </div>
                
                <div class="relative group" data-aos="zoom-in" data-aos-delay="100">
                    <div class="absolute -inset-1 bg-gradient-to-r from-purple-500 to-pink-500 rounded-lg blur opacity-25 group-hover:opacity-100 transition duration-200"></div>
                    <div class="relative bg-white h-full p-6 rounded-lg shadow-md">
                        <h3 class="text-xl font-semibold mb-3 text-purple-600">High Demand Skills</h3>
                        <p class="text-gray-600">Materials engineers are sought after in industries from aerospace to biomedical to energy.</p>
                    </div>
                </div>
                
                <div class="relative group" data-aos="zoom-in" data-aos-delay="200">
                    <div class="absolute -inset-1 bg-gradient-to-r from-emerald-500 to-blue-500 rounded-lg blur opacity-25 group-hover:opacity-100 transition duration-200"></div>
                    <div class="relative bg-white h-full p-6 rounded-lg shadow-md">
                        <h3 class="text-xl font-semibold mb-3 text-emerald-600">Research Opportunities</h3>
                        <p class="text-gray-600">Contribute to cutting-edge research in nanotechnology, biomaterials, and sustainable materials.</p>
                    </div>
                </div>
                
                <div class="relative group" data-aos="zoom-in" data-aos-delay="300">
                    <div class="absolute -inset-1 bg-gradient-to-r from-yellow-500 to-orange-500 rounded-lg blur opacity-25 group-hover:opacity-100 transition duration-200"></div>
                    <div class="relative bg-white h-full p-6 rounded-lg shadow-md">
                        <h3 class="text-xl font-semibold mb-3 text-yellow-600">Global Impact</h3>
                        <p class="text-gray-600">Develop solutions for global challenges like clean energy, water purification, and sustainable manufacturing.</p>
                    </div>
                </div>
                
                <div class="relative group" data-aos="zoom-in" data-aos-delay="400">
                    <div class="absolute -inset-1 bg-gradient-to-r from-red-500 to-pink-500 rounded-lg blur opacity-25 group-hover:opacity-100 transition duration-200"></div>
                    <div class="relative bg-white h-full p-6 rounded-lg shadow-md">
                        <h3 class="text-xl font-semibold mb-3 text-red-600">Entrepreneurial Potential</h3>
                        <p class="text-gray-600">Create startups around new materials, coatings, or manufacturing processes.</p>
                    </div>
                </div>
                
                <div class="relative group" data-aos="zoom-in" data-aos-delay="500">
                    <div class="absolute -inset-1 bg-gradient-to-r from-indigo-500 to-purple-500 rounded-lg blur opacity-25 group-hover:opacity-100 transition duration-200"></div>
                    <div class="relative bg-white h-full p-6 rounded-lg shadow-md">
                        <h3 class="text-xl font-semibold mb-3 text-indigo-600">Competitive Salaries</h3>
                        <p class="text-gray-600">Materials engineers enjoy above-average compensation with strong growth potential.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Career Opportunities Section -->
    <section id="careers" class="py-20 bg-gray-50">
        <div style="width: 100%; margin: 0; padding: 0;">
            <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">Career Opportunities</h2>
                <div class="w-20 h-1 bg-emerald-500 mx-auto mb-6"></div>
                <p class="text-gray-600 max-w-3xl mx-auto">Materials engineers find rewarding careers across diverse industries with excellent growth prospects.</p>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
                <div class="bg-white p-6 rounded-lg shadow-md card-hover" data-aos="flip-left">
                    <div class="bg-blue-100 w-16 h-16 rounded-full flex items-center justify-center mb-4 mx-auto">
                        <i class="fas fa-plane text-blue-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2">Aerospace</h3>
                    <p class="text-gray-600 text-center">Develop lightweight, high-strength materials for aircraft and spacecraft.</p>
                </div>
                
                <div class="bg-white p-6 rounded-lg shadow-md card-hover" data-aos="flip-left" data-aos-delay="100">
                    <div class="bg-green-100 w-16 h-16 rounded-full flex items-center justify-center mb-4 mx-auto">
                        <i class="fas fa-car text-green-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2">Automotive</h3>
                    <p class="text-gray-600 text-center">Create advanced materials for safer, more efficient vehicles.</p>
                </div>
                
                <div class="bg-white p-6 rounded-lg shadow-md card-hover" data-aos="flip-left" data-aos-delay="200">
                    <div class="bg-red-100 w-16 h-16 rounded-full flex items-center justify-center mb-4 mx-auto">
                        <i class="fas fa-heart text-red-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2">Biomedical</h3>
                    <p class="text-gray-600 text-center">Design biocompatible materials for implants and medical devices.</p>
                </div>
                
                <div class="bg-white p-6 rounded-lg shadow-md card-hover" data-aos="flip-left" data-aos-delay="300">
                    <div class="bg-yellow-100 w-16 h-16 rounded-full flex items-center justify-center mb-4 mx-auto">
                        <i class="fas fa-bolt text-yellow-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2">Energy</h3>
                    <p class="text-gray-600 text-center">Improve materials for solar cells, batteries, and nuclear reactors.</p>
                </div>
                
                <div class="bg-white p-6 rounded-lg shadow-md card-hover" data-aos="flip-right" data-aos-delay="400">
                    <div class="bg-purple-100 w-16 h-16 rounded-full flex items-center justify-center mb-4 mx-auto">
                        <i class="fas fa-microchip text-purple-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2">Electronics</h3>
                    <p class="text-gray-600 text-center">Develop semiconductors and nanomaterials for faster devices.</p>
                </div>
                
                <div class="bg-white p-6 rounded-lg shadow-md card-hover" data-aos="flip-right" data-aos-delay="500">
                    <div class="bg-indigo-100 w-16 h-16 rounded-full flex items-center justify-center mb-4 mx-auto">
                        <i class="fas fa-industry text-indigo-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2">Manufacturing</h3>
                    <p class="text-gray-600 text-center">Optimize materials for production processes and quality control.</p>
                </div>
                
                <div class="bg-white p-6 rounded-lg shadow-md card-hover" data-aos="flip-right" data-aos-delay="600">
                    <div class="bg-pink-100 w-16 h-16 rounded-full flex items-center justify-center mb-4 mx-auto">
                        <i class="fas fa-flask text-pink-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2">Research & Development</h3>
                    <p class="text-gray-600 text-center">Push boundaries in national labs, universities, and corporate R&D.</p>
                </div>
                
                <div class="bg-white p-6 rounded-lg shadow-md card-hover" data-aos="flip-right" data-aos-delay="700">
                    <div class="bg-teal-100 w-16 h-16 rounded-full flex items-center justify-center mb-4 mx-auto">
                        <i class="fas fa-recycle text-teal-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold text-center mb-2">Sustainability</h3>
                    <p class="text-gray-600 text-center">Develop eco-friendly materials and recycling technologies.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- GATE Exam Section -->
    <section id="gate" class="py-20 bg-gradient-to-r from-blue-600 to-emerald-600 text-white">
        <div style="width: 100%; margin: 0; padding: 0;">
            <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">GATE (MT) - Metallurgy Exam</h2>
                <div class="w-20 h-1 bg-white mx-auto mb-6"></div>
                <p class="max-w-3xl mx-auto">The Graduate Aptitude Test in Engineering (GATE) for Metallurgical Engineering opens doors to prestigious opportunities.</p>
            </div>
            
            <div class="grid md:grid-cols-3 gap-10">
                <div class="bg-white bg-opacity-10 p-8 rounded-lg backdrop-blur-sm card-hover" data-aos="fade-up">
                    <h3 class="text-xl font-semibold mb-4 flex items-center">
                        <span class="bg-white text-blue-600 w-8 h-8 rounded-full flex items-center justify-center mr-3">1</span>
                        PSU Recruitment
                    </h3>
                    <p>GATE scores are used by Public Sector Undertakings like SAIL, NALCO, and Hindustan Copper for direct recruitment.</p>
                </div>
                
                <div class="bg-white bg-opacity-10 p-8 rounded-lg backdrop-blur-sm card-hover" data-aos="fade-up" data-aos-delay="100">
                    <h3 class="text-xl font-semibold mb-4 flex items-center">
                        <span class="bg-white text-blue-600 w-8 h-8 rounded-full flex items-center justify-center mr-3">2</span>
                        Higher Education
                    </h3>
                    <p>Admission to MTech and PhD programs at IITs, NITs, and other prestigious institutions in India and abroad.</p>
                </div>
                
                <div class="bg-white bg-opacity-10 p-8 rounded-lg backdrop-blur-sm card-hover" data-aos="fade-up" data-aos-delay="200">
                    <h3 class="text-xl font-semibold mb-4 flex items-center">
                        <span class="bg-white text-blue-600 w-8 h-8 rounded-full flex items-center justify-center mr-3">3</span>
                        Research Fellowships
                    </h3>
                    <p>Qualify for CSIR, DST, and other research fellowships to pursue cutting-edge materials research.</p>
                </div>
            </div>
            
            <div class="mt-16 bg-white bg-opacity-20 p-8 rounded-lg max-w-4xl mx-auto" data-aos="zoom-in">
                <h3 class="text-xl font-semibold mb-4 text-center">GATE (MT) Exam Pattern</h3>
                <div class="grid md:grid-cols-4 gap-4 text-center">
                    <div class="bg-white bg-opacity-30 p-4 rounded-lg">
                        <div class="text-2xl font-bold text-white">65</div>
                        <div class="text-sm">Total Questions</div>
                    </div>
                    <div class="bg-white bg-opacity-30 p-4 rounded-lg">
                        <div class="text-2xl font-bold text-white">100</div>
                        <div class="text-sm">Maximum Marks</div>
                    </div>
                    <div class="bg-white bg-opacity-30 p-4 rounded-lg">
                        <div class="text-2xl font-bold text-white">3</div>
                        <div class="text-sm">Hours Duration</div>
                    </div>
                    <div class="bg-white bg-opacity-30 p-4 rounded-lg">
                        <div class="text-2xl font-bold text-white">5</div>
                        <div class="text-sm">Sections</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Elon Musk Quote Section -->
    <section class="py-20 bg-gray-800 text-white">
        <div style="width: 100%; margin: 0; padding: 0;">
            <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">Industry Perspectives</h2>
                <div class="w-20 h-1 bg-emerald-500 mx-auto mb-6"></div>
                <p class="max-w-3xl mx-auto">What leaders say about the importance of materials science and engineering.</p>
            </div>
            
            <div class="max-w-4xl mx-auto bg-gray-700 rounded-xl overflow-hidden shadow-2xl" data-aos="zoom-in">
                <div class="p-8">
                    <div class="flex items-start">
                        <img src="https://pbs.twimg.com/profile_images/1683325380441128960/yRsRRjGO_400x400.jpg" 
                             alt="Elon Musk" 
                             class="w-16 h-16 rounded-full mr-6">
                        <div>
                            <div class="flex items-center mb-2">
                                <h3 class="text-xl font-bold mr-2">Elon Musk</h3>
                                <span class="text-gray-400">@elonmusk</span>
                            </div>
                            <p class="text-lg mb-4">"The fundamental limitation in rocket design is materials science. If we had materials that could withstand higher temperatures, we could make rockets dramatically more efficient."</p>
                            <div class="flex items-center text-gray-400 text-sm">
                                <i class="fas fa-retweet mr-2"></i>
                                <span class="mr-4">24.5K</span>
                                <i class="fas fa-heart mr-2"></i>
                                <span>128.7K</span>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="bg-gray-600 px-8 py-4 flex items-center">
                    <i class="fab fa-twitter text-blue-400 mr-2"></i>
                    <span>Posted on Twitter, June 2022</span>
                </div>
            </div>
            
            <div class="mt-12 grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="bg-gray-700 p-6 rounded-lg" data-aos="fade-up">
                    <blockquote class="text-lg italic mb-4">"Advanced materials are key to solving our energy challenges. Better batteries, solar cells, and nuclear materials could transform our energy landscape."</blockquote>
                    <div class="flex items-center">
                        <div class="bg-gray-600 w-10 h-10 rounded-full flex items-center justify-center mr-4">
                            <i class="fas fa-user"></i>
                        </div>
                        <div>
                            <div class="font-semibold">Dr. Mildred Dresselhaus</div>
                            <div class="text-sm text-gray-400">"Queen of Carbon Science"</div>
                        </div>
                    </div>
                </div>
                
                <div class="bg-gray-700 p-6 rounded-lg" data-aos="fade-up" data-aos-delay="100">
                    <blockquote class="text-lg italic mb-4">"The next decade will belong to materials engineers who can develop sustainable alternatives to current industrial materials."</blockquote>
                    <div class="flex items-center">
                        <div class="bg-gray-600 w-10 h-10 rounded-full flex items-center justify-center mr-4">
                            <i class="fas fa-user"></i>
                        </div>
                        <div>
                            <div class="font-semibold">Dr. Jennifer Lewis</div>
                            <div class="text-sm text-gray-400">Harvard Materials Scientist</div>
                        </div>
                    </div>
                </div>
                
                <div class="bg-gray-700 p-6 rounded-lg" data-aos="fade-up" data-aos-delay="200">
                    <blockquote class="text-lg italic mb-4">"Materials innovation is the invisible backbone of technological progress across all industries."</blockquote>
                    <div class="flex items-center">
                        <div class="bg-gray-600 w-10 h-10 rounded-full flex items-center justify-center mr-4">
                            <i class="fas fa-user"></i>
                        </div>
                        <div>
                            <div class="font-semibold">Dr. Yet-Ming Chiang</div>
                            <div class="text-sm text-gray-400">MIT Professor, Battery Innovator</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Future Trends Section -->
    <section id="future" class="py-20 bg-white">
        <div style="width: 100%; margin: 0; padding: 0;">
            <div class="text-center mb-16" data-aos="fade-up">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">The Future of Materials Engineering</h2>
                <div class="w-20 h-1 bg-blue-500 mx-auto mb-6"></div>
                <p class="text-gray-600 max-w-3xl mx-auto">Emerging trends that will shape the next decade of materials innovation.</p>
            </div>
            
            <div class="grid md:grid-cols-2 gap-10 items-center mb-16">
                <div data-aos="fade-right">
                    <img src="https://images.unsplash.com/photo-1581094794329-c8112a89af12?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
                         alt="Nanotechnology" 
                         class="rounded-lg shadow-xl w-full">
                </div>
                
                <div class="space-y-6" data-aos="fade-left">
                    <h3 class="text-2xl font-bold text-blue-600">Nanomaterials Revolution</h3>
                    <p class="text-gray-600">Engineered materials at the nanoscale (1-100 nanometers) exhibit extraordinary properties not found in bulk materials.</p>
                    <ul class="space-y-3">
                        <li class="flex items-start">
                            <span class="bg-blue-100 text-blue-600 rounded-full p-1 mr-3">
                                <i class="fas fa-check text-xs"></i>
                            </span>
                            <span>Graphene - 200x stronger than steel yet flexible</span>
                        </li>
                        <li class="flex items-start">
                            <span class="bg-blue-100 text-blue-600 rounded-full p-1 mr-3">
                                <i class="fas fa-check text-xs"></i>
                            </span>
                            <span>Quantum dots for ultra-efficient displays and solar cells</span>
                        </li>
                        <li class="flex items-start">
                            <span class="bg-blue-100 text-blue-600 rounded-full p-1 mr-3">
                                <i class="fas fa-check text-xs"></i>
                            </span>
                            <span>Nanomedicine for targeted drug delivery</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="grid md:grid-cols-2 gap-10 items-center mb-16">
                <div class="md:order-2" data-aos="fade-left">
                    <img src="https://images.unsplash.com/photo-1575505586569-646b2ca898fc?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2086&q=80" 
                         alt="Biomaterials" 
                         class="rounded-lg shadow-xl w-full">
                </div>
                
                <div class="md:order-1 space-y-6" data-aos="fade-right">
                    <h3 class="text-2xl font-bold text-emerald-600">Biomaterials & Tissue Engineering</h3>
                    <p class="text-gray-600">Materials that interact with biological systems for medical applications and beyond.</p>
                    <ul class="space-y-3">
                        <li class="flex items-start">
                            <span class="bg-emerald-100 text-emerald-600 rounded-full p-1 mr-3">
                                <i class="fas fa-check text-xs"></i>
                            </span>
                            <span>3D-printed organs and tissue scaffolds</span>
                        </li>
                        <li class="flex items-start">
                            <span class="bg-emerald-100 text-emerald-600 rounded-full p-1 mr-3">
                                <i class="fas fa-check text-xs"></i>
                            </span>
                            <span>Bioabsorbable implants that dissolve after healing</span>
                        </li>
                        <li class="flex items-start">
                            <span class="bg-emerald-100 text-emerald-600 rounded-full p-1 mr-3">
                                <i class="fas fa-check text-xs"></i>
                            </span>
                            <span>Smart materials that respond to biological signals</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="grid md:grid-cols-2 gap-10 items-center">
                <div data-aos="fade-right">
                    <img src="https://images.unsplash.com/photo-1508514177221-188b1cf16e9d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2072&q=80" 
                         alt="Sustainable materials" 
                         class="rounded-lg shadow-xl w-full">
                </div>
                
                <div class="space-y-6" data-aos="fade-left">
                    <h3 class="text-2xl font-bold text-purple-600">Sustainable & Smart Materials</h3>
                    <p class="text-gray-600">Materials designed for environmental sustainability and intelligent functionality.</p>
                    <ul class="space-y-3">
                        <li class="flex items-start">
                            <span class="bg-purple-100 text-purple-600 rounded-full p-1 mr-3">
                                <i class="fas fa-check text-xs"></i>
                            </span>
                            <span>Self-healing materials that repair cracks automatically</span>
                        </li>
                        <li class="flex items-start">
                            <span class="bg-purple-100 text-purple-600 rounded-full p-1 mr-3">
                                <i class="fas fa-check text-xs"></i>
                            </span>
                            <span>Phase-change materials for energy-efficient buildings</span>
                        </li>
                        <li class="flex items-start">
                            <span class="bg-purple-100 text-purple-600 rounded-full p-1 mr-3">
                                <i class="fas fa-check text-xs"></i>
                            </span>
                            <span>Biodegradable polymers to replace conventional plastics</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Call to Action -->
    <section class="py-20 bg-gradient-to-r from-blue-500 to-purple-600 text-white">
        <div style="width: 100%; margin: 0; padding: 0;">
            <div class="max-w-3xl mx-auto" data-aos="zoom-in">
                <h2 class="text-3xl md:text-4xl font-bold mb-6">Ready to Explore Materials Engineering?</h2>
                <p class="text-xl mb-8">Join the next generation of innovators shaping our material world.</p>
                
                <div class="flex flex-col sm:flex-row justify-center gap-4">
                    <a href="#" class="bg-white text-blue-600 font-semibold px-8 py-3 rounded-full hover:bg-gray-100 transition duration-300 transform hover:scale-105">
                        Download Brochure
                    </a>
                    <a href="#" class="bg-transparent border-2 border-white text-white font-semibold px-8 py-3 rounded-full hover:bg-white hover:text-blue-600 transition duration-300 transform hover:scale-105">
                        Contact Advisor
                    </a>
                </div>
            </div>
            
            <div class="mt-16 grid md:grid-cols-3 gap-8 text-left max-w-6xl mx-auto">
                <div class="bg-white bg-opacity-10 p-6 rounded-lg backdrop-blur-sm" data-aos="fade-up">
                    <h3 class="text-xl font-semibold mb-3">Upcoming Webinar</h3>
                    <p class="mb-4">"Nanomaterials: The Next Frontier" - June 15, 2023</p>
                    <a href="#" class="text-white font-medium inline-flex items-center">
                        Register Now <i class="fas fa-arrow-right ml-2"></i>
                    </a>
                </div>
                
                <div class="bg-white bg-opacity-10 p-6 rounded-lg backdrop-blur-sm" data-aos="fade-up" data-aos-delay="100">
                    <h3 class="text-xl font-semibold mb-3">GATE Preparation</h3>
                    <p class="mb-4">Comprehensive materials for GATE (MT) 2024 preparation.</p>
                    <a href="#" class="text-white font-medium inline-flex items-center">
                        Explore Courses <i class="fas fa-arrow-right ml-2"></i>
                    </a>
                </div>
                
                <div class="bg-white bg-opacity-10 p-6 rounded-lg backdrop-blur-sm" data-aos="fade-up" data-aos-delay="200">
                    <h3 class="text-xl font-semibold mb-3">Career Guidance</h3>
                    <p class="mb-4">Schedule a one-on-one session with our career experts.</p>
                    <a href="#" class="text-white font-medium inline-flex items-center">
                        Book Session <i class="fas fa-arrow-right ml-2"></i>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-400 py-12">
        <div style="width: 100%; margin: 0; padding: 0;">
            <div class="grid md:grid-cols-4 gap-10">
                <div>
                    <h3 class="text-white text-lg font-semibold mb-4">MaterialScience</h3>
                    <p class="mb-4">Empowering the next generation of materials engineers and scientists.</p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-white">
                            <i class="fab fa-twitter text-xl"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white">
                            <i class="fab fa-linkedin text-xl"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white">
                            <i class="fab fa-youtube text-xl"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white">
                            <i class="fab fa-instagram text-xl"></i>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h3 class="text-white text-lg font-semibold mb-4">Quick Links</h3>
                    <ul class="space-y-2">
                        <li><a href="#introduction" class="hover:text-white">Introduction</a></li>
                        <li><a href="#importance" class="hover:text-white">Why It Matters</a></li>
                        <li><a href="#careers" class="hover:text-white">Career Paths</a></li>
                        <li><a href="#gate" class="hover:text-white">GATE (MT) Exam</a></li>
                        <li><a href="#future" class="hover:text-white">Future Trends</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-white text-lg font-semibold mb-4">Resources</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="hover:text-white">Blog</a></li>
                        <li><a href="#" class="hover:text-white">Research Papers</a></li>
                        <li><a href="#" class="hover:text-white">Industry Reports</a></li>
                        <li><a href="#" class="hover:text-white">Webinars</a></li>
                        <li><a href="#" class="hover:text-white">FAQ</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-white text-lg font-semibold mb-4">Contact Us</h3>
                    <ul class="space-y-2">
                        <li class="flex items-start">
                            <i class="fas fa-map-marker-alt mt-1 mr-3"></i>
                            <span>123 Science Park, Innovation City, IN 560001</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-envelope mr-3"></i>
                            <span>info@materialscience.edu</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-phone-alt mr-3"></i>
                            <span>+91 9876543210</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-10 pt-6 flex flex-col md:flex-row justify-between items-center">
                <p>&copy; 2023 MaterialScience. All rights reserved.</p>
                <div class="mt-4 md:mt-0">
                    <a href="#" class="text-sm hover:text-white mr-4">Privacy Policy</a>
                    <a href="#" class="text-sm hover:text-white mr-4">Terms of Service</a>
                    <a href="#" class="text-sm hover:text-white">Sitemap</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- Back to Top Button -->
    <button id="back-to-top" class="fixed bottom-8 right-8 bg-blue-600 text-white w-12 h-12 rounded-full shadow-lg hidden items-center justify-center hover:bg-blue-700 transition duration-300">
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
        
        // Testimonial carousel functionality
        let currentTestimonial = 0;
        const testimonials = document.querySelectorAll('.testimonial-slide');
        const totalTestimonials = testimonials.length;
        
        function showTestimonial(index) {
            testimonials.forEach((testimonial, i) => {
                testimonial.style.transform = `translateX(${100 * (i - index)}%)`;
            });
        }
        
        function nextTestimonial() {
            currentTestimonial = (currentTestimonial + 1) % totalTestimonials;
            showTestimonial(currentTestimonial);
        }
        
        // Auto-rotate testimonials every 5 seconds
        setInterval(nextTestimonial, 5000);
    </script>
</body>
</html>
