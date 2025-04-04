<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Phase Diagram Equations | TestUrSelf</title>
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --highlight: #f39c12;
            --text: #333;
            --iso: #e74c3c;
            --vol: #3498db;
            --eutectic: #9b59b6;
            --fec: #f39c12;
            --thermo: #2ecc71;
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: var(--text);
            background-color: #f5f5f5;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--dark));
            color: white;
            padding: 2rem 1rem;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        h1 {
            font-size: 2rem;
            margin-bottom: 0.5rem;
        }
        
        .container {
            max-width: 1000px;
            margin: 2rem auto;
            padding: 0 1rem;
        }
        
        .toc-container {
            background: white;
            border-radius: 8px;
            padding: 1.5rem;
            margin-bottom: 2rem;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .toc-title {
            color: var(--primary);
            border-bottom: 2px solid var(--highlight);
            padding-bottom: 0.5rem;
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }
        
        .toc-list {
            list-style-type: none;
            padding-left: 1rem;
        }
        
        .toc-item {
            margin-bottom: 0.8rem;
            position: relative;
            padding-left: 1.2rem;
        }
        
        .toc-item::before {
            content: "•";
            color: var(--secondary);
            position: absolute;
            left: 0;
        }
        
        .toc-link {
            color: var(--primary);
            text-decoration: none;
            transition: color 0.2s;
        }
        
        .toc-link:hover {
            color: var(--secondary);
            text-decoration: underline;
        }
        
        .section {
            background: white;
            border-radius: 8px;
            padding: 1.5rem;
            margin-bottom: 2rem;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            scroll-margin-top: 20px;
        }
        
        h2 {
            color: var(--primary);
            border-bottom: 2px solid var(--highlight);
            padding-bottom: 0.5rem;
            margin-bottom: 1.5rem;
            font-size: 1.5rem;
        }
        
        .equation-card {
            background: #f8f9fa;
            border-left: 4px solid var(--secondary);
            padding: 1.2rem;
            margin-bottom: 1.2rem;
            border-radius: 0 4px 4px 0;
        }
        
        .equation-card.iso { border-left-color: var(--iso); }
        .equation-card.vol { border-left-color: var(--vol); }
        .equation-card.eutectic { border-left-color: var(--eutectic); }
        .equation-card.fec { border-left-color: var(--fec); }
        .equation-card.thermo { border-left-color: var(--thermo); }
        
        .equation {
            font-family: monospace;
            font-size: 1.1rem;
            background: #e9ecef;
            padding: 0.8rem;
            border-radius: 4px;
            margin: 0.5rem 0;
            display: inline-block;
            width: 100%;
            overflow-x: auto;
        }
        
        .equation-desc {
            margin: 0.8rem 0;
            color: #555;
        }
        
        .category-tag {
            display: inline-block;
            padding: 0.3rem 0.8rem;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 500;
            margin-top: 0.5rem;
            background-color: rgba(52, 152, 219, 0.1);
            color: var(--secondary);
        }
        
        .tag-iso { background-color: rgba(231, 76, 60, 0.1); color: var(--iso); }
        .tag-vol { background-color: rgba(52, 152, 219, 0.1); color: var(--vol); }
        .tag-eutectic { background-color: rgba(155, 89, 182, 0.1); color: var(--eutectic); }
        .tag-fec { background-color: rgba(243, 156, 18, 0.1); color: var(--fec); }
        .tag-thermo { background-color: rgba(46, 204, 113, 0.1); color: var(--thermo); }
        
        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 1.5rem;
            margin-top: 2rem;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 1.8rem;
            }
            
            .container {
                padding: 0 0.5rem;
            }
            
            .section, .toc-container {
                padding: 1rem;
            }
        }
    </style>
    <!-- MathJax for LaTeX rendering -->
    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
</head>
<body>
    <header>
        <h1>Phase Diagram Equations</h1>
        <p>Essential formulas for materials science and engineering</p>
    </header>
    
    <div class="container">
        <div class="toc-container">
            <h2 class="toc-title">Table of Contents</h2>
            <ul class="toc-list">
                <li class="toc-item"><a href="#binary-iso" class="toc-link">Binary Isomorphous System</a></li>
                <li class="toc-item"><a href="#volume-fractions" class="toc-link">Volume Fractions</a></li>
                <li class="toc-item"><a href="#binary-eutectic" class="toc-link">Binary Eutectic System</a></li>
                <li class="toc-item"><a href="#fec-system" class="toc-link">Fe–C Alloy System</a></li>
                <li class="toc-item"><a href="#thermodynamics" class="toc-link">Thermodynamics</a></li>
            </ul>
        </div>
        
        <section id="binary-iso" class="section">
            <h2>Binary Isomorphous System</h2>
            
            <div class="equation-card iso">
                <div class="equation">$W_L = \frac{C_a - C_0}{C_a - C_L}$</div>
                <p class="equation-desc">The lever rule equation for calculating the mass fraction of liquid phase (W<sub>L</sub>) in a binary isomorphous system at a given temperature. Here, C<sub>a</sub> is the composition of the α phase, C<sub>0</sub> is the overall composition, and C<sub>L</sub> is the composition of the liquid phase.</p>
                <span class="category-tag tag-iso">Binary Isomorphous</span>
            </div>
            
            <div class="equation-card iso">
                <div class="equation">$W_a = \frac{C_0 - C_L}{C_a - C_L}$</div>
                <p class="equation-desc">Mass fraction of α solid-solution phase (W<sub>a</sub>) in a binary isomorphous system. This is the complementary equation to the liquid fraction calculation, using the same composition parameters.</p>
                <span class="category-tag tag-iso">Binary Isomorphous</span>
            </div>
        </section>
        
        <section id="volume-fractions" class="section">
            <h2>Volume Fractions</h2>
            
            <div class="equation-card vol">
                <div class="equation">$V_a = \frac{V_a}{V_a + V_\beta}$</div>
                <p class="equation-desc">Basic definition of volume fraction of α phase (V<sub>a</sub>), where V<sub>a</sub> is the volume of α phase and V<sub>β</sub> is the volume of β phase.</p>
                <span class="category-tag tag-vol">Volume Fractions</span>
            </div>
            
            <div class="equation-card vol">
                <div class="equation">$V_a = \frac{\frac{W_a}{\rho_a}}{\frac{W_a}{\rho_a} + \frac{W_\beta}{\rho_\beta}}$</div>
                <p class="equation-desc">Conversion of mass fraction to volume fraction for α phase, where W<sub>a</sub> and W<sub>β</sub> are mass fractions, and ρ<sub>a</sub> and ρ<sub>β</sub> are densities of the respective phases.</p>
                <span class="category-tag tag-vol">Volume Fractions</span>
            </div>
            
            <div class="equation-card vol">
                <div class="equation">$W_a = \frac{V_a \rho_a}{V_a \rho_a + V_\beta \rho_\beta}$</div>
                <p class="equation-desc">Conversion of volume fraction to mass fraction for α phase, using the densities of both phases.</p>
                <span class="category-tag tag-vol">Volume Fractions</span>
            </div>
        </section>
        
        <section id="binary-eutectic" class="section">
            <h2>Binary Eutectic System</h2>
            
            <div class="equation-card eutectic">
                <div class="equation">$W_e = \frac{P}{P + Q} = \frac{C_0 - C_a}{C_e - C_a}$</div>
                <p class="equation-desc">Mass fraction of eutectic microconstituent (W<sub>e</sub>) in a binary eutectic system, where P and Q represent lever arms on the phase diagram, C<sub>0</sub> is the overall composition, C<sub>a</sub> is the composition of primary α, and C<sub>e</sub> is the eutectic composition.</p>
                <span class="category-tag tag-eutectic">Eutectic System</span>
            </div>
            
            <div class="equation-card eutectic">
                <div class="equation">$W_{a'} = \frac{Q}{P + Q} = \frac{C_e - C_0}{C_e - C_a}$</div>
                <p class="equation-desc">Mass fraction of primary α microconstituent (W<sub>a'</sub>) that forms before the eutectic reaction in a hypoeutectic alloy.</p>
                <span class="category-tag tag-eutectic">Eutectic System</span>
            </div>
            
            <div class="equation-card eutectic">
                <div class="equation">$W_a = \frac{Q + R}{P + Q + R} = \frac{C_\beta - C_0}{C_\beta - C_a}$</div>
                <p class="equation-desc">Mass fraction of total α phase (both primary and eutectic α) in a binary eutectic system, where C<sub>β</sub> is the composition of the β phase.</p>
                <span class="category-tag tag-eutectic">Eutectic System</span>
            </div>
            
            <div class="equation-card eutectic">
                <div class="equation">$W_\beta = \frac{P}{P + Q + R} = \frac{C_0 - C_a}{C_\beta - C_a}$</div>
                <p class="equation-desc">Mass fraction of β phase (W<sub>β</sub>) in a binary eutectic system, which includes both eutectic β and any proeutectic β in hypereutectic alloys.</p>
                <span class="category-tag tag-eutectic">Eutectic System</span>
            </div>
        </section>
        
        <section id="fec-system" class="section">
            <h2>Fe–C Alloy System</h2>
            
            <div class="equation-card fec">
                <div class="equation">$W_\rho = \frac{C_0' - 0.022}{0.74}$</div>
                <p class="equation-desc">Mass fraction of pearlite (W<sub>ρ</sub>) in a hypoeutectoid Fe–C alloy, where C<sub>0</sub>' is the carbon content in wt% (between 0.022 and 0.76 wt%).</p>
                <span class="category-tag tag-fec">Fe-C System</span>
            </div>
            
            <div class="equation-card fec">
                <div class="equation">$W_{a'} = \frac{0.76 - C_0'}{0.74}$</div>
                <p class="equation-desc">Mass fraction of proeutectoid α ferrite (W<sub>a'</sub>) that forms above the eutectoid temperature in a hypoeutectoid Fe–C alloy.</p>
                <span class="category-tag tag-fec">Fe-C System</span>
            </div>
            
            <div class="equation-card fec">
                <div class="equation">$W_\rho = \frac{6.70 - C_1'}{5.94}$</div>
                <p class="equation-desc">Mass fraction of pearlite (W<sub>ρ</sub>) in a hypereutectoid Fe–C alloy, where C<sub>1</sub>' is the carbon content in wt% (between 0.76 and 2.14 wt%).</p>
                <span class="category-tag tag-fec">Fe-C System</span>
            </div>
            
            <div class="equation-card fec">
                <div class="equation">$W_{\text{Fe}_3\text{C}'} = \frac{C_1' - 0.76}{5.94}$</div>
                <p class="equation-desc">Mass fraction of proeutectoid cementite (W<sub>Fe<sub>3</sub>C'</sub>) that forms above the eutectoid temperature in a hypereutectoid Fe–C alloy.</p>
                <span class="category-tag tag-fec">Fe-C System</span>
            </div>
        </section>
        
        <section id="thermodynamics" class="section">
            <h2>Thermodynamics</h2>
            
            <div class="equation-card thermo">
                <div class="equation">$P + F = C + N$</div>
                <p class="equation-desc">Gibbs phase rule (general form), where P is the number of phases, F is the number of degrees of freedom, C is the number of components, and N is the number of non-compositional variables (typically 2 for temperature and pressure).</p>
                <span class="category-tag tag-thermo">Thermodynamics</span>
            </div>
        </section>
    </div>
    
    <footer>
        <p>&copy; <script>document.write(new Date().getFullYear())</script> TestUrSelf - GATE Preparation</p>
    </footer>

    <script>
        // MathJax configuration
        MathJax = {
            tex: {
                inlineMath: [['$', '$'], ['\\(', '\\)']]
            }
        };
        
        // Smooth scrolling for TOC links
        document.querySelectorAll('.toc-link').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                document.querySelector(targetId).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
