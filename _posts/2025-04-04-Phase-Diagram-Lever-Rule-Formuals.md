<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Phase Diagram Equations | TestUrSelf</title>
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #1a252f;
            --text-color: #333;
            --highlight-color: #f39c12;
            --success-color: #27ae60;
            --error-color: #c0392b;
            --iso-color: #e74c3c;
            --vol-color: #3498db;
            --eutectic-color: #9b59b6;
            --fec-color: #f39c12;
            --thermo-color: #2ecc71;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            line-height: 1.8;
            color: var(--text-color);
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
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
            background: linear-gradient(135deg, #f5f7fa 0%, #e4e8eb 50%, #f5f7fa 100%);
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
            margin-bottom: 2rem;
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
            font-weight: 900;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            letter-spacing: 1px;
        }
        
        h2 {
            color: var(--primary-color);
            border-bottom: 4px solid var(--highlight-color);
            padding-bottom: 0.8rem;
            margin-top: 3rem;
            font-size: 2rem;
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
        
        h3 {
            color: var(--dark-color);
            margin-top: 2.5rem;
            font-size: 1.5rem;
            border-left: 5px solid var(--highlight-color);
            padding-left: 1rem;
            position: relative;
        }
        
        h3::before {
            content: "";
            position: absolute;
            left: 0;
            bottom: -5px;
            width: 50%;
            height: 2px;
            background: linear-gradient(to right, var(--highlight-color), transparent);
        }
        
        .section {
            background-color: white;
            border-radius: 12px;
            padding: 2rem;
            margin-bottom: 2rem;
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
        
        /* Table of Contents - Fixed Position */
        .toc-container {
            position: sticky;
            top: 20px;
            z-index: 5;
            margin-bottom: 2rem;
        }
        
        .toc {
            background-color: white;
            border-radius: 12px;
            padding: 1.5rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            max-height: 80vh;
            overflow-y: auto;
        }
        
        .toc h2 {
            margin-top: 0;
            text-align: left;
            padding-left: 0;
            position: sticky;
            top: 0;
            background: white;
            z-index: 1;
            padding-bottom: 1rem;
        }
        
        .toc ul {
            list-style-type: none;
            padding: 0;
            margin: 0;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 10px;
        }
        
        .toc li {
            margin-bottom: 0.5rem;
        }
        
        .toc a {
            display: block;
            padding: 0.8rem 1rem;
            background-color: var(--light-color);
            color: var(--primary-color);
            text-decoration: none;
            border-radius: 6px;
            transition: all 0.3s ease;
            font-weight: 500;
            border-left: 4px solid var(--secondary-color);
        }
        
        .toc a:hover {
            background-color: rgba(52, 152, 219, 0.1);
            transform: translateX(5px);
        }
        
        /* Equation Cards */
        .equation-card {
            background-color: white;
            border-radius: 8px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            border-top: 5px solid var(--secondary-color);
        }
        
        .equation-card.iso { border-top-color: var(--iso-color); }
        .equation-card.vol { border-top-color: var(--vol-color); }
        .equation-card.eutectic { border-top-color: var(--eutectic-color); }
        .equation-card.fec { border-top-color: var(--fec-color); }
        .equation-card.thermo { border-top-color: var(--thermo-color); }
        
        .equation-card:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .equation {
            font-family: 'Courier New', monospace;
            font-size: 1.1rem;
            background: #f8f9fa;
            padding: 1rem;
            border-radius: 4px;
            margin: 0.5rem 0;
            display: block;
            overflow-x: auto;
            white-space: nowrap;
        }
        
        .equation-desc {
            margin: 1rem 0;
            color: #555;
            line-height: 1.6;
        }
        
        .category-tag {
            display: inline-block;
            padding: 0.3rem 0.8rem;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 600;
            margin-top: 0.5rem;
            background-color: rgba(52, 152, 219, 0.1);
            color: var(--secondary-color);
        }
        
        .tag-iso { background-color: rgba(231, 76, 60, 0.1); color: var(--iso-color); }
        .tag-vol { background-color: rgba(52, 152, 219, 0.1); color: var(--vol-color); }
        .tag-eutectic { background-color: rgba(155, 89, 182, 0.1); color: var(--eutectic-color); }
        .tag-fec { background-color: rgba(243, 156, 18, 0.1); color: var(--fec-color); }
        .tag-thermo { background-color: rgba(46, 204, 113, 0.1); color: var(--thermo-color); }
        
        /* Key Points */
        .key-point {
            background: linear-gradient(to right, #f8f9fa, #e9ecef);
            border-left: 6px solid var(--highlight-color);
            padding: 1.5rem;
            margin: 2rem 0;
            border-radius: 0 8px 8px 0;
            position: relative;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
        }
        
        .key-point::before {
            content: "!";
            position: absolute;
            left: -15px;
            top: -15px;
            width: 30px;
            height: 30px;
            background-color: var(--highlight-color);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        
        /* Process Steps */
        .process-steps {
            counter-reset: step;
            margin: 2rem 0;
        }
        
        .process-step {
            position: relative;
            padding-left: 3.5rem;
            margin-bottom: 1.5rem;
            min-height: 2.5rem;
        }
        
        .process-step::before {
            counter-increment: step;
            content: counter(step);
            position: absolute;
            left: 0;
            top: 0;
            width: 2.2rem;
            height: 2.2rem;
            background: linear-gradient(to bottom right, var(--primary-color), var(--dark-color));
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            box-shadow: 0 3px 8px rgba(0,0,0,0.1);
        }
        
        /* Score Counter */
        .score-counter {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            color: white;
            padding: 1rem 1.5rem;
            border-radius: 50px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
            z-index: 10;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 100% {transform: translateY(0);}
            50% {transform: translateY(-5px);}
        }
        
        .score-counter i {
            font-size: 1.2rem;
        }
        
        /* Responsive adjustments */
        @media (max-width: 768px) {
            body {
                padding: 10px;
            }
            
            body::after {
                font-size: 80px;
            }
            
            header {
                padding: 2rem 1rem;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            h2 {
                font-size: 1.5rem;
            }
            
            .section {
                padding: 1.5rem;
            }
            
            .toc ul {
                grid-template-columns: 1fr;
            }
            
            .toc-container {
                position: static;
            }
            
            .toc {
                max-height: none;
            }
            
            .score-counter {
                bottom: 10px;
                right: 10px;
                padding: 0.8rem 1.2rem;
                font-size: 0.9rem;
            }
            
            .equation {
                white-space: pre-wrap;
                word-wrap: break-word;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700;900&display=swap" rel="stylesheet">
    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
</head>
<body>
    <header>
        <h1>Phase Diagram Equations</h1>
        <p>Essential formulas for materials science and engineering</p>
    </header>
    
    <div class="toc-container">
        <div class="toc">
            <h2>Table of Contents</h2>
            <ul>
                <li><a href="#binary-iso"><i class="fas fa-atom"></i> Binary Isomorphous System</a></li>
                <li><a href="#volume-fractions"><i class="fas fa-cube"></i> Volume Fractions</a></li>
                <li><a href="#binary-eutectic"><i class="fas fa-project-diagram"></i> Binary Eutectic System</a></li>
                <li><a href="#fec-system"><i class="fas fa-magnet"></i> Fe–C Alloy System</a></li>
                <li><a href="#thermodynamics"><i class="fas fa-fire"></i> Thermodynamics</a></li>
            </ul>
        </div>
    </div>
    
    <div class="container">
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
            
            <div class="key-point">
                <h4>Key Thermodynamic Relationships</h4>
                <ul>
                    <li>Gibbs free energy: $G = H - TS$</li>
                    <li>Chemical potential: $\mu_i = \left(\frac{\partial G}{\partial n_i}\right)_{T,P,n_j}$</li>
                    <li>Phase equilibrium condition: $\mu_i^\alpha = \mu_i^\beta$</li>
                </ul>
            </div>
        </section>
    </div>

    <div class="score-counter" id="scoreCounter">
        <i class="fas fa-star"></i> <span id="score">0</span> Points
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
        
        // Initialize elements
        document.addEventListener('DOMContentLoaded', function() {
            // Add scroll margin to account for fixed header
            document.querySelectorAll('h2').forEach(h2 => {
                h2.style.scrollMarginTop = '120px';
            });
        });
    </script>
</body>
</html>
