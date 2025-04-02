<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GATE MT - Engineering Mathematics</title>
    <style>
        :root {
            --primary-color: #d81b60;
            --secondary-color: #8e24aa;
            --accent-color: #5e35b1;
            --light-color: #fce4ec;
            --dark-color: #ad1457;
            --text-color: #212121;
            --highlight-color: #ffd600;
            --success-color: #43a047;
            --algebra-color: #3949ab;
            --calculus-color: #e53935;
            --vector-color: #00897b;
            --diffeq-color: #8e24aa;
            --stats-color: #fb8c00;
            --numerical-color: #7cb342;
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
        
        /* Animated Math Pattern Background */
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                linear-gradient(135deg, rgba(216,27,96,0.05) 0%, rgba(142,36,170,0.05) 50%, rgba(94,53,177,0.05) 100%),
                url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><text x="10" y="20" font-family="Arial" font-size="10" fill="%23d81b60" opacity="0.05">∫</text><text x="30" y="50" font-family="Arial" font-size="15" fill="%238e24aa" opacity="0.05">Σ</text><text x="70" y="30" font-family="Arial" font-size="12" fill="%235e35b1" opacity="0.05">∂</text><text x="50" y="80" font-family="Arial" font-size="18" fill="%23e53935" opacity="0.05">∇</text><text x="80" y="60" font-family="Arial" font-size="14" fill="%2300897b" opacity="0.05">π</text></svg>');
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
            color: rgba(216, 27, 96, 0.05);
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
            border-left: 5px solid var(--algebra-color);
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
            background-color: var(--algebra-color);
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
        .algebra {
            border-top: 4px solid var(--algebra-color);
        }
        
        .calculus {
            border-top: 4px solid var(--calculus-color);
        }
        
        .vector {
            border-top: 4px solid var(--vector-color);
        }
        
        .diffeq {
            border-top: 4px solid var(--diffeq-color);
        }
        
        .stats {
            border-top: 4px solid var(--stats-color);
        }
        
        .numerical {
            border-top: 4px solid var(--numerical-color);
        }
        
        /* Math visualization */
        .math-vis {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin: 2rem 0;
        }
        
        .math-concept {
            width: 150px;
            text-align: center;
            margin: 1rem;
            transition: all 0.3s ease;
        }
        
        .math-concept:hover {
            transform: scale(1.1);
        }
        
        .math-icon {
            width: 100px;
            height: 100px;
            margin: 0 auto;
            background-color: var(--light-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            color: white;
            box-shadow: 0 3px 6px rgba(0,0,0,0.2);
        }
        
        /* Matrix visualization */
        .matrix {
            display: inline-grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 5px;
            margin: 1rem 0;
            padding: 10px;
            background-color: #f5f5f5;
            border-radius: 5px;
        }
        
        .matrix-cell {
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: white;
            border-radius: 3px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.1);
        }
        
        /* Graph visualization */
        .graph {
            height: 200px;
            margin: 2rem auto;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="400" height="200" viewBox="0 0 400 200"><path d="M50,150 L100,120 L150,80 L200,100 L250,50 L300,100 L350,150" fill="none" stroke="%23d81b60" stroke-width="2"/><path d="M50,50 L100,80 L150,120 L200,100 L250,150 L300,100 L350,50" fill="none" stroke="%238e24aa" stroke-width="2"/></svg>') no-repeat center;
            background-size: contain;
            position: relative;
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
        
        /* Floating math symbols */
        .floating-math {
            position: absolute;
            font-size: 24px;
            opacity: 0.7;
            animation: float 10s infinite ease-in-out;
            z-index: -1;
        }
        
        @keyframes float {
            0%, 100% {transform: translate(0, 0) rotate(0deg);}
            25% {transform: translate(10px, 10px) rotate(5deg);}
            50% {transform: translate(-10px, 5px) rotate(-5deg);}
            75% {transform: translate(5px, -10px) rotate(3deg);}
        }
        
        /* Add floating math symbols */
        .math-symbols {
            position: relative;
            height: 0;
            overflow: visible;
        }
        
        .math-symbols span:nth-child(1) {
            top: 10%;
            left: 5%;
            animation-delay: 0s;
            color: var(--algebra-color);
        }
        
        .math-symbols span:nth-child(2) {
            top: 30%;
            left: 80%;
            animation-delay: 2s;
            color: var(--calculus-color);
        }
        
        .math-symbols span:nth-child(3) {
            top: 70%;
            left: 15%;
            animation-delay: 4s;
            color: var(--vector-color);
        }
        
        .math-symbols span:nth-child(4) {
            top: 50%;
            left: 90%;
            animation-delay: 6s;
            color: var(--diffeq-color);
        }
    </style>
</head>
<body>
    <div class="math-symbols">
        <span class="floating-math">∫</span>
        <span class="floating-math">∇</span>
        <span class="floating-math">Σ</span>
        <span class="floating-math">∂</span>
    </div>

    <header>
        <h1>Engineering Mathematics</h1>
        <p>Complete Guide for GATE Metallurgy (MT) - Section 1 (TestUrSelf)</p>
    </header>

    <div class="toc">
        <h2>Table of Contents</h2>
        <ol>
            <li><a href="#algebra">Linear Algebra</a></li>
            <li><a href="#calculus">Calculus</a></li>
            <li><a href="#vector">Vector Calculus</a></li>
            <li><a href="#diffeq">Differential Equations</a></li>
            <li><a href="#stats">Probability & Statistics</a></li>
            <li><a href="#numerical">Numerical Methods</a></li>
        </ol>
    </div>

    <div class="section algebra" id="algebra">
        <h2>1.1 Linear Algebra</h2>
        
        <div class="subsection" id="matrices">
            <h3>Matrices & Determinants</h3>
            <div class="topic-card">
                <div class="math-vis">
                    <div class="math-concept">
                        <div class="math-icon" style="background-color: var(--algebra-color);">A</div>
                        <p>Matrix Operations</p>
                    </div>
                    <div class="math-concept">
                        <div class="math-icon" style="background-color: var(--algebra-color);">|A|</div>
                        <p>Determinants</p>
                    </div>
                    <div class="math-concept">
                        <div class="math-icon" style="background-color: var(--algebra-color);">A⁻¹</div>
                        <p>Inverse Matrix</p>
                    </div>
                </div>
                
                <h4>Matrix Example</h4>
                <div class="matrix">
                    <div class="matrix-cell">a₁₁</div>
                    <div class="matrix-cell">a₁₂</div>
                    <div class="matrix-cell">a₁₃</div>
                    <div class="matrix-cell">a₂₁</div>
                    <div class="matrix-cell">a₂₂</div>
                    <div class="matrix-cell">a₂₃</div>
                    <div class="matrix-cell">a₃₁</div>
                    <div class="matrix-cell">a₃₂</div>
                    <div class="matrix-cell">a₃₃</div>
                </div>
                
                <div class="formula">
                    det(A) = a₁₁(a₂₂a₃₃ - a₂₃a₃₂) - a₁₂(a₂₁a₃₃ - a₂₃a₃₁) + a₁₃(a₂₁a₃₂ - a₂₂a₃₁)
                </div>
            </div>
        </div>
        
        <div class="subsection" id="eigen">
            <h3>Eigenvalues & Eigenvectors</h3>
            <div class="topic-card">
                <div class="formula">
                    Ax = λx
                </div>
                <p>Where:</p>
                <ul>
                    <li>A = square matrix</li>
                    <li>λ = eigenvalue (scalar)</li>
                    <li>x = eigenvector (non-zero)</li>
                </ul>
                
                <div class="example">
                    <h5>Example: Find Eigenvalues</h5>
                    <p>For matrix A = [[2, 1], [1, 2]]:</p>
                    <div class="formula">
                        det(A - λI) = (2-λ)² - 1 = 0 → λ = 1, 3
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="section calculus" id="calculus">
        <h2>1.2 Calculus</h2>
        
        <div class="subsection" id="limits">
            <h3>Limits & Continuity</h3>
            <div class="topic-card">
                <div class="formula">
                    lim<sub>x→a</sub> f(x) = L if ∀ε>0, ∃δ>0 : 0 < |x-a| < δ ⇒ |f(x)-L| < ε
                </div>
                
                <h4>Key Concepts</h4>
                <ul>
                    <li>Continuity: lim<sub>x→a</sub> f(x) = f(a)</li>
                    <li>Differentiability: f'(a) exists</li>
                    <li>L'Hôpital's Rule for 0/0 or ∞/∞ forms</li>
                </ul>
            </div>
        </div>
        
        <div class="subsection" id="maxima">
            <h3>Maxima & Minima</h3>
            <div class="topic-card">
                <div class="graph"></div>
                
                <div class="formula">
                    Critical points: f'(x) = 0 or undefined
                </div>
                <div class="formula">
                    Second derivative test: f''(x) > 0 ⇒ local min, f''(x) < 0 ⇒ local max
                </div>
            </div>
        </div>
    </div>

    <div class="section vector" id="vector">
        <h2>1.3 Vector Calculus</h2>
        
        <div class="subsection" id="grad-div-curl">
            <h3>Gradient, Divergence & Curl</h3>
            <div class="topic-card">
                <div class="math-vis">
                    <div class="math-concept">
                        <div class="math-icon" style="background-color: var(--vector-color);">∇f</div>
                        <p>Gradient</p>
                    </div>
                    <div class="math-concept">
                        <div class="math-icon" style="background-color: var(--vector-color);">∇·F</div>
                        <p>Divergence</p>
                    </div>
                    <div class="math-concept">
                        <div class="math-icon" style="background-color: var(--vector-color);">∇×F</div>
                        <p>Curl</p>
                    </div>
                </div>
                
                <div class="formula">
                    ∇f = (∂f/∂x, ∂f/∂y, ∂f/∂z)
                </div>
                <div class="formula">
                    ∇·F = ∂F<sub>x</sub>/∂x + ∂F<sub>y</sub>/∂y + ∂F<sub>z</sub>/∂z
                </div>
                <div class="formula">
                    ∇×F = (∂F<sub>z</sub>/∂y - ∂F<sub>y</sub>/∂z, ∂F<sub>x</sub>/∂z - ∂F<sub>z</sub>/∂x, ∂F<sub>y</sub>/∂x - ∂F<sub>x</sub>/∂y)
                </div>
            </div>
        </div>
        
        <div class="subsection" id="theorems">
            <h3>Integral Theorems</h3>
            <div class="topic-card">
                <table>
                    <tr>
                        <th>Theorem</th>
                        <th>Equation</th>
                        <th>Application</th>
                    </tr>
                    <tr>
                        <td>Green's</td>
                        <td>∮<sub>C</sub> (Pdx + Qdy) = ∬<sub>D</sub> (∂Q/∂x - ∂P/∂y) dA</td>
                        <td>2D regions</td>
                    </tr>
                    <tr>
                        <td>Stokes'</td>
                        <td>∮<sub>C</sub> F·dr = ∬<sub>S</sub> (∇×F)·dS</td>
                        <td>3D surfaces</td>
                    </tr>
                    <tr>
                        <td>Gauss'</td>
                        <td>∯<sub>S</sub> F·dS = ∭<sub>V</sub> (∇·F) dV</td>
                        <td>3D volumes</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>

    <div class="section diffeq" id="diffeq">
        <h2>1.4 Differential Equations</h2>
        
        <div class="subsection" id="odes">
            <h3>Ordinary Differential Equations</h3>
            <div class="topic-card">
                <h4>First Order ODEs</h4>
                <div class="formula">
                    dy/dx + P(x)y = Q(x) (Linear)
                </div>
                <div class="formula">
                    M(x,y)dx + N(x,y)dy = 0 (Exact)
                </div>
                
                <h4>Second Order Linear</h4>
                <div class="formula">
                    ay'' + by' + cy = 0 → Characteristic equation: ar² + br + c = 0
                </div>
            </div>
        </div>
        
        <div class="subsection" id="pdes">
            <h3>Partial Differential Equations</h3>
            <div class="topic-card">
                <table>
                    <tr>
                        <th>Equation</th>
                        <th>Form</th>
                        <th>Solution Method</th>
                    </tr>
                    <tr>
                        <td>Laplace</td>
                        <td>∇²u = 0</td>
                        <td>Separation of variables</td>
                    </tr>
                    <tr>
                        <td>Heat</td>
                        <td>∂u/∂t = α∇²u</td>
                        <td>Fourier series</td>
                    </tr>
                    <tr>
                        <td>Wave</td>
                        <td>∂²u/∂t² = c²∇²u</td>
                        <td>d'Alembert's solution</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>

    <div class="section stats" id="stats">
        <h2>1.5 Probability & Statistics</h2>
        
        <div class="subsection" id="probability">
            <h3>Probability Basics</h3>
            <div class="topic-card">
                <div class="formula">
                    P(A∪B) = P(A) + P(B) - P(A∩B)
                </div>
                <div class="formula">
                    P(A|B) = P(A∩B)/P(B) (Conditional Probability)
                </div>
                
                <div class="math-vis">
                    <div class="math-concept">
                        <div class="math-icon" style="background-color: var(--stats-color);">μ</div>
                        <p>Mean</p>
                    </div>
                    <div class="math-concept">
                        <div class="math-icon" style="background-color: var(--stats-color);">σ</div>
                        <p>Std Dev</p>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="subsection" id="distributions">
            <h3>Probability Distributions</h3>
            <div class="topic-card">
                <table>
                    <tr>
                        <th>Distribution</th>
                        <th>PMF/PDF</th>
                        <th>Parameters</th>
                    </tr>
                    <tr>
                        <td>Binomial</td>
                        <td>C(n,k)p<sup>k</sup>(1-p)<sup>n-k</sup></td>
                        <td>n, p</td>
                    </tr>
                    <tr>
                        <td>Poisson</td>
                        <td>(λ<sup>k</sup>e<sup>-λ</sup>)/k!</td>
                        <td>λ</td>
                    </tr>
                    <tr>
                        <td>Normal</td>
                        <td>(1/σ√2π)e<sup>-(x-μ)²/2σ²</sup></td>
                        <td>μ, σ</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>

    <div class="section numerical" id="numerical">
        <h2>1.6 Numerical Methods</h2>
        
        <div class="subsection" id="root-finding">
            <h3>Root Finding Methods</h3>
            <div class="topic-card">
                <div class="math-vis">
                    <div class="math-concept">
                        <div class="math-icon" style="background-color: var(--numerical-color);">B</div>
                        <p>Bisection</p>
                    </div>
                    <div class="math-concept">
                        <div class="math-icon" style="background-color: var(--numerical-color);">N</div>
                        <p>Newton-Raphson</p>
                    </div>
                    <div class="math-concept">
                        <div class="math-icon" style="background-color: var(--numerical-color);">S</div>
                        <p>Secant</p>
                    </div>
                </div>
                
                <div class="formula">
                    Newton-Raphson: x<sub>n+1</sub> = x<sub>n</sub> - f(x<sub>n</sub>)/f'(x<sub>n</sub>)
                </div>
            </div>
        </div>
        
        <div class="subsection" id="integration">
            <h3>Numerical Integration</h3>
            <div class="topic-card">
                <div class="formula">
                    Trapezoidal: ∫<sub>a</sub><sup>b</sup> f(x)dx ≈ (h/2)[f(x₀) + 2Σf(xᵢ) + f(xₙ)]
                </div>
                <div class="formula">
                    Simpson's: ∫<sub>a</sub><sup>b</sup> f(x)dx ≈ (h/3)[f(x₀) + 4Σf(x<sub>odd</sub>) + 2Σf(x<sub>even</sub>) + f(xₙ)]
                </div>
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
