<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GATE MT - Mechanical Metallurgy</title>
    <style>
        :root {
            --primary-color: #1a237e;
            --secondary-color: #c62828;
            --accent-color: #1565c0;
            --light-color: #e3f2fd;
            --dark-color: #0d47a1;
            --text-color: #212121;
            --highlight-color: #ffc107;
            --success-color: #2e7d32;
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
        
        /* Watermark */
        body::before {
            content: "TestUrSelf";
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-45deg);
            font-size: 120px;
            font-weight: bold;
            color: rgba(198, 40, 40, 0.08);
            z-index: -1;
            pointer-events: none;
            white-space: nowrap;
            text-transform: uppercase;
            letter-spacing: 10px;
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
            box-shadow: 0 4px 20px rgba(0,0,0,0.2);
            position: relative;
            z-index: 1;
        }
        
        h1 {
            margin: 0;
            font-size: 2.5rem;
            font-weight: 700;
        }
        
        h2 {
            color: var(--primary-color);
            border-bottom: 3px solid var(--accent-color);
            padding-bottom: 0.8rem;
            margin-top: 3rem;
            font-size: 2rem;
        }
        
        h3 {
            color: var(--dark-color);
            margin-top: 2.5rem;
            font-size: 1.6rem;
            border-left: 5px solid var(--accent-color);
            padding-left: 1rem;
        }
        
        h4 {
            color: #424242;
            margin-top: 1.8rem;
            font-size: 1.3rem;
        }
        
        .section {
            background-color: white;
            border-radius: 8px;
            padding: 2.5rem;
            margin-bottom: 3rem;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: relative;
            z-index: 1;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .subsection {
            margin-left: 1.5rem;
            border-left: 3px solid #e0e0e0;
            padding-left: 2rem;
            margin-top: 2rem;
            transition: border-color 0.3s;
        }
        
        .subsection:hover {
            border-left-color: var(--accent-color);
        }
        
        .topic-card {
            background-color: var(--light-color);
            border-radius: 8px;
            padding: 1.8rem;
            margin: 1.8rem 0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
        }
        
        .formula {
            font-family: 'Courier New', monospace;
            background-color: #f5f5f5;
            padding: 1rem 1.5rem;
            border-radius: 6px;
            overflow-x: auto;
            margin: 1.2rem 0;
            border-left: 4px solid var(--accent-color);
            font-size: 1.1rem;
        }
        
        .tensor {
            display: inline-block;
            margin: 1rem 0;
            padding: 0.5rem;
            background-color: #f0f0f0;
            border-radius: 4px;
            font-family: 'Courier New', monospace;
        }
        
        .tensor-row {
            display: flex;
            justify-content: center;
        }
        
        .tensor-cell {
            padding: 0.3rem 0.6rem;
            text-align: center;
        }
        
        .mohr-circle {
            text-align: center;
            margin: 1.5rem 0;
            padding: 1rem;
            background-color: #f9f9f9;
            border-radius: 8px;
        }
        
        .mohr-circle img {
            max-width: 100%;
            height: auto;
        }
        
        .toc-container {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4e8eb 100%);
            padding: 2rem;
            border-radius: 8px;
            margin-bottom: 3rem;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            border-left: 6px solid var(--accent-color);
        }
        
        .toc {
            columns: 2;
            column-gap: 2rem;
        }
        
        .toc-list {
            list-style-type: none;
            padding: 0;
            margin: 0;
        }
        
        .toc-item {
            break-inside: avoid;
            padding: 0.8rem 0;
            position: relative;
            padding-left: 2rem;
        }
        
        .toc-item::before {
            content: "•";
            position: absolute;
            left: 0;
            color: var(--accent-color);
            font-size: 1.5rem;
            line-height: 1;
        }
        
        .toc-link {
            text-decoration: none;
            color: var(--dark-color);
            font-weight: 500;
            transition: color 0.3s;
            display: block;
        }
        
        .toc-link:hover {
            color: var(--secondary-color);
            transform: translateX(5px);
        }
        
        .toc-sublist {
            list-style-type: none;
            padding-left: 1.5rem;
            margin-top: 0.5rem;
        }
        
        .toc-subitem {
            padding: 0.4rem 0;
            position: relative;
            padding-left: 1.5rem;
        }
        
        .toc-subitem::before {
            content: "○";
            position: absolute;
            left: 0;
            color: var(--secondary-color);
        }
        
        .diagram {
            text-align: center;
            margin: 1.5rem 0;
            padding: 1rem;
            background-color: #f0f8ff;
            border-radius: 8px;
        }
        
        .diagram img {
            max-width: 100%;
            height: auto;
            border: 1px solid #ddd;
        }
        
        .test-yourself {
            background: linear-gradient(135deg, #fff3e0 0%, #ffecb3 100%);
            border-left: 6px solid var(--highlight-color);
        }
        
        footer {
            text-align: center;
            margin-top: 3rem;
            padding: 2rem;
            color: var(--primary-color);
            border-top: 1px solid #e0e0e0;
        }
        
        @media (max-width: 768px) {
            .toc {
                columns: 1;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Mechanical Metallurgy</h1>
        <p>Complete Guide for GATE Metallurgy (MT) - Section 6 (TestUrSelf)</p>
    </header>

    <div class="toc-container">
        <h2>Table of Contents</h2>
        <div class="toc">
            <ul class="toc-list">
                <li class="toc-item">
                    <a href="#stress-strain" class="toc-link">6.1 Stress and Strain Analysis</a>
                    <ul class="toc-sublist">
                        <li class="toc-subitem"><a href="#tensors" class="toc-link">Stress and Strain Tensors</a></li>
                        <li class="toc-subitem"><a href="#mohr-circle" class="toc-link">Mohr's Circle</a></li>
                        <li class="toc-subitem"><a href="#elasticity" class="toc-link">Elasticity and Stiffness</a></li>
                        <li class="toc-subitem"><a href="#yield-criteria" class="toc-link">Yield Criteria</a></li>
                    </ul>
                </li>
                <li class="toc-item">
                    <a href="#plastic-deformation" class="toc-link">6.2 Plastic Deformation</a>
                    <ul class="toc-sublist">
                        <li class="toc-subitem"><a href="#slip-twinning" class="toc-link">Slip and Twinning</a></li>
                    </ul>
                </li>
                <li class="toc-item">
                    <a href="#dislocations" class="toc-link">6.3 Dislocation Theory</a>
                    <ul class="toc-sublist">
                        <li class="toc-subitem"><a href="#dislocation-types" class="toc-link">Dislocation Types</a></li>
                        <li class="toc-subitem"><a href="#dislocation-dynamics" class="toc-link">Dislocation Dynamics</a></li>
                    </ul>
                </li>
                <li class="toc-item">
                    <a href="#strengthening" class="toc-link">6.4 Strengthening Mechanisms</a>
                </li>
                <li class="toc-item">
                    <a href="#fracture" class="toc-link">6.5 Fracture Behavior</a>
                    <ul class="toc-sublist">
                        <li class="toc-subitem"><a href="#griffith-theory" class="toc-link">Griffith Theory</a></li>
                        <li class="toc-subitem"><a href="#fracture-mechanics" class="toc-link">Fracture Mechanics</a></li>
                    </ul>
                </li>
                <li class="toc-item">
                    <a href="#fatigue" class="toc-link">6.6 Fatigue</a>
                </li>
                <li class="toc-item">
                    <a href="#creep" class="toc-link">6.7 High Temperature Deformation</a>
                </li>
                <li class="toc-item">
                    <a href="#test-yourself" class="toc-link">TestUrSelf's Course</a>
                </li>
            </ul>
        </div>
    </div>

    <!-- 6.1 Stress and Strain Analysis -->
    <div class="section" id="stress-strain">
        <h2>6.1 Stress and Strain Analysis</h2>
        
        <div class="subsection" id="tensors">
            <h3>Stress and Strain Tensors</h3>
            <div class="topic-card">
                <h4>Stress Tensor (σ<sub>ij</sub>)</h4>
                <div class="tensor">
                    <div class="tensor-row">
                        <div class="tensor-cell">σ<sub>xx</sub></div>
                        <div class="tensor-cell">τ<sub>xy</sub></div>
                        <div class="tensor-cell">τ<sub>xz</sub></div>
                    </div>
                    <div class="tensor-row">
                        <div class="tensor-cell">τ<sub>yx</sub></div>
                        <div class="tensor-cell">σ<sub>yy</sub></div>
                        <div class="tensor-cell">τ<sub>yz</sub></div>
                    </div>
                    <div class="tensor-row">
                        <div class="tensor-cell">τ<sub>zx</sub></div>
                        <div class="tensor-cell">τ<sub>zy</sub></div>
                        <div class="tensor-cell">σ<sub>zz</sub></div>
                    </div>
                </div>
                
                <h4>Strain Tensor (ε<sub>ij</sub>)</h4>
                <div class="tensor">
                    <div class="tensor-row">
                        <div class="tensor-cell">ε<sub>xx</sub></div>
                        <div class="tensor-cell">γ<sub>xy</sub>/2</div>
                        <div class="tensor-cell">γ<sub>xz</sub>/2</div>
                    </div>
                    <div class="tensor-row">
                        <div class="tensor-cell">γ<sub>yx</sub>/2</div>
                        <div class="tensor-cell">ε<sub>yy</sub></div>
                        <div class="tensor-cell">γ<sub>yz</sub>/2</div>
                    </div>
                    <div class="tensor-row">
                        <div class="tensor-cell">γ<sub>zx</sub>/2</div>
                        <div class="tensor-cell">γ<sub>zy</sub>/2</div>
                        <div class="tensor-cell">ε<sub>zz</sub></div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="mohr-circle">
            <h3>Mohr's Circle Representation</h3>
            <div class="topic-card">
                <div class="mohr-circle">
                    <img src="Mohrs-circle-construction.png" alt="Mohr's Circle Diagram">
                    <p>Mohr's Circle for 2D stress state</p>
                </div>
                
                <div class="formula">
                    Center: C = (σ<sub>x</sub> + σ<sub>y</sub>)/2
                </div>
                <div class="formula">
                    Radius: R = √[((σ<sub>x</sub> - σ<sub>y</sub>)/2)² + τ<sub>xy</sub>²]
                </div>
                <div class="formula">
                    Principal Stresses: σ<sub>1,2</sub> = C ± R
                </div>
            </div>
        </div>
        
        <div class="subsection" id="elasticity">
            <h3>Elasticity, Stiffness and Compliance Tensors</h3>
            <div class="topic-card">
                <h4>Generalized Hooke's Law</h4>
                <div class="formula">
                    σ<sub>ij</sub> = C<sub>ijkl</sub>ε<sub>kl</sub>
                </div>
                <p>Where C<sub>ijkl</sub> is the stiffness tensor (4th rank, 81 components)</p>
                
                <h4>For Isotropic Materials</h4>
                <div class="formula">
                    C<sub>1111</sub> = C<sub>2222</sub> = C<sub>3333</sub> = λ + 2μ
                </div>
                <div class="formula">
                    C<sub>1122</sub> = C<sub>1133</sub> = C<sub>2233</sub> = λ
                </div>
                <div class="formula">
                    C<sub>1212</sub> = C<sub>1313</sub> = C<sub>2323</sub> = μ
                </div>
                <p>Where λ and μ are Lamé constants:</p>
                <div class="formula">
                    λ = Eν/[(1+ν)(1-2ν)]
                </div>
                <div class="formula">
                    μ = G = E/[2(1+ν)]
                </div>
            </div>
        </div>
        
        <div class="subsection" id="yield-criteria">
            <h3>Yield Criteria</h3>
            <div class="topic-card">
                <h4>Von Mises Criterion</h4>
                <div class="formula">
                    (σ<sub>1</sub> - σ<sub>2</sub>)² + (σ<sub>2</sub> - σ<sub>3</sub>)² + (σ<sub>3</sub> - σ<sub>1</sub>)² = 2σ<sub>y</sub>²
                </div>
                
                <h4>Tresca Criterion</h4>
                <div class="formula">
                    max(|σ<sub>1</sub> - σ<sub>2</sub>|, |σ<sub>2</sub> - σ<sub>3</sub>|, |σ<sub>3</sub> - σ<sub>1</sub>|) = σ<sub>y</sub>
                </div>
                
                <div class="diagram">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3d/Yield_surfaces.png/600px-Yield_surfaces.png" alt="Yield Criteria Comparison">
                    <p>Comparison of Von Mises and Tresca yield criteria</p>
                </div>
            </div>
        </div>
    </div>

    <!-- 6.2 Plastic Deformation -->
    <div class="section" id="plastic-deformation">
        <h2>6.2 Plastic Deformation</h2>
        
        <div class="subsection" id="slip-twinning">
            <h3>Slip and Twinning</h3>
            <div class="topic-card">
                <h4>Slip Systems</h4>
                <table>
                    <tr>
                        <th>Crystal Structure</th>
                        <th>Slip Plane</th>
                        <th>Slip Direction</th>
                        <th># Slip Systems</th>
                    </tr>
                    <tr>
                        <td>FCC</td>
                        <td>{111}</td>
                        <td>&lt;110&gt;</td>
                        <td>12</td>
                    </tr>
                    <tr>
                        <td>BCC</td>
                        <td>{110}, {112}, {123}</td>
                        <td>&lt;111&gt;</td>
                        <td>48</td>
                    </tr>
                    <tr>
                        <td>HCP</td>
                        <td>(0001)</td>
                        <td>&lt;11-20&gt;</td>
                        <td>3</td>
                    </tr>
                </table>
                
                <h4>Schmid's Law</h4>
                <div class="formula">
                    τ<sub>CRSS</sub> = σcosφcosλ
                </div>
                <p>Where φ is angle between stress axis and slip plane normal, λ is angle between stress axis and slip direction</p>
                
                <h4>Twinning</h4>
                <div class="formula">
                    K<sub>1</sub> = {10-12} ⟨10-1-1⟩ for HCP metals
                </div>
                <p>Twinning shear (γ) for common metals:</p>
                <div class="formula">
                    γ = s/2 where s is twinning shear magnitude
                </div>
            </div>
        </div>
    </div>

    <!-- 6.3 Dislocation Theory -->
    <div class="section" id="dislocations">
        <h2>6.3 Dislocation Theory</h2>
        
        <div class="subsection" id="dislocation-types">
            <h3>Dislocation Types</h3>
            <div class="topic-card">
                <h4>Edge Dislocation</h4>
                <div class="diagram">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3a/Edge_dislocation.svg/500px-Edge_dislocation.svg.png" alt="Edge Dislocation">
                    <p>Edge dislocation with extra half-plane</p>
                </div>
                <div class="formula">
                    b ⊥ dislocation line
                </div>
                
                <h4>Screw Dislocation</h4>
                <div class="diagram">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1b/Screw_dislocation.svg/500px-Screw_dislocation.svg.png" alt="Screw Dislocation">
                    <p>Screw dislocation with spiral ramp</p>
                </div>
                <div class="formula">
                    b ∥ dislocation line
                </div>
                
                <h4>Mixed Dislocation</h4>
                <div class="formula">
                    b = b<sub>edge</sub> + b<sub>screw</sub>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="dislocation-dynamics">
            <h3>Dislocation Dynamics</h3>
            <div class="topic-card">
                <h4>Stress Fields</h4>
                <p><strong>Edge dislocation:</strong></p>
                <div class="formula">
                    σ<sub>xx</sub> = -[Gb/(2π(1-ν))][y(3x²+y²)/(x²+y²)²]
                </div>
                <div class="formula">
                    σ<sub>yy</sub> = [Gb/(2π(1-ν))][y(x²-y²)/(x²+y²)²]
                </div>
                
                <p><strong>Screw dislocation:</strong></p>
                <div class="formula">
                    σ<sub>xz</sub> = -[Gb/(2π)][y/(x²+y²)]
                </div>
                <div class="formula">
                    σ<sub>yz</sub> = [Gb/(2π)][x/(x²+y²)]
                </div>
                
                <h4>Dislocation Energy</h4>
                <div class="formula">
                    E = [Gb²/(4πK)]ln(R/r<sub>0</sub>)
                </div>
                <p>Where K = 1 for screw, K = 1-ν for edge dislocations</p>
                
                <h4>Frank-Read Source</h4>
                <div class="formula">
                    Critical stress: τ<sub>c</sub> = Gb/L
                </div>
                <p>Where L is segment length between pinning points</p>
            </div>
        </div>
    </div>

    <!-- 6.4 Strengthening Mechanisms -->
    <div class="section" id="strengthening">
        <h2>6.4 Strengthening Mechanisms</h2>
        
        <div class="topic-card">
            <h4>Work/Strain Hardening</h4>
            <div class="formula">
                σ = σ<sub>0</sub> + Kε<sup>n</sup>
            </div>
            <p>Where n is strain hardening exponent (0.1-0.5 for metals)</p>
            
            <h4>Grain Boundary Strengthening (Hall-Petch)</h4>
            <div class="formula">
                σ<sub>y</sub> = σ<sub>0</sub> + k<sub>y</sub>d<sup>-1/2</sup>
            </div>
            
            <h4>Solid Solution Strengthening</h4>
            <div class="formula">
                Δτ = Gb√(cε)
            </div>
            <p>Where c is solute concentration, ε is size misfit parameter</p>
            
            <h4>Precipitation Strengthening</h4>
            <div class="formula">
                Δτ = Gb/L (Orowan bypassing)
            </div>
            <div class="formula">
                Δτ = γ<sub>APB</sub>b/r (Ordered precipitates)
            </div>
        </div>
    </div>

    <!-- 6.5 Fracture Behavior -->
    <div class="section" id="fracture">
        <h2>6.5 Fracture Behavior</h2>
        
        <div class="subsection" id="griffith-theory">
            <h3>Griffith Theory</h3>
            <div class="topic-card">
                <div class="formula">
                    σ<sub>f</sub> = √(2Eγ<sub>s</sub>/πa)
                </div>
                <p>Where γ<sub>s</sub> is surface energy, a is crack length</p>
                
                <h4>Modified for Plasticity</h4>
                <div class="formula">
                    σ<sub>f</sub> = √(E(2γ<sub>s</sub> + γ<sub>p</sub>)/πa)
                </div>
                <p>Where γ<sub>p</sub> is plastic work per unit area</p>
            </div>
        </div>
        
        <div class="subsection" id="fracture-mechanics">
            <h3>Linear Elastic Fracture Mechanics</h3>
            <div class="topic-card">
                <h4>Stress Intensity Factor</h4>
                <div class="formula">
                    K<sub>I</sub> = Yσ√(πa)
                </div>
                <p>Where Y is geometry factor (~1 for center crack)</p>
                
                <h4>Fracture Toughness</h4>
                <div class="formula">
                    K<sub>Ic</sub> = √(EG<sub>c</sub>)
                </div>
                <p>Where G<sub>c</sub> is critical strain energy release rate</p>
                
                <h4>Ductile-to-Brittle Transition</h4>
                <div class="formula">
                    T<sub>c</sub> = T<sub>0</sub> + (1/β)ln(K̇/K̇<sub>0</sub>)
                </div>
                <p>Where β is material constant, K̇ is loading rate</p>
            </div>
        </div>
    </div>

    <!-- 6.6 Fatigue -->
    <div class="section" id="fatigue">
        <h2>6.6 Fatigue</h2>
        
        <div class="topic-card">
            <h4>S-N Curve</h4>
            <div class="formula">
                σ<sub>a</sub> = σ'<sub>f</sub>(2N<sub>f</sub>)<sup>b</sup>
            </div>
            <p>Where σ'<sub>f</sub> is fatigue strength coefficient, b is exponent</p>
            
            <h4>Crack Growth (Paris Law)</h4>
            <div class="formula">
                da/dN = C(ΔK)<sup>m</sup>
            </div>
            <p>Where C and m are material constants</p>
            
            <h4>Endurance Limit</h4>
            <div class="formula">
                σ<sub>e</sub> ≈ 0.5σ<sub>u</sub> (for steels)
            </div>
        </div>
    </div>

    <!-- 6.7 High Temperature Deformation -->
    <div class="section" id="creep">
        <h2>6.7 High Temperature Deformation</h2>
        
        <div class="topic-card">
            <h4>Creep Stages</h4>
            <div class="formula">
                ε = ε<sub>0</sub> + βt<sup>1/3</sup> + kt (Primary + Secondary)
            </div>
            
            <h4>Norton's Law</h4>
            <div class="formula">
                ε̇ = Aσ<sup>n</sup>exp(-Q/RT)
            </div>
            <p>Where n is stress exponent, Q is activation energy</p>
            
            <h4>Larson-Miller Parameter</h4>
            <div class="formula">
                P = T(C + log t<sub>r</sub>)
            </div>
            <p>Where C ≈ 20 for many metals</p>
        </div>
    </div>

    <!-- TestUrSelf Course Section -->
    <div class="section test-yourself" id="test-yourself">
        <h2>TestUrSelf's Course Features</h2>
        
        <div class="topic-card">
            <h3>Mechanical Metallurgy Mastery Course</h3>
            
            <h4>Course Highlights</h4>
            <ul>
                <li>600+ practice problems with detailed solutions</li>
                <li>Interactive dislocation dynamics simulations</li>
                <li>12 full-length mock tests with performance analysis</li>
                <li>Microstructure interpretation workshops</li>
                <li>Fracture surface analysis exercises</li>
            </ul>
            
            <h4>Special Modules</h4>
            <table>
                <tr>
                    <th>Module</th>
                    <th>Topics</th>
                    <th>Problems</th>
                </tr>
                <tr>
                    <td>1</td>
                    <td>Stress-Strain Analysis</td>
                    <td>120</td>
                </tr>
                <tr>
                    <td>2</td>
                    <td>Dislocation Theory</td>
                    <td>150</td>
                </tr>
                <tr>
                    <td>3</td>
                    <td>Fracture Mechanics</td>
                    <td>130</td>
                </tr>
                <tr>
                    <td>4</td>
                    <td>Fatigue & Creep</td>
                    <td>100</td>
                </tr>
                <tr>
                    <td>5</td>
                    <td>Numerical Problem Solving</td>
                    <td>100</td>
                </tr>
            </table>
        </div>
    </div>
    
    <footer>
        <p>© 2023 GATE Metallurgy Guide | TestUrSelf Educational Services</p>
    </footer>
</body>
</html>
