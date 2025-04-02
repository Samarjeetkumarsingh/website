<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GATE MT - Mineral Processing & Extractive Metallurgy</title>
    <style>
        :root {
            --primary-color: #2e7d32;
            --secondary-color: #ff8f00;
            --accent-color: #1b5e20;
            --light-color: #e8f5e9;
            --dark-color: #1b5e20;
            --text-color: #212121;
            --highlight-color: #ffd600;
            --success-color: #2e7d32;
            --mineral-color: #4caf50;
            --extractive-color: #ff9800;
            --steel-color: #607d8b;
            --slag-color: #795548;
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
        
        /* Animated Ore Texture Background */
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                linear-gradient(135deg, rgba(76,175,80,0.05) 0%, rgba(255,152,0,0.05) 50%, rgba(96,125,139,0.05) 100%),
                url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect fill="%234caf50" opacity="0.05" width="10" height="10" x="20" y="20"/><rect fill="%23ff9800" opacity="0.05" width="15" height="15" x="60" y="30"/><rect fill="%23607d8b" opacity="0.05" width="12" height="12" x="40" y="70"/></svg>');
            background-size: 200% 200%, 100px 100px;
            animation: gradientBG 15s ease infinite;
            z-index: -2;
        }
        
        @keyframes gradientBG {
            0% {background-position: 0% 50%, 0 0;}
            50% {background-position: 100% 50%, 50px 50px;}
            100% {background-position: 0% 50%, 0 0;}
        }
        
        /* Large Diagonal Watermark */
        body::after {
            content: "TestUrSelf";
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-30deg);
            font-size: 120px;
            font-weight: bold;
            color: rgba(46, 125, 50, 0.05);
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
            margin-bottom: 3rem;
            box-shadow: 0 8px 25px rgba(0,0,0,0.2);
            position: relative;
            z-index: 1;
            overflow: hidden;
            border-bottom: 5px solid var(--secondary-color);
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
            font-size: 2.8rem;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            letter-spacing: 1px;
        }
        
        h2 {
            color: var(--primary-color);
            border-bottom: 3px solid var(--accent-color);
            padding-bottom: 0.8rem;
            margin-top: 3rem;
            font-size: 2.2rem;
            background: linear-gradient(to right, transparent, var(--light-color), transparent);
            padding: 1rem 0;
            text-align: center;
            border-radius: 8px;
            position: relative;
        }
        
        h2::after {
            content: "";
            position: absolute;
            bottom: -3px;
            left: 25%;
            width: 50%;
            height: 3px;
            background: linear-gradient(to right, transparent, var(--secondary-color), transparent);
        }
        
        h3 {
            color: var(--dark-color);
            margin-top: 2.5rem;
            font-size: 1.8rem;
            border-left: 5px solid var(--accent-color);
            padding-left: 1.5rem;
            position: relative;
        }
        
        h3::before {
            content: "";
            position: absolute;
            left: 0;
            bottom: -5px;
            width: 50%;
            height: 2px;
            background: linear-gradient(to right, var(--accent-color), transparent);
        }
        
        h4 {
            color: #424242;
            margin-top: 1.8rem;
            font-size: 1.4rem;
            position: relative;
            display: inline-block;
        }
        
        h4::after {
            content: "";
            position: absolute;
            left: 0;
            bottom: -5px;
            width: 100%;
            height: 2px;
            background: linear-gradient(to right, currentColor, transparent);
        }
        
        .section {
            background-color: white;
            border-radius: 12px;
            padding: 2.5rem;
            margin-bottom: 3rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
            z-index: 1;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(0,0,0,0.05);
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }
        
        .subsection {
            margin-left: 1.5rem;
            border-left: 3px solid #e0e0e0;
            padding-left: 2rem;
            margin-top: 2rem;
            transition: border-color 0.3s ease;
        }
        
        .subsection:hover {
            border-left-color: var(--accent-color);
        }
        
        .topic-card {
            background-color: var(--light-color);
            border-radius: 10px;
            padding: 2rem;
            margin: 2rem 0;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
            position: relative;
            overflow: hidden;
        }
        
        .topic-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--primary-color), var(--secondary-color));
        }
        
        .important {
            background: linear-gradient(to right, #fff8e1, #fffde7);
            border-left: 6px solid var(--highlight-color);
            padding: 1.8rem;
            margin: 2.5rem 0;
            border-radius: 0 10px 10px 0;
            position: relative;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
        }
        
        .important::before {
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
        
        .formula {
            font-family: 'Courier New', monospace;
            background-color: #f5f5f5;
            padding: 1.2rem 1.8rem;
            border-radius: 8px;
            overflow-x: auto;
            margin: 1.5rem 0;
            border-left: 5px solid var(--accent-color);
            font-size: 1.2rem;
            position: relative;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        
        .formula::before {
            content: "≡";
            position: absolute;
            left: -25px;
            top: 50%;
            transform: translateY(-50%);
            color: var(--accent-color);
            font-size: 1.5rem;
        }
        
        .key-points {
            background: linear-gradient(to right, #e8f5e9, #f1f8e9);
            padding: 1.8rem;
            border-radius: 10px;
            margin: 2.5rem 0;
            border-left: 6px solid var(--success-color);
            position: relative;
        }
        
        .key-points::before {
            content: "★";
            position: absolute;
            left: -15px;
            top: -15px;
            width: 30px;
            height: 30px;
            background-color: var(--success-color);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1rem;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 2.5rem 0;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            border-radius: 8px;
            overflow: hidden;
        }
        
        th, td {
            padding: 1.2rem;
            text-align: left;
            border-bottom: 1px solid #e0e0e0;
        }
        
        th {
            background: linear-gradient(to right, var(--primary-color), var(--dark-color));
            color: white;
            font-weight: 500;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            font-size: 0.9rem;
        }
        
        tr:nth-child(even) {
            background-color: #f9f9f9;
        }
        
        tr:hover {
            background-color: #f0f0f0;
        }
        
        .toc {
            background-color: white;
            padding: 2.5rem;
            border-radius: 12px;
            margin-bottom: 3rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
        }
        
        footer {
            text-align: center;
            margin-top: 4rem;
            padding: 2.5rem;
            color: var(--primary-color);
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .example {
            background-color: #e3f2fd;
            border-left: 5px solid var(--extractive-color);
            padding: 1.8rem;
            margin: 2rem 0;
            border-radius: 0 10px 10px 0;
            position: relative;
        }
        
        .example::before {
            content: "Example";
            position: absolute;
            left: 0;
            top: -12px;
            background-color: var(--extractive-color);
            color: white;
            padding: 0.3rem 1rem;
            border-radius: 4px;
            font-size: 0.8rem;
            font-weight: bold;
        }
        
        .definition {
            background-color: #f5f5f5;
            border-left: 5px solid #9e9e9e;
            padding: 1.8rem;
            margin: 2rem 0;
            border-radius: 0 10px 10px 0;
            font-style: italic;
            position: relative;
        }
        
        .definition::before {
            content: "Definition";
            position: absolute;
            left: 0;
            top: -12px;
            background-color: #9e9e9e;
            color: white;
            padding: 0.3rem 1rem;
            border-radius: 4px;
            font-size: 0.8rem;
            font-weight: bold;
            font-style: normal;
        }
        
        /* Color-coded sections */
        .mineral {
            border-top: 4px solid var(--mineral-color);
        }
        
        .extractive {
            border-top: 4px solid var(--extractive-color);
        }
        
        .steel {
            border-top: 4px solid var(--steel-color);
        }
        
        .slag {
            border-top: 4px solid var(--slag-color);
        }
        
        /* Responsive adjustments */
        @media (max-width: 768px) {
            body {
                padding: 10px;
            }
            
            header {
                padding: 2rem 1rem;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .section {
                padding: 1.5rem;
            }
            
            .subsection {
                margin-left: 0.5rem;
                padding-left: 1rem;
            }
            
            body::after {
                font-size: 60px;
            }
        }
        
        /* Animation for formulas */
        @keyframes pulse {
            0% {transform: scale(1);}
            50% {transform: scale(1.02);}
            100% {transform: scale(1);}
        }
        
        .formula:hover {
            animation: pulse 1s ease;
        }
        
        /* Process flow diagram styling */
        .process-flow {
            background-color: #f5f5f5;
            padding: 1.5rem;
            border-radius: 8px;
            margin: 2rem 0;
            position: relative;
        }
        
        .process-step {
            background-color: white;
            border: 2px solid var(--primary-color);
            border-radius: 50%;
            width: 60px;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto;
            position: relative;
            z-index: 1;
            font-weight: bold;
            box-shadow: 0 3px 6px rgba(0,0,0,0.1);
        }
        
        .process-arrow {
            position: relative;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .process-arrow::after {
            content: "↓";
            font-size: 2rem;
            color: var(--primary-color);
        }
        
        /* Periodic table highlight */
        .element {
            display: inline-block;
            width: 40px;
            height: 40px;
            margin: 2px;
            text-align: center;
            line-height: 40px;
            font-weight: bold;
            border-radius: 4px;
            background-color: #e0e0e0;
            transition: all 0.3s ease;
        }
        
        .element:hover {
            transform: scale(1.2);
            box-shadow: 0 0 10px rgba(0,0,0,0.2);
        }
        
        .metal {
            background-color: #ffcc80;
        }
        
        .transition {
            background-color: #ffab91;
        }
        
        .alkali {
            background-color: #ff8a65;
        }
    </style>
</head>
<body>
    <header>
        <h1>Mineral Processing & Extractive Metallurgy</h1>
        <p>Complete Guide for GATE Metallurgy (MT) - Section 4 (TestUrSelf)</p>
    </header>

    <div class="toc">
        <h2>Table of Contents</h2>
        <ol>
            <li><a href="#mineral-processing">Mineral Processing</a></li>
            <li><a href="#extractive">Extractive Metallurgy</a></li>
            <li><a href="#iron-steel">Iron & Steel Making</a></li>
            <li><a href="#slag">Slag Properties</a></li>
            <li><a href="#steel-making">Steel Making Processes</a></li>
            <li><a href="#casting">Continuous Casting</a></li>
        </ol>
    </div>

    <div class="section mineral" id="mineral-processing">
        <h2>4.1 Mineral Processing</h2>
        
        <div class="subsection" id="comminution">
            <h3>Comminution Techniques</h3>
            <div class="topic-card">
                <div class="definition">
                    Comminution is the process of reducing the size of ore particles to liberate valuable minerals from waste rock.
                </div>
                
                <h4>Crushing and Grinding Equipment</h4>
                <table>
                    <tr>
                        <th>Equipment</th>
                        <th>Size Reduction Range</th>
                        <th>Application</th>
                    </tr>
                    <tr>
                        <td>Jaw Crusher</td>
                        <td>150-250 mm → 25-50 mm</td>
                        <td>Primary crushing</td>
                    </tr>
                    <tr>
                        <td>Cone Crusher</td>
                        <td>50-100 mm → 10-25 mm</td>
                        <td>Secondary crushing</td>
                    </tr>
                    <tr>
                        <td>Ball Mill</td>
                        <td>1-5 mm → 75-150 μm</td>
                        <td>Fine grinding</td>
                    </tr>
                    <tr>
                        <td>Rod Mill</td>
                        <td>5-20 mm → 300-1000 μm</td>
                        <td>Coarse grinding</td>
                    </tr>
                </table>
                
                <div class="important">
                    <h4>Bond's Law</h4>
                    <div class="formula">
                        W = 10W<sub>i</sub>(1/√P - 1/√F)
                    </div>
                    <p>Where:</p>
                    <ul>
                        <li>W = work input (kWh/ton)</li>
                        <li>W<sub>i</sub> = Bond work index (kWh/ton)</li>
                        <li>P = 80% passing size of product (μm)</li>
                        <li>F = 80% passing size of feed (μm)</li>
                    </ul>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="classification">
            <h3>Size Classification</h3>
            <div class="topic-card">
                <h4>Screening</h4>
                <div class="formula">
                    Screening efficiency = (mass of undersize in product)/(mass of undersize in feed) × 100%
                </div>
                
                <h4>Hydrocyclones</h4>
                <div class="formula">
                    d<sub>50</sub> = k(D<sub>c</sub><sup>0.67</sup>D<sub>i</sub><sup>0.45</sup>)/(D<sub>o</sub><sup>0.71</sup>h<sup>0.38</sup>Q<sup>0.45</sup>(ρ<sub>s</sub>-ρ)<sup>0.5</sup>)
                </div>
                <p>Where d<sub>50</sub> = cut size, D<sub>c</sub> = cyclone diameter, D<sub>i</sub> = inlet diameter, D<sub>o</sub> = overflow diameter, h = pressure head, Q = flow rate</p>
                
                <div class="process-flow">
                    <div class="process-step">1</div>
                    <div class="process-arrow"></div>
                    <div class="process-step">2</div>
                    <div class="process-arrow"></div>
                    <div class="process-step">3</div>
                    <p style="text-align: center; margin-top: 1rem;">
                        Typical comminution circuit: (1) Primary crushing → (2) Secondary crushing → (3) Grinding
                    </p>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="flotation">
            <h3>Flotation</h3>
            <div class="topic-card">
                <div class="definition">
                    Froth flotation is a process for selectively separating hydrophobic materials from hydrophilic by using differences in their surface properties.
                </div>
                
                <h4>Flotation Reagents</h4>
                <table>
                    <tr>
                        <th>Type</th>
                        <th>Function</th>
                        <th>Examples</th>
                    </tr>
                    <tr>
                        <td>Collectors</td>
                        <td>Render mineral surface hydrophobic</td>
                        <td>Xanthates, Dithiophosphates</td>
                    </tr>
                    <tr>
                        <td>Frothers</td>
                        <td>Stabilize bubbles</td>
                        <td>Pine oil, MIBC</td>
                    </tr>
                    <tr>
                        <td>Modifiers</td>
                        <td>Control pH and selectivity</td>
                        <td>Lime, Na<sub>2</sub>CO<sub>3</sub>, Na<sub>2</sub>S</td>
                    </tr>
                </table>
                
                <h4>Flotation Kinetics</h4>
                <div class="formula">
                    R = R<sub>∞</sub>[1 - exp(-kt)]
                </div>
                <p>Where R = recovery at time t, R<sub>∞</sub> = maximum recovery, k = rate constant</p>
            </div>
        </div>
        
        <div class="subsection" id="beneficiation">
            <h3>Gravity and Other Beneficiation Methods</h3>
            <div class="topic-card">
                <h4>Gravity Separation</h4>
                <div class="formula">
                    V<sub>t</sub> = [2g(ρ<sub>s</sub>-ρ)d<sup>2</sup>]/(9μ)
                </div>
                <p>Where V<sub>t</sub> = terminal settling velocity, ρ<sub>s</sub> = particle density, ρ = fluid density, d = particle diameter, μ = fluid viscosity</p>
                
                <h4>Equipment</h4>
                <ul>
                    <li>Jigs: Pulsating water flow separates heavy and light minerals</li>
                    <li>Spirals: Centrifugal force separates particles by density</li>
                    <li>Shaking tables: Stratification and differential movement</li>
                </ul>
                
                <div class="key-points">
                    <h4>Other Methods</h4>
                    <ul>
                        <li>Magnetic separation: For ferromagnetic minerals (magnetite)</li>
                        <li>Electrostatic separation: For conductive vs non-conductive minerals</li>
                        <li>Leaching: Chemical dissolution of valuable minerals</li>
                    </ul>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="agglomeration">
            <h3>Agglomeration</h3>
            <div class="topic-card">
                <h4>Sintering</h4>
                <p>Process of compacting and forming a solid mass by heat or pressure without melting</p>
                <div class="formula">
                    % Sinter = (mass of sinter)/(mass of raw mix) × 100%
                </div>
                
                <h4>Pelletizing</h4>
                <p>Process of rolling moist fines into balls (green pellets) which are then hardened by firing</p>
                <div class="formula">
                    Drop number = Number of drops from 45 cm height before breakage
                </div>
                
                <h4>Briquetting</h4>
                <p>Compaction of fine materials into larger lumps using binders under high pressure</p>
                
                <table>
                    <tr>
                        <th>Process</th>
                        <th>Temperature Range</th>
                        <th>Typical Binders</th>
                    </tr>
                    <tr>
                        <td>Sintering</td>
                        <td>1200-1400°C</td>
                        <td>None (self-fluxing)</td>
                    </tr>
                    <tr>
                        <td>Pelletizing</td>
                        <td>1250-1350°C</td>
                        <td>Bentonite (0.5-1%)</td>
                    </tr>
                    <tr>
                        <td>Briquetting</td>
                        <td>Ambient</td>
                        <td>Pitch, tar, cement</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>

    <div class="section extractive" id="extractive">
        <h2>4.2 Extractive Metallurgy</h2>
        
        <div class="subsection" id="material-balance">
            <h3>Material and Energy Balances</h3>
            <div class="topic-card">
                <div class="formula">
                    Input = Output + Accumulation + Losses
                </div>
                
                <h4>Heat Balance Components</h4>
                <ol>
                    <li>Sensible heat of reactants</li>
                    <li>Heat of reactions</li>
                    <li>Sensible heat of products</li>
                    <li>Heat losses</li>
                </ol>
                
                <div class="example">
                    <h5>Example: Copper Smelting</h5>
                    <p>For a copper concentrate (30% Cu) smelted to matte (50% Cu):</p>
                    <div class="formula">
                        Mass balance: 100 kg concentrate → 60 kg matte + 40 kg slag
                    </div>
                    <div class="formula">
                        Cu recovery = (60×0.5)/(100×0.3) × 100% = 100%
                    </div>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="non-ferrous">
            <h3>Non-Ferrous Metal Extraction</h3>
            <div class="topic-card">
                <h4>Aluminium Production</h4>
                <div class="process-flow">
                    <div class="process-step">Bauxite</div>
                    <div class="process-arrow"></div>
                    <div class="process-step">Al<sub>2</sub>O<sub>3</sub></div>
                    <div class="process-arrow"></div>
                    <div class="process-step">Al</div>
                    <p style="text-align: center; margin-top: 1rem;">
                        Bayer Process → Hall-Héroult Process
                    </p>
                </div>
                
                <div class="formula">
                    Al<sub>2</sub>O<sub>3</sub> + 3C → 2Al + 3CO (Hall-Héroult)
                </div>
                <p>Conditions: 950°C, cryolite (Na<sub>3</sub>AlF<sub>6</sub>) electrolyte, 4-5 V, 150-300 kA</p>
                
                <h4>Copper Extraction</h4>
                <div class="formula">
                    2CuFeS<sub>2</sub> + 5.5O<sub>2</sub> → Cu<sub>2</sub>S·FeS (matte) + 3SO<sub>2</sub> + FeO (slag)
                </div>
                <div class="formula">
                    Cu<sub>2</sub>S + O<sub>2</sub> → 2Cu + SO<sub>2</sub> (converting)
                </div>
                
                <h4>Titanium Production</h4>
                <div class="formula">
                    TiO<sub>2</sub> + 2Cl<sub>2</sub> + 2C → TiCl<sub>4</sub> + 2CO (chlorination)
                </div>
                <div class="formula">
                    TiCl<sub>4</sub> + 2Mg → Ti + 2MgCl<sub>2</sub> (Kroll process)
                </div>
                
                <div class="key-points">
                    <h4>Key Metals</h4>
                    <div style="text-align: center; margin: 1rem 0;">
                        <span class="element alkali">Na</span>
                        <span class="element metal">Al</span>
                        <span class="element transition">Ti</span>
                        <span class="element metal">Cu</span>
                        <span class="element metal">Zn</span>
                        <span class="element metal">Pb</span>
                    </div>
                    <p>Extraction methods vary based on metal reactivity and ore type</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section steel" id="iron-steel">
        <h2>4.3 Iron and Steel Making</h2>
        
        <div class="subsection" id="blast-furnace">
            <h3>Blast Furnace Process</h3>
            <div class="topic-card">
                <div class="definition">
                    The blast furnace is a counter-current reactor where iron ore is reduced to molten iron using coke as both fuel and reductant.
                </div>
                
                <h4>Key Reactions</h4>
                <div class="formula">
                    C + O<sub>2</sub> → CO<sub>2</sub> (combustion)
                </div>
                <div class="formula">
                    CO<sub>2</sub> + C → 2CO (Boudouard reaction)
                </div>
                <div class="formula">
                    Fe<sub>2</sub>O<sub>3</sub> + 3CO → 2Fe + 3CO<sub>2</sub> (reduction)
                </div>
                
                <h4>Material Balance</h4>
                <table>
                    <tr>
                        <th>Input (per ton of hot metal)</th>
                        <th>Amount (kg)</th>
                    </tr>
                    <tr>
                        <td>Iron ore</td>
                        <td>1600-1800</td>
                    </tr>
                    <tr>
                        <td>Coke</td>
                        <td>300-400</td>
                    </tr>
                    <tr>
                        <td>Limestone</td>
                        <td>200-300</td>
                    </tr>
                    <tr>
                        <td>Hot blast</td>
                        <td>1400-1600 Nm<sup>3</sup></td>
                    </tr>
                </table>
                
                <div class="important">
                    <h4>Heat Balance</h4>
                    <ul>
                        <li>Heat input: Coke combustion (75-80%), Hot blast (20-25%)</li>
                        <li>Heat output: Hot metal (35-40%), Slag (10-15%), Top gas (25-30%), Losses (15-20%)</li>
                    </ul>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="alternative-iron">
            <h3>Alternative Iron Making (COREX, MIDREX)</h3>
            <div class="topic-card">
                <h4>COREX Process</h4>
                <p>Two-stage smelting reduction using coal instead of coke:</p>
                <ol>
                    <li>Reduction shaft: Pre-reduction to 85-90% metallization</li>
                    <li>Melter-gasifier: Final reduction and melting</li>
                </ol>
                
                <h4>MIDREX Process</h4>
                <p>Direct reduction using natural gas (H<sub>2</sub> + CO):</p>
                <div class="formula">
                    Fe<sub>2</sub>O<sub>3</sub> + 3H<sub>2</sub> → 2Fe + 3H<sub>2</sub>O
                </div>
                <div class="formula">
                    Fe<sub>2</sub>O<sub>3</sub> + 3CO → 2Fe + 3CO<sub>2</sub>
                </div>
                
                <table>
                    <tr>
                        <th>Process</th>
                        <th>Reductant</th>
                        <th>Product</th>
                        <th>Energy (GJ/ton)</th>
                    </tr>
                    <tr>
                        <td>Blast Furnace</td>
                        <td>Coke</td>
                        <td>Hot Metal</td>
                        <td>14-16</td>
                    </tr>
                    <tr>
                        <td>COREX</td>
                        <td>Coal</td>
                        <td>Hot Metal</td>
                        <td>16-18</td>
                    </tr>
                    <tr>
                        <td>MIDREX</td>
                        <td>Natural Gas</td>
                        <td>DRI</td>
                        <td>10-12</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>

    <div class="section slag" id="slag">
        <h2>4.4 Slag Properties</h2>
        
        <div class="subsection" id="slag-structure">
            <h3>Structure and Properties of Slags</h3>
            <div class="topic-card">
                <div class="definition">
                    Slag is a molten mixture of oxides (CaO, SiO<sub>2</sub>, Al<sub>2</sub>O<sub>3</sub>, MgO) that floats on molten metal, protecting it from oxidation and removing impurities.
                </div>
                
                <h4>Basicity Index</h4>
                <div class="formula">
                    V-ratio = %CaO/%SiO<sub>2</sub>
                </div>
                <div class="formula">
                    B<sub>2</sub> = (%CaO + %MgO)/(%SiO<sub>2</sub> + %Al<sub>2</sub>O<sub>3</sub>)
                </div>
                
                <h4>Sulfide Capacity</h4>
                <div class="formula">
                    C<sub>S</sub> = (%S)(P<sub>O<sub>2</sub></sub>/P<sub>S<sub>2</sub></sub>)<sup>1/2</sup>
                </div>
                
                <h4>Phosphate Capacity</h4>
                <div class="formula">
                    C<sub>PO<sub>4</sub></sub> = (%PO<sub>4</sub><sup>3-</sup>)(P<sub>O<sub>2</sub></sub><sup>5/4</sup>/P<sub>P<sub>2</sub></sub><sup>1/2</sup>)
                </div>
                
                <table>
                    <tr>
                        <th>Slag Type</th>
                        <th>Composition</th>
                        <th>Basicity</th>
                        <th>Viscosity (Poise)</th>
                    </tr>
                    <tr>
                        <td>Blast Furnace</td>
                        <td>35-45% CaO, 30-40% SiO<sub>2</sub></td>
                        <td>1.0-1.2</td>
                        <td>5-15</td>
                    </tr>
                    <tr>
                        <td>Steelmaking</td>
                        <td>40-50% CaO, 10-20% FeO</td>
                        <td>2.0-3.5</td>
                        <td>0.2-2.0</td>
                    </tr>
                </table>
            </div>
        </div>
        
        <div class="subsection" id="coke">
            <h3>Metallurgical Coke Production</h3>
            <div class="topic-card">
                <h4>Coking Process</h4>
                <p>Destructive distillation of coal at 1000-1100°C in absence of air</p>
                <div class="process-flow">
                    <div class="process-step">Coal</div>
                    <div class="process-arrow"></div>
                    <div class="process-step">Oven</div>
                    <div class="process-arrow"></div>
                    <div class="process-step">Coke</div>
                </div>
                
                <h4>Coke Properties</h4>
                <table>
                    <tr>
                        <th>Property</th>
                        <th>Value</th>
                    </tr>
                    <tr>
                        <td>Fixed Carbon</td>
                        <td>85-90%</td>
                    </tr>
                    <tr>
                        <td>Ash</td>
                        <td>8-12%</td>
                    </tr>
                    <tr>
                        <td>Volatile Matter</td>
                        <td>1-2%</td>
                    </tr>
                    <tr>
                        <td>CSR (Coke Strength after Reaction)</td>
                        <td>60-65%</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>

    <div class="section steel" id="steel-making">
        <h2>4.5 Steel Making Processes</h2>
        
        <div class="subsection" id="primary-steel">
            <h3>Primary Steel Making</h3>
            <div class="topic-card">
                <h4>Basic Oxygen Furnace (BOF)</h4>
                <p>Process dynamics:</p>
                <ul>
                    <li>Oxygen (99.5% pure) blown at supersonic speed (Mach 2)</li>
                    <li>Temperature: 1600-1650°C</li>
                    <li>Process time: 40-50 minutes</li>
                </ul>
                
                <h4>Key Oxidation Reactions</h4>
                <div class="formula">
                    C + ½O<sub>2</sub> → CO
                </div>
                <div class="formula">
                    Si + O<sub>2</sub> → SiO<sub>2</sub> (ΔH = -832 kJ/mol)
                </div>
                <div class="formula">
                    Mn + ½O<sub>2</sub> → MnO (ΔH = -385 kJ/mol)
                </div>
                
                <h4>Electric Arc Furnace (EAF)</h4>
                <p>Uses electrical energy (400-700 kWh/ton) to melt scrap:</p>
                <div class="formula">
                    Power input = √3 × V × I × cosφ
                </div>
            </div>
        </div>
        
        <div class="subsection" id="secondary-steel">
            <h3>Secondary Steel Making</h3>
            <div class="topic-card">
                <h4>Ladle Processes</h4>
                <table>
                    <tr>
                        <th>Process</th>
                        <th>Purpose</th>
                        <th>Reagents</th>
                    </tr>
                    <tr>
                        <td>Deoxidation</td>
                        <td>Remove dissolved oxygen</td>
                        <td>Al, FeSi, FeMn</td>
                    </tr>
                    <tr>
                        <td>Desulfurization</td>
                        <td>Reduce sulfur content</td>
                        <td>CaO, CaC<sub>2</sub>, Mg</td>
                    </tr>
                    <tr>
                        <td>Argon Stirring</td>
                        <td>Homogenize temperature and composition</td>
                        <td>Argon gas (2-10 Nm<sup>3</sup>/min)</td>
                    </tr>
                </table>
                
                <h4>Degassing Methods</h4>
                <ul>
                    <li>RH (Ruhrstahl-Heraeus): Recirculation degassing</li>
                    <li>VD (Vacuum Degassing): Ladle degassing</li>
                    <li>DH (Dortmund-Hörder): Lift degassing</li>
                </ul>
                
                <div class="important">
                    <h4>Inclusion Shape Control</h4>
                    <p>Calcium treatment modifies alumina inclusions:</p>
                    <div class="formula">
                        3Ca + Al<sub>2</sub>O<sub>3</sub> → 3CaO + 2Al
                    </div>
                    <p>Forms liquid calcium aluminate inclusions (12CaO·7Al<sub>2</sub>O<sub>3</sub>)</p>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="stainless">
            <h3>Stainless Steel Manufacturing</h3>
            <div class="topic-card">
                <h4>Key Processes</h4>
                <ol>
                    <li>Melting: EAF or AOD (Argon Oxygen Decarburization)</li>
                    <li>Decarburization: Reduce carbon while retaining chromium</li>
                    <li>Alloying: Add Ni, Mo, etc. for required properties</li>
                </ol>
                
                <h4>AOD Process</h4>
                <p>Uses mixed gas (O<sub>2</sub> + Ar/N<sub>2</sub>) to reduce carbon without excessive chromium oxidation:</p>
                <div class="formula">
                    [C] + [O] → CO<sub>(g)</sub>
                </div>
                <div class="formula">
                    3[C] + Cr<sub>2</sub>O<sub>3</sub> → 2[Cr] + 3CO<sub>(g)</sub>
                </div>
                
                <table>
                    <tr>
                        <th>Grade</th>
                        <th>Composition</th>
                        <th>Properties</th>
                    </tr>
                    <tr>
                        <td>304</td>
                        <td>18Cr-8Ni</td>
                        <td>General purpose</td>
                    </tr>
                    <tr>
                        <td>316</td>
                        <td>16Cr-10Ni-2Mo</td>
                        <td>Marine applications</td>
                    </tr>
                    <tr>
                        <td>430</td>
                        <td>17Cr</td>
                        <td>Ferritic, low cost</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>

    <div class="section" id="casting">
        <h2>4.6 Continuous Casting</h2>
        
        <div class="subsection" id="fluid-flow">
            <h3>Fluid Flow in Tundish and Mold</h3>
            <div class="topic-card">
                <h4>Tundish Flow Control</h4>
                <p>Flow modifiers used to:</p>
                <ul>
                    <li>Increase residence time (3-5 minutes)</li>
                    <li>Promote inclusion floatation</li>
                    <li>Minimize short-circuiting</li>
                </ul>
                
                <h4>Mold Flow Patterns</h4>
                <div class="formula">
                    Froude number = v<sup>2</sup>/gD (should be 0.2-0.4)
                </div>
                <p>Where v = nozzle exit velocity, D = nozzle diameter</p>
                
                <div class="key-points">
                    <h4>Meniscus Control</h4>
                    <ul>
                        <li>Level fluctuations < ±3 mm</li>
                        <li>Mold powder consumption: 0.3-0.6 kg/ton</li>
                        <li>Oscillation marks: 3-5 mm pitch</li>
                    </ul>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="heat-transfer">
            <h3>Heat Transfer in the Mold</h3>
            <div class="topic-card">
                <h4>Heat Flux</h4>
                <div class="formula">
                    q = k(ΔT/δ)
                </div>
                <p>Where δ = slag film thickness (1-2 mm), k = thermal conductivity (1-2 W/m·K)</p>
                
                <h4>Solidification</h4>
                <div class="formula">
                    Shell thickness = K√t
                </div>
                <p>Where K = solidification constant (20-30 mm/min<sup>1/2</sup>), t = time in mold (1-2 min)</p>
                
                <table>
                    <tr>
                        <th>Parameter</th>
                        <th>Slab</th>
                        <th>Bloom</th>
                        <th>Billet</th>
                    </tr>
                    <tr>
                        <td>Mold length (mm)</td>
                        <td>900</td>
                        <td>800</td>
                        <td>700</td>
                    </tr>
                    <tr>
                        <td>Withdrawal speed (m/min)</td>
                        <td>1.0-1.5</td>
                        <td>0.8-1.2</td>
                        <td>2.0-4.0</td>
                    </tr>
                </table>
            </div>
        </div>
        
        <div class="subsection" id="defects">
            <h3>Segregation and Inclusion Control</h3>
            <div class="topic-card">
                <h4>Segregation</h4>
                <div class="formula">
                    Segregation ratio = C<sub>max</sub>/C<sub>0</sub>
                </div>
                <p>Where C<sub>max</sub> = maximum concentration, C<sub>0</sub> = bulk concentration</p>
                
                <h4>Inclusion Control</h4>
                <ul>
                    <li>Tundish: Ceramic filters, flow modifiers</li>
                    <li>Mold: Electromagnetic braking (EMBr)</li>
                    <li>Secondary cooling: Avoid reheating</li>
                </ul>
                
                <div class="important">
                    <h4>Clean Steel Practices</h4>
                    <ul>
                        <li>[O] < 20 ppm for most applications</li>
                        <li>[N] < 50 ppm for drawing quality steels</li>
                        <li>Total inclusions < 0.01% by volume</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
    
    <footer>
        <p>© TestUrSelf | All Rights Reserved</p>
    </footer>
</body>
</html>
