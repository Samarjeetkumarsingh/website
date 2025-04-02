<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GATE MT - Physical Metallurgy</title>
    <style>
        :root {
            --primary-color: #5e35b1;
            --secondary-color: #ff7043;
            --accent-color: #4527a0;
            --light-color: #ede7f6;
            --dark-color: #4527a0;
            --text-color: #212121;
            --highlight-color: #ffd600;
            --success-color: #43a047;
            --crystal-color: #7e57c2;
            --diffusion-color: #26a69a;
            --transformation-color: #ef5350;
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
        
        /* Animated Crystal Lattice Background */
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                linear-gradient(135deg, rgba(94,53,177,0.05) 0%, rgba(255,112,67,0.05) 50%, rgba(38,166,154,0.05) 100%),
                url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><circle fill="%235e35b1" opacity="0.05" cx="20" cy="20" r="3"/><circle fill="%23ff7043" opacity="0.05" cx="50" cy="50" r="3"/><circle fill="%2326a69a" opacity="0.05" cx="80" cy="80" r="3"/><line x1="20" y1="20" x2="50" y2="50" stroke="%235e35b1" stroke-width="1" opacity="0.05"/><line x1="50" y1="50" x2="80" y2="80" stroke="%23ff7043" stroke-width="1" opacity="0.05"/></svg>');
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
            color: rgba(94, 53, 177, 0.05);
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
            border-left: 5px solid var(--diffusion-color);
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
            background-color: var(--diffusion-color);
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
        .bonding {
            border-top: 4px solid var(--crystal-color);
        }
        
        .diffusion {
            border-top: 4px solid var(--diffusion-color);
        }
        
        .transformation {
            border-top: 4px solid var(--transformation-color);
        }
        
        .heat-treatment {
            border-top: 4px solid var(--secondary-color);
        }
        
        /* Crystal structure visualization */
        .crystal-structure {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin: 2rem 0;
        }
        
        .crystal-type {
            width: 150px;
            text-align: center;
            margin: 1rem;
            transition: all 0.3s ease;
        }
        
        .crystal-type:hover {
            transform: scale(1.1);
        }
        
        .crystal-vis {
            width: 100px;
            height: 100px;
            margin: 0 auto;
            position: relative;
        }
        
        .atom {
            position: absolute;
            border-radius: 50%;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        
        /* TTT/CCT diagram styling */
        .diagram {
            background-color: white;
            padding: 1.5rem;
            border-radius: 8px;
            margin: 2rem auto;
            max-width: 600px;
            position: relative;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
        }
        
        .diagram::before {
            content: "Time-Temperature-Transformation";
            position: absolute;
            top: -12px;
            left: 20px;
            background-color: var(--secondary-color);
            color: white;
            padding: 0.3rem 1rem;
            border-radius: 4px;
            font-size: 0.8rem;
            font-weight: bold;
        }
        
        /* Corrosion types visualization */
        .corrosion-types {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            margin: 2rem 0;
        }
        
        .corrosion-card {
            width: 120px;
            padding: 1rem;
            margin: 0.5rem;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            text-align: center;
        }
        
        .corrosion-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .corrosion-icon {
            width: 60px;
            height: 60px;
            margin: 0 auto 1rem;
            background-color: #e0e0e0;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
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
        <h1>Physical Metallurgy</h1>
        <p>Complete Guide for GATE Metallurgy (MT) - Section 5 (TestUrSelf)</p>
    </header>

    <div class="toc">
        <h2>Table of Contents</h2>
        <ol>
            <li><a href="#bonding">Chemical Bonding & Crystal Structure</a></li>
            <li><a href="#characterization">Characterization Techniques</a></li>
            <li><a href="#defects">Crystal Imperfections</a></li>
            <li><a href="#diffusion">Diffusion in Solids</a></li>
            <li><a href="#transformations">Phase Transformations</a></li>
            <li><a href="#heat-treatment">Heat Treatment</a></li>
            <li><a href="#properties">Material Properties</a></li>
            <li><a href="#corrosion">Corrosion</a></li>
        </ol>
    </div>

    <div class="section bonding" id="bonding">
        <h2>5.1 Chemical Bonding & Crystal Structure</h2>
        
        <div class="subsection" id="bonding-types">
            <h3>Types of Chemical Bonding</h3>
            <div class="topic-card">
                <table>
                    <tr>
                        <th>Bond Type</th>
                        <th>Energy Range (kJ/mol)</th>
                        <th>Examples</th>
                        <th>Characteristics</th>
                    </tr>
                    <tr>
                        <td>Ionic</td>
                        <td>600-1500</td>
                        <td>NaCl, MgO</td>
                        <td>Electron transfer, high melting point</td>
                    </tr>
                    <tr>
                        <td>Covalent</td>
                        <td>150-1100</td>
                        <td>Diamond, SiO<sub>2</sub></td>
                        <td>Electron sharing, directional</td>
                    </tr>
                    <tr>
                        <td>Metallic</td>
                        <td>100-350</td>
                        <td>Cu, Fe, Al</td>
                        <td>Electron sea, ductile</td>
                    </tr>
                    <tr>
                        <td>Secondary</td>
                        <td>1-50</td>
                        <td>Polymers, H<sub>2</sub>O</td>
                        <td>Van der Waals, hydrogen bonds</td>
                    </tr>
                </table>
            </div>
        </div>
        
        <div class="subsection" id="crystal-structures">
            <h3>Crystal Structures of Solids</h3>
            <div class="topic-card">
                <div class="crystal-structure">
                    <div class="crystal-type">
                        <div class="crystal-vis" style="background-color: rgba(126, 87, 194, 0.1);">
                            <div class="atom" style="width: 20px; height: 20px; background-color: #5e35b1; top: 40px; left: 40px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #ff7043; top: 10px; left: 10px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #ff7043; top: 10px; left: 70px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #ff7043; top: 70px; left: 10px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #ff7043; top: 70px; left: 70px;"></div>
                        </div>
                        <p>NaCl (Rock Salt)</p>
                    </div>
                    <div class="crystal-type">
                        <div class="crystal-vis" style="background-color: rgba(126, 87, 194, 0.1);">
                            <div class="atom" style="width: 20px; height: 20px; background-color: #5e35b1; top: 20px; left: 20px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #5e35b1; top: 20px; left: 60px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #5e35b1; top: 60px; left: 20px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #5e35b1; top: 60px; left: 60px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #ff7043; top: 40px; left: 40px;"></div>
                        </div>
                        <p>BCC (Fe, W)</p>
                    </div>
                    <div class="crystal-type">
                        <div class="crystal-vis" style="background-color: rgba(126, 87, 194, 0.1);">
                            <div class="atom" style="width: 20px; height: 20px; background-color: #5e35b1; top: 20px; left: 40px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #5e35b1; top: 40px; left: 20px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #5e35b1; top: 40px; left: 60px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #5e35b1; top: 60px; left: 40px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #ff7043; top: 40px; left: 40px;"></div>
                        </div>
                        <p>FCC (Cu, Al)</p>
                    </div>
                    <div class="crystal-type">
                        <div class="crystal-vis" style="background-color: rgba(126, 87, 194, 0.1);">
                            <div class="atom" style="width: 20px; height: 20px; background-color: #5e35b1; top: 15px; left: 40px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #5e35b1; top: 40px; left: 15px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #5e35b1; top: 40px; left: 65px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #5e35b1; top: 65px; left: 40px;"></div>
                            <div class="atom" style="width: 20px; height: 20px; background-color: #ff7043; top: 40px; left: 40px;"></div>
                        </div>
                        <p>HCP (Mg, Zn)</p>
                    </div>
                </div>
                
                <h4>Key Parameters</h4>
                <div class="formula">
                    Atomic Packing Factor (APF) = (Volume of atoms in unit cell)/(Volume of unit cell)
                </div>
                <table>
                    <tr>
                        <th>Structure</th>
                        <th>Coordination #</th>
                        <th>APF</th>
                        <th>Examples</th>
                    </tr>
                    <tr>
                        <td>BCC</td>
                        <td>8</td>
                        <td>0.68</td>
                        <td>Fe(α), W, Mo</td>
                    </tr>
                    <tr>
                        <td>FCC</td>
                        <td>12</td>
                        <td>0.74</td>
                        <td>Cu, Al, Ni, Fe(γ)</td>
                    </tr>
                    <tr>
                        <td>HCP</td>
                        <td>12</td>
                        <td>0.74</td>
                        <td>Mg, Zn, Ti(α)</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>

    <div class="section" id="characterization">
        <h2>5.2 Characterization Techniques</h2>
        
        <div class="subsection" id="xrd">
            <h3>X-ray Diffraction</h3>
            <div class="topic-card">
                <div class="formula">
                    nλ = 2d sinθ (Bragg's Law)
                </div>
                <p>Where:</p>
                <ul>
                    <li>n = order of reflection (1, 2, 3...)</li>
                    <li>λ = wavelength of X-rays (Cu Kα = 1.54 Å)</li>
                    <li>d = interplanar spacing</li>
                    <li>θ = Bragg angle</li>
                </ul>
                
                <h4>Interplanar Spacing</h4>
                <p>For cubic crystals:</p>
                <div class="formula">
                    1/d<sup>2</sup> = (h<sup>2</sup> + k<sup>2</sup> + l<sup>2</sup>)/a<sup>2</sup>
                </div>
                
                <div class="example">
                    <h5>Example: FCC Pattern</h5>
                    <p>Allowed reflections: h,k,l all odd or all even</p>
                    <p>First 5 peaks: (111), (200), (220), (311), (222)</p>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="microscopy">
            <h3>Optical & Electron Microscopy</h3>
            <div class="topic-card">
                <h4>Optical Metallography</h4>
                <ul>
                    <li>Resolution limit: ~0.2 μm</li>
                    <li>Magnification: 50-1000×</li>
                    <li>Sample preparation: Cutting, mounting, grinding, polishing, etching</li>
                </ul>
                
                <h4>SEM Imaging</h4>
                <ul>
                    <li>Resolution: 1-10 nm</li>
                    <li>Depth of field: 100× better than optical</li>
                    <li>Signals: Secondary electrons (topography), Backscattered electrons (composition)</li>
                </ul>
                
                <div class="key-points">
                    <h4>Comparison</h4>
                    <table>
                        <tr>
                            <th>Feature</th>
                            <th>Optical</th>
                            <th>SEM</th>
                        </tr>
                        <tr>
                            <td>Resolution</td>
                            <td>~0.2 μm</td>
                            <td>1-10 nm</td>
                        </tr>
                        <tr>
                            <td>Depth of Field</td>
                            <td>Low</td>
                            <td>High</td>
                        </tr>
                        <tr>
                            <td>Sample Prep</td>
                            <td>Polished+etched</td>
                            <td>Conductive coating</td>
                        </tr>
                    </table>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="defects">
        <h2>5.3 Crystal Imperfections</h2>
        
        <div class="subsection" id="point-defects">
            <h3>Point Defects</h3>
            <div class="topic-card">
                <h4>Types</h4>
                <ul>
                    <li>Vacancies: Missing atoms</li>
                    <li>Interstitials: Extra atoms in voids</li>
                    <li>Substitutional: Impurity atoms</li>
                </ul>
                
                <h4>Concentration</h4>
                <div class="formula">
                    N<sub>v</sub>/N = exp(-Q<sub>v</sub>/kT)
                </div>
                <p>Where Q<sub>v</sub> ≈ 1 eV for many metals</p>
                
                <div class="example">
                    <h5>Example: Cu Vacancies</h5>
                    <p>At 1000K (Q<sub>v</sub> = 1 eV):</p>
                    <div class="formula">
                        N<sub>v</sub>/N ≈ exp(-1/(8.617×10<sup>-5</sup>×1000)) ≈ 10<sup>-5</sup>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="line-defects">
            <h3>Line Defects (Dislocations)</h3>
            <div class="topic-card">
                <h4>Types</h4>
                <ul>
                    <li>Edge: Extra half-plane of atoms</li>
                    <li>Screw: Spiral ramp of atoms</li>
                    <li>Mixed: Combination of edge and screw</li>
                </ul>
                
                <h4>Burgers Vector (b)</h4>
                <p>Magnitude and direction of lattice distortion</p>
                <div class="formula">
                    τ<sub>critical</sub> = Gb/L (for Frank-Read source)
                </div>
                
                <div class="important">
                    <h4>Dislocation Density</h4>
                    <div class="formula">
                        ρ = (Total dislocation length)/(Volume)
                    </div>
                    <p>Annealed metals: 10<sup>6</sup>-10<sup>8</sup> cm/cm<sup>3</sup></p>
                    <p>Heavily deformed: 10<sup>11</sup>-10<sup>12</sup> cm/cm<sup>3</sup></p>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="interfaces">
            <h3>Interfaces</h3>
            <div class="topic-card">
                <table>
                    <tr>
                        <th>Interface Type</th>
                        <th>Misfit</th>
                        <th>Energy (J/m<sup>2</sup>)</th>
                        <th>Example</th>
                    </tr>
                    <tr>
                        <td>Coherent</td>
                        <td><5%</td>
                        <td>0.05-0.5</td>
                        <td>GP zones</td>
                    </tr>
                    <tr>
                        <td>Semi-coherent</td>
                        <td>5-25%</td>
                        <td>0.5-1.0</td>
                        <td>θ' in Al-Cu</td>
                    </tr>
                    <tr>
                        <td>Incoherent</td>
                        <td>>25%</td>
                        <td>1.0-2.0</td>
                        <td>θ in Al-Cu</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>

    <div class="section diffusion" id="diffusion">
        <h2>5.4 Diffusion in Solids</h2>
        
        <div class="subsection" id="diffusion-equation">
            <h3>Diffusion Equations</h3>
            <div class="topic-card">
                <h4>Fick's First Law</h4>
                <div class="formula">
                    J = -D(∂C/∂x)
                </div>
                
                <h4>Fick's Second Law</h4>
                <div class="formula">
                    ∂C/∂t = D(∂<sup>2</sup>C/∂x<sup>2</sup>)
                </div>
                
                <h4>Solutions</h4>
                <p>Error function solution for constant surface concentration:</p>
                <div class="formula">
                    (C<sub>x</sub>-C<sub>0</sub>)/(C<sub>s</sub>-C<sub>0</sub>) = 1 - erf(x/(2√(Dt)))
                </div>
            </div>
        </div>
        
        <div class="subsection" id="diffusion-types">
            <h3>Types of Diffusion</h3>
            <div class="topic-card">
                <h4>Kirkendall Effect</h4>
                <p>Different diffusion rates create voids (e.g., Cu-Ni diffusion couple)</p>
                
                <h4>Uphill Diffusion</h4>
                <p>Diffusion against concentration gradient due to chemical potential gradient</p>
                
                <h4>Diffusion Mechanisms</h4>
                <table>
                    <tr>
                        <th>Mechanism</th>
                        <th>Activation Energy</th>
                        <th>Example</th>
                    </tr>
                    <tr>
                        <td>Interstitial</td>
                        <td>Low (0.1-1 eV)</td>
                        <td>C in Fe</td>
                    </tr>
                    <tr>
                        <td>Vacancy</td>
                        <td>High (1-5 eV)</td>
                        <td>Self-diffusion</td>
                    </tr>
                    <tr>
                        <td>Grain Boundary</td>
                        <td>Very Low (~0.5Q<sub>v</sub>)</td>
                        <td>Fast diffusion paths</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>

    <div class="section transformation" id="transformations">
        <h2>5.5 Phase Transformations</h2>
        
        <div class="subsection" id="solidification">
            <h3>Solidification</h3>
            <div class="topic-card">
                <h4>Nucleation</h4>
                <div class="formula">
                    ΔG* = (16πγ<sup>3</sup>)/(3ΔG<sub>v</sub><sup>2</sup>)
                </div>
                <p>Where γ = interfacial energy, ΔG<sub>v</sub> = volume free energy change</p>
                
                <h4>Growth</h4>
                <div class="formula">
                    v = μΔT (where μ = growth mobility)
                </div>
                
                <h4>Cast Structures</h4>
                <ol>
                    <li>Chill zone: Fine equiaxed grains</li>
                    <li>Columnar zone: Dendritic growth</li>
                    <li>Equiaxed zone: Central coarse grains</li>
                </ol>
            </div>
        </div>
        
        <div class="subsection" id="solid-state">
            <h3>Solid State Transformations</h3>
            <div class="topic-card">
                <table>
                    <tr>
                        <th>Transformation</th>
                        <th>Mechanism</th>
                        <th>Example</th>
                    </tr>
                    <tr>
                        <td>Precipitation</td>
                        <td>Nucleation & growth</td>
                        <td>Al-Cu (θ")</td>
                    </tr>
                    <tr>
                        <td>Spinoidal</td>
                        <td>Continuous decomposition</td>
                        <td>Cu-Ni-Fe</td>
                    </tr>
                    <tr>
                        <td>Eutectoid</td>
                        <td>Cooperative growth</td>
                        <td>Fe-C (pearlite)</td>
                    </tr>
                    <tr>
                        <td>Martensitic</td>
                        <td>Diffusionless shear</td>
                        <td>Fe-C, Ti alloys</td>
                    </tr>
                </table>
                
                <div class="important">
                    <h4>Gibbs-Thomson Effect</h4>
                    <div class="formula">
                        C<sub>r</sub> = C<sub>∞</sub>exp(2γV<sub>m</sub>/rRT)
                    </div>
                    <p>Where C<sub>r</sub> = solubility of particle with radius r</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section heat-treatment" id="heat-treatment">
        <h2>5.6 Heat Treatment</h2>
        
        <div class="subsection" id="steel-heat">
            <h3>Heat Treatment of Steels</h3>
            <div class="topic-card">
                <h4>TTT Diagrams</h4>
                <div class="diagram" style="background: url('data:image/svg+xml;utf8,<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"500\" height=\"300\" viewBox=\"0 0 500 300\"><path d=\"M50,250 L150,150 L200,100 L300,50 L400,80\" fill=\"none\" stroke=\"%235e35b1\" stroke-width=\"2\"/><path d=\"M50,250 L150,200 L200,180 L250,200 L300,220 L350,240\" fill=\"none\" stroke=\"%23ff7043\" stroke-width=\"2\"/><path d=\"M50,250 L100,200 L150,150 L200,120 L250,150 L300,200\" fill=\"none\" stroke=\"%2326a69a\" stroke-width=\"2\"/><text x=\"100\" y=\"270\" font-size=\"12\">Time (log scale)</text><text x=\"20\" y=\"150\" font-size=\"12\">Temperature (°C)</text><text x=\"200\" y=\"30\" fill=\"%235e35b1\">Martensite</text><text x=\"300\" y=\"270\" fill=\"%23ff7043\">Pearlite</text><text x=\"200\" y=\"180\" fill=\"%2326a69a\">Bainite</text></svg>') no-repeat center; background-size: contain; height: 300px;"></div>
                
                <h4>CCT Diagrams</h4>
                <p>Continuous Cooling Transformation - shows transformation products at different cooling rates</p>
                
                <h4>Surface Hardening</h4>
                <ul>
                    <li>Carburizing: Add carbon at surface (900-950°C)</li>
                    <li>Nitriding: Add nitrogen at surface (500-550°C)</li>
                    <li>Induction hardening: Localized heating + quenching</li>
                </ul>
            </div>
        </div>
        
        <div class="subsection" id="recrystallization">
            <h3>Recovery, Recrystallization & Grain Growth</h3>
            <div class="topic-card">
                <div class="formula">
                    t<sub>R</sub> = t<sub>0</sub>exp(Q<sub>R</sub>/RT)
                </div>
                <p>Where t<sub>R</sub> = recrystallization time, Q<sub>R</sub> ≈ 0.3-0.5Q<sub>v</sub></p>
                
                <div class="formula">
                    D<sup>n</sup> - D<sub>0</sub><sup>n</sup> = kt (Grain growth kinetics)
                </div>
                <p>Where n ≈ 2 for normal grain growth</p>
            </div>
        </div>
    </div>

    <div class="section" id="properties">
        <h2>5.7 Material Properties</h2>
        
        <div class="subsection" id="electronic">
            <h3>Electronic Properties</h3>
            <div class="topic-card">
                <table>
                    <tr>
                        <th>Property</th>
                        <th>Metals</th>
                        <th>Semiconductors</th>
                        <th>Insulators</th>
                    </tr>
                    <tr>
                        <td>Resistivity (Ω·m)</td>
                        <td>10<sup>-8</sup>-10<sup>-6</sup></td>
                        <td>10<sup>-5</sup>-10<sup>6</sup></td>
                        <td>10<sup>10</sup>-10<sup>20</sup></td>
                    </tr>
                    <tr>
                        <td>Band Gap (eV)</td>
                        <td>0</td>
                        <td>0.1-3.0</td>
                        <td>>3.0</td>
                    </tr>
                </table>
            </div>
        </div>
        
        <div class="subsection" id="magnetic">
            <h3>Magnetic Properties</h3>
            <div class="topic-card">
                <table>
                    <tr>
                        <th>Type</th>
                        <th>χ (Susceptibility)</th>
                        <th>Examples</th>
                    </tr>
                    <tr>
                        <td>Diamagnetic</td>
                        <td>-10<sup>-5</sup></td>
                        <td>Cu, Au, Si</td>
                    </tr>
                    <tr>
                        <td>Paramagnetic</td>
                        <td>10<sup>-5</sup>-10<sup>-3</sup></td>
                        <td>Al, Ti, Na</td>
                    </tr>
                    <tr>
                        <td>Ferromagnetic</td>
                        <td>>10<sup>3</sup></td>
                        <td>Fe, Co, Ni</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>

    <div class="section" id="corrosion">
        <h2>5.8 Corrosion</h2>
        
        <div class="subsection" id="corrosion-types">
            <h3>Basic Forms of Corrosion</h3>
            <div class="topic-card">
                <div class="corrosion-types">
                    <div class="corrosion-card">
                        <div class="corrosion-icon">⚡</div>
                        <p>Galvanic</p>
                    </div>
                    <div class="corrosion-card">
                        <div class="corrosion-icon">🔄</div>
                        <p>Uniform</p>
                    </div>
                    <div class="corrosion-card">
                        <div class="corrosion-icon">🕳️</div>
                        <p>Pitting</p>
                    </div>
                    <div class="corrosion-card">
                        <div class="corrosion-icon">↔️</div>
                        <p>Crevice</p>
                    </div>
                    <div class="corrosion-card">
                        <div class="corrosion-icon">🧵</div>
                        <p>Stress</p>
                    </div>
                </div>
                
                <h4>Prevention Methods</h4>
                <ul>
                    <li>Material selection (noble metals, stainless steels)</li>
                    <li>Cathodic protection (sacrificial anodes, impressed current)</li>
                    <li>Coatings (paint, plating, anodizing)</li>
                    <li>Corrosion inhibitors (chromates, phosphates)</li>
                </ul>
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
