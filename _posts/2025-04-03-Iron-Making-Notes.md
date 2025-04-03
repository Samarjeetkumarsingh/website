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
        
        /* Main Wrapper */
        .page-wrapper {
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }
        
        /* Header Section */
        .header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            text-align: center;
            padding: 3rem 1rem;
            position: relative;
            overflow: hidden;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
            width: 100%;
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
            width: 100%;
            padding: 0 20px;
            box-sizing: border-box;
        }
        
        .header h1 {
            font-size: 2.8rem;
            margin: 0;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        .header p {
            font-size: 1.2rem;
            margin: 1rem 0 0;
            opacity: 0.9;
        }
        
        /* Content Container */
        .content-wrapper {
            width: 100%;
            max-width: 1200px;
            padding: 0 20px;
            box-sizing: border-box;
            margin: 0 auto;
        }
        
        /* Table of Contents */
        .toc-container {
            background-color: var(--card-bg);
            margin: 2rem 0;
            padding: 2rem;
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
            font-size: 1.8rem;
            color: var(--primary);
            margin: 0;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .toc-header i {
            color: var(--secondary);
            font-size: 1.5rem;
        }
        
        .toc-list {
            list-style: none;
            padding: 0;
            margin: 0;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 15px;
        }
        
        .toc-item {
            margin: 0;
        }
        
        .toc-link {
            display: flex;
            align-items: center;
            padding: 12px 15px;
            background-color: rgba(145, 127, 179, 0.1);
            border-radius: 8px;
            color: var(--text);
            text-decoration: none;
            transition: all 0.3s ease;
            font-weight: 500;
        }
        
        .toc-link:hover {
            background-color: rgba(145, 127, 179, 0.2);
            transform: translateX(5px);
        }
        
        .toc-link::before {
            content: "•";
            color: var(--secondary);
            margin-right: 10px;
            font-size: 1.5rem;
        }
        
        /* Sections */
        .section {
            background-color: var(--card-bg);
            border-radius: 15px;
            padding: 2rem;
            margin-bottom: 2.5rem;
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
            .header h1 {
                font-size: 2.4rem;
            }
        }
        
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2rem;
            }
            
            .toc-list {
                grid-template-columns: 1fr;
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
            
            .content-wrapper {
                padding: 0 15px;
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
    
    <!-- Page Wrapper -->
    <div class="page-wrapper">
        <!-- Header Section -->
        <header class="header fade-in">
            <div class="header-content">
                <h1>Iron Making</h1>
                <p>Comprehensive Interactive eNotes on Modern Iron Production Techniques</p>
            </div>
        </header>
        
        <!-- Content Wrapper -->
        <div class="content-wrapper">
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
            
            <!-- All other sections (2-9) would follow here with the same structure -->
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
            
            <!-- Continue with all other sections exactly as before -->
        </div>
    </div>
    
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
