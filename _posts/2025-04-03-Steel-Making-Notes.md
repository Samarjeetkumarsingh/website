<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Steel Making - TestUrSelf</title>
    <style>
        :root {
            --primary-color: #d32f2f;
            --secondary-color: #ffa000;
            --accent-color: #f44336;
            --light-color: #ffebee;
            --dark-color: #b71c1c;
            --text-color: #212121;
            --highlight-color: #ffc107;
            --success-color: #4caf50;
            --error-color: #f44336;
            --process-color: #2196f3;
            --eaf-color: #9c27b0;
            --bof-color: #ff5722;
            --secondary-process-color: #009688;
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
            background: linear-gradient(135deg, #ffebee 0%, #ffcdd2 50%, #ffebee 100%);
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
            content: "STEEL";
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-30deg);
            font-size: 180px;
            font-weight: bold;
            color: rgba(211, 47, 47, 0.05);
            z-index: -1;
            pointer-events: none;
            white-space: nowrap;
            text-transform: uppercase;
            letter-spacing: 20px;
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
            background: linear-gradient(135deg, #d32f2f, #b71c1c);
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
                rgba(255,255,255,0.2) 50%,
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
            font-size: 3.5rem;
            font-weight: 900;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            letter-spacing: 2px;
            text-transform: uppercase;
        }
        
        h2 {
            color: var(--primary-color);
            border-bottom: 4px solid var(--highlight-color);
            padding-bottom: 0.8rem;
            margin-top: 3rem;
            font-size: 2.4rem;
            background: linear-gradient(to right, transparent, #ffebee, transparent);
            padding: 1rem 0;
            text-align: center;
            border-radius: 8px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }
        
        h3 {
            color: var(--dark-color);
            margin-top: 2.5rem;
            font-size: 1.8rem;
            border-left: 6px solid var(--highlight-color);
            padding-left: 1.5rem;
            position: relative;
        }
        
        h3::before {
            content: "";
            position: absolute;
            left: 0;
            bottom: -5px;
            width: 50%;
            height: 3px;
            background: linear-gradient(to right, var(--highlight-color), transparent);
        }
        
        .section {
            background-color: white;
            border-radius: 12px;
            padding: 2.5rem;
            margin-bottom: 3rem;
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
            position: relative;
            z-index: 1;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(0,0,0,0.05);
            overflow: hidden;
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }
        
        /* MCQ Styling - Enhanced with Vibrant Colors */
        .mcq {
            background-color: rgba(255, 235, 59, 0.1);
            border-left: 5px solid var(--highlight-color);
            padding: 1.5rem;
            margin: 2rem 0;
            border-radius: 0 8px 8px 0;
            transition: all 0.3s ease;
            position: relative;
        }
        
        .mcq:hover {
            background-color: rgba(255, 235, 59, 0.15);
        }
        
        .question {
            font-weight: 700;
            font-size: 1.2rem;
            margin-bottom: 1.2rem;
            color: var(--dark-color);
            position: relative;
            padding-left: 1.5rem;
        }
        
        .question::before {
            content: "?";
            position: absolute;
            left: 0;
            top: 0;
            color: var(--primary-color);
            font-weight: bold;
            font-size: 1.3rem;
        }
        
        .options {
            display: grid;
            gap: 10px;
        }
        
        .option {
            padding: 12px 18px;
            background-color: white;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s ease;
            border: 2px solid #e0e0e0;
            position: relative;
            font-weight: 500;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
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
            transform: translateX(5px) translateY(0);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            border-color: var(--highlight-color);
        }
        
        .option.correct {
            background-color: rgba(76, 175, 80, 0.2);
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
            background-color: rgba(244, 67, 54, 0.1);
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
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 8px;
            margin-top: 0;
        }
        
        .answer.show {
            max-height: 500px;
            padding: 1.5rem;
            margin-top: 1.5rem;
            border: 2px solid var(--highlight-color);
            animation: pulse 1.5s infinite alternate;
        }
        
        @keyframes pulse {
            0% {box-shadow: 0 0 0 0 rgba(255, 235, 59, 0.4);}
            100% {box-shadow: 0 0 0 10px rgba(255, 235, 59, 0);}
        }
        
        .answer-content {
            padding: 1rem;
        }
        
        .answer-content strong {
            color: var(--primary-color);
        }
        
        .show-answer-btn {
            background: linear-gradient(to right, var(--primary-color), var(--accent-color));
            color: white;
            border: none;
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            cursor: pointer;
            margin-top: 1.5rem;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 8px rgba(211, 47, 47, 0.3);
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .show-answer-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(211, 47, 47, 0.4);
        }
        
        .show-answer-btn:active {
            transform: translateY(1px);
        }
        
        /* Content Boxes */
        .key-point {
            background: linear-gradient(to right, #fff3e0, #ffe0b2);
            border-left: 6px solid var(--secondary-color);
            padding: 1.8rem;
            margin: 2.5rem 0;
            border-radius: 0 10px 10px 0;
            position: relative;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        
        .key-point::before {
            content: "!";
            position: absolute;
            left: -20px;
            top: -20px;
            width: 40px;
            height: 40px;
            background: linear-gradient(to bottom right, var(--secondary-color), var(--accent-color));
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 1.5rem;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        
        .diagram {
            background-color: white;
            padding: 1.5rem;
            border-radius: 10px;
            margin: 2rem 0;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            border: 1px solid #e0e0e0;
            transition: transform 0.3s ease;
        }
        
        .diagram:hover {
            transform: scale(1.02);
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
        }
        
        .diagram img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            border: 1px solid #eee;
        }
        
        .caption {
            font-style: italic;
            color: #666;
            margin-top: 1rem;
            font-size: 0.95rem;
            text-align: center;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 2.5rem 0;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            border-radius: 10px;
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
            letter-spacing: 1px;
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
            padding-left: 5rem;
            margin-bottom: 2.5rem;
            min-height: 3rem;
            background-color: rgba(33, 150, 243, 0.05);
            padding: 1.5rem;
            border-radius: 8px;
            border-left: 4px solid var(--process-color);
        }
        
        .process-step::before {
            counter-increment: step;
            content: counter(step);
            position: absolute;
            left: 1.5rem;
            top: 1.5rem;
            width: 2.5rem;
            height: 2.5rem;
            background: linear-gradient(to bottom right, var(--process-color), #0d47a1);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 1.2rem;
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
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
            border-top: 5px solid var(--primary-color);
        }
        
        .comparison-item.eaf {
            border-top-color: var(--eaf-color);
        }
        
        .comparison-item.bof {
            border-top-color: var(--bof-color);
        }
        
        .comparison-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }
        
        /* About TestUrSelf Section */
        .about-section {
            background: linear-gradient(135deg, #673ab7, #512da8);
            color: white;
            padding: 3rem;
            border-radius: 12px;
            margin-top: 4rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            position: relative;
            overflow: hidden;
        }
        
        .about-section::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path fill="rgba(255,255,255,0.05)" d="M0,0 L100,0 L100,100 L0,100 Z" /></svg>');
            background-size: cover;
        }
        
        .about-section h2 {
            color: white;
            border-bottom: 3px solid var(--highlight-color);
            text-align: center;
            background: transparent;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 2rem;
            position: relative;
            z-index: 1;
        }
        
        .about-logo {
            flex: 1;
            text-align: center;
        }
        
        .about-logo i {
            font-size: 8rem;
            color: var(--highlight-color);
            text-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        
        .about-text {
            flex: 2;
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .feature {
            background-color: rgba(255,255,255,0.1);
            padding: 1.5rem;
            border-radius: 8px;
            text-align: center;
            transition: transform 0.3s ease;
            backdrop-filter: blur(5px);
        }
        
        .feature:hover {
            transform: translateY(-5px);
            background-color: rgba(255,255,255,0.15);
        }
        
        .feature i {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: var(--highlight-color);
        }
        
        /* Responsive adjustments */
        @media (max-width: 768px) {
            body {
                padding: 10px;
            }
            
            body::after {
                font-size: 100px;
            }
            
            header {
                padding: 2rem 1rem;
            }
            
            h1 {
                font-size: 2.5rem;
            }
            
            .section {
                padding: 1.5rem;
            }
            
            .comparison-item {
                min-width: 100%;
            }
            
            .process-step {
                padding-left: 4rem;
            }
            
            .process-step::before {
                left: 1rem;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .features {
                grid-template-columns: 1fr;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700;900&display=swap" rel="stylesheet">
</head>
<body>
    <header>
        <h1>Steel Making</h1>
        <p>Interactive Learning Experience | Test Your Knowledge</p>
    </header>

    <div class="section" id="introduction">
        <h2>1. Introduction to Steel Production</h2>
        <p>Steel making is the process of producing steel from iron ore and scrap. Steel is an alloy of iron and carbon, with the carbon content typically between 0.2% and 2.1% by weight. Modern steel production involves two main routes: the Basic Oxygen Furnace (BOF) route and the Electric Arc Furnace (EAF) route.</p>
        
        <div class="key-point">
            <h3>Key Fact</h3>
            <p>Steel is the world's most important engineering and construction material, with global production reaching over 1.8 billion metric tons annually. About 70% of steel is produced via the BOF route, while 30% comes from EAFs.</p>
        </div>
        
        <div class="mcq">
            <div class="question">What is the primary difference between iron and steel?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Steel contains only iron, while iron ore contains impurities</div>
                <div class="option" onclick="checkAnswer(this, false)">Iron is a natural mineral, while steel is synthetic</div>
                <div class="option" onclick="checkAnswer(this, true)">Steel is an iron-carbon alloy with controlled carbon content</div>
                <div class="option" onclick="checkAnswer(this, false)">There is no difference - the terms are interchangeable</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-bolt"></i> REVEAL ANSWER</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Steel is an iron-carbon alloy with controlled carbon content</strong></p>
                    <p>The key distinction is that steel is an alloy of iron with controlled amounts of carbon (typically 0.2-2.1%) and often other alloying elements, while pure iron or pig iron has higher carbon content and more impurities.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="production-routes">
        <h2>2. Steel Production Routes</h2>
        <p>There are two main routes for steel production, each with distinct characteristics and applications:</p>
        
        <div class="comparison">
            <div class="comparison-item bof">
                <h3>Basic Oxygen Furnace (BOF)</h3>
                <ul>
                    <li>Uses 70-80% liquid hot metal (from blast furnace) and 20-30% scrap</li>
                    <li>Oxygen is blown through the molten metal to reduce carbon content</li>
                    <li>Process takes about 40 minutes per heat</li>
                    <li>Produces high-quality steel for automotive and construction</li>
                    <li>Higher capital costs but lower operating costs</li>
                </ul>
            </div>
            
            <div class="comparison-item eaf">
                <h3>Electric Arc Furnace (EAF)</h3>
                <ul>
                    <li>Uses almost 100% scrap metal (or alternative iron sources)</li>
                    <li>Electric arcs melt the scrap (temperatures up to 3000°C)</li>
                    <li>Process takes about 90 minutes per heat</li>
                    <li>More flexible for specialty steel production</li>
                    <li>Lower capital costs but higher energy costs</li>
                </ul>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">Which steelmaking method primarily uses scrap metal as its raw material?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Basic Oxygen Furnace (BOF)</div>
                <div class="option" onclick="checkAnswer(this, true)">Electric Arc Furnace (EAF)</div>
                <div class="option" onclick="checkAnswer(this, false)">Both use primarily scrap metal</div>
                <div class="option" onclick="checkAnswer(this, false)">Neither uses scrap metal</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-bolt"></i> REVEAL ANSWER</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Electric Arc Furnace (EAF)</strong></p>
                    <p>EAFs use almost 100% scrap metal as their raw material, while BOFs use primarily liquid hot metal from blast furnaces (70-80%) with only 20-30% scrap.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="bof-process">
        <h2>3. Basic Oxygen Furnace (BOF) Process</h2>
        <p>The Basic Oxygen Steelmaking process is the dominant steel production method, capable of producing 200-400 tons of steel in a single heat lasting about 40 minutes.</p>
        
        <div class="process-steps">
            <div class="process-step">
                <h4>Charging</h4>
                <p>Scrap metal (20-30%) is loaded into the furnace first, followed by hot metal (70-80%) from the blast furnace at about 1300°C.</p>
            </div>
            
            <div class="process-step">
                <h4>Blowing</h4>
                <p>A water-cooled lance blows 99.5% pure oxygen at supersonic speeds onto the molten bath. This initiates several reactions:</p>
                <ul>
                    <li>Decarburization: C + ½O₂ → CO</li>
                    <li>Silicon oxidation: Si + O₂ → SiO₂</li>
                    <li>Phosphorus removal: 2P + 5O → P₂O₅</li>
                </ul>
            </div>
            
            <div class="process-step">
                <h4>Flux Addition</h4>
                <p>Lime (CaO) is added to form slag with impurities:</p>
                <ul>
                    <li>SiO₂ + CaO → CaSiO₃ (slag)</li>
                    <li>P₂O₅ + 3CaO → Ca₃(PO₄)₂ (slag)</li>
                </ul>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">What is the typical carbon content of steel when tapping from a BOF?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">0.5-1.0%</div>
                <div class="option" onclick="checkAnswer(this, false)">0.2-0.5%</div>
                <div class="option" onclick="checkAnswer(this, true)">0.04-0.08%</div>
                <div class="option" onclick="checkAnswer(this, false)">1.5-2.0%</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-bolt"></i> REVEAL ANSWER</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: 0.04-0.08%</strong></p>
                    <p>The BOF process reduces carbon content from about 4% in hot metal to 0.04-0.08% in the final steel product. Further adjustments can be made during secondary metallurgy.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="eaf-process">
        <h2>4. Electric Arc Furnace (EAF) Process</h2>
        <p>The Electric Arc Furnace is the primary method for recycling steel scrap, accounting for about 30% of global steel production.</p>
        
        <div class="process-steps">
            <div class="process-step">
                <h4>Furnace Charging</h4>
                <p>Scrap steel is loaded into the furnace using a large bucket. Different grades of scrap are carefully selected to achieve the desired steel composition.</p>
            </div>
            
            <div class="process-step">
                <h4>Melting</h4>
                <p>Three graphite electrodes create electric arcs with temperatures up to 3000°C, melting the scrap within 50-60 minutes. Chemical energy is often supplemented by oxy-fuel burners.</p>
            </div>
            
            <div class="process-step">
                <h4>Refining</h4>
                <p>Oxygen is lanced to remove impurities, and fluxes are added to form slag. The carbon content is adjusted by adding carbon or oxygen blowing.</p>
            </div>
        </div>
        
        <div class="key-point">
            <h3>Energy Efficiency</h3>
            <p>Modern EAFs consume about 350-400 kWh per ton of steel, compared to 20-25 GJ/ton for integrated steelmaking (BF-BOF route). The use of scrap reduces energy requirements by 70-75% compared to primary production.</p>
        </div>
        
        <div class="mcq">
            <div class="question">What is the primary advantage of EAF steelmaking compared to BOF?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Higher production capacity per furnace</div>
                <div class="option" onclick="checkAnswer(this, true)">Lower energy consumption and CO₂ emissions</div>
                <div class="option" onclick="checkAnswer(this, false)">Faster production cycle times</div>
                <div class="option" onclick="checkAnswer(this, false)">Better quality steel products</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-bolt"></i> REVEAL ANSWER</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Lower energy consumption and CO₂ emissions</strong></p>
                    <p>EAFs use about 70-75% less energy than BOFs because they melt scrap rather than reduce iron ore, resulting in significantly lower CO₂ emissions (0.4-0.6 tons CO₂/ton steel vs 1.8-2.2 tons for BOF).</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="secondary-metallurgy">
        <h2>5. Secondary Metallurgy Processes</h2>
        <p>After primary steelmaking, most steel undergoes secondary metallurgy to achieve precise composition and quality requirements.</p>
        
        <div class="comparison">
            <div class="comparison-item" style="border-top-color: var(--secondary-process-color);">
                <h3>Ladle Furnace</h3>
                <ul>
                    <li>Provides precise temperature control</li>
                    <li>Allows for composition adjustments</li>
                    <li>Enables deoxidation and desulfurization</li>
                    <li>Typical treatment time: 30-45 minutes</li>
                </ul>
            </div>
            
            <div class="comparison-item" style="border-top-color: var(--process-color);">
                <h3>Vacuum Degassing</h3>
                <ul>
                    <li>Removes hydrogen to prevent flaking</li>
                    <li>Reduces nitrogen and oxygen content</li>
                    <li>Essential for high-grade steels</li>
                    <li>Processes: RH, VD, VOD</li>
                </ul>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">Which secondary metallurgy process is essential for producing ultra-low carbon steels?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Ladle furnace treatment</div>
                <div class="option" onclick="checkAnswer(this, true)">Vacuum oxygen decarburization (VOD)</div>
                <div class="option" onclick="checkAnswer(this, false)">Argon stirring</div>
                <div class="option" onclick="checkAnswer(this, false)">Calcium treatment</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-bolt"></i> REVEAL ANSWER</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Vacuum oxygen decarburization (VOD)</strong></p>
                    <p>VOD combines vacuum treatment with oxygen blowing to achieve carbon contents below 0.01%, which is essential for producing ultra-low carbon stainless steels and electrical steels.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="casting">
        <h2>6. Continuous Casting</h2>
        <p>Continuous casting revolutionized steel production by directly converting molten steel into semi-finished products (slabs, blooms, billets).</p>
        
        <div class="process-steps">
            <div class="process-step">
                <h4>Tundish</h4>
                <p>Molten steel from the ladle flows into a tundish that distributes it to the molds while maintaining steady flow and removing inclusions.</p>
            </div>
            
            <div class="process-step">
                <h4>Water-Cooled Mold</h4>
                <p>The mold gives the initial shape and forms a solid shell while the interior remains liquid. Mold oscillation prevents sticking.</p>
            </div>
            
            <div class="process-step">
                <h4>Secondary Cooling</h4>
                <p>Water sprays complete solidification while supporting the strand with rollers. Cooling rates affect microstructure and quality.</p>
            </div>
        </div>
        
        <div class="key-point">
            <h3>Yield Improvement</h3>
            <p>Continuous casting improved yields from 80-85% with ingot casting to 95-98% by eliminating ingot molds and primary mills, while also reducing energy consumption by about 30%.</p>
        </div>
    </div>

    <div class="about-section">
        <h2>About TestUrSelf</h2>
        <div class="about-content">
            <div class="about-logo">
                <i class="fas fa-graduation-cap"></i>
            </div>
            <div class="about-text">
                <p>TestUrSelf: Consistently Producing AIR-1 in GATE Since 2019

TestUrSelf is a premier online learning platform dedicated to helping engineering aspirants crack competitive exams like GATE (Graduate Aptitude Test in Engineering) and other PSU exams with outstanding results. Since 2019, TestUrSelf has been the backbone behind numerous top rankers, including AIR-1 holders in GATE, showcasing its unparalleled expertise in exam preparation.</p>
                
                <div class="features">
                    <div class="feature">
                        <i class="fas fa-bolt"></i>
                        <h4>Video Courses</h4>
                        <p>Engage with dynamic content that responds to your inputs</p>
                    </div>
                    <div class="feature">
                        <i class="fas fa-check-circle"></i>
                        <h4>Instant Feedback</h4>
                        <p>Get immediate validation of your understanding</p>
                    </div>
                    <div class="feature">
                        <i class="fas fa-chart-line"></i>
                        <h4>Progress Tracking</h4>
                        <p>Monitor your learning journey with detailed analytics</p>
                    </div>
                    <div class="feature">
                        <i class="fas fa-industry"></i>
                        <h4>Industrial Focus</h4>
                        <p>Content designed by industry experts for practical knowledge</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Enhanced MCQ functionality with immediate feedback
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
                option.style.boxShadow = '0 4px 8px rgba(76, 175, 80, 0.3)';
            } else {
                option.classList.add('incorrect');
                option.style.transform = 'scale(0.98)';
                option.style.boxShadow = '0 4px 8px rgba(244, 67, 54, 0.3)';
                
                // Find and highlight the correct answer
                const correctOption = Array.from(options).find(opt => 
                    opt.getAttribute('onclick').includes('true'));
                if (correctOption) {
                    correctOption.classList.add('correct');
                    correctOption.style.transform = 'scale(1.02)';
                    correctOption.style.boxShadow = '0 4px 8px rgba(76, 175, 80, 0.3)';
                }
            }
        }
        
        function toggleAnswer(button) {
            const answer = button.nextElementSibling;
            answer.classList.toggle('show');
            
            if (answer.classList.contains('show')) {
                button.innerHTML = '<i class="fas fa-eye-slash"></i> HIDE ANSWER';
                button.style.background = 'linear-gradient(to right, #f44336, #d32f2f)';
            } else {
                button.innerHTML = '<i class="fas fa-bolt"></i> REVEAL ANSWER';
                button.style.background = 'linear-gradient(to right, var(--primary-color), var(--accent-color))';
            }
        }
        
        // Animate options on page load
        document.addEventListener('DOMContentLoaded', function() {
            const options = document.querySelectorAll('.option');
            options.forEach((option, index) => {
                setTimeout(() => {
                    option.style.opacity = '1';
                    option.style.transform = 'translateY(0)';
                }, index * 100);
            });
        });
    </script>
</body>
</html>
