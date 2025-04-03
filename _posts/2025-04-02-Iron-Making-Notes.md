<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Iron Making - Interactive eNotes</title>
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #e74c3c;
            --accent-color: #2980b9;
            --light-bg: #f9f9f9;
            --card-bg: #ffffff;
            --text-color: #333333;
            --highlight-color: #f39c12;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--light-bg);
            margin: 0;
            padding: 0;
        }
        
        .container {
            display: flex;
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
            gap: 30px;
        }
        
        /* Table of Contents Styles */
        #toc-container {
            width: 280px;
            position: sticky;
            top: 20px;
            height: fit-content;
            max-height: 95vh;
            overflow-y: auto;
            background-color: var(--card-bg);
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            padding: 20px;
            transition: all 0.3s ease;
        }
        
        #toc-container:hover {
            box-shadow: 0 6px 16px rgba(0, 0, 0, 0.15);
        }
        
        #toc-title {
            color: var(--primary-color);
            font-size: 1.4rem;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--secondary-color);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        #toc-title i {
            color: var(--secondary-color);
        }
        
        .toc-list {
            list-style-type: none;
            padding: 0;
            margin: 0;
        }
        
        .toc-item {
            margin-bottom: 8px;
            position: relative;
        }
        
        .toc-link {
            display: block;
            padding: 8px 12px;
            color: var(--text-color);
            text-decoration: none;
            border-radius: 5px;
            transition: all 0.2s ease;
            font-size: 0.95rem;
        }
        
        .toc-link:hover {
            background-color: rgba(231, 76, 60, 0.1);
            color: var(--secondary-color);
            transform: translateX(5px);
        }
        
        .toc-link.active {
            background-color: rgba(231, 76, 60, 0.2);
            color: var(--secondary-color);
            font-weight: 600;
            border-left: 3px solid var(--secondary-color);
        }
        
        .toc-sublist {
            list-style-type: none;
            padding-left: 15px;
            margin-top: 5px;
            display: none;
        }
        
        .toc-item.expanded .toc-sublist {
            display: block;
        }
        
        .toc-toggle {
            position: absolute;
            right: 10px;
            top: 8px;
            cursor: pointer;
            color: var(--accent-color);
            font-size: 0.8rem;
            transition: transform 0.2s ease;
        }
        
        .toc-item.expanded .toc-toggle {
            transform: rotate(90deg);
        }
        
        /* Main Content Styles */
        #content {
            flex: 1;
            background-color: var(--card-bg);
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            padding: 30px;
        }
        
        h1 {
            color: var(--primary-color);
            text-align: center;
            border-bottom: 3px solid var(--secondary-color);
            padding-bottom: 15px;
            margin-bottom: 30px;
            font-size: 2.2rem;
        }
        
        h2 {
            color: var(--accent-color);
            border-left: 5px solid var(--secondary-color);
            padding-left: 15px;
            margin-top: 40px;
            font-size: 1.6rem;
            scroll-margin-top: 80px;
        }
        
        h3 {
            color: #16a085;
            margin-top: 25px;
            font-size: 1.3rem;
        }
        
        .section {
            margin-bottom: 40px;
        }
        
        /* Interactive Elements */
        .mcq {
            background-color: #f0f8ff;
            border-left: 4px solid var(--accent-color);
            padding: 20px;
            margin: 25px 0;
            border-radius: 0 8px 8px 0;
            transition: all 0.3s ease;
        }
        
        .mcq:hover {
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        
        .question {
            font-weight: bold;
            margin-bottom: 15px;
            font-size: 1.1rem;
        }
        
        .options {
            margin-left: 20px;
        }
        
        .options p {
            margin: 10px 0;
            padding: 8px;
            border-radius: 5px;
            transition: background-color 0.2s ease;
        }
        
        .options p:hover {
            background-color: rgba(52, 152, 219, 0.1);
        }
        
        .answer {
            background-color: #e8f8f5;
            padding: 15px;
            margin-top: 15px;
            border-radius: 8px;
            display: none;
            animation: fadeIn 0.3s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .show-answer {
            background-color: #27ae60;
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
            font-size: 0.95rem;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .show-answer:hover {
            background-color: #2ecc71;
            transform: translateY(-2px);
        }
        
        .show-answer i {
            font-size: 0.9rem;
        }
        
        /* Diagrams and Visuals */
        .diagram {
            text-align: center;
            margin: 25px 0;
            background-color: #f5f5f5;
            padding: 20px;
            border-radius: 8px;
            box-shadow: inset 0 0 10px rgba(0,0,0,0.05);
        }
        
        .diagram img {
            max-width: 100%;
            height: auto;
            border: 1px solid #ddd;
            border-radius: 5px;
            transition: transform 0.3s ease;
        }
        
        .diagram img:hover {
            transform: scale(1.02);
        }
        
        .caption {
            font-style: italic;
            margin-top: 12px;
            font-size: 0.9rem;
            color: #666;
        }
        
        /* Tables */
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 25px 0;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }
        
        table, th, td {
            border: 1px solid #ddd;
        }
        
        th, td {
            padding: 12px 15px;
            text-align: left;
        }
        
        th {
            background-color: var(--accent-color);
            color: white;
            font-weight: 600;
        }
        
        tr:nth-child(even) {
            background-color: #f2f2f2;
        }
        
        tr:hover {
            background-color: rgba(52, 152, 219, 0.1);
        }
        
        /* Key Points */
        .key-point {
            background-color: #fffde7;
            border-left: 4px solid #ffd600;
            padding: 20px;
            margin: 25px 0;
            border-radius: 0 8px 8px 0;
            position: relative;
        }
        
        .key-point h4 {
            margin-top: 0;
            color: #f39c12;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .key-point h4 i {
            color: #f39c12;
        }
        
        /* Process Steps */
        .process-steps {
            counter-reset: step;
            margin: 25px 0;
        }
        
        .process-step {
            position: relative;
            padding-left: 60px;
            margin-bottom: 25px;
            min-height: 50px;
        }
        
        .process-step:before {
            counter-increment: step;
            content: counter(step);
            position: absolute;
            left: 0;
            top: 0;
            background-color: var(--secondary-color);
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            text-align: center;
            line-height: 40px;
            font-weight: bold;
            font-size: 1.1rem;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        
        /* Comparison Sections */
        .comparison {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin: 25px 0;
            gap: 20px;
        }
        
        .comparison-item {
            flex: 1;
            min-width: 300px;
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .comparison-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.15);
        }
        
        .comparison-item h4 {
            color: #8e44ad;
            border-bottom: 2px solid #9b59b6;
            padding-bottom: 8px;
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
            background: var(--secondary-color);
            width: 0%;
            transition: width 0.1s ease;
        }
        
        /* Back to Top Button */
        #back-to-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: var(--secondary-color);
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
            z-index: 999;
        }
        
        #back-to-top.visible {
            opacity: 1;
            visibility: visible;
        }
        
        #back-to-top:hover {
            background-color: #c0392b;
            transform: translateY(-3px);
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .container {
                flex-direction: column;
            }
            
            #toc-container {
                width: 100%;
                position: static;
                margin-bottom: 30px;
                max-height: none;
            }
            
            #content {
                padding: 20px;
            }
        }
        
        @media (max-width: 768px) {
            .comparison-item {
                min-width: 100%;
            }
            
            h1 {
                font-size: 1.8rem;
            }
            
            h2 {
                font-size: 1.4rem;
            }
        }
        
        /* Animation Classes */
        .fade-in {
            animation: fadeIn 0.5s ease forwards;
        }
        
        .slide-up {
            animation: slideUp 0.5s ease forwards;
        }
        
        @keyframes slideUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Print Styles */
        @media print {
            #toc-container, #back-to-top, .progress-container {
                display: none;
            }
            
            .container {
                display: block;
            }
            
            .show-answer, .toc-toggle {
                display: none;
            }
            
            .answer {
                display: block !important;
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
    <div id="back-to-top">
        <i class="fas fa-arrow-up"></i>
    </div>
    
    <div class="container">
        <!-- Table of Contents -->
        <div id="toc-container">
            <div id="toc-title">
                <i class="fas fa-list-ul"></i>
                Table of Contents
            </div>
            <ul class="toc-list" id="toc">
                <!-- TOC will be populated by JavaScript -->
            </ul>
        </div>
        
        <!-- Main Content -->
        <div id="content">
            <h1>Iron Making - Interactive eNotes</h1>
            
            <!-- Introduction Section -->
            <div class="section" id="introduction">
                <h2>1. Introduction to Iron Making</h2>
                <p>Iron making is the process of producing iron from iron ore through reduction reactions in blast furnaces or direct reduction plants. Iron is one of the most important metals in modern industry, serving as the primary raw material for steel production.</p>
                
                <div class="key-point">
                    <h4><i class="fas fa-lightbulb"></i> Key Historical Note</h4>
                    <p>The production of iron dates back to around 1200 BC, marking the beginning of the Iron Age. Modern iron making began with the development of the blast furnace in the 14th century.</p>
                </div>
                
                <div class="mcq">
                    <div class="question">1. What is the primary purpose of iron making?</div>
                    <div class="options">
                        <p>A) To extract pure iron from its ores</p>
                        <p>B) To produce steel directly from iron ore</p>
                        <p>C) To reduce iron oxides to metallic iron</p>
                        <p>D) To alloy iron with carbon for immediate use</p>
                    </div>
                    <button class="show-answer" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
                    <div class="answer">
                        <p><strong>Correct Answer: C) To reduce iron oxides to metallic iron</strong></p>
                        <p>Explanation: The primary purpose of iron making is the reduction of iron oxides (Fe₂O₃, Fe₃O₄) present in iron ore to metallic iron (Fe). This is typically done through chemical reduction using carbon monoxide in a blast furnace.</p>
                    </div>
                </div>
            </div>
            
            <!-- Raw Materials Section -->
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
                    <div class="question">2. Which of the following iron ores has the highest iron content?</div>
                    <div class="options">
                        <p>A) Hematite (Fe₂O₃)</p>
                        <p>B) Magnetite (Fe₃O₄)</p>
                        <p>C) Limonite (FeO(OH)·nH₂O)</p>
                        <p>D) Siderite (FeCO₃)</p>
                    </div>
                    <button class="show-answer" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
                    <div class="answer">
                        <p><strong>Correct Answer: B) Magnetite (Fe₃O₄)</strong></p>
                        <p>Explanation: Magnetite typically contains 60-70% iron by weight, which is higher than hematite (50-65%), limonite (35-50%), and siderite (30-40%).</p>
                    </div>
                </div>
            </div>
            
            <!-- Blast Furnace Section -->
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
                    <div class="question">3. Which reaction is primarily responsible for producing carbon monoxide in the blast furnace?</div>
                    <div class="options">
                        <p>A) Fe₂O₃ + CO → 2Fe₃O₄ + CO₂</p>
                        <p>B) C + CO₂ → 2CO</p>
                        <p>C) FeO + C → Fe + CO</p>
                        <p>D) CaCO₃ → CaO + CO₂</p>
                    </div>
                    <button class="show-answer" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
                    <div class="answer">
                        <p><strong>Correct Answer: B) C + CO₂ → 2CO</strong></p>
                        <p>Explanation: This is the Boudouard reaction, which is crucial for generating the reducing gas (CO) in the blast furnace. The other options either consume CO or produce CO₂.</p>
                    </div>
                </div>
            </div>
            
            <!-- Alternative Processes Section -->
            <div class="section" id="alternative-processes">
                <h2>4. Alternative Iron Making Processes</h2>
                
                <div class="comparison">
                    <div class="comparison-item">
                        <h4>4.1 Direct Reduction Processes</h4>
                        <p>Produce solid metallic iron (DRI - Direct Reduced Iron) without melting:</p>
                        <ul>
                            <li><strong>Midrex Process</strong>: Uses reformed natural gas (H₂ + CO) in shaft furnace</li>
                            <li><strong>HYL Process</strong>: Uses hydrogen-rich gas in retorts</li>
                            <li><strong>SL/RN Process</strong>: Rotary kiln using coal as reductant</li>
                        </ul>
                        <p><strong>Advantages:</strong> Lower capital cost, flexibility in raw materials, lower emissions</p>
                        <p><strong>Disadvantages:</strong> Requires high-grade ore, produces lower carbon iron</p>
                    </div>
                    
                    <div class="comparison-item">
                        <h4>4.2 Smelting Reduction Processes</h4>
                        <p>Combine ore reduction and melting in single unit:</p>
                        <ul>
                            <li><strong>COREX Process</strong>: Two-stage process with reduction shaft and melter-gasifier</li>
                            <li><strong>FINEX Process</strong>: Fluidized bed reduction followed by melter-gasifier</li>
                            <li><strong>HIsarna Process</strong>: Cyclone converter furnace</li>
                        </ul>
                        <p><strong>Advantages:</strong> No coking plant needed, can use fine ores and non-coking coal</p>
                        <p><strong>Disadvantages:</strong> Higher energy consumption, operational complexity</p>
                    </div>
                </div>
                
                <div class="mcq">
                    <div class="question">4. Which of the following processes produces solid metallic iron (DRI) rather than liquid iron?</div>
                    <div class="options">
                        <p>A) COREX process</p>
                        <p>B) Blast furnace process</p>
                        <p>C) Midrex process</p>
                        <p>D) HIsarna process</p>
                    </div>
                    <button class="show-answer" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
                    <div class="answer">
                        <p><strong>Correct Answer: C) Midrex process</strong></p>
                        <p>Explanation: The Midrex process is a direct reduction process that produces solid DRI (Direct Reduced Iron), while the other options produce liquid iron.</p>
                    </div>
                </div>
            </div>
            
            <!-- Physical Chemistry Section -->
            <div class="section" id="physical-chemistry">
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
                
                <div class="mcq">
                    <div class="question">5. Below what temperature does FeO become unstable in the iron oxide reduction sequence?</div>
                    <div class="options">
                        <p>A) 300°C</p>
                        <p>B) 570°C</p>
                        <p>C) 900°C</p>
                        <p>D) 1200°C</p>
                    </div>
                    <button class="show-answer" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
                    <div class="answer">
                        <p><strong>Correct Answer: B) 570°C</strong></p>
                        <p>Explanation: Below 570°C, FeO is thermodynamically unstable, and Fe₃O₄ reduces directly to Fe without forming FeO as an intermediate.</p>
                    </div>
                </div>
            </div>
            
            <!-- Modern Developments Section -->
            <div class="section" id="modern-developments">
                <h2>6. Modern Developments in Iron Making</h2>
                
                <h3>6.1 Energy Efficiency Improvements</h3>
                <ul>
                    <li><strong>Top pressure recovery turbines (TRT)</strong>: Generate electricity from blast furnace top gas pressure</li>
                    <li><strong>Pulverized coal injection (PCI)</strong>: Reduces coke consumption by up to 30%</li>
                    <li><strong>Waste heat recovery</strong>: Utilization of slag and gas heat</li>
                </ul>
                
                <h3>6.2 Environmental Considerations</h3>
                <ul>
                    <li><strong>CO₂ emissions reduction</strong>: Through process optimization and carbon capture</li>
                    <li><strong>Slag utilization</strong>: 100% of blast furnace slag can be utilized (cement, road construction)</li>
                    <li><strong>Dust recycling</strong>: Recycling of blast furnace and BOF dusts</li>
                </ul>
                
                <h3>6.3 Industry 4.0 Applications</h3>
                <ul>
                    <li><strong>Digital twins</strong>: Virtual models of blast furnaces for optimization</li>
                    <li><strong>AI-based process control</strong>: Predictive models for furnace operation</li>
                    <li><strong>Automated quality control</strong>: Machine vision for slag and hot metal analysis</li>
                </ul>
                
                <div class="mcq">
                    <div class="question">6. Which technology can reduce coke consumption in blast furnaces by injecting alternative carbon sources?</div>
                    <div class="options">
                        <p>A) TRT (Top Recovery Turbine)</p>
                        <p>B) PCI (Pulverized Coal Injection)</p>
                        <p>C) DRI (Direct Reduced Iron)</p>
                        <p>D) BOF (Basic Oxygen Furnace)</p>
                    </div>
                    <button class="show-answer" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
                    <div class="answer">
                        <p><strong>Correct Answer: B) PCI (Pulverized Coal Injection)</strong></p>
                        <p>Explanation: PCI technology injects pulverized coal into the blast furnace tuyeres, replacing part of the coke requirement while maintaining the necessary reducing conditions.</p>
                    </div>
                </div>
            </div>
            
            <!-- Quality Control Section -->
            <div class="section" id="quality-control">
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
                
                <div class="mcq">
                    <div class="question">7. What is the typical basicity ratio (CaO/SiO₂) of blast furnace slag?</div>
                    <div class="options">
                        <p>A) 0.5-0.7</p>
                        <p>B) 1.0-1.2</p>
                        <p>C) 1.5-1.8</p>
                        <p>D) 2.0-2.5</p>
                    </div>
                    <button class="show-answer" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
                    <div class="answer">
                        <p><strong>Correct Answer: B) 1.0-1.2</strong></p>
                        <p>Explanation: Blast furnace slag typically has a basicity ratio (CaO/SiO₂) of 1.0-1.2, which provides good sulfur removal capability while maintaining proper fluidity.</p>
                    </div>
                </div>
            </div>
            
            <!-- Safety Section -->
            <div class="section" id="safety-environment">
                <h2>8. Safety and Environmental Aspects</h2>
                
                <h3>8.1 Safety Considerations</h3>
                <ul>
                    <li><strong>High temperature hazards</strong>: Proper PPE and barriers</li>
                    <li><strong>Gas hazards</strong>: CO poisoning prevention</li>
                    <li><strong>Molten metal hazards</strong>: Prevention of explosions from moisture contact</li>
                </ul>
                
                <h3>8.2 Environmental Impact and Mitigation</h3>
                <ul>
                    <li><strong>Air emissions</strong>: Particulates, CO, CO₂, SOₓ, NOₓ</li>
                    <li><strong>Waste management</strong>: Slag, dust, and sludge utilization</li>
                    <li><strong>Water usage</strong>: Closed-loop cooling systems</li>
                    <li><strong>Energy efficiency</strong>: Heat recovery systems</li>
                </ul>
                
                <div class="mcq">
                    <div class="question">8. What is the primary gas hazard in iron making operations?</div>
                    <div class="options">
                        <p>A) Oxygen</p>
                        <p>B) Nitrogen</p>
                        <p>C) Carbon monoxide</p>
                        <p>D) Carbon dioxide</p>
                    </div>
                    <button class="show-answer" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
                    <div class="answer">
                        <p><strong>Correct Answer: C) Carbon monoxide</strong></p>
                        <p>Explanation: CO is a colorless, odorless, and highly toxic gas produced in large quantities during iron making. It's the primary gas hazard due to its ability to form carboxyhemoglobin in blood, preventing oxygen transport.</p>
                    </div>
                </div>
            </div>
            
            <!-- Future Trends Section -->
            <div class="section" id="future-trends">
                <h2>9. Future Trends in Iron Making</h2>
                
                <h3>9.1 Hydrogen-Based Iron Making</h3>
                <p>Using hydrogen as a reducing agent instead of carbon:</p>
                <ul>
                    <li>Fe₂O₃ + 3H₂ → 2Fe + 3H₂O</li>
                    <li>Potential for near-zero CO₂ emissions if green hydrogen is used</li>
                    <li>HYBRIT (Sweden) and other pilot projects underway</li>
                </ul>
                
                <h3>9.2 Carbon Capture and Utilization (CCU)</h3>
                <ul>
                    <li>Capture of CO₂ from blast furnace gases</li>
                    <li>Utilization in chemical synthesis or mineralization</li>
                    <li>Storage in geological formations (CCS)</li>
                </ul>
                
                <h3>9.3 Increased Use of Biomass</h3>
                <ul>
                    <li>Partial replacement of coke with charcoal</li>
                    <li>Carbon-neutral if from sustainable sources</li>
                    <li>Technical challenges in maintaining furnace permeability</li>
                </ul>
                
                <div class="mcq">
                    <div class="question">9. Which emerging iron making technology has the potential for near-zero CO₂ emissions when using renewable energy?</div>
                    <div class="options">
                        <p>A) Increased PCI rates</p>
                        <p>B) Hydrogen-based reduction</p>
                        <p>C) Higher blast temperatures</p>
                        <p>D) Oxygen enrichment</p>
                    </div>
                    <button class="show-answer" onclick="toggleAnswer(this)"><i class="fas fa-eye"></i> Show Answer</button>
                    <div class="answer">
                        <p><strong>Correct Answer: B) Hydrogen-based reduction</strong></p>
                        <p>Explanation: Hydrogen-based reduction produces water vapor instead of CO₂ as the byproduct. When the hydrogen is produced via electrolysis using renewable electricity, the process can achieve near-zero CO₂ emissions.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <script>
        // Table of Contents Generation
        document.addEventListener('DOMContentLoaded', function() {
            const toc = document.getElementById('toc');
            const sections = document.querySelectorAll('.section');
            const headings = ['h2', 'h3'];
            
            sections.forEach(section => {
                const sectionId = section.id;
                const sectionTitle = section.querySelector('h2').textContent;
                
                // Create main TOC item
                const tocItem = document.createElement('li');
                tocItem.className = 'toc-item';
                
                const tocLink = document.createElement('a');
                tocLink.href = `#${sectionId}`;
                tocLink.className = 'toc-link';
                tocLink.textContent = sectionTitle;
                
                // Check if section has subsections (h3 elements)
                const subHeadings = section.querySelectorAll('h3');
                if (subHeadings.length > 0) {
                    const toggle = document.createElement('span');
                    toggle.className = 'toc-toggle';
                    toggle.innerHTML = '<i class="fas fa-chevron-right"></i>';
                    toggle.addEventListener('click', function(e) {
                        e.preventDefault();
                        e.stopPropagation();
                        this.parentElement.classList.toggle('expanded');
                    });
                    
                    const subList = document.createElement('ul');
                    subList.className = 'toc-sublist';
                    
                    subHeadings.forEach(subHeading => {
                        const subItem = document.createElement('li');
                        const subLink = document.createElement('a');
                        subLink.href = `#${subHeading.parentElement.id || subHeading.id}`;
                        subLink.className = 'toc-link';
                        subLink.textContent = subHeading.textContent;
                        subItem.appendChild(subLink);
                        subList.appendChild(subItem);
                    });
                    
                    tocItem.appendChild(tocLink);
                    tocItem.appendChild(toggle);
                    tocItem.appendChild(subList);
                } else {
                    tocItem.appendChild(tocLink);
                }
                
                toc.appendChild(tocItem);
            });
            
            // Smooth scrolling for TOC links
            document.querySelectorAll('.toc-link').forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Update URL without page jump
                    history.pushState(null, null, targetId);
                });
            });
            
            // Set active TOC item based on scroll position
            function setActiveTOCItem() {
                const scrollPosition = window.scrollY + 100;
                
                document.querySelectorAll('.section').forEach(section => {
                    const sectionTop = section.offsetTop;
                    const sectionHeight = section.offsetHeight;
                    const sectionId = section.id;
                    
                    if (scrollPosition >= sectionTop && scrollPosition < sectionTop + sectionHeight) {
                        document.querySelectorAll('.toc-link').forEach(link => {
                            link.classList.remove('active');
                            if (link.getAttribute('href') === `#${sectionId}`) {
                                link.classList.add('active');
                                
                                // Expand parent if in sublist
                                const parentItem = link.closest('.toc-item');
                                if (parentItem && parentItem.querySelector('.toc-sublist')) {
                                    parentItem.classList.add('expanded');
                                }
                            }
                        });
                    }
                });
            }
            
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
            
            // Toggle answer visibility
            window.toggleAnswer = function(button) {
                const answer = button.nextElementSibling;
                if (answer.style.display === "block") {
                    answer.style.display = "none";
                    button.innerHTML = '<i class="fas fa-eye"></i> Show Answer';
                } else {
                    answer.style.display = "block";
                    button.innerHTML = '<i class="fas fa-eye-slash"></i> Hide Answer';
                }
            };
            
            // Initialize
            setActiveTOCItem();
            toggleBackToTop();
            
            // Event listeners
            window.addEventListener('scroll', function() {
                setActiveTOCItem();
                updateProgressBar();
                toggleBackToTop();
            });
            
            // Highlight TOC item when navigating via URL hash
            if (window.location.hash) {
                const targetElement = document.querySelector(window.location.hash);
                if (targetElement) {
                    setTimeout(() => {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }, 100);
                }
            }
        });
    </script>
</body>
</html>
