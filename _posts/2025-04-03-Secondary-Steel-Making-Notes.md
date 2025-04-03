<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Steel Making & Casting - TestUrSelf</title>
    <style>
        :root {
            --primary-color: #D50000;
            --secondary-color: #FF6D00;
            --accent-color: #BF360C;
            --light-color: #FFEBEE;
            --dark-color: #B71C1C;
            --text-color: #212121;
            --highlight-color: #FFAB00;
            --success-color: #388E3C;
            --error-color: #D32F2F;
            --ladle-color: #5D4037;
            --casting-color: #00695C;
            --stainless-color: #37474F;
            --tundish-color: #4527A0;
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
            background: linear-gradient(135deg, #FFF3E0 0%, #FFE0B2 50%, #FFF3E0 100%);
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
            color: rgba(213, 0, 0, 0.05);
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
            background-color: rgba(213, 0, 0, 0.1);
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
            box-shadow: 0 4px 8px rgba(213, 0, 0, 0.3);
        }
        
        .show-answer-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(213, 0, 0, 0.4);
        }
        
        /* Content Boxes */
        .key-point {
            background: linear-gradient(to right, #FFF8E1, #FFECB3);
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
            background-color: #EFEBE9;
            border-left: 4px solid var(--ladle-color);
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
            background-color: var(--ladle-color);
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
            background: linear-gradient(to bottom right, var(--ladle-color), #3E2723);
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
            border-top: 5px solid var(--ladle-color);
            transition: transform 0.3s ease;
        }
        
        .method-card.casting {
            border-top-color: var(--casting-color);
        }
        
        .method-card.stainless {
            border-top-color: var(--stainless-color);
        }
        
        .method-card.tundish {
            border-top-color: var(--tundish-color);
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
        
        /* Interactive Diagram */
        .interactive-diagram {
            background-color: white;
            border-radius: 10px;
            padding: 1.5rem;
            margin: 2rem 0;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            text-align: center;
        }
        
        .diagram-element {
            display: inline-block;
            padding: 1rem;
            margin: 0.5rem;
            background-color: var(--light-color);
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }
        
        .diagram-element:hover {
            transform: scale(1.05);
            border-color: var(--highlight-color);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .diagram-element.active {
            background-color: var(--highlight-color);
            color: white;
            font-weight: bold;
        }
        
        .diagram-info {
            margin-top: 1rem;
            padding: 1rem;
            background-color: #f5f5f5;
            border-radius: 6px;
            display: none;
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
</head>
<body>
    <header>
        <h1>Secondary Steel Making & Continuous Casting</h1>
        <p>Master the processes that refine molten steel and transform it into solid products</p>
    </header>

    <div class="toc-container">
        <div class="toc">
            <h2>Table of Contents</h2>
            <ul>
                <li><a href="#secondary-steel">1. Secondary Steel Making</a></li>
                <li><a href="#stainless-steel">2. Stainless Steel Basics</a></li>
                <li><a href="#continuous-casting">3. Continuous Casting</a></li>
                <li><a href="#interactive">4. Process Diagram</a></li>
                <li><a href="#quiz">5. Knowledge Test</a></li>
            </ul>
        </div>
    </div>

    <div class="section" id="secondary-steel">
        <h2>1. Secondary Steel Making: Ladle Processes</h2>
        <p>Secondary steel making refines molten steel through various ladle treatments to achieve precise chemical composition, temperature control, and cleanliness.</p>
        
        <h3>1.1 Deoxidation</h3>
        <div class="process-steps">
            <div class="process-step">
                <h4>Purpose</h4>
                <p>Remove dissolved oxygen to prevent gas porosity and improve mechanical properties</p>
            </div>
            
            <div class="process-step">
                <h4>Methods</h4>
                <p>
                    <strong>Precipitation Deoxidation:</strong> Add elements with higher oxygen affinity than iron
                    <ul>
                        <li>Aluminum (most common): 0.02-0.06%</li>
                        <li>Silicon: Often used with manganese (Si-Mn)</li>
                        <li>Calcium: For inclusion modification</li>
                    </ul>
                </p>
                <p><strong>Vacuum Deoxidation:</strong> Carbon deoxidation under reduced pressure</p>
            </div>
            
            <div class="process-step">
                <h4>Reactions</h4>
                <div class="formula-box">
                    2[Al] + 3[O] → Al<sub>2</sub>O<sub>3</sub>(s) ΔG° = -1,200,000 + 386T J/mol<br>
                    [Si] + 2[O] → SiO<sub>2</sub>(s) ΔG° = -576,000 + 218T J/mol<br>
                    [C] + [O] → CO(g) ΔG° = -22,400 - 39.6T J/mol
                </div>
            </div>
        </div>
        
        <h3>1.2 Argon Stirring</h3>
        <table>
            <tr>
                <th>Parameter</th>
                <th>Porous Plug</th>
                <th>Top Lance</th>
                <th>Induction Stirring</th>
            </tr>
            <tr>
                <td>Gas Flow Rate</td>
                <td>50-200 NL/min</td>
                <td>100-500 NL/min</td>
                <td>N/A</td>
            </tr>
            <tr>
                <td>Stirring Energy</td>
                <td>50-200 W/ton</td>
                <td>100-500 W/ton</td>
                <td>100-400 W/ton</td>
            </tr>
            <tr>
                <td>Mixing Time</td>
                <td>2-5 min</td>
                <td>1-3 min</td>
                <td>3-8 min</td>
            </tr>
            <tr>
                <td>Applications</td>
                <td>Homogenization</td>
                <td>Slag-metal reaction</td>
                <td>Clean steel production</td>
            </tr>
        </table>
        
        <div class="key-point">
            <h4>Benefits of Argon Stirring</h4>
            <ul>
                <li>Homogenizes temperature and composition (ΔT < 5°C)</li>
                <li>Promotes inclusion floatation (removes 50-70% of inclusions)</li>
                <li>Accelerates slag-metal reactions</li>
                <li>Reduces hydrogen and nitrogen content</li>
            </ul>
        </div>
        
        <h3>1.3 Desulphurization</h3>
        <div class="method-card">
            <p>Reduces sulfur content to <0.005% for critical applications:</p>
            <ul>
                <li><strong>Slag-Metal Reaction:</strong> High basicity slag (CaO/SiO<sub>2</sub> >3) with Al reduction</li>
                <li><strong>Calcium Treatment:</strong> Ca injection (wire or powder) forms CaS</li>
                <li><strong>Optimal Conditions:</strong>
                    <ul>
                        <li>Temperature: 1550-1650°C</li>
                        <li>Oxygen activity: <10ppm</li>
                        <li>Stirring intensity: 100-300 W/ton</li>
                    </ul>
                </li>
            </ul>
            
            <div class="formula-box">
                [S] + (CaO) + [Al] → (CaS) + (Al<sub>2</sub>O<sub>3</sub>)<br>
                K = (a<sub>CaS</sub>·a<sub>Al2O3</sub>)/(a<sub>S</sub>·a<sub>CaO</sub>·a<sub>Al</sub>)
            </div>
        </div>
        
        <h3>1.4 Inclusion Shape Control</h3>
        <div class="process-steps">
            <div class="process-step">
                <h4>Objective</h4>
                <p>Modify harmful alumina and sulfide inclusions into less detrimental forms</p>
            </div>
            
            <div class="process-step">
                <h4>Methods</h4>
                <p>
                    <strong>Calcium Treatment:</strong> Converts Al<sub>2</sub>O<sub>3</sub> to liquid calcium aluminates<br>
                    <strong>Rare Earth Metals:</strong> Form globular oxysulfides<br>
                    <strong>Magnesium:</strong> For sulfide shape control in resulfurized steels
                </p>
            </div>
            
            <div class="process-step">
                <h4>Target Inclusion Types</h4>
                <p>
                    <strong>Soft:</strong> Liquid calcium aluminates (12CaO·7Al<sub>2</sub>O<sub>3</sub>)<br>
                    <strong>Deformable:</strong> MnS in low melting point silicate matrix<br>
                    <strong>Non-deformable:</strong> Avoided (alumina, spinel)
                </p>
            </div>
        </div>
        
        <h3>1.5 Degassing Principles</h3>
        <div class="method-card">
            <h4>Vacuum Degassing Methods</h4>
            <table>
                <tr>
                    <th>Method</th>
                    <th>Vacuum Level</th>
                    <th>Treatment Time</th>
                    <th>H Reduction</th>
                    <th>N Reduction</th>
                </tr>
                <tr>
                    <td>RH (Ruhrstahl-Heraeus)</td>
                    <td>0.1-1 mbar</td>
                    <td>15-25 min</td>
                    <td>60-80%</td>
                    <td>20-40%</td>
                </tr>
                <tr>
                    <td>VD (Vacuum Arc Degassing)</td>
                    <td>0.5-2 mbar</td>
                    <td>20-30 min</td>
                    <td>50-70%</td>
                    <td>15-30%</td>
                </tr>
                <tr>
                    <td>DH (Dortmund-Hörder)</td>
                    <td>0.1-1 mbar</td>
                    <td>10-20 min</td>
                    <td>70-90%</td>
                    <td>25-45%</td>
                </tr>
            </table>
            
            <div class="key-point">
                <h4>Degassing Reactions</h4>
                <div class="formula-box">
                    2[H] → H<sub>2</sub>(g) ΔG° = 364,800 - 104.6T J/mol<br>
                    2[N] → N<sub>2</sub>(g) ΔG° = 864,800 - 157.3T J/mol<br>
                    [C] + [O] → CO(g) ΔG° = -22,400 - 39.6T J/mol
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">What is the primary purpose of argon stirring in ladle metallurgy?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">To increase steel temperature</div>
                <div class="option" onclick="checkAnswer(this, true)">To homogenize composition and promote inclusion removal</div>
                <div class="option" onclick="checkAnswer(this, false)">To reduce carbon content</div>
                <div class="option" onclick="checkAnswer(this, false)">To increase nitrogen pickup</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: To homogenize composition and promote inclusion removal</strong></p>
                    <p>Argon stirring creates a recirculating flow pattern that equalizes temperature and composition throughout the ladle while promoting the floatation of non-metallic inclusions to the slag layer. Typical stirring energies range from 50-500 W/ton.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">Which element is most commonly used for deoxidation in aluminum-killed steels?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Silicon</div>
                <div class="option" onclick="checkAnswer(this, true)">Aluminum</div>
                <div class="option" onclick="checkAnswer(this, false)">Calcium</div>
                <div class="option" onclick="checkAnswer(this, false)">Magnesium</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Aluminum</strong></p>
                    <p>Aluminum is the most powerful common deoxidizer, typically added at 0.02-0.06%. It forms alumina (Al<sub>2</sub>O<sub>3</sub>) inclusions which must be controlled through calcium treatment or flotation.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="stainless-steel">
        <h2>2. Basics of Stainless Steel Manufacturing</h2>
        
        <div class="method-card stainless">
            <h3>2.1 Stainless Steel Types</h3>
            <table>
                <tr>
                    <th>Type</th>
                    <th>Main Alloys</th>
                    <th>Cr (%)</th>
                    <th>Ni (%)</th>
                    <th>Key Properties</th>
                </tr>
                <tr>
                    <td>Ferritic (400 series)</td>
                    <td>Cr, Mo</td>
                    <td>10.5-30</td>
                    <td>0-4</td>
                    <td>Magnetic, moderate corrosion resistance</td>
                </tr>
                <tr>
                    <td>Martensitic (400 series)</td>
                    <td>Cr, C</td>
                    <td>11.5-18</td>
                    <td>0-2</td>
                    <td>Hardenable, high strength</td>
                </tr>
                <tr>
                    <td>Austenitic (300 series)</td>
                    <td>Cr, Ni, Mn</td>
                    <td>16-26</td>
                    <td>6-22</td>
                    <td>Non-magnetic, excellent corrosion resistance</td>
                </tr>
                <tr>
                    <td>Duplex (2205 etc.)</td>
                    <td>Cr, Ni, Mo, N</td>
                    <td>21-26</td>
                    <td>4.5-8</td>
                    <td>High strength, stress corrosion resistance</td>
                </tr>
            </table>
        </div>
        
        <h3>2.2 Production Routes</h3>
        <div class="process-steps">
            <div class="process-step">
                <h4>EAF → AOD Route</h4>
                <p>
                    <strong>Electric Arc Furnace:</strong> Melts scrap and ferroalloys (1600-1650°C)<br>
                    <strong>Argon Oxygen Decarburization:</strong> Key refining step for Cr retention
                </p>
            </div>
            
            <div class="process-step">
                <h4>AOD Process</h4>
                <p>
                    <strong>Stage 1:</strong> High O<sub>2</sub> blowing (Cr oxidation)<br>
                    <strong>Stage 2:</strong> Mixed Ar/O<sub>2</sub> blowing (controlled decarburization)<br>
                    <strong>Stage 3:</strong> Argon stirring (final reduction)
                </p>
                <div class="formula-box">
                    Cr<sub>2</sub>O<sub>3</sub> + 3[C] → 2[Cr] + 3CO(g) ΔG° = 546,000 - 344T J/mol
                </div>
            </div>
            
            <div class="process-step">
                <h4>Alternative Processes</h4>
                <p>
                    <strong>VOD:</strong> Vacuum Oxygen Decarburization for ultra-low carbon grades<br>
                    <strong>CLU:</strong> Creusot-Loire Uddeholm process (similar to AOD)<br>
                    <strong>Converter:</strong> K-OBM-S process with bottom tuyeres
                </p>
            </div>
        </div>
        
        <h3>2.3 Special Considerations</h3>
        <div class="key-point">
            <ul>
                <li><strong>Chromium Recovery:</strong> Must maintain Cr >10.5% while reducing carbon</li>
                <li><strong>Nitrogen Control:</strong> Added in duplex steels (0.1-0.3%), removed in others</li>
                <li><strong>Low Carbon:</strong> <0.03% C prevents sensitization (Cr carbide precipitation)</li>
                <li><strong>Slag Chemistry:</strong> CaO-SiO<sub>2</sub>-MgO-Al<sub>2</sub>O<sub>3</sub> system with basicity 1.5-2.5</li>
            </ul>
        </div>
        
        <div class="mcq">
            <div class="question">What is the primary purpose of the AOD process in stainless steel production?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">To increase chromium content</div>
                <div class="option" onclick="checkAnswer(this, true)">To decarburize while minimizing chromium oxidation</div>
                <div class="option" onclick="checkAnswer(this, false)">To remove sulfur completely</div>
                <div class="option" onclick="checkAnswer(this, false)">To increase nitrogen content</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: To decarburize while minimizing chromium oxidation</strong></p>
                    <p>The AOD (Argon Oxygen Decarburization) process uses argon dilution to lower CO partial pressure, allowing carbon removal at lower temperatures without excessive chromium oxidation. This enables production of low-carbon stainless steels while maintaining high chromium content.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="continuous-casting">
        <h2>3. Continuous Casting Processes</h2>
        
        <div class="method-card casting">
            <h3>3.1 Fluid Flow in Tundish</h3>
            <p>Tundish serves as a buffer and refining vessel between ladle and mold:</p>
            <ul>
                <li><strong>Flow Control:</strong> Impact pads, dams, weirs to optimize flow patterns</li>
                <li><strong>Residence Time:</strong> Typically 5-10 minutes (minimum 3 min for inclusion floatation)</li>
                <li><strong>Flow Models:</strong>
                    <ul>
                        <li>Plug flow (ideal)</li>
                        <li>Mixed flow (actual)</li>
                        <li>Dead zones (undesirable)</li>
                    </ul>
                </li>
            </ul>
            
            <div class="formula-box">
                Residence Time Distribution (RTD): E(t) = C(t)/∫C(t)dt<br>
                Mean Residence Time: τ = V/Q (V = volume, Q = flow rate)
            </div>
        </div>
        
        <h3>3.2 Fluid Flow in Mold</h3>
        <div class="process-steps">
            <div class="process-step">
                <h4>Meniscus Flow</h4>
                <p>
                    <strong>Importance:</strong> Affects slag entrapment and surface quality<br>
                    <strong>Control:</strong> Submerged Entry Nozzle (SEN) design and casting speed
                </p>
            </div>
            
            <div class="process-step">
                <h4>Flow Patterns</h4>
                <p>
                    <strong>Double Roll:</strong> Standard for slabs (2 recirculation zones)<br>
                    <strong>Single Roll:</strong> For high-speed casting<br>
                    <strong>Unstable Flow:</strong> Causes level fluctuations (>±3mm problematic)
                </p>
            </div>
            
            <div class="process-step">
                <h4>Electromagnetic Control</h4>
                <p>
                    <strong>EMBr:</strong> Electromagnetic braking reduces jet velocity<br>
                    <strong>EMLS:</strong> Level stabilization<br>
                    <strong>EMS:</strong> Stirring for equiaxed zone enlargement
                </p>
            </div>
        </div>
        
        <h3>3.3 Heat Transfer in Mold</h3>
        <table>
            <tr>
                <th>Mechanism</th>
                <th>Heat Flux (MW/m²)</th>
                <th>Importance</th>
            </tr>
            <tr>
                <td>Initial Solidification</td>
                <td>2.0-3.5</td>
                <td>Shell formation (10-30mm)</td>
            </tr>
            <tr>
                <td>Steady-State</td>
                <td>1.0-2.0</td>
                <td>Shell growth</td>
            </tr>
            <tr>
                <td>Air Gap Formation</td>
                <td>0.5-1.5</td>
                <td>Reduces heat transfer</td>
            </tr>
        </table>
        
        <div class="key-point">
            <h4>Heat Transfer Equation</h4>
            <div class="formula-box">
                q = h × (T<sub>steel</sub> - T<sub>water</sub>)<br>
                h = 1/(1/h<sub>gap</sub> + d<sub>cu</sub>/k<sub>cu</sub> + 1/h<sub>water</sub>)
            </div>
            <p>Where h<sub>gap</sub> ≈ 1000-3000 W/m²K, h<sub>water</sub> ≈ 30,000-50,000 W/m²K</p>
        </div>
        
        <h3>3.4 Segregation</h3>
        <div class="method-card">
            <h4>Types of Segregation</h4>
            <ul>
                <li><strong>Microsegregation:</strong> Within dendrites (C, P, S enriched in interdendritic regions)</li>
                <li><strong>Macrosegregation:</strong> Across product (centerline segregation of C, S, P)</li>
                <li><strong>Inverse Segregation:</strong> Near surface (enriched in alloying elements)</li>
            </ul>
            
            <div class="formula-box">
                Segregation Ratio: SR = C<sub>max</sub>/C<sub>0</sub><br>
                Typical SR values: C (1.5-3), S (2-5), P (1.5-3)
            </div>
        </div>
        
        <h3>3.5 Inclusion Control</h3>
        <div class="process-steps">
            <div class="process-step">
                <h4>Sources</h4>
                <p>
                    <strong>Endogenous:</strong> Deoxidation products (Al<sub>2</sub>O<sub>3</sub>, SiO<sub>2</sub>, etc.)<br>
                    <strong>Exogenous:</strong> Refractory erosion, slag entrapment
                </p>
            </div>
            
            <div class="process-step">
                <h4>Control Methods</h4>
                <p>
                    <strong>Ladle Treatment:</strong> Argon stirring, calcium treatment<br>
                    <strong>Tundish:</strong> Flow control, ceramic filters<br>
                    <strong>Mold:</strong> SEN design, mold powder absorption
                </p>
            </div>
            
            <div class="process-step">
                <h4>Target Levels</h4>
                <p>
                    <strong>Clean Steels:</strong> <10ppm total oxygen<br>
                    <strong>Ultra-Clean Steels:</strong> <5ppm total oxygen
                </p>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">What is the primary purpose of the tundish in continuous casting?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">To superheat the steel</div>
                <div class="option" onclick="checkAnswer(this, true)">To ensure steady flow to mold and allow inclusion floatation</div>
                <div class="option" onclick="checkAnswer(this, false)">To reduce carbon content</div>
                <div class="option" onclick="checkAnswer(this, false)">To add alloying elements</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: To ensure steady flow to mold and allow inclusion floatation</strong></p>
                    <p>The tundish maintains constant metal head pressure for even flow to the mold while providing residence time (5-10 min) for inclusions to float out. Proper tundish design with flow modifiers can remove 30-50% of remaining inclusions.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">Which factor most significantly affects heat transfer in the mold during continuous casting?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Steel carbon content</div>
                <div class="option" onclick="checkAnswer(this, true)">Air gap formation between shell and mold</div>
                <div class="option" onclick="checkAnswer(this, false)">Mold material</div>
                <div class="option" onclick="checkAnswer(this, false)">Tundish temperature</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Air gap formation between shell and mold</strong></p>
                    <p>As the shell solidifies and contracts, an air gap forms which dramatically reduces heat transfer (h<sub>gap</sub> ≈ 1000-3000 W/m²K vs. h<sub>water</sub> ≈ 30,000-50,000 W/m²K). This is the dominant resistance in the heat transfer path.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="interactive">
        <h2>4. Interactive Process Diagram</h2>
        <div class="interactive-diagram">
            <div class="diagram-element" onclick="showDiagramInfo(this, 'ladle')">
                <i class="fas fa-flask"></i> Ladle Treatment
            </div>
            <div class="diagram-element" onclick="showDiagramInfo(this, 'tundish')">
                <i class="fas fa-tint"></i> Tundish
            </div>
            <div class="diagram-element" onclick="showDiagramInfo(this, 'mold')">
                <i class="fas fa-border-style"></i> Mold
            </div>
            <div class="diagram-element" onclick="showDiagramInfo(this, 'secondary')">
                <i class="fas fa-snowflake"></i> Secondary Cooling
            </div>
            <div class="diagram-element" onclick="showDiagramInfo(this, 'cutting')">
                <i class="fas fa-cut"></i> Cutting
            </div>
            
            <div class="diagram-info" id="ladle-info">
                <h4>Ladle Treatment</h4>
                <p>Key processes:</p>
                <ul>
                    <li>Temperature homogenization</li>
                    <li>Chemical composition adjustment</li>
                    <li>Inclusion removal</li>
                    <li>Degassing (if required)</li>
                </ul>
            </div>
            
            <div class="diagram-info" id="tundish-info">
                <h4>Tundish</h4>
                <p>Functions:</p>
                <ul>
                    <li>Steady metal flow to mold</li>
                    <li>Inclusion floatation</li>
                    <li>Last chance for composition adjustment</li>
                    <li>Flow control with dams/weirs</li>
                </ul>
            </div>
            
            <div class="diagram-info" id="mold-info">
                <h4>Mold</h4>
                <p>Critical parameters:</p>
                <ul>
                    <li>Heat flux: 1-3 MW/m²</li>
                    <li>Meniscus control (±2mm)</li>
                    <li>Oscillation: 100-200 cpm</li>
                    <li>Strand shell thickness: 10-30mm</li>
                </ul>
            </div>
            
            <div class="diagram-info" id="secondary-info">
                <h4>Secondary Cooling</h4>
                <p>Zones:</p>
                <ul>
                    <li>Spray cooling (water/air mist)</li>
                    <li>Target surface temperature</li>
                    <li>Avoid overcooling/reheating</li>
                    <li>Final solidification point control</li>
                </ul>
            </div>
            
            <div class="diagram-info" id="cutting-info">
                <h4>Cutting</h4>
                <p>Methods:</p>
                <ul>
                    <li>Torch cutting (most common)</li>
                    <li>Shearing (for small sections)</li>
                    <li>Sawing (special applications)</li>
                </ul>
            </div>
        </div>
    </div>

    <div class="section" id="quiz">
        <h2>5. Knowledge Test</h2>
        <p>Test your understanding with these interactive questions. Earn 2 points for each correct answer!</p>
        
        <div class="mcq">
            <div class="question">Which degassing method typically achieves the highest hydrogen removal efficiency?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">VD (Vacuum Arc Degassing)</div>
                <div class="option" onclick="checkAnswer(this, true)">RH (Ruhrstahl-Heraeus)</div>
                <div class="option" onclick="checkAnswer(this, false)">Ladle furnace treatment</div>
                <div class="option" onclick="checkAnswer(this, false)">Argon stirring alone</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: RH (Ruhrstahl-Heraeus)</strong></p>
                    <p>The RH process achieves 70-90% hydrogen removal due to its efficient recirculation under high vacuum (0.1-1 mbar), compared to 50-70% for VD and minimal reduction with argon stirring alone.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">What is the primary mechanism for inclusion removal in the tundish?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Chemical dissolution</div>
                <div class="option" onclick="checkAnswer(this, true)">Floatation to the slag layer</div>
                <div class="option" onclick="checkAnswer(this, false)">Filtration through ceramic materials</div>
                <div class="option" onclick="checkAnswer(this, false)">Electromagnetic separation</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Floatation to the slag layer</strong></p>
                    <p>Inclusions are removed in the tundish primarily by Stokes floatation - buoyant forces cause them to rise to the slag layer. Proper tundish design provides sufficient residence time (5-10 min) for this process.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">Which stainless steel type contains both austenite and ferrite phases?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Martensitic</div>
                <div class="option" onclick="checkAnswer(this, true)">Duplex</div>
                <div class="option" onclick="checkAnswer(this, false)">Ferritic</div>
                <div class="option" onclick="checkAnswer(this, false)">Precipitation-hardened</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Duplex</strong></p>
                    <p>Duplex stainless steels have a mixed microstructure of approximately equal parts austenite and ferrite, combining benefits of both phases - strength from ferrite and corrosion resistance from austenite.</p>
                </div>
            </div>
        </div>
    </div>

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
                button.style.background = 'linear-gradient(to right, #B71C1C, #D50000)';
            } else {
                button.innerHTML = '<i class="fas fa-lightbulb"></i> Show Answer';
                button.style.background = 'linear-gradient(to right, var(--primary-color), var(--accent-color))';
            }
        }
        
        // Interactive diagram functionality
        function showDiagramInfo(element, infoId) {
            // Remove active class from all elements
            document.querySelectorAll('.diagram-element').forEach(el => {
                el.classList.remove('active');
            });
            
            // Hide all info boxes
            document.querySelectorAll('.diagram-info').forEach(info => {
                info.style.display = 'none';
            });
            
            // Activate clicked element
            element.classList.add('active');
            
            // Show corresponding info
            document.getElementById(infoId + '-info').style.display = 'block';
        }
        
        // Initialize first diagram element as active
        document.addEventListener('DOMContentLoaded', function() {
            // Animate MCQ options sequentially
            const options = document.querySelectorAll('.option');
            options.forEach((option, index) => {
                setTimeout(() => {
                    option.style.opacity = '1';
                    option.style.transform = 'translateY(0)';
                }, index * 100);
            });
            
            // Activate first diagram element
            if (document.querySelector('.diagram-element')) {
                document.querySelector('.diagram-element').click();
            }
            
            // Add scroll margin to account for fixed header
            document.querySelectorAll('h2').forEach(h2 => {
                h2.style.scrollMarginTop = '120px';
            });
        });
    </script>
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.4.0/dist/confetti.browser.min.js"></script>
</body>
</html>
