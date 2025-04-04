<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Phase Diagram Equations | TestUrSelf</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Roboto+Mono&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #1a365d;
            --secondary: #2c5282;
            --accent: #4299e1;
            --light: #ebf8ff;
            --dark: #2d3748;
            --text: #4a5568;
            --light-gray: #edf2f7;
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: var(--text);
            background-color: #f7fafc;
            padding: 0;
            margin: 0;
        }
        
        .header {
            padding: 1.5rem 2rem;
            border-bottom: 1px solid #e2e8f0;
            background-color: white;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .name-title {
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--dark);
        }
        
        .affiliations {
            font-size: 0.9rem;
            color: var(--text);
            margin-top: 0.2rem;
        }
        
        .nav {
            display: flex;
            gap: 1.5rem;
        }
        
        .nav-link {
            text-decoration: none;
            color: var(--text);
            font-weight: 500;
            transition: color 0.2s;
        }
        
        .nav-link:hover {
            color: var(--accent);
        }
        
        .container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 2rem;
        }
        
        .page-header {
            margin-bottom: 2rem;
        }
        
        .page-title {
            font-size: 2rem;
            font-weight: 700;
            color: var(--dark);
            margin-bottom: 0.5rem;
        }
        
        .page-date {
            color: #718096;
            font-size: 0.9rem;
            margin-bottom: 1.5rem;
        }
        
        .page-description {
            font-size: 1.1rem;
            color: var(--text);
            margin-bottom: 2rem;
            max-width: 800px;
        }
        
        .search-container {
            margin-bottom: 2rem;
        }
        
        #searchInput {
            width: 100%;
            max-width: 600px;
            padding: 0.8rem 1.2rem;
            border: 1px solid #cbd5e0;
            border-radius: 6px;
            font-size: 1rem;
            font-family: 'Inter', sans-serif;
            background-color: white;
            transition: all 0.2s;
        }
        
        #searchInput:focus {
            outline: none;
            border-color: var(--accent);
            box-shadow: 0 0 0 3px rgba(66, 153, 225, 0.2);
        }
        
        .categories {
            display: flex;
            gap: 1rem;
            margin-bottom: 1.5rem;
            overflow-x: auto;
            padding-bottom: 0.5rem;
        }
        
        .category {
            padding: 0.5rem 1rem;
            background-color: white;
            border: 1px solid #e2e8f0;
            border-radius: 6px;
            font-weight: 500;
            color: var(--dark);
            cursor: pointer;
            transition: all 0.2s;
            white-space: nowrap;
        }
        
        .category:hover, .category.active {
            background-color: var(--accent);
            color: white;
            border-color: var(--accent);
        }
        
        .equations-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
        }
        
        .equation-card {
            background-color: white;
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
            border: 1px solid #e2e8f0;
            transition: transform 0.2s, box-shadow 0.2s;
        }
        
        .equation-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        .equation {
            font-family: 'Roboto Mono', monospace;
            font-size: 1rem;
            background-color: var(--light-gray);
            padding: 0.8rem;
            border-radius: 6px;
            margin-bottom: 1rem;
            overflow-x: auto;
        }
        
        .equation-desc {
            font-size: 0.95rem;
            color: var(--text);
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                align-items: flex-start;
                gap: 1rem;
            }
            
            .nav {
                width: 100%;
                justify-content: space-between;
            }
            
            .categories {
                gap: 0.5rem;
            }
            
            .category {
                padding: 0.5rem 0.8rem;
                font-size: 0.9rem;
            }
            
            .equations-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <div class="header-content">
            <div>
                <div class="name-title">Samarjeet Kumar Singh</div>
                <div class="affiliations">Building, TestUrSelf | IISc Bengaluru | BOD, Kartavya | Materials</div>
            </div>
            <nav class="nav">
                <a href="#" class="nav-link">Home</a>
                <a href="#" class="nav-link">Projects</a>
                <a href="#" class="nav-link">Blog</a>
                <a href="#" class="nav-link">Archive</a>
            </nav>
        </div>
    </header>
    
    <main class="container">
        <div class="page-header">
            <h1 class="page-title">Phase Diagram Lever Rule Formulas</h1>
            <div class="page-date">April 04, 2025</div>
            <h2 class="page-title">Phase Diagram Equations</h2>
            <p class="page-description">Essential formulas for materials science and engineering</p>
        </div>
        
        <div class="search-container">
            <input type="text" id="searchInput" placeholder="Search equations...">
        </div>
        
        <div class="categories">
            <div class="category active">Binary Isomorphous</div>
            <div class="category">Volume Fractions</div>
            <div class="category">Eutectic System</div>
            <div class="category">Fe-C System</div>
            <div class="category">Thermodynamics</div>
        </div>
        
        <div class="equations-grid">
            <!-- Binary Isomorphous -->
            <div class="equation-card">
                <div class="equation">$W_L = \frac{C_a - C_0}{C_a - C_L}$</div>
                <p class="equation-desc">Mass fraction of liquid phase in a binary isomorphous system</p>
            </div>
            
            <div class="equation-card">
                <div class="equation">$W_a = \frac{C_0 - C_L}{C_a - C_L}$</div>
                <p class="equation-desc">Mass fraction of α solid-solution phase in a binary isomorphous system</p>
            </div>
            
            <!-- Volume Fractions -->
            <div class="equation-card">
                <div class="equation">$V_a = \frac{V_a}{V_a + V_\beta}$</div>
                <p class="equation-desc">Volume fraction of α phase</p>
            </div>
            
            <div class="equation-card">
                <div class="equation">$V_a = \frac{\rho_a}{\rho_a + \rho_\beta}$</div>
                <p class="equation-desc">Conversion of mass fraction to volume fraction for α phase</p>
            </div>
            
            <div class="equation-card">
                <div class="equation">$W_a = \frac{V_a \rho_a}{V_a \rho_a + V_\beta \rho_\beta}$</div>
                <p class="equation-desc">Conversion of volume fraction to mass fraction for α phase</p>
            </div>
            
            <!-- Eutectic System -->
            <div class="equation-card">
                <div class="equation">$W_e = \frac{P}{P + Q}$</div>
                <p class="equation-desc">Mass fraction of eutectic microconstituent</p>
            </div>
            
            <div class="equation-card">
                <div class="equation">$W_{a'} = \frac{Q}{P + Q}$</div>
                <p class="equation-desc">Mass fraction of primary α microconstituent</p>
            </div>
            
            <div class="equation-card">
                <div class="equation">$W_a = \frac{Q + R}{P + Q + R}$</div>
                <p class="equation-desc">Mass fraction of total α phase</p>
            </div>
            
            <div class="equation-card">
                <div class="equation">$W_\beta = \frac{P}{P + Q + R}$</div>
                <p class="equation-desc">Mass fraction of β phase</p>
            </div>
            
            <!-- Fe-C System -->
            <div class="equation-card">
                <div class="equation">$W_\rho = \frac{C_0' + 0.022}{0.74}$</div>
                <p class="equation-desc">Mass fraction of pearlite in a hypoeutectoid Fe-C alloy</p>
            </div>
            
            <div class="equation-card">
                <div class="equation">$W_{a'} = \frac{0.76 - C_0'}{0.74}$</div>
                <p class="equation-desc">Mass fraction of proeutectoid α ferrite in a hypoeutectoid Fe-C alloy</p>
            </div>
            
            <div class="equation-card">
                <div class="equation">$W_\rho = \frac{6.70 - C_1'}{5.94}$</div>
                <p class="equation-desc">Mass fraction of pearlite in a hypereutectoid Fe-C alloy</p>
            </div>
            
            <div class="equation-card">
                <div class="equation">$W_{\text{Fe}_3\text{C}'} = \frac{C_1' - 0.76}{5.94}$</div>
                <p class="equation-desc">Mass fraction of proeutectoid Fe₃C in a hypereutectoid Fe-C alloy</p>
            </div>
            
            <!-- Thermodynamics -->
            <div class="equation-card">
                <div class="equation">$P + F = C + N$</div>
                <p class="equation-desc">Gibbs phase rule (general form)</p>
            </div>
        </div>
    </main>

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
        // Category filtering
        const categories = document.querySelectorAll('.category');
        const equationCards = document.querySelectorAll('.equation-card');
        
        categories.forEach(category => {
            category.addEventListener('click', () => {
                categories.forEach(c => c.classList.remove('active'));
                category.classList.add('active');
                
                // In a real implementation, you would filter equations here
                // This is just a UI demonstration
            });
        });
        
        // Search functionality
        document.getElementById('searchInput').addEventListener('input', function() {
            const searchTerm = this.value.toLowerCase();
            
            equationCards.forEach(card => {
                const text = card.textContent.toLowerCase();
                if (text.includes(searchTerm)) {
                    card.style.display = 'block';
                } else {
                    card.style.display = 'none';
                }
            });
        });
    </script>
</body>
</html>
