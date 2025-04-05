<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Master GATE Metallurgy | TestUrSelf - India's #1 GATE Coaching</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.11.4/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.11.4/ScrollTrigger.min.js"></script>
    <style>
        :root {
            --primary-blue: #176b87;
            --secondary-teal: #229954;
            --accent-gold: #FFD700;
            --dark-blue: #0d47a1;
            --light-blue: #e8f9fd;
            --highlight-yellow: #f8e71c;
            --danger-red: #ff1744;
            --purple: #7c4dff;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.8;
            color: #2d3436;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0;
            background-color: #f0f7ff;
            position: relative;
            overflow-x: hidden;
        }

        /* Particle Background */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.3;
        }

        .particle {
            position: absolute;
            border-radius: 50%;
            background: radial-gradient(circle, var(--primary-blue), transparent);
            opacity: 0.6;
        }

        /* Confetti Animation */
        .confetti {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: -1;
            pointer-events: none;
        }

        .confetti-piece {
            position: absolute;
            width: 10px;
            height: 10px;
            background-color: var(--accent-gold);
            opacity: 0;
        }

        @keyframes confetti-fall {
            0% { transform: translateY(-100px) rotate(0deg); opacity: 1; }
            100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
        }

        /* Celebration Badge */
        .celebration-badge {
            position: absolute;
            top: -15px;
            right: -15px;
            background: var(--accent-gold);
            color: var(--dark-blue);
            width: 70px;
            height: 70px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 1.1rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            z-index: 10;
            transform: rotate(15deg);
            animation: pulse-gold 2s infinite;
        }

        @keyframes pulse-gold {
            0% { transform: scale(1) rotate(15deg); }
            50% { transform: scale(1.1) rotate(15deg); }
            100% { transform: scale(1) rotate(15deg); }
        }

        /* Navigation */
        nav {
            background: linear-gradient(135deg, var(--dark-blue), var(--primary-blue));
            color: white;
            padding: 1.2rem 2rem;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 18px rgba(0,0,0,0.1);
            backdrop-filter: blur(10px);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        .logo {
            font-size: 2rem;
            font-weight: 700;
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
            transition: all 0.3s ease;
        }

        .logo:hover {
            transform: scale(1.05);
        }

        .logo i {
            margin-right: 12px;
            color: var(--highlight-yellow);
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            position: relative;
            padding: 0.5rem 0;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 3px;
            bottom: 0;
            left: 0;
            background-color: var(--highlight-yellow);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-links a:hover {
            color: var(--highlight-yellow);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--dark-blue), var(--primary-blue));
            color: white;
            padding: 6rem 2rem 8rem;
            text-align: center;
            position: relative;
            overflow: hidden;
            clip-path: polygon(0 0, 100% 0, 100% 90%, 0 100%);
        }

        .hero::before {
            content: "";
            position: absolute;
            top: -50%;
            left: -50%;
            right: -50%;
            bottom: -50%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: pulse 8s infinite alternate;
        }

        @keyframes pulse {
            0% { transform: scale(0.8); opacity: 0.3; }
            100% { transform: scale(1.2); opacity: 0.1; }
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            text-shadow: 0 4px 12px rgba(0,0,0,0.2);
            position: relative;
            display: inline-block;
            background: linear-gradient(to right, white, var(--accent-gold));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .hero h1::after {
            content: '';
            position: absolute;
            width: 60%;
            height: 4px;
            bottom: -10px;
            left: 20%;
            background: var(--accent-gold);
            border-radius: 2px;
        }

        .hero p {
            font-size: 1.3rem;
            max-width: 700px;
            margin: 0 auto 3rem;
            opacity: 0.9;
        }

        .achievement-badge {
            display: inline-block;
            background: rgba(255,255,255,0.2);
            backdrop-filter: blur(10px);
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            margin: 1rem 0;
            border: 2px solid var(--accent-gold);
            font-weight: bold;
            animation: float 3s ease-in-out infinite;
        }

        .cta-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            margin-top: 2rem;
        }

        .btn {
            padding: 1rem 2.2rem;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.4s ease;
            display: inline-flex;
            align-items: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .btn i {
            margin-right: 8px;
        }

        .btn-primary {
            background-color: var(--highlight-yellow);
            color: var(--dark-blue);
        }

        .btn-primary:hover {
            background-color: #e6d41a;
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 25px rgba(248, 231, 28, 0.3);
        }

        .btn-secondary {
            background-color: transparent;
            border: 2px solid white;
            color: white;
        }

        .btn-secondary:hover {
            background-color: rgba(255,255,255,0.15);
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }

        /* Floating Elements */
        .floating-shape {
            position: absolute;
            opacity: 0.1;
            z-index: 0;
        }

        .shape-1 {
            top: 20%;
            left: 5%;
            width: 100px;
            height: 100px;
            border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
            background: var(--secondary-teal);
            animation: float 8s ease-in-out infinite;
        }

        .shape-2 {
            top: 60%;
            right: 10%;
            width: 150px;
            height: 150px;
            border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%;
            background: var(--purple);
            animation: float 10s ease-in-out infinite reverse;
        }

        .shape-3 {
            bottom: 15%;
            left: 10%;
            width: 120px;
            height: 120px;
            border-radius: 40% 60% 70% 30% / 40% 50% 60% 70%;
            background: var(--accent-gold);
            animation: float 9s ease-in-out infinite 2s;
        }

        .floating-trophy {
            position: absolute;
            font-size: 3rem;
            color: var(--accent-gold);
            animation: float 6s ease-in-out infinite;
            opacity: 0.7;
            z-index: 0;
        }

        @keyframes float {
            0% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(5deg); }
            100% { transform: translateY(0) rotate(0deg); }
        }

        /* Section Styling */
        .section {
            background-color: white;
            border-radius: 16px;
            padding: 4rem 3rem;
            margin: 4rem 2rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            position: relative;
            z-index: 3;
            transition: transform 0.4s ease, box-shadow 0.4s ease;
            border: none;
            overflow: hidden;
        }

        .section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--primary-blue), var(--secondary-teal));
        }

        .section:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.1);
        }

        h2 {
            color: var(--dark-blue);
            border-bottom: none;
            padding-bottom: 0;
            margin-top: 0;
            font-size: 2.5rem;
            background: none;
            padding: 0;
            text-align: center;
            position: relative;
            margin-bottom: 3rem;
        }

        h2::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            background: linear-gradient(to right, var(--primary-blue), var(--accent-gold));
            border-radius: 2px;
        }

        h3 {
            color: var(--dark-blue);
            margin-top: 2.5rem;
            font-size: 1.8rem;
            border-left: none;
            padding-left: 0;
            position: relative;
            padding-bottom: 0.5rem;
        }

        h3::after {
            content: '';
            position: absolute;
            width: 50px;
            height: 3px;
            bottom: 0;
            left: 0;
            background: var(--accent-gold);
            border-radius: 2px;
        }

        /* Importance Points */
        .importance-points {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2.5rem;
            margin-top: 3rem;
        }

        .point-card {
            background: white;
            border-radius: 12px;
            padding: 2.5rem;
            box-shadow: 0 8px 25px rgba(0,0,0,0.05);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(0,0,0,0.03);
        }

        .point-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary-blue), var(--secondary-teal));
        }

        .point-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
        }

        .point-number {
            font-size: 3rem;
            font-weight: bold;
            color: rgba(0,0,0,0.05);
            position: absolute;
            top: 1rem;
            right: 1.5rem;
            z-index: 0;
            font-family: 'Poppins', sans-serif;
        }

        .point-content {
            position: relative;
            z-index: 1;
        }

        .point-card h4 {
            color: var(--dark-blue);
            margin-top: 0;
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
        }

        .point-card h4 i {
            margin-right: 12px;
            color: var(--secondary-teal);
            font-size: 1.8rem;
        }

        /* Chart Containers */
        .chart-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(450px, 1fr));
            gap: 2.5rem;
            margin-top: 3rem;
        }

        .chart-card {
            background: white;
            border-radius: 14px;
            padding: 2.5rem;
            box-shadow: 0 8px 25px rgba(0,0,0,0.05);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .chart-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--primary-blue), var(--secondary-teal));
        }

        .chart-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
        }

        .chart-wrapper {
            position: relative;
            height: 350px;
            width: 100%;
        }

        /* Animated Pie Chart */
        .pie-chart-container {
            position: relative;
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
        }

        .pie-chart-wrapper {
            flex: 1;
            position: relative;
        }

        .pie-chart-legend {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .legend-item {
            display: flex;
            align-items: center;
            font-size: 0.9rem;
            background: rgba(0,0,0,0.03);
            padding: 0.5rem 1rem;
            border-radius: 20px;
        }

        .legend-color {
            width: 15px;
            height: 15px;
            border-radius: 3px;
            margin-right: 8px;
        }

        /* Comparison Table */
        .comparison-table {
            width: 100%;
            border-collapse: separate;
            border-spacing: 0;
            margin-top: 2rem;
            box-shadow: 0 5px 25px rgba(0,0,0,0.05);
            border-radius: 12px;
            overflow: hidden;
        }

        .comparison-table th, .comparison-table td {
            padding: 1.2rem 1.5rem;
            text-align: left;
            border-bottom: 1px solid rgba(0,0,0,0.05);
        }

        .comparison-table th {
            background-color: var(--dark-blue);
            color: white;
            font-weight: 600;
            text-transform: uppercase;
            font-size: 0.9rem;
            letter-spacing: 0.5px;
        }

        .comparison-table tr:nth-child(even) {
            background-color: #f8fafc;
        }

        .comparison-table tr:hover {
            background-color: #f1f5f9;
        }

        .comparison-table tr:last-child td {
            border-bottom: none;
        }

        .check-mark {
            color: var(--secondary-teal);
            font-weight: bold;
            font-size: 1.1rem;
        }

        .cross-mark {
            color: var(--danger-red);
            font-weight: bold;
            font-size: 1.1rem;
        }

        /* TestUrSelf Advantage */
        .advantage-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2.5rem;
            margin-top: 3rem;
        }

        .advantage-card {
            background: white;
            border-radius: 12px;
            padding: 2.5rem;
            box-shadow: 0 8px 25px rgba(0,0,0,0.05);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(0,0,0,0.03);
        }

        .advantage-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--secondary-teal), var(--accent-gold));
        }

        .advantage-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
        }

        .advantage-icon {
            font-size: 3rem;
            color: var(--primary-blue);
            margin-bottom: 1.5rem;
            transition: all 0.4s ease;
        }

        .advantage-card:hover .advantage-icon {
            transform: scale(1.1) rotate(5deg);
            color: var(--secondary-teal);
        }

        .advantage-card h4 {
            color: var(--dark-blue);
            margin-top: 0;
            font-size: 1.4rem;
            margin-bottom: 1.2rem;
        }

        /* Timeline Section */
        .timeline-section {
            position: relative;
            padding: 5rem 2rem;
            background: linear-gradient(to bottom, #f8f9fa, white);
            margin: 0 2rem 6rem;
            width: calc(100% - 4rem);
            box-sizing: border-box;
            z-index: 2;
            border-radius: 16px;
        }

        .timeline-container {
            max-width: 1200px;
            margin: 0 auto;
            position: relative;
        }

        .timeline-header {
            text-align: center;
            margin-bottom: 4rem;
        }

        .timeline-header h2 {
            font-size: 2.8rem;
            color: var(--dark-blue);
            margin-bottom: 1rem;
            position: relative;
            display: inline-block;
        }

        .timeline-header h2::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            background: linear-gradient(to right, var(--primary-blue), var(--accent-gold));
            border-radius: 2px;
        }

        .timeline-header p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto;
            color: var(--dark-blue);
        }

        .timeline {
            position: relative;
            max-width: 1200px;
            margin: 0 auto;
        }

        .timeline-1::after {
            content: '';
            position: absolute;
            width: 6px;
            background: linear-gradient(to bottom, var(--primary-blue), var(--accent-gold));
            top: 50%;
                height: 100%;
            bottom: 0;
            left: 4px;
            margin-left: -3px;
            border-radius: 10px;
            z-index:0
        }
         .timeline-2::after {
            content: '';
            position: absolute;
            width: 6px;
            background: linear-gradient(to bottom, var(--primary-blue), var(--accent-gold));
            top: 40%;
                height: 0%;
            bottom: 0;
            left: 4px;
            margin-left: -3px;
            border-radius: 10px;
            z-index:0
        }

        .timeline-item {
            padding: 20px 40px;
            position: relative;
            width: 100%;
            box-sizing: border-box;
            padding-bottom: 3rem;
            z-index:99
        }

        .timeline-item::after {
            content: '';
            position: absolute;
            width: 25px;
            height: 25px;
            left: -12px;
            background-color: var(--accent-gold);
            border: 4px solid var(--primary-blue);
            top: 40%;
            border-radius: 50%;
            z-index: 999;
        }

        .left {
            left: -32 px;
        }

        .right {
            right: -32 px;
        }

        .right::after {
            left: -12px;
        }

        .timeline-content {
            padding: 2rem;
            background-color: white;
            position: relative;
            border-radius: 16px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            border-top: 5px solid var(--primary-blue);
        }

        .timeline-content:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.15);
        }

        .timeline-content h3 {
            margin-top: 0;
            color: var(--dark-blue);
            font-size: 1.5rem;
        }

        .timeline-content p {
            margin-bottom: 0;
        }

        .timeline-year {
            position: absolute;
            top: -15px;
            left: 20px;
            background: var(--primary-blue);
            color: white;
            padding: 0.5rem 1.5rem;
            border-radius: 50px;
            font-weight: bold;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .timeline-highlight {
            position: absolute;
            bottom: -15px;
            right: 20px;
            background: var(--accent-gold);
            color: var(--dark-blue);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            font-weight: bold;
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Testimonials Section */
        .testimonials-section {
            background: linear-gradient(135deg, var(--light-blue) 0%, #e8f5ee 100%);
            padding: 6rem 2rem;
            position: relative;
            overflow: hidden;
            margin: 0;
            width: 100%;
            box-sizing: border-box;
        }

        .testimonials-container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .testimonials-header {
            text-align: center;
            margin-bottom: 4rem;
        }

        .testimonials-header h2 {
            font-size: 2.8rem;
            color: var(--primary-blue);
            margin-bottom: 1rem;
            position: relative;
            display: inline-block;
        }

        .testimonials-header h2::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            background: linear-gradient(to right, var(--primary-blue), var(--accent-gold));
            border-radius: 2px;
        }

        .testimonials-header p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto;
            color: var(--dark-blue);
        }

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .testimonial-card {
            background: white;
            padding: 2.5rem;
            border-radius: 16px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            position: relative;
            transition: all 0.3s ease;
            border-top: 5px solid var(--accent-gold);
        }

        .testimonial-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.15);
        }

        .testimonial-card::before {
            content: "";
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 5rem;
            color: rgba(23, 107, 135, 0.1);
            font-family: serif;
            line-height: 1;
        }

        .testimonial-text {
            font-style: italic;
            color: #2d3436;
            font-size: 1.1rem;
            margin-bottom: 2rem;
            line-height: 1.8;
            position: relative;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
        }

        .author-avatar {
            width: 60px;
            height: 60px;
            background: var(--primary-blue);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            margin-right: 1.5rem;
            font-size: 1.5rem;
            flex-shrink: 0;
        }

        .author-info p {
            margin: 0;
        }

        .author-name {
            font-weight: 700;
            color: var(--primary-blue);
        }

        .author-rank {
            color: var(--secondary-teal);
            font-size: 0.95rem;
        }

        .satisfaction-badge {
            position: absolute;
            bottom: -15px;
            right: 20px;
            background: var(--primary-blue);
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 50px;
            font-weight: bold;
            font-size: 0.8rem;
        }

        /* CTA Sections */
        .cta-section {
            text-align: center;
            padding: 6rem 2rem;
            position: relative;
            overflow: hidden;
            clip-path: polygon(0 10%, 100% 0, 100% 100%, 0% 100%);
            margin-top: 4rem;
            width: 100%;
            box-sizing: border-box;
        }

        .cta-section.gradient {
            background: linear-gradient(135deg, var(--dark-blue), var(--primary-blue));
            color: white;
        }

        .cta-section h2 {
            color: white;
            position: relative;
            margin-bottom: 2rem;
        }

        .cta-section h2::after {
            background: var(--highlight-yellow);
        }

        /* Responsive Adjustments */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero {
                padding: 5rem 2rem 7rem;
                clip-path: polygon(0 0, 100% 0, 100% 95%, 0 100%);
            }

            .hero h1 {
                font-size: 2.4rem;
            }

            .section {
                padding: 3rem 2rem;
                margin: 2rem 1rem;
            }

            .importance-points, .advantage-container, .testimonial-grid {
                grid-template-columns: 1fr;
            }

            .chart-container {
                grid-template-columns: 1fr;
            }

            .cta-buttons {
                flex-direction: column;
                gap: 1rem;
            }

            .timeline::after {
                left: 34px;
            }

            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
                left: 0
            }
            

            .timeline-item::after {
                left: 18px;
            }

            .left::after, .right::after {
                left: 18px;
            }

            .right {
                left: 0%;
            }

            .timeline-section {
                margin: 0 1rem 4rem;
                width: calc(100% - 2rem);
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1.1rem;
            }

            .section {
                padding: 2.5rem 1.5rem;
            }

            h2 {
                font-size: 2rem;
            }

            .pie-chart-legend {
                flex-direction: column;
                align-items: center;
            }

            .timeline-content {
                padding: 1.5rem;
            }

            .timeline-year, .timeline-highlight {
                font-size: 0.7rem;
                padding: 0.3rem 1rem;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Particle Background -->
    <div class="particles" id="particles"></div>
    <div class="confetti" id="confetti"></div>
    
    <!-- Floating Elements -->
    <div class="floating-shape shape-1"></div>
    <div class="floating-shape shape-2"></div>
    <div class="floating-shape shape-3"></div>
    <div class="floating-trophy" style="top: 20%; left: 10%;"><i class="fas fa-trophy"></i></div>
    <div class="floating-trophy" style="top: 30%; right: 15%;"><i class="fas fa-medal"></i></div>
    <div class="floating-trophy" style="bottom: 20%; left: 15%;"><i class="fas fa-award"></i></div>

    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <a href="#" class="logo">
                <i class="fas fa-atom"></i> TestUrSelf
            </a>
            <div class="nav-links">
                <a href="#methodology" class="nav-link">Methodology</a>
                <a href="#results" class="nav-link">Results</a>
                <a href="#timeline" class="nav-link">Our Legacy</a>
                <a href="#testimonials" class="nav-link">Testimonials</a>
                <a href="#cta" class="nav-link">Get Started</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Master GATE Metallurgy with India's #1 Coaching</h1>
            <div class="achievement-badge">
                <i class="fas fa-star"></i> Unstoppable Success Since 2019 <i class="fas fa-star"></i>
            </div>
            <p>Join our legacy of excellence that has produced <strong>7 consecutive AIR-1s</strong>, including <strong>two AIR-1s in 2021</strong> and already secured <strong>GATE 2025 AIR-1</strong>!</p>
            <div class="cta-buttons">
                <a href="#cta" class="btn btn-primary">
                    <i class="fas fa-rocket"></i> Join the Champions
                </a>
                <a href="#timeline" class="btn btn-secondary">
                    <i class="fas fa-trophy"></i> See Our Legacy
                </a>
            </div>
        </div>
    </section>

    <!-- Methodology Section -->
    <section id="methodology" class="section">
        <h2>Our <span>Proven</span> Methodology</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">The system that has consistently produced top rankers in GATE Metallurgical Engineering</p>
        
        <div class="importance-points">
            <div class="point-card">
                <div class="point-number">01</div>
                <div class="point-content">
                    <h4><i class="fas fa-book-open"></i> Comprehensive Study Material</h4>
                    <p>Expert-designed content covering all GATE MT syllabus with depth and clarity. Updated annually by GATE Top rankers.</p>
                </div>
            </div>
            
            <div class="point-card">
                <div class="point-number">02</div>
                <div class="point-content">
                    <h4><i class="fas fa-pen-fancy"></i> Strategic Test Series</h4>
                    <p>25+ full-length tests simulating actual GATE exam conditions with detailed performance analysis.</p>
                </div>
            </div>
            
            <div class="point-card">
                <div class="point-number">03</div>
                <div class="point-content">
                    <h4><i class="fas fa-brain"></i> Concept Clarity Sessions</h4>
                    <p>Regular doubt-clearing sessions focused on core metallurgy concepts and problem-solving techniques.</p>
                </div>
            </div>
            
            <div class="point-card">
                <div class="point-number">04</div>
                <div class="point-content">
                    <h4><i class="fas fa-chart-line"></i> Performance Analytics</h4>
                    <p>Advanced dashboard tracking your progress, strengths, and areas needing improvement.</p>
                </div>
            </div>
            
            <div class="point-card">
                <div class="point-number">05</div>
                <div class="point-content">
                    <h4><i class="fas fa-history"></i> PYQ Mastery Program</h4>
                    <p>Complete analysis of previous year questions (2000-2025) with pattern recognition techniques.</p>
                </div>
            </div>
            
            <div class="point-card">
                <div class="point-number">06</div>
                <div class="point-content">
                    <h4><i class="fas fa-user-graduate"></i> Mentorship Program</h4>
                    <p>Personal guidance from past GATE toppers who've been through our program.</p>
                </div>
            </div>
        </div>
        
        <div class="chart-container">
            <div class="chart-card">
                <h3>Score Improvement Over Time</h3>
                <div class="chart-wrapper">
                    <canvas id="improvementChart"></canvas>
                </div>
                <p style="text-align: center; margin-top: 1rem; font-weight: 500; color: var(--dark-blue);">Average score progression of our students (n=850)</p>
            </div>
            
            <div class="chart-card">
                <h3>Topic-Wise Score Distribution</h3>
                <div class="chart-wrapper">
                    <canvas id="topicChart"></canvas>
                </div>
                <p style="text-align: center; margin-top: 1rem; font-weight: 500; color: var(--dark-blue);">Our students' performance across key MT topics</p>
            </div>
        </div>
    </section>

    <!-- Results Section -->
    <section id="results" class="section">
        <h2>Consistent <span>Top Results</span></h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">Our students' achievements in recent GATE Metallurgy exams</p>
        
        <div class="chart-container">
            <div class="chart-card">
                <h3>Rank Distribution of Our Students</h3>
                <div class="chart-wrapper">
                    <div class="pie-chart-container">
                        <div class="pie-chart-wrapper">
                            <canvas id="rankChart"></canvas>
                        </div>
                        <div class="pie-chart-legend">
                            <div class="legend-item">
                                <span class="legend-color" style="background: #176b87;"></span>
                                <span>AIR 1-10 (8%)</span>
                            </div>
                            <div class="legend-item">
                                <span class="legend-color" style="background: #229954;"></span>
                                <span>AIR 11-100 (32%)</span>
                            </div>
                            <div class="legend-item">
                                <span class="legend-color" style="background: #7c4dff;"></span>
                                <span>AIR 101-500 (45%)</span>
                            </div>
                            <div class="legend-item">
                                <span class="legend-color" style="background: #f8e71c;"></span>
                                <span>AIR 500+ (15%)</span>
                            </div>
                        </div>
                    </div>
                </div>
                <p style="text-align: center; margin-top: 1rem; font-weight: 500; color: var(--dark-blue);">40% of our students achieve AIR < 100</p>
            </div>
            
            <div class="chart-card">
                <h3>Year-wise AIR-1 Production</h3>
                <div class="chart-wrapper">
                    <canvas id="air1Chart"></canvas>
                </div>
                <p style="text-align: center; margin-top: 1rem; font-weight: 500; color: var(--dark-blue);">Consistent production of GATE MT toppers</p>
            </div>
        </div>
        
        <table class="comparison-table">
            <thead>
                <tr>
                    <th>Parameter</th>
                    <th>TestUrSelf Students</th>
                    <th>National Average</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>AIR < 100</td>
                    <td class="check-mark">40%</td>
                    <td class="cross-mark">8%</td>
                </tr>
                <tr>
                    <td>Average Score</td>
                    <td class="check-mark">68.5</td>
                    <td class="cross-mark">52.3</td>
                </tr>
                <tr>
                    <td>Qualification Rate</td>
                    <td class="check-mark">92%</td>
                    <td class="cross-mark">67%</td>
                </tr>
                <tr>
                    <td>Negative Marking</td>
                    <td class="check-mark">-4.2 avg</td>
                    <td class="cross-mark">-9.8 avg</td>
                </tr>
                <tr>
                    <td>Time Management</td>
                    <td class="check-mark">94% complete paper</td>
                    <td class="cross-mark">72% complete paper</td>
                </tr>
            </tbody>
        </table>
    </section>

    <!-- Timeline Section -->
    <section id="timeline" class="timeline-section">
        <div class="timeline-container">
            <div class="timeline-header">
                <h2>Our Legacy of Excellence</h2>
                <p>Every year, a new champion emerges from TestUrSelf. Join us in this journey of continuous achievement.</p>
            </div>
            
            <div class="timeline">
                <div class="timeline-item left">
                <div class="timeline-1"></div>
                    <div class="timeline-content">
                        <div class="timeline-year">GATE 2019</div>
                        <h3>The Beginning of Dominance</h3>
                        <p>First AIR-1 in GATE Metallurgy, establishing our reputation as the premier coaching institute.</p>
                        <div class="timeline-highlight">Trailblazer</div>
                    </div>
                </div>
                
                <div class="timeline-item left">
                 <div class="timeline-1"></div>
                    <div class="timeline-content">
                        <div class="timeline-year">GATE 2020</div>
                        <h3>Consistency Proved</h3>
                        <p>Back-to-back AIR-1 achievement, demonstrating our systematic approach to success.</p>
                        <div class="timeline-highlight">Repeat Champion</div>
                    </div>
                </div>
                
                <div class="timeline-item left" style="position: relative;">
                 <div class="timeline-1"></div>
                    <div class="celebration-badge">2X</div>
                    <div class="timeline-content">
                        <div class="timeline-year">GATE 2021</div>
                        <h3>Double Triumph</h3>
                        <p>Historic year with <strong>two AIR-1 rankers</strong> from our institute, a feat unmatched in GATE MT coaching.</p>
                        <div class="timeline-highlight">Unprecedented</div>
                    </div>
                </div>
                
                <div class="timeline-item left">
                 <div class="timeline-1"></div>
                    <div class="timeline-content">
                        <div class="timeline-year">GATE 2022</div>
                        <h3>Sustaining Excellence</h3>
                        <p>Continued our streak with another top ranker, proving our methodology works year after year.</p>
                        <div class="timeline-highlight">Consistent</div>
                    </div>
                </div>
                
                <div class="timeline-item left">
                 <div class="timeline-1"></div>
                    <div class="timeline-content">
                        <div class="timeline-year">GATE 2023</div>
                        <h3>Perfecting the Process</h3>
                        <p>Our refined teaching approach delivered yet another outstanding result.</p>
                        <div class="timeline-highlight">Refined</div>
                    </div>
                </div>
                
                <div class="timeline-item left">
                 <div class="timeline-1"></div>
                    <div class="timeline-content">
                        <div class="timeline-year">GATE 2024</div>
                        <h3>Tradition of Triumph</h3>
                        <p>Sixth consecutive year producing the GATE MT topper, setting a new benchmark.</p>
                        <div class="timeline-highlight">Tradition</div>
                    </div>
                </div>
                
                <div class="timeline-item left" style="position: relative;">
                 <div class="timeline-2"></div>
                    <div class="celebration-badge">NEW</div>
                    <div class="timeline-content">
                        <div class="timeline-year">GATE 2025</div>
                        <h3>The Legacy Continues</h3>
                        <p>Already secured AIR-1 for GATE 2025! Our seventh consecutive year at the top.</p>
                        <div class="timeline-highlight">Unstoppable</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Advantage Section -->
    <section id="advantage" class="section">
        <h2>The <span>TestUrSelf</span> Advantage</h2>
        <p class="text-center" style="max-width: 700px; margin: 0 auto 2rem;">Why our GATE Metallurgy program delivers superior results</p>
        
        <div class="advantage-container">
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-medal"></i>
                </div>
                <h4>Proven Track Record</h4>
                <p>7 consecutive years producing GATE MT toppers with identical methodology.</p>
            </div>
            
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-chalkboard-teacher"></i>
                </div>
                <h4>Expert Faculty</h4>
                <p>Learn from Samarjeet Kumar Singh and past GATE toppers who understand exam patterns.</p>
            </div>
            
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-project-diagram"></i>
                </div>
                <h4>Comprehensive Material</h4>
                <p>5000+ questions with 30% annual renewal to match evolving GATE patterns.</p>
            </div>
            
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-brain"></i>
                </div>
                <h4>Concept Mastery</h4>
                <p>Focus on deep conceptual understanding rather than rote memorization.</p>
            </div>
            
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-user-friends"></i>
                </div>
                <h4>Personal Mentorship</h4>
                <p>Regular one-on-one sessions to address individual weaknesses.</p>
            </div>
            
            <div class="advantage-card">
                <div class="advantage-icon">
                    <i class="fas fa-percentage"></i>
                </div>
                <h4>High Match Rate</h4>
                <p>Last year, 22 questions matched directly with our final test series.</p>
            </div>
        </div>
        
        <div class="chart-container">
            <div class="chart-card">
                <h3>Student Satisfaction Survey</h3>
                <div class="chart-wrapper">
                    <canvas id="satisfactionChart"></canvas>
                </div>
                <p style="text-align: center; margin-top: 1rem; font-weight: 500; color: var(--dark-blue);">2023 GATE batch satisfaction ratings</p>
            </div>
            
            <div class="chart-card">
                <h3>Question Match Rate</h3>
                <div class="chart-wrapper">
                    <div class="pie-chart-container">
                        <div class="pie-chart-wrapper">
                            <canvas id="matchRateChart"></canvas>
                        </div>
                        <div class="pie-chart-legend">
                            <div class="legend-item">
                                <span class="legend-color" style="background: #176b87;"></span>
                                <span>Direct Match (22%)</span>
                            </div>
                            <div class="legend-item">
                                <span class="legend-color" style="background: #229954;"></span>
                                <span>Concept Match (63%)</span>
                            </div>
                            <div class="legend-item">
                                <span class="legend-color" style="background: #7c4dff;"></span>
                                <span>No Match (15%)</span>
                            </div>
                        </div>
                    </div>
                </div>
                <p style="text-align: center; margin-top: 1rem; font-weight: 500; color: var(--dark-blue);">Our tests have highest conceptual match with actual GATE</p>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section id="testimonials" class="testimonials-section">
        <div class="testimonials-container">
            <div class="testimonials-header">
                <h2>Your Success, Our Pride</h2>
                <p>Join thousands of satisfied students who transformed their GATE preparation with TestUrSelf</p>
                <div class="achievement-badge" style="background: var(--primary-blue); color: white; border-color: var(--accent-gold);">
                    <i class="fas fa-heart"></i> 94% Satisfaction Rate <i class="fas fa-heart"></i>
                </div>
            </div>
            
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        The test series was incredibly accurate - I saw at least 30 questions in GATE that were nearly identical to what we practiced. The faculty's guidance was instrumental in my AIR-1 achievement.
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">JG</div>
                        <div class="author-info">
                            <p class="author-name">Jaya Gupta</p>
                            <p class="author-rank">AIR-1 GATE Metallurgy 2020</p>
                        </div>
                    </div>
                    <div class="satisfaction-badge">100% Satisfied</div>
                </div>
                
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        I enrolled in the TestUrSelf Test Series and Practice Question Series (PQS) for GATE MT 2024. The quantity and quality of questions in both were exceptional. These resources helped me identify my strong and weak areas, allowing me to focus on the topics that needed improvement. The well-structured tests played a crucial role in my preparation.
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">HP</div>
                        <div class="author-info">
                            <p class="author-name">Hrutidipan Pradhan</p>
                            <p class="author-rank">AIR-1 GATE Metallurgy 2024</p>
                        </div>
                    </div>
                    <div class="satisfaction-badge">100% Satisfied</div>
                </div>
                
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        Testurself provides me amazing platform to check my GATE MT preparation at the end. The level of questions in Test series are similar to that of GATE Metallurgy level which helped me to do experiment on how to attempt a paper within given time. Overall it was a nice experience.
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">SK</div>
                        <div class="author-info">
                            <p class="author-name">B Vinith Kumar</p>
                            <p class="author-rank">AIR-1 GATE Metallurgy 2021</p>
                        </div>
                    </div>
                    <div class="satisfaction-badge">100% Satisfied</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section id="cta" class="cta-section gradient">
        <div class="floating-trophy" style="top: 30%; left: 20%;"><i class="fas fa-trophy"></i></div>
        <div class="floating-trophy" style="bottom: 30%; right: 20%;"><i class="fas fa-medal"></i></div>
        
        <h2>Ready to Join Our Legacy of Champions?</h2>
        <p style="max-width: 700px; margin: 0 auto 3rem;">Be part of the institute that's redefining GATE Metallurgy success year after year</p>
        
        <div class="cta-buttons">
            <a href="https://online.testurself.in" class="btn btn-primary">
                <i class="fas fa-gem"></i> Enroll Now
            </a>
            <a href="https://online.testurself.in" class="btn btn-secondary">
                <i class="fas fa-book-open"></i> Free Demo
            </a>
        </div>
    </section>

    <script>
        // Create Particle Background
        function createParticles() {
            const container = document.getElementById('particles');
            const particleCount = 30;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                
                // Random properties
                const size = Math.random() * 10 + 5;
                const posX = Math.random() * 100;
                const posY = Math.random() * 100;
                const delay = Math.random() * 5;
                const duration = Math.random() * 10 + 10;
                
                // Apply styles
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                particle.style.left = `${posX}%`;
                particle.style.top = `${posY}%`;
                particle.style.animation = `float ${duration}s ease-in-out ${delay}s infinite alternate`;
                
                container.appendChild(particle);
            }
        }
        
        // Create Confetti
        function createConfetti() {
            const container = document.getElementById('confetti');
            const colors = ['#176b87', '#229954', '#FFD700', '#f8e71c', '#FFFFFF'];
            
            for (let i = 0; i < 100; i++) {
                const confetti = document.createElement('div');
                confetti.classList.add('confetti-piece');
                
                // Random properties
                const size = Math.random() * 10 + 5;
                const posX = Math.random() * 100;
                const delay = Math.random() * 5;
                const duration = Math.random() * 5 + 3;
                const color = colors[Math.floor(Math.random() * colors.length)];
                
                // Apply styles
                confetti.style.width = `${size}px`;
                confetti.style.height = `${size}px`;
                confetti.style.left = `${posX}%`;
                confetti.style.backgroundColor = color;
                confetti.style.animation = `confetti-fall ${duration}s ease-in ${delay}s infinite`;
                confetti.style.animationDelay = `${delay}s`;
                
                container.appendChild(confetti);
            }
        }
        
        // Initialize Charts
        function initCharts() {
            // Improvement Chart
            const improvementCtx = document.getElementById('improvementChart').getContext('2d');
            new Chart(improvementCtx, {
                type: 'line',
                data: {
                    labels: ['Baseline', 'After 5 Tests', 'After 10 Tests', 'After 15 Tests', 'After 20 Tests', 'GATE Actual'],
                    datasets: [{
                        label: 'Average Score',
                        data: [32, 45, 58, 67, 72, 68],
                        backgroundColor: 'rgba(23, 107, 135, 0.1)',
                        borderColor: 'rgba(23, 107, 135, 1)',
                        borderWidth: 3,
                        tension: 0.3,
                        fill: true,
                        pointBackgroundColor: 'white',
                        pointBorderColor: 'rgba(23, 107, 135, 1)',
                        pointBorderWidth: 2,
                        pointRadius: 5,
                        pointHoverRadius: 7
                    }, {
                        label: 'AIR < 100 Cutoff',
                        data: [65, 65, 65, 65, 65, 65],
                        backgroundColor: 'rgba(255, 23, 68, 0.05)',
                        borderColor: 'rgba(255, 23, 68, 1)',
                        borderWidth: 2,
                        borderDash: [5, 5],
                        tension: 0,
                        pointRadius: 0
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            position: 'top',
                            labels: {
                                usePointStyle: true,
                                padding: 20
                            }
                        }
                    },
                    scales: {
                        y: {
                            beginAtZero: true,
                            max: 100,
                            grid: {
                                color: 'rgba(0,0,0,0.05)'
                            },
                            title: {
                                display: true,
                                text: 'Marks (out of 100)'
                            }
                        },
                        x: {
                            grid: {
                                display: false
                            }
                        }
                    }
                }
            });
            
            // Topic Chart
            const topicCtx = document.getElementById('topicChart').getContext('2d');
            new Chart(topicCtx, {
                type: 'radar',
                data: {
                    labels: ['Physical Metallurgy', 'Mechanical Metallurgy', 'Manufacturing', 'Thermodynamics', 'Extractive', 'Maths'],
                    datasets: [{
                        label: 'Initial Accuracy',
                        data: [45, 52, 38, 60, 48, 65],
                        backgroundColor: 'rgba(23, 107, 135, 0.2)',
                        borderColor: 'rgba(23, 107, 135, 1)',
                        borderWidth: 2,
                        pointBackgroundColor: 'rgba(23, 107, 135, 1)',
                        pointRadius: 4
                    }, {
                        label: 'Final Accuracy',
                        data: [78, 82, 75, 88, 80, 92],
                        backgroundColor: 'rgba(34, 153, 84, 0.2)',
                        borderColor: 'rgba(34, 153, 84, 1)',
                        borderWidth: 2,
                        pointBackgroundColor: 'rgba(34, 153, 84, 1)',
                        pointRadius: 4
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            position: 'top',
                            labels: {
                                usePointStyle: true,
                                padding: 20
                            }
                        }
                    },
                    scales: {
                        r: {
                            angleLines: {
                                color: 'rgba(0,0,0,0.1)'
                            },
                            suggestedMin: 30,
                            suggestedMax: 100,
                            grid: {
                                color: 'rgba(0,0,0,0.05)'
                            },
                            pointLabels: {
                                font: {
                                    size: 11
                                }
                            },
                            ticks: {
                                display: false,
                                stepSize: 20
                            }
                        }
                    },
                    elements: {
                        line: {
                            tension: 0.1
                        }
                    }
                }
            });
            
            // Rank Chart
            const rankCtx = document.getElementById('rankChart').getContext('2d');
            new Chart(rankCtx, {
                type: 'doughnut',
                data: {
                    labels: ['AIR 1-10', 'AIR 11-100', 'AIR 101-500', 'AIR 500+'],
                    datasets: [{
                        data: [8, 32, 45, 15],
                        backgroundColor: [
                            'rgba(23, 107, 135, 0.8)',
                            'rgba(34, 153, 84, 0.8)',
                            'rgba(124, 77, 255, 0.8)',
                            'rgba(248, 231, 28, 0.8)'
                        ],
                        borderColor: [
                            'rgba(23, 107, 135, 1)',
                            'rgba(34, 153, 84, 1)',
                            'rgba(124, 77, 255, 1)',
                            'rgba(248, 231, 28, 1)'
                        ],
                        borderWidth: 1,
                        hoverOffset: 10
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    cutout: '65%',
                    plugins: {
                        legend: {
                            display: false
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `${context.label}: ${context.raw}%`;
                                }
                            }
                        }
                    },
                    animation: {
                        animateScale: true,
                        animateRotate: true
                    }
                }
            });
            
            // AIR-1 Chart
            const air1Ctx = document.getElementById('air1Chart').getContext('2d');
            new Chart(air1Ctx, {
                type: 'bar',
                data: {
                    labels: ['2019', '2020', '2021', '2022', '2023', '2024', '2025'],
                    datasets: [{
                        label: 'AIR-1 Produced',
                        data: [1, 1, 2, 1, 1, 1, 1],
                        backgroundColor: 'rgba(23, 107, 135, 0.8)',
                        borderColor: 'rgba(23, 107, 135, 1)',
                        borderWidth: 1,
                        borderRadius: 6
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            display: false
                        }
                    },
                    scales: {
                        y: {
                            beginAtZero: true,
                            max: 1.2,
                            grid: {
                                color: 'rgba(0,0,0,0.05)'
                            }
                        },
                        x: {
                            grid: {
                                display: false
                            }
                        }
                    }
                }
            });
            
            // Satisfaction Chart
            const satisfactionCtx = document.getElementById('satisfactionChart').getContext('2d');
            new Chart(satisfactionCtx, {
                type: 'bar',
                data: {
                    labels: ['TestUrSelf', 'Platform A', 'Platform B', 'Platform C'],
                    datasets: [{
                        label: 'Satisfaction Score (out of 10)',
                        data: [9.2, 7.1, 6.8, 6.3],
                        backgroundColor: [
                            'rgba(23, 107, 135, 0.8)',
                            'rgba(158, 158, 158, 0.8)',
                            'rgba(158, 158, 158, 0.8)',
                            'rgba(158, 158, 158, 0.8)'
                        ],
                        borderColor: [
                            'rgba(23, 107, 135, 1)',
                            'rgba(97, 97, 97, 1)',
                            'rgba(97, 97, 97, 1)',
                            'rgba(97, 97, 97, 1)'
                        ],
                        borderWidth: 1,
                        borderRadius: 6
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            display: false
                        }
                    },
                    scales: {
                        y: {
                            beginAtZero: true,
                            max: 10,
                            grid: {
                                color: 'rgba(0,0,0,0.05)'
                            }
                        },
                        x: {
                            grid: {
                                display: false
                            }
                        }
                    }
                }
            });
            
            // Match Rate Chart
            const matchCtx = document.getElementById('matchRateChart').getContext('2d');
            new Chart(matchCtx, {
                type: 'doughnut',
                data: {
                    labels: ['Direct Match', 'Conceptual Match', 'No Match'],
                    datasets: [{
                        data: [22, 63, 15],
                        backgroundColor: [
                            'rgba(23, 107, 135, 0.8)',
                            'rgba(34, 153, 84, 0.8)',
                            'rgba(124, 77, 255, 0.8)'
                        ],
                        borderColor: [
                            'rgba(23, 107, 135, 1)',
                            'rgba(34, 153, 84, 1)',
                            'rgba(124, 77, 255, 1)'
                        ],
                        borderWidth: 1,
                        hoverOffset: 10
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    cutout: '70%',
                    plugins: {
                        legend: {
                            display: false
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `${context.label}: ${context.raw}%`;
                                }
                            }
                        }
                    },
                    animation: {
                        animateScale: true,
                        animateRotate: true
                    }
                }
            });
        }
        
        // Initialize GSAP Animations
        function initAnimations() {
            gsap.registerPlugin(ScrollTrigger);
            
            // Animate hero elements
            gsap.from('.hero h1', {
                duration: 1,
                y: 50,
                opacity: 0,
                ease: 'power3.out'
            });
            
            gsap.from('.hero p', {
                duration: 1,
                y: 30,
                opacity: 0,
                delay: 0.3,
                ease: 'power3.out'
            });
            
            gsap.from('.cta-buttons', {
                duration: 1,
                y: 30,
                opacity: 0,
                delay: 0.6,
                ease: 'power3.out'
            });
            
            // Animate section headings
            gsap.utils.toArray('h2').forEach((heading, i) => {
                gsap.from(heading, {
                    scrollTrigger: {
                        trigger: heading,
                        start: 'top 80%'
                    },
                    duration: 0.8,
                    y: 30,
                    opacity: 0,
                    ease: 'power3.out'
                });
            });
            
            // Animate cards
            gsap.utils.toArray('.point-card, .advantage-card, .chart-card, .testimonial-card').forEach((card, i) => {
                gsap.from(card, {
                    scrollTrigger: {
                        trigger: card,
                        start: 'top 80%'
                    },
                    duration: 0.6,
                    y: 40,
                    opacity: 0,
                    delay: i * 0.1,
                    ease: 'power3.out'
                });
            });
            
            // Animate table rows
            gsap.utils.toArray('.comparison-table tr').forEach((row, i) => {
                gsap.from(row, {
                    scrollTrigger: {
                        trigger: row,
                        start: 'top 90%'
                    },
                    duration: 0.5,
                    x: i % 2 === 0 ? -30 : 30,
                    opacity: 0,
                    delay: i * 0.05,
                    ease: 'power3.out'
                });
            });
            
            // Animate timeline items
            gsap.utils.toArray('.timeline-item').forEach((item, i) => {
                gsap.from(item, {
                    scrollTrigger: {
                        trigger: item,
                        start: 'top 80%'
                    },
                    duration: 0.8,
                    x: i % 2 === 0 ? -100 : 100,
                    opacity: 0,
                    delay: i * 0.1,
                    ease: 'power3.out'
                });
            });
            
            // Make navigation links clickable with smooth scroll
            document.querySelectorAll('.nav-link').forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    
                    if (targetElement) {
                        gsap.to(window, {
                            duration: 1,
                            scrollTo: {
                                y: targetElement,
                                offsetY: 80
                            },
                            ease: 'power3.inOut'
                        });
                        
                        // Update active state
                        document.querySelectorAll('.nav-link').forEach(navLink => {
                            navLink.classList.remove('active');
                        });
                        this.classList.add('active');
                    }
                });
            });
        }
        
        // Initialize everything when DOM loads
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            createConfetti();
            initCharts();
            initAnimations();
        });
    </script>
</body>
</html>
