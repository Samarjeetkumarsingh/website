<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GATE Metallurgy (MT) - Complete Study Guide</title>
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #e74c3c;
            --accent-color: #3498db;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
            --text-color: #333;
            --highlight-color: #f1c40f;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f9f9f9;
        }
        
        header {
            background-color: var(--primary-color);
            color: white;
            padding: 2rem;
            text-align: center;
            border-radius: 8px;
            margin-bottom: 2rem;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        h1 {
            margin: 0;
            font-size: 2.5rem;
        }
        
        h2 {
            color: var(--secondary-color);
            border-bottom: 2px solid var(--accent-color);
            padding-bottom: 0.5rem;
            margin-top: 2rem;
        }
        
        h3 {
            color: var(--primary-color);
            margin-top: 1.5rem;
        }
        
        .section {
            background-color: white;
            border-radius: 8px;
            padding: 1.5rem;
            margin-bottom: 2rem;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        
        .topic-card {
            background-color: var(--light-color);
            border-left: 4px solid var(--accent-color);
            padding: 1rem;
            margin: 1rem 0;
            border-radius: 0 4px 4px 0;
        }
        
        .important {
            background-color: #fffde7;
            border-left: 4px solid var(--highlight-color);
            padding: 1rem;
            margin: 1rem 0;
            border-radius: 0 4px 4px 0;
        }
        
        .formula {
            font-family: 'Courier New', Courier, monospace;
            background-color: #f5f5f5;
            padding: 0.5rem 1rem;
            border-radius: 4px;
            overflow-x: auto;
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
        
        .key-points {
            background-color: #e8f5e9;
            padding: 1rem;
            border-radius: 8px;
            margin: 1rem 0;
        }
        
        .key-points h4 {
            margin-top: 0;
            color: #2e7d32;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 1.5rem 0;
        }
        
        table, th, td {
            border: 1px solid #ddd;
        }
        
        th, td {
            padding: 0.75rem;
            text-align: left;
        }
        
        th {
            background-color: var(--primary-color);
            color: white;
        }
        
        tr:nth-child(even) {
            background-color: #f2f2f2;
        }
        
        .toc {
            background-color: white;
            padding: 1.5rem;
            border-radius: 8px;
            margin-bottom: 2rem;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        
        .toc ul {
            list-style-type: none;
            padding: 0;
        }
        
        .toc li {
            padding: 0.5rem 0;
            border-bottom: 1px solid #eee;
        }
        
        .toc a {
            text-decoration: none;
            color: var(--primary-color);
            display: block;
            transition: color 0.3s;
        }
        
        .toc a:hover {
            color: var(--secondary-color);
        }
        
        footer {
            text-align: center;
            margin-top: 3rem;
            padding: 1.5rem;
            color: var(--primary-color);
            border-top: 1px solid #eee;
        }
        
        @media (max-width: 768px) {
            body {
                padding: 10px;
            }
            
            h1 {
                font-size: 1.8rem;
            }
            
            .section {
                padding: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>GATE Metallurgy (MT) Comprehensive Study Guide</h1>
        <p>Master the complete syllabus with detailed explanations, formulas, diagrams, and practice questions</p>
    </header>
    
    <div class="toc">
        <h2>Table of Contents</h2>
        <ul>
            <li><a href="#section1">Section 1: Engineering Mathematics</a></li>
            <li><a href="#section2">Section 2: Metallurgical Thermodynamics</a></li>
            <li><a href="#section3">Section 3: Transport Phenomena and Rate Processes</a></li>
            <li><a href="#section4">Section 4: Mineral Processing and Extractive Metallurgy</a></li>
            <li><a href="#section5">Section 5: Physical Metallurgy</a></li>
            <li><a href="#section6">Section 6: Mechanical Metallurgy</a></li>
            <li><a href="#section7">Section 7: Manufacturing Processes</a></li>
        </ul>
    </div>
    
    <div class="section" id="section1">
        <h2>Section 1: Engineering Mathematics</h2>
        
        <div class="topic-card">
            <h3>Linear Algebra</h3>
            <p><strong>Matrices and Determinants:</strong> Properties of matrices, special matrices (symmetric, skew-symmetric, orthogonal, etc.), determinant properties, adjoint and inverse of matrices.</p>
            
            <div class="formula">
                For a 2×2 matrix A = [a b; c d], det(A) = ad - bc
            </div>
            
            <p><strong>Systems of linear equations:</strong> Solution methods (Gaussian elimination, matrix inversion), consistency of systems, rank of a matrix.</p>
            
            <p><strong>Eigen values and Eigen vectors:</strong> Characteristic equation, properties, diagonalization, Cayley-Hamilton theorem.</p>
            
            <div class="important">
                <h4>Key Concept</h4>
                <p>Eigenvalues (λ) satisfy |A - λI| = 0, and eigenvectors (v) satisfy (A - λI)v = 0</p>
            </div>
        </div>
        
        <div class="topic-card">
            <h3>Calculus</h3>
            <p><strong>Limit, Continuity and Differentiability:</strong> ε-δ definition, L'Hôpital's rule, partial derivatives, chain rule.</p>
            
            <p><strong>Maxima and minima:</strong> Critical points, second derivative test, Lagrange multipliers.</p>
            
            <p><strong>Sequences and series:</strong> Convergence tests (ratio, root, comparison, integral), Taylor and Maclaurin series.</p>
            
            <div class="formula">
                Taylor series: f(x) = f(a) + f'(a)(x-a) + f''(a)(x-a)²/2! + ...
            </div>
        </div>
        
        <div class="topic-card">
            <h3>Vector Calculus</h3>
            <p><strong>Gradient, Divergence and Curl:</strong> Physical interpretations, vector identities.</p>
            
            <div class="formula">
                ∇·(∇×F) = 0 (Divergence of curl is zero)
            </div>
            
            <p><strong>Integral theorems:</strong> Applications of Green's, Stokes' and Gauss' theorems.</p>
        </div>
        
        <!-- Additional topics would continue in similar fashion -->
    </div>
    
    <div class="section" id="section2">
        <h2>Section 2: Metallurgical Thermodynamics</h2>
        
        <div class="topic-card">
            <h3>Laws of Thermodynamics</h3>
            <p><strong>First law:</strong> Energy conservation, internal energy, enthalpy, heat capacity.</p>
            
            <div class="formula">
                ΔU = q + w (First Law)
            </div>
            
            <p><strong>Second law:</strong> Entropy, Clausius inequality, Carnot cycle.</p>
            
            <div class="formula">
                dS ≥ δq/T (Second Law)
            </div>
            
            <div class="important">
                <h4>Key Concept</h4>
                <p>Gibbs free energy (G = H - TS) determines spontaneity at constant T and P</p>
            </div>
        </div>
        
        <div class="topic-card">
            <h3>Solutions and Phase Equilibria</h3>
            <p><strong>Ideal and regular solutions:</strong> Raoult's law, Henry's law, activity coefficients.</p>
            
            <div class="formula">
                μᵢ = μᵢ° + RTln(aᵢ) (Chemical potential)
            </div>
            
            <p><strong>Phase diagrams:</strong> Lever rule, eutectic, peritectic reactions, invariant points.</p>
            
            <div class="diagram">
                <h4>Binary Phase Diagram</h4>
                <img src="binary_phase_diagram.png" alt="Binary Phase Diagram">
                <p>Typical binary phase diagram showing liquidus, solidus, and various phase fields</p>
            </div>
        </div>
        
        <div class="topic-card">
            <h3>Electrochemistry</h3>
            <p><strong>Nernst equation:</strong> Relationship between cell potential and concentration.</p>
            
            <div class="formula">
                E = E° - (RT/nF)lnQ (Nernst equation)
            </div>
            
            <p><strong>Potential-pH diagrams:</strong> Pourbaix diagrams, corrosion immunity/passivation regions.</p>
        </div>
    </div>
    
    <!-- Sections 3 through 7 would follow the same pattern -->
    
    <div class="section" id="section3">
        <h2>Section 3: Transport Phenomena and Rate Processes</h2>
        
        <div class="topic-card">
            <h3>Momentum Transfer</h3>
            <p><strong>Viscosity:</strong> Newtonian vs. non-Newtonian fluids, shell balances.</p>
            
            <div class="formula">
                τ = -μ(du/dy) (Newton's law of viscosity)
            </div>
            
            <p><strong>Bernoulli's equation:</strong> Applications in fluid flow.</p>
        </div>
        
        <div class="topic-card">
            <h3>Heat Transfer</h3>
            <p><strong>Conduction:</strong> Fourier's law, thermal conductivity.</p>
            
            <div class="formula">
                q = -k(dT/dx) (Fourier's law)
            </div>
            
            <p><strong>Convection:</strong> Nusselt number correlations.</p>
            
            <p><strong>Radiation:</strong> Black body radiation laws.</p>
        </div>
        
        <div class="topic-card">
            <h3>Mass Transfer</h3>
            <p><strong>Fick's laws:</strong> Diffusion mechanisms, concentration profiles.</p>
            
            <div class="formula">
                J = -D(dC/dx) (Fick's first law)
            </div>
        </div>
    </div>
    
    <div class="section" id="section4">
        <h2>Section 4: Mineral Processing and Extractive Metallurgy</h2>
        
        <div class="topic-card">
            <h3>Mineral Beneficiation</h3>
            <p><strong>Comminution:</strong> Crushing and grinding laws (Rittinger's, Kick's, Bond's).</p>
            
            <p><strong>Flotation:</strong> Froth flotation process, collectors, frothers.</p>
            
            <div class="diagram">
                <h4>Flotation Cell Diagram</h4>
                <img src="flotation_cell.png" alt="Flotation Cell Diagram">
                <p>Components of a typical flotation cell</p>
            </div>
        </div>
        
        <div class="topic-card">
            <h3>Iron and Steel Making</h3>
            <p><strong>Blast furnace:</strong> Reactions, zones, burden materials.</p>
            
            <div class="important">
                <h4>Key Reactions</h4>
                <p>C + O₂ → CO₂<br>
                CO₂ + C → 2CO<br>
                Fe₂O₃ + 3CO → 2Fe + 3CO₂</p>
            </div>
            
            <p><strong>Basic oxygen furnace:</strong> Process dynamics, decarburization.</p>
        </div>
    </div>
    
    <div class="section" id="section5">
        <h2>Section 5: Physical Metallurgy</h2>
        
        <div class="topic-card">
            <h3>Crystal Structure</h3>
            <p><strong>BCC, FCC, HCP:</strong> Packing fractions, coordination numbers.</p>
            
            <div class="key-points">
                <h4>Crystal Structures Comparison</h4>
                <table>
                    <tr>
                        <th>Structure</th>
                        <th>APF</th>
                        <th>CN</th>
                        <th>Examples</th>
                    </tr>
                    <tr>
                        <td>BCC</td>
                        <td>0.68</td>
                        <td>8</td>
                        <td>Fe(α), W, Mo</td>
                    </tr>
                    <tr>
                        <td>FCC</td>
                        <td>0.74</td>
                        <td>12</td>
                        <td>Fe(γ), Al, Cu</td>
                    </tr>
                    <tr>
                        <td>HCP</td>
                        <td>0.74</td>
                        <td>12</td>
                        <td>Mg, Zn, Ti(α)</td>
                    </tr>
                </table>
            </div>
        </div>
        
        <div class="topic-card">
            <h3>Phase Transformations</h3>
            <p><strong>TTT diagrams:</strong> Pearlite, bainite, martensite formation.</p>
            
            <div class="diagram">
                <h4>TTT Diagram for Eutectoid Steel</h4>
                <img src="ttt_diagram.png" alt="TTT Diagram">
                <p>Time-Temperature-Transformation diagram showing various transformation products</p>
            </div>
        </div>
    </div>
    
    <div class="section" id="section6">
        <h2>Section 6: Mechanical Metallurgy</h2>
        
        <div class="topic-card">
            <h3>Dislocation Theory</h3>
            <p><strong>Edge, screw dislocations:</strong> Burgers vector, slip systems.</p>
            
            <div class="formula">
                τ = Gb/2πr (Stress field around dislocation)
            </div>
        </div>
        
        <div class="topic-card">
            <h3>Fracture Mechanics</h3>
            <p><strong>Griffith theory:</strong> Critical crack length, fracture toughness.</p>
            
            <div class="formula">
                Kᵢ = Yσ√(πa) (Stress intensity factor)
            </div>
        </div>
    </div>
    
    <div class="section" id="section7">
        <h2>Section 7: Manufacturing Processes</h2>
        
        <div class="topic-card">
            <h3>Metal Casting</h3>
            <p><strong>Mold design:</strong> Gating system, risers, solidification.</p>
            
            <div class="important">
                <h4>Casting Defects</h4>
                <p>Shrinkage porosity, gas porosity, misruns, cold shuts, hot tears</p>
            </div>
        </div>
        
        <div class="topic-card">
            <h3>Welding Metallurgy</h3>
            <p><strong>Heat affected zone:</strong> Microstructural changes, weld defects.</p>
            
            <div class="diagram">
                <h4>Welding Zones</h4>
                <img src="weld_zones.png" alt="Welding Zones">
                <p>Different microstructural zones in a weld joint</p>
            </div>
        </div>
    </div>
    
    <footer>
        <p>© 2023 GATE Metallurgy Study Guide | Designed for GATE MT Aspirants</p>
        <p>For more study materials and practice questions, visit our online portal</p>
    </footer>
</body>
</html>
