<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Iron Making - Ultimate eNotes</title>
    <style>
        :root {
            --primary-color: #6a1b9a;
            --secondary-color: #ff9800;
            --accent-color: #4a148c;
            --light-color: #f3e5f5;
            --dark-color: #4a148c;
            --text-color: #212121;
            --highlight-color: #ffeb3b;
            --success-color: #388e3c;
            --error-color: #e53935;
            --fluid-color: #1e88e5;
            --mass-color: #43a047;
            --kinetics-color: #8e24aa;
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
            background: linear-gradient(135deg, #f5f5f5 0%, #e0e0e0 50%, #f5f5f5 100%);
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
            font-size: 120px;
            font-weight: bold;
            color: rgba(106, 27, 154, 0.05);
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
        }
        
        h2 {
            color: var(--primary-color);
            border-bottom: 3px solid var(--accent-color);
            padding-bottom: 0.8rem;
            margin-top: 3rem;
            font-size: 2.2rem;
            background: linear-gradient(to right, transparent, #f3e5f5, transparent);
            padding: 1rem 0;
            text-align: center;
            border-radius: 8px;
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
        
        /* MCQ Styling */
        .mcq {
            background-color: rgba(255, 235, 59, 0.1);
            border-left: 4px solid var(--highlight-color);
            padding: 1.5rem;
            margin: 2rem 0;
            border-radius: 0 8px 8px 0;
            transition: all 0.3s ease;
        }
        
        .mcq:hover {
            background-color: rgba(255, 235, 59, 0.15);
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
            background-color: rgba(255, 235, 59, 0.2);
            border-color: var(--highlight-color);
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
        }
        
        .answer-content {
            padding: 1rem;
        }
        
        .show-answer-btn {
            background-color: var(--primary-color);
            color: white;
            border: none;
            padding: 0.6rem 1.2rem;
            border-radius: 6px;
            cursor: pointer;
            margin-top: 1rem;
            font-weight: 500;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: all 0.2s ease;
        }
        
        .show-answer-btn:hover {
            background-color: var(--dark-color);
            transform: translateY(-2px);
        }
        
        /* Content Boxes */
        .key-point {
            background: linear-gradient(to right, #fff8e1, #fffde7);
            border-left: 6px solid var(--highlight-color);
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
            background-color: var(--highlight-color);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        
        .diagram {
            background-color: white;
            padding: 1.5rem;
            border-radius: 10px;
            margin: 2rem 0;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
        }
        
        .diagram img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            border: 1px solid #eee;
            transition: transform 0.3s ease;
        }
        
        .diagram img:hover {
            transform: scale(1.02);
        }
        
        .caption {
            font-style: italic;
            color: #666;
            margin-top: 0.8rem;
            font-size: 0.9rem;
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
        }
        
        tr:nth-child(even) {
            background-color: #f9f9f9;
        }
        
        tr:hover {
            background-color: #f0f0f0;
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
            background: linear-gradient(to bottom right, var(--secondary-color), var(--accent-color));
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .comparison {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 20px;
            margin: 2rem 0;
        }
        
        .comparison-item {
            flex: 1;
            min-width: 300px;
            background-color: white;
            border-radius: 10px;
            padding: 1.5rem;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s ease;
        }
        
        .comparison-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
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
            
            .comparison-item {
                min-width: 100%;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <header>
        <h1>Iron Making</h1>
        <p>Comprehensive Interactive eNotes on Modern Iron Production Techniques</p>
    </header>

    <div class="section" id="introduction">
        <h2>1. Introduction to Iron Making</h2>
        <p>Iron making is the process of producing iron from iron ore through reduction reactions in blast furnaces or direct reduction plants. Iron is one of the most important metals in modern industry, serving as the primary raw material for steel production.</p>
        
        <div class="key-point">
            <h3>Key Historical Note</h3>
            <p>The production of iron dates back to around 1200 BC, marking the beginning of the Iron Age. Modern iron making began with the development of the blast furnace in the 14th century.</p>
        </div>
        
        <div class="mcq">
            <div class="question">What is the primary purpose of iron making?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this)">To extract pure iron from its ores</div>
                <div class="option" onclick="checkAnswer(this)">To produce steel directly from iron ore</div>
                <div class="option" onclick="checkAnswer(this)">To reduce iron oxides to metallic iron</div>
                <div class="option" onclick="checkAnswer(this)">To alloy iron with carbon for immediate use</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: To reduce iron oxides to metallic iron</strong></p>
                    <p>The primary purpose of iron making is the reduction of iron oxides (Fe₂O₃, Fe₃O₄) present in iron ore to metallic iron (Fe). This is typically done through chemical reduction using carbon monoxide in a blast furnace.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">Which historical period is associated with the beginning of iron production?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this)">Bronze Age</div>
                <div class="option" onclick="checkAnswer(this)">Stone Age</div>
                <div class="option" onclick="checkAnswer(this)">Industrial Revolution</div>
                <div class="option" onclick="checkAnswer(this)">Iron Age</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Iron Age</strong></p>
                    <p>The Iron Age (around 1200 BC) marks the beginning of widespread iron production and use, following the Bronze Age.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="raw-materials">
        <h2>2. Raw Materials for Iron Making</h2>
        <p>The production of iron requires several key raw materials, each playing a specific role in the process:</p>
        
        <h3>2.1 Iron Ores</h3>
        <p>The principal iron ores used in iron making include:</p>
        <ul>
            <li><strong>Hematite (Fe₂O₃)</strong>: Contains 50-65% iron, most abundant iron ore</li>
            <li><strong>Magnetite (Fe₃O₄)</strong>: Contains 60-70% iron, highly magnetic</li>
            <li><strong>Limonite (FeO(OH)·nH₂O)</strong>: Contains 35-50% iron</li>
            <li><strong>Siderite (FeCO₃)</strong>: Contains 30-40% iron</li>
        </ul>
        
        <div class="diagram">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5c/Hematite.jpg/800px-Hematite.jpg" alt="Iron Ores">
            <div class="caption">Figure 1: Common iron ores used in iron making (Hematite shown)</div>
        </div>
        
        <h3>2.2 Fluxes</h3>
        <p>Fluxes are added to remove impurities by forming slag:</p>
        <ul>
            <li><strong>Limestone (CaCO₃)</strong>: Most common flux</li>
            <li><strong>Dolomite (CaMg(CO₃)₂)</strong>: Provides both CaO and MgO</li>
        </ul>
        
        <h3>2.3 Fuels and Reducing Agents</h3>
        <ul>
            <li><strong>Coke</strong>: Primary fuel and reducing agent in blast furnaces</li>
            <li><strong>Coal</strong>: Used in some direct reduction processes</li>
            <li><strong>Natural gas</strong>: Used in direct reduction processes</li>
        </ul>
        
        <div class="mcq">
            <div class="question">Which of the following iron ores has the highest iron content?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this)">Hematite (Fe₂O₃)</div>
                <div class="option" onclick="checkAnswer(this)">Magnetite (Fe₃O₄)</div>
                <div class="option" onclick="checkAnswer(this)">Limonite (FeO(OH)·nH₂O)</div>
                <div class="option" onclick="checkAnswer(this)">Siderite (FeCO₃)</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Magnetite (Fe₃O₄)</strong></p>
                    <p>Magnetite typically contains 60-70% iron by weight, which is higher than hematite (50-65%), limonite (35-50%), and siderite (30-40%).</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">What is the primary function of fluxes in iron making?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this)">To provide heat energy</div>
                <div class="option" onclick="checkAnswer(this)">To reduce iron oxides</div>
                <div class="option" onclick="checkAnswer(this)">To remove impurities by forming slag</div>
                <div class="option" onclick="checkAnswer(this)">To increase furnace temperature</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: To remove impurities by forming slag</strong></p>
                    <p>Fluxes combine with impurities (like silica and alumina) to form slag, which can be separated from the molten iron.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">Which of these is NOT typically used as a reducing agent in iron making?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this)">Coke</div>
                <div class="option" onclick="checkAnswer(this)">Coal</div>
                <div class="option" onclick="checkAnswer(this)">Natural gas</div>
                <div class="option" onclick="checkAnswer(this)">Limestone</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Limestone</strong></p>
                    <p>Limestone is a flux, not a reducing agent. Coke, coal, and natural gas all serve as reducing agents in different iron making processes.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="blast-furnace">
        <h2>3. Blast Furnace Iron Making</h2>
        <p>The blast furnace is the most common method for producing iron on an industrial scale. It's a counter-current reactor where iron ore, coke, and flux descend while hot gases ascend.</p>
        
        <div class="diagram">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/7e/Blast_furnace.svg/800px-Blast_furnace.svg.png" alt="Blast Furnace Diagram">
            <div class="caption">Figure 2: Schematic diagram of a blast furnace</div>
        </div>
        
        <h3>3.1 Blast Furnace Zones and Reactions</h3>
        
        <div class="process-steps">
            <div class="process-step">
                <h4>Stack (Preheating Zone)</h4>
                <p>Temperature: 200-800°C</p>
                <p>Reactions:</p>
                <ul>
                    <li>3Fe₂O₃ + CO → 2Fe₃O₄ + CO₂</li>
                    <li>Fe₃O₄ + CO → 3FeO + CO₂</li>
                    <li>Removal of moisture and volatile matter</li>
                </ul>
            </div>
            
            <div class="process-step">
                <h4>Bosh (Reduction Zone)</h4>
                <p>Temperature: 800-1200°C</p>
                <p>Reactions:</p>
                <ul>
                    <li>FeO + CO → Fe + CO₂ (indirect reduction)</li>
                    <li>C + CO₂ → 2CO (Boudouard reaction)</li>
                    <li>CaCO₃ → CaO + CO₂ (calcination)</li>
                </ul>
            </div>
            
            <div class="process-step">
                <h4>Hearth (Melting Zone)</h4>
                <p>Temperature: 1200-1600°C</p>
                <p>Reactions:</p>
                <ul>
                    <li>FeO + C → Fe + CO (direct reduction)</li>
                    <li>Formation of slag: CaO + SiO₂ → CaSiO₃</li>
                    <li>Carburization of iron: 3Fe + C → Fe₃C</li>
                </ul>
            </div>
        </div>
        
        <h3>3.2 Blast Furnace Products</h3>
        <table>
            <tr>
                <th>Product</th>
                <th>Composition</th>
                <th>Temperature</th>
                <th>Use</th>
            </tr>
            <tr>
                <td>Hot Metal (Pig Iron)</td>
                <td>93-95% Fe, 3.5-4.5% C, 0.5-1.5% Si, 0.5-1% Mn, 0.05-0.1% S, 0.1-0.5% P</td>
                <td>1400-1500°C</td>
                <td>Primary product for steel making</td>
            </tr>
            <tr>
                <td>Slag</td>
                <td>30-40% CaO, 30-40% SiO₂, 5-15% Al₂O₃, 5-10% MgO</td>
                <td>1400-1500°C</td>
                <td>Cement additive, road construction</td>
            </tr>
            <tr>
                <td>Top Gas</td>
                <td>20-25% CO, 20-25% CO₂, 50-55% N₂</td>
                <td>100-300°C</td>
                <td>Fuel for stoves, power generation</td>
            </tr>
        </table>
        
        <div class="mcq">
            <div class="question">Which reaction is primarily responsible for producing carbon monoxide in the blast furnace?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this)">Fe₂O₃ + CO → 2Fe₃O₄ + CO₂</div>
                <div class="option" onclick="checkAnswer(this)">C + CO₂ → 2CO</div>
                <div class="option" onclick="checkAnswer(this)">FeO + C → Fe + CO</div>
                <div class="option" onclick="checkAnswer(this)">CaCO₃ → CaO + CO₂</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: C + CO₂ → 2CO</strong></p>
                    <p>This is the Boudouard reaction, which is crucial for generating the reducing gas (CO) in the blast furnace. The other options either consume CO or produce CO₂.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">What is the typical carbon content of pig iron produced in a blast furnace?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this)">0.1-0.5%</div>
                <div class="option" onclick="checkAnswer(this)">1.0-1.5%</div>
                <div class="option" onclick="checkAnswer(this)">2.0-2.5%</div>
                <div class="option" onclick="checkAnswer(this)">3.5-4.5%</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: 3.5-4.5%</strong></p>
                    <p>Pig iron typically contains 3.5-4.5% carbon, along with other impurities like silicon, manganese, sulfur, and phosphorus.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">Which zone of the blast furnace operates at the highest temperature?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this)">Stack</div>
                <div class="option" onclick="checkAnswer(this)">Bosh</div>
                <div class="option" onclick="checkAnswer(this)">Hearth</div>
                <div class="option" onclick="checkAnswer(this)">Throat</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Hearth</strong></p>
                    <p>The hearth is the hottest zone (1200-1600°C) where final reduction and melting occur. The stack is cooler (200-800°C) for preheating, and the bosh is intermediate (800-1200°C).</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Additional sections (Alternative Processes, Physical Chemistry, etc.) would continue here -->
    <!-- Each section would follow the same pattern with content and MCQs -->

    <script>
        // MCQ functionality
        function checkAnswer(option) {
            const options = option.parentElement.querySelectorAll('.option');
            options.forEach(opt => {
                opt.style.backgroundColor = '';
                opt.style.borderColor = '#e0e0e0';
            });
            
            // Visual feedback for selected option
            option.style.backgroundColor = 'rgba(255, 235, 59, 0.3)';
            option.style.borderColor = 'var(--highlight-color)';
        }
        
        function toggleAnswer(button) {
            const answer = button.nextElementSibling;
            answer.classList.toggle('show');
            
            if (answer.classList.contains('show')) {
                button.innerHTML = '<i class="fas fa-eye-slash"></i> Hide Answer';
            } else {
                button.innerHTML = '<i class="fas fa-eye"></i> Show Answer';
            }
        }
    </script>
</body>
</html>
