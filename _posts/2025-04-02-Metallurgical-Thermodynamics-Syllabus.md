<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GATE MT - Metallurgical Thermodynamics</title>
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
        
        /* Large Diagonal Watermark */
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
        }
        
        .subsection {
            margin-left: 1.5rem;
            border-left: 3px solid #e0e0e0;
            padding-left: 2rem;
            margin-top: 2rem;
        }
        
        .topic-card {
            background-color: var(--light-color);
            border-radius: 8px;
            padding: 1.8rem;
            margin: 1.8rem 0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
        }
        
        .important {
            background: linear-gradient(to right, #fff8e1, #fffde7);
            border-left: 6px solid var(--highlight-color);
            padding: 1.5rem;
            margin: 2rem 0;
            border-radius: 0 8px 8px 0;
            position: relative;
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
        
        .key-points {
            background: linear-gradient(to right, #e8f5e9, #f1f8e9);
            padding: 1.5rem;
            border-radius: 8px;
            margin: 2rem 0;
            border-left: 6px solid var(--success-color);
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 2rem 0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }
        
        th, td {
            padding: 1rem;
            text-align: left;
            border-bottom: 1px solid #e0e0e0;
        }
        
        th {
            background-color: var(--primary-color);
            color: white;
        }
        
        .toc {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            margin-bottom: 3rem;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        footer {
            text-align: center;
            margin-top: 3rem;
            padding: 2rem;
            color: var(--primary-color);
        }
    </style>
</head>
<body>
    <header>
        <h1>Metallurgical Thermodynamics</h1>
        <p>Complete Guide for GATE Metallurgy (MT) - Section 2 (TestUrSelf)</p>
    </header>

    <div class="section" id="laws">
        <h2>2.1 Laws of Thermodynamics</h2>
        
        <div class="subsection" id="first-law">
            <h3>First Law of Thermodynamics</h3>
            <div class="topic-card">
                <h4>Energy Conservation</h4>
                <p>The first law establishes the principle of energy conservation for thermodynamic systems:</p>
                <div class="formula">
                    ΔU = q + w
                </div>
                <p>Where ΔU is change in internal energy, q is heat transferred to the system, and w is work done on the system.</p>
                
                <h4>Enthalpy</h4>
                <p>Defined for constant pressure processes:</p>
                <div class="formula">
                    H = U + PV
                </div>
                
                <h4>Heat Capacity</h4>
                <p>At constant volume and pressure:</p>
                <div class="formula">
                    C<sub>V</sub> = (∂U/∂T)<sub>V</sub>; C<sub>P</sub> = (∂H/∂T)<sub>P</sub>
                </div>
                
                <div class="important">
                    <h4>Applications to Metallurgical Systems</h4>
                    <p>Heat effects in metallurgical processes:</p>
                    <div class="formula">
                        ΔH = ΣH<sub>products</sub> - ΣH<sub>reactants</sub>
                    </div>
                    <p>Kirchhoff's Law:</p>
                    <div class="formula">
                        (∂(ΔH)/∂T)<sub>P</sub> = ΔC<sub>P</sub>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="second-law">
            <h3>Second Law of Thermodynamics</h3>
            <div class="topic-card">
                <h4>Entropy</h4>
                <p>The second law introduces entropy and the direction of spontaneous processes:</p>
                <div class="formula">
                    dS ≥ δq/T (Clausius Inequality)
                </div>
                <p>For reversible processes:</p>
                <div class="formula">
                    dS = δq<sub>rev</sub>/T
                </div>
                
                <h4>Carnot Cycle Efficiency</h4>
                <div class="formula">
                    η = 1 - T<sub>cold</sub>/T<sub>hot</sub>
                </div>
                
                <h4>Entropy Changes</h4>
                <p>For ideal gases:</p>
                <div class="formula">
                    ΔS = nC<sub>V</sub>ln(T<sub>2</sub>/T<sub>1</sub>) + nRln(V<sub>2</sub>/V<sub>1</sub>)
                </div>
                <div class="formula">
                    ΔS = nC<sub>P</sub>ln(T<sub>2</sub>/T<sub>1</sub>) - nRln(P<sub>2</sub>/P<sub>1</sub>)
                </div>
            </div>
        </div>
        
        <div class="subsection" id="thermo-potentials">
            <h3>Thermodynamic Potentials</h3>
            <div class="topic-card">
                <h4>Gibbs and Helmholtz Free Energy</h4>
                <div class="formula">
                    G = H - TS; A = U - TS
                </div>
                
                <h4>Chemical Potential</h4>
                <div class="formula">
                    μ<sub>i</sub> = (∂G/∂n<sub>i</sub>)<sub>T,P,n<sub>j≠i</sub></sub>
                </div>
                
                <div class="important">
                    <h4>Maxwell's Relations</h4>
                    <div class="formula">
                        (∂T/∂V)<sub>S</sub> = -(∂P/∂S)<sub>V</sub>
                    </div>
                    <div class="formula">
                        (∂T/∂P)<sub>S</sub> = (∂V/∂S)<sub>P</sub>
                    </div>
                    <div class="formula">
                        (∂S/∂V)<sub>T</sub> = (∂P/∂T)<sub>V</sub>
                    </div>
                    <div class="formula">
                        (∂S/∂P)<sub>T</sub> = -(∂V/∂T)<sub>P</sub>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="solutions">
        <h2>2.2 Solutions and Phase Equilibria</h2>
        
        <div class="subsection" id="ideal-solutions">
            <h3>Ideal and Regular Solutions</h3>
            <div class="topic-card">
                <h4>Raoult's Law</h4>
                <div class="formula">
                    P<sub>i</sub> = x<sub>i</sub>P<sub>i</sub><sup>0</sup>
                </div>
                
                <h4>Activity</h4>
                <div class="formula">
                    μ<sub>i</sub> = μ<sub>i</sub><sup>0</sup> + RTln(a<sub>i</sub>)
                </div>
                <div class="formula">
                    a<sub>i</sub> = γ<sub>i</sub>x<sub>i</sub>
                </div>
                
                <h4>Excess Properties</h4>
                <div class="formula">
                    G<sup>E</sup> = G<sub>actual</sub> - G<sub>ideal</sub>
                </div>
                <p>For regular solutions:</p>
                <div class="formula">
                    G<sup>E</sup> = Ωx<sub>1</sub>x<sub>2</sub>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="phase-diagrams">
            <h3>Phase Diagrams</h3>
            <div class="topic-card">
                <h4>Gibbs Phase Rule</h4>
                <div class="formula">
                    F = C - P + 2
                </div>
                
                <h4>Lever Rule</h4>
                <div class="formula">
                    W<sub>α</sub>/W<sub>β</sub> = (C<sub>β</sub> - C<sub>0</sub>)/(C<sub>0</sub> - C<sub>α</sub>)
                </div>
                
                <h4>Free Energy vs Composition</h4>
                <div class="formula">
                    (∂G/∂x<sub>B</sub>)<sub>α</sub> = (∂G/∂x<sub>B</sub>)<sub>β</sub>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="thermo-diagrams">
            <h3>Thermodynamic Diagrams</h3>
            <div class="topic-card">
                <h4>Equilibrium Constant</h4>
                <div class="formula">
                    ΔG° = -RTlnK
                </div>
                
                <h4>Ellingham Diagrams</h4>
                <div class="formula">
                    ΔG° = A + BT
                </div>
                
                <h4>Phase Stability Diagrams</h4>
                <p>Showing stable phases as functions of thermodynamic variables.</p>
            </div>
        </div>
    </div>

    <div class="section" id="defects">
        <h2>2.3 Defects and Interfaces</h2>
        
        <div class="subsection" id="point-defects">
            <h3>Point Defects</h3>
            <div class="topic-card">
                <h4>Vacancies</h4>
                <div class="formula">
                    n<sub>v</sub>/N = exp(-ΔG<sub>f</sub>/kT)
                </div>
                
                <h4>Schottky Defects</h4>
                <div class="formula">
                    [V<sub>M</sub>][V<sub>X</sub>] = K<sub>S</sub> = exp(-ΔG<sub>S</sub>/kT)
                </div>
            </div>
        </div>
        
        <div class="subsection" id="interfaces">
            <h3>Surfaces and Interfaces</h3>
            <div class="topic-card">
                <h4>Surface Energy</h4>
                <div class="formula">
                    γ = (∂G/∂A)<sub>T,P,n<sub>i</sub></sub>
                </div>
                
                <h4>Gibbs Adsorption Equation</h4>
                <div class="formula">
                    dγ = -Γ<sub>2</sub>dμ<sub>2</sub>
                </div>
                
                <h4>Segregation Phenomena</h4>
                <p>Thermodynamics of adsorption and segregation at surfaces and interfaces.</p>
            </div>
        </div>
    </div>

    <div class="section" id="electrochem">
        <h2>2.4 Electrochemistry</h2>
        
        <div class="subsection" id="electrode-pot">
            <h3>Single Electrode Potential</h3>
            <div class="topic-card">
                <p>Standard electrode potential measured against SHE (Standard Hydrogen Electrode).</p>
            </div>
        </div>
        
        <div class="subsection" id="cells">
            <h3>Electrochemical Cells</h3>
            <div class="topic-card">
                <div class="formula">
                    E<sub>cell</sub> = E<sub>cathode</sub> - E<sub>anode</sub>
                </div>
                <div class="formula">
                    ΔG = -nFE<sub>cell</sub>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="nernst">
            <h3>Nernst Equation</h3>
            <div class="topic-card">
                <div class="formula">
                    E = E° - (RT/nF)ln(Q)
                </div>
                <p>At 298K:</p>
                <div class="formula">
                    E = E° - (0.0591/n)log(Q)
                </div>
            </div>
        </div>
        
        <div class="subsection" id="ph-diagrams">
            <h3>Potential-pH Diagrams</h3>
            <div class="topic-card">
                <h4>Pourbaix Diagrams</h4>
                <p>Showing stable phases as functions of potential (E) and pH.</p>
                
                <div class="key-points">
                    <h4>Key Lines</h4>
                    <p>Hydrogen line:</p>
                    <div class="formula">
                        2H<sup>+</sup> + 2e<sup>-</sup> → H<sub>2</sub>; E = -0.0591pH
                    </div>
                    <p>Oxygen line:</p>
                    <div class="formula">
                        O<sub>2</sub> + 4H<sup>+</sup> + 4e<sup>-</sup> → 2H<sub>2</sub>O; E = 1.23 - 0.0591pH
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <footer>
        <p>© TestUrSelf | All Rights Reserved</p>
    </footer>
</body>
</html>
