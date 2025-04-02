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
        
        tr:nth-child(even) {
            background-color: #f9f9f9;
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
        
        .example {
            background-color: #f0f7ff;
            border-left: 4px solid var(--accent-color);
            padding: 1.5rem;
            margin: 1.5rem 0;
            border-radius: 0 8px 8px 0;
        }
        
        .definition {
            background-color: #f9f9f9;
            border-left: 4px solid #9e9e9e;
            padding: 1.5rem;
            margin: 1.5rem 0;
            border-radius: 0 8px 8px 0;
            font-style: italic;
        }
    </style>
</head>
<body>
    <header>
        <h1>Metallurgical Thermodynamics</h1>
        <p>Complete Guide for GATE Metallurgy (MT) - Section 2 (TestUrSelf)</p>
    </header>

    <div class="toc">
        <h2>Table of Contents</h2>
        <ol>
            <li><a href="#laws">Laws of Thermodynamics</a></li>
            <li><a href="#solutions">Solutions and Phase Equilibria</a></li>
            <li><a href="#defects">Defects and Interfaces</a></li>
            <li><a href="#electrochem">Electrochemistry</a></li>
        </ol>
    </div>

    <div class="section" id="laws">
        <h2>2.1 Laws of Thermodynamics</h2>
        
        <div class="subsection" id="first-law">
            <h3>First Law of Thermodynamics</h3>
            <div class="topic-card">
                <h4>Energy Conservation</h4>
                <div class="definition">
                    The first law states that energy cannot be created or destroyed, only converted from one form to another.
                </div>
                <div class="formula">
                    ΔU = q + w
                </div>
                <p>Where:</p>
                <ul>
                    <li>ΔU = change in internal energy of the system</li>
                    <li>q = heat transferred to the system</li>
                    <li>w = work done on the system</li>
                </ul>
                
                <h4>Enthalpy</h4>
                <div class="formula">
                    H = U + PV
                </div>
                <div class="formula">
                    ΔH = ΔU + PΔV (at constant pressure)
                </div>
                
                <h4>Heat Capacity</h4>
                <table>
                    <tr>
                        <th>Type</th>
                        <th>Definition</th>
                        <th>Relation</th>
                    </tr>
                    <tr>
                        <td>Constant Volume (C<sub>V</sub>)</td>
                        <td>(∂U/∂T)<sub>V</sub></td>
                        <td>C<sub>V</sub> = (∂q/∂T)<sub>V</sub></td>
                    </tr>
                    <tr>
                        <td>Constant Pressure (C<sub>P</sub>)</td>
                        <td>(∂H/∂T)<sub>P</sub></td>
                        <td>C<sub>P</sub> = (∂q/∂T)<sub>P</sub></td>
                    </tr>
                </table>
                
                <div class="important">
                    <h4>Applications to Metallurgical Systems</h4>
                    <p>Heat effects in metallurgical processes:</p>
                    <div class="formula">
                        ΔH = ΣH<sub>products</sub> - ΣH<sub>reactants</sub>
                    </div>
                    <p>Kirchhoff's Law for temperature dependence:</p>
                    <div class="formula">
                        (∂(ΔH)/∂T)<sub>P</sub> = ΔC<sub>P</sub>
                    </div>
                    <div class="formula">
                        ΔH(T<sub>2</sub>) = ΔH(T<sub>1</sub>) + ∫ΔC<sub>P</sub>dT
                    </div>
                    
                    <div class="example">
                        <h5>Example: Heat of Formation</h5>
                        <p>For the reaction: Fe + ½O<sub>2</sub> → FeO</p>
                        <p>ΔH<sub>298</sub> = -267 kJ/mol</p>
                        <p>Calculate ΔH at 500K given ΔC<sub>P</sub> = 10 J/mol·K</p>
                        <p>Solution: ΔH<sub>500</sub> = -267,000 + 10×(500-298) = -265 kJ/mol</p>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="second-law">
            <h3>Second Law of Thermodynamics</h3>
            <div class="topic-card">
                <h4>Entropy</h4>
                <div class="definition">
                    The second law introduces the concept of entropy as a measure of disorder and establishes the direction of spontaneous processes.
                </div>
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
                <table>
                    <tr>
                        <th>Process</th>
                        <th>Entropy Change</th>
                    </tr>
                    <tr>
                        <td>Isothermal expansion</td>
                        <td>ΔS = nRln(V<sub>2</sub>/V<sub>1</sub>)</td>
                    </tr>
                    <tr>
                        <td>Isochoric heating</td>
                        <td>ΔS = nC<sub>V</sub>ln(T<sub>2</sub>/T<sub>1</sub>)</td>
                    </tr>
                    <tr>
                        <td>Isobaric heating</td>
                        <td>ΔS = nC<sub>P</sub>ln(T<sub>2</sub>/T<sub>1</sub>)</td>
                    </tr>
                    <tr>
                        <td>Phase transition</td>
                        <td>ΔS = ΔH<sub>transition</sub>/T<sub>transition</sub></td>
                    </tr>
                </table>
                
                <div class="key-points">
                    <h4>Key Points</h4>
                    <ul>
                        <li>Entropy always increases for irreversible processes</li>
                        <li>The universe tends toward maximum entropy</li>
                        <li>Entropy is a state function</li>
                    </ul>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="thermo-potentials">
            <h3>Thermodynamic Potentials</h3>
            <div class="topic-card">
                <h4>Gibbs and Helmholtz Free Energy</h4>
                <table>
                    <tr>
                        <th>Potential</th>
                        <th>Definition</th>
                        <th>Natural Variables</th>
                    </tr>
                    <tr>
                        <td>Gibbs Free Energy (G)</td>
                        <td>G = H - TS</td>
                        <td>T, P, n</td>
                    </tr>
                    <tr>
                        <td>Helmholtz Free Energy (A)</td>
                        <td>A = U - TS</td>
                        <td>T, V, n</td>
                    </tr>
                </table>
                
                <h4>Chemical Potential</h4>
                <div class="formula">
                    μ<sub>i</sub> = (∂G/∂n<sub>i</sub>)<sub>T,P,n<sub>j≠i</sub></sub>
                </div>
                <p>For a pure substance: μ = G<sub>m</sub> (molar Gibbs free energy)</p>
                
                <div class="important">
                    <h4>Maxwell's Relations</h4>
                    <table>
                        <tr>
                            <th>Relation</th>
                            <th>Derived From</th>
                        </tr>
                        <tr>
                            <td>(∂T/∂V)<sub>S</sub> = -(∂P/∂S)<sub>V</sub></td>
                            <td>dU = TdS - PdV</td>
                        </tr>
                        <tr>
                            <td>(∂T/∂P)<sub>S</sub> = (∂V/∂S)<sub>P</sub></td>
                            <td>dH = TdS + VdP</td>
                        </tr>
                        <tr>
                            <td>(∂S/∂V)<sub>T</sub> = (∂P/∂T)<sub>V</sub></td>
                            <td>dA = -SdT - PdV</td>
                        </tr>
                        <tr>
                            <td>(∂S/∂P)<sub>T</sub> = -(∂V/∂T)<sub>P</sub></td>
                            <td>dG = -SdT + VdP</td>
                        </tr>
                    </table>
                    
                    <div class="example">
                        <h5>Example Application</h5>
                        <p>Using (∂S/∂P)<sub>T</sub> = -(∂V/∂T)<sub>P</sub> to find entropy change with pressure:</p>
                        <p>For an ideal gas: (∂V/∂T)<sub>P</sub> = nR/P</p>
                        <p>Thus: (∂S/∂P)<sub>T</sub> = -nR/P</p>
                        <p>ΔS = -nRln(P<sub>2</sub>/P<sub>1</sub>) for isothermal pressure change</p>
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
                <p>Where P<sub>i</sub><sup>0</sup> is the vapor pressure of pure component i</p>
                
                <h4>Activity and Activity Coefficient</h4>
                <div class="formula">
                    μ<sub>i</sub> = μ<sub>i</sub><sup>0</sup> + RTln(a<sub>i</sub>)
                </div>
                <div class="formula">
                    a<sub>i</sub> = γ<sub>i</sub>x<sub>i</sub>
                </div>
                <p>Where γ<sub>i</sub> is the activity coefficient (γ<sub>i</sub> = 1 for ideal solutions)</p>
                
                <h4>Excess Properties</h4>
                <table>
                    <tr>
                        <th>Solution Type</th>
                        <th>G<sup>E</sup></th>
                        <th>Behavior</th>
                    </tr>
                    <tr>
                        <td>Ideal</td>
                        <td>0</td>
                        <td>ΔH<sub>mix</sub> = 0, ΔV<sub>mix</sub> = 0</td>
                    </tr>
                    <tr>
                        <td>Regular</td>
                        <td>Ωx<sub>1</sub>x<sub>2</sub></td>
                        <td>ΔH<sub>mix</sub> ≠ 0, ΔS<sub>mix</sub> = ideal</td>
                    </tr>
                    <tr>
                        <td>Athermal</td>
                        <td>-TΔS<sup>E</sup></td>
                        <td>ΔH<sub>mix</sub> = 0, ΔS<sub>mix</sub> ≠ ideal</td>
                    </tr>
                </table>
                
                <div class="important">
                    <h4>Henry's Law</h4>
                    <div class="formula">
                        P<sub>i</sub> = K<sub>H</sub>x<sub>i</sub> (for dilute solutions)
                    </div>
                    <p>Where K<sub>H</sub> is Henry's constant</p>
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
                <p>Where:</p>
                <ul>
                    <li>F = degrees of freedom</li>
                    <li>C = number of components</li>
                    <li>P = number of phases</li>
                </ul>
                
                <h4>Lever Rule</h4>
                <div class="formula">
                    W<sub>α</sub>/W<sub>β</sub> = (C<sub>β</sub> - C<sub>0</sub>)/(C<sub>0</sub> - C<sub>α</sub>)
                </div>
                <p>Where W<sub>α</sub> and W<sub>β</sub> are weight fractions of phases α and β</p>
                
                <h4>Common Binary Phase Diagrams</h4>
                <table>
                    <tr>
                        <th>Type</th>
                        <th>Features</th>
                        <th>Example System</th>
                    </tr>
                    <tr>
                        <td>Isomorphous</td>
                        <td>Complete solid solubility</td>
                        <td>Cu-Ni</td>
                    </tr>
                    <tr>
                        <td>Eutectic</td>
                        <td>Eutectic point, limited solubility</td>
                        <td>Pb-Sn</td>
                    </tr>
                    <tr>
                        <td>Peritectic</td>
                        <td>Peritectic reaction: L + α → β</td>
                        <td>Fe-C (δ-ferrite region)</td>
                    </tr>
                    <tr>
                        <td>Monotectic</td>
                        <td>Liquid immiscibility gap</td>
                        <td>Cu-Pb</td>
                    </tr>
                </table>
                
                <h4>Free Energy vs Composition</h4>
                <div class="formula">
                    (∂G/∂x<sub>B</sub>)<sub>α</sub> = (∂G/∂x<sub>B</sub>)<sub>β</sub> (common tangent rule)
                </div>
                <div class="formula">
                    G<sub>mix</sub> = RT(x<sub>A</sub>lnx<sub>A</sub> + x<sub>B</sub>lnx<sub>B</sub>) (ideal solution)
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
                <div class="formula">
                    K = exp(-ΔG°/RT)
                </div>
                
                <h4>Ellingham Diagrams</h4>
                <div class="formula">
                    ΔG° = A + BT
                </div>
                <p>Key features:</p>
                <ul>
                    <li>Slope = -ΔS°</li>
                    <li>Y-intercept = ΔH°</li>
                    <li>Phase change points show slope changes</li>
                </ul>
                
                <table>
                    <tr>
                        <th>Reaction</th>
                        <th>ΔG° (J/mol) Equation</th>
                    </tr>
                    <tr>
                        <td>4/3Al + O<sub>2</sub> → 2/3Al<sub>2</sub>O<sub>3</sub></td>
                        <td>-1,120,000 + 214T</td>
                    </tr>
                    <tr>
                        <td>2C + O<sub>2</sub> → 2CO</td>
                        <td>-223,000 - 175T</td>
                    </tr>
                    <tr>
                        <td>2Fe + O<sub>2</sub> → 2FeO</td>
                        <td>-529,000 + 125T</td>
                    </tr>
                </table>
                
                <h4>Phase Stability Diagrams</h4>
                <p>Showing stable phases as functions of thermodynamic variables (T, P, composition)</p>
                <div class="example">
                    <h5>Example: Fe-O System</h5>
                    <p>Stable phases at different oxygen partial pressures and temperatures:</p>
                    <ul>
                        <li>Low pO<sub>2</sub>: Metallic Fe</li>
                        <li>Intermediate pO<sub>2</sub>: FeO (wüstite)</li>
                        <li>High pO<sub>2</sub>: Fe<sub>2</sub>O<sub>3</sub> (hematite)</li>
                    </ul>
                </div>
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
                <p>Where:</p>
                <ul>
                    <li>n<sub>v</sub> = number of vacancies</li>
                    <li>N = number of lattice sites</li>
                    <li>ΔG<sub>f</sub> = Gibbs free energy of formation</li>
                </ul>
                
                <h4>Schottky Defects</h4>
                <div class="formula">
                    [V<sub>M</sub>][V<sub>X</sub>] = K<sub>S</sub> = exp(-ΔG<sub>S</sub>/kT)
                </div>
                <p>For NaCl: [V<sub>Na</sub>] = [V<sub>Cl</sub>] = exp(-ΔG<sub>S</sub>/2kT)</p>
                
                <h4>Frenkel Defects</h4>
                <div class="formula">
                    [V<sub>M</sub>][M<sub>i</sub>] = K<sub>F</sub> = exp(-ΔG<sub>F</sub>/kT)
                </div>
                <p>Where M<sub>i</sub> is interstitial metal ion</p>
                
                <table>
                    <tr>
                        <th>Defect Type</th>
                        <th>Example Materials</th>
                        <th>Formation Energy (eV)</th>
                    </tr>
                    <tr>
                        <td>Vacancy</td>
                        <td>Metals (Cu, Fe)</td>
                        <td>0.5-2.0</td>
                    </tr>
                    <tr>
                        <td>Schottky</td>
                        <td>NaCl, MgO</td>
                        <td>2.0-4.0</td>
                    </tr>
                    <tr>
                        <td>Frenkel</td>
                        <td>AgCl, ZrO<sub>2</sub></td>
                        <td>1.5-3.0</td>
                    </tr>
                </table>
            </div>
        </div>
        
        <div class="subsection" id="interfaces">
            <h3>Surfaces and Interfaces</h3>
            <div class="topic-card">
                <h4>Surface Energy</h4>
                <div class="formula">
                    γ = (∂G/∂A)<sub>T,P,n<sub>i</sub></sub>
                </div>
                <p>Typical values:</p>
                <ul>
                    <li>Metals: 1-3 J/m<sup>2</sup></li>
                    <li>Oxides: 0.5-1.5 J/m<sup>2</sup></li>
                    <li>Water: 0.072 J/m<sup>2</sup> at 20°C</li>
                </ul>
                
                <h4>Gibbs Adsorption Equation</h4>
                <div class="formula">
                    dγ = -ΣΓ<sub>i</sub>dμ<sub>i</sub>
                </div>
                <p>For binary systems:</p>
                <div class="formula">
                    Γ<sub>2</sub> = -(∂γ/∂μ<sub>2</sub>)<sub>T</sub>
                </div>
                
                <h4>Segregation Phenomena</h4>
                <div class="formula">
                    X<sub>i</sub><sup>surface</sup>/X<sub>i</sub><sup>bulk</sup> = exp(-ΔG<sub>seg</sub>/RT)
                </div>
                <p>Where ΔG<sub>seg</sub> is segregation free energy</p>
                
                <table>
                    <tr>
                        <th>Interface Type</th>
                        <th>Energy (J/m<sup>2</sup>)</th>
                        <th>Characteristics</th>
                    </tr>
                    <tr>
                        <td>Grain boundary</td>
                        <td>0.5-1.0</td>
                        <td>Depends on misorientation angle</td>
                    </tr>
                    <tr>
                        <td>Phase boundary</td>
                        <td>0.2-0.8</td>
                        <td>Depends on lattice mismatch</td>
                    </tr>
                    <tr>
                        <td>Solid-liquid</td>
                        <td>0.1-0.5</td>
                        <td>Important in wetting phenomena</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>

    <div class="section" id="electrochem">
        <h2>2.4 Electrochemistry</h2>
        
        <div class="subsection" id="electrode-pot">
            <h3>Single Electrode Potential</h3>
            <div class="topic-card">
                <p>Standard electrode potential measured against SHE (Standard Hydrogen Electrode)</p>
                <table>
                    <tr>
                        <th>Electrode Reaction</th>
                        <th>E° (V vs SHE)</th>
                    </tr>
                    <tr>
                        <td>Li<sup>+</sup> + e<sup>-</sup> → Li</td>
                        <td>-3.04</td>
                    </tr>
                    <tr>
                        <td>Al<sup>3+</sup> + 3e<sup>-</sup> → Al</td>
                        <td>-1.66</td>
                    </tr>
                    <tr>
                        <td>Fe<sup>2+</sup> + 2e<sup>-</sup> → Fe</td>
                        <td>-0.44</td>
                    </tr>
                    <tr>
                        <td>Cu<sup>2+</sup> + 2e<sup>-</sup> → Cu</td>
                        <td>+0.34</td>
                    </tr>
                    <tr>
                        <td>Ag<sup>+</sup> + e<sup>-</sup> → Ag</td>
                        <td>+0.80</td>
                    </tr>
                </table>
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
                <p>Where:</p>
                <ul>
                    <li>n = number of electrons transferred</li>
                    <li>F = Faraday's constant (96,485 C/mol)</li>
                </ul>
                
                <table>
                    <tr>
                        <th>Cell Type</th>
                        <th>Example</th>
                        <th>E° (V)</th>
                    </tr>
                    <tr>
                        <td>Galvanic</td>
                        <td>Zn|Zn<sup>2+</sup>||Cu<sup>2+</sup>|Cu</td>
                        <td>+1.10</td>
                    </tr>
                    <tr>
                        <td>Concentration</td>
                        <td>Cu|Cu<sup>2+</sup>(0.1M)||Cu<sup>2+</sup>(1M)|Cu</td>
                        <td>≈0.03</td>
                    </tr>
                </table>
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
                
                <div class="example">
                    <h5>Example: Zn/Zn<sup>2+</sup> Electrode</h5>
                    <p>For Zn<sup>2+</sup> + 2e<sup>-</sup> → Zn, E° = -0.76V</p>
                    <p>At [Zn<sup>2+</sup>] = 0.01M:</p>
                    <p>E = -0.76 - (0.0591/2)log(1/0.01) = -0.76 - 0.0591 = -0.82V</p>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="ph-diagrams">
            <h3>Potential-pH Diagrams</h3>
            <div class="topic-card">
                <h4>Pourbaix Diagrams</h4>
                <p>Showing stable phases as functions of potential (E) and pH</p>
                
                <div class="key-points">
                    <h4>Key Lines</h4>
                    <p>Hydrogen evolution reaction (HER):</p>
                    <div class="formula">
                        2H<sup>+</sup> + 2e<sup>-</sup> → H<sub>2</sub>; E = -0.0591pH
                    </div>
                    <p>Oxygen evolution reaction (OER):</p>
                    <div class="formula">
                        O<sub>2</sub> + 4H<sup>+</sup> + 4e<sup>-</sup> → 2H<sub>2</sub>O; E = 1.23 - 0.0591pH
                    </div>
                </div>
                
                <table>
                    <tr>
                        <th>Region</th>
                        <th>Fe Species</th>
                        <th>Condition</th>
                    </tr>
                    <tr>
                        <td>Immunity</td>
                        <td>Fe</td>
                        <td>Low potential</td>
                    </tr>
                    <tr>
                        <td>Corrosion</td>
                        <td>Fe<sup>2+</sup>, Fe<sup>3+</sup></td>
                        <td>Intermediate potential, acidic pH</td>
                    </tr>
                    <tr>
                        <td>Passivation</td>
                        <td>Fe<sub>2</sub>O<sub>3</sub>, Fe<sub>3</sub>O<sub>4</sub></td>
                        <td>High potential, neutral/alkaline pH</td>
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
