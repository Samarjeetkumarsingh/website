<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GATE MT - Manufacturing Processes</title>
    <style>
        :root {
            --primary-color: #0277bd;
            --secondary-color: #ff8f00;
            --accent-color: #01579b;
            --light-color: #e1f5fe;
            --dark-color: #01579b;
            --text-color: #212121;
            --highlight-color: #ffd600;
            --success-color: #2e7d32;
            --casting-color: #00838f;
            --forming-color: #d84315;
            --joining-color: #6a1b9a;
            --powder-color: #5d4037;
            --ndt-color: #37474f;
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
        
        /* Animated Manufacturing Background */
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                linear-gradient(135deg, rgba(2,119,189,0.05) 0%, rgba(255,143,0,0.05) 50%, rgba(106,27,154,0.05) 100%),
                url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect fill="%230277bd" opacity="0.05" width="10" height="10" x="20" y="20"/><rect fill="%23ff8f00" opacity="0.05" width="15" height="15" x="60" y="30"/><rect fill="%236a1b9a" opacity="0.05" width="12" height="12" x="40" y="70"/><circle fill="%2302838f" opacity="0.05" cx="80" cy="20" r="5"/><circle fill="%23d84315" opacity="0.05" cx="20" cy="80" r="7"/></svg>');
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
            color: rgba(2, 119, 189, 0.05);
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
            border-left: 5px solid var(--casting-color);
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
            background-color: var(--casting-color);
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
        .casting {
            border-top: 4px solid var(--casting-color);
        }
        
        .forming {
            border-top: 4px solid var(--forming-color);
        }
        
        .joining {
            border-top: 4px solid var(--joining-color);
        }
        
        .powder {
            border-top: 4px solid var(--powder-color);
        }
        
        .ndt {
            border-top: 4px solid var(--ndt-color);
        }
        
        /* Process visualization */
        .process-vis {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin: 2rem 0;
        }
        
        .process-step {
            width: 150px;
            text-align: center;
            margin: 1rem;
            transition: all 0.3s ease;
        }
        
        .process-step:hover {
            transform: scale(1.1);
        }
        
        .process-icon {
            width: 100px;
            height: 100px;
            margin: 0 auto;
            background-color: #e0e0e0;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            color: white;
            box-shadow: 0 3px 6px rgba(0,0,0,0.2);
        }
        
        /* NDT methods visualization */
        .ndt-methods {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            margin: 2rem 0;
        }
        
        .ndt-card {
            width: 120px;
            padding: 1rem;
            margin: 0.5rem;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            text-align: center;
        }
        
        .ndt-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .ndt-icon {
            width: 60px;
            height: 60px;
            margin: 0 auto 1rem;
            background-color: var(--ndt-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: white;
        }
        
        /* Welding types visualization */
        .welding-types {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            margin: 2rem 0;
        }
        
        .welding-card {
            width: 120px;
            padding: 1rem;
            margin: 0.5rem;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            text-align: center;
        }
        
        .welding-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .welding-icon {
            width: 60px;
            height: 60px;
            margin: 0 auto 1rem;
            background-color: var(--joining-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: white;
        }
        
        /* Copyright notice */
        .copyright {
            text-align: center;
            margin-top: 3rem;
            padding: 1rem;
            color: var(--primary-color);
            font-weight: bold;
            border-top: 1px solid #e0e0e0;
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
    </style>
</head>
<body>
    <header>
        <h1>Manufacturing Processes</h1>
        <p>Complete Guide for GATE Metallurgy (MT) - Section 7 (TestUrSelf)</p>
    </header>

    <div class="toc">
        <h2>Table of Contents</h2>
        <ol>
            <li><a href="#casting">Metal Casting</a></li>
            <li><a href="#forming">Metal Forming</a></li>
            <li><a href="#joining">Metal Joining</a></li>
            <li><a href="#powder">Powder Metallurgy</a></li>
            <li><a href="#ndt">Non-Destructive Testing</a></li>
        </ol>
    </div>

    <div class="section casting" id="casting">
        <h2>7.1 Metal Casting</h2>
        
        <div class="subsection" id="mold-design">
            <h3>Mould Design</h3>
            <div class="topic-card">
                <div class="process-vis">
                    <div class="process-step">
                        <div class="process-icon" style="background-color: var(--casting-color);">G</div>
                        <p>Gating System</p>
                    </div>
                    <div class="process-step">
                        <div class="process-icon" style="background-color: var(--casting-color);">R</div>
                        <p>Riser Design</p>
                    </div>
                    <div class="process-step">
                        <div class="process-icon" style="background-color: var(--casting-color);">F</div>
                        <p>Feeding</p>
                    </div>
                </div>
                
                <h4>Key Principles</h4>
                <ul>
                    <li>Chvorinov's Rule: t<sub>solidification</sub> ∝ (V/A)<sup>2</sup></li>
                    <li>Gating ratio: A<sub>sprue</sub>:A<sub>runner</sub>:A<sub>gate</sub> (typically 1:2:2)</li>
                    <li>Riser must solidify after casting (modulus > casting modulus)</li>
                </ul>
                
                <div class="important">
                    <h4>Casting Defects</h4>
                    <table>
                        <tr>
                            <th>Defect</th>
                            <th>Causes</th>
                            <th>Prevention</th>
                        </tr>
                        <tr>
                            <td>Porosity</td>
                            <td>Gas entrapment, shrinkage</td>
                            <td>Proper venting, riser design</td>
                        </tr>
                        <tr>
                            <td>Misrun</td>
                            <td>Incomplete filling</td>
                            <td>Higher pouring temp, better fluidity</td>
                        </tr>
                        <tr>
                            <td>Hot tears</td>
                            <td>Restrained contraction</td>
                            <td>Better mold collapsibility</td>
                        </tr>
                    </table>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="casting-practices">
            <h3>Casting Practices</h3>
            <div class="topic-card">
                <table>
                    <tr>
                        <th>Process</th>
                        <th>Tolerance (mm/mm)</th>
                        <th>Surface Finish (μm)</th>
                        <th>Applications</th>
                    </tr>
                    <tr>
                        <td>Sand Casting</td>
                        <td>±0.8-3.0</td>
                        <td>5-25</td>
                        <td>Large parts, low volume</td>
                    </tr>
                    <tr>
                        <td>Investment</td>
                        <td>±0.1-0.5</td>
                        <td>1.5-3.0</td>
                        <td>Complex shapes, high precision</td>
                    </tr>
                    <tr>
                        <td>Die Casting</td>
                        <td>±0.1-0.3</td>
                        <td>0.8-1.6</td>
                        <td>High volume, thin walls</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>

    <div class="section forming" id="forming">
        <h2>7.2 Metal Forming</h2>
        
        <div class="subsection" id="working-temps">
            <h3>Hot, Warm & Cold Working</h3>
            <div class="topic-card">
                <table>
                    <tr>
                        <th>Process</th>
                        <th>Temperature</th>
                        <th>Advantages</th>
                        <th>Disadvantages</th>
                    </tr>
                    <tr>
                        <td>Hot Working</td>
                        <td>>0.6T<sub>m</sub></td>
                        <td>Low forces, no strain hardening</td>
                        <td>Oxidation, poor tolerances</td>
                    </tr>
                    <tr>
                        <td>Warm Working</td>
                        <td>0.3-0.5T<sub>m</sub></td>
                        <td>Reduced forces, better finish</td>
                        <td>Special equipment needed</td>
                    </tr>
                    <tr>
                        <td>Cold Working</td>
                        <td><0.3T<sub>m</sub></td>
                        <td>Good finish, strain hardening</td>
                        <td>High forces, limited ductility</td>
                    </tr>
                </table>
            </div>
        </div>
        
        <div class="subsection" id="forming-processes">
            <h3>Metal Forming Processes</h3>
            <div class="topic-card">
                <div class="process-vis">
                    <div class="process-step">
                        <div class="process-icon" style="background-color: var(--forming-color);">R</div>
                        <p>Rolling</p>
                    </div>
                    <div class="process-step">
                        <div class="process-icon" style="background-color: var(--forming-color);">F</div>
                        <p>Forging</p>
                    </div>
                    <div class="process-step">
                        <div class="process-icon" style="background-color: var(--forming-color);">E</div>
                        <p>Extrusion</p>
                    </div>
                    <div class="process-step">
                        <div class="process-icon" style="background-color: var(--forming-color);">D</div>
                        <p>Drawing</p>
                    </div>
                </div>
                
                <h4>Key Formulas</h4>
                <div class="formula">
                    Rolling: h<sub>f</sub> = h<sub>0</sub> - 2R(1 - cosα) (α = bite angle)
                </div>
                <div class="formula">
                    Forging: F = Y<sub>f</sub>A(1 + μD/3h) (Y<sub>f</sub> = flow stress)
                </div>
                <div class="formula">
                    Extrusion: P = Y<sub>f</sub>ln(A<sub>0</sub>/A<sub>f</sub>) (ideal work)
                </div>
                
                <div class="important">
                    <h4>Forming Defects</h4>
                    <ul>
                        <li>Rolling: Edge cracks, alligatoring</li>
                        <li>Forging: Laps, cold shuts</li>
                        <li>Extrusion: Surface cracking, piping</li>
                        <li>Drawing: Center burst, wrinkling</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <div class="section joining" id="joining">
        <h2>7.3 Metal Joining</h2>
        
        <div class="subsection" id="welding">
            <h3>Welding Processes</h3>
            <div class="topic-card">
                <div class="welding-types">
                    <div class="welding-card">
                        <div class="welding-icon">⚡</div>
                        <p>Arc Welding</p>
                    </div>
                    <div class="welding-card">
                        <div class="welding-icon">🔥</div>
                        <p>Gas Welding</p>
                    </div>
                    <div class="welding-card">
                        <div class="welding-icon">💥</div>
                        <p>Resistance</p>
                    </div>
                    <div class="welding-card">
                        <div class="welding-icon">🔄</div>
                        <p>Friction</p>
                    </div>
                </div>
                
                <h4>Welding Metallurgy</h4>
                <ul>
                    <li>Fusion zone: Rapid solidification structure</li>
                    <li>HAZ: Grain growth, phase transformations</li>
                    <li>Residual stresses due to thermal gradients</li>
                </ul>
                
                <div class="example">
                    <h5>Example: Steel Welding</h5>
                    <p>Preheat temperature calculation:</p>
                    <div class="formula">
                        T<sub>preheat</sub> (°C) = 144√CE - 392
                    </div>
                    <p>Where CE = C + Mn/6 + (Cr+Mo+V)/5 + (Ni+Cu)/15</p>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="joining-defects">
            <h3>Joining Defects</h3>
            <div class="topic-card">
                <table>
                    <tr>
                        <th>Material</th>
                        <th>Common Defects</th>
                        <th>Prevention</th>
                    </tr>
                    <tr>
                        <td>Steels</td>
                        <td>Hydrogen cracks, porosity</td>
                        <td>Preheat, low-H electrodes</td>
                    </tr>
                    <tr>
                        <td>Al Alloys</td>
                        <td>Hot cracks, lack of fusion</td>
                        <td>Proper filler, high heat input</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>

    <div class="section powder" id="powder">
        <h2>7.4 Powder Metallurgy</h2>
        
        <div class="subsection" id="powder-production">
            <h3>Powder Production</h3>
            <div class="topic-card">
                <table>
                    <tr>
                        <th>Method</th>
                        <th>Particle Size (μm)</th>
                        <th>Shape</th>
                        <th>Applications</th>
                    </tr>
                    <tr>
                        <td>Atomization</td>
                        <td>10-300</td>
                        <td>Spherical</td>
                        <td>High performance parts</td>
                    </tr>
                    <tr>
                        <td>Reduction</td>
                        <td>1-100</td>
                        <td>Irregular</td>
                        <td>Fe, W, Cu powders</td>
                    </tr>
                    <tr>
                        <td>Electrolysis</td>
                        <td>10-150</td>
                        <td>Dendritic</td>
                        <td>Cu, Fe powders</td>
                    </tr>
                </table>
            </div>
        </div>
        
        <div class="subsection" id="compaction-sintering">
            <h3>Compaction & Sintering</h3>
            <div class="topic-card">
                <div class="process-vis">
                    <div class="process-step">
                        <div class="process-icon" style="background-color: var(--powder-color);">C</div>
                        <p>Compaction</p>
                    </div>
                    <div class="process-step">
                        <div class="process-icon" style="background-color: var(--powder-color);">S</div>
                        <p>Sintering</p>
                    </div>
                </div>
                
                <h4>Key Parameters</h4>
                <div class="formula">
                    Green density ≈ 80% theoretical (pressure dependent)
                </div>
                <div class="formula">
                    Sintering temperature ≈ 0.7-0.9T<sub>m</sub>
                </div>
                
                <div class="important">
                    <h4>Sintering Mechanisms</h4>
                    <ol>
                        <li>Initial: Neck formation</li>
                        <li>Intermediate: Pore rounding</li>
                        <li>Final: Pore elimination</li>
                    </ol>
                </div>
            </div>
        </div>
    </div>

    <div class="section ndt" id="ndt">
        <h2>7.5 Non-Destructive Testing</h2>
        
        <div class="subsection" id="ndt-methods">
            <h3>NDT Methods</h3>
            <div class="topic-card">
                <div class="ndt-methods">
                    <div class="ndt-card">
                        <div class="ndt-icon">💧</div>
                        <p>Dye Penetrant</p>
                    </div>
                    <div class="ndt-card">
                        <div class="ndt-icon">📡</div>
                        <p>Ultrasonic</p>
                    </div>
                    <div class="ndt-card">
                        <div class="ndt-icon">☢️</div>
                        <p>Radiography</p>
                    </div>
                    <div class="ndt-card">
                        <div class="ndt-icon">🌀</div>
                        <p>Eddy Current</div>
                    </div>
                    <div class="ndt-card">
                        <div class="ndt-icon">🎤</div>
                        <p>Acoustic Emission</div>
                    </div>
                    <div class="ndt-card">
                        <div class="ndt-icon">🧲</div>
                        <p>Magnetic Particle</div>
                    </div>
                </div>
                
                <table>
                    <tr>
                        <th>Method</th>
                        <th>Sensitivity</th>
                        <th>Materials</th>
                        <th>Defects Detected</th>
                    </tr>
                    <tr>
                        <td>Ultrasonic</td>
                        <td>0.5-5% wall thickness</td>
                        <td>All</td>
                        <td>Internal, subsurface</td>
                    </tr>
                    <tr>
                        <td>Radiography</td>
                        <td>1-2% thickness</td>
                        <td>All</td>
                        <td>Volumetric</td>
                    </tr>
                    <tr>
                        <td>Magnetic Particle</td>
                        <td>Surface breaking</td>
                        <td>Ferromagnetic</td>
                        <td>Cracks, laps</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>
    
    <div class="copyright">
        <p>© Copyright 2023 TestUrSelf. All Rights Reserved.</p>
    </div>

    <footer>
        <p>Complete GATE Metallurgy Study Material | TestUrSelf</p>
    </footer>
</body>
</html>
