<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GATE MT - Transport Phenomena and Rate Processes</title>
    <style>
        :root {
            --primary-color: #6a1b9a;
            --secondary-color: #ff9800;
            --accent-color: #4a148c;
            --light-color: #f3e5f5;
            --dark-color: #4a148c;
            --text-color: #212121;
            --highlight-color: #ffeb3b;
            --success-color: #388e3c;
            --thermal-color: #e53935;
            --fluid-color: #1e88e5;
            --mass-color: #43a047;
            --kinetics-color: #8e24aa;
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
            background: linear-gradient(135deg, #f5f5f5 0%, #e0e0e0 50%, #f5f5f5 100%);
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
            content: "Transport Phenomena";
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-30deg);
            font-size: 120px;
            font-weight: bold;
            color: rgba(106, 27, 154, 0.05);
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
        }
        
        h2 {
            color: var(--primary-color);
            border-bottom: 3px solid var(--accent-color);
            padding-bottom: 0.8rem;
            margin-top: 3rem;
            font-size: 2.2rem;
            background: linear-gradient(to right, transparent, #f3e5f5, transparent);
            padding: 1rem 0;
            text-align: center;
            border-radius: 8px;
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
            border-left: 5px solid var(--fluid-color);
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
            background-color: var(--fluid-color);
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
        .momentum {
            border-top: 4px solid var(--fluid-color);
        }
        
        .heat {
            border-top: 4px solid var(--thermal-color);
        }
        
        .mass {
            border-top: 4px solid var(--mass-color);
        }
        
        .kinetics {
            border-top: 4px solid var(--kinetics-color);
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
        <h1>Transport Phenomena and Rate Processes</h1>
        <p>Complete Guide for GATE Metallurgy (MT) - Section 3 (TestUrSelf)</p>
    </header>

    <div class="toc">
        <h2>Table of Contents</h2>
        <ol>
            <li><a href="#momentum">Momentum Transfer</a></li>
            <li><a href="#heat">Heat Transfer</a></li>
            <li><a href="#mass">Mass Transfer</a></li>
            <li><a href="#dimensional">Dimensional Analysis</a></li>
            <li><a href="#kinetics">Chemical Kinetics</a></li>
            <li><a href="#electro-kinetics">Electrochemical Kinetics</a></li>
        </ol>
    </div>

    <div class="section momentum" id="momentum">
        <h2>3.1 Momentum Transfer</h2>
        
        <div class="subsection" id="viscosity">
            <h3>Concept of Viscosity</h3>
            <div class="topic-card">
                <div class="definition">
                    Viscosity is a measure of a fluid's resistance to deformation under shear stress.
                </div>
                
                <h4>Newton's Law of Viscosity</h4>
                <div class="formula">
                    τ<sub>yx</sub> = -μ(∂v<sub>x</sub>/∂y)
                </div>
                <p>Where:</p>
                <ul>
                    <li>τ<sub>yx</sub> = shear stress in x-direction on y-face</li>
                    <li>μ = dynamic viscosity (Pa·s or kg/m·s)</li>
                    <li>∂v<sub>x</sub>/∂y = velocity gradient</li>
                </ul>
                
                <table>
                    <tr>
                        <th>Fluid</th>
                        <th>Viscosity (Pa·s at 20°C)</th>
                    </tr>
                    <tr>
                        <td>Water</td>
                        <td>0.001</td>
                    </tr>
                    <tr>
                        <td>Air</td>
                        <td>1.8×10<sup>-5</sup></td>
                    </tr>
                    <tr>
                        <td>Molten Iron (1600°C)</td>
                        <td>0.005</td>
                    </tr>
                    <tr>
                        <td>Molten Slag</td>
                        <td>0.1-1.0</td>
                    </tr>
                </table>
                
                <div class="important">
                    <h4>Kinematic Viscosity</h4>
                    <div class="formula">
                        ν = μ/ρ
                    </div>
                    <p>Where ν = kinematic viscosity (m<sup>2</sup>/s) and ρ = density (kg/m<sup>3</sup>)</p>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="shell-balances">
            <h3>Shell Balances</h3>
            <div class="topic-card">
                <h4>General Approach</h4>
                <ol>
                    <li>Select shell geometry (rectangular, cylindrical, spherical)</li>
                    <li>Write momentum balance over thin shell</li>
                    <li>Take limit as shell thickness → 0 to get differential equation</li>
                    <li>Integrate with appropriate boundary conditions</li>
                </ol>
                
                <h4>Example: Laminar Flow in Pipe</h4>
                <div class="formula">
                    (1/r)(d/dr)(rτ<sub>rz</sub>) = ΔP/L
                </div>
                <div class="formula">
                    τ<sub>rz</sub> = -(ΔP/L)(r/2)
                </div>
                <div class="formula">
                    v<sub>z</sub>(r) = (ΔPR<sup>2</sup>/4μL)[1 - (r/R)<sup>2</sup>]
                </div>
                <p>Where R = pipe radius, ΔP = pressure drop, L = pipe length</p>
            </div>
        </div>
        
        <div class="subsection" id="bernoulli">
            <h3>Bernoulli's Equation</h3>
            <div class="topic-card">
                <div class="formula">
                    P<sub>1</sub> + ½ρv<sub>1</sub><sup>2</sup> + ρgh<sub>1</sub> = P<sub>2</sub> + ½ρv<sub>2</sub><sup>2</sup> + ρgh<sub>2</sub>
                </div>
                <p>Assumptions:</p>
                <ul>
                    <li>Steady flow</li>
                    <li>Incompressible fluid</li>
                    <li>Inviscid (frictionless) flow</li>
                    <li>Along a streamline</li>
                </ul>
                
                <div class="example">
                    <h5>Example: Venturi Meter</h5>
                    <p>Given a horizontal venturi with D<sub>1</sub> = 10 cm, D<sub>2</sub> = 5 cm, ΔP = 500 Pa, ρ = 1000 kg/m<sup>3</sup>:</p>
                    <div class="formula">
                        v<sub>1</sub> = √[2ΔP/(ρ((A<sub>1</sub>/A<sub>2</sub>)<sup>2</sup> - 1))] = 0.57 m/s
                    </div>
                    <div class="formula">
                        Q = A<sub>1</sub>v<sub>1</sub> = 0.0045 m<sup>3</sup>/s
                    </div>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="mechanical-energy">
            <h3>Mechanical Energy Balance Equation</h3>
            <div class="topic-card">
                <div class="formula">
                    Δ(P/ρ) + ½Δv<sup>2</sup> + gΔh + F + W<sub>s</sub> = 0
                </div>
                <p>Where:</p>
                <ul>
                    <li>F = friction loss (J/kg)</li>
                    <li>W<sub>s</sub> = shaft work (J/kg)</li>
                </ul>
                
                <h4>Friction Factor Correlations</h4>
                <p>Laminar flow (Re < 2100):</p>
                <div class="formula">
                    f = 16/Re
                </div>
                <p>Turbulent flow (Re > 4000, smooth pipes):</p>
                <div class="formula">
                    1/√f = 4.0 log(Re√f) - 0.4 (Prandtl equation)
                </div>
                <div class="formula">
                    f ≈ 0.0791/Re<sup>0.25</sup> (Blasius equation, 4000 < Re < 10<sup>5</sup>)
                </div>
            </div>
        </div>
        
        <div class="subsection" id="flow-past-surfaces">
            <h3>Flow Past Plane Surfaces and Through Pipes</h3>
            <div class="topic-card">
                <h4>Boundary Layer Concepts</h4>
                <div class="formula">
                    δ ≈ 5x/√Re<sub>x</sub> (laminar)
                </div>
                <div class="formula">
                    δ ≈ 0.37x/Re<sub>x</sub><sup>1/5</sup> (turbulent)
                </div>
                <p>Where Re<sub>x</sub> = ρv<sub>∞</sub>x/μ</p>
                
                <h4>Drag Coefficient</h4>
                <table>
                    <tr>
                        <th>Geometry</th>
                        <th>Laminar C<sub>D</sub></th>
                        <th>Turbulent C<sub>D</sub></th>
                    </tr>
                    <tr>
                        <td>Flat plate (parallel)</td>
                        <td>1.328/√Re<sub>L</sub></td>
                        <td>0.074/Re<sub>L</sub><sup>1/5</sup></td>
                    </tr>
                    <tr>
                        <td>Sphere</td>
                        <td>24/Re</td>
                        <td>≈0.44</td>
                    </tr>
                    <tr>
                        <td>Cylinder (cross flow)</td>
                        <td>Varies</td>
                        <td>≈1.0</td>
                    </tr>
                </table>
                
                <div class="key-points">
                    <h4>Pipe Flow Characteristics</h4>
                    <ul>
                        <li>Laminar: Re < 2100, parabolic velocity profile</li>
                        <li>Transitional: 2100 < Re < 4000</li>
                        <li>Turbulent: Re > 4000, flatter velocity profile</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <div class="section heat" id="heat">
        <h2>3.2 Heat Transfer</h2>
        
        <div class="subsection" id="conduction">
            <h3>Conduction and Fourier's Law</h3>
            <div class="topic-card">
                <div class="definition">
                    Heat conduction is the transfer of thermal energy from more energetic to less energetic particles due to interactions between particles.
                </div>
                
                <h4>Fourier's Law</h4>
                <div class="formula">
                    q<sub>x</sub> = -k(∂T/∂x)
                </div>
                <p>Where:</p>
                <ul>
                    <li>q<sub>x</sub> = heat flux (W/m<sup>2</sup>)</li>
                    <li>k = thermal conductivity (W/m·K)</li>
                    <li>∂T/∂x = temperature gradient</li>
                </ul>
                
                <table>
                    <tr>
                        <th>Material</th>
                        <th>k (W/m·K at 300K)</th>
                    </tr>
                    <tr>
                        <td>Copper</td>
                        <td>401</td>
                    </tr>
                    <tr>
                        <td>Steel (304)</td>
                        <td>16.2</td>
                    </tr>
                    <tr>
                        <td>Alumina</td>
                        <td>30</td>
                    </tr>
                    <tr>
                        <td>Air</td>
                        <td>0.026</td>
                    </tr>
                </table>
                
                <h4>1-D Steady State Conduction</h4>
                <p>Planar wall:</p>
                <div class="formula">
                    q = (k/L)(T<sub>1</sub> - T<sub>2</sub>)
                </div>
                <p>Cylindrical wall:</p>
                <div class="formula">
                    q = (2πkL/ln(r<sub>2</sub>/r<sub>1</sub>))(T<sub>1</sub> - T<sub>2</sub>)
                </div>
            </div>
        </div>
        
        <div class="subsection" id="convection">
            <h3>Convection</h3>
            <div class="topic-card">
                <div class="definition">
                    Convection is heat transfer between a surface and a moving fluid at different temperatures.
                </div>
                
                <h4>Newton's Law of Cooling</h4>
                <div class="formula">
                    q = hA(T<sub>s</sub> - T<sub>∞</sub>)
                </div>
                <p>Where h = convective heat transfer coefficient (W/m<sup>2</sup>·K)</p>
                
                <h4>Forced Convection Correlations</h4>
                <p>Flat plate (laminar, Re < 5×10<sup>5</sup>):</p>
                <div class="formula">
                    Nu<sub>x</sub> = 0.332Re<sub>x</sub><sup>1/2</sup>Pr<sup>1/3</sup>
                </div>
                <p>Flat plate (turbulent):</p>
                <div class="formula">
                    Nu<sub>x</sub> = 0.0296Re<sub>x</sub><sup>4/5</sup>Pr<sup>1/3</sup>
                </div>
                <p>Pipe flow (Re > 10<sup>4</sup>, 0.6 < Pr < 160):</p>
                <div class="formula">
                    Nu<sub>D</sub> = 0.023Re<sub>D</sub><sup>4/5</sup>Pr<sup>n</sup>
                </div>
                <p>Where n = 0.4 for heating, 0.3 for cooling</p>
                
                <div class="important">
                    <h4>Nusselt Number Relationships</h4>
                    <div class="formula">
                        Nu = hL/k = (convective heat transfer)/(conductive heat transfer)
                    </div>
                    <p>Where L = characteristic length</p>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="radiation">
            <h3>Radiation</h3>
            <div class="topic-card">
                <h4>Black Body Radiation</h4>
                <div class="formula">
                    E<sub>b</sub> = σT<sup>4</sup> (Stefan-Boltzmann Law)
                </div>
                <p>Where σ = 5.67×10<sup>-8</sup> W/m<sup>2</sup>·K<sup>4</sup></p>
                
                <h4>Planck's Law</h4>
                <div class="formula">
                    E<sub>λb</sub> = (2πhc<sub>0</sub><sup>2</sup>)/(λ<sup>5</sup>[exp(hc<sub>0</sub>/λkT) - 1])
                </div>
                
                <h4>Kirchhoff's Law</h4>
                <div class="formula">
                    α = ε (for surfaces in thermal equilibrium)
                </div>
                <p>Where α = absorptivity, ε = emissivity</p>
                
                <h4>View Factors</h4>
                <div class="formula">
                    F<sub>12</sub> = (1/A<sub>1</sub>)∫∫(cosθ<sub>1</sub>cosθ<sub>2</sub>/πr<sup>2</sup>)dA<sub>1</sub>dA<sub>2</sub>
                </div>
                
                <div class="example">
                    <h5>Example: Radiation Shield</h5>
                    <p>Two large parallel plates with ε = 0.8 at T<sub>1</sub> = 800K and T<sub>2</sub> = 500K:</p>
                    <p>Without shield: q/A = σ(T<sub>1</sub><sup>4</sup> - T<sub>2</sub><sup>4</sup>)/(1/ε<sub>1</sub> + 1/ε<sub>2</sub> - 1) = 12.2 kW/m<sup>2</sup></p>
                    <p>With shield (ε<sub>s</sub> = 0.05): q/A = σ(T<sub>1</sub><sup>4</sup> - T<sub>2</sub><sup>4</sup>)/(1/ε<sub>1</sub> + 1/ε<sub>2</sub> + 2/ε<sub>s</sub> - 2) = 0.3 kW/m<sup>2</sup></p>
                </div>
            </div>
        </div>
    </div>

    <div class="section mass" id="mass">
        <h2>3.3 Mass Transfer</h2>
        
        <div class="subsection" id="diffusion">
            <h3>Diffusion and Fick's Laws</h3>
            <div class="topic-card">
                <h4>Fick's First Law</h4>
                <div class="formula">
                    J<sub>A</sub> = -D<sub>AB</sub>(∂C<sub>A</sub>/∂x)
                </div>
                <p>Where:</p>
                <ul>
                    <li>J<sub>A</sub> = molar flux (mol/m<sup>2</sup>·s)</li>
                    <li>D<sub>AB</sub> = diffusion coefficient (m<sup>2</sup>/s)</li>
                    <li>C<sub>A</sub> = concentration of A (mol/m<sup>3</sup>)</li>
                </ul>
                
                <h4>Fick's Second Law</h4>
                <div class="formula">
                    ∂C<sub>A</sub>/∂t = D<sub>AB</sub>(∂<sup>2</sup>C<sub>A</sub>/∂x<sup>2</sup>)
                </div>
                
                <table>
                    <tr>
                        <th>System</th>
                        <th>D (m<sup>2</sup>/s)</th>
                    </tr>
                    <tr>
                        <td>O<sub>2</sub> in air (25°C)</td>
                        <td>2.1×10<sup>-5</sup></td>
                    </tr>
                    <tr>
                        <td>Cu in Al (500°C)</td>
                        <td>1.3×10<sup>-14</sup></td>
                    </tr>
                    <tr>
                        <td>C in γ-Fe (900°C)</td>
                        <td>1.5×10<sup>-11</sup></td>
                    </tr>
                </table>
            </div>
        </div>
        
        <div class="subsection" id="mass-coeff">
            <h3>Mass Transfer Coefficients</h3>
            <div class="topic-card">
                <div class="formula">
                    N<sub>A</sub> = k<sub>c</sub>(C<sub>As</sub> - C<sub>A∞</sub>)
                </div>
                <p>Where k<sub>c</sub> = mass transfer coefficient (m/s)</p>
                
                <h4>Sherwood Number</h4>
                <div class="formula">
                    Sh = k<sub>c</sub>L/D<sub>AB</sub>
                </div>
                
                <h4>Correlations</h4>
                <p>Flat plate (laminar):</p>
                <div class="formula">
                    Sh<sub>x</sub> = 0.332Re<sub>x</sub><sup>1/2</sup>Sc<sup>1/3</sup>
                </div>
                <p>Pipe flow:</p>
                <div class="formula">
                    Sh<sub>D</sub> = 0.023Re<sub>D</sub><sup>0.8</sup>Sc<sup>1/3</sup>
                </div>
                <p>Where Sc = ν/D<sub>AB</sub> = Schmidt number</p>
            </div>
        </div>
    </div>

    <div class="section" id="dimensional">
        <h2>3.4 Dimensional Analysis</h2>
        
        <div class="subsection" id="buckingham">
            <h3>Buckingham Pi Theorem</h3>
            <div class="topic-card">
                <div class="definition">
                    If a physical process involves n variables and m fundamental dimensions, then there are n - m independent dimensionless groups that describe the process.
                </div>
                
                <h4>Procedure</h4>
                <ol>
                    <li>List all n variables involved</li>
                    <li>Express each variable in terms of m fundamental dimensions (M, L, T, θ)</li>
                    <li>Select m repeating variables that include all fundamental dimensions</li>
                    <li>Form n - m dimensionless π groups</li>
                </ol>
                
                <div class="example">
                    <h5>Example: Pipe Flow</h5>
                    <p>Variables: ΔP, ρ, μ, v, D, L → n = 6</p>
                    <p>Dimensions: M, L, T → m = 3</p>
                    <p>π groups: Eu = ΔP/ρv<sup>2</sup>, Re = ρvD/μ, L/D</p>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="dimensionless">
            <h3>Significant Dimensionless Numbers</h3>
            <div class="topic-card">
                <table>
                    <tr>
                        <th>Number</th>
                        <th>Formula</th>
                        <th>Significance</th>
                    </tr>
                    <tr>
                        <td>Reynolds (Re)</td>
                        <td>ρvL/μ</td>
                        <td>Inertial/viscous forces</td>
                    </tr>
                    <tr>
                        <td>Prandtl (Pr)</td>
                        <td>C<sub>p</sub>μ/k</td>
                        <td>Momentum/thermal diffusivity</td>
                    </tr>
                    <tr>
                        <td>Nusselt (Nu)</td>
                        <td>hL/k</td>
                        <td>Convection/conduction</td>
                    </tr>
                    <tr>
                        <td>Schmidt (Sc)</td>
                        <td>ν/D</td>
                        <td>Momentum/mass diffusivity</td>
                    </tr>
                    <tr>
                        <td>Sherwood (Sh)</td>
                        <td>k<sub>c</sub>L/D</td>
                        <td>Convective/diffusive mass transfer</td>
                    </tr>
                    <tr>
                        <td>Grashof (Gr)</td>
                        <td>gβΔTL<sup>3</sup>/ν<sup>2</sup></td>
                        <td>Buoyancy/viscous forces</td>
                    </tr>
                </table>
                
                <div class="important">
                    <h4>Analogies</h4>
                    <p>Reynolds analogy:</p>
                    <div class="formula">
                        f/2 = St = St<sub>m</sub>
                    </div>
                    <p>Chilton-Colburn analogy:</p>
                    <div class="formula">
                        j<sub>H</sub> = j<sub>D</sub> = f/2
                    </div>
                    <p>Where j<sub>H</sub> = StPr<sup>2/3</sup>, j<sub>D</sub> = St<sub>m</sub>Sc<sup>2/3</sup></p>
                </div>
            </div>
        </div>
    </div>

    <div class="section kinetics" id="kinetics">
        <h2>3.5 Chemical Kinetics</h2>
        
        <div class="subsection" id="basic-laws">
            <h3>Basic Laws of Chemical Kinetics</h3>
            <div class="topic-card">
                <h4>Reaction Rate</h4>
                <div class="formula">
                    r = (1/ν<sub>i</sub>)(dC<sub>i</sub>/dt)
                </div>
                <p>Where ν<sub>i</sub> = stoichiometric coefficient</p>
                
                <h4>First Order Reaction</h4>
                <div class="formula">
                    -dC<sub>A</sub>/dt = kC<sub>A</sub>
                </div>
                <div class="formula">
                    ln(C<sub>A</sub>/C<sub>A0</sub>) = -kt
                </div>
                <p>Half-life:</p>
                <div class="formula">
                    t<sub>1/2</sub> = ln(2)/k
                </div>
                
                <h4>Arrhenius Equation</h4>
                <div class="formula">
                    k = A exp(-E<sub>a</sub>/RT)
                </div>
                <p>Where:</p>
                <ul>
                    <li>A = pre-exponential factor</li>
                    <li>E<sub>a</sub> = activation energy (J/mol)</li>
                    <li>R = gas constant (8.314 J/mol·K)</li>
                </ul>
            </div>
        </div>
        
        <div class="subsection" id="heterogeneous">
            <h3>Heterogeneous Reactions</h3>
            <div class="topic-card">
                <h4>Shrinking Core Model</h4>
                <p>Three resistances in series:</p>
                <ol>
                    <li>Gas film diffusion</li>
                    <li>Ash layer diffusion</li>
                    <li>Chemical reaction</li>
                </ol>
                
                <h4>Rate Controlling Steps</h4>
                <p>Film diffusion control:</p>
                <div class="formula">
                    t = τ(1 - X)
                </div>
                <p>Ash diffusion control:</p>
                <div class="formula">
                    t = τ[1 - 3(1 - X)<sup>2/3</sup> + 2(1 - X)]
                </div>
                <p>Chemical reaction control:</p>
                <div class="formula">
                    t = τ[1 - (1 - X)<sup>1/3</sup>]
                </div>
                <p>Where τ = complete conversion time</p>
            </div>
        </div>
        
        <div class="subsection" id="oxidation">
            <h3>Oxidation Kinetics</h3>
            <div class="topic-card">
                <h4>Parabolic Law</h4>
                <div class="formula">
                    x<sup>2</sup> = k<sub>p</sub>t
                </div>
                <p>Where x = oxide thickness, k<sub>p</sub> = parabolic rate constant</p>
                
                <h4>Linear Law</h4>
                <div class="formula">
                    x = k<sub>l</sub>t
                </div>
                <p>Where k<sub>l</sub> = linear rate constant</p>
                
                <table>
                    <tr>
                        <th>Metal</th>
                        <th>Oxide</th>
                        <th>Rate Law</th>
                        <th>Activation Energy (kJ/mol)</th>
                    </tr>
                    <tr>
                        <td>Copper</td>
                        <td>Cu<sub>2</sub>O</td>
                        <td>Parabolic</td>
                        <td>110</td>
                    </tr>
                    <tr>
                        <td>Iron</td>
                        <td>FeO</td>
                        <td>Parabolic</td>
                        <td>96</td>
                    </tr>
                    <tr>
                        <td>Aluminum</td>
                        <td>Al<sub>2</sub>O<sub>3</sub></td>
                        <td>Parabolic</td>
                        <td>330</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>

    <div class="section" id="electro-kinetics">
        <h2>3.6 Electrochemical Kinetics</h2>
        
        <div class="subsection" id="polarization">
            <h3>Polarization</h3>
            <div class="topic-card">
                <h4>Butler-Volmer Equation</h4>
                <div class="formula">
                    i = i<sub>0</sub>[exp(α<sub>a</sub>Fη/RT) - exp(-α<sub>c</sub>Fη/RT)]
                </div>
                <p>Where:</p>
                <ul>
                    <li>i<sub>0</sub> = exchange current density</li>
                    <li>α = transfer coefficients</li>
                    <li>η = overpotential</li>
                </ul>
                
                <h4>Tafel Equation</h4>
                <div class="formula">
                    η = a + b log|i|
                </div>
                <p>Where:</p>
                <div class="formula">
                    b = ±(2.3RT/αF)
                </div>
                
                <table>
                    <tr>
                        <th>Electrode Reaction</th>
                        <th>i<sub>0</sub> (A/cm<sup>2</sup>)</th>
                    </tr>
                    <tr>
                        <td>H<sup>+</sup>/H<sub>2</sub> on Pt</td>
                        <td>10<sup>-3</sup></td>
                    </tr>
                    <tr>
                        <td>H<sup>+</sup>/H<sub>2</sub> on Hg</td>
                        <td>10<sup>-12</sup></td>
                    </tr>
                    <tr>
                        <td>Fe<sup>2+</sup>/Fe<sup>3+</sup> on Pt</td>
                        <td>10<sup>-5</sup></td>
                    </tr>
                </table>
            </div>
        </div>
    </div>
    
    <footer>
        <p>© TestUrSelf | All Rights Reserved</p>
    </footer>
</body>
</html>
