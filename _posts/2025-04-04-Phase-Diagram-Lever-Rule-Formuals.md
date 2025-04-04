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
        
        /* Table of Contents */
        .toc {
            background-color: white;
            border-radius: 12px;
            padding: 2rem;
            margin: 2rem auto;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
            z-index: 1;
        }
        
        .toc h2 {
            text-align: left;
            padding-left: 0;
            background: none;
            border-bottom: 2px solid var(--highlight-color);
        }
        
        .toc ul {
            list-style-type: none;
            padding-left: 1rem;
        }
        
        .toc li {
            margin-bottom: 0.8rem;
            position: relative;
            padding-left: 1.5rem;
        }
        
        .toc li::before {
            content: "•";
            color: var(--secondary-color);
            font-weight: bold;
            position: absolute;
            left: 0;
        }
        
        .toc a {
            color: var(--dark-color);
            text-decoration: none;
            transition: all 0.2s ease;
        }
        
        .toc a:hover {
            color: var(--secondary-color);
            text-decoration: underline;
        }
        
        /* Introduction section */
        .intro {
            background-color: white;
            border-radius: 12px;
            padding: 2rem;
            margin: 2rem auto;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .intro p {
            margin-bottom: 1rem;
            line-height: 1.7;
        }
        
        /* Example styling */
        .example {
            background-color: #f0f8ff;
            border-left: 4px solid var(--secondary-color);
            padding: 1.2rem;
            margin: 1.2rem 0;
            border-radius: 0 8px 8px 0;
        }
        
        .example-title {
            font-weight: 600;
            color: var(--secondary-color);
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .example-title i {
            font-size: 1.1rem;
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
            
            .toc, .intro {
                padding: 1.5rem;
                margin: 1rem;
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
            <a href="#introduction" class="nav-link active">Introduction</a>
            <a href="#toc" class="nav-link">Table of Contents</a>
            <a href="#binary-iso" class="nav-link">Binary Isomorphous</a>
            <a href="#volume-fractions" class="nav-link">Volume Fractions</a>
            <a href="#eutectic" class="nav-link">Eutectic System</a>
            <a href="#fec" class="nav-link">Fe-C System</a>
            <a href="#thermo" class="nav-link">Thermodynamics</a>
        </div>
    </nav>
    
    <div class="container">
        <section id="introduction" class="intro">
            <h2>Introduction to Phase Diagrams</h2>
            <p>Phase diagrams are graphical representations of the physical states of a substance under different conditions of temperature and pressure. They are essential tools in materials science and engineering, providing valuable information about phase stability, phase transformations, and the equilibrium conditions between different phases.</p>
            
            <p>This reference guide covers the fundamental equations used to analyze binary phase diagrams, including isomorphous systems, eutectic systems, and the important iron-carbon system. Each equation is accompanied by a clear explanation and practical examples to help you understand and apply these concepts in your studies and research.</p>
            
            <p>The equations presented here are particularly relevant for students preparing for competitive exams like GATE in Materials Science and Metallurgical Engineering, as well as for professionals working in materials characterization and development.</p>
        </section>
        
        <section id="toc" class="toc">
            <h2>Table of Contents</h2>
            <ul>
                <li><a href="#binary-iso">Binary Isomorphous System</a></li>
                <li><a href="#volume-fractions">Volume Fractions Calculations</a></li>
                <li><a href="#eutectic">Binary Eutectic System</a></li>
                <li><a href="#fec">Fe-C Alloy System</a></li>
                <li><a href="#thermo">Thermodynamic Principles</a></li>
            </ul>
        </section>
        
        <div class="search-container">
            <input type="text" id="searchInput" placeholder="Search equations...">
        </div>
        
        <section id="binary-iso" class="section">
            <h2>Binary Isomorphous System</h2>
            
            <div class="equation-card iso">
                <div class="equation">$W_L = \frac{C_a - C_0}{C_a - C_L}$</div>
                <p class="equation-desc">The lever rule equation for calculating the mass fraction of liquid phase (W<sub>L</sub>) in a binary isomorphous system at a given temperature. Here, C<sub>a</sub> is the composition of the α phase, C<sub>0</sub> is the overall composition, and C<sub>L</sub> is the composition of the liquid phase.</p>
                
                <div class="example">
                    <div class="example-title"><i class="fas fa-lightbulb"></i> Example Calculation</div>
                    <p>For a Cu-Ni alloy with overall composition C<sub>0</sub> = 45 wt% Ni, at a temperature where the liquid composition C<sub>L</sub> = 32 wt% Ni and solid composition C<sub>a</sub> = 53 wt% Ni:</p>
                    <p>$W_L = \frac{53 - 45}{53 - 32} = \frac{8}{21} ≈ 0.38$ or 38% liquid</p>
                    <p>$W_a = 1 - W_L = 62%$ solid</p>
                </div>
                
                <span class="category-tag tag-iso">Binary Isomorphous</span>
            </div>
            
            <div class="equation-card iso">
                <div class="equation">$W_a = \frac{C_0 - C_L}{C_a - C_L}$</div>
                <p class="equation-desc">Mass fraction of α solid-solution phase (W<sub>a</sub>) in a binary isomorphous system. This is the complementary equation to the liquid fraction calculation, using the same composition parameters.</p>
                
                <div class="example">
                    <div class="example-title"><i class="fas fa-lightbulb"></i> Example Application</div>
                    <p>For a 60 wt% Cu-40 wt% Ni alloy at 1300°C, where the phase compositions are C<sub>L</sub> = 35 wt% Ni and C<sub>a</sub> = 46 wt% Ni:</p>
                    <p>$W_a = \frac{40 - 35}{46 - 35} = \frac{5}{11} ≈ 0.45$ or 45% solid</p>
                    <p>This means 45% of the alloy is solid solution and 55% remains liquid at this temperature.</p>
                </div>
                
                <span class="category-tag tag-iso">Binary Isomorphous</span>
            </div>
        </section>
        
        <section id="volume-fractions" class="section">
            <h2>Volume Fractions</h2>
            
            <div class="equation-card vol">
                <div class="equation">$V_a = \frac{V_a}{V_a + V_\beta}$</div>
                <p class="equation-desc">Basic definition of volume fraction of α phase (V<sub>a</sub>), where V<sub>a</sub> is the volume of α phase and V<sub>β</sub> is the volume of β phase.</p>
                
                <div class="example">
                    <div class="example-title"><i class="fas fa-lightbulb"></i> Practical Measurement</div>
                    <p>If microscopic analysis reveals that in a given microstructure, the α phase occupies 12 μm<sup>3</sup> and the β phase occupies 18 μm<sup>3</sup>:</p>
                    <p>$V_a = \frac{12}{12 + 18} = 0.4$ or 40%</p>
                    <p>This means 40% of the total volume is α phase and 60% is β phase.</p>
                </div>
                
                <span class="category-tag tag-vol">Volume Fractions</span>
            </div>
            
            <div class="equation-card vol">
                <div class="equation">$V_a = \frac{\frac{W_a}{\rho_a}}{\frac{W_a}{\rho_a} + \frac{W_\beta}{\rho_\beta}}$</div>
                <p class="equation-desc">Conversion of mass fraction to volume fraction for α phase, where W<sub>a</sub> and W<sub>β</sub> are mass fractions, and ρ<sub>a</sub> and ρ<sub>β</sub> are densities of the respective phases.</p>
                
                <div class="example">
                    <div class="example-title"><i class="fas fa-lightbulb"></i> Density Conversion</div>
                    <p>For an alloy with W<sub>a</sub> = 0.3 (30% α phase) with ρ<sub>a</sub> = 8.9 g/cm<sup>3</sup> and W<sub>β</sub> = 0.7 (70% β phase) with ρ<sub>β</sub> = 7.2 g/cm<sup>3</sup>:</p>
                    <p>$V_a = \frac{\frac{0.3}{8.9}}{\frac{0.3}{8.9} + \frac{0.7}{7.2}} = \frac{0.0337}{0.0337 + 0.0972} ≈ 0.257$ or 25.7%</p>
                    <p>Despite having 30% by mass, the α phase occupies only about 25.7% by volume due to its higher density.</p>
                </div>
                
                <span class="category-tag tag-vol">Volume Fractions</span>
            </div>
            
            <div class="equation-card vol">
                <div class="equation">$W_a = \frac{V_a \rho_a}{V_a \rho_a + V_\beta \rho_\beta}$</div>
                <p class="equation-desc">Conversion of volume fraction to mass fraction for α phase, using the densities of both phases.</p>
                
                <div class="example">
                    <div class="example-title"><i class="fas fa-lightbulb"></i> Reverse Calculation</div>
                    <p>Given a material with V<sub>a</sub> = 0.4 (40% α phase by volume), ρ<sub>a</sub> = 4.5 g/cm<sup>3</sup>, and V<sub>β</sub> = 0.6 (60% β phase by volume), ρ<sub>β</sub> = 3.2 g/cm<sup>3</sup>:</p>
                    <p>$W_a = \frac{0.4 × 4.5}{(0.4 × 4.5) + (0.6 × 3.2)} = \frac{1.8}{1.8 + 1.92} ≈ 0.484$ or 48.4%</p>
                    <p>The α phase accounts for 48.4% of the mass despite occupying only 40% of the volume.</p>
                </div>
                
                <span class="category-tag tag-vol">Volume Fractions</span>
            </div>
        </section>
        
        <section id="eutectic" class="section">
            <h2>Binary Eutectic System</h2>
            
            <div class="equation-card eutectic">
                <div class="equation">$W_e = \frac{P}{P + Q} = \frac{C_0 - C_a}{C_e - C_a}$</div>
                <p class="equation-desc">Mass fraction of eutectic microconstituent (W<sub>e</sub>) in a binary eutectic system, where P and Q represent lever arms on the phase diagram, C<sub>0</sub> is the overall composition, C<sub>a</sub> is the composition of primary α, and C<sub>e</sub> is the eutectic composition.</p>
                
                <div class="example">
                    <div class="example-title"><i class="fas fa-lightbulb"></i> Eutectic Calculation</div>
                    <p>For a Pb-Sn alloy with C<sub>0</sub> = 40 wt% Sn, where the eutectic composition C<sub>e</sub> = 61.9 wt% Sn and the maximum solubility C<sub>a</sub> = 18.3 wt% Sn:</p>
                    <p>$W_e = \frac{40 - 18.3}{61.9 - 18.3} = \frac{21.7}{43.6} ≈ 0.498$ or 49.8%</p>
                    <p>This means about half of the alloy's mass is eutectic microstructure at room temperature.</p>
                </div>
                
                <span class="category-tag tag-eutectic">Eutectic System</span>
            </div>
            
            <div class="equation-card eutectic">
                <div class="equation">$W_{a'} = \frac{Q}{P + Q} = \frac{C_e - C_0}{C_e - C_a}$</div>
                <p class="equation-desc">Mass fraction of primary α microconstituent (W<sub>a'</sub>) that forms before the eutectic reaction in a hypoeutectic alloy.</p>
                
                <div class="example">
                    <div class="example-title"><i class="fas fa-lightbulb"></i> Primary Phase Calculation</div>
                    <p>Using the same Pb-Sn alloy (C<sub>0</sub> = 40 wt% Sn):</p>
                    <p>$W_{a'} = \frac{61.9 - 40}{61.9 - 18.3} = \frac{21.9}{43.6} ≈ 0.502$ or 50.2%</p>
                    <p>This matches our previous calculation since W<sub>e</sub> + W<sub>a'</sub> should equal 1 (49.8% + 50.2% = 100%).</p>
                </div>
                
                <span class="category-tag tag-eutectic">Eutectic System</span>
            </div>
            
            <div class="equation-card eutectic">
                <div class="equation">$W_a = \frac{Q + R}{P + Q + R} = \frac{C_\beta - C_0}{C_\beta - C_a}$</div>
                <p class="equation-desc">Mass fraction of total α phase (both primary and eutectic α) in a binary eutectic system, where C<sub>β</sub> is the composition of the β phase.</p>
                
                <div class="example">
                    <div class="example-title"><i class="fas fa-lightbulb"></i> Total Alpha Phase</div>
                    <p>For our Pb-Sn example (C<sub>0</sub> = 40 wt% Sn), with C<sub>β</sub> = 97.8 wt% Sn at room temperature:</p>
                    <p>$W_a = \frac{97.8 - 40}{97.8 - 18.3} = \frac{57.8}{79.5} ≈ 0.727$ or 72.7%</p>
                    <p>This indicates that 72.7% of the alloy is α phase (both primary and eutectic α combined).</p>
                </div>
                
                <span class="category-tag tag-eutectic">Eutectic System</span>
            </div>
            
            <div class="equation-card eutectic">
                <div class="equation">$W_\beta = \frac{P}{P + Q + R} = \frac{C_0 - C_a}{C_\beta - C_a}$</div>
                <p class="equation-desc">Mass fraction of β phase (W<sub>β</sub>) in a binary eutectic system, which includes both eutectic β and any proeutectic β in hypereutectic alloys.</p>
                
                <div class="example">
                    <div class="example-title"><i class="fas fa-lightbulb"></i> Beta Phase Fraction</div>
                    <p>Continuing with our Pb-Sn alloy:</p>
                    <p>$W_\beta = \frac{40 - 18.3}{97.8 - 18.3} = \frac{21.7}{79.5} ≈ 0.273$ or 27.3%</p>
                    <p>This complements the total α phase calculation (72.7% α + 27.3% β = 100%).</p>
                </div>
                
                <span class="category-tag tag-eutectic">Eutectic System</span>
            </div>
        </section>
        
        <section id="fec" class="section">
            <h2>Fe–C Alloy System</h2>
            
            <div class="equation-card fec">
                <div class="equation">$W_\rho = \frac{C_0' - 0.022}{0.74}$</div>
                <p class="equation-desc">Mass fraction of pearlite (W<sub>ρ</sub>) in a hypoeutectoid Fe–C alloy, where C<sub>0</sub>' is the carbon content in wt% (between 0.022 and 0.76 wt%).</p>
                
                <div class="example">
                    <div class="example-title"><i class="fas fa-lightbulb"></i> Pearlite in Steel</div>
                    <p>For a 0.4 wt% C steel:</p>
                    <p>$W_\rho = \frac{0.40 - 0.022}{0.74} ≈ 0.511$ or 51.1%</p>
                    <p>This steel would consist of about 51% pearlite and 49% proeutectoid ferrite at room temperature.</p>
                </div>
                
                <span class="category-tag tag-fec">Fe-C System</span>
            </div>
            
            <div class="equation-card fec">
                <div class="equation">$W_{a'} = \frac{0.76 - C_0'}{0.74}$</div>
                <p class="equation-desc">Mass fraction of proeutectoid α ferrite (W<sub>a'</sub>) that forms above the eutectoid temperature in a hypoeutectoid Fe–C alloy.</p>
                
                <div class="example">
                    <div class="example-title"><i class="fas fa-lightbulb"></i> Proeutectoid Ferrite</div>
                    <p>For the same 0.4 wt% C steel:</p>
                    <p>$W_{a'} = \frac{0.76 - 0.40}{0.74} ≈ 0.486$ or 48.6%</p>
                    <p>This confirms our previous calculation (51.4% pearlite + 48.6% ferrite ≈ 100%).</p>
                </div>
                
                <span class="category-tag tag-fec">Fe-C System</span>
            </div>
            
            <div class="equation-card fec">
                <div class="equation">$W_\rho = \frac{6.70 - C_1'}{5.94}$</div>
                <p class="equation-desc">Mass fraction of pearlite (W<sub>ρ</sub>) in a hypereutectoid Fe–C alloy, where C<sub>1</sub>' is the carbon content in wt% (between 0.76 and 2.14 wt%).</p>
                
                <div class="example">
                    <div class="example-title"><i class="fas fa-lightbulb"></i> Hyperectoid Pearlite</div>
                    <p>For a 1.2 wt% C steel:</p>
                    <p>$W_\rho = \frac{6.70 - 1.20}{5.94} ≈ 0.926$ or 92.6%</p>
                    <p>The microstructure would be about 92.6% pearlite and 7.4% proeutectoid cementite.</p>
                </div>
                
                <span class="category-tag tag-fec">Fe-C System</span>
            </div>
            
            <div class="equation-card fec">
                <div class="equation">$W_{\text{Fe}_3\text{C}'} = \frac{C_1' - 0.76}{5.94}$</div>
                <p class="equation-desc">Mass fraction of proeutectoid cementite (W<sub>Fe<sub>3</sub>C'</sub>) that forms above the eutectoid temperature in a hypereutectoid Fe–C alloy.</p>
                
                <div class="example">
                    <div class="example-title"><i class="fas fa-lightbulb"></i> Proeutectoid Cementite</div>
                    <p>For the 1.2 wt% C steel:</p>
                    <p>$W_{\text{Fe}_3\text{C}'} = \frac{1.20 - 0.76}{5.94} ≈ 0.074$ or 7.4%</p>
                    <p>This matches our previous pearlite calculation (92.6% + 7.4% = 100%).</p>
                </div>
                
                <span class="category-tag tag-fec">Fe-C System</span>
            </div>
        </section>
        
        <section id="thermo" class="section">
            <h2>Thermodynamics</h2>
            
            <div class="equation-card thermo">
                <div class="equation">$P + F = C + N$</div>
                <p class="equation-desc">Gibbs phase rule (general form), where P is the number of phases, F is the number of degrees of freedom, C is the number of components, and N is the number of non-compositional variables (typically 2 for temperature and pressure).</p>
                
                <div class="example">
                    <div class="example-title"><i class="fas fa-lightbulb"></i> Phase Rule Application</div>
                    <p>For a single-component system (C=1) with two phases (P=2) at fixed pressure (N=1):</p>
                    <p>$F = C + N - P = 1 + 1 - 2 = 0$</p>
                    <p>This means there are no degrees of freedom - the temperature is fixed at the phase transition point (e.g., melting point at given pressure).</p>
                </div>
                
                <span class="category-tag tag-thermo">Thermodynamics</span>
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
    </script>
</body>
</html>
