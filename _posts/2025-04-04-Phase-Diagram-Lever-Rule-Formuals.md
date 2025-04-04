<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Materials Science Reference | Phase Diagram Equations</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&family=Source+Code+Pro&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #2ecc71;
            --warning: #f39c12;
            --info: #3498db;
            --text: #333;
            --light-gray: #f5f5f5;
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            line-height: 1.6;
            color: var(--text);
            background-color: #f9f9f9;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 2rem 1rem;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            width: 100%;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
            flex: 1;
        }
        
        h1 {
            font-size: clamp(1.8rem, 5vw, 2.5rem);
            margin-bottom: 0.5rem;
        }
        
        .subtitle {
            font-weight: 300;
            font-size: clamp(1rem, 3vw, 1.2rem);
            opacity: 0.9;
        }
        
        nav {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            width: 100%;
            overflow-x: auto;
            -webkit-overflow-scrolling: touch;
        }
        
        .nav-container {
            display: flex;
            justify-content: center;
            padding: 0.8rem 0;
            min-width: max-content;
        }
        
        .nav-link {
            padding: 0.5rem 1rem;
            color: var(--dark);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            border-radius: 4px;
            margin: 0 0.3rem;
            white-space: nowrap;
            font-size: clamp(0.8rem, 3vw, 1rem);
        }
        
        .nav-link:hover, .nav-link.active {
            background-color: var(--secondary);
            color: white;
        }
        
        main {
            padding: 1.5rem 0;
            width: 100%;
        }
        
        .section {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 15px rgba(0,0,0,0.05);
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            width: 100%;
        }
        
        h2 {
            color: var(--secondary);
            margin-bottom: 1.2rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--light);
            font-size: clamp(1.3rem, 4vw, 1.6rem);
        }
        
        .equation-card {
            border-left: 4px solid var(--secondary);
            padding: 1.2rem;
            margin-bottom: 1.2rem;
            background-color: #f8fafc;
            border-radius: 0 8px 8px 0;
            transition: all 0.3s ease;
            width: 100%;
        }
        
        .equation-card:hover {
            transform: translateX(5px);
            box-shadow: 2px 5px 15px rgba(0,0,0,0.1);
        }
        
        .equation {
            font-family: 'Source Code Pro', monospace;
            font-size: clamp(0.9rem, 3vw, 1.1rem);
            background-color: var(--light-gray);
            padding: 0.7rem 0.9rem;
            border-radius: 6px;
            display: inline-block;
            margin: 0.4rem 0;
            color: var(--dark);
            width: 100%;
            overflow-x: auto;
        }
        
        .equation-desc {
            margin-top: 0.7rem;
            color: #555;
            font-size: clamp(0.9rem, 3vw, 1rem);
        }
        
        .category-tag {
            display: inline-block;
            padding: 0.2rem 0.7rem;
            border-radius: 20px;
            font-size: clamp(0.7rem, 2.5vw, 0.8rem);
            font-weight: 500;
            margin-top: 0.5rem;
        }
        
        .tag-iso { background-color: #ffeceb; color: #e74c3c; }
        .tag-vol { background-color: #ebf5ff; color: #3498db; }
        .tag-eutectic { background-color: #f3ebff; color: #9b59b6; }
        .tag-fec { background-color: #fff8eb; color: #f39c12; }
        .tag-thermo { background-color: #e8f8f0; color: #27ae60; }
        
        footer {
            background-color: var(--dark);
            color: white;
            text-align: center;
            padding: 1.5rem 0;
            margin-top: auto;
            width: 100%;
        }
        
        .watermark {
            position: fixed;
            bottom: 10px;
            right: 10px;
            opacity: 0.05;
            font-size: clamp(4rem, 20vw, 8rem);
            font-weight: bold;
            color: var(--dark);
            pointer-events: none;
            transform: rotate(-15deg);
            z-index: -1;
            font-family: 'Roboto', sans-serif;
        }
        
        .search-container {
            margin: 1.5rem 0;
            width: 100%;
        }
        
        #searchInput {
            width: 100%;
            max-width: 600px;
            padding: 0.8rem 1.2rem;
            border: 2px solid #ddd;
            border-radius: 30px;
            font-size: clamp(0.9rem, 3vw, 1rem);
            transition: all 0.3s ease;
            display: block;
            margin: 0 auto;
        }
        
        #searchInput:focus {
            outline: none;
            border-color: var(--secondary);
            box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.2);
        }
        
        /* Responsive adjustments */
        @media (max-width: 768px) {
            header {
                padding: 1.5rem 1rem;
            }
            
            .nav-container {
                justify-content: flex-start;
                padding: 0.8rem 1rem;
            }
            
            .section {
                padding: 1.2rem;
            }
            
            .equation-card {
                padding: 1rem;
            }
        }
        
        @media (max-width: 480px) {
            .nav-link {
                padding: 0.5rem 0.8rem;
                margin: 0 0.2rem;
            }
            
            .section {
                padding: 1rem;
            }
            
            .equation-card {
                padding: 0.8rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Phase Diagram Equations</h1>
            <p class="subtitle">Essential formulas for materials science and engineering</p>
        </div>
    </header>
    
    <nav>
        <div class="nav-container">
            <a href="#binary-iso" class="nav-link active">Binary Isomorphous</a>
            <a href="#volume-fractions" class="nav-link">Volume Fractions</a>
            <a href="#eutectic" class="nav-link">Eutectic System</a>
            <a href="#fec" class="nav-link">Fe-C System</a>
            <a href="#thermo" class="nav-link">Thermodynamics</a>
        </div>
    </nav>
    
    <main>
        <div class="container">
            <div class="search-container">
                <input type="text" id="searchInput" placeholder="Search equations...">
            </div>
            
            <section id="binary-iso" class="section">
                <h2>Binary Isomorphous System</h2>
                
                <div class="equation-card">
                    <div class="equation">$W_L = \frac{C_a - C_0}{C_a - C_L}$</div>
                    <p class="equation-desc">Mass fraction of liquid phase in a binary isomorphous system</p>
                    <span class="category-tag tag-iso">Binary Isomorphous</span>
                </div>
                
                <div class="equation-card">
                    <div class="equation">$W_a = \frac{C_0 - C_L}{C_a - C_L}$</div>
                    <p class="equation-desc">Mass fraction of $\alpha$ solid-solution phase in a binary isomorphous system</p>
                    <span class="category-tag tag-iso">Binary Isomorphous</span>
                </div>
            </section>
            
            <section id="volume-fractions" class="section">
                <h2>Volume Fractions</h2>
                
                <div class="equation-card">
                    <div class="equation">$V_a = \frac{V_a}{V_a + V_\beta}$</div>
                    <p class="equation-desc">Volume fraction of $\alpha$ phase</p>
                    <span class="category-tag tag-vol">Volume Fractions</span>
                </div>
                
                <div class="equation-card">
                    <div class="equation">$V_a = \frac{\rho_a}{\rho_a + \rho_\beta}$</div>
                    <p class="equation-desc">Conversion of mass fraction to volume fraction for $\alpha$ phase</p>
                    <span class="category-tag tag-vol">Volume Fractions</span>
                </div>
                
                <div class="equation-card">
                    <div class="equation">$W_a = \frac{V_a \rho_a}{V_a \rho_a + V_\beta \rho_\beta}$</div>
                    <p class="equation-desc">Conversion of volume fraction to mass fraction for $\alpha$ phase</p>
                    <span class="category-tag tag-vol">Volume Fractions</span>
                </div>
            </section>
            
            <section id="eutectic" class="section">
                <h2>Binary Eutectic System</h2>
                
                <div class="equation-card">
                    <div class="equation">$W_e = \frac{P}{P + Q}$</div>
                    <p class="equation-desc">Mass fraction of eutectic microconstituent</p>
                    <span class="category-tag tag-eutectic">Eutectic System</span>
                </div>
                
                <div class="equation-card">
                    <div class="equation">$W_{a'} = \frac{Q}{P + Q}$</div>
                    <p class="equation-desc">Mass fraction of primary $\alpha$ microconstituent</p>
                    <span class="category-tag tag-eutectic">Eutectic System</span>
                </div>
                
                <div class="equation-card">
                    <div class="equation">$W_a = \frac{Q + R}{P + Q + R}$</div>
                    <p class="equation-desc">Mass fraction of total $\alpha$ phase</p>
                    <span class="category-tag tag-eutectic">Eutectic System</span>
                </div>
                
                <div class="equation-card">
                    <div class="equation">$W_\beta = \frac{P}{P + Q + R}$</div>
                    <p class="equation-desc">Mass fraction of $\beta$ phase</p>
                    <span class="category-tag tag-eutectic">Eutectic System</span>
                </div>
            </section>
            
            <section id="fec" class="section">
                <h2>Fe–C Alloy System</h2>
                
                <div class="equation-card">
                    <div class="equation">$W_\rho = \frac{C_0' + 0.022}{0.74}$</div>
                    <p class="equation-desc">Mass fraction of pearlite in a hypoeutectoid Fe–C alloy</p>
                    <span class="category-tag tag-fec">Fe-C System</span>
                </div>
                
                <div class="equation-card">
                    <div class="equation">$W_{a'} = \frac{0.76 - C_0'}{0.74}$</div>
                    <p class="equation-desc">Mass fraction of proeutectoid $\alpha$ ferrite in a hypoeutectoid Fe–C alloy</p>
                    <span class="category-tag tag-fec">Fe-C System</span>
                </div>
                
                <div class="equation-card">
                    <div class="equation">$W_\rho = \frac{6.70 - C_1'}{5.94}$</div>
                    <p class="equation-desc">Mass fraction of pearlite in a hypereutectoid Fe–C alloy</p>
                    <span class="category-tag tag-fec">Fe-C System</span>
                </div>
                
                <div class="equation-card">
                    <div class="equation">$W_{\text{Fe}_3\text{C}'} = \frac{C_1' - 0.76}{5.94}$</div>
                    <p class="equation-desc">Mass fraction of proeutectoid $\text{Fe}_3\text{C}$ in a hypereutectoid Fe–C alloy</p>
                    <span class="category-tag tag-fec">Fe-C System</span>
                </div>
            </section>
            
            <section id="thermo" class="section">
                <h2>Thermodynamics</h2>
                
                <div class="equation-card">
                    <div class="equation">$P + F = C + N$</div>
                    <p class="equation-desc">Gibbs phase rule (general form)</p>
                    <span class="category-tag tag-thermo">Thermodynamics</span>
                </div>
            </section>
        </div>
    </main>
    
    <footer>
        <div class="container">
            <p>&copy; <span id="current-year"></span> Join us for GATE MT Prep | TestUrSelf</p>
        </div>
    </footer>
    
    <div class="watermark">TestUrSelf</div>

    <!-- MathJax Configuration -->
    <script>
        MathJax = {
          tex: {
            inlineMath: [['$', '$'], ['\\(', '\\)']]
          },
          options: {
            skipHtmlTags: ['script', 'noscript', 'style', 'textarea', 'pre']
          }
        };
    </script>
    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
    
    <script>
        // Set current year in footer
        document.getElementById('current-year').textContent = new Date().getFullYear();
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
                
                // Update active nav link
                document.querySelectorAll('.nav-link').forEach(link => {
                    link.classList.remove('active');
                });
                this.classList.add('active');
            });
        });
        
        // Search functionality
        document.getElementById('searchInput').addEventListener('input', function() {
            const searchTerm = this.value.toLowerCase();
            const equationCards = document.querySelectorAll('.equation-card');
            
            equationCards.forEach(card => {
                const text = card.textContent.toLowerCase();
                if (text.includes(searchTerm)) {
                    card.style.display = 'block';
                } else {
                    card.style.display = 'none';
                }
            });
        });
        
        // Highlight active section in nav while scrolling
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('.nav-link');
            
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (pageYOffset >= sectionTop - 200) {
                    current = section.getAttribute('id');
                }
            });
            
            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === `#${current}`) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>
