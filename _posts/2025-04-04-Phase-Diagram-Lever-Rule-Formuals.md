<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Phase Diagram Equations | TestUrSelf</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&family=Source+Code+Pro&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
            --highlight-color: #f39c12;
            --success-color: #2ecc71;
            --error-color: #e74c3c;
            --text-color: #333;
            --iso-color: #e74c3c;
            --vol-color: #3498db;
            --eutectic-color: #9b59b6;
            --fec-color: #f39c12;
            --thermo-color: #2ecc71;
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            line-height: 1.8;
            color: var(--text-color);
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
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 50%, #f8f9fa 100%);
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
            content: "TestUrSelf";
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-30deg);
            font-size: 150px;
            font-weight: bold;
            color: rgba(44, 62, 80, 0.05);
            z-index: -1;
            pointer-events: none;
            white-space: nowrap;
            text-transform: uppercase;
            letter-spacing: 15px;
            width: 200%;
            text-align: center;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            color: white;
            padding: 3rem;
            text-align: center;
            border-radius: 8px;
            margin: 2rem auto;
            max-width: 1200px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.2);
            position: relative;
            z-index: 1;
            overflow: hidden;
        }
        
        header::after {
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
        
        h1 {
            margin: 0;
            font-size: 2.5rem;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            letter-spacing: 1px;
        }
        
        .subtitle {
            font-weight: 300;
            font-size: 1.2rem;
            opacity: 0.9;
            margin-top: 0.5rem;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        nav {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
            margin-bottom: 2rem;
        }
        
        .nav-container {
            display: flex;
            justify-content: center;
            padding: 1rem 0;
            max-width: 1200px;
            margin: 0 auto;
            overflow-x: auto;
        }
        
        .nav-link {
            padding: 0.8rem 1.5rem;
            color: var(--dark-color);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            border-radius: 4px;
            margin: 0 0.5rem;
            white-space: nowrap;
        }
        
        .nav-link:hover, .nav-link.active {
            background-color: var(--secondary-color);
            color: white;
        }
        
        .search-container {
            margin: 2rem auto;
            max-width: 800px;
        }
        
        #searchInput {
            width: 100%;
            padding: 1rem 1.5rem;
            border: 2px solid #ddd;
            border-radius: 50px;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
        }
        
        #searchInput:focus {
            outline: none;
            border-color: var(--secondary-color);
            box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.2);
        }
        
        .section {
            background-color: white;
            border-radius: 12px;
            padding: 2.5rem;
            margin-bottom: 3rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
            z-index: 1;
            transition: all 0.3s ease;
            border: 1px solid rgba(0,0,0,0.05);
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }
        
        h2 {
            color: var(--primary-color);
            border-bottom: 4px solid var(--highlight-color);
            padding-bottom: 0.8rem;
            margin-top: 0;
            font-size: 1.8rem;
            background: linear-gradient(to right, transparent, var(--light-color), transparent);
            padding: 1rem 0;
            text-align: center;
            border-radius: 8px;
            position: relative;
            scroll-margin-top: 120px;
        }
        
        h2::after {
            content: "";
            position: absolute;
            left: 0;
            right: 0;
            bottom: -5px;
            height: 3px;
            background: linear-gradient(to right, transparent, var(--highlight-color), transparent);
        }
        
        .equation-card {
            background-color: #f8f9fa;
            border-radius: 10px;
            padding: 1.8rem;
            margin-bottom: 1.8rem;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            border-left: 5px solid var(--secondary-color);
            position: relative;
            overflow: hidden;
        }
        
        .equation-card:hover {
            transform: translateX(5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .equation-card.iso { border-left-color: var(--iso-color); }
        .equation-card.vol { border-left-color: var(--vol-color); }
        .equation-card.eutectic { border-left-color: var(--eutectic-color); }
        .equation-card.fec { border-left-color: var(--fec-color); }
        .equation-card.thermo { border-left-color: var(--thermo-color); }
        
        .equation-card::before {
            content: "";
            position: absolute;
            top: 0;
            right: 0;
            width: 0;
            height: 0;
            border-style: solid;
            border-width: 0 50px 50px 0;
            border-color: transparent rgba(0,0,0,0.05) transparent transparent;
        }
        
        .equation {
            font-family: 'Source Code Pro', monospace;
            font-size: 1.2rem;
            background-color: #e9ecef;
            padding: 1rem 1.2rem;
            border-radius: 8px;
            display: inline-block;
            margin: 0.5rem 0;
            color: var(--dark-color);
            width: 100%;
            overflow-x: auto;
            transition: all 0.3s ease;
        }
        
        .equation:hover {
            background-color: #dee2e6;
        }
        
        .equation-desc {
            margin-top: 1rem;
            color: #555;
            font-size: 1rem;
            line-height: 1.6;
        }
        
        .category-tag {
            display: inline-block;
            padding: 0.4rem 1rem;
            border-radius: 50px;
            font-size: 0.85rem;
            font-weight: 600;
            margin-top: 1rem;
            background-color: var(--light-color);
            color: var(--dark-color);
        }
        
        .tag-iso { background-color: rgba(231, 76, 60, 0.1); color: var(--iso-color); }
        .tag-vol { background-color: rgba(52, 152, 219, 0.1); color: var(--vol-color); }
        .tag-eutectic { background-color: rgba(155, 89, 182, 0.1); color: var(--eutectic-color); }
        .tag-fec { background-color: rgba(243, 156, 18, 0.1); color: var(--fec-color); }
        .tag-thermo { background-color: rgba(46, 204, 113, 0.1); color: var(--thermo-color); }
        
        footer {
            background-color: var(--dark-color);
            color: white;
            text-align: center;
            padding: 2rem 0;
            margin-top: 3rem;
            border-top: 5px solid var(--highlight-color);
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .watermark {
            position: fixed;
            bottom: 20px;
            right: 20px;
            opacity: 0.05;
            font-size: 8rem;
            font-weight: bold;
            color: var(--dark-color);
            pointer-events: none;
            transform: rotate(-15deg);
            z-index: -1;
            font-family: 'Roboto', sans-serif;
        }
        
        /* Interactive elements */
        .copy-btn {
            background-color: var(--light-color);
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 4px;
            cursor: pointer;
            margin-top: 0.5rem;
            font-size: 0.8rem;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .copy-btn:hover {
            background-color: var(--secondary-color);
            color: white;
        }
        
        /* Responsive adjustments */
        @media (max-width: 768px) {
            header {
                padding: 2rem 1rem;
                margin: 1rem;
                border-radius: 0;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .nav-container {
                justify-content: flex-start;
                padding: 0.8rem 1rem;
            }
            
            .nav-link {
                padding: 0.6rem 1rem;
                margin: 0 0.3rem;
                font-size: 0.9rem;
            }
            
            .section {
                padding: 1.5rem;
                margin: 1rem;
            }
            
            .equation-card {
                padding: 1.2rem;
            }
            
            .equation {
                font-size: 1rem;
                padding: 0.8rem 1rem;
            }
            
            body::after {
                font-size: 80px;
            }
        }
        
        @media (max-width: 480px) {
            header {
                padding: 1.5rem 1rem;
            }
            
            h1 {
                font-size: 1.8rem;
            }
            
            .subtitle {
                font-size: 1rem;
            }
            
            .section {
                padding: 1.2rem;
            }
            
            h2 {
                font-size: 1.5rem;
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
    
    <div class="container">
        <div class="search-container">
            <input type="text" id="searchInput" placeholder="Search equations...">
        </div>
        
        <section id="binary-iso" class="section">
            <h2>Binary Isomorphous System</h2>
            
            <div class="equation-card iso">
                <div class="equation">$W_L = \frac{C_a - C_0}{C_a - C_L}$</div>
                <p class="equation-desc">Mass fraction of liquid phase in a binary isomorphous system</p>
                <span class="category-tag tag-iso">Binary Isomorphous</span>
                <button class="copy-btn" onclick="copyToClipboard('W_L = \\frac{C_a - C_0}{C_a - C_L}')">
                    <i class="far fa-copy"></i> Copy Equation
                </button>
            </div>
            
            <div class="equation-card iso">
                <div class="equation">$W_a = \frac{C_0 - C_L}{C_a - C_L}$</div>
                <p class="equation-desc">Mass fraction of $\alpha$ solid-solution phase in a binary isomorphous system</p>
                <span class="category-tag tag-iso">Binary Isomorphous</span>
                <button class="copy-btn" onclick="copyToClipboard('W_a = \\frac{C_0 - C_L}{C_a - C_L}')">
                    <i class="far fa-copy"></i> Copy Equation
                </button>
            </div>
        </section>
        
        <section id="volume-fractions" class="section">
            <h2>Volume Fractions</h2>
            
            <div class="equation-card vol">
                <div class="equation">$V_a = \frac{V_a}{V_a + V_\beta}$</div>
                <p class="equation-desc">Volume fraction of $\alpha$ phase</p>
                <span class="category-tag tag-vol">Volume Fractions</span>
                <button class="copy-btn" onclick="copyToClipboard('V_a = \\frac{V_a}{V_a + V_\\beta}')">
                    <i class="far fa-copy"></i> Copy Equation
                </button>
            </div>
            
            <div class="equation-card vol">
                <div class="equation">$V_a = \frac{\rho_a}{\rho_a + \rho_\beta}$</div>
                <p class="equation-desc">Conversion of mass fraction to volume fraction for $\alpha$ phase</p>
                <span class="category-tag tag-vol">Volume Fractions</span>
                <button class="copy-btn" onclick="copyToClipboard('V_a = \\frac{\\rho_a}{\\rho_a + \\rho_\\beta}')">
                    <i class="far fa-copy"></i> Copy Equation
                </button>
            </div>
            
            <div class="equation-card vol">
                <div class="equation">$W_a = \frac{V_a \rho_a}{V_a \rho_a + V_\beta \rho_\beta}$</div>
                <p class="equation-desc">Conversion of volume fraction to mass fraction for $\alpha$ phase</p>
                <span class="category-tag tag-vol">Volume Fractions</span>
                <button class="copy-btn" onclick="copyToClipboard('W_a = \\frac{V_a \\rho_a}{V_a \\rho_a + V_\\beta \\rho_\\beta}')">
                    <i class="far fa-copy"></i> Copy Equation
                </button>
            </div>
        </section>
        
        <section id="eutectic" class="section">
            <h2>Binary Eutectic System</h2>
            
            <div class="equation-card eutectic">
                <div class="equation">$W_e = \frac{P}{P + Q}$</div>
                <p class="equation-desc">Mass fraction of eutectic microconstituent</p>
                <span class="category-tag tag-eutectic">Eutectic System</span>
                <button class="copy-btn" onclick="copyToClipboard('W_e = \\frac{P}{P + Q}')">
                    <i class="far fa-copy"></i> Copy Equation
                </button>
            </div>
            
            <div class="equation-card eutectic">
                <div class="equation">$W_{a'} = \frac{Q}{P + Q}$</div>
                <p class="equation-desc">Mass fraction of primary $\alpha$ microconstituent</p>
                <span class="category-tag tag-eutectic">Eutectic System</span>
                <button class="copy-btn" onclick="copyToClipboard('W_{a\\'} = \\frac{Q}{P + Q}')">
                    <i class="far fa-copy"></i> Copy Equation
                </button>
            </div>
            
            <div class="equation-card eutectic">
                <div class="equation">$W_a = \frac{Q + R}{P + Q + R}$</div>
                <p class="equation-desc">Mass fraction of total $\alpha$ phase</p>
                <span class="category-tag tag-eutectic">Eutectic System</span>
                <button class="copy-btn" onclick="copyToClipboard('W_a = \\frac{Q + R}{P + Q + R}')">
                    <i class="far fa-copy"></i> Copy Equation
                </button>
            </div>
            
            <div class="equation-card eutectic">
                <div class="equation">$W_\beta = \frac{P}{P + Q + R}$</div>
                <p class="equation-desc">Mass fraction of $\beta$ phase</p>
                <span class="category-tag tag-eutectic">Eutectic System</span>
                <button class="copy-btn" onclick="copyToClipboard('W_\\beta = \\frac{P}{P + Q + R}')">
                    <i class="far fa-copy"></i> Copy Equation
                </button>
            </div>
        </section>
        
        <section id="fec" class="section">
            <h2>Fe–C Alloy System</h2>
            
            <div class="equation-card fec">
                <div class="equation">$W_\rho = \frac{C_0' + 0.022}{0.74}$</div>
                <p class="equation-desc">Mass fraction of pearlite in a hypoeutectoid Fe–C alloy</p>
                <span class="category-tag tag-fec">Fe-C System</span>
                <button class="copy-btn" onclick="copyToClipboard('W_\\rho = \\frac{C_0\\' + 0.022}{0.74}')">
                    <i class="far fa-copy"></i> Copy Equation
                </button>
            </div>
            
            <div class="equation-card fec">
                <div class="equation">$W_{a'} = \frac{0.76 - C_0'}{0.74}$</div>
                <p class="equation-desc">Mass fraction of proeutectoid $\alpha$ ferrite in a hypoeutectoid Fe–C alloy</p>
                <span class="category-tag tag-fec">Fe-C System</span>
                <button class="copy-btn" onclick="copyToClipboard('W_{a\\'} = \\frac{0.76 - C_0\\'}{0.74}')">
                    <i class="far fa-copy"></i> Copy Equation
                </button>
            </div>
            
            <div class="equation-card fec">
                <div class="equation">$W_\rho = \frac{6.70 - C_1'}{5.94}$</div>
                <p class="equation-desc">Mass fraction of pearlite in a hypereutectoid Fe–C alloy</p>
                <span class="category-tag tag-fec">Fe-C System</span>
                <button class="copy-btn" onclick="copyToClipboard('W_\\rho = \\frac{6.70 - C_1\\'}{5.94}')">
                    <i class="far fa-copy"></i> Copy Equation
                </button>
            </div>
            
            <div class="equation-card fec">
                <div class="equation">$W_{\text{Fe}_3\text{C}'} = \frac{C_1' - 0.76}{5.94}$</div>
                <p class="equation-desc">Mass fraction of proeutectoid $\text{Fe}_3\text{C}$ in a hypereutectoid Fe–C alloy</p>
                <span class="category-tag tag-fec">Fe-C System</span>
                <button class="copy-btn" onclick="copyToClipboard('W_{\\text{Fe}_3\\text{C}\\'} = \\frac{C_1\\' - 0.76}{5.94}')">
                    <i class="far fa-copy"></i> Copy Equation
                </button>
            </div>
        </section>
        
        <section id="thermo" class="section">
            <h2>Thermodynamics</h2>
            
            <div class="equation-card thermo">
                <div class="equation">$P + F = C + N$</div>
                <p class="equation-desc">Gibbs phase rule (general form)</p>
                <span class="category-tag tag-thermo">Thermodynamics</span>
                <button class="copy-btn" onclick="copyToClipboard('P + F = C + N')">
                    <i class="far fa-copy"></i> Copy Equation
                </button>
            </div>
        </section>
    </div>
    
    <footer>
        <div class="footer-content">
            <p>&copy; <span id="current-year"></span> Join TestUrSelf for your GATE Prep | TestUrSelf</p>
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
        
        // Copy to clipboard function
        function copyToClipboard(text) {
            navigator.clipboard.writeText(text).then(function() {
                // Show copied notification
                const notification = document.createElement('div');
                notification.textContent = 'Equation copied!';
                notification.style.position = 'fixed';
                notification.style.bottom = '20px';
                notification.style.left = '50%';
                notification.style.transform = 'translateX(-50%)';
                notification.style.backgroundColor = 'var(--success-color)';
                notification.style.color = 'white';
                notification.style.padding = '10px 20px';
                notification.style.borderRadius = '5px';
                notification.style.boxShadow = '0 2px 10px rgba(0,0,0,0.2)';
                notification.style.zIndex = '1000';
                notification.style.animation = 'fadeInOut 2s ease-in-out';
                
                document.body.appendChild(notification);
                
                // Remove notification after animation
                setTimeout(function() {
                    notification.remove();
                }, 2000);
            }, function(err) {
                console.error('Could not copy text: ', err);
            });
        }
        
        // Add animation for notification
        const style = document.createElement('style');
        style.textContent = `
            @keyframes fadeInOut {
                0% { opacity: 0; transform: translateX(-50%) translateY(20px); }
                20% { opacity: 1; transform: translateX(-50%) translateY(0); }
                80% { opacity: 1; transform: translateX(-50%) translateY(0); }
                100% { opacity: 0; transform: translateX(-50%) translateY(-20px); }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
