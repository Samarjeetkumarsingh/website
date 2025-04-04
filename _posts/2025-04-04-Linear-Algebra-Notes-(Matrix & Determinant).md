<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Linear Algebra: Matrices & Determinants | TestUrSelf</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #1565C0;
            --secondary: #00897B;
            --accent: #6A1B9A;
            --text: #212121;
            --light: #E3F2FD;
            --dark: #0D47A1;
            --highlight: #FFC107;
            --success: #388E3C;
            --error: #D32F2F;
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
            background: linear-gradient(135deg, #E3F2FD 0%, #BBDEFB 50%, #E3F2F 100%);
            background-attachment: fixed;
            background-size: 200% 200%;
            animation: gradientBG 15s ease infinite;
            position: relative;
            min-height: 100vh;
        }

        @keyframes gradientBG {
            0% {background-position: 0% 50%;}
            50% {background-position: 100% 50%;}
            100% {background-position: 0% 50%;}
        }

        /* Watermark */
        body::after {
            content: "TestUrSelf";
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-30deg);
            font-size: 120px;
            font-weight: bold;
            color: rgba(21, 101, 192, 0.08);
            z-index: -1;
            pointer-events: none;
            white-space: nowrap;
            text-transform: uppercase;
            letter-spacing: 15px;
            width: 100%;
            text-align: center;
        }

        /* Container with max-width like original */
        .main-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
        }

        header {
            background: linear-gradient(135deg, var(--primary), var(--dark));
            color: white;
            padding: 3rem;
            text-align: center;
            border-radius: 8px;
            margin-bottom: 2rem;
            box-shadow: 0 8px 25px rgba(0,0,0,0.2);
            position: relative;
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
            font-size: 2.5rem;
            font-weight: 900;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            letter-spacing: 1px;
        }

        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
            font-weight: 400;
        }

        /* Table of Contents - Sticky like original */
        .toc-container {
            position: sticky;
            top: 20px;
            z-index: 10;
            margin-bottom: 2rem;
            background: linear-gradient(135deg, #ffffff, #f5f5f5);
            border-radius: 12px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            overflow: hidden;
        }

        .toc-header {
            background: linear-gradient(135deg, var(--primary), var(--dark));
            color: white;
            padding: 1.5rem;
            font-size: 1.5rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .toc {
            padding: 1.5rem;
            max-height: 80vh;
            overflow-y: auto;
        }

        .toc-list {
            list-style: none;
            padding: 0;
            margin: 0;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 12px;
        }

        .toc-item {
            margin-bottom: 0.5rem;
            transition: all 0.3s ease;
        }

        .toc-link {
            display: flex;
            align-items: center;
            padding: 0.8rem 1.2rem;
            background-color: var(--light);
            color: var(--dark);
            text-decoration: none;
            border-radius: 8px;
            transition: all 0.3s ease;
            font-weight: 500;
            border-left: 4px solid var(--primary);
            gap: 10px;
        }

        .toc-link:hover {
            background-color: rgba(21, 101, 192, 0.1);
            transform: translateX(8px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }

        /* Section styling - matches original */
        .section {
            background-color: white;
            border-radius: 12px;
            padding: 2.5rem;
            margin-bottom: 3rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
            transition: all 0.3s ease;
            border: 1px solid rgba(0,0,0,0.05);
        }

        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }

        h2 {
            color: var(--primary);
            border-bottom: 4px solid var(--highlight);
            padding-bottom: 0.8rem;
            margin-top: 3rem;
            font-size: 2.2rem;
            background: linear-gradient(to right, transparent, var(--light), transparent);
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
            background: linear-gradient(to right, transparent, var(--highlight), transparent);
        }

        /* Keep all your other styles for equations, quiz, etc. */

        /* Footer with watermark like original */
        footer {
            background: linear-gradient(135deg, var(--dark), #0D47A1);
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

        @media (max-width: 768px) {
            .main-container {
                padding: 10px;
            }
            
            body::after {
                font-size: 60px;
            }
            
            header {
                padding: 2rem 1rem;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .toc-list {
                grid-template-columns: 1fr;
            }
            
            .toc-container {
                position: static;
            }
        }
    </style>
</head>
<body>
    <div class="main-container">
        <header>
            <h1>Linear Algebra</h1>
            <p class="subtitle">Matrices & Determinants</p>
            <div class="gate-banner">
                <strong>Join TestUrSelf for your GATE MT & XE Prep</strong> - Master these concepts with our comprehensive study materials!
            </div>
        </header>

        <div class="toc-container">
            <div class="toc-header">
                <i class="fas fa-list-ul"></i>
                <span>Table of Contents</span>
            </div>
            <div class="toc">
                <ul class="toc-list">
                    <li class="toc-item"><a href="#matrices" class="toc-link"><i class="fas fa-matrix"></i> Matrices</a></li>
                    <li class="toc-item"><a href="#determinants" class="toc-link"><i class="fas fa-calculator"></i> Determinants</a></li>
                    <li class="toc-item"><a href="#quiz" class="toc-link"><i class="fas fa-question-circle"></i> Practice Quiz</a></li>
                </ul>
            </div>
        </div>

        <!-- Your content sections here -->
        <section id="matrices" class="section">
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

        <section id="quiz" class="section">
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
        <div class="main-container">
            <p>&copy; <span id="current-year"></span> TestUrSelf | GATE Preparation</p>
            <p>Master linear algebra and other key topics with our comprehensive study materials!</p>
        </div>
        <div class="footer-watermark">TestUrSelf</div>
    </footer>

    <!-- Your scripts -->
</body>
</html>
