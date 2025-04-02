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
        }
        
        header {
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            color: white;
            padding: 3rem;
            text-align: center;
            border-radius: 8px;
            margin-bottom: 3rem;
            box-shadow: 0 4px 20px rgba(0,0,0,0.2);
        }
        
        h1 {
            margin: 0;
            font-size: 2.5rem;
            font-weight: 700;
        }
        
        h2 {
            color: var(--primary-color);
            border-left: 6px solid var(--accent-color);
            padding-left: 1rem;
            margin-top: 3rem;
            font-size: 2rem;
        }
        
        h3 {
            color: var(--dark-color);
            margin-top: 2.5rem;
            font-size: 1.6rem;
            border-bottom: 2px solid var(--accent-color);
            padding-bottom: 0.5rem;
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
            border-top: 4px solid var(--accent-color);
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
        
        .important::before {
            content: "★";
            position: absolute;
            left: 10px;
            top: 10px;
            color: var(--highlight-color);
            font-size: 1.5rem;
        }
        
        .formula {
            font-family: 'Courier New', Courier, monospace;
            background-color: #f5f5f5;
            padding: 1rem 1.5rem;
            border-radius: 6px;
            overflow-x: auto;
            margin: 1.2rem 0;
            border-left: 4px solid var(--accent-color);
            font-size: 1.1rem;
            box-shadow: inset 0 1px 3px rgba(0,0,0,0.1);
        }
        
        .key-points {
            background: linear-gradient(to right, #e8f5e9, #f1f8e9);
            padding: 1.5rem;
            border-radius: 8px;
            margin: 2rem 0;
            border-left: 6px solid var(--success-color);
        }
        
        .key-points h4 {
            color: var(--success-color);
            margin-top: 0;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 2rem 0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }
        
        table, th, td {
            border: 1px solid #e0e0e0;
        }
        
        th, td {
            padding: 1rem;
            text-align: left;
        }
        
        th {
            background: linear-gradient(to right, var(--primary-color), var(--dark-color));
            color: white;
            font-weight: 500;
        }
        
        tr:nth-child(even) {
            background-color: #f5f5f5;
        }
        
        tr:hover {
            background-color: #e3f2fd;
        }
        
        .toc {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            margin-bottom: 3rem;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .toc ul {
            list-style-type: none;
            padding: 0;
        }
        
        .toc li {
            padding: 0.8rem 0;
            border-bottom: 1px dashed #e0e0e0;
        }
        
        .toc a {
            text-decoration: none;
            color: var(--dark-color);
            display: block;
            transition: color 0.3s;
            font-weight: 500;
        }
        
        .toc a:hover {
            color: var(--secondary-color);
        }
        
        .toc-inner {
            margin-left: 1.5rem;
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
        <p>Complete Guide for GATE Metallurgy (MT) - Section 2</p>
    </header>
    
    <div class="toc">
        <h2>Detailed Table of Contents</h2>
        <ul>
            <li><a href="#laws">2.1 Laws of Thermodynamics</a>
                <div class="toc-inner">
                    <ul>
                        <li><a href="#first-law">First Law of Thermodynamics</a></li>
                        <li><a href="#second-law">Second Law of Thermodynamics</a></li>
                        <li><a href="#thermo-potentials">Thermodynamic Potentials</a></li>
                    </ul>
                </div>
            </li>
            <li><a href="#solutions">2.2 Solutions and Phase Equilibria</a>
                <div class="toc-inner">
                    <ul>
                        <li><a href="#ideal-solutions">Ideal and Regular Solutions</a></li>
                        <li><a href="#phase-diagrams">Phase Diagrams</a></li>
                        <li><a href="#thermo-diagrams">Thermodynamic Diagrams</a></li>
                    </ul>
                </div>
            </li>
            <li><a href="#defects">2.3 Defects and Interfaces</a>
                <div class="toc-inner">
                    <ul>
                        <li><a href="#point-defects">Point Defects</a></li>
                        <li><a href="#interfaces">Surfaces and Interfaces</a></li>
                    </ul>
                </div>
            </li>
            <li><a href="#electrochem">2.4 Electrochemistry</a>
                <div class="toc-inner">
                    <ul>
                        <li><a href="#electrode-pot">Electrode Potential</a></li>
                        <li><a href="#cells">Electrochemical Cells</a></li>
                        <li><a href="#nernst">Nernst Equation</a></li>
                        <li><a href="#ph-diagrams">Potential-pH Diagrams</a></li>
                    </ul>
                </div>
            </li>
        </ul>
    </div>

    <div class="section" id="laws">
        <h2>2.1 Laws of Thermodynamics</h2>
        
        <div class="subsection" id="first-law">
            <h3>First Law of Thermodynamics</h3>
            <p>The first law establishes the principle of energy conservation for thermodynamic systems:</p>
            
            <div class="formula">
                ΔU = q + w
            </div>
            
            <p>Where:</p>
            <ul>
                <li>ΔU = Change in internal energy</li>
                <li>q = Heat transferred to the system</li>
                <li>w = Work done on the system</li>
            </ul>
            
            <div class="important">
                <h4>Key Concepts</h4>
                <p><strong>Enthalpy (H):</strong> Defined for constant pressure processes:</p>
                <div class="formula">
                    H = U + PV
                </div>
                <p><strong>Heat Capacity:</strong> At constant volume (C<sub>V</sub>) and constant pressure (C<sub>P</sub>):</p>
                <div class="formula">
                    C<sub>V</sub> = (∂U/∂T)<sub>V</sub>; C<sub>P</sub> = (∂H/∂T)<sub>P</sub>
                </div>
            </div>
            
            <h4>Applications in Metallurgy</h4>
            <p>Heat effects in metallurgical processes can be calculated using:</p>
            <div class="formula">
                ΔH = ΣH<sub>products</sub> - ΣH<sub>reactants</sub>
            </div>
            <p>Kirchhoff's Law relates heat of reaction to temperature:</p>
            <div class="formula">
                (∂(ΔH)/∂T)<sub>P</sub> = ΔC<sub>P</sub>
            </div>
        </div>
        
        <div class="subsection" id="second-law">
            <h3>Second Law of Thermodynamics</h3>
            <p>The second law introduces the concept of entropy and the direction of spontaneous processes:</p>
            
            <div class="formula">
                dS ≥ δq/T (Clausius Inequality)
            </div>
            
            <p>For reversible processes, the equality holds:</p>
            <div class="formula">
                dS = δq<sub>rev</sub>/T
            </div>
            
            <div class="key-points">
                <h4>Carnot Cycle Efficiency</h4>
                <p>The maximum efficiency of a heat engine operating between two reservoirs:</p>
                <div class="formula">
                    η = 1 - T<sub>cold</sub>/T<sub>hot</sub>
                </div>
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
        
        <div class="subsection" id="thermo-potentials">
            <h3>Thermodynamic Potentials</h3>
            <p>Fundamental equations for different thermodynamic potentials:</p>
            
            <table>
                <tr>
                    <th>Potential</th>
                    <th>Definition</th>
                    <th>Differential Form</th>
                </tr>
                <tr>
                    <td>Internal Energy (U)</td>
                    <td>-</td>
                    <td>dU = TdS - PdV + Σμ<sub>i</sub>dn<sub>i</sub></td>
                </tr>
                <tr>
                    <td>Enthalpy (H)</td>
                    <td>H = U + PV</td>
                    <td>dH = TdS + VdP + Σμ<sub>i</sub>dn<sub>i</sub></td>
                </tr>
                <tr>
                    <td>Helmholtz Free Energy (A)</td>
                    <td>A = U - TS</td>
                    <td>dA = -SdT - PdV + Σμ<sub>i</sub>dn<sub>i</sub></td>
                </tr>
                <tr>
                    <td>Gibbs Free Energy (G)</td>
                    <td>G = H - TS</td>
                    <td>dG = -SdT + VdP + Σμ<sub>i</sub>dn<sub>i</sub></td>
                </tr>
            </table>
            
            <div class="important">
                <h4>Maxwell Relations</h4>
                <p>Derived from the exact differentials of thermodynamic potentials:</p>
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
            
            <h4>Chemical Potential</h4>
            <p>The chemical potential μ<sub>i</sub> is defined as:</p>
            <div class="formula">
                μ<sub>i</sub> = (∂G/∂n<sub>i</sub>)<sub>T,P,n<sub>j≠i</sub></sub>
            </div>
            <p>For a pure substance, it equals the molar Gibbs free energy:</p>
            <div class="formula">
                μ = G<sub>m</sub>
            </div>
        </div>
    </div>

    <div class="section" id="solutions">
        <h2>2.2 Solutions and Phase Equilibria</h2>
        
        <div class="subsection" id="ideal-solutions">
            <h3>Ideal and Regular Solutions</h3>
            <p>An ideal solution follows Raoult's Law for all components:</p>
            <div class="formula">
                P<sub>i</sub> = x<sub>i</sub>P<sub>i</sub><sup>0</sup>
            </div>
            <p>Where P<sub>i</sub> is the partial pressure, x<sub>i</sub> is the mole fraction, and P<sub>i</sub><sup>0</sup> is the vapor pressure of pure component i.</p>
            
            <div class="key-points">
                <h4>Excess Properties</h4>
                <p>For non-ideal solutions, excess properties are defined:</p>
                <div class="formula">
                    G<sup>E</sup> = G<sub>actual</sub> - G<sub>ideal</sub>
                </div>
                <p>Regular solutions have:</p>
                <div class="formula">
                    G<sup>E</sup> = Ωx<sub>1</sub>x<sub>2</sub>
                </div>
                <p>Where Ω is the interaction parameter.</p>
            </div>
            
            <h4>Activity</h4>
            <p>The activity a<sub>i</sub> is defined relative to a standard state:</p>
            <div class="formula">
                μ<sub>i</sub> = μ<sub>i</sub><sup>0</sup> + RTln(a<sub>i</sub>)
            </div>
            <p>Activity coefficient γ<sub>i</sub> relates activity to concentration:</p>
            <div class="formula">
                a<sub>i</sub> = γ<sub>i</sub>x<sub>i</sub>
            </div>
        </div>
        
        <div class="subsection" id="phase-diagrams">
            <h3>Phase Diagrams</h3>
            <p>The Gibbs Phase Rule determines the number of degrees of freedom (F) in a system:</p>
            <div class="formula">
                F = C - P + 2
            </div>
            <p>Where C is the number of components and P is the number of phases.</p>
            
            <div class="important">
                <h4>Lever Rule</h4>
                <p>For a two-phase (α + β) region in a binary system:</p>
                <div class="formula">
                    W<sub>α</sub>/W<sub>β</sub> = (C<sub>β</sub> - C<sub>0</sub>)/(C<sub>0</sub> - C<sub>α</sub>)
                </div>
                <p>Where W is the weight fraction and C is composition.</p>
            </div>
            
            <h4>Free Energy vs. Composition</h4>
            <p>The common tangent construction determines equilibrium phases:</p>
            <div class="formula">
                (∂G/∂x<sub>B</sub>)<sub>α</sub> = (∂G/∂x<sub>B</sub>)<sub>β</sub>
            </div>
        </div>
        
        <div class="subsection" id="thermo-diagrams">
            <h3>Thermodynamic Diagrams</h3>
            <p>The equilibrium constant K for a reaction is related to ΔG°:</p>
            <div class="formula">
                ΔG° = -RTlnK
            </div>
            
            <h4>Ellingham Diagrams</h4>
            <p>Plot of ΔG° vs T for formation of oxides, sulfides, etc. The standard form is:</p>
            <div class="formula">
                ΔG° = A + BT
            </div>
            <p>Where A and B are constants for each reaction.</p>
            
            <h4>Phase Stability Diagrams</h4>
            <p>Show stable phases as functions of thermodynamic variables (T, P, composition).</p>
        </div>
    </div>

    <div class="section" id="defects">
        <h2>2.3 Defects and Interfaces</h2>
        
        <div class="subsection" id="point-defects">
            <h3>Point Defects</h3>
            <p>The equilibrium concentration of vacancies is given by:</p>
            <div class="formula">
                n<sub>v</sub>/N = exp(-ΔG<sub>f</sub>/kT)
            </div>
            <p>Where ΔG<sub>f</sub> is the free energy of formation, k is Boltzmann's constant, and T is temperature.</p>
            
            <div class="key-points">
                <h4>Schottky Defects</h4>
                <p>In ionic crystals, the equilibrium constant is:</p>
                <div class="formula">
                    [V<sub>M</sub>][V<sub>X</sub>] = K<sub>S</sub> = exp(-ΔG<sub>S</sub>/kT)
                </div>
                <p>Where ΔG<sub>S</sub> is the Schottky formation energy.</p>
            </div>
        </div>
        
        <div class="subsection" id="interfaces">
            <h3>Surfaces and Interfaces</h3>
            <p>The surface energy γ is the excess free energy per unit area:</p>
            <div class="formula">
                γ = (∂G/∂A)<sub>T,P,n<sub>i</sub></sub>
            </div>
            
            <h4>Gibbs Adsorption Equation</h4>
            <p>For a binary system:</p>
            <div class="formula">
                dγ = -Γ<sub>2</sub>dμ<sub>2</sub>
            </div>
            <p>Where Γ<sub>2</sub> is the surface excess of component 2.</p>
        </div>
    </div>

    <div class="section" id="electrochem">
        <h2>2.4 Electrochemistry</h2>
        
        <div class="subsection" id="electrode-pot">
            <h3>Electrode Potential</h3>
            <p>The standard electrode potential E° is measured against the Standard Hydrogen Electrode (SHE).</p>
            
            <div class="important">
                <h4>Single Electrode Potential</h4>
                <p>For a general reduction reaction:</p>
                <div class="formula">
                    aA + ne<sup>-</sup> → bB
                </div>
                <p>The potential is given by the Nernst equation.</p>
            </div>
        </div>
        
        <div class="subsection" id="cells">
            <h3>Electrochemical Cells</h3>
            <p>The cell potential E<sub>cell</sub> is the difference between cathode and anode potentials:</p>
            <div class="formula">
                E<sub>cell</sub> = E<sub>cathode</sub> - E<sub>anode</sub>
            </div>
            
            <p>The relationship between cell potential and ΔG:</p>
            <div class="formula">
                ΔG = -nFE<sub>cell</sub>
            </div>
            <p>Where n is number of electrons and F is Faraday's constant.</p>
        </div>
        
        <div class="subsection" id="nernst">
            <h3>Nernst Equation</h3>
            <p>For the reaction aA + bB → cC + dD:</p>
            <div class="formula">
                E = E° - (RT/nF)ln(Q) = E° - (0.0591/n)log(Q) at 298K
            </div>
            <p>Where Q is the reaction quotient:</p>
            <div class="formula">
                Q = (a<sub>C</sub><sup>c</sup>a<sub>D</sub><sup>d</sup>)/(a<sub>A</sub><sup>a</sup>a<sub>B</sub><sup>b</sup>)
            </div>
        </div>
        
        <div class="subsection" id="ph-diagrams">
            <h3>Potential-pH Diagrams (Pourbaix Diagrams)</h3>
            <p>Show stable phases as functions of potential (E) and pH.</p>
            
            <div class="key-points">
                <h4>Key Lines</h4>
                <p><strong>Hydrogen line:</strong> 2H<sup>+</sup> + 2e<sup>-</sup> → H<sub>2</sub></p>
                <div class="formula">
                    E = -0.0591pH
                </div>
                <p><strong>Oxygen line:</strong> O<sub>2</sub> + 4H<sup>+</sup> + 4e<sup>-</sup> → 2H<sub>2</sub>O</p>
                <div class="formula">
                    E = 1.23 - 0.0591pH
                </div>
            </div>
        </div>
    </div>
    
    <footer>
        <p>© 2023 GATE Metallurgy Thermodynamics Guide | All Rights Reserved</p>
        <p>Complete coverage of Section 2 with detailed formulas and concepts</p>
    </footer>
</body>
</html>
