<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Linear Algebra: Matrices & Determinants | TestUrSelf</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #6a11cb;
            --secondary: #2575fc;
            --accent: #ff3e9d;
            --text: #2d3748;
            --light: #f7fafc;
            --dark: #1a202c;
            --success: #48bb78;
            --warning: #ed8936;
            --danger: #f56565;
            --code-bg: #282c34;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            line-height: 1.8;
            color: var(--text);
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            background-attachment: fixed;
            overflow-x: hidden;
            position: relative;
        }

        /* Watermark */
        body::before {
            content: "TestUrSelf";
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-30deg);
            font-size: 120px;
            font-weight: bold;
            color: rgba(106, 17, 203, 0.08);
            z-index: -1;
            pointer-events: none;
            white-space: nowrap;
            text-transform: uppercase;
            letter-spacing: 15px;
            width: 100%;
            text-align: center;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 4rem 2rem;
            text-align: center;
            margin-bottom: 3rem;
            border-radius: 0 0 20px 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            position: relative;
            overflow: hidden;
        }

        header::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(
                to bottom right,
                rgba(255,255,255,0.1) 0%,
                rgba(255,255,255,0) 50%,
                rgba(255,255,255,0.1) 100%
            );
            animation: shine 8s infinite;
        }

        @keyframes shine {
            0% { transform: translateX(-100%) translateY(-100%) rotate(30deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(30deg); }
        }

        h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
            font-weight: 400;
        }

        .gate-banner {
            background: rgba(255, 255, 255, 0.9);
            border-radius: 10px;
            padding: 1rem;
            margin: 1.5rem 0;
            text-align: center;
            border-left: 5px solid var(--accent);
            box-shadow: 0 3px 15px rgba(0,0,0,0.1);
        }

        .gate-banner strong {
            color: var(--accent);
            font-weight: 700;
        }

        .toc-container {
            background: white;
            border-radius: 15px;
            padding: 2rem;
            margin-bottom: 3rem;
            box-shadow: 0 5px 25px rgba(0,0,0,0.1);
            position: sticky;
            top: 20px;
            z-index: 10;
        }

        .toc-title {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .toc-list {
            list-style: none;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1rem;
        }

        .toc-item {
            margin-bottom: 0.5rem;
        }

        .toc-link {
            color: var(--text);
            text-decoration: none;
            padding: 0.5rem 1rem;
            border-radius: 8px;
            display: block;
            transition: all 0.3s ease;
            background: rgba(106, 17, 203, 0.05);
            border-left: 4px solid var(--primary);
        }

        .toc-link:hover {
            background: rgba(106, 17, 203, 0.1);
            transform: translateX(5px);
        }

        .section {
            background: white;
            border-radius: 15px;
            padding: 2.5rem;
            margin-bottom: 3rem;
            box-shadow: 0 5px 25px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0,0,0,0.15);
        }

        h2 {
            color: var(--primary);
            margin-bottom: 1.5rem;
            font-size: 2rem;
            position: relative;
            padding-bottom: 0.5rem;
            scroll-margin-top: 120px;
        }

        h2::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100px;
            height: 4px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            border-radius: 2px;
        }

        h3 {
            color: var(--secondary);
            margin: 1.5rem 0 1rem;
            font-size: 1.5rem;
        }

        p {
            margin-bottom: 1.5rem;
        }

        .equation {
            font-family: 'Fira Code', monospace;
            background: rgba(40, 44, 52, 0.05);
            padding: 1.5rem;
            border-radius: 10px;
            margin: 1.5rem 0;
            overflow-x: auto;
            border-left: 4px solid var(--accent);
        }

        .equation.large {
            font-size: 1.2rem;
            text-align: center;
        }

        .example {
            background: rgba(37, 117, 252, 0.05);
            border-left: 4px solid var(--secondary);
            padding: 1.5rem;
            border-radius: 0 10px 10px 0;
            margin: 1.5rem 0;
        }

        .example-title {
            font-weight: 600;
            color: var(--secondary);
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .properties {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
            margin: 1.5rem 0;
        }

        .property-card {
            background: white;
            border-radius: 10px;
            padding: 1.5rem;
            box-shadow: 0 3px 15px rgba(0,0,0,0.05);
            border-top: 4px solid var(--accent);
            transition: all 0.3s ease;
        }

        .property-card:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }

        .property-title {
            color: var(--accent);
            margin-bottom: 0.5rem;
            font-weight: 600;
        }

        /* Quiz Section */
        .quiz-section {
            background: linear-gradient(135deg, rgba(255,255,255,0.9), rgba(245,247,250,0.9));
            border-radius: 15px;
            padding: 2.5rem;
            margin: 3rem 0;
            box-shadow: 0 5px 25px rgba(0,0,0,0.1);
            border: 2px dashed var(--accent);
        }

        .quiz-title {
            color: var(--accent);
            text-align: center;
            margin-bottom: 2rem;
            font-size: 1.8rem;
        }

        .quiz-question {
            background: white;
            border-radius: 10px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
            border-left: 4px solid var(--secondary);
        }

        .question-text {
            font-weight: 600;
            margin-bottom: 1rem;
            color: var(--dark);
        }

        .options {
            display: grid;
            grid-template-columns: 1fr;
            gap: 0.8rem;
        }

        .option {
            padding: 0.8rem 1rem;
            background: rgba(106, 17, 203, 0.05);
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s ease;
            position: relative;
            padding-left: 2.5rem;
        }

        .option:hover {
            background: rgba(106, 17, 203, 0.1);
        }

        .option input {
            position: absolute;
            opacity: 0;
        }

        .option label {
            cursor: pointer;
            display: flex;
            align-items: center;
        }

        .option label::before {
            content: "";
            width: 1.2rem;
            height: 1.2rem;
            border: 2px solid var(--secondary);
            border-radius: 50%;
            margin-right: 1rem;
            position: absolute;
            left: 1rem;
        }

        .option input:checked + label::before {
            background: var(--secondary);
            box-shadow: inset 0 0 0 2px white;
        }

        .feedback {
            margin-top: 1rem;
            padding: 0.8rem;
            border-radius: 6px;
            display: none;
        }

        .correct {
            background: rgba(72, 187, 120, 0.1);
            color: var(--success);
            border-left: 4px solid var(--success);
        }

        .incorrect {
            background: rgba(245, 101, 101, 0.1);
            color: var(--danger);
            border-left: 4px solid var(--danger);
        }

        .submit-btn {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            border: none;
            padding: 0.8rem 1.5rem;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            margin-top: 1rem;
            transition: all 0.3s ease;
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .results {
            text-align: center;
            margin-top: 1.5rem;
            font-weight: 600;
            display: none;
        }

        footer {
            background: linear-gradient(135deg, var(--dark), #2d3748);
            color: white;
            text-align: center;
            padding: 3rem 0;
            margin-top: 3rem;
            position: relative;
        }

        .footer-watermark {
            position: absolute;
            bottom: 20px;
            right: 20px;
            opacity: 0.05;
            font-size: 8rem;
            font-weight: bold;
            color: white;
            pointer-events: none;
            transform: rotate(-15deg);
            z-index: 0;
            font-family: 'Montserrat', sans-serif;
        }

        .back-to-top {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            box-shadow: 0 5px 20px rgba(0,0,0,0.2);
            opacity: 0;
            transition: all 0.3s ease;
            z-index: 100;
        }

        .back-to-top.visible {
            opacity: 1;
        }

        @media (max-width: 768px) {
            .container {
                padding: 1rem;
            }

            header {
                padding: 3rem 1rem;
            }

            h1 {
                font-size: 2.2rem;
            }

            body::before {
                font-size: 60px;
            }

            .toc-list {
                grid-template-columns: 1fr;
            }

            .section {
                padding: 1.5rem;
            }
        }

        /* Animation for section entrance */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .section {
            animation: fadeInUp 0.6s ease-out forwards;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Linear Algebra</h1>
            <p class="subtitle">Matrices & Determinants</p>
            <div class="gate-banner">
                <strong>Join TestUrSelf for your GATE MT & XE Prep</strong> - Master these concepts with our comprehensive study materials and practice tests!
            </div>
        </div>
    </header>

    <div class="container">
        <div class="toc-container">
            <h2 class="toc-title"><i class="fas fa-list-ul"></i> Table of Contents</h2>
            <ul class="toc-list">
                <li class="toc-item"><a href="#matrices" class="toc-link">1. Matrices Fundamentals</a></li>
                <li class="toc-item"><a href="#operations" class="toc-link">2. Matrix Operations</a></li>
                <li class="toc-item"><a href="#types" class="toc-link">3. Special Matrix Types</a></li>
                <li class="toc-item"><a href="#determinants" class="toc-link">4. Determinants</a></li>
                <li class="toc-item"><a href="#properties" class="toc-link">5. Properties of Determinants</a></li>
                <li class="toc-item"><a href="#applications" class="toc-link">6. Applications</a></li>
                <li class="toc-item"><a href="#quiz" class="toc-link">7. Practice Quiz</a></li>
            </ul>
        </div>

        <!-- Previous sections remain unchanged (matrices, operations, types, determinants, properties, applications) -->
        <!-- ... -->
        <section id="matrices" class="section">
            <h2>1. Matrices Fundamentals</h2>
            <p>A matrix is a rectangular array of numbers arranged in rows and columns. Matrices are fundamental objects in linear algebra and have wide applications in mathematics, physics, engineering, and computer science.</p>
            
            <div class="equation">
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
            
            <div class="example">
                <div class="example-title"><i class="fas fa-lightbulb"></i> Example: 2×3 Matrix</div>
                <p>Consider matrix B:</p>
                <div class="equation">
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
            
            <div class="equation large">
                $$ (A + B)_{ij} = A_{ij} + B_{ij} $$
            </div>
            
            <div class="example">
                <div class="example-title"><i class="fas fa-lightbulb"></i> Example</div>
                <div class="equation">
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
            
            <div class="equation large">
                $$ (cA)_{ij} = c \cdot A_{ij} $$
            </div>
            
            <h3>Matrix Multiplication</h3>
            <p>For matrix multiplication AB, the number of columns in A must equal the number of rows in B.</p>
            
            <div class="equation large">
                $$ (AB)_{ij} = \sum_{k=1}^{n} A_{ik} B_{kj} $$
            </div>
            
            <div class="example">
                <div class="example-title"><i class="fas fa-lightbulb"></i> Example</div>
                <div class="equation">
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
            
            <div class="properties">
                <div class="property-card">
                    <h3 class="property-title">Square Matrix</h3>
                    <p>Number of rows equals number of columns (n × n)</p>
                    <div class="equation">
                        $$ A = \begin{bmatrix}
                        a & b \\
                        c & d
                        \end{bmatrix} $$
                    </div>
                </div>
                
                <div class="property-card">
                    <h3 class="property-title">Identity Matrix</h3>
                    <p>Diagonal elements are 1, others are 0</p>
                    <div class="equation">
                        $$ I_3 = \begin{bmatrix}
                        1 & 0 & 0 \\
                        0 & 1 & 0 \\
                        0 & 0 & 1
                        \end{bmatrix} $$
                    </div>
                </div>
                
                <div class="property-card">
                    <h3 class="property-title">Diagonal Matrix</h3>
                    <p>Non-diagonal elements are zero</p>
                    <div class="equation">
                        $$ D = \begin{bmatrix}
                        a & 0 & 0 \\
                        0 & b & 0 \\
                        0 & 0 & c
                        \end{bmatrix} $$
                    </div>
                </div>
                
                <div class="property-card">
                    <h3 class="property-title">Symmetric Matrix</h3>
                    <p>A = A<sup>T</sup> (equal to its transpose)</p>
                    <div class="equation">
                        $$ S = \begin{bmatrix}
                        1 & 2 & 3 \\
                        2 & 4 & 5 \\
                        3 & 5 & 6
                        \end{bmatrix} $$
                    </div>
                </div>
            </div>
        </section>

        <section id="determinants" class="section">
            <h2>4. Determinants</h2>
            <p>The determinant is a scalar value that can be computed from a square matrix and encodes important properties of the matrix.</p>
            
            <h3>2×2 Determinant</h3>
            <div class="equation large">
                $$ \det \begin{bmatrix}
                a & b \\
                c & d
                \end{bmatrix} = ad - bc $$
            </div>
            
            <h3>3×3 Determinant (Sarrus Rule)</h3>
            <div class="equation large">
                $$ \det \begin{bmatrix}
                a & b & c \\
                d & e & f \\
                g & h & i
                \end{bmatrix} = aei + bfg + cdh - ceg - bdi - afh $$
            </div>
            
            <div class="example">
                <div class="example-title"><i class="fas fa-lightbulb"></i> Example</div>
                <div class="equation">
                    $$ \det \begin{bmatrix}
                    1 & 2 & 3 \\
                    4 & 5 & 6 \\
                    7 & 8 & 9
                    \end{bmatrix} = (1×5×9) + (2×6×7) + (3×4×8) - (3×5×7) - (2×4×9) - (1×6×8) $$
                    $$ = 45 + 84 + 96 - 105 - 72 - 48 = 0 $$
                </div>
            </div>
            
            <h3>General n×n Determinant (Laplace Expansion)</h3>
            <div class="equation">
                $$ \det(A) = \sum_{j=1}^{n} (-1)^{i+j} a_{ij} \det(A_{ij}) $$
            </div>
            <p>where A<sub>ij</sub> is the submatrix obtained by removing the i-th row and j-th column.</p>
        </section>

        <section id="properties" class="section">
            <h2>5. Properties of Determinants</h2>
            
            <div class="properties">
                <div class="property-card">
                    <h3 class="property-title">Determinant of Identity</h3>
                    <div class="equation">
                        $$ \det(I) = 1 $$
                    </div>
                </div>
                
                <div class="property-card">
                    <h3 class="property-title">Triangular Matrix</h3>
                    <div class="equation">
                        $$ \det \begin{bmatrix}
                        a & b \\
                        0 & d
                        \end{bmatrix} = ad $$
                    </div>
                </div>
                
                <div class="property-card">
                    <h3 class="property-title">Product of Matrices</h3>
                    <div class="equation">
                        $$ \det(AB) = \det(A)\det(B) $$
                    </div>
                </div>
                
                <div class="property-card">
                    <h3 class="property-title">Transpose Property</h3>
                    <div class="equation">
                        $$ \det(A^T) = \det(A) $$
                    </div>
                </div>
                
                <div class="property-card">
                    <h3 class="property-title">Scalar Multiplication</h3>
                    <div class="equation">
                        $$ \det(cA) = c^n \det(A) $$
                    </div>
                </div>
                
                <div class="property-card">
                    <h3 class="property-title">Inverse Matrix</h3>
                    <div class="equation">
                        $$ \det(A^{-1}) = \frac{1}{\det(A)} $$
                    </div>
                </div>
            </div>
        </section>

        <section id="applications" class="section">
            <h2>6. Applications</h2>
            
            <h3>Solving Linear Systems (Cramer's Rule)</h3>
            <p>For a system Ax = b, if A is invertible:</p>
            <div class="equation">
                $$ x_i = \frac{\det(A_i)}{\det(A)} $$
            </div>
            <p>where A<sub>i</sub> is A with the i-th column replaced by b.</p>
            
            <h3>Area/Volume Calculation</h3>
            <p>The absolute value of the determinant gives the scaling factor of the linear transformation described by the matrix.</p>
            <div class="equation">
                $$ \text{Area} = \left| \det \begin{bmatrix}
                a & c \\
                b & d
                \end{bmatrix} \right| $$
            </div>
            
            <h3>Eigenvalues</h3>
            <p>The determinant is used in finding eigenvalues:</p>
            <div class="equation">
                $$ \det(A - \lambda I) = 0 $$
            </div>
        </section>
    </div>

        <section id="quiz" class="quiz-section">
            <h2 class="quiz-title"><i class="fas fa-question-circle"></i> Practice Quiz</h2>
            <p>Test your understanding with these GATE-style multiple choice questions:</p>
            
            <div class="quiz-question">
                <div class="question-text">1. What is the determinant of the following 2×2 matrix?
                    $$ \begin{bmatrix} 3 & 4 \\ 1 & 2 \end{bmatrix} $$
                </div>
                <div class="options">
                    <div class="option">
                        <input type="radio" id="q1a" name="q1" value="a">
                        <label for="q1a">2</label>
                    </div>
                    <div class="option">
                        <input type="radio" id="q1b" name="q1" value="b">
                        <label for="q1b">5</label>
                    </div>
                    <div class="option">
                        <input type="radio" id="q1c" name="q1" value="c">
                        <label for="q1c">10</label>
                    </div>
                    <div class="option">
                        <input type="radio" id="q1d" name="q1" value="d">
                        <label for="q1d">-2</label>
                    </div>
                </div>
                <div class="feedback correct" id="feedback1">
                    <strong>Correct!</strong> The determinant is calculated as (3×2) - (4×1) = 6 - 4 = 2.
                </div>
                <div class="feedback incorrect" id="feedback1-wrong">
                    <strong>Incorrect.</strong> Remember the formula for 2×2 determinant is ad - bc.
                </div>
            </div>
            
            <div class="quiz-question">
                <div class="question-text">2. Which of the following is NOT a property of determinants?</div>
                <div class="options">
                    <div class="option">
                        <input type="radio" id="q2a" name="q2" value="a">
                        <label for="q2a">det(AB) = det(A)det(B)</label>
                    </div>
                    <div class="option">
                        <input type="radio" id="q2b" name="q2" value="b">
                        <label for="q2b">det(A+B) = det(A) + det(B)</label>
                    </div>
                    <div class="option">
                        <input type="radio" id="q2c" name="q2" value="c">
                        <label for="q2c">det(A<sup>T</sup>) = det(A)</label>
                    </div>
                    <div class="option">
                        <input type="radio" id="q2d" name="q2" value="d">
                        <label for="q2d">det(cA) = c<sup>n</sup>det(A) for n×n matrix A</label>
                    </div>
                </div>
                <div class="feedback correct" id="feedback2">
                    <strong>Correct!</strong> Determinant of sum is not equal to sum of determinants.
                </div>
                <div class="feedback incorrect" id="feedback2-wrong">
                    <strong>Incorrect.</strong> Review the properties of determinants - they are multiplicative but not additive.
                </div>
            </div>
            
            <div class="quiz-question">
                <div class="question-text">3. For a 3×3 matrix A with det(A) = 5, what is det(2A)?</div>
                <div class="options">
                    <div class="option">
                        <input type="radio" id="q3a" name="q3" value="a">
                        <label for="q3a">10</label>
                    </div>
                    <div class="option">
                        <input type="radio" id="q3b" name="q3" value="b">
                        <label for="q3b">40</label>
                    </div>
                    <div class="option">
                        <input type="radio" id="q3c" name="q3" value="c">
                        <label for="q3c">5</label>
                    </div>
                    <div class="option">
                        <input type="radio" id="q3d" name="q3" value="d">
                        <label for="q3d">2.5</label>
                    </div>
                </div>
                <div class="feedback correct" id="feedback3">
                    <strong>Correct!</strong> For n×n matrix, det(kA) = k<sup>n</sup>det(A). Here 2<sup>3</sup>×5 = 8×5 = 40.
                </div>
                <div class="feedback incorrect" id="feedback3-wrong">
                    <strong>Incorrect.</strong> Remember the scalar multiplication property: det(kA) = k<sup>n</sup>det(A) for n×n matrix.
                </div>
            </div>
            
            <div class="quiz-question">
                <div class="question-text">4. What is the determinant of the identity matrix I<sub>4</sub>?</div>
                <div class="options">
                    <div class="option">
                        <input type="radio" id="q4a" name="q4" value="a">
                        <label for="q4a">0</label>
                    </div>
                    <div class="option">
                        <input type="radio" id="q4b" name="q4" value="b">
                        <label for="q4b">1</label>
                    </div>
                    <div class="option">
                        <input type="radio" id="q4c" name="q4" value="c">
                        <label for="q4c">4</label>
                    </div>
                    <div class="option">
                        <input type="radio" id="q4d" name="q4" value="d">
                        <label for="q4d">Undefined</label>
                    </div>
                </div>
                <div class="feedback correct" id="feedback4">
                    <strong>Correct!</strong> The determinant of any identity matrix is always 1.
                </div>
                <div class="feedback incorrect" id="feedback4-wrong">
                    <strong>Incorrect.</strong> The determinant of identity matrix is always 1 regardless of size.
                </div>
            
            <button class="submit-btn" id="submitQuiz">Submit Answers</button>
            <div class="results" id="quizResults"></div>
        </section>
    </div>
 </div>
    <a href="#" class="back-to-top" id="backToTop"><i class="fas fa-arrow-up"></i></a>

    <footer>
        <div class="container">
            <p>&copy; <span id="current-year"></span> TestUrSelf | GATE MT & XE Preparation</p>
            <p>Master linear algebra and other key topics with our comprehensive study materials!</p>
        </div>
        <div class="footer-watermark">TestUrSelf</div>
    </footer>

    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
    
    <script>
        // Set current year in footer
        document.getElementById('current-year').textContent = new Date().getFullYear();
        
        // Back to top button
        const backToTop = document.getElementById('backToTop');
        
        window.addEventListener('scroll', () => {
            if (window.pageYOffset > 300) {
                backToTop.classList.add('visible');
            } else {
                backToTop.classList.remove('visible');
            }
        });
        
        backToTop.addEventListener('click', (e) => {
            e.preventDefault();
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });
        
        // Smooth scrolling for TOC links
        document.querySelectorAll('.toc-link').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Quiz functionality
        const quizForm = document.getElementById('quizForm');
        const submitBtn = document.getElementById('submitQuiz');
        const resultsDiv = document.getElementById('quizResults');
        
        const correctAnswers = {
            q1: 'a',
            q2: 'b',
            q3: 'b',
            q4: 'b'
        };
        
        submitBtn.addEventListener('click', () => {
            let score = 0;
            const totalQuestions = Object.keys(correctAnswers).length;
            
            // Check each question
            for (const question in correctAnswers) {
                const selectedOption = document.querySelector(`input[name="${question}"]:checked`);
                
                if (selectedOption) {
                    // Hide all feedback for this question
                    document.querySelectorAll(`[id^="feedback${question.slice(1)}"]`).forEach(el => {
                        el.style.display = 'none';
                    });
                    
                    if (selectedOption.value === correctAnswers[question]) {
                        score++;
                        document.getElementById(`feedback${question.slice(1)}`).style.display = 'block';
                    } else {
                        document.getElementById(`feedback${question.slice(1)}-wrong`).style.display = 'block';
                    }
                }
            }
            
            // Show results
            resultsDiv.style.display = 'block';
            resultsDiv.innerHTML = `
                <p>You scored ${score} out of ${totalQuestions}</p>
                <p>${score >= totalQuestions/2 ? 'Great job!' : 'Keep practicing!'} For more practice questions, join <strong>TestUrSelf</strong> GATE prep program!</p>
            `;
            
            // Scroll to results
            resultsDiv.scrollIntoView({ behavior: 'smooth' });
        });
        
        // Animation for sections when they come into view
        const sections = document.querySelectorAll('.section');
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = 1;
                }
            });
        }, { threshold: 0.1 });
        
        sections.forEach(section => {
            section.style.opacity = 0;
            observer.observe(section);
        });
    </script>
</body>
</html>
