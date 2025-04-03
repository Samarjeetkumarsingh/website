<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mineral Beneficiation - TestUrSelf</title>
    <style>
        :root {
            --primary-color: #2E7D32;
            --secondary-color: #FF8F00;
            --accent-color: #1B5E20;
            --light-color: #E8F5E9;
            --dark-color: #1B5E20;
            --text-color: #212121;
            --highlight-color: #FFC107;
            --success-color: #388E3C;
            --error-color: #D32F2F;
            --process-color: #0288D1;
            --flotation-color: #7B1FA2;
            --gravity-color: #E65100;
            --formula-color: #5D4037;
            --magnetic-color: #1565C0;
            --leaching-color: #00838F;
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
            background: linear-gradient(135deg, #E8F5E9 0%, #C8E6C9 50%, #E8F5E9 100%);
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
            content: "MINERALS";
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-30deg);
            font-size: 150px;
            font-weight: bold;
            color: rgba(46, 125, 50, 0.05);
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
            background-color: rgba(46, 125, 50, 0.1);
            transform: translateX(5px);
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
            background-color: rgba(255, 235, 59, 0.2);
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
            0% {box-shadow: 0 0 0 0 rgba(255, 235, 59, 0.4);}
            100% {box-shadow: 0 0 0 10px rgba(255, 235, 59, 0);}
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
            box-shadow: 0 4px 8px rgba(46, 125, 50, 0.3);
        }
        
        .show-answer-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(46, 125, 50, 0.4);
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
            border-left: 4px solid var(--formula-color);
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
            background-color: var(--formula-color);
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
            background: linear-gradient(to bottom right, var(--process-color), #01579B);
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
            border-top: 5px solid var(--process-color);
            transition: transform 0.3s ease;
        }
        
        .method-card.flotation {
            border-top-color: var(--flotation-color);
        }
        
        .method-card.gravity {
            border-top-color: var(--gravity-color);
        }
        
        .method-card.magnetic {
            border-top-color: var(--magnetic-color);
        }
        
        .method-card.leaching {
            border-top-color: var(--leaching-color);
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
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700;900&display=swap" rel="stylesheet">
</head>
<body>
    <header>
        <h1>Mineral Beneficiation & Agglomeration</h1>
        <p>Master the processes that transform raw ores into valuable concentrates</p>
    </header>

    <div class="toc-container">
        <div class="toc">
            <h2>Table of Contents</h2>
            <ul>
                <li><a href="#comminution">1. Comminution Techniques</a></li>
                <li><a href="#classification">2. Size Classification</a></li>
                <li><a href="#concentration">3. Concentration Methods</a></li>
                <li><a href="#agglomeration">4. Agglomeration</a></li>
                <li><a href="#formulas">5. Key Formulas</a></li>
                <li><a href="#interactive">6. Process Diagram</a></li>
            </ul>
        </div>
    </div>

    <div class="section" id="comminution">
        <h2>1. Comminution Techniques</h2>
        <p>Comminution is the process of reducing ore size to liberate valuable minerals from gangue through crushing and grinding, accounting for 30-50% of total mineral processing costs.</p>
        
        <h3>1.1 Crushing (Coarse Size Reduction)</h3>
        <div class="process-steps">
            <div class="process-step">
                <h4>Primary Crushing</h4>
                <p><strong>Jaw Crushers:</strong> Reduce run-of-mine ore (150-250mm) to 50-100mm using compressive force between fixed and moving jaws</p>
                <p><strong>Gyratory Crushers:</strong> For high-capacity primary crushing (5000+ tph), consisting of a conical head gyrating inside a crushing chamber</p>
            </div>
            
            <div class="process-step">
                <h4>Secondary Crushing</h4>
                <p><strong>Cone Crushers:</strong> Further reduce to 10-30mm using a gyrating cone inside a bowl liner</p>
                <p><strong>Impact Crushers:</strong> Best for softer ores, using high-speed impact forces (hammers or blow bars)</p>
                <p><strong>High Pressure Grinding Rolls (HPGR):</strong> Emerging technology that compresses feed material between two counter-rotating rollers</p>
            </div>
        </div>
        
        <h3>1.2 Grinding (Fine Size Reduction)</h3>
        <table>
            <tr>
                <th>Equipment</th>
                <th>Particle Size</th>
                <th>Energy Consumption</th>
                <th>Key Features</th>
            </tr>
            <tr>
                <td>Ball Mills</td>
                <td>75-250 µm</td>
                <td>10-20 kWh/ton</td>
                <td>Steel balls as grinding media, wet/dry operation</td>
            </tr>
            <tr>
                <td>Rod Mills</td>
                <td>1-5 mm</td>
                <td>8-15 kWh/ton</td>
                <td>Steel rods as grinding media, prevents overgrinding</td>
            </tr>
            <tr>
                <td>SAG Mills</td>
                <td>80% <2mm</td>
                <td>15-25 kWh/ton</td>
                <td>Semi-autogenous, uses ore itself as grinding media</td>
            </tr>
            <tr>
                <td>HPGR</td>
                <td>1-20 mm</td>
                <td>30% less than ball mills</td>
                <td>Energy efficient, generates micro-cracks in particles</td>
            </tr>
        </table>
        
        <div class="key-point">
            <h3>Bond's Law of Comminution</h3>
            <p>The energy required to reduce particle size is proportional to the square root of the size reduction ratio:</p>
            <div class="formula-box">
                W = W<sub>i</sub> (10/√P<sub>80</sub> - 10/√F<sub>80</sub>)
            </div>
            <p>Where:</p>
            <ul>
                <li>W = Work input (kWh/ton)</li>
                <li>W<sub>i</sub> = Work index (material-specific constant)</li>
                <li>P<sub>80</sub> = Product size (µm) at 80% passing</li>
                <li>F<sub>80</sub> = Feed size (µm) at 80% passing</li>
            </ul>
            <p>Typical Work Index Values: Bauxite (8.8), Copper Ore (12.7), Iron Ore (13.5), Gold Ore (15.1)</p>
        </div>
        
        <div class="mcq">
            <div class="question">What is the primary purpose of comminution in mineral processing?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">To chemically separate minerals</div>
                <div class="option" onclick="checkAnswer(this, true)">To liberate valuable minerals from gangue</div>
                <div class="option" onclick="checkAnswer(this, false)">To increase the ore's chemical reactivity</div>
                <div class="option" onclick="checkAnswer(this, false)">To remove impurities through heating</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: To liberate valuable minerals from gangue</strong></p>
                    <p>Comminution breaks ore into smaller particles to free valuable minerals from the surrounding waste rock (gangue) for subsequent separation processes. The degree of liberation required depends on the mineral grain size and association with gangue minerals.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">Which crushing equipment is most suitable for primary crushing of hard, abrasive ores?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Cone crusher</div>
                <div class="option" onclick="checkAnswer(this, true)">Gyratory crusher</div>
                <div class="option" onclick="checkAnswer(this, false)">Impact crusher</div>
                <div class="option" onclick="checkAnswer(this, false)">Hammer mill</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Gyratory crusher</strong></p>
                    <p>Gyratory crushers are preferred for primary crushing of hard, abrasive ores due to their high capacity, robust construction, and ability to handle tough materials. They can process up to 12,000 tph and reduce feed sizes up to 1.5m down to 100-200mm.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="classification">
        <h2>2. Size Classification</h2>
        <p>Separating particles by size using screening or hydroclassification methods to ensure proper sizing for downstream processes.</p>
        
        <div class="method-card">
            <h3>2.1 Screening</h3>
            <p>Mechanical separation using apertures to sort particles by size:</p>
            <ul>
                <li><strong>Grizzly Screens:</strong> Coarse screening (>50mm) using parallel bars or rails</li>
                <li><strong>Trommel Screens:</strong> Rotating cylindrical screens for wet/dry materials (5-100mm)</li>
                <li><strong>Vibrating Screens:</strong> Most common for 0.5-50mm, with various motion types:
                    <ul>
                        <li>Linear motion - for precise cuts</li>
                        <li>Circular motion - for high capacity</li>
                        <li>Elliptical motion - for sticky materials</li>
                    </ul>
                </li>
                <li><strong>Flip-Flow Screens:</strong> For difficult-to-screen materials <1mm</li>
            </ul>
            
            <div class="formula-box">
                Screening Efficiency (%) = [(O<sub>u</sub> × (F<sub>f</sub> - O<sub>o</sub>)) / (F<sub>f</sub> × (O<sub>u</sub> - O<sub>o</sub>))] × 100
            </div>
            <p>Where O<sub>u</sub> is undersize in overflow, F<sub>f</sub> is undersize in feed, O<sub>o</sub> is undersize in underflow</p>
        </div>
        
        <div class="method-card">
            <h3>2.2 Hydroclassification</h3>
            <p>Separation based on particle settling rates in fluid (usually water):</p>
            <ul>
                <li><strong>Hydrocyclones:</strong> Centrifugal separation (10-300µm)
                    <ul>
                        <li>Feed pressure: 30-70 kPa</li>
                        <li>Cut size range: 10-300µm</li>
                        <li>Capacity: Up to 1000 m³/hr</li>
                    </ul>
                </li>
                <li><strong>Spiral Classifiers:</strong> Gravity-based settling (100-1000µm)
                    <ul>
                        <li>Single or double pitch designs</li>
                        <li>Slope: 12-18 degrees</li>
                    </ul>
                </li>
                <li><strong>Sedimentation:</strong> For very fine particles (<10µm)</li>
                <li><strong>Centrifugal Classifiers:</strong> For fine classification (5-100µm)</li>
            </ul>
            
            <div class="key-point">
                <h4>Cut Size (d<sub>50</sub>)</h4>
                <p>The particle size at which 50% reports to overflow and 50% to underflow. Critical parameter for classifier efficiency.</p>
                <div class="formula-box">
                    d<sub>50</sub> = K × (μ × D<sub>c</sub><sup>3</sup> / (Δρ × Q))<sup>0.5</sup>
                </div>
                <p>Where:</p>
                <ul>
                    <li>K = Cyclone design constant</li>
                    <li>μ = Fluid viscosity (Pa·s)</li>
                    <li>D<sub>c</sub> = Cyclone diameter (m)</li>
                    <li>Δρ = Density difference between particle and fluid (kg/m³)</li>
                    <li>Q = Volumetric feed rate (m³/s)</li>
                </ul>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">Which classification method is most suitable for particles smaller than 300µm?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Grizzly screens</div>
                <div class="option" onclick="checkAnswer(this, true)">Hydrocyclones</div>
                <div class="option" onclick="checkAnswer(this, false)">Trommel screens</div>
                <div class="option" onclick="checkAnswer(this, false)">Vibrating screens</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Hydrocyclones</strong></p>
                    <p>Hydrocyclones are effective for particle sizes between 10-300µm, while screens are generally used for coarser separations (>0.5mm). Hydrocyclones use centrifugal force to separate particles based on size and density differences.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">What happens to the cut size (d<sub>50</sub>) of a hydrocyclone when feed density increases?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Increases proportionally</div>
                <div class="option" onclick="checkAnswer(this, false)">Remains unchanged</div>
                <div class="option" onclick="checkAnswer(this, true)">Increases (coarser separation)</div>
                <div class="option" onclick="checkAnswer(this, false)">Decreases (finer separation)</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Increases (coarser separation)</strong></p>
                    <p>As feed density increases, the cut size (d<sub>50</sub>) increases because the higher solids content reduces the effective separation efficiency, resulting in coarser particles reporting to the overflow.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="concentration">
        <h2>3. Concentration Methods</h2>
        <p>Processes that separate valuable minerals from gangue based on physical or chemical properties.</p>
        
        <div class="method-card flotation">
            <h3>3.1 Froth Flotation</h3>
            <p>Process that selectively separates hydrophobic minerals from hydrophilic gangue using air bubbles (particle size range: 10-300µm).</p>
            
            <div class="process-steps">
                <div class="process-step">
                    <h4>Conditioning</h4>
                    <p>Add reagents to modify surface properties:
                        <ul>
                            <li><strong>Collectors:</strong> Make minerals hydrophobic (e.g., xanthates for sulfides)</li>
                            <li><strong>Frothers:</strong> Stabilize bubbles (e.g., MIBC, pine oil)</li>
                            <li><strong>Modifiers:</strong> Adjust pH (lime, sulfuric acid) or depress gangue</li>
                        </ul>
                    </p>
                </div>
                
                <div class="process-step">
                    <h4>Flotation</h4>
                    <p>Key parameters:
                        <ul>
                            <li>Air flow rate: 0.5-2 m³/min/m²</li>
                            <li>Impeller speed: 5-10 m/s tip speed</li>
                            <li>Residence time: 5-15 minutes</li>
                            <li>Pulp density: 25-45% solids</li>
                        </ul>
                    </p>
                </div>
                
                <div class="process-step">
                    <h4>Concentrate Collection</h4>
                    <p>Skim froth to recover mineral concentrate (typically 20-50% grade improvement)</p>
                </div>
            </div>
            
            <div class="formula-box">
                Recovery (%) = (C × c) / (F × f) × 100
            </div>
            <p>Where:</p>
            <ul>
                <li>C = Mass of concentrate</li>
                <li>c = Grade of concentrate</li>
                <li>F = Mass of feed</li>
                <li>f = Grade of feed</li>
            </ul>
            
            <div class="key-point">
                <h4>Flotation Kinetics</h4>
                <div class="formula-box">
                    R = R<sub>∞</sub>(1 - e<sup>-kt</sup>)
                </div>
                <p>Where R is recovery at time t, R<sub>∞</sub> is maximum possible recovery, k is rate constant</p>
            </div>
        </div>
        
        <div class="method-card gravity">
            <h3>3.2 Gravity Separation</h3>
            <p>Uses density differences between minerals (effective when ΔSG >1.0):</p>
            <ul>
                <li><strong>Jigs:</strong> Pulsating water flow (particle size: 0.5-50mm)
                    <ul>
                        <li>Pulsation rate: 50-300 strokes/min</li>
                        <li>Applications: Coal, tin, tungsten</li>
                    </ul>
                </li>
                <li><strong>Spirals:</strong> For 1-3mm particles
                    <ul>
                        <li>Slope: 10-20 degrees</li>
                        <li>Capacity: 1-3 tph per start</li>
                    </ul>
                </li>
                <li><strong>Shaking Tables:</strong> Precise separation (50µm-3mm)
                    <ul>
                        <li>Deck slope: 2-5 degrees</li>
                        <li>Stroke: 10-25mm</li>
                        <li>Frequency: 250-300 rpm</li>
                    </ul>
                </li>
                <li><strong>Centrifugal Concentrators:</strong> For fine gold (10-100µm)
                    <ul>
                        <li>G-force: 50-200G</li>
                        <li>Feed rate: 1-2 tph</li>
                    </ul>
                </li>
            </ul>
            
            <div class="formula-box">
                E = (ρ<sub>h</sub> - ρ<sub>f</sub>) / (ρ<sub>l</sub> - ρ<sub>f</sub>)
            </div>
            <p>Where E is separation efficiency, ρ<sub>h</sub> and ρ<sub>l</sub> are heavy/light mineral densities, ρ<sub>f</sub> is fluid density</p>
        </div>
        
        <div class="method-card magnetic">
            <h3>3.3 Magnetic Separation</h3>
            <p>Separates minerals based on magnetic susceptibility:</p>
            <ul>
                <li><strong>Low Intensity (0.1-0.3T):</strong> For ferromagnetic minerals (magnetite, pyrrhotite)</li>
                <li><strong>High Intensity (0.5-2T):</strong> For paramagnetic minerals (hematite, ilmenite)</li>
                <li><strong>High Gradient (>2T):</strong> For weakly magnetic minerals</li>
            </ul>
            
            <div class="formula-box">
                Magnetic Force: F<sub>m</sub> = μ<sub>0</sub>χVH(dH/dx)
            </div>
            <p>Where μ<sub>0</sub> is permeability of free space, χ is susceptibility, V is particle volume, H is field intensity</p>
        </div>
        
        <div class="method-card leaching">
            <h3>3.4 Leaching</h3>
            <p>Chemical dissolution of valuable minerals:</p>
            <ul>
                <li><strong>Cyanidation:</strong> For gold/silver (0.05-0.3% NaCN, pH 10-11)</li>
                <li><strong>Acid Leaching:</strong> For copper, uranium (pH 1.5-3.5)</li>
                <li><strong>Bacterial Leaching:</strong> For sulfide ores (Thiobacillus ferrooxidans)</li>
            </ul>
            
            <div class="formula-box">
                Gold Dissolution: 4Au + 8NaCN + O<sub>2</sub> + 2H<sub>2</sub>O → 4Na[Au(CN)<sub>2</sub>] + 4NaOH
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">Which chemical is commonly used as a collector in sulfide mineral flotation?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Sodium silicate</div>
                <div class="option" onclick="checkAnswer(this, true)">Potassium amyl xanthate</div>
                <div class="option" onclick="checkAnswer(this, false)">Calcium oxide</div>
                <div class="option" onclick="checkAnswer(this, false)">Polyacrylamide</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Potassium amyl xanthate</strong></p>
                    <p>Xanthates are the most common collectors for sulfide minerals, making them hydrophobic for flotation. Sodium silicate is a dispersant, calcium oxide is a pH modifier, and polyacrylamide is a flocculant.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">Which gravity separator is most effective for recovering fine gold particles?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Jig</div>
                <div class="option" onclick="checkAnswer(this, false)">Shaking table</div>
                <div class="option" onclick="checkAnswer(this, true)">Centrifugal concentrator</div>
                <div class="option" onclick="checkAnswer(this, false)">Spiral classifier</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Centrifugal concentrator</strong></p>
                    <p>Centrifugal concentrators use enhanced gravitational forces (50-200G) to recover fine gold particles (10-100µm) that are too small for conventional gravity methods.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="agglomeration">
        <h2>4. Agglomeration Techniques</h2>
        <p>Processes that bind fine particles into larger masses for improved handling and processing.</p>
        
        <h3>4.1 Sintering</h3>
        <div class="process-steps">
            <div class="process-step">
                <h4>Blending</h4>
                <p>Mix iron ore fines (0-10mm) with:
                    <ul>
                        <li>Coke breeze (5-8%) as fuel</li>
                        <li>Flux (10-15% limestone/dolomite)</li>
                        <li>Return fines (20-30%)</li>
                        <li>Moisture (6-8%)</li>
                    </ul>
                </p>
            </div>
            
            <div class="process-step">
                <h4>Ignition</h4>
                <p>Heat to 1300-1480°C to form partial melts:
                    <ul>
                        <li>Ignition hood temperature: 1100-1300°C</li>
                        <li>Burn-through point: 300-400°C</li>
                        <li>Sintering time: 15-30 minutes</li>
                    </ul>
                </p>
            </div>
            
            <div class="process-step">
                <h4>Cooling</h4>
                <p>Produce hard, porous lumps (5-50mm) with:
                    <ul>
                        <li>Cold crushing strength: 200-300 kg/cm²</li>
                        <li>Porosity: 40-50%</li>
                        <li>Reducibility index: 60-70%</li>
                    </ul>
                </p>
            </div>
        </div>
        
        <h3>4.2 Pelletizing</h3>
        <table>
            <tr>
                <th>Stage</th>
                <th>Process Parameters</th>
                <th>Equipment</th>
            </tr>
            <tr>
                <td>Balling</td>
                <td>
                    <ul>
                        <li>Green balls: 9-16mm diameter</li>
                        <li>Moisture: 8-10%</li>
                        <li>Bentonite binder: 0.5-1.5%</li>
                    </ul>
                </td>
                <td>Disc or drum pelletizers</td>
            </tr>
            <tr>
                <td>Induration</td>
                <td>
                    <ul>
                        <li>Drying: 100-400°C</li>
                        <li>Firing: 1250-1350°C</li>
                        <li>Cooling: 100-200°C</li>
                    </ul>
                </td>
                <td>Grate-kiln or straight grate</td>
            </tr>
        </table>
        
        <div class="formula-box">
            Cold Crushing Strength (kg/pellet) = F / (π × r<sup>2</sup>)
        </div>
        <p>Where F is crushing force (kg), r is pellet radius (cm)</p>
        
        <h3>4.3 Briquetting</h3>
        <div class="method-card">
            <p>Process that compacts fines into defined shapes using binders:</p>
            <ul>
                <li><strong>Binder Types:</strong>
                    <ul>
                        <li>Organic: Pitch, tar, starch (2-10%)</li>
                        <li>Inorganic: Cement, lime (5-15%)</li>
                    </ul>
                </li>
                <li><strong>Pressure:</strong> 50-200 MPa</li>
                <li><strong>Applications:</strong> DRI, ferroalloys, coal</li>
            </ul>
        </div>
        
        <div class="key-point">
            <h3>Agglomeration Benefits</h3>
            <ul>
                <li>Improved permeability in blast furnaces</li>
                <li>Reduced dust losses</li>
                <li>Better gas-solid contact</li>
                <li>Increased production rates</li>
                <li>Lower energy consumption compared to direct use of fines</li>
            </ul>
        </div>
        
        <div class="mcq">
            <div class="question">What is the primary purpose of agglomeration in mineral processing?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">To chemically purify the ore</div>
                <div class="option" onclick="checkAnswer(this, true)">To improve handling and furnace performance</div>
                <div class="option" onclick="checkAnswer(this, false)">To increase the ore's mineral content</div>
                <div class="option" onclick="checkAnswer(this, false)">To reduce energy consumption in grinding</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: To improve handling and furnace performance</strong></p>
                    <p>Agglomeration converts fines into larger, stronger masses that resist breakdown during handling and allow better gas flow in smelting furnaces, improving reduction efficiency.</p>
                </div>
            </div>
        </div>
        
        <div class="mcq">
            <div class="question">Which binder is typically used in iron ore pelletizing?</div>
            <div class="options">
                <div class="option" onclick="checkAnswer(this, false)">Portland cement</div>
                <div class="option" onclick="checkAnswer(this, true)">Bentonite clay</div>
                <div class="option" onclick="checkAnswer(this, false)">Coal tar</div>
                <div class="option" onclick="checkAnswer(this, false)">Lime</div>
            </div>
            <button class="show-answer-btn" onclick="toggleAnswer(this)"><i class="fas fa-lightbulb"></i> Show Answer</button>
            <div class="answer">
                <div class="answer-content">
                    <p><strong>Correct Answer: Bentonite clay</strong></p>
                    <p>Bentonite clay (0.5-1.5%) is the standard binder in iron ore pelletizing due to its excellent binding properties and minimal effect on iron content. Other binders are used in different applications.</p>
                </div>
            </div>
        </div>
    </div>

    <div class="section" id="formulas">
        <h2>5. Key Formulas</h2>
        
        <div class="method-card">
            <h3>Comminution</h3>
            <div class="formula-box">
                Bond Work Index: W<sub>i</sub> = 1.1 × 44.5 × P<sub>1</sub><sup>0.23</sup> × G<sub>bp</sub><sup>0.82</sup> × (10/√P<sub>80</sub> - 10/√F<sub>80</sub>)
            </div>
            <p>Where P<sub>1</sub> is test sieve size (µm), G<sub>bp</sub> is grams per revolution</p>
        </div>
        
        <div class="method-card">
            <h3>Classification</h3>
            <div class="formula-box">
                Screen Efficiency: E = [(O<sub>u</sub> × (F<sub>f</sub> - O<sub>o</sub>)) / (F<sub>f</sub> × (O<sub>u</sub> - O<sub>o</sub>))] × 100
            </div>
            <p>Where O<sub>u</sub> is undersize in overflow, F<sub>f</sub> is undersize in feed, O<sub>o</sub> is undersize in underflow</p>
        </div>
        
        <div class="method-card">
            <h3>Flotation</h3>
            <div class="formula-box">
                Selectivity Index: SI = (R<sub>a</sub>/R<sub>b</sub>) × (G<sub>b</sub>/G<sub>a</sub>)
            </div>
            <p>Where R is recovery, G is grade, a and b are different minerals</p>
        </div>
        
        <div class="method-card">
            <h3>Gravity Separation</h3>
            <div class="formula-box">
                Concentration Criterion: CC = (ρ<sub>h</sub> - ρ<sub>f</sub>)/(ρ<sub>l</sub> - ρ<sub>f</sub>)
            </div>
            <p>Where ρ<sub>h</sub> and ρ<sub>l</sub> are heavy/light mineral densities, ρ<sub>f</sub> is fluid density</p>
        </div>
    </div>

    <div class="section" id="interactive">
        <h2>6. Interactive Process Diagram</h2>
        <div class="interactive-diagram">
            <div class="diagram-element" onclick="showDiagramInfo(this, 'crushing')">
                <i class="fas fa-hammer"></i> Crushing
            </div>
            <div class="diagram-element" onclick="showDiagramInfo(this, 'grinding')">
                <i class="fas fa-cogs"></i> Grinding
            </div>
            <div class="diagram-element" onclick="showDiagramInfo(this, 'classification')">
                <i class="fas fa-filter"></i> Classification
            </div>
            <div class="diagram-element" onclick="showDiagramInfo(this, 'flotation')">
                <i class="fas fa-water"></i> Flotation
            </div>
            <div class="diagram-element" onclick="showDiagramInfo(this, 'agglomeration')">
                <i class="fas fa-cubes"></i> Agglomeration
            </div>
            
            <div class="diagram-info" id="crushing-info">
                <h4>Crushing Process</h4>
                <p>Reduces ore from 150-250mm to 10-30mm using:</p>
                <ul>
                    <li>Primary: Jaw or gyratory crushers</li>
                    <li>Secondary: Cone or impact crushers</li>
                    <li>Energy: 0.5-1.5 kWh/ton</li>
                </ul>
            </div>
            
            <div class="diagram-info" id="grinding-info">
                <h4>Grinding Process</h4>
                <p>Further reduces size to 75-250µm using:</p>
                <ul>
                    <li>Ball mills (10-20 kWh/ton)</li>
                    <li>Rod mills (8-15 kWh/ton)</li>
                    <li>SAG mills (15-25 kWh/ton)</li>
                </ul>
            </div>
            
            <div class="diagram-info" id="classification-info">
                <h4>Classification</h4>
                <p>Separates particles by size:</p>
                <ul>
                    <li>Screens (>0.5mm)</li>
                    <li>Hydrocyclones (10-300µm)</li>
                    <li>Spiral classifiers (100-1000µm)</li>
                </ul>
            </div>
            
            <div class="diagram-info" id="flotation-info">
                <h4>Flotation Process</h4>
                <p>Separates minerals based on surface chemistry:</p>
                <ul>
                    <li>Particle size: 10-300µm</li>
                    <li>pH range: 6-11</li>
                    <li>Recovery: 80-95%</li>
                </ul>
            </div>
            
            <div class="diagram-info" id="agglomeration-info">
                <h4>Agglomeration</h4>
                <p>Converts fines into usable forms:</p>
                <ul>
                    <li>Sintering (5-50mm lumps)</li>
                    <li>Pelletizing (9-16mm balls)</li>
                    <li>Briquetting (defined shapes)</li>
                </ul>
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
                button.style.background = 'linear-gradient(to right, #1B5E20, #2E7D32)';
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
