<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Iron Making - Ultimate eNotes</title>
    <style>
        :root {
            --primary: #2A2F4F;
            --secondary: #917FB3;
            --accent: #E5BEEC;
            --highlight: #FDE2F3;
            --text: #2A2F4F;
            --light-bg: #FDE2F3;
            --card-bg: #FFFFFF;
            --progress: #917FB3;
            --correct: #4CAF50;
            --incorrect: #F44336;
        }
        
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.7;
            color: var(--text);
            background-color: var(--light-bg);
            margin: 0;
            padding: 0;
            overflow-x: hidden;
        }
        
        /* Layout Adjustments for Desktop */
        .content-container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 2rem;
            display: grid;
            grid-template-columns: minmax(250px, 300px) 1fr;
            gap: 2rem;
        }
        
        .toc-container {
            position: sticky;
            top: 20px;
            align-self: start;
            height: fit-content;
            max-height: 90vh;
            overflow-y: auto;
        }
        
        .main-content {
            grid-column: 2;
        }
        
        /* Header Section */
        .header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            text-align: center;
            padding: 4rem 1rem;
            position: relative;
            overflow: hidden;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
            grid-column: 1 / -1;
        }
        
        .header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('https://images.unsplash.com/photo-1584811644727-e2c9d1107358?q=80&w=1000') center/cover;
            opacity: 0.15;
            z-index: 0;
        }
        
        .header-content {
            position: relative;
            z-index: 1;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .header h1 {
            font-size: 3rem;
            margin: 0;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        .header p {
            font-size: 1.3rem;
            margin: 1.5rem 0 0;
            opacity: 0.9;
        }
        
        /* Table of Contents */
        .toc-container {
            background-color: var(--card-bg);
            padding: 1.5rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.08);
            position: relative;
            overflow: hidden;
        }
        
        .toc-container::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--secondary), var(--accent));
        }
        
        .toc-header {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
        }
        
        .toc-header h2 {
            font-size: 1.5rem;
            color: var(--primary);
            margin: 0;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .toc-header i {
            color: var(--secondary);
            font-size: 1.3rem;
        }
        
        .toc-list {
            list-style: none;
            padding: 0;
            margin: 0;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        
        .toc-item {
            margin: 0;
        }
        
        .toc-link {
            display: flex;
            align-items: center;
            padding: 10px 15px;
            background-color: rgba(145, 127, 179, 0.1);
            border-radius: 8px;
            color: var(--text);
            text-decoration: none;
            transition: all 0.3s ease;
            font-weight: 500;
            font-size: 0.95rem;
        }
        
        .toc-link:hover, .toc-link.active {
            background-color: rgba(145, 127, 179, 0.2);
            transform: translateX(5px);
        }
        
        .toc-link::before {
            content: "•";
            color: var(--secondary);
            margin-right: 10px;
            font-size: 1.5rem;
        }
        
        /* Main Content */
        .section {
            background-color: var(--card-bg);
            border-radius: 15px;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 5px 20px rgba(0,0,0,0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        .section::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--secondary), var(--accent));
        }
        
        h2 {
            color: var(--primary);
            font-size: 1.8rem;
            margin-top: 0;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--accent);
            display: inline-block;
        }
        
        h3 {
            color: var(--secondary);
            font-size: 1.4rem;
            margin-top: 1.8rem;
        }
        
        /* Interactive Elements */
        .mcq {
            background-color: rgba(229, 190, 236, 0.2);
            border-left: 4px solid var(--secondary);
            padding: 1.5rem;
            margin: 2rem 0;
            border-radius: 0 10px 10px 0;
            transition: all 0.3s ease;
        }
        
        .mcq:hover {
            background-color: rgba(229, 190, 236, 0.3);
        }
        
        .question {
            font-weight: 600;
            font-size: 1.1rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }
        
        .options {
            display: grid;
            gap: 10px;
        }
        
        .option {
            padding: 10px 15px;
            background-color: rgba(255,255,255,0.7);
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s ease;
            border: 1px solid #eee;
        }
        
        .option:hover {
            background-color: rgba(145, 127, 179, 0.1);
            border-color: var(--secondary);
        }
        
        .answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease, padding 0.5s ease;
            background-color: rgba(255,255,255,0.8);
            border-radius: 8px;
        }
        
        .answer.show {
            max-height: 500px;
            padding: 1rem;
            margin-top: 1rem;
        }
        
        .answer-content {
            padding: 1rem;
        }
        
        .correct {
            color: var(--correct);
            font-weight: 600;
        }
        
        .show-answer-btn {
            background-color: var(--secondary);
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
            background-color: var(--primary);
            transform: translateY(-2px);
        }
        
        /* Diagrams */
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
        
        /* Tables */
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 2rem 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            border-radius: 10px;
            overflow: hidden;
        }
        
        th, td {
            padding: 1rem;
            text-align: left;
            border-bottom: 1px solid #eee;
        }
        
        th {
            background-color: var(--secondary);
            color: white;
            font-weight: 500;
        }
        
        tr:nth-child(even) {
            background-color: rgba(229, 190, 236, 0.1);
        }
        
        tr:hover {
            background-color: rgba(229, 190, 236, 0.2);
        }
        
        /* Key Points */
        .key-point {
            background: linear-gradient(to right, rgba(253, 226, 243, 0.8), rgba(255,255,255,0.8));
            border-left: 4px solid var(--secondary);
            padding: 1.5rem;
            margin: 2rem 0;
            border-radius: 0 10px 10px 0;
            position: relative;
        }
        
        .key-point h4 {
            margin-top: 0;
            color: var(--secondary);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .key-point h4 i {
            color: var(--secondary);
        }
        
        /* Process Steps */
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
            background: linear-gradient(to bottom right, var(--secondary), var(--accent));
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        /* Comparison Sections */
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
        
        .comparison-item h4 {
            color: var(--secondary);
            border-bottom: 2px solid var(--accent);
            padding-bottom: 0.5rem;
            margin-top: 0;
        }
        
        /* Progress Bar */
        .progress-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: transparent;
            z-index: 1000;
        }
        
        .progress-bar {
            height: 100%;
            background: linear-gradient(to right, var(--secondary), var(--accent));
            width: 0%;
            transition: width 0.1s ease;
        }
        
        /* Back to Top Button */
        #back-to-top {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            width: 50px;
            height: 50px;
            background: linear-gradient(to bottom right, var(--secondary), var(--accent));
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            z-index: 999;
            border: none;
        }
        
        #back-to-top.visible {
            opacity: 1;
            visibility: visible;
        }
        
        #back-to-top:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 20px rgba(0,0,0,0.3);
        }
        
        /* Responsive Design */
        @media (max-width: 1024px) {
            .content-container {
                grid-template-columns: 1fr;
                padding: 0 1.5rem;
            }
            
            .toc-container {
                position: static;
                max-height: none;
            }
            
            .main-content {
                grid-column: 1;
            }
            
            .header h1 {
                font-size: 2.5rem;
            }
            
            .header p {
                font-size: 1.1rem;
            }
        }
        
        @media (max-width: 768px) {
            .header {
                padding: 3rem 1rem;
            }
            
            .header h1 {
                font-size: 2rem;
            }
            
            .section {
                padding: 1.5rem;
            }
            
            h2 {
                font-size: 1.5rem;
            }
            
            h3 {
                font-size: 1.2rem;
            }
            
            .comparison-item {
                min-width: 100%;
            }
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .fade-in {
            animation: fadeIn 0.6s ease forwards;
        }
        
        .delay-1 { animation-delay: 0.1s; }
        .delay-2 { animation-delay: 0.2s; }
        .delay-3 { animation-delay: 0.3s; }
        .delay-4 { animation-delay: 0.4s; }
        
        /* Print Styles */
        @media print {
            .header, .toc-container, #back-to-top, .progress-container {
                display: none;
            }
            
            .answer {
                max-height: none !important;
                display: block !important;
            }
            
            body {
                background-color: white;
                color: black;
            }
            
            .section {
                box-shadow: none;
                border: 1px solid #ddd;
                page-break-inside: avoid;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <!-- Progress Bar -->
    <div class="progress-container">
        <div class="progress-bar" id="progressBar"></div>
    </div>
    
    <!-- Back to Top Button -->
    <button id="back-to-top" aria-label="Back to top">
        <i class="fas fa-arrow-up"></i>
    </button>
    
    <!-- Header Section -->
    <header class="header fade-in">
        <div class="header-content">
            <h1>Iron Making</h1>
            <p>Comprehensive Interactive eNotes on Modern Iron Production Techniques</p>
        </div>
    </header>
    
    <!-- Main Content -->
    <main class="content-container">
        <!-- Table of Contents -->
        <section class="toc-container fade-in delay-1">
            <div class="toc-header">
                <h2><i class="fas fa-book-open"></i> Table of Contents</h2>
            </div>
            <ul class="toc-list">
                <li class="toc-item"><a href="#introduction" class="toc-link">Introduction to Iron Making</a></li>
                <li class="toc-item"><a href="#raw-materials" class="toc-link">Raw Materials for Iron Making</a></li>
                <li class="toc-item"><a href="#blast-furnace" class="toc-link">Blast Furnace Iron Making</a></li>
                <li class="toc-item"><a href="#alternative-processes" class="toc-link">Alternative Iron Making Processes</a></li>
                <li class="toc-item"><a href="#physical-chemistry" class="toc-link">Physical Chemistry of Iron Making</a></li>
                <li class="toc-item"><a href="#modern-developments" class="toc-link">Modern Developments</a></li>
                <li class="toc-item"><a href="#quality-control" class="toc-link">Quality Control and Testing</a></li>
                <li class="toc-item"><a href="#safety-environment" class="toc-link">Safety and Environmental Aspects</a></li>
                <li class="toc-item"><a href="#future-trends" class="toc-link">Future Trends in Iron Making</a></li>
            </ul>
        </section>
        
        <!-- Main Content Sections -->
        <div class="main-content">
            <!-- Introduction Section -->
            <section id="introduction" class="section fade-in delay-2">
                <h2>1. Introduction to Iron Making</h2>
                <p>Iron making is the process of producing iron from iron ore through reduction reactions in blast furnaces or direct reduction plants. Iron is one of the most important metals in modern industry, serving as the primary raw material for steel production.</p>
                
                <div class="key-point">
                    <h4><i class="fas fa-lightbulb"></i> Key Historical Note</h4>
                    <p>The production of iron dates back to around 1200 BC, marking the beginning of the Iron Age. Modern iron making began with the development of the blast furnace in the 14th century.</p>
                </div>
                
                <div class="mcq">
                    <div class="question">What is the primary purpose of iron making?</div>
                    <div class="options">
                        <div class="option" onclick="checkAnswer(this, 'C')">To extract pure iron from its ores</div>
                        <div class="option" onclick="checkAnswer(this, 'C')">To produce steel directly from iron ore</div>
                        <div class="option correct-option" onclick="checkAnswer(this, 'C')">To reduce iron oxides to metallic iron</div>
                        <div class="option" onclick="checkAnswer(this, 'C')">To alloy iron with carbon for immediate use</div>
                    </div>
                    <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Explanation</button>
                    <div class="answer" id="answer1">
                        <div class="answer-content">
                            <p><strong>Correct Answer: To reduce iron oxides to metallic iron</strong></p>
                            <p>The primary purpose of iron making is the reduction of iron oxides (Fe₂O₃, Fe₃O₄) present in iron ore to metallic iron (Fe). This is typically done through chemical reduction using carbon monoxide in a blast furnace.</p>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- Raw Materials Section -->
            <section id="raw-materials" class="section fade-in delay-3">
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
                        <div class="option" onclick="checkAnswer(this, 'B')">Hematite (Fe₂O₃)</div>
                        <div class="option correct-option" onclick="checkAnswer(this, 'B')">Magnetite (Fe₃O₄)</div>
                        <div class="option" onclick="checkAnswer(this, 'B')">Limonite (FeO(OH)·nH₂O)</div>
                        <div class="option" onclick="checkAnswer(this, 'B')">Siderite (FeCO₃)</div>
                    </div>
                    <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Explanation</button>
                    <div class="answer" id="answer2">
                        <div class="answer-content">
                            <p><strong>Correct Answer: Magnetite (Fe₃O₄)</strong></p>
                            <p>Magnetite typically contains 60-70% iron by weight, which is higher than hematite (50-65%), limonite (35-50%), and siderite (30-40%).</p>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- Blast Furnace Section -->
            <section id="blast-furnace" class="section fade-in delay-4">
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
                        <div class="option" onclick="checkAnswer(this, 'B')">Fe₂O₃ + CO → 2Fe₃O₄ + CO₂</div>
                        <div class="option correct-option" onclick="checkAnswer(this, 'B')">C + CO₂ → 2CO</div>
                        <div class="option" onclick="checkAnswer(this, 'B')">FeO + C → Fe + CO</div>
                        <div class="option" onclick="checkAnswer(this, 'B')">CaCO₃ → CaO + CO₂</div>
                    </div>
                    <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Explanation</button>
                    <div class="answer" id="answer3">
                        <div class="answer-content">
                            <p><strong>Correct Answer: C + CO₂ → 2CO</strong></p>
                            <p>This is the Boudouard reaction, which is crucial for generating the reducing gas (CO) in the blast furnace. The other options either consume CO or produce CO₂.</p>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- Alternative Processes Section -->
            <section id="alternative-processes" class="section">
                <h2>4. Alternative Iron Making Processes</h2>
                <p>While blast furnaces dominate iron production, several alternative processes have been developed to address environmental concerns, reduce costs, or utilize different raw materials.</p>
                
                <div class="comparison">
                    <div class="comparison-item">
                        <h4>4.1 Direct Reduction Processes</h4>
                        <p>Produce solid metallic iron (DRI - Direct Reduced Iron) without melting:</p>
                        <ul>
                            <li><strong>Midrex Process</strong>: Uses reformed natural gas (H₂ + CO) in shaft furnace</li>
                            <li><strong>HYL Process</strong>: Uses hydrogen-rich gas in retorts</li>
                            <li><strong>SL/RN Process</strong>: Rotary kiln using coal as reductant</li>
                        </ul>
                        <p><strong>Advantages:</strong></p>
                        <ul>
                            <li>Lower capital cost</li>
                            <li>Flexibility in raw materials</li>
                            <li>Lower CO₂ emissions</li>
                        </ul>
                        <p><strong>Disadvantages:</strong></p>
                        <ul>
                            <li>Requires high-grade ore</li>
                            <li>Produces lower carbon iron</li>
                            <li>Limited production scale</li>
                        </ul>
                    </div>
                    
                    <div class="comparison-item">
                        <h4>4.2 Smelting Reduction Processes</h4>
                        <p>Combine ore reduction and melting in single unit:</p>
                        <ul>
                            <li><strong>COREX Process</strong>: Two-stage process with reduction shaft and melter-gasifier</li>
                            <li><strong>FINEX Process</strong>: Fluidized bed reduction followed by melter-gasifier</li>
                            <li><strong>HIsarna Process</strong>: Cyclone converter furnace</li>
                        </ul>
                        <p><strong>Advantages:</strong></p>
                        <ul>
                            <li>No coking plant needed</li>
                            <li>Can use fine ores and non-coking coal</li>
                            <li>Lower environmental impact</li>
                        </ul>
                        <p><strong>Disadvantages:</strong></p>
                        <ul>
                            <li>Higher energy consumption</li>
                            <li>Operational complexity</li>
                            <li>Limited commercial adoption</li>
                        </ul>
                    </div>
                </div>
                
                <div class="diagram">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9d/Midrex_Process.svg/800px-Midrex_Process.svg.png" alt="Midrex Process Diagram">
                    <div class="caption">Figure 3: Midrex direct reduction process flow diagram</div>
                </div>
                
                <div class="mcq">
                    <div class="question">Which of the following processes produces solid metallic iron (DRI) rather than liquid iron?</div>
                    <div class="options">
                        <div class="option" onclick="checkAnswer(this, 'C')">COREX process</div>
                        <div class="option" onclick="checkAnswer(this, 'C')">Blast furnace process</div>
                        <div class="option correct-option" onclick="checkAnswer(this, 'C')">Midrex process</div>
                        <div class="option" onclick="checkAnswer(this, 'C')">HIsarna process</div>
                    </div>
                    <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Explanation</button>
                    <div class="answer" id="answer4">
                        <div class="answer-content">
                            <p><strong>Correct Answer: Midrex process</strong></p>
                            <p>The Midrex process is a direct reduction process that produces solid DRI (Direct Reduced Iron), while the other options produce liquid iron.</p>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- Physical Chemistry Section -->
            <section id="physical-chemistry" class="section">
                <h2>5. Physical Chemistry of Iron Making</h2>
                
                <h3>5.1 Thermodynamics of Iron Oxide Reduction</h3>
                <p>The reduction of iron oxides proceeds in stages:</p>
                <p>Fe₂O₃ → Fe₃O₄ → FeO → Fe</p>
                
                <p>The Ellingham diagram shows the thermodynamic feasibility of reduction reactions at different temperatures. Key points:</p>
                <ul>
                    <li>Below 570°C: Fe₃O₄ reduces directly to Fe (FeO is unstable)</li>
                    <li>Above 570°C: Stepwise reduction through FeO</li>
                    <li>The Boudouard reaction (C + CO₂ ⇌ 2CO) becomes important above 700°C</li>
                </ul>
                
                <div class="diagram">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/7f/Ellingham_Diagram.svg/800px-Ellingham_Diagram.svg.png" alt="Ellingham Diagram">
                    <div class="caption">Figure 4: Ellingham diagram showing iron oxide reduction thermodynamics</div>
                </div>
                
                <h3>5.2 Slag Formation and Properties</h3>
                <p>Slag performs several critical functions:</p>
                <ul>
                    <li>Absorbs impurities (SiO₂, Al₂O₃, S, etc.)</li>
                    <li>Protects hot metal from reoxidation</li>
                    <li>Controls sulfur distribution</li>
                </ul>
                
                <p>Important slag properties:</p>
                <ul>
                    <li><strong>Basicity</strong>: Ratio of basic to acidic oxides (CaO/SiO₂)</li>
                    <li><strong>Viscosity</strong>: Affects separation from metal and heat transfer</li>
                    <li><strong>Melting point</strong>: Typically 1300-1400°C</li>
                </ul>
                
                <div class="key-point">
                    <h4><i class="fas fa-lightbulb"></i> Key Concept</h4>
                    <p>The ideal slag basicity (CaO/SiO₂ ratio) for blast furnace operation is typically 1.0-1.2, providing good sulfur removal capability while maintaining proper fluidity.</p>
                </div>
                
                <div class="mcq">
                    <div class="question">Below what temperature does FeO become unstable in the iron oxide reduction sequence?</div>
                    <div class="options">
                        <div class="option" onclick="checkAnswer(this, 'B')">300°C</div>
                        <div class="option correct-option" onclick="checkAnswer(this, 'B')">570°C</div>
                        <div class="option" onclick="checkAnswer(this, 'B')">900°C</div>
                        <div class="option" onclick="checkAnswer(this, 'B')">1200°C</div>
                    </div>
                    <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Explanation</button>
                    <div class="answer" id="answer5">
                        <div class="answer-content">
                            <p><strong>Correct Answer: 570°C</strong></p>
                            <p>Below 570°C, FeO is thermodynamically unstable, and Fe₃O₄ reduces directly to Fe without forming FeO as an intermediate.</p>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- Modern Developments Section -->
            <section id="modern-developments" class="section">
                <h2>6. Modern Developments in Iron Making</h2>
                
                <h3>6.1 Energy Efficiency Improvements</h3>
                <ul>
                    <li><strong>Top pressure recovery turbines (TRT)</strong>: Generate electricity from blast furnace top gas pressure</li>
                    <li><strong>Pulverized coal injection (PCI)</strong>: Reduces coke consumption by up to 30%</li>
                    <li><strong>Waste heat recovery</strong>: Utilization of slag and gas heat</li>
                    <li><strong>Oxygen enrichment</strong>: Increases combustion efficiency</li>
                </ul>
                
                <div class="diagram">
                    <img src="https://www.researchgate.net/publication/334387343/figure/fig1/AS:779806923943936@1562868432524/Schematic-diagram-of-the-top-gas-recovery-turbine-unit-TRT.png" alt="TRT Unit Diagram">
                    <div class="caption">Figure 5: Top gas recovery turbine unit (TRT) schematic</div>
                </div>
                
                <h3>6.2 Environmental Considerations</h3>
                <ul>
                    <li><strong>CO₂ emissions reduction</strong>: Through process optimization and carbon capture</li>
                    <li><strong>Slag utilization</strong>: 100% of blast furnace slag can be utilized (cement, road construction)</li>
                    <li><strong>Dust recycling</strong>: Recycling of blast furnace and BOF dusts</li>
                    <li><strong>Water conservation</strong>: Closed-loop cooling systems</li>
                </ul>
                
                <h3>6.3 Industry 4.0 Applications</h3>
                <ul>
                    <li><strong>Digital twins</strong>: Virtual models of blast furnaces for optimization</li>
                    <li><strong>AI-based process control</strong>: Predictive models for furnace operation</li>
                    <li><strong>Automated quality control</strong>: Machine vision for slag and hot metal analysis</li>
                    <li><strong>IoT sensors</strong>: Real-time monitoring of furnace conditions</li>
                </ul>
                
                <div class="mcq">
                    <div class="question">Which technology can reduce coke consumption in blast furnaces by injecting alternative carbon sources?</div>
                    <div class="options">
                        <div class="option" onclick="checkAnswer(this, 'B')">TRT (Top Recovery Turbine)</div>
                        <div class="option correct-option" onclick="checkAnswer(this, 'B')">PCI (Pulverized Coal Injection)</div>
                        <div class="option" onclick="checkAnswer(this, 'B')">DRI (Direct Reduced Iron)</div>
                        <div class="option" onclick="checkAnswer(this, 'B')">BOF (Basic Oxygen Furnace)</div>
                    </div>
                    <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Explanation</button>
                    <div class="answer" id="answer6">
                        <div class="answer-content">
                            <p><strong>Correct Answer: PCI (Pulverized Coal Injection)</strong></p>
                            <p>PCI technology injects pulverized coal into the blast furnace tuyeres, replacing part of the coke requirement while maintaining the necessary reducing conditions.</p>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- Quality Control Section -->
            <section id="quality-control" class="section">
                <h2>7. Quality Control and Testing</h2>
                
                <h3>7.1 Hot Metal Analysis</h3>
                <p>Key parameters monitored:</p>
                <ul>
                    <li><strong>Chemical composition</strong>: C, Si, Mn, P, S content</li>
                    <li><strong>Temperature</strong>: Typically 1400-1500°C</li>
                    <li><strong>Physical properties</strong>: Fluidity, slag separation</li>
                </ul>
                
                <h3>7.2 Slag Analysis</h3>
                <p>Important slag characteristics:</p>
                <ul>
                    <li><strong>Basicity ratio</strong> (CaO/SiO₂): Typically 1.0-1.2</li>
                    <li><strong>Viscosity</strong>: Affects metal-slag separation</li>
                    <li><strong>Sulfur capacity</strong>: Ability to absorb sulfur from metal</li>
                </ul>
                
                <table>
                    <tr>
                        <th>Parameter</th>
                        <th>Typical Range</th>
                        <th>Measurement Method</th>
                    </tr>
                    <tr>
                        <td>Hot Metal Temperature</td>
                        <td>1400-1500°C</td>
                        <td>Optical pyrometer</td>
                    </tr>
                    <tr>
                        <td>Carbon Content</td>
                        <td>3.5-4.5%</td>
                        <td>Combustion analysis</td>
                    </tr>
                    <tr>
                        <td>Silicon Content</td>
                        <td>0.5-1.5%</td>
                        <td>Spectroscopy</td>
                    </tr>
                    <tr>
                        <td>Slag Basicity (CaO/SiO₂)</td>
                        <td>1.0-1.2</td>
                        <td>X-ray fluorescence</td>
                    </tr>
                </table>
                
                <div class="mcq">
                    <div class="question">What is the typical basicity ratio (CaO/SiO₂) of blast furnace slag?</div>
                    <div class="options">
                        <div class="option" onclick="checkAnswer(this, 'B')">0.5-0.7</div>
                        <div class="option correct-option" onclick="checkAnswer(this, 'B')">1.0-1.2</div>
                        <div class="option" onclick="checkAnswer(this, 'B')">1.5-1.8</div>
                        <div class="option" onclick="checkAnswer(this, 'B')">2.0-2.5</div>
                    </div>
                    <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Explanation</button>
                    <div class="answer" id="answer7">
                        <div class="answer-content">
                            <p><strong>Correct Answer: 1.0-1.2</strong></p>
                            <p>Blast furnace slag typically has a basicity ratio (CaO/SiO₂) of 1.0-1.2, which provides good sulfur removal capability while maintaining proper fluidity.</p>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- Safety Section -->
            <section id="safety-environment" class="section">
                <h2>8. Safety and Environmental Aspects</h2>
                
                <h3>8.1 Safety Considerations</h3>
                <ul>
                    <li><strong>High temperature hazards</strong>: Proper PPE and barriers</li>
                    <li><strong>Gas hazards</strong>: CO poisoning prevention</li>
                    <li><strong>Molten metal hazards</strong>: Prevention of explosions from moisture contact</li>
                    <li><strong>Dust exposure</strong>: Respiratory protection</li>
                    <li><strong>Noise control</strong>: Hearing protection in high-noise areas</li>
                </ul>
                
                <div class="key-point">
                    <h4><i class="fas fa-exclamation-triangle"></i> Safety Alert</h4>
                    <p>Carbon monoxide (CO) is particularly dangerous as it is colorless and odorless. Proper gas detection systems and ventilation are essential in all iron making facilities.</p>
                </div>
                
                <h3>8.2 Environmental Impact and Mitigation</h3>
                <ul>
                    <li><strong>Air emissions</strong>: Particulates, CO, CO₂, SOₓ, NOₓ</li>
                    <li><strong>Waste management</strong>: Slag, dust, and sludge utilization</li>
                    <li><strong>Water usage</strong>: Closed-loop cooling systems</li>
                    <li><strong>Energy efficiency</strong>: Heat recovery systems</li>
                </ul>
                
                <div class="comparison">
                    <div class="comparison-item">
                        <h4>Environmental Challenges</h4>
                        <ul>
                            <li>High CO₂ emissions (1.8-2.2 tons CO₂/ton iron)</li>
                            <li>Particulate emissions from handling raw materials</li>
                            <li>Water consumption in cooling processes</li>
                            <li>Solid waste generation (slag, dust)</li>
                        </ul>
                    </div>
                    
                    <div class="comparison-item">
                        <h4>Mitigation Strategies</h4>
                        <ul>
                            <li>Carbon capture and storage (CCS)</li>
                            <li>Improved dust collection systems</li>
                            <li>Water recycling and treatment</li>
                            <li>Slag utilization in cement production</li>
                        </ul>
                    </div>
                </div>
                
                <div class="mcq">
                    <div class="question">What is the primary gas hazard in iron making operations?</div>
                    <div class="options">
                        <div class="option" onclick="checkAnswer(this, 'C')">Oxygen</div>
                        <div class="option" onclick="checkAnswer(this, 'C')">Nitrogen</div>
                        <div class="option correct-option" onclick="checkAnswer(this, 'C')">Carbon monoxide</div>
                        <div class="option" onclick="checkAnswer(this, 'C')">Carbon dioxide</div>
                    </div>
                    <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Explanation</button>
                    <div class="answer" id="answer8">
                        <div class="answer-content">
                            <p><strong>Correct Answer: Carbon monoxide</strong></p>
                            <p>CO is a colorless, odorless, and highly toxic gas produced in large quantities during iron making. It's the primary gas hazard due to its ability to form carboxyhemoglobin in blood, preventing oxygen transport.</p>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- Future Trends Section -->
            <section id="future-trends" class="section">
                <h2>9. Future Trends in Iron Making</h2>
                
                <h3>9.1 Hydrogen-Based Iron Making</h3>
                <p>Using hydrogen as a reducing agent instead of carbon:</p>
                <ul>
                    <li>Fe₂O₃ + 3H₂ → 2Fe + 3H₂O</li>
                    <li>Potential for near-zero CO₂ emissions if green hydrogen is used</li>
                    <li>HYBRIT (Sweden) and other pilot projects underway</li>
                    <li>Technical challenges in hydrogen storage and high-temperature reduction</li>
                </ul>
                
                <div class="diagram">
                    <img src="https://hybritdevelopment.com/wp-content/uploads/2021/03/HYBRIT-process-schematic.png" alt="HYBRIT Process">
                    <div class="caption">Figure 6: HYBRIT hydrogen-based iron making process</div>
                </div>
                
                <h3>9.2 Carbon Capture and Utilization (CCU)</h3>
                <ul>
                    <li>Capture of CO₂ from blast furnace gases</li>
                    <li>Utilization in chemical synthesis or mineralization</li>
                    <li>Storage in geological formations (CCS)</li>
                    <li>Economic challenges in implementation</li>
                </ul>
                
                <h3>9.3 Increased Use of Biomass</h3>
                <ul>
                    <li>Partial replacement of coke with charcoal</li>
                    <li>Carbon-neutral if from sustainable sources</li>
                    <li>Technical challenges in maintaining furnace permeability</li>
                    <li>Limited availability of biomass at required scale</li>
                </ul>
                
                <div class="key-point">
                    <h4><i class="fas fa-chart-line"></i> Industry Outlook</h4>
                    <p>The iron and steel industry is expected to undergo significant transformation in the coming decades, with hydrogen-based reduction and carbon capture technologies playing key roles in decarbonization efforts.</p>
                </div>
                
                <div class="mcq">
                    <div class="question">Which emerging iron making technology has the potential for near-zero CO₂ emissions when using renewable energy?</div>
                    <div class="options">
                        <div class="option" onclick="checkAnswer(this, 'B')">Increased PCI rates</div>
                        <div class="option correct-option" onclick="checkAnswer(this, 'B')">Hydrogen-based reduction</div>
                        <div class="option" onclick="checkAnswer(this, 'B')">Higher blast temperatures</div>
                        <div class="option" onclick="checkAnswer(this, 'B')">Oxygen enrichment</div>
                    </div>
                    <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Explanation</button>
                    <div class="answer" id="answer9">
                        <div class="answer-content">
                            <p><strong>Correct Answer: Hydrogen-based reduction</strong></p>
                            <p>Hydrogen-based reduction produces water vapor instead of CO₂ as the byproduct. When the hydrogen is produced via electrolysis using renewable electricity, the process can achieve near-zero CO₂ emissions.</p>
                        </div>
                    </div>
                </div>
            </section>
        </div>
    </main>
    
    <script>
        // Progress bar
        function updateProgressBar() {
            const scrollTotal = document.documentElement.scrollHeight - window.innerHeight;
            const scrollPosition = window.scrollY;
            const scrollPercentage = (scrollPosition / scrollTotal) * 100;
            document.getElementById('progressBar').style.width = scrollPercentage + '%';
        }
        
        // Back to top button
        const backToTopButton = document.getElementById('back-to-top');
        
        function toggleBackToTop() {
            if (window.scrollY > 300) {
                backToTopButton.classList.add('visible');
            } else {
                backToTopButton.classList.remove('visible');
            }
        }
        
        backToTopButton.addEventListener('click', function() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
        
        // MCQ functionality
        function checkAnswer(option, correctAnswer) {
            const options = option.parentElement.querySelectorAll('.option');
            options.forEach(opt => {
                opt.style.backgroundColor = '';
                opt.style.borderColor = '#eee';
            });
            
            if (option.classList.contains('correct-option')) {
                option.style.backgroundColor = 'rgba(76, 175, 80, 0.1)';
                option.style.borderColor = 'var(--correct)';
            } else {
                option.style.backgroundColor = 'rgba(244, 67, 54, 0.1)';
                option.style.borderColor = 'var(--incorrect)';
                const correctOpt = option.parentElement.querySelector('.correct-option');
                correctOpt.style.backgroundColor = 'rgba(76, 175, 80, 0.1)';
                correctOpt.style.borderColor = 'var(--correct)';
            }
        }
        
        function toggleAnswer(button) {
            const answer = button.nextElementSibling;
            answer.classList.toggle('show');
            
            if (answer.classList.contains('show')) {
                button.innerHTML = '<i class="fas fa-eye-slash"></i> Hide Explanation';
            } else {
                button.innerHTML = '<i class="fas fa-eye"></i> Show Explanation';
            }
        }
        
        // Smooth scrolling for TOC links
        document.querySelectorAll('.toc-link').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 100,
                    behavior: 'smooth'
                });
                
                // Update URL without page jump
                history.pushState(null, null, targetId);
                
                // Highlight active TOC item
                document.querySelectorAll('.toc-link').forEach(link => {
                    link.classList.remove('active');
                });
                this.classList.add('active');
            });
        });
        
        // Highlight active section in TOC
        function highlightActiveTOC() {
            const sections = document.querySelectorAll('.section');
            const scrollPosition = window.scrollY + 150;
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.offsetHeight;
                const sectionId = section.id;
                
                if (scrollPosition >= sectionTop && scrollPosition < sectionTop + sectionHeight) {
                    document.querySelectorAll('.toc-link').forEach(link => {
                        link.classList.remove('active');
                        if (link.getAttribute('href') === `#${sectionId}`) {
                            link.classList.add('active');
                        }
                    });
                }
            });
        }
        
        // Initialize
        window.addEventListener('scroll', function() {
            updateProgressBar();
            toggleBackToTop();
            highlightActiveTOC();
        });
        
        // Highlight TOC item when navigating via URL hash
        if (window.location.hash) {
            const targetElement = document.querySelector(window.location.hash);
            if (targetElement) {
                setTimeout(() => {
                    window.scrollTo({
                        top: targetElement.offsetTop - 100,
                        behavior: 'smooth'
                    });
                    
                    document.querySelectorAll('.toc-link').forEach(link => {
                        link.classList.remove('active');
                        if (link.getAttribute('href') === window.location.hash) {
                            link.classList.add('active');
                        }
                    });
                }, 100);
            }
        }
        
        // Add animation to sections when they come into view
        const sections = document.querySelectorAll('.section');
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('fade-in');
                }
            });
        }, { threshold: 0.1 });
        
        sections.forEach(section => {
            observer.observe(section);
        });
    </script>
</body>
</html>
