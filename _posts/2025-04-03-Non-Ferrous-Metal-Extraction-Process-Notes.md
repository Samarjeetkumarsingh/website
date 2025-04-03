<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Non-Ferrous Metal Extraction - TestUrSelf</title>
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
            --aluminium-color: #E0E0E0;
            --copper-color: #B71C1C;
            --titanium-color: #757575;
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
        
        /* Beautiful Table of Contents */
        .toc-container {
            position: sticky;
            top: 20px;
            z-index: 5;
            margin-bottom: 2rem;
            background: linear-gradient(135deg, #ffffff, #f5f5f5);
            border-radius: 12px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            overflow: hidden;
        }
        
        .toc-header {
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            color: white;
            padding: 1.5rem;
            font-size: 1.5rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .toc-header i {
            font-size: 1.8rem;
        }
        
        .toc {
            padding: 1.5rem;
            max-height: 80vh;
            overflow-y: auto;
        }
        
        .toc-list {
            list-style-type: none;
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
            background-color: var(--light-color);
            color: var(--dark-color);
            text-decoration: none;
            border-radius: 8px;
            transition: all 0.3s ease;
            font-weight: 500;
            border-left: 4px solid var(--primary-color);
            gap: 10px;
        }
        
        .toc-link i {
            font-size: 1.1rem;
            color: var(--primary-color);
        }
        
        .toc-link:hover {
            background-color: rgba(21, 101, 192, 0.1);
            transform: translateX(8px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        /* Beautiful Tables */
        .metal-table {
            width: 100%;
            border-collapse: separate;
            border-spacing: 0;
            margin: 2rem 0;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            border-radius: 12px;
            overflow: hidden;
            background: white;
        }
        
        .metal-table th {
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            color: white;
            padding: 1.2rem;
            text-align: left;
            font-weight: 600;
            position: sticky;
            top: 0;
        }
        
        .metal-table td {
            padding: 1rem;
            border-bottom: 1px solid #e0e0e0;
            vertical-align: middle;
        }
        
        .metal-table tr:nth-child(even) {
            background-color: #f9f9f9;
        }
        
        .metal-table tr:hover {
            background-color: #f0f0f0;
        }
        
        .metal-table tr:last-child td {
            border-bottom: none;
        }
        
        /* Metal-Specific Table Colors */
        .aluminium-table th {
            background: linear-gradient(135deg, #616161, #9E9E9E);
        }
        
        .copper-table th {
            background: linear-gradient(135deg, #B71C1C, #D32F2F);
        }
        
        .titanium-table th {
            background: linear-gradient(135deg, #455A64, #607D8B);
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
            
            .toc-list {
                grid-template-columns: 1fr;
            }
            
            .toc-container {
                position: static;
            }
            
            .toc {
                max-height: none;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700;900&display=swap" rel="stylesheet">
</head>
<body>
    <header>
        <h1>Non-Ferrous Metal Extraction</h1>
        <p>Principles and processes for aluminium, copper and titanium production</p>
    </header>

    <div class="toc-container">
        <div class="toc-header">
            <i class="fas fa-list-ul"></i>
            <span>Table of Contents</span>
        </div>
        <div class="toc">
            <ul class="toc-list">
                <li class="toc-item"><a href="#aluminium" class="toc-link"><i class="fas fa-atom"></i> Aluminium Extraction</a></li>
                <li class="toc-item"><a href="#copper" class="toc-link"><i class="fas fa-coins"></i> Copper Extraction</a></li>
                <li class="toc-item"><a href="#titanium" class="toc-link"><i class="fas fa-shield-alt"></i> Titanium Extraction</a></li>
                <li class="toc-item"><a href="#aluminium-mcqs" class="toc-link"><i class="fas fa-question-circle"></i> Aluminium MCQs</a></li>
                <li class="toc-item"><a href="#copper-mcqs" class="toc-link"><i class="fas fa-question-circle"></i> Copper MCQs</a></li>
                <li class="toc-item"><a href="#titanium-mcqs" class="toc-link"><i class="fas fa-question-circle"></i> Titanium MCQs</a></li>
                <li class="toc-item"><a href="#comparative-mcqs" class="toc-link"><i class="fas fa-balance-scale"></i> Comparative MCQs</a></li>
            </ul>
        </div>
    </div>

    <div class="section" id="aluminium">
        <h2>1. Aluminium Extraction</h2>
        <p>Aluminium is extracted from bauxite ore through the Bayer process followed by the Hall-Héroult electrolytic process.</p>
        
        <h3>1.1 Hall-Héroult Process Components</h3>
        <table class="metal-table aluminium-table">
            <tr>
                <th>Component</th>
                <th>Purpose</th>
                <th>Composition</th>
            </tr>
            <tr>
                <td>Cryolite (Na<sub>3</sub>AlF<sub>6</sub>)</td>
                <td>Electrolyte solvent</td>
                <td>80-85% of bath</td>
            </tr>
            <tr>
                <td>Alumina (Al<sub>2</sub>O<sub>3</sub>)</td>
                <td>Aluminium source</td>
                <td>2-8% dissolved</td>
            </tr>
            <tr>
                <td>Aluminium Fluoride (AlF<sub>3</sub>)</td>
                <td>Lowers melting point</td>
                <td>5-12%</td>
            </tr>
            <tr>
                <td>Calcium Fluoride (CaF<sub>2</sub>)</td>
                <td>Improves conductivity</td>
                <td>3-7%</td>
            </tr>
        </table>
        
        <h3>1.2 Bayer Process Parameters</h3>
        <table class="metal-table aluminium-table">
            <tr>
                <th>Stage</th>
                <th>Temperature</th>
                <th>Pressure</th>
                <th>Time</th>
            </tr>
            <tr>
                <td>Digestion</td>
                <td>150-250°C</td>
                <td>20-30 atm</td>
                <td>1-3 hours</td>
            </tr>
            <tr>
                <td>Precipitation</td>
                <td>50-70°C</td>
                <td>Atmospheric</td>
                <td>24-48 hours</td>
            </tr>
            <tr>
                <td>Calcination</td>
                <td>1000-1200°C</td>
                <td>Atmospheric</td>
                <td>1-2 hours</td>
            </tr>
        </table>
    </div>

    <div class="section" id="copper">
        <h2>2. Copper Extraction</h2>
        <p>Copper is extracted from sulfide ores through pyrometallurgical processes or from oxide ores via hydrometallurgy.</p>
        
        <h3>2.1 Copper Smelting Reactions</h3>
        <table class="metal-table copper-table">
            <tr>
                <th>Stage</th>
                <th>Reaction</th>
                <th>Temperature</th>
            </tr>
            <tr>
                <td>Roasting</td>
                <td>2CuFeS<sub>2</sub> + 5O<sub>2</sub> → 2CuS + 2FeO + 4SO<sub>2</sub></td>
                <td>500-700°C</td>
            </tr>
            <tr>
                <td>Smelting</td>
                <td>2CuS + 3O<sub>2</sub> → 2Cu<sub>2</sub>O + 2SO<sub>2</sub></td>
                <td>1200-1300°C</td>
            </tr>
            <tr>
                <td>Converting</td>
                <td>Cu<sub>2</sub>S + 2Cu<sub>2</sub>O → 6Cu + SO<sub>2</sub></td>
                <td>1150-1250°C</td>
            </tr>
        </table>
        
        <h3>2.2 Hydrometallurgical Parameters</h3>
        <table class="metal-table copper-table">
            <tr>
                <th>Process</th>
                <th>Conditions</th>
                <th>Recovery</th>
            </tr>
            <tr>
                <td>Leaching</td>
                <td>H<sub>2</sub>SO<sub>4</sub> (pH 1.5-2.0), 25-50°C</td>
                <td>70-90%</td>
            </tr>
            <tr>
                <td>Solvent Extraction</td>
                <td>LIX reagents, O:A ratio 1:1 to 3:1</td>
                <td>95-99%</td>
            </tr>
            <tr>
                <td>Electrowinning</td>
                <td>2.0-2.5 V, 200-300 A/m<sup>2</sup></td>
                <td>99.99% pure</td>
            </tr>
        </table>
    </div>

    <div class="section" id="titanium">
        <h2>3. Titanium Extraction</h2>
        <p>Titanium is extracted from rutile (TiO<sub>2</sub>) or ilmenite (FeTiO<sub>3</sub>) through the Kroll process.</p>
        
        <h3>3.1 Kroll Process Parameters</h3>
        <table class="metal-table titanium-table">
            <tr>
                <th>Stage</th>
                <th>Conditions</th>
                <th>Duration</th>
            </tr>
            <tr>
                <td>Chlorination</td>
                <td>900-1000°C with petroleum coke</td>
                <td>4-12 hours</td>
            </tr>
            <tr>
                <td>Purification</td>
                <td>Distillation at 136°C</td>
                <td>2-4 hours</td>
            </tr>
            <tr>
                <td>Reduction</td>
                <td>800-850°C, Ar atmosphere</td>
                <td>36-50 hours</td>
            </tr>
            <tr>
                <td>Vacuum Distillation</td>
                <td>1000°C at 0.1-1 mbar</td>
                <td>48-72 hours</td>
            </tr>
        </table>
    </div>

    <!-- MCQ Sections -->
    <div class="section" id="aluminium-mcqs">
        <h2>Aluminium Extraction MCQs</h2>
        
        <div class="mcq">
            <div class="question">1. What is the primary purpose of cryolite in the Hall-Héroult process?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">To provide aluminium ions</div>
                <div class="option" onclick="checkAnswer(this, true)">To dissolve alumina and lower the melting point</div>
                <div class="option" onclick="checkAnswer(this, false)">To act as a reducing agent</div>
                <div class="option" onclick="checkAnswer(this, false)">To prevent oxidation of the aluminium</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: To dissolve alumina and lower the melting point</strong></p>
                    <p>Cryolite (Na<sub>3</sub>AlF<sub>6</sub>) serves as a solvent for alumina (Al<sub>2</sub>O<sub>3</sub>), allowing electrolysis to occur at 950°C instead of alumina's melting point of 2072°C. This dramatically reduces energy requirements.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">2. In the Bayer process, what is the purpose of adding sodium hydroxide (NaOH) to bauxite?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">To neutralize acidic impurities</div>
                <div class="option" onclick="checkAnswer(this, true)">To selectively dissolve aluminium hydroxide</div>
                <div class="option" onclick="checkAnswer(this, false)">To precipitate iron oxides</div>
                <div class="option" onclick="checkAnswer(this, false)">To increase the melting point of the mixture</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: To selectively dissolve aluminium hydroxide</strong></p>
                    <p>NaOH reacts with Al(OH)<sub>3</sub> in bauxite to form soluble sodium aluminate (NaAlO<sub>2</sub>), while impurities like Fe<sub>2</sub>O<sub>3</sub> remain insoluble. This selective dissolution is the key separation mechanism in the Bayer process.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="copper-mcqs">
        <h2>Copper Extraction MCQs</h2>
        
        <div class="mcq">
            <div class="question">1. What is the primary purpose of the converting stage in copper pyrometallurgy?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">To remove gangue minerals</div>
                <div class="option" onclick="checkAnswer(this, true)">To oxidize iron sulfides and produce blister copper</div>
                <div class="option" onclick="checkAnswer(this, false)">To reduce copper oxides to metallic copper</div>
                <div class="option" onclick="checkAnswer(this, false)">To dissolve copper minerals in acid</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: To oxidize iron sulfides and produce blister copper</strong></p>
                    <p>The converting stage uses oxygen injection to oxidize remaining FeS in the matte to FeO (which forms slag) and produce blister copper (98.5% Cu) through the reaction: Cu<sub>2</sub>S + O<sub>2</sub> → 2Cu + SO<sub>2</sub>.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">2. In copper hydrometallurgy, what is the purpose of solvent extraction?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">To melt the copper concentrate</div>
                <div class="option" onclick="checkAnswer(this, true)">To selectively transfer copper from leach solution to organic phase</div>
                <div class="option" onclick="checkAnswer(this, false)">To reduce copper ions to metal</div>
                <div class="option" onclick="checkAnswer(this, false)">To remove sulfur dioxide emissions</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: To selectively transfer copper from leach solution to organic phase</strong></p>
                    <p>Solvent extraction uses organic reagents like LIX 984N to selectively extract Cu<sup>2+</sup> ions from the pregnant leach solution into an organic phase, leaving impurities behind. The copper is then stripped into a high-purity electrolyte for electrowinning.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="titanium-mcqs">
        <h2>Titanium Extraction MCQs</h2>
        
        <div class="mcq">
            <div class="question">1. Why is magnesium used in the Kroll process instead of carbon for titanium reduction?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Magnesium is cheaper than carbon</div>
                <div class="option" onclick="checkAnswer(this, true)">Carbon would form titanium carbide which contaminates the metal</div>
                <div class="option" onclick="checkAnswer(this, false)">Magnesium reduces at lower temperatures</div>
                <div class="option" onclick="checkAnswer(this, false)">Carbon cannot reduce titanium tetrachloride</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Carbon would form titanium carbide which contaminates the metal</strong></p>
                    <p>Carbon reduction of TiCl<sub>4</sub> would produce brittle titanium carbide (TiC) instead of pure titanium. Magnesium is used because it reduces TiCl<sub>4</sub> to pure titanium while forming MgCl<sub>2</sub> byproduct that can be separated.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">2. What is the primary reason the Kroll process is batch rather than continuous?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Lower equipment costs</div>
                <div class="option" onclick="checkAnswer(this, true)">The need to physically remove titanium sponge from the reactor</div>
                <div class="option" onclick="checkAnswer(this, false)">Easier temperature control</div>
                <div class="option" onclick="checkAnswer(this, false)">Government regulations</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: The need to physically remove titanium sponge from the reactor</strong></p>
                    <p>The Kroll process produces titanium in a porous "sponge" form that adheres to reactor walls and must be mechanically removed after each batch. This makes continuous operation impractical, unlike processes that produce molten metals.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="comparative-mcqs">
        <h2>Comparative Extraction MCQs</h2>
        
        <div class="mcq">
            <div class="question">1. Which of these metals is primarily extracted using electrolysis of a molten salt?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, true)">Aluminium</div>
                <div class="option" onclick="checkAnswer(this, false)">Copper</div>
                <div class="option" onclick="checkAnswer(this, false)">Titanium</div>
                <div class="option" onclick="checkAnswer(this, false)">All of the above</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Aluminium</strong></p>
                    <p>Aluminium is produced by electrolysis of alumina dissolved in molten cryolite (Hall-Héroult process). Copper is typically produced by pyrometallurgy or electrowinning from aqueous solutions, while titanium is produced by magnesium reduction (Kroll process).</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">2. Which extraction process uses chloride chemistry for metal production?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Bayer process (Al)</div>
                <div class="option" onclick="checkAnswer(this, false)">Flash smelting (Cu)</div>
                <div class="option" onclick="checkAnswer(this, true)">Kroll process (Ti)</div>
                <div class="option" onclick="checkAnswer(this, false)">All of the above</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Kroll process (Ti)</strong></p>
                    <p>The Kroll process converts TiO<sub>2</sub> to TiCl<sub>4</sub> which is then reduced by Mg. The Bayer process uses hydroxide chemistry, while copper smelting uses sulfide/oxide chemistry.</p>
                </div>
            </div>
        </div>
    </div>
<div class="test-section" id="test-yourself">
        <div class="test-header">
            <i class="fas fa-graduation-cap"></i>
            <div>
                <h2>TestUrSelf</h2>
                <p>Evaluate your knowledge with these interactive courses</p>
            </div>
        </div>
        
        <div class="test-grid">
            <div class="test-card">
                <h3>Aluminium Extraction</h3>
                <p>10 questions covering Bayer process and Hall-Héroult electrolysis</p>
                <button class="start-btn" onclick="startQuiz('aluminium')">
                    <i class="fas fa-play"></i> Start Course
                </button>
            </div>
            
            <div class="test-card">
                <h3>Copper Metallurgy</h3>
                <p>8 questions on pyrometallurgical and hydrometallurgical routes</p>
                <button class="start-btn" onclick="startQuiz('copper')">
                    <i class="fas fa-play"></i> Start Course
                </button>
            </div>
            
            <div class="test-card">
                <h3>Titanium Production</h3>
                <p>6 questions focusing on Kroll process and alternatives</p>
                <button class="start-btn" onclick="startQuiz('titanium')">
                    <i class="fas fa-play"></i> Start Course
                </button>
            </div>
            
            <div class="test-card">
                <h3>Comparative Analysis</h3>
                <p>12 questions comparing all three extraction processes</p>
                <button class="start-btn" onclick="startQuiz('comparative')">
                    <i class="fas fa-play"></i> Start Course
                </button>
            </div>
        </div>
    </div>

    <script>
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
        
        // Add scroll margin to account for fixed header
        document.addEventListener('DOMContentLoaded', function() {
            document.querySelectorAll('h2').forEach(h2 => {
                h2.style.scrollMarginTop = '120px';
            });
        });
    </script>
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.4.0/dist/confetti.browser.min.js"></script>
</body>
</html>
