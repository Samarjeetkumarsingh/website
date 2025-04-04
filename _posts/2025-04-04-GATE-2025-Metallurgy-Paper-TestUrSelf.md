<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GATE 2025 MT Quiz | TestUrSelf</title>
    <style>
        :root {
            --primary-blue: #153475;
            --primary-green: #3c9d36;
            --accent-gold: #b7af0f;
            --light-bg: #f8f9fa;
            --card-bg: #ffffff;
            --text-dark: #212529;
            --text-light: #6c757d;
            --mark-1: #3a86ff;
            --mark-2: #ff7b54;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--light-bg);
            color: var(--text-dark);
            min-height: 100vh;
            position: relative;
            line-height: 1.6;
        }

        /* Responsive Watermark */
        body::before {
            content: 'TestUrSelf';
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-15deg);
            font-size: 20vw;
            font-weight: 900;
            color: rgba(21, 52, 117, 0.08);
            z-index: 0;
            pointer-events: none;
            opacity: 0.5;
            text-shadow: 0 0 10px rgba(0,0,0,0.1);
        }

        .container {
            max-width: 100%;
            width: 100%;
            margin: 0 auto;
            padding: 1rem;
            position: relative;
            z-index: 1;
        }

        header {
            text-align: center;
            margin-bottom: 1.5rem;
            padding: 1.5rem;
            border-radius: 10px;
            background: linear-gradient(135deg, var(--primary-blue), var(--primary-green));
            color: white;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
        }

        /* Header watermark */
        header::after {
            content: 'TestUrSelf';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-15deg);
            font-size: 8rem;
            font-weight: 900;
            color: rgba(255,255,255,0.1);
            z-index: -1;
            pointer-events: none;
        }

        .logo {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            text-shadow: 0 2px 4px rgba(0,0,0,0.2);
        }

        h1 {
            font-size: 1.8rem;
            margin: 0.5rem 0;
        }

        .subtitle {
            font-size: 1rem;
            opacity: 0.9;
        }

        .stats-bar {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            background: white;
            padding: 0.8rem;
            border-radius: 10px;
            margin-bottom: 1rem;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
            gap: 0.5rem;
        }

        .stat {
            display: flex;
            align-items: center;
            font-weight: 600;
            padding: 0.3rem 0;
            flex: 1;
            min-width: 120px;
            justify-content: center;
        }

        .correct-stat { color: var(--primary-green); }
        .incorrect-stat { color: #dc3545; }
        .score-stat { color: var(--primary-blue); }

        .quiz-section {
            background-color: var(--card-bg);
            border-radius: 12px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 4px 12px rgba(0,0,0,0.08);
            position: relative;
            overflow: hidden;
            transition: transform 0.3s ease;
        }

        .quiz-section:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 16px rgba(0,0,0,0.12);
        }

        /* Section watermark */
        .quiz-section::after {
            content: 'TestUrSelf';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-15deg);
            font-size: 6rem;
            font-weight: 900;
            color: rgba(21, 52, 117, 0.05);
            z-index: 0;
            pointer-events: none;
        }

        h2 {
            color: var(--primary-blue);
            margin-top: 0;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid rgba(21, 52, 117, 0.2);
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: relative;
            z-index: 1;
            font-size: 1.5rem;
        }

        .question {
            background-color: white;
            padding: 1.2rem;
            border-radius: 8px;
            margin-bottom: 1.2rem;
            box-shadow: 0 2px 6px rgba(0,0,0,0.05);
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        /* Question watermark */
        .question::before {
            content: 'TestUrSelf';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-15deg);
            font-size: 4rem;
            font-weight: 900;
            color: rgba(21, 52, 117, 0.08);
            z-index: -1;
            pointer-events: none;
        }

        .question-content {
            position: relative;
            z-index: 2;
        }

        .question-header {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1rem;
            gap: 0.5rem;
        }

        .question-number {
            font-weight: 700;
            color: var(--primary-blue);
            font-size: 1.1rem;
        }

        .question-marks {
            background-color: var(--primary-green);
            color: white;
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 600;
        }

        .mark-1 { background-color: var(--mark-1); }
        .mark-2 { background-color: var(--mark-2); }

        .question-type {
            display: inline-block;
            background-color: var(--accent-gold);
            color: var(--text-dark);
            padding: 0.2rem 0.6rem;
            border-radius: 4px;
            font-size: 0.8rem;
            font-weight: 600;
            margin-left: 0.5rem;
        }

        .options {
            margin-top: 1rem;
            position: relative;
            z-index: 2;
        }

        .option {
            display: block;
            margin: 0.8rem 0;
            padding: 0.8rem;
            background-color: white;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s;
            border: 1px solid #dee2e6;
            position: relative;
            padding-left: 3rem;
        }

        .option:hover {
            border-color: var(--primary-blue);
            transform: translateX(3px);
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }

        .checkmark {
            position: absolute;
            top: 50%;
            left: 1rem;
            transform: translateY(-50%);
            height: 20px;
            width: 20px;
            border: 2px solid #adb5bd;
            border-radius: 50%;
            transition: all 0.2s;
        }

        .option:hover .checkmark {
            border-color: var(--primary-blue);
        }

        input:checked ~ .checkmark {
            background-color: var(--primary-blue);
            border-color: var(--primary-blue);
        }

        input:checked ~ .checkmark::after {
            content: '';
            position: absolute;
            left: 5px;
            top: 2px;
            width: 5px;
            height: 10px;
            border: solid white;
            border-width: 0 2px 2px 0;
            transform: rotate(45deg);
        }

        /* For MSQ questions */
        .msq-option input[type="checkbox"] ~ .checkmark {
            border-radius: 4px;
        }

        .msq-option input[type="checkbox"]:checked ~ .checkmark::after {
            left: 4px;
            top: 0;
            width: 6px;
            height: 12px;
        }

        /* For NAT questions */
        .nat-input {
            width: 100%;
            max-width: 200px;
            padding: 0.8rem;
            border: 1px solid #dee2e6;
            border-radius: 8px;
            font-size: 1rem;
            margin-top: 1rem;
            position: relative;
            z-index: 2;
        }

        .nat-input:focus {
            outline: none;
            border-color: var(--primary-blue);
            box-shadow: 0 0 0 3px rgba(21, 52, 117, 0.2);
        }

        /* TestUrSelf Action Button */
        .testurself-action {
            background: linear-gradient(135deg, var(--primary-blue), var(--primary-green));
            color: white;
            border: none;
            padding: 0.8rem 1.5rem;
            font-size: 1rem;
            font-weight: 600;
            border-radius: 8px;
            cursor: pointer;
            margin-top: 1rem;
            width: 100%;
            text-align: center;
            transition: all 0.3s;
            box-shadow: 0 4px 8px rgba(21, 52, 117, 0.2);
            text-transform: uppercase;
            letter-spacing: 1px;
            position: relative;
            z-index: 2;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .testurself-action:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(21, 52, 117, 0.3);
            background: linear-gradient(135deg, var(--primary-green), var(--primary-blue));
        }

        .testurself-action:active {
            transform: translateY(0);
        }

        /* Button watermark effect */
        .testurself-action::before {
            content: 'TestUrSelf';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 1.2rem;
            font-weight: 900;
            color: rgba(255,255,255,0.2);
            pointer-events: none;
        }

        .result {
            margin-top: 1rem;
            padding: 1rem;
            border-radius: 8px;
            display: none;
            animation: fadeIn 0.5s ease;
            position: relative;
            z-index: 2;
        }

        .correct {
            background-color: rgba(60, 157, 54, 0.1);
            border-left: 4px solid var(--primary-green);
        }

        .incorrect {
            background-color: rgba(220, 53, 69, 0.1);
            border-left: 4px solid #dc3545;
        }

        .marks-awarded {
            font-weight: 600;
            color: var(--primary-green);
            margin-top: 0.5rem;
        }

        .navigation {
            display: flex;
            justify-content: space-between;
            margin-top: 1.5rem;
            position: relative;
            z-index: 2;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .nav-btn {
            background-color: white;
            color: var(--primary-blue);
            border: 2px solid var(--primary-blue);
            padding: 0.7rem 1.2rem;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s;
            font-weight: 600;
            flex: 1;
            min-width: 150px;
        }

        .nav-btn:hover {
            background-color: rgba(21, 52, 117, 0.1);
        }

        .progress-container {
            width: 100%;
            background-color: #e9ecef;
            border-radius: 10px;
            margin: 1rem 0;
            height: 8px;
            overflow: hidden;
            position: relative;
            z-index: 2;
        }

        .progress-bar {
            height: 100%;
            border-radius: 10px;
            background: linear-gradient(90deg, var(--primary-blue), var(--primary-green));
            width: 0%;
            transition: width 0.5s;
            position: relative;
        }

        .progress-bar::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(90deg, 
                          transparent, 
                          rgba(255, 255, 255, 0.3), 
                          transparent);
            animation: shimmer 2s infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        footer {
            text-align: center;
            margin-top: 2rem;
            padding-top: 1.5rem;
            border-top: 1px solid #dee2e6;
            color: var(--text-light);
            position: relative;
            z-index: 2;
        }

        .powered-by {
            font-weight: 600;
            color: var(--primary-blue);
        }

        /* Animation */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Floating animation for correct answers */
        @keyframes floatUp {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-20px); opacity: 0; }
        }

        .floating-marks {
            position: absolute;
            right: 20px;
            font-weight: bold;
            color: var(--primary-green);
            animation: floatUp 1s forwards;
        }

        /* Matrix styling */
        .matrix {
            display: inline-block;
            margin-left: 0.5rem;
            border-collapse: collapse;
        }

        .matrix td {
            padding: 0.3rem 0.5rem;
            border: 1px solid #dee2e6;
            text-align: center;
        }

        /* Responsive adjustments */
        @media (min-width: 768px) {
            .container {
                max-width: 900px;
                padding: 2rem;
            }
            
            header {
                padding: 2rem;
                margin-bottom: 2rem;
            }
            
            .logo {
                font-size: 2.5rem;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            .subtitle {
                font-size: 1.1rem;
            }
            
            .stats-bar {
                padding: 1rem;
            }
            
            .quiz-section {
                padding: 2rem;
                margin-bottom: 2rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            .question {
                padding: 1.5rem;
            }
            
            .testurself-action {
                padding: 1rem 2rem;
            }
            
            .nav-btn {
                padding: 0.8rem 1.5rem;
            }
            
            .progress-container {
                height: 10px;
            }
        }

        @media (max-width: 480px) {
            body::before {
                font-size: 15vw;
            }
            
            header::after {
                font-size: 4rem;
            }
            
            .quiz-section::after {
                font-size: 3rem;
            }
            
            .question::before {
                font-size: 2.5rem;
            }
            
            .option {
                padding: 0.7rem;
                padding-left: 2.5rem;
            }
            
            .checkmark {
                height: 18px;
                width: 18px;
                left: 0.8rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="logo">TestUrSelf</div>
            <h1>GATE 2025 Metallurgical Engineering</h1>
            <p class="subtitle">Practice with authentic GATE questions and boost your preparation</p>
        </header>

        <div class="stats-bar">
            <div class="stat correct-stat">
                <span id="correct-count">0</span> Correct
            </div>
            <div class="stat incorrect-stat">
                <span id="incorrect-count">0</span> Incorrect
            </div>
            <div class="stat score-stat">
                Score: <span id="current-score">0</span>/<span id="total-marks">0</span>
            </div>
        </div>

        <div class="progress-container">
            <div class="progress-bar" id="progressBar"></div>
        </div>

        <!-- General Aptitude Section -->
        <div class="quiz-section" id="generalAptitude">
            <h2>General Aptitude (Q1-Q5)</h2>

            <!-- 1 Mark MCQ -->
            <div class="question" id="q1">
                <div class="question-content">
                    <div class="question-header">
                        <div class="question-number">Q1.</div>
                        <div class="question-marks mark-1">1 Mark</div>
                    </div>
                    <div class="question-text">
                        Despite his initial hesitation, Rehman's ______ to contribute to the success of the project never wavered.
                    </div>
                    <div class="options">
                        <label class="option">
                            <input type="radio" name="q1" value="A">
                            <span class="checkmark"></span>
                            A) ambivalence
                        </label>
                        <label class="option">
                            <input type="radio" name="q1" value="B">
                            <span class="checkmark"></span>
                            B) satisfaction
                        </label>
                        <label class="option">
                            <input type="radio" name="q1" value="C">
                            <span class="checkmark"></span>
                            C) resolve
                        </label>
                        <label class="option">
                            <input type="radio" name="q1" value="D">
                            <span class="checkmark"></span>
                            D) revolve
                        </label>
                    </div>
                    <button class="testurself-action" onclick="checkAnswer('q1', 'C', 'The correct answer is C) resolve. "Resolve" means firm determination, which fits the context of the sentence.', 1)">
                        TestUrSelf
                    </button>
                    <div class="result" id="q1-result"></div>
                </div>
            </div>

            <!-- 2 Mark MCQ -->
            <div class="question" id="q2">
                <div class="question-content">
                    <div class="question-header">
                        <div class="question-number">Q2.</div>
                        <div class="question-marks mark-2">2 Marks</div>
                    </div>
                    <div class="question-text">
                        Bird : Nest :: Bee : ______
                    </div>
                    <div class="options">
                        <label class="option">
                            <input type="radio" name="q2" value="A">
                            <span class="checkmark"></span>
                            A) Kennel
                        </label>
                        <label class="option">
                            <input type="radio" name="q2" value="B">
                            <span class="checkmark"></span>
                            B) Hammock
                        </label>
                        <label class="option">
                            <input type="radio" name="q2" value="C">
                            <span class="checkmark"></span>
                            C) Hive
                        </label>
                        <label class="option">
                            <input type="radio" name="q2" value="D">
                            <span class="checkmark"></span>
                            D) Lair
                        </label>
                    </div>
                    <button class="testurself-action" onclick="checkAnswer('q2', 'C', 'The correct answer is C) Hive. The analogy shows the relationship between an animal and its dwelling - birds live in nests, bees live in hives.', 2)">
                        TestUrSelf
                    </button>
                    <div class="result" id="q2-result"></div>
                </div>
            </div>
        </div>

        <!-- Metallurgical Engineering Section -->
        <div class="quiz-section" id="metallurgicalEngineering">
            <h2>Metallurgical Engineering (Q11-Q35)</h2>

            <!-- MSQ Question -->
            <div class="question" id="q11">
                <div class="question-content">
                    <div class="question-header">
                        <div class="question-number">Q11.</div>
                        <div class="question-marks mark-2">2 Marks <span class="question-type">MSQ</span></div>
                    </div>
                    <div class="question-text">
                        Which of the following matrices have eigenvalues 1 and 6? (Select all that apply)
                    </div>
                    <div class="options">
                        <label class="option msq-option">
                            <input type="checkbox" name="q11" value="A">
                            <span class="checkmark"></span>
                            A) 
                            <table class="matrix">
                                <tr><td>5</td><td>-2</td></tr>
                                <tr><td>-2</td><td>2</td></tr>
                            </table>
                        </label>
                        <label class="option msq-option">
                            <input type="checkbox" name="q11" value="B">
                            <span class="checkmark"></span>
                            B) 
                            <table class="matrix">
                                <tr><td>3</td><td>-1</td></tr>
                                <tr><td>-2</td><td>2</td></tr>
                            </table>
                        </label>
                        <label class="option msq-option">
                            <input type="checkbox" name="q11" value="C">
                            <span class="checkmark"></span>
                            C) 
                            <table class="matrix">
                                <tr><td>3</td><td>-1</td></tr>
                                <tr><td>-1</td><td>2</td></tr>
                            </table>
                        </label>
                        <label class="option msq-option">
                            <input type="checkbox" name="q11" value="D">
                            <span class="checkmark"></span>
                            D) 
                            <table class="matrix">
                                <tr><td>2</td><td>-1</td></tr>
                                <tr><td>-1</td><td>3</td></tr>
                            </table>
                        </label>
                    </div>
                    <button class="testurself-action" onclick="checkMSQAnswer('q11', ['A'], 'The correct answer is A. The matrix [5 -2; -2 2] has eigenvalues 1 and 6.', 2)">
                        TestUrSelf
                    </button>
                    <div class="result" id="q11-result"></div>
                </div>
            </div>

            <!-- NAT Question -->
            <div class="question" id="q12">
                <div class="question-content">
                    <div class="question-header">
                        <div class="question-number">Q12.</div>
                        <div class="question-marks mark-1">1 Mark <span class="question-type">NAT</span></div>
                    </div>
                    <div class="question-text">
                        The hydrostatic stress for the given stress tensor is ______ MPa (enter integer value):
                        <table class="matrix">
                            <tr><td>150</td><td>0</td><td>0</td></tr>
                            <tr><td>0</td><td>-100</td><td>100</td></tr>
                            <tr><td>0</td><td>100</td><td>250</td></tr>
                        </table>
                    </div>
                    <input type="number" class="nat-input" id="q12-answer" placeholder="Enter your answer">
                    <button class="testurself-action" onclick="checkNATAnswer('q12', 100, 'The correct answer is 100 MPa. Hydrostatic stress is the average of the diagonal elements.', 1)">
                        TestUrSelf
                    </button>
                    <div class="result" id="q12-result"></div>
                </div>
            </div>
        </div>

        <div class="navigation">
            <button class="nav-btn" id="prevBtn" onclick="prevSection()" disabled>
                ← Previous Section
            </button>
            <button class="nav-btn" id="nextBtn" onclick="nextSection()">
                Next Section →
            </button>
        </div>

        <footer>
            <p>© 2025 TestUrSelf - Premium GATE Preparation Platform</p>
            <p class="powered-by">Powered by TestUrSelf</p>
        </footer>
    </div>

    <script>
        // Quiz state
        const quizState = {
            totalQuestions: 4,
            answered: 0,
            correct: 0,
            incorrect: 0,
            score: 0,
            totalMarks: 6, // Sum of all question marks
            currentSection: 0,
            sections: ['generalAptitude', 'metallurgicalEngineering']
        };

        // Initialize the quiz
        function initQuiz() {
            updateStats();
            showSection(quizState.currentSection);
            document.getElementById('total-marks').textContent = quizState.totalMarks;
        }

        // Update stats display
        function updateStats() {
            document.getElementById('correct-count').textContent = quizState.correct;
            document.getElementById('incorrect-count').textContent = quizState.incorrect;
            document.getElementById('current-score').textContent = quizState.score;
            
            const progress = (quizState.answered / quizState.totalQuestions) * 100;
            document.getElementById('progressBar').style.width = `${progress}%`;
        }

        // Check MCQ answer
        function checkAnswer(questionId, correctAnswer, explanation, marks) {
            const selectedOption = document.querySelector(`input[name="${questionId}"]:checked`);
            const resultDiv = document.getElementById(`${questionId}-result`);
            
            if (!selectedOption) {
                alert('Please select an option!');
                return;
            }
            
            quizState.answered++;
            
            if (selectedOption.value === correctAnswer) {
                resultDiv.innerHTML = `
                    <strong>✓ Correct!</strong> ${explanation}
                    <div class="marks-awarded">+${marks} mark${marks > 1 ? 's' : ''} awarded</div>
                `;
                resultDiv.className = 'result correct';
                quizState.correct++;
                quizState.score += marks;
                
                // Create floating marks animation
                const floatingMarks = document.createElement('div');
                floatingMarks.className = 'floating-marks';
                floatingMarks.textContent = `+${marks}`;
                resultDiv.appendChild(floatingMarks);
                
                setTimeout(() => {
                    floatingMarks.remove();
                }, 1000);
            } else {
                resultDiv.innerHTML = `
                    <strong>✗ Incorrect.</strong> ${explanation}
                    <div class="marks-awarded">0 marks awarded</div>
                `;
                resultDiv.className = 'result incorrect';
                quizState.incorrect++;
            }
            
            resultDiv.style.display = 'block';
            updateStats();
            
            // Disable all options after submission
            document.querySelectorAll(`input[name="${questionId}"]`).forEach(input => {
                input.disabled = true;
            });
        }

        // Check MSQ answer
        function checkMSQAnswer(questionId, correctAnswers, explanation, marks) {
            const selectedOptions = Array.from(document.querySelectorAll(`input[name="${questionId}"]:checked`)).map(el => el.value);
            const resultDiv = document.getElementById(`${questionId}-result`);
            
            if (selectedOptions.length === 0) {
                alert('Please select at least one option!');
                return;
            }
            
            quizState.answered++;
            
            // Check if all correct answers are selected and no incorrect ones
            const isCorrect = correctAnswers.length === selectedOptions.length && 
                             correctAnswers.every(val => selectedOptions.includes(val));
            
            if (isCorrect) {
                resultDiv.innerHTML = `
                    <strong>✓ Correct!</strong> ${explanation}
                    <div class="marks-awarded">+${marks} mark${marks > 1 ? 's' : ''} awarded</div>
                `;
                resultDiv.className = 'result correct';
                quizState.correct++;
                quizState.score += marks;
                
                // Floating marks animation
                const floatingMarks = document.createElement('div');
                floatingMarks.className = 'floating-marks';
                floatingMarks.textContent = `+${marks}`;
                resultDiv.appendChild(floatingMarks);
                
                setTimeout(() => {
                    floatingMarks.remove();
                }, 1000);
            } else {
                resultDiv.innerHTML = `
                    <strong>✗ Incorrect.</strong> ${explanation}
                    <div class="marks-awarded">0 marks awarded</div>
                `;
                resultDiv.className = 'result incorrect';
                quizState.incorrect++;
            }
            
            resultDiv.style.display = 'block';
            updateStats();
            
            // Disable all options after submission
            document.querySelectorAll(`input[name="${questionId}"]`).forEach(input => {
                input.disabled = true;
            });
        }

        // Check NAT answer
        function checkNATAnswer(questionId, correctAnswer, explanation, marks) {
            const userAnswer = document.getElementById(`${questionId}-answer`).value.trim();
            const resultDiv = document.getElementById(`${questionId}-result`);
            
            if (!userAnswer) {
                alert('Please enter your answer!');
                return;
            }
            
            quizState.answered++;
            
            if (parseInt(userAnswer) === correctAnswer) {
                resultDiv.innerHTML = `
                    <strong>✓ Correct!</strong> ${explanation}
                    <div class="marks-awarded">+${marks} mark${marks > 1 ? 's' : ''} awarded</div>
                `;
                resultDiv.className = 'result correct';
                quizState.correct++;
                quizState.score += marks;
                
                // Floating marks animation
                const floatingMarks = document.createElement('div');
                floatingMarks.className = 'floating-marks';
                floatingMarks.textContent = `+${marks}`;
                resultDiv.appendChild(floatingMarks);
                
                setTimeout(() => {
                    floatingMarks.remove();
                }, 1000);
            } else {
                resultDiv.innerHTML = `
                    <strong>✗ Incorrect.</strong> ${explanation}
                    <div class="marks-awarded">0 marks awarded</div>
                `;
                resultDiv.className = 'result incorrect';
                quizState.incorrect++;
            }
            
            resultDiv.style.display = 'block';
            updateStats();
            
            // Disable input after submission
            document.getElementById(`${questionId}-answer`).disabled = true;
        }

        // Navigation between sections
        function showSection(index) {
            document.querySelectorAll('.quiz-section').forEach((section, i) => {
                section.style.display = i === index ? 'block' : 'none';
            });
            
            document.getElementById('prevBtn').disabled = index === 0;
            document.getElementById('nextBtn').disabled = index === quizState.sections.length - 1;
            
            quizState.currentSection = index;
        }

        function prevSection() {
            if (quizState.currentSection > 0) {
                showSection(quizState.currentSection - 1);
            }
        }

        function nextSection() {
            if (quizState.currentSection < quizState.sections.length - 1) {
                showSection(quizState.currentSection + 1);
            }
        }

        // Initialize the quiz when page loads
        window.onload = initQuiz;
    </script>
</body>
</html>
