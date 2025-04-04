<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Linear Algebra: Matrices & Determinants | TestUrSelf</title>
    <style>
        :root {
            --primary-color: #1565C0;
            --secondary-color: #00897B;
            --accent-color: #6A1B9A;
            --light-color: #E3F2FD;
            --dark-color: #0D47A1;
            --text-color: #212121;
            --highlight-color: #FFC107;
            --success-color: #388E3C;
            --error-color: #D32F2F;
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
            background: linear-gradient(135deg, #E3F2FD 0%, #BBDEFB 50%, #E3F2FD 100%);
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
            content: "TestUrSelf";
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-30deg);
            font-size: 150px;
            font-weight: bold;
            color: rgba(21, 101, 192, 0.05);
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
            margin-bottom: 2rem;
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
            font-size: 3rem;
            font-weight: 900;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            letter-spacing: 1px;
        }
        
        h2 {
            color: var(--primary-color);
            border-bottom: 4px solid var(--highlight-color);
            padding-bottom: 0.8rem;
            margin-top: 3rem;
            font-size: 2.2rem;
            background: linear-gradient(to right, transparent, var(--light-color), transparent);
            padding: 1rem 0;
            text-align: center;
            border-radius: 8px;
            position: relative;
            scroll-margin-top: 120px;
        }
        
        h2::after {
            content: "";
            position: absolute;
            left: 0;
            right: 0;
            bottom: -5px;
            height: 3px;
            background: linear-gradient(to right, transparent, var(--highlight-color), transparent);
        }
        
        h3 {
            color: var(--dark-color);
            margin-top: 2.5rem;
            font-size: 1.8rem;
            border-left: 5px solid var(--highlight-color);
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
            background: linear-gradient(to right, var(--highlight-color), transparent);
        }
        
        .section {
            background-color: white;
            border-radius: 12px;
            padding: 2.5rem;
            margin-bottom: 3rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
            z-index: 1;
            transition: all 0.3s ease;
            border: 1px solid rgba(0,0,0,0.05);
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }
        
        /* Table of Contents - Fixed Position */
        .toc-container {
            position: sticky;
            top: 20px;
            z-index: 5;
            margin-bottom: 2rem;
        }
        
        .toc {
            background-color: white;
            border-radius: 12px;
            padding: 1.5rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            max-height: 80vh;
            overflow-y: auto;
        }
        
        .toc h2 {
            margin-top: 0;
            text-align: left;
            padding-left: 0;
            position: sticky;
            top: 0;
            background: white;
            z-index: 1;
            padding-bottom: 1rem;
        }
        
        .toc ul {
            list-style-type: none;
            padding: 0;
            margin: 0;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 10px;
        }
        
        .toc li {
            margin-bottom: 0.5rem;
        }
        
        .toc a {
            display: block;
            padding: 0.8rem 1rem;
            background-color: var(--light-color);
            color: var(--dark-color);
            text-decoration: none;
            border-radius: 6px;
            transition: all 0.3s ease;
            font-weight: 500;
            border-left: 4px solid var(--primary-color);
        }
        
        .toc a:hover {
            background-color: rgba(21, 101, 192, 0.1);
            transform: translateX(5px);
        }
        
        /* MCQ Styling */
        .mcq {
            background-color: rgba(255, 213, 79, 0.1);
            border-left: 4px solid var(--highlight-color);
            padding: 1.5rem;
            margin: 2rem 0;
            border-radius: 0 8px 8px 0;
            transition: all 0.3s ease;
        }
        
        .mcq:hover {
            background-color: rgba(255, 213, 79, 0.15);
        }
        
        .question {
            font-weight: 600;
            font-size: 1.1rem;
            margin-bottom: 1rem;
            color: var(--primary-color);
        }
        
        .options {
            display: grid;
            gap: 8px;
        }
        
        .option {
            padding: 10px 15px;
            background-color: rgba(255,255,255,0.8);
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.2s ease;
            border: 1px solid #e0e0e0;
            position: relative;
            opacity: 0;
            transform: translateY(20px);
            animation: fadeIn 0.5s forwards;
        }
        
        @keyframes fadeIn {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .option:hover {
            background-color: rgba(255, 213, 79, 0.2);
            border-color: var(--highlight-color);
        }
        
        .option.correct {
            background-color: rgba(56, 142, 60, 0.2);
            border-color: var(--success-color);
            color: var(--success-color);
        }
        
        .option.correct::after {
            content: "✓";
            position: absolute;
            right: 15px;
            color: var(--success-color);
            font-weight: bold;
        }
        
        .option.incorrect {
            background-color: rgba(211, 47, 47, 0.1);
            border-color: var(--error-color);
            color: var(--error-color);
        }
        
        .option.incorrect::after {
            content: "✗";
            position: absolute;
            right: 15px;
            color: var(--error-color);
            font-weight: bold;
        }
        
        .answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease, padding 0.5s ease;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 6px;
        }
        
        .answer.show {
            max-height: 500px;
            padding: 1rem;
            margin-top: 1rem;
            border: 2px solid var(--highlight-color);
            animation: pulse 1.5s infinite alternate;
        }
        
        @keyframes pulse {
            0% {box-shadow: 0 0 0 0 rgba(255, 171, 0, 0.4);}
            100% {box-shadow: 0 0 0 10px rgba(255, 171, 0, 0);}
        }
        
        .answer-content {
            padding: 1rem;
        }
        
        .show-answer-btn {
            background: linear-gradient(to right, var(--primary-color), var(--accent-color));
            color: white;
            border: none;
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            cursor: pointer;
            margin-top: 1rem;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 8px rgba(21, 101, 192, 0.3);
        }
        
        .show-answer-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(21, 101, 192, 0.4);
        }
        
        /* Content Boxes */
        .key-point {
            background: linear-gradient(to right, #E3F2FD, #BBDEFB);
            border-left: 6px solid var(--secondary-color);
            padding: 1.8rem;
            margin: 2.5rem 0;
            border-radius: 0 10px 10px 0;
            position: relative;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
        }
        
        .key-point::before {
            content: "!";
            position: absolute;
            left: -15px;
            top: -15px;
            width: 30px;
            height: 30px;
            background-color: var(--secondary-color);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        
        .formula-box {
            background-color: #E8EAF6;
            border-left: 4px solid var(--accent-color);
            padding: 1.5rem;
            margin: 1.5rem 0;
            border-radius: 0 8px 8px 0;
            font-family: 'Courier New', monospace;
            position: relative;
            overflow: hidden;
        }
        
        .formula-box::before {
            content: "FORMULA";
            position: absolute;
            top: 0;
            right: 0;
            background-color: var(--accent-color);
            color: white;
            padding: 0.2rem 0.8rem;
            font-size: 0.8rem;
            border-bottom-left-radius: 8px;
            font-family: 'Roboto', sans-serif;
        }
        
        .process-steps {
            counter-reset: step;
            margin: 2rem 0;
        }
        
        .process-step {
            position: relative;
            padding-left: 4rem;
            margin-bottom: 2rem;
            min-height: 3rem;
        }
        
        .process-step::before {
            counter-increment: step;
            content: counter(step);
            position: absolute;
            left: 0;
            top: 0;
            width: 2.5rem;
            height: 2.5rem;
            background: linear-gradient(to bottom right, var(--primary-color), var(--dark-color));
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .method-card {
            background: white;
            border-radius: 10px;
            padding: 1.5rem;
            margin: 1.5rem 0;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            border-top: 5px solid var(--primary-color);
            transition: transform 0.3s ease;
        }
        
        .method-card.determinants {
            border-top-color: var(--secondary-color);
        }
        
        .method-card.matrices {
            border-top-color: var(--accent-color);
        }
        
        .method-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 2rem 0;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            border-radius: 8px;
            overflow: hidden;
        }
        
        th, td {
            padding: 1rem;
            text-align: left;
            border-bottom: 1px solid #e0e0e0;
        }
        
        th {
            background: linear-gradient(to right, var(--primary-color), var(--dark-color));
            color: white;
            font-weight: 500;
        }
        
        tr:nth-child(even) {
            background-color: #f9f9f9;
        }
        
        tr:hover {
            background-color: #f0f0f0;
        }
        
        /* Score Counter */
        .score-counter {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            color: white;
            padding: 1rem 1.5rem;
            border-radius: 50px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
            z-index: 10;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 100% {transform: translateY(0);}
            50% {transform: translateY(-5px);}
        }
        
        .score-counter i {
            font-size: 1.2rem;
        }
        
        /* Responsive adjustments */
        @media (max-width: 768px) {
            body {
                padding: 10px;
            }
            
            body::after {
                font-size: 80px;
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
            
            .toc ul {
                grid-template-columns: 1fr;
            }
            
            .toc-container {
                position: static;
            }
            
            .toc {
                max-height: none;
            }
            
            .score-counter {
                bottom: 10px;
                right: 10px;
                padding: 0.8rem 1.2rem;
                font-size: 0.9rem;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700;900&display=swap" rel="stylesheet">
    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
</head>
<body>
    <header>
        <h1>Linear Algebra</h1>
        <p>Matrices & Determinants</p>
        <div class="gate-banner">
            <strong>Join TestUrSelf for your GATE MT & XE Prep</strong> - Master these concepts with our comprehensive study materials!
        </div>
    </header>

    <div class="toc-container">
        <div class="toc">
            <h2>Table of Contents</h2>
            <ul>
                <li><a href="#matrices"><i class="fas fa-matrix"></i> Matrices Fundamentals</a></li>
                <li><a href="#operations"><i class="fas fa-calculator"></i> Matrix Operations</a></li>
                <li><a href="#types"><i class="fas fa-shapes"></i> Special Matrix Types</a></li>
                <li><a href="#determinants"><i class="fas fa-square-root-alt"></i> Determinants</a></li>
                <li><a href="#properties"><i class="fas fa-list-ol"></i> Properties of Determinants</a></li>
                <li><a href="#applications"><i class="fas fa-cogs"></i> Applications</a></li>
                <li><a href="#quiz"><i class="fas fa-question-circle"></i> Practice Quiz</a></li>
            </ul>
        </div>
    </div>

    <section id="matrices" class="section">
        <h2>1. Matrices Fundamentals</h2>
        <p>A matrix is a rectangular array of numbers arranged in rows and columns. Matrices are fundamental objects in linear algebra and have wide applications in mathematics, physics, engineering, and computer science.</p>
        
        <div class="formula-box">
            $$ A = \begin{bmatrix}
            a_{11} & a_{12} & \cdots & a_{1n} \\
            a_{21} & a_{22} & \cdots & a_{2n} \\
            \vdots & \vdots & \ddots & \vdots \\
            a_{m1} & a_{m2} & \cdots & a_{mn}
            \end{bmatrix} $$
        </div>
        
        <p>An <strong>m × n</strong> matrix has <strong>m</strong> rows and <strong>n</strong> columns. The element in the i-th row and j-th column is denoted as <strong>a<sub>ij</sub></strong>.</p>
        
        <h3>Matrix Notation</h3>
        <p>Matrices are typically denoted by uppercase letters (A, B, C, ...) and their elements by corresponding lowercase letters with subscripts.</p>
        
        <div class="method-card matrices">
            <h4>Example: 2×3 Matrix</h4>
            <p>Consider matrix B:</p>
            <div class="formula-box">
                $$ B = \begin{bmatrix}
                1 & 4 & 0 \\
                -2 & 3 & 5
                \end{bmatrix} $$
            </div>
            <p>Here, b<sub>11</sub> = 1, b<sub>12</sub> = 4, b<sub>21</sub> = -2, etc.</p>
        </div>
    </section>

    <section id="operations" class="section">
        <h2>2. Matrix Operations</h2>
        <h3>Matrix Addition</h3>
        <p>Two matrices of the same dimensions can be added by adding their corresponding elements.</p>
        
        <div class="formula-box">
            $$ (A + B)_{ij} = A_{ij} + B_{ij} $$
        </div>
        
        <div class="method-card matrices">
            <h4>Example</h4>
            <div class="formula-box">
                $$ \begin{bmatrix}
                1 & 3 \\
                2 & 4
                \end{bmatrix} +
                \begin{bmatrix}
                5 & 7 \\
                6 & 8
                \end{bmatrix} =
                \begin{bmatrix}
                1+5 & 3+7 \\
                2+6 & 4+8
                \end{bmatrix} =
                \begin{bmatrix}
                6 & 10 \\
                8 & 12
                \end{bmatrix} $$
            </div>
        </div>
        
        <h3>Scalar Multiplication</h3>
        <p>A matrix can be multiplied by a scalar by multiplying each element by that scalar.</p>
        
        <div class="formula-box">
            $$ (cA)_{ij} = c \cdot A_{ij} $$
        </div>
        
        <h3>Matrix Multiplication</h3>
        <p>For matrix multiplication AB, the number of columns in A must equal the number of rows in B.</p>
        
        <div class="formula-box">
            $$ (AB)_{ij} = \sum_{k=1}^{n} A_{ik} B_{kj} $$
        </div>
        
        <div class="method-card matrices">
            <h4>Example</h4>
            <div class="formula-box">
                $$ \begin{bmatrix}
                1 & 2 \\
                3 & 4
                \end{bmatrix}
                \begin{bmatrix}
                5 & 6 \\
                7 & 8
                \end{bmatrix} =
                \begin{bmatrix}
                1×5+2×7 & 1×6+2×8 \\
                3×5+4×7 & 3×6+4×8
                \end{bmatrix} =
                \begin{bmatrix}
                19 & 22 \\
                43 & 50
                \end{bmatrix} $$
            </div>
        </div>
    </section>

    <section id="types" class="section">
        <h2>3. Special Matrix Types</h2>
        
        <div class="method-card">
            <h3>Square Matrix</h3>
            <p>Number of rows equals number of columns (n × n)</p>
            <div class="formula-box">
                $$ A = \begin{bmatrix}
                a & b \\
                c & d
                \end{bmatrix} $$
            </div>
        </div>
        
        <div class="method-card">
            <h3>Identity Matrix</h3>
            <p>Diagonal elements are 1, others are 0</p>
            <div class="formula-box">
                $$ I_3 = \begin{bmatrix}
                1 & 0 & 0 \\
                0 & 1 & 0 \\
                0 & 0 & 1
                \end{bmatrix} $$
            </div>
        </div>
        
        <div class="method-card">
            <h3>Diagonal Matrix</h3>
            <p>Non-diagonal elements are zero</p>
            <div class="formula-box">
                $$ D = \begin{bmatrix}
                a & 0 & 0 \\
                0 & b & 0 \\
                0 & 0 & c
                \end{bmatrix} $$
            </div>
        </div>
        
        <div class="method-card">
            <h3>Symmetric Matrix</h3>
            <p>A = A<sup>T</sup> (equal to its transpose)</p>
            <div class="formula-box">
                $$ S = \begin{bmatrix}
                1 & 2 & 3 \\
                2 & 4 & 5 \\
                3 & 5 & 6
                \end{bmatrix} $$
            </div>
        </div>
    </section>

    <section id="determinants" class="section">
        <h2>4. Determinants</h2>
        <p>The determinant is a scalar value that can be computed from a square matrix and encodes important properties of the matrix.</p>
        
        <h3>2×2 Determinant</h3>
        <div class="formula-box">
            $$ \det \begin{bmatrix}
            a & b \\
            c & d
            \end{bmatrix} = ad - bc $$
        </div>
        
        <h3>3×3 Determinant (Sarrus Rule)</h3>
        <div class="formula-box">
            $$ \det \begin{bmatrix}
            a & b & c \\
            d & e & f \\
            g & h & i
            \end{bmatrix} = aei + bfg + cdh - ceg - bdi - afh $$
        </div>
        
        <div class="method-card determinants">
            <h4>Example</h4>
            <div class="formula-box">
                $$ \det \begin{bmatrix}
                1 & 2 & 3 \\
                4 & 5 & 6 \\
                7 & 8 & 9
                \end{bmatrix} = (1×5×9) + (2×6×7) + (3×4×8) - (3×5×7) - (2×4×9) - (1×6×8) $$
                $$ = 45 + 84 + 96 - 105 - 72 - 48 = 0 $$
            </div>
        </div>
        
        <h3>General n×n Determinant (Laplace Expansion)</h3>
        <div class="formula-box">
            $$ \det(A) = \sum_{j=1}^{n} (-1)^{i+j} a_{ij} \det(A_{ij}) $$
        </div>
        <p>where A<sub>ij</sub> is the submatrix obtained by removing the i-th row and j-th column.</p>
    </section>

    <section id="properties" class="section">
        <h2>5. Properties of Determinants</h2>
        
        <div class="key-point">
            <h4>Key Properties</h4>
            <ul>
                <li><strong>Determinant of Identity:</strong> det(I) = 1</li>
                <li><strong>Triangular Matrix:</strong> det = product of diagonal elements</li>
                <li><strong>Product of Matrices:</strong> det(AB) = det(A)det(B)</li>
                <li><strong>Transpose Property:</strong> det(A<sup>T</sup>) = det(A)</li>
                <li><strong>Scalar Multiplication:</strong> det(cA) = c<sup>n</sup>det(A)</li>
                <li><strong>Inverse Matrix:</strong> det(A<sup>-1</sup>) = 1/det(A)</li>
            </ul>
        </div>
        
        <div class="method-card determinants">
            <h4>Example: Product Property</h4>
            <p>For matrices A and B:</p>
            <div class="formula-box">
                $$ A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}, \quad B = \begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix} $$
                $$ \det(A) = -2, \quad \det(B) = 1 $$
                $$ AB = \begin{bmatrix} 2 & -1 \\ 4 & -3 \end{bmatrix}, \quad \det(AB) = -2 $$
                $$ \det(A)\det(B) = -2 \times 1 = -2 $$
            </div>
        </div>
    </section>

    <section id="applications" class="section">
        <h2>6. Applications</h2>
        
        <h3>Solving Linear Systems (Cramer's Rule)</h3>
        <p>For a system Ax = b, if A is invertible:</p>
        <div class="formula-box">
            $$ x_i = \frac{\det(A_i)}{\det(A)} $$
        </div>
        <p>where A<sub>i</sub> is A with the i-th column replaced by b.</p>
        
        <h3>Area/Volume Calculation</h3>
        <p>The absolute value of the determinant gives the scaling factor of the linear transformation described by the matrix.</p>
        <div class="formula-box">
            $$ \text{Area} = \left| \det \begin{bmatrix}
            a & c \\
            b & d
            \end{bmatrix} \right| $$
        </div>
        
        <h3>Eigenvalues</h3>
        <p>The determinant is used in finding eigenvalues:</p>
        <div class="formula-box">
            $$ \det(A - \lambda I) = 0 $$
        </div>
    </section>

    <section id="quiz" class="section">
        <h2>7. Practice Quiz</h2>
        <p>Test your understanding with these GATE-style multiple choice questions:</p>
        
        <div class="mcq">
            <div class="question">1. What is the determinant of the following 2×2 matrix?
                $$ \begin{bmatrix} 3 & 4 \\ 1 & 2 \end{bmatrix} $$
            </div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">2</div>
                <div class="option" onclick="checkAnswer(this, false)">5</div>
                <div class="option" onclick="checkAnswer(this, false)">10</div>
                <div class="option" onclick="checkAnswer(this, true)">2</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: 2</strong></p>
                    <p>The determinant is calculated as (3×2) - (4×1) = 6 - 4 = 2.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">2. Which of the following is NOT a property of determinants?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">det(AB) = det(A)det(B)</div>
                <div class="option" onclick="checkAnswer(this, true)">det(A+B) = det(A) + det(B)</div>
                <div class="option" onclick="checkAnswer(this, false)">det(A<sup>T</sup>) = det(A)</div>
                <div class="option" onclick="checkAnswer(this, false)">det(cA) = c<sup>n</sup>det(A) for n×n matrix A</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: det(A+B) = det(A) + det(B)</strong></p>
                    <p>Determinant of sum is not equal to sum of determinants. The determinant is multiplicative but not additive.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">3. For a 3×3 matrix A with det(A) = 5, what is det(2A)?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">10</div>
                <div class="option" onclick="checkAnswer(this, true)">40</div>
                <div class="option" onclick="checkAnswer(this, false)">5</div>
                <div class="option" onclick="checkAnswer(this, false)">2.5</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: 40</strong></p>
                    <p>For n×n matrix, det(kA) = k<sup>n</sup>det(A). Here 2<sup>3</sup>×5 = 8×5 = 40.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">4. What is the determinant of the identity matrix I<sub>4</sub>?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">0</div>
                <div class="option" onclick="checkAnswer(this, true)">1</div>
                <div class="option" onclick="checkAnswer(this, false)">4</div>
                <div class="option" onclick="checkAnswer(this, false)">Undefined</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: 1</strong></p>
                    <p>The determinant of any identity matrix is always 1 regardless of size.</p>
                </div>
            </div>
        </div>
    </section>

    <div class="score-counter" id="scoreCounter">
        <i class="fas fa-star"></i> <span id="score">0</span> Points
    </div>

    <script>
        // Score tracking
        let score = 0;
        const scoreElement = document.getElementById('score');
        
        // MCQ functionality
        function checkAnswer(option, isCorrect) {
            const options = option.parentElement.querySelectorAll('.option');
            options.forEach(opt => {
                opt.classList.remove('correct', 'incorrect');
                opt.style.transform = '';
                opt.style.boxShadow = '';
            });
            
            if (isCorrect) {
                option.classList.add('correct');
                option.style.transform = 'scale(1.02)';
                option.style.boxShadow = '0 4px 8px rgba(56, 142, 60, 0.3)';
                
                // Add points for correct answer
                score += 2;
                scoreElement.textContent = score;
                
                // Confetti effect for correct answer
                if (typeof confetti === 'function') {
                    confetti({
                        particleCount: 100,
                        spread: 70,
                        origin: { y: 0.6 }
                    });
                }
            } else {
                option.classList.add('incorrect');
                option.style.transform = 'scale(0.98)';
                option.style.boxShadow = '0 4px 8px rgba(211, 47, 47, 0.3)';
                
                // Highlight correct answer
                const correctOption = Array.from(options).find(opt => 
                    opt.getAttribute('onclick').includes('true'));
                if (correctOption) {
                    correctOption.classList.add('correct');
                    correctOption.style.transform = 'scale(1.02)';
                    correctOption.style.boxShadow = '0 4px 8px rgba(56, 142, 60, 0.3)';
                }
            }
        }
        
        function toggleAnswer(button) {
            const answer = button.nextElementSibling;
            answer.classList.toggle('show');
            
            if (answer.classList.contains('show')) {
                button.innerHTML = '<i class="fas fa-eye-slash"></i> Hide Answer';
                button.style.background = 'linear-gradient(to right, #0D47A1, #1565C0)';
            } else {
                button.innerHTML = '<i class="fas fa-lightbulb"></i> Show Answer';
                button.style.background = 'linear-gradient(to right, var(--primary-color), var(--accent-color))';
            }
        }
        
        // Initialize MCQ options animation
        document.addEventListener('DOMContentLoaded', function() {
            // Animate MCQ options sequentially
            const options = document.querySelectorAll('.option');
            options.forEach((option, index) => {
                setTimeout(() => {
                    option.style.opacity = '1';
                    option.style.transform = 'translateY(0)';
                }, index * 100);
            });
            
            // Add scroll margin to account for fixed header
            document.querySelectorAll('h2').forEach(h2 => {
                h2.style.scrollMarginTop = '120px';
            });
        });
    </script>
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.4.0/dist/confetti.browser.min.js"></script>
</body>
</html>
