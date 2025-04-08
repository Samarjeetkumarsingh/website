<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Samarjeet | GATE AIR-7 | Founder of TestUrSelf</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Montserrat:wght@700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --black: #000000;
            --white: #FFFFFF;
            --accent: #00BFFF;
            --accent-dark: #0080FF;
            --gray: #111111;
            --light-gray: #222222;
            --section-padding: 120px;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--black);
            color: var(--white);
            line-height: 1.7;
            overflow-x: hidden;
        }
        
        h1, h2, h3 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
        }
        
        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 40px;
        }
        
        /* Header */
        header {
            padding: 25px 0;
            position: relative;
            width: 100%;
            top: 0;
            z-index: 1000;
            background-color: rgba(0, 0, 0, 0.9);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }
        
        header.scrolled {
            padding: 15px 0;
            box-shadow: 0 10px 30px rgba(0, 191, 255, 0.1);
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 28px;
            font-weight: 700;
            color: var(--white);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .logo span {
            color: var(--accent);
        }
        
        .logo-icon {
            width: 30px;
            height: 30px;
            background-color: var(--accent);
            border-radius: 5px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .nav-links {
            display: flex;
            gap: 35px;
        }
        
        .nav-links a {
            color: var(--white);
            text-decoration: none;
            font-weight: 500;
            font-size: 16px;
            transition: all 0.3s;
            position: relative;
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: var(--accent);
            transition: width 0.3s;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .nav-links a:hover {
            color: var(--accent);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--white);
            font-size: 24px;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            min-height: 800px;
            display: flex;
            align-items: center;
            padding-top: 80px;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 100%;
            height: 200%;
            background: radial-gradient(circle, rgba(0, 191, 255, 0.1) 0%, rgba(0, 0, 0, 0) 70%);
            z-index: -1;
            animation: pulse 15s infinite alternate;
        }
        
        @keyframes pulse {
            0% {
                transform: scale(1);
                opacity: 0.3;
            }
            100% {
                transform: scale(1.1);
                opacity: 0.1;
            }
        }
        
        .hero-content {
            display: flex;
            align-items: center;
            gap: 80px;
        }
        
        .hero-text {
            flex: 1;
            position: relative;
            z-index: 2;
        }
        
        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
            position: relative;
        }
        
        .hero-image img {
            width: 400px;
            height: 400px;
            border-radius: 20px;
            object-fit: cover;
            border: 5px solid var(--accent);
            box-shadow: 0 20px 50px rgba(0, 191, 255, 0.2);
            transform-style: preserve-3d;
            transition: all 0.5s ease;
        }
        
        .hero-image:hover img {
            transform: perspective(1000px) rotateY(-10deg) rotateX(5deg) scale(1.05);
            box-shadow: 0 30px 70px rgba(0, 191, 255, 0.3);
        }
        
        .hero h1 {
            font-size: 60px;
            margin-bottom: 25px;
            line-height: 1.2;
        }
        
        .hero h1 span {
            color: var(--accent);
            position: relative;
            display: inline-block;
        }
        
        .hero h1 span::after {
            content: '';
            position: absolute;
            bottom: 5px;
            left: 0;
            width: 100%;
            height: 10px;
            background-color: rgba(0, 191, 255, 0.3);
            z-index: -1;
            transform: skewX(-15deg);
        }
        
        .hero p.subtitle {
            font-size: 22px;
            color: #AAAAAA;
            margin-bottom: 40px;
            max-width: 600px;
        }
        
        .typing-text {
            color: var(--accent);
            border-right: 2px solid var(--accent);
            animation: blink 0.7s infinite, typing 3s steps(30) 1s 1 normal both;
            white-space: nowrap;
            overflow: hidden;
            display: inline-block;
        }
        
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        
        @keyframes blink {
            50% { border-color: transparent }
        }
        
        .cta-buttons {
            display: flex;
            gap: 25px;
            margin-top: 50px;
            flex-wrap: wrap;
        }
        
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 15px 35px;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }
        
        .btn i {
            margin-right: 10px;
            font-size: 18px;
        }
        
        .btn-primary {
            background-color: var(--accent);
            color: var(--black);
        }
        
        .btn-primary::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 0;
            height: 100%;
            background-color: var(--white);
            transition: all 0.3s;
            z-index: -1;
        }
        
        .btn-primary:hover::before {
            width: 100%;
        }
        
        .btn-primary:hover {
            color: var(--black);
            box-shadow: 0 10px 30px rgba(0, 191, 255, 0.4);
        }
        
        .btn-secondary {
            border: 2px solid var(--accent);
            color: var(--accent);
        }
        
        .btn-secondary::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 0;
            height: 100%;
            background-color: var(--accent);
            transition: all 0.3s;
            z-index: -1;
        }
        
        .btn-secondary:hover::before {
            width: 100%;
        }
        
        .btn-secondary:hover {
            color: var(--black);
            box-shadow: 0 10px 30px rgba(0, 191, 255, 0.2);
        }
        
        .social-links-hero {
            display: flex;
            gap: 20px;
            margin-top: 40px;
        }
        
        .social-links-hero a {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: var(--light-gray);
            color: var(--white);
            font-size: 18px;
            transition: all 0.3s;
        }
        
        .social-links-hero a:hover {
            background-color: var(--accent);
            color: var(--black);
            transform: translateY(-5px);
        }
        
        /* Stats Section */
        .stats {
            padding: 80px 0;
            background-color: var(--gray);
        }
        
        .stats-container {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 30px;
        }
        
        .stat-item {
            text-align: center;
            padding: 30px;
            flex: 1;
            min-width: 200px;
            position: relative;
        }
        
        .stat-item::after {
            content: '';
            position: absolute;
            right: 0;
            top: 50%;
            transform: translateY(-50%);
            width: 1px;
            height: 60px;
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        .stat-item:last-child::after {
            display: none;
        }
        
        .stat-number {
            font-size: 50px;
            font-weight: 700;
            color: var(--accent);
            margin-bottom: 10px;
            font-family: 'Montserrat', sans-serif;
        }
        
        .stat-label {
            font-size: 16px;
            color: #AAAAAA;
        }
        
        /* About Section */
        .section {
            padding: var(--section-padding) 0;
            position: relative;
        }
        
        .section-title {
            font-size: 42px;
            margin-bottom: 70px;
            text-align: center;
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .section-title span {
            color: var(--accent);
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--accent);
            border-radius: 2px;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 80px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text p {
            margin-bottom: 25px;
            font-size: 18px;
            position: relative;
            padding-left: 20px;
        }
        
        .about-text p::before {
            content: '▹';
            position: absolute;
            left: 0;
            color: var(--accent);
        }
        
        .about-text blockquote {
            border-left: 3px solid var(--accent);
            padding: 20px 30px;
            margin: 40px 0;
            font-style: italic;
            color: #CCCCCC;
            background-color: rgba(0, 191, 255, 0.05);
            border-radius: 0 10px 10px 0;
            position: relative;
            font-size: 20px;
        }
        
        .about-text blockquote::before {
            content: '"';
            position: absolute;
            top: 10px;
            left: 10px;
            font-size: 60px;
            color: rgba(0, 191, 255, 0.1);
            font-family: Georgia, serif;
            line-height: 1;
        }
        
        .about-image {
            flex: 1;
            position: relative;
        }
        
        .about-image-main {
            width: 100%;
            max-width: 500px;
            border-radius: 15px;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5);
            transition: all 0.5s ease;
            position: relative;
            z-index: 2;
        }
        
        .about-image:hover .about-image-main {
            transform: translate(-10px, -10px);
        }
        
        .about-image::before {
            content: '';
            position: absolute;
            top: 20px;
            left: 20px;
            width: 100%;
            height: 100%;
            border: 2px solid var(--accent);
            border-radius: 15px;
            z-index: 1;
            transition: all 0.5s ease;
        }
        
        .about-image:hover::before {
            top: 10px;
            left: 10px;
        }
        
        /* TestUrSelf Section */
        .testurself {
            background-color: var(--gray);
            position: relative;
            overflow: hidden;
        }
        
        .testurself::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 20% 50%, rgba(0, 191, 255, 0.05) 0%, rgba(0, 0, 0, 0) 50%);
            z-index: 0;
        }
        
        .testurself-content {
            display: flex;
            align-items: center;
            gap: 80px;
            position: relative;
            z-index: 1;
        }
        
        .testurself-text {
            flex: 1;
        }
        
        .testurself-text h2 {
            font-size: 36px;
            margin-bottom: 30px;
            color: var(--accent);
        }
        
        .testurself-text p {
            margin-bottom: 25px;
            font-size: 18px;
        }
        
        .testurself-features {
            margin-top: 40px;
        }
        
        .feature-item {
            display: flex;
            align-items: flex-start;
            gap: 20px;
            margin-bottom: 25px;
        }
        
        .feature-icon {
            width: 50px;
            height: 50px;
            background-color: rgba(0, 191, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--accent);
            font-size: 20px;
            flex-shrink: 0;
        }
        
        .feature-content h3 {
            font-size: 20px;
            margin-bottom: 10px;
        }
        
        .feature-content p {
            margin-bottom: 0;
            color: #AAAAAA;
        }
        
        .testurself-image {
            flex: 1;
            position: relative;
        }
        
        .testurself-image img {
            width: 100%;
            border-radius: 15px;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.7);
            transition: all 0.5s ease;
        }
        
        .testurself-image:hover img {
            transform: scale(1.03);
        }
        
        .testurself-cta {
            margin-top: 50px;
        }
        
        /* Journey Section */
        .journey {
            position: relative;
        }
        
        .journey-container {
            position: relative;
            max-width: 1200px;
            margin: 0 auto;
            padding: 60px 0;
        }
        
        .journey-line {
            position: absolute;
            top: 0;
            left: 50%;
            width: 4px;
            height: 100%;
            background: linear-gradient(to bottom, var(--accent), rgba(0, 191, 255, 0.3));
            transform: translateX(-50%);
            z-index: 1;
        }
        
        .timeline {
            position: relative;
            z-index: 2;
        }
        
        .timeline-item {
            position: relative;
            margin-bottom: 80px;
            width: calc(50% - 40px);
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.5s ease;
        }
        
        .timeline-item.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        .timeline-item:nth-child(odd) {
            margin-left: auto;
            padding-left: 70px;
        }
        
        .timeline-item:nth-child(even) {
            margin-right: auto;
            padding-right: 70px;
            text-align: right;
        }
        
        .timeline-content {
            background-color: var(--light-gray);
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            position: relative;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }
        
        .timeline-item:nth-child(odd) .timeline-content::before {
            content: '';
            position: absolute;
            top: 30px;
            left: -10px;
            width: 20px;
            height: 20px;
            background-color: var(--accent);
            transform: rotate(45deg);
            z-index: -1;
        }
        
        .timeline-item:nth-child(even) .timeline-content::before {
            content: '';
            position: absolute;
            top: 30px;
            right: -10px;
            width: 20px;
            height: 20px;
            background-color: var(--accent);
            transform: rotate(45deg);
            z-index: -1;
        }
        
        .timeline-content:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0, 191, 255, 0.2);
            border-color: rgba(0, 191, 255, 0.3);
        }
        
        .timeline-year {
            font-weight: 700;
            color: var(--accent);
            margin-bottom: 15px;
            font-size: 18px;
            display: flex;
            align-items: center;
        }
        
        .timeline-item:nth-child(odd) .timeline-year {
            justify-content: flex-start;
        }
        
        .timeline-item:nth-child(even) .timeline-year {
            justify-content: flex-end;
        }
        
        .timeline-year::before {
            content: '';
            width: 30px;
            height: 2px;
            background-color: var(--accent);
            margin: 0 15px;
        }
        
        .timeline-item:nth-child(even) .timeline-year::before {
            order: 1;
        }
        
        .timeline-content h3 {
            font-size: 24px;
            margin-bottom: 15px;
        }
        
        .timeline-content p {
            color: #CCCCCC;
            margin-bottom: 0;
        }
        
        .timeline-icon {
            position: absolute;
            top: 30px;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background-color: var(--black);
            border: 3px solid var(--accent);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            color: var(--accent);
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.5);
        }
        
        .timeline-item:nth-child(odd) .timeline-icon {
            left: -30px;
        }
        
        .timeline-item:nth-child(even) .timeline-icon {
            right: -30px;
        }
        
        /* Guidance Section */
        .guidance {
            background-color: var(--gray);
            text-align: center;
            position: relative;
        }
        
        .guidance::before {
            content: '';
            position: absolute;
            bottom: 0;
            right: 0;
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, rgba(0, 191, 255, 0.1) 0%, rgba(0, 0, 0, 0) 70%);
            z-index: 0;
        }
        
        .guidance-container {
            position: relative;
            z-index: 1;
        }
        
        .guidance-intro {
            max-width: 800px;
            margin: 0 auto 60px;
        }
        
        .guidance-cards {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 30px;
            margin-top: 50px;
        }
        
        .guidance-card {
            background: linear-gradient(145deg, #111111, #0a0a0a);
            border-radius: 15px;
            padding: 50px 30px;
            width: 350px;
            transition: all 0.5s ease;
            border: 1px solid rgba(255, 255, 255, 0.05);
            position: relative;
            overflow: hidden;
            z-index: 1;
        }
        
        .guidance-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(0, 191, 255, 0.1) 0%, rgba(0, 0, 0, 0) 100%);
            z-index: -1;
            opacity: 0;
            transition: all 0.5s ease;
        }
        
        .guidance-card:hover::before {
            opacity: 1;
        }
        
        .guidance-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 50px rgba(0, 191, 255, 0.1);
            border-color: rgba(0, 191, 255, 0.3);
        }
        
        .guidance-card-icon {
            width: 80px;
            height: 80px;
            background-color: rgba(0, 191, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 25px;
            font-size: 30px;
            color: var(--accent);
            transition: all 0.3s ease;
        }
        
        .guidance-card:hover .guidance-card-icon {
            background-color: var(--accent);
            color: var(--black);
            transform: rotateY(180deg);
        }
        
        .guidance-card h3 {
            font-size: 24px;
            margin-bottom: 20px;
        }
        
        .guidance-card p {
            margin-bottom: 30px;
            color: #CCCCCC;
        }
        
        .guidance-card-price {
            font-size: 28px;
            font-weight: 700;
            color: var(--accent);
            margin-bottom: 25px;
            font-family: 'Montserrat', sans-serif;
        }
        
        .guidance-card-features {
            text-align: left;
            margin-bottom: 30px;
        }
        
        .guidance-card-features li {
            list-style: none;
            margin-bottom: 10px;
            padding-left: 25px;
            position: relative;
        }
        
        .guidance-card-features li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--accent);
        }
        
        /* Contact Section */
        .contact {
            position: relative;
        }
        
        .contact-container {
            display: flex;
            gap: 80px;
        }
        
        .contact-info {
            flex: 1;
        }
        
        .contact-info h2 {
            font-size: 36px;
            margin-bottom: 30px;
            color: var(--accent);
        }
        
        .contact-info p {
            margin-bottom: 40px;
            font-size: 18px;
        }
        
        .contact-details {
            margin-bottom: 40px;
        }
        
        .contact-item {
            display: flex;
            align-items: flex-start;
            gap: 20px;
            margin-bottom: 25px;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background-color: rgba(0, 191, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--accent);
            font-size: 20px;
            flex-shrink: 0;
        }
        
        .contact-content h3 {
            font-size: 20px;
            margin-bottom: 5px;
        }
        
        .contact-content a {
            color: var(--white);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .contact-content a:hover {
            color: var(--accent);
        }
        
        .contact-social {
            display: flex;
            gap: 15px;
        }
        
        .contact-social a {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: var(--light-gray);
            color: var(--white);
            font-size: 18px;
            transition: all 0.3s;
        }
        
        .contact-social a:hover {
            background-color: var(--accent);
            color: var(--black);
            transform: translateY(-5px);
        }
        
        .contact-form {
            flex: 1;
            background-color: var(--light-gray);
            padding: 50px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 10px;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 15px 20px;
            background-color: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 8px;
            color: var(--white);
            font-family: 'Poppins', sans-serif;
            font-size: 16px;
            transition: all 0.3s;
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--accent);
            box-shadow: 0 0 0 3px rgba(0, 191, 255, 0.2);
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        .submit-btn {
            background-color: var(--accent);
            color: var(--black);
            border: none;
            padding: 15px 30px;
            border-radius: 8px;
            font-weight: 600;
            font-size: 16px;
            cursor: pointer;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }
        
        .submit-btn:hover {
            background-color: var(--accent-dark);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 191, 255, 0.2);
        }
        
        /* Footer */
        footer {
            padding: 70px 0 30px;
            background-color: var(--gray);
            position: relative;
        }
        
        .footer-content {
            display: flex;
            gap: 80px;
            margin-bottom: 50px;
        }
        
        .footer-about {
            flex: 2;
        }
        
        .footer-logo {
            font-size: 28px;
            font-weight: 700;
            color: var(--white);
            margin-bottom: 20px;
            display: inline-block;
        }
        
        .footer-logo span {
            color: var(--accent);
        }
        
        .footer-about p {
            margin-bottom: 25px;
            color: #AAAAAA;
        }
        
        .footer-links {
            flex: 1;
        }
        
        .footer-links h3 {
            font-size: 20px;
            margin-bottom: 25px;
            color: var(--white);
        }
        
        .footer-links ul {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 15px;
        }
        
        .footer-links a {
            color: #AAAAAA;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--accent);
        }
        
        .footer-social {
            flex: 1;
        }
        
        .footer-social h3 {
            font-size: 20px;
            margin-bottom: 25px;
            color: var(--white);
        }
        
        .footer-social-links {
            display: flex;
            gap: 15px;
        }
        
        .footer-social-links a {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: var(--light-gray);
            color: var(--white);
            font-size: 18px;
            transition: all 0.3s;
        }
        
        .footer-social-links a:hover {
            background-color: var(--accent);
            color: var(--black);
            transform: translateY(-5px);
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #777777;
        }
        
        /* Back to Top Button */
        .back-to-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            background-color: var(--accent);
            color: var(--black);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            cursor: pointer;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s;
            z-index: 999;
        }
        
        .back-to-top.active {
            opacity: 1;
            visibility: visible;
        }
        
        .back-to-top:hover {
            background-color: var(--white);
            transform: translateY(-5px);
        }
        
        /* Responsive Design */
        @media (max-width: 1200px) {
            .container {
                padding: 0 30px;
            }
            
            .hero-content, .about-content, .testurself-content, .contact-container {
                gap: 50px;
            }
            
            .hero h1 {
                font-size: 50px;
            }
        }
        
        @media (max-width: 992px) {
            .section {
                padding: 80px 0;
            }
            
            .section-title {
                font-size: 36px;
                margin-bottom: 50px;
            }
            
            .hero-content, .about-content, .testurself-content {
                flex-direction: column;
            }
            
            .hero-text, .about-text, .testurself-text {
                order: 2;
            }
            
            .hero-image, .about-image, .testurself-image {
                order: 1;
                margin-bottom: 50px;
            }
            
            .hero h1 {
                font-size: 42px;
            }
            
            .hero p.subtitle {
                font-size: 18px;
            }
            
            .journey-line {
                left: 40px;
            }
            
            .timeline-item {
                width: calc(100% - 80px);
                margin-left: 80px !important;
                padding-left: 50px !important;
                padding-right: 0 !important;
                text-align: left !important;
            }
            
            .timeline-item:nth-child(even) .timeline-icon {
                right: auto;
                left: -30px;
            }
            
            .contact-container {
                flex-direction: column;
            }
            
            .footer-content {
                flex-direction: column;
                gap: 50px;
            }
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 0 20px;
            }
            
            .nav-links {
                display: none;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero {
                min-height: auto;
                padding-top: 100px;
                padding-bottom: 80px;
                height: auto;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero-image img {
                width: 280px;
                height: 280px;
            }
            
            .cta-buttons {
                flex-direction: column;
                gap: 15px;
            }
            
            .btn {
                width: 100%;
                text-align: center;
            }
            
            .stats-container {
                flex-direction: column;
                gap: 30px;
            }
            
            .stat-item::after {
                display: none;
            }
            
            .section-title {
                font-size: 32px;
            }
            
            .contact-form {
                padding: 30px;
            }
        }
        
        @media (max-width: 576px) {
            .hero h1 {
                font-size: 32px;
            }
            
            .section-title {
                font-size: 28px;
            }
            
            .timeline-content {
                padding: 20px;
            }
            
            .timeline-content h3 {
                font-size: 20px;
            }
            
            .guidance-card {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="container">
            <nav>
                <a href="#" class="logo">
                    <div class="logo-icon">S</div>
                    <span>Samarjeet</span>
                </a>
                <div class="nav-links">
                    <a href="#about">About</a>
                    <a href="#testurself">TestUrSelf</a>
                    <a href="#journey">Journey</a>
                    <a href="#guidance">Guidance</a>
                    <a href="#contact">Contact</a>
                </div>
                <button class="mobile-menu-btn">
                    <i class="fas fa-bars"></i>
                </button>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>Hi, I'm <span>Samarjeet</span> <br><span class="typing-text">Turning struggles into strategies</span></h1>
                    <p class="subtitle">Materials Engineer | Founder @ TestUrSelf | BOD @ Mission Kartavya</p>
                    <div class="cta-buttons">
                        <a href="https://www.testurself.in" class="btn btn-primary"><i class="fas fa-rocket"></i> Visit TestUrSelf</a>
                        <a href="#" class="btn btn-secondary"><i class="fas fa-book"></i> View My Notes</a>
                    </div>
                    <div class="social-links-hero">
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-github"></i></a>
                    </div>
                </div>
                <div class="hero-image">
                    <img src="https://images-website-testurself.s3.us-east-1.amazonaws.com/personal.png" alt="Samarjeet">
                </div>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <div class="container">
            <div class="stats-container">
                <div class="stat-item">
                    <div class="stat-number">AIR-7</div>
                    <div class="stat-label">GATE Rank</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">5000+</div>
                    <div class="stat-label">Students Mentored</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">8+</div>
                    <div class="stat-label">Years Experience</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">AIR-1</div>
                    <div class="stat-label">Student Achievements</div>
                </div>
            </div>
        </div>
    </section>

<!-- About Section -->
<section id="about" class="section about-section">
    <div class="container">
        <div class="section-header">
            <h2 class="section-title">About <span>Me</span></h2>
            <div class="title-decoration">
                <div class="decoration-line"></div>
                <div class="decoration-dot"></div>
            </div>
        </div>
        
        <div class="about-content">
            <div class="about-text">
                <div class="intro-text animate-fade">
                    <p>I'm a passionate materials engineer with a dedication for knowledge sharing. Through my personal journey, I document experiences and insights on education systems, exam strategies, and the science of effective learning.</p>
                </div>
                
                <div class="achievements animate-slide">
                    <div class="achievement-item">
                        <div class="achievement-icon">
                            <i class="fas fa-graduation-cap"></i>
                        </div>
                        <div class="achievement-content">
                            <h3>Academic Excellence</h3>
                            <p>Cracked IIT-JEE Advanced & Mains & Secured GATE AIR-7 (2016)</p>
                        </div>
                    </div>
                    
                    <div class="achievement-item">
                        <div class="achievement-icon">
                            <i class="fas fa-university"></i>
                        </div>
                        <div class="achievement-content">
                            <h3>Education</h3>
                            <p>B.Tech in Metallurgical Engineering | Master's from IISc Bangalore</p>
                        </div>
                    </div>
                    
                    <div class="achievement-item">
                        <div class="achievement-icon">
                            <i class="fas fa-book"></i>
                        </div>
                        <div class="achievement-content">
                            <h3>Published Author</h3>
                            <p>Authored a Metallurgy Book during my M.Tech</p>
                        </div>
                    </div>
                    
                    <div class="achievement-item">
                        <div class="achievement-icon">
                            <i class="fas fa-lightbulb"></i>
                        </div>
                        <div class="achievement-content">
                            <h3>Initiatives</h3>
                            <p>Founder of <a href="https://www.testurself.in" class="accent-link">TestUrSelf</a> | BOD at <a href="https://www.instagram.com/kartavya_niamt" class="accent-link">Mission Kartavya Foundation</a></p>
                        </div>
                    </div>
                </div>
                
                <div class="quote-block animate-fade">
                    <div class="quote-icon">
                        <i class="fas fa-quote-left"></i>
                    </div>
                    <blockquote>"Education is the most powerful weapon to change the world."</blockquote>
                </div>
            </div>
            
            <div class="about-image">
                <div class="image-wrapper animate-scale">
                    <img src="https://images-website-testurself.s3.us-east-1.amazonaws.com/2.png" alt="Samarjeet at work" class="about-image-main">
                    <div class="image-border"></div>
                    <div class="image-overlay"></div>
                </div>
            </div>
        </div>
    </div>
</section>

<style>
    /* About Section Styles */
    .about-section {
        background-color: #0a0a0a;
        color: #ffffff;
        padding: 100px 0;
        position: relative;
        overflow: hidden;
    }
    
    .section-header {
        text-align: center;
        margin-bottom: 60px;
    }
    
    .section-title {
        font-size: 3rem;
        font-weight: 700;
        margin: 0;
        color: #ffffff;
        position: relative;
        display: inline-block;
    }
    
    .section-title span {
        color: #00bfff;
        position: relative;
    }
    
    .title-decoration {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-top: 15px;
    }
    
    .decoration-line {
        width: 80px;
        height: 2px;
        background: linear-gradient(90deg, transparent, #00bfff, transparent);
    }
    
    .decoration-dot {
        width: 10px;
        height: 10px;
        background-color: #00bfff;
        border-radius: 50%;
        margin: 0 15px;
    }
    
    /* Content Layout */
    .about-content {
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        gap: 60px;
    }
    
    .about-text {
        flex: 1;
        min-width: 300px;
    }
    
    .about-image {
        flex: 1;
        min-width: 300px;
        position: relative;
    }
    
    /* Text Content */
    .intro-text p {
        font-size: 1.2rem;
        line-height: 1.8;
        color: rgba(255, 255, 255, 0.9);
        margin-bottom: 40px;
    }
    
    /* Achievements */
    .achievements {
        display: grid;
        grid-template-columns: 1fr;
        gap: 25px;
        margin-bottom: 40px;
    }
    
    .achievement-item {
        display: flex;
        gap: 20px;
        align-items: flex-start;
        padding: 20px;
        background: rgba(255, 255, 255, 0.05);
        border-radius: 10px;
        border-left: 3px solid #00bfff;
        transition: all 0.3s ease;
    }
    
    .achievement-item:hover {
        background: rgba(0, 191, 255, 0.1);
        transform: translateY(-5px);
    }
    
    .achievement-icon {
        width: 50px;
        height: 50px;
        background: linear-gradient(135deg, #00bfff, #0066cc);
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        color: white;
        font-size: 20px;
        flex-shrink: 0;
    }
    
    .achievement-content h3 {
        color: #00bfff;
        margin: 0 0 8px 0;
        font-size: 1.2rem;
    }
    
    .achievement-content p {
        margin: 0;
        color: rgba(255, 255, 255, 0.8);
        line-height: 1.6;
    }
    
    .accent-link {
        color: #00bfff;
        text-decoration: none;
        transition: all 0.3s ease;
        border-bottom: 1px solid transparent;
    }
    
    .accent-link:hover {
        color: #ffffff;
        border-bottom: 1px solid #00bfff;
    }
    
    /* Quote Block */
    .quote-block {
        position: relative;
        padding: 30px;
        background: rgba(0, 191, 255, 0.1);
        border-radius: 10px;
        border-left: 4px solid #00bfff;
    }
    
    .quote-icon {
        position: absolute;
        top: -15px;
        left: 30px;
        width: 40px;
        height: 40px;
        background: #0a0a0a;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        color: #00bfff;
        font-size: 18px;
    }
    
    .quote-block blockquote {
        margin: 0;
        font-size: 1.2rem;
        font-style: italic;
        color: rgba(255, 255, 255, 0.9);
        line-height: 1.8;
    }
    
    /* Image Styling */
    .image-wrapper {
        position: relative;
        border-radius: 15px;
        overflow: hidden;
        box-shadow: 0 25px 50px rgba(0, 0, 0, 0.3);
    }
    
    .about-image-main {
        width: 100%;
        height: auto;
        display: block;
        position: relative;
        z-index: 1;
        transition: transform 0.5s ease;
    }
    
    .image-border {
        position: absolute;
        top: 10px;
        left: 10px;
        right: 10px;
        bottom: 10px;
        border: 2px solid rgba(0, 191, 255, 0.5);
        border-radius: 10px;
        z-index: 2;
        pointer-events: none;
    }
    
    .image-overlay {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: linear-gradient(135deg, rgba(0, 191, 255, 0.1), rgba(0, 191, 255, 0));
        z-index: 1;
    }
    
    .image-wrapper:hover .about-image-main {
        transform: scale(1.03);
    }
    
    /* Animations */
    .animate-fade {
        opacity: 0;
        animation: fadeIn 1s ease-out forwards;
    }
    
    .animate-slide {
        opacity: 0;
        transform: translateY(30px);
        animation: slideUp 1s ease-out forwards;
    }
    
    .animate-scale {
        opacity: 0;
        transform: scale(0.95);
        animation: scaleIn 1s ease-out forwards;
    }
    
    @keyframes fadeIn {
        to { opacity: 1; }
    }
    
    @keyframes slideUp {
        to { opacity: 1; transform: translateY(0); }
    }
    
    @keyframes scaleIn {
        to { opacity: 1; transform: scale(1); }
    }
    
    /* Animation Delays */
    .intro-text { animation-delay: 0.3s; }
    .achievement-item:nth-child(1) { animation-delay: 0.5s; }
    .achievement-item:nth-child(2) { animation-delay: 0.7s; }
    .achievement-item:nth-child(3) { animation-delay: 0.9s; }
    .achievement-item:nth-child(4) { animation-delay: 1.1s; }
    .quote-block { animation-delay: 1.3s; }
    .image-wrapper { animation-delay: 0.5s; }
    
    /* Responsive Design */
    @media (max-width: 768px) {
        .about-content {
            flex-direction: column-reverse;
        }
        
        .section-title {
            font-size: 2.2rem;
        }
        
        .achievement-item {
            flex-direction: column;
            align-items: flex-start;
        }
        
        .achievement-icon {
            margin-bottom: 15px;
        }
    }
</style>
 <!-- TestUrSelf Section -->
<section id="testurself" class="section testurself">
    <div class="container">
        <div class="testurself-content">
            <div class="testurself-text">
                <div class="heading-container">
                    <h2 class="section-heading">TestUrSelf - For GATE Aspirants</h2>
                    <svg class="curly-arrow" width="180" height="60" viewBox="0 0 180 60" xmlns="http://www.w3.org/2000/svg">
                        <path d="M5,30 C50,-20 100,80 175,30" 
                              fill="none" 
                              stroke="#00bfff" 
                              stroke-width="3" 
                              stroke-linecap="round"
                              stroke-dasharray="250" 
                              stroke-dashoffset="250"/>
                    </svg>
                </div>
                <div class="content-block">
                    <p>Founded with a vision to revolutionize exam preparation, TestUrSelf provides comprehensive resources and guidance for GATE aspirants, especially in Metallurgical and Materials Engineering.</p>
                    <p>What started as a small initiative from my room has now helped hundreds of students achieve their dreams, including producing AIR-1 rank holders.</p>
                </div>
                
                <div class="testurself-features">
                    <div class="feature-item">
                        <div class="feature-icon">
                            <i class="fas fa-book"></i>
                        </div>
                        <div class="feature-content">
                            <h3>Comprehensive Study Material</h3>
                            <p>Curated notes, practice questions, and previous year papers with detailed solutions.</p>
                        </div>
                    </div>
                    <div class="feature-item">
                        <div class="feature-icon">
                            <i class="fas fa-chalkboard-teacher"></i>
                        </div>
                        <div class="feature-content">
                            <h3>Expert Guidance</h3>
                            <p>Personal mentorship from toppers who understand the exam inside out.</p>
                        </div>
                    </div>
                    <div class="feature-item">
                        <div class="feature-icon">
                            <i class="fas fa-tasks"></i>
                        </div>
                        <div class="feature-content">
                            <h3>Strategic Preparation</h3>
                            <p>Customized study plans tailored to individual strengths and weaknesses.</p>
                        </div>
                    </div>
                </div>
                
                <div class="testurself-cta">
                    <a href="https://www.testurself.in" class="btn btn-primary"><i class="fas fa-external-link-alt"></i> Explore TestUrSelf</a>
                </div>
            </div>
            <div class="testurself-image">
                <div class="image-container">
                    <img src="https://images-website-testurself.s3.us-east-1.amazonaws.com/AIR-1+Toppers.png" alt="TestUrSelf Students">
                </div>
            </div>
        </div>
    </div>
</section>

<style>
    /* Base Styles */
    .testurself {
        background-color: #000;
        color: #fff;
        padding: 100px 0;
        position: relative;
        overflow: hidden;
    }
    
    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 0 20px;
    }
    
    /* Content Layout */
    .testurself-content {
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        gap: 60px;
    }
    
    .testurself-text {
        flex: 1;
        min-width: 300px;
    }
    
    .testurself-image {
        flex: 1;
        min-width: 300px;
        position: relative;
    }
    
    /* Heading Styles */
    .heading-container {
        position: relative;
        margin-bottom: 40px;
    }
    
    .section-heading {
        color: #00bfff;
        font-size: 2.5rem;
        margin: 0;
        position: relative;
        display: inline-block;
    }
    
    /* Curly Arrow Styles */
    .curly-arrow {
        position: absolute;
        right: -180px;
        top: 50%;
        transform: translateY(-50%);
    }
    
    .curly-arrow path {
        animation: drawArrow 1.5s ease-out forwards;
        animation-delay: 0.5s;
    }
    
    @keyframes drawArrow {
        to { stroke-dashoffset: 0; }
    }
    
    /* Content Block */
    .content-block {
        margin-bottom: 40px;
    }
    
    .content-block p {
        color: #fff;
        font-size: 1.1rem;
        line-height: 1.6;
        margin-bottom: 20px;
        opacity: 0;
        animation: fadeInUp 0.8s ease-out forwards;
    }
    
    .content-block p:nth-child(1) {
        animation-delay: 0.3s;
    }
    
    .content-block p:nth-child(2) {
        animation-delay: 0.6s;
    }
    
    @keyframes fadeInUp {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
    }
    
    /* Features Section */
    .testurself-features {
        margin: 50px 0;
    }
    
    .feature-item {
        display: flex;
        gap: 20px;
        margin-bottom: 30px;
        background: rgba(255, 255, 255, 0.05);
        padding: 25px;
        border-radius: 12px;
        border-left: 3px solid #00bfff;
        opacity: 0;
        transform: translateY(20px);
        animation: fadeInUp 0.8s ease-out forwards;
    }
    
    .feature-item:nth-child(1) {
        animation-delay: 0.9s;
    }
    
    .feature-item:nth-child(2) {
        animation-delay: 1.1s;
    }
    
    .feature-item:nth-child(3) {
        animation-delay: 1.3s;
    }
    
    .feature-icon {
        width: 60px;
        height: 60px;
        background: linear-gradient(135deg, #00bfff 0%, #0066cc 100%);
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        color: white;
        font-size: 24px;
        flex-shrink: 0;
    }
    
    .feature-content h3 {
        color: #00bfff;
        margin-top: 0;
        margin-bottom: 10px;
        font-size: 1.3rem;
    }
    
    .feature-content p {
        color: rgba(255, 255, 255, 0.8);
        margin: 0;
        line-height: 1.6;
    }
    
    /* Image Container */
    .image-container {
        border-radius: 12px;
        overflow: hidden;
        box-shadow: 0 25px 50px rgba(0, 191, 255, 0.15);
        opacity: 0;
        transform: scale(0.95);
        animation: fadeInScale 1s ease-out forwards;
        animation-delay: 0.8s;
    }
    
    @keyframes fadeInScale {
        to { opacity: 1; transform: scale(1); }
    }
    
    .image-container img {
        width: 100%;
        height: auto;
        display: block;
        transition: transform 0.5s ease;
    }
    
    .image-container:hover img {
        transform: scale(1.03);
    }
    
    /* CTA Button */
    .testurself-cta {
        opacity: 0;
        animation: fadeIn 0.8s ease-out forwards;
        animation-delay: 1.5s;
    }
    
    @keyframes fadeIn {
        to { opacity: 1; }
    }
    
    .btn-primary {
        display: inline-flex;
        align-items: center;
        gap: 10px;
        background: linear-gradient(135deg, #00bfff 0%, #0066cc 100%);
        color: white;
        padding: 15px 30px;
        border-radius: 50px;
        text-decoration: none;
        font-weight: 600;
        font-size: 1.1rem;
        box-shadow: 0 5px 15px rgba(0, 191, 255, 0.3);
        transition: all 0.3s ease;
    }
    
    .btn-primary:hover {
        transform: translateY(-3px);
        box-shadow: 0 8px 25px rgba(0, 191, 255, 0.5);
    }
    
    /* Responsive Design */
    @media (max-width: 1100px) {
        .curly-arrow {
            right: -150px;
            width: 150px;
        }
    }
    
    @media (max-width: 992px) {
        .curly-arrow {
            right: -120px;
            width: 120px;
        }
    }
    
    @media (max-width: 768px) {
        .testurself-content {
            flex-direction: column;
        }
        
        .heading-container {
            margin-bottom: 70px;
        }
        
        .curly-arrow {
            right: auto;
            left: 50%;
            top: 100%;
            transform: translateX(-50%) rotate(90deg);
            width: 80px;
            height: 120px;
        }
        
        .section-heading {
            font-size: 2rem;
        }
    }
</style>

    <!-- Journey Section -->
<section id="journey" class="section journey">
    <div class="container">
        <h2 class="section-title">My <span>Journey</span></h2>
        <div class="journey-container">
            <div class="journey-line"></div>
            <div class="timeline">
                <!-- Timeline Item 1 -->
                <div class="timeline-item">
                    <div class="timeline-year">2008</div>
                    <div class="timeline-icon">
                        <i class="fas fa-medal"></i>
                    </div>
                    <div class="timeline-content">
                        <h3>Cracked Bihar Polytechnic</h3>
                        <p>Achieved top ranks in Bihar Polytechnic entrance exam, marking my first major academic success.</p>
                        <div class="timeline-badge">First Achievement</div>
                    </div>
                </div>
                
                <!-- Timeline Item 2 -->
                <div class="timeline-item">
                    <div class="timeline-year">2011</div>
                    <div class="timeline-icon">
                        <i class="fas fa-atom"></i>
                    </div>
                    <div class="timeline-content">
                        <h3>Cracked IIT-JEE Advanced & Mains</h3>
                        <p>Cleared one of India's toughest engineering entrance exams with exceptional scores.</p>
                        <div class="timeline-badge">National Level</div>
                    </div>
                </div>
                
                <!-- Timeline Item 3 -->
                <div class="timeline-item">
                    <div class="timeline-year">2012</div>
                    <div class="timeline-icon">
                        <i class="fas fa-graduation-cap"></i>
                    </div>
                    <div class="timeline-content">
                        <h3>Cracked IIT Mains</h3>
                        <p>Secured admission to premier engineering institute for Metallurgical Engineering.</p>
                        <div class="timeline-badge">Engineering Start</div>
                    </div>
                </div>
                
                <!-- Timeline Item 4 -->
                <div class="timeline-item">
                    <div class="timeline-year">2016</div>
                    <div class="timeline-icon">
                        <i class="fas fa-trophy"></i>
                    </div>
                    <div class="timeline-content">
                        <h3>GATE AIR-7</h3>
                        <p>Achieved All India Rank 7 in GATE for Metallurgical Engineering.</p>
                        <div class="timeline-badge">Top 0.1%</div>
                    </div>
                </div>
                
                <!-- Timeline Item 5 -->
                <div class="timeline-item">
                    <div class="timeline-year">2017</div>
                    <div class="timeline-icon">
                        <i class="fas fa-lightbulb"></i>
                    </div>
                    <div class="timeline-content">
                        <h3>Founded TestUrSelf</h3>
                        <p>Launched educational initiative to help students crack competitive exams.</p>
                        <div class="timeline-badge">Entrepreneurship</div>
                    </div>
                </div>
                
                <!-- Timeline Item 6 -->
                <div class="timeline-item">
                    <div class="timeline-year">2019</div>
                    <div class="timeline-icon">
                        <i class="fas fa-university"></i>
                    </div>
                    <div class="timeline-content">
                        <h3>Master's from IISc</h3>
                        <p>Completed M.Tech from Indian Institute of Science, Bangalore.</p>
                        <div class="timeline-badge">Research Excellence</div>
                    </div>
                </div>
                
                <!-- Timeline Item 7 -->
                <div class="timeline-item">
                    <div class="timeline-year">2022</div>
                    <div class="timeline-icon">
                        <i class="fas fa-hands-helping"></i>
                    </div>
                    <div class="timeline-content">
                        <h3>Mission Kartavya</h3>
                        <p>Became BOD at Mission Kartavya Foundation to mentor students.</p>
                        <div class="timeline-badge">Social Impact</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<style>
/* Journey Section Styles */
.journey {
    background-color: #0a0e17;
    position: relative;
    padding: 100px 0;
}

.journey-container {
    position: relative;
    max-width: 1200px;
    margin: 0 auto;
    padding: 60px 0;
}

.journey-line {
    position: absolute;
    top: 0;
    left: 50%;
    width: 4px;
    height: 100%;
    background: linear-gradient(to bottom, #00BFFF, rgba(0, 191, 255, 0.3));
    transform: translateX(-50%);
    z-index: 1;
}

.timeline {
    position: relative;
    z-index: 2;
}

.timeline-item {
    position: relative;
    margin-bottom: 80px;
    width: calc(50% - 40px);
}

.timeline-item:nth-child(odd) {
    margin-left: auto;
    padding-left: 70px;
}

.timeline-item:nth-child(even) {
    margin-right: auto;
    padding-right: 70px;
    text-align: right;
}

.timeline-content {
    background: linear-gradient(145deg, #111827, #0a0e17);
    border-radius: 15px;
    padding: 30px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
    position: relative;
    border: 1px solid rgba(0, 191, 255, 0.1);
    transition: all 0.5s ease;
}

.timeline-item:nth-child(odd) .timeline-content::before {
    content: '';
    position: absolute;
    top: 30px;
    left: -10px;
    width: 20px;
    height: 20px;
    background-color: #00BFFF;
    transform: rotate(45deg);
    z-index: -1;
}

.timeline-item:nth-child(even) .timeline-content::before {
    content: '';
    position: absolute;
    top: 30px;
    right: -10px;
    width: 20px;
    height: 20px;
    background-color: #00BFFF;
    transform: rotate(45deg);
    z-index: -1;
}

.timeline-content:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 40px rgba(0, 191, 255, 0.2);
    border-color: rgba(0, 191, 255, 0.3);
}

.timeline-year {
    font-weight: 700;
    color: #00BFFF;
    margin-bottom: 15px;
    font-size: 18px;
    display: flex;
    align-items: center;
}

.timeline-item:nth-child(odd) .timeline-year {
    justify-content: flex-start;
}

.timeline-item:nth-child(even) .timeline-year {
    justify-content: flex-end;
}

.timeline-year::before {
    content: '';
    width: 30px;
    height: 2px;
    background-color: #00BFFF;
    margin: 0 15px;
}

.timeline-item:nth-child(even) .timeline-year::before {
    order: 1;
}

.timeline-content h3 {
    font-size: 24px;
    margin-bottom: 15px;
    color: white;
}

.timeline-content p {
    color: #CCCCCC;
    margin-bottom: 0;
}

.timeline-icon {
    position: absolute;
    top: 30px;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    background-color: #0a0e17;
    border: 3px solid #00BFFF;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 24px;
    color: #00BFFF;
    box-shadow: 0 5px 20px rgba(0, 0, 0, 0.5);
}

.timeline-item:nth-child(odd) .timeline-icon {
    left: -30px;
}

.timeline-item:nth-child(even) .timeline-icon {
    right: -30px;
}

.timeline-badge {
    display: inline-block;
    padding: 5px 12px;
    background: rgba(0, 191, 255, 0.1);
    color: #00BFFF;
    border-radius: 20px;
    font-size: 12px;
    font-weight: 600;
    margin-top: 15px;
}

/* Responsive Styles */
@media (max-width: 992px) {
    .journey-line {
        left: 40px;
    }
    
    .timeline-item {
        width: calc(100% - 80px);
        margin-left: 80px !important;
        padding-left: 50px !important;
        padding-right: 0 !important;
        text-align: left !important;
    }
    
    .timeline-item:nth-child(even) .timeline-icon {
        right: auto;
        left: -30px;
    }
}
</style>

<!-- Guidance Section -->
<section id="guidance" class="section guidance">
    <div class="container">
        <h2 class="section-title">1:1 <span>Mentorship Program</span></h2>
        <div class="guidance-intro">
            <p>Personalized guidance for GATE Metallurgy/Materials Science aspirants who want structured preparation and expert insights.</p>
        </div>
        
        <div class="guidance-cards">
            <!-- Card 1 -->
            <div class="guidance-card">
                <div class="guidance-card-badge">Most Popular</div>
                <div class="guidance-card-icon">
                    <i class="fas fa-chess-knight"></i>
                </div>
                <h3>Strategy Blueprint</h3>
                <div class="guidance-card-price">₹3,999 <span>/ session</span></div>
                <div class="guidance-card-features">
                    <ul>
                        <li><i class="fas fa-check"></i> 2-hour intensive consultation</li>
                        <li><i class="fas fa-check"></i> Customized 3-month roadmap</li>
                        <li><i class="fas fa-check"></i> Resource recommendations</li>
                        <li><i class="fas fa-check"></i> Priority email support</li>
                    </ul>
                </div>
                <a href="#" class="btn btn-secondary">Book Now</a>
            </div>
            
            <!-- Card 2 -->
            <div class="guidance-card featured">
                <div class="guidance-card-badge">Recommended</div>
                <div class="guidance-card-icon">
                    <i class="fas fa-calendar-alt"></i>
                </div>
                <h3>3-Month Accelerator</h3>
                <div class="guidance-card-price">₹24,999 <span>/ 3 months</span></div>
                <div class="guidance-card-features">
                    <ul>
                        <li><i class="fas fa-check"></i> 12 sessions (1 per week)</li>
                        <li><i class="fas fa-check"></i> Doubt resolution sessions</li>
                        <li><i class="fas fa-check"></i> Study material recommendations</li>
                        <li><i class="fas fa-check"></i> Mock test analysis (3 tests)</li>
                        <li><i class="fas fa-check"></i> WhatsApp support</li>
                    </ul>
                </div>
                <a href="#" class="btn btn-primary">Enroll Now</a>
            </div>
            
            <!-- Card 3 -->
            <div class="guidance-card">
                <div class="guidance-card-icon">
                    <i class="fas fa-crown"></i>
                </div>
                <h3>Elite Mentorship</h3>
                <div class="guidance-card-price">₹49,999 <span>/ 6 months</span></div>
                <div class="guidance-card-features">
                    <ul>
                        <li><i class="fas fa-check"></i> 24 sessions (1 per week)</li>
                        <li><i class="fas fa-check"></i> Comprehensive preparation plan</li>
                        <li><i class="fas fa-check"></i> 6 mock tests with analysis</li>
                        <li><i class="fas fa-check"></i> Personalized notes review</li>
                        <li><i class="fas fa-check"></i> 24/7 priority support</li>
                        <li><i class="fas fa-check"></i> Interview preparation</li>
                    </ul>
                </div>
                <a href="#" class="btn btn-secondary">Apply Now</a>
            </div>
        </div>
    </div>
</section>

<style>
/* Guidance Section Styles */
.guidance {
    background: linear-gradient(135deg, #111827 0%, #0a0e17 100%);
    padding: 100px 0;
}

.guidance-intro {
    max-width: 800px;
    margin: 0 auto 60px;
    text-align: center;
    color: #AAAAAA;
}

.guidance-cards {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 30px;
    margin-top: 50px;
}

.guidance-card {
    background: linear-gradient(145deg, #111827, #0a0e17);
    border-radius: 15px;
    padding: 40px 30px;
    width: 350px;
    transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    position: relative;
    overflow: hidden;
    border: 1px solid rgba(0, 191, 255, 0.1);
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
}

.guidance-card::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(135deg, rgba(0, 191, 255, 0.05) 0%, transparent 100%);
    opacity: 0;
    transition: all 0.5s ease;
}

.guidance-card:hover {
    transform: translateY(-10px) scale(1.02);
    box-shadow: 0 20px 50px rgba(0, 191, 255, 0.15);
    border-color: rgba(0, 191, 255, 0.3);
}

.guidance-card:hover::after {
    opacity: 1;
}

.guidance-card.featured {
    border: 2px solid #00BFFF;
    transform: translateY(-10px);
}

.guidance-card.featured:hover {
    transform: translateY(-15px) scale(1.03);
}

.guidance-card-badge {
    position: absolute;
    top: 15px;
    right: -30px;
    background: #00BFFF;
    color: #000000;
    padding: 5px 30px;
    font-size: 12px;
    font-weight: 700;
    transform: rotate(45deg);
    width: 120px;
    text-align: center;
}

.guidance-card-icon {
    width: 80px;
    height: 80px;
    background: rgba(0, 191, 255, 0.1);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 25px;
    font-size: 30px;
    color: #00BFFF;
    border: 2px solid rgba(0, 191, 255, 0.2);
    transition: all 0.5s ease;
}

.guidance-card:hover .guidance-card-icon {
    background: #00BFFF;
    color: #000000;
    transform: rotateY(360deg);
}

.guidance-card h3 {
    font-size: 24px;
    margin-bottom: 20px;
    color: white;
    text-align: center;
}

.guidance-card-price {
    font-size: 28px;
    font-weight: 700;
    color: #00BFFF;
    margin: 20px 0;
    text-align: center;
    font-family: 'Montserrat', sans-serif;
}

.guidance-card-price span {
    font-size: 16px;
    color: #AAAAAA;
    font-weight: normal;
}

.guidance-card-features {
    margin: 30px 0;
}

.guidance-card-features ul {
    padding-left: 0;
}

.guidance-card-features li {
    list-style: none;
    margin-bottom: 12px;
    padding-left: 30px;
    position: relative;
    color: #CCCCCC;
}

.guidance-card-features li i {
    color: #00BFFF;
    position: absolute;
    left: 0;
    top: 5px;
}

.btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 12px 30px;
    border-radius: 50px;
    font-weight: 600;
    text-decoration: none;
    transition: all 0.3s;
    width: 100%;
    text-align: center;
}

.btn-primary {
    background-color: #00BFFF;
    color: #000000;
}

.btn-primary:hover {
    background-color: #0080FF;
    transform: translateY(-3px);
    box-shadow: 0 10px 20px rgba(0, 191, 255, 0.2);
}

.btn-secondary {
    border: 2px solid #00BFFF;
    color: #00BFFF;
    background: transparent;
}

.btn-secondary:hover {
    background-color: rgba(0, 191, 255, 0.1);
    transform: translateY(-3px);
}

/* Responsive Styles */
@media (max-width: 1200px) {
    .guidance-card {
        width: 300px;
    }
}

@media (max-width: 992px) {
    .guidance-cards {
        flex-direction: column;
        align-items: center;
    }
    
    .guidance-card {
        width: 100%;
        max-width: 500px;
    }
    
    .guidance-card.featured {
        transform: none;
    }
    
    .guidance-card.featured:hover {
        transform: translateY(-5px) scale(1.01);
    }
}
</style>

    <!-- Contact Section -->
    <section id="contact" class="section contact">
        <div class="container">
            <h2 class="section-title">Get In <span>Touch</span></h2>
            <div class="contact-container">
                <div class="contact-info">
                    <h2>Let's Connect</h2>
                    <p>Want to say hello? I'd love to hear from you — whether it's about GATE prep, education, or just to connect.</p>
                    
                    <div class="contact-details">
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div class="contact-content">
                                <h3>Email</h3>
                                <a href="mailto:samarjeet.xyz@gmail.com">samarjeet.xyz@gmail.com</a>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-globe"></i>
                            </div>
                            <div class="contact-content">
                                <h3>Website</h3>
                                <a href="https://www.testurself.in">www.testurself.in</a>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div class="contact-content">
                                <h3>Location</h3>
                                <p>India</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="contact-social">
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-github"></i></a>
                    </div>
                </div>
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Your Name</label>
                            <input type="text" id="name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email Address</label>
                            <input type="email" id="email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="subject">Subject</label>
                            <input type="text" id="subject" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" class="form-control" required></textarea>
                        </div>
                        <button type="submit" class="submit-btn">
                            <i class="fas fa-paper-plane"></i> Send Message
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-about">
                    <a href="#" class="footer-logo">Samarjeet<span>.</span></a>
                    <p>Materials Engineer | GATE AIR-7 | Founder of TestUrSelf | BOD at Mission Kartavya Foundation</p>
                    <p>Turning struggles into strategies — one student at a time.</p>
                </div>
                <div class="footer-links">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#about">About Me</a></li>
                        <li><a href="#testurself">TestUrSelf</a></li>
                        <li><a href="#journey">My Journey</a></li>
                        <li><a href="#guidance">Guidance Program</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h3>Resources</h3>
                    <ul>
                        <li><a href="#">GATE Preparation</a></li>
                        <li><a href="#">Study Materials</a></li>
                        <li><a href="#">My Notes</a></li>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">FAQs</a></li>
                    </ul>
                </div>
                <div class="footer-social">
                    <h3>Connect With Me</h3>
                    <div class="footer-social-links">
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-github"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <p>© 2023 Samarjeet. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- Back to Top Button -->
    <div class="back-to-top">
        <i class="fas fa-arrow-up"></i>
    </div>

    <script>
        // Mobile Menu Toggle
        const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
        const navLinks = document.querySelector('.nav-links');
        
        mobileMenuBtn.addEventListener('click', () => {
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
        });
        
        // Header Scroll Effect
        const header = document.getElementById('header');
        
        window.addEventListener('scroll', () => {
            if (window.scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
        
        // Back to Top Button
        const backToTopBtn = document.querySelector('.back-to-top');
        
        window.addEventListener('scroll', () => {
            if (window.scrollY > 300) {
                backToTopBtn.classList.add('active');
            } else {
                backToTopBtn.classList.remove('active');
            }
        });
        
        backToTopBtn.addEventListener('click', () => {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
        
        // Typing Animation
        const typingText = document.querySelector('.typing-text');
        const texts = ["Turning struggles into strategies", "Helping students succeed", "GATE AIR-7, Mentor", "Founder of TestUrSelf"];
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        
        function type() {
            const currentText = texts[textIndex];
            
            if (isDeleting) {
                typingText.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typingText.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
            }
            
            if (!isDeleting && charIndex === currentText.length) {
                isDeleting = true;
                setTimeout(type, 1500);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex = (textIndex + 1) % texts.length;
                setTimeout(type, 500);
            } else {
                setTimeout(type, isDeleting ? 50 : 100);
            }
        }
        
        setTimeout(type, 1500);
        
        // Animate Timeline Items on Scroll
        const timelineItems = document.querySelectorAll('.timeline-item');
        
        function checkTimelineItems() {
            timelineItems.forEach(item => {
                const itemTop = item.getBoundingClientRect().top;
                const windowHeight = window.innerHeight;
                
                if (itemTop < windowHeight * 0.8) {
                    item.classList.add('visible');
                }
            });
        }
        
        window.addEventListener('scroll', checkTimelineItems);
        window.addEventListener('load', checkTimelineItems);
        
        // Smooth Scrolling for Anchor Links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    if (navLinks.style.display === 'flex') {
                        navLinks.style.display = 'none';
                    }
                }
            });
        });
        
        // Responsive adjustments
        function handleResize() {
            if (window.innerWidth > 992) {
                navLinks.style.display = 'flex';
            } else {
                navLinks.style.display = 'none';
            }
        }
        
        window.addEventListener('resize', handleResize);
        handleResize();
    </script>
</body>
</html>
