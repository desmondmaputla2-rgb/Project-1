# Project-1
Website for tutoring 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EduMentor - Professional Tutoring Services</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Global Styles */
        :root {
            --primary: #4a6fa5;
            --secondary: #166088;
            --accent: #ff6b6b;
            --light: #f8f9fa;
            --dark: #343a40;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .btn {
            display: inline-block;
            background: var(--primary);
            color: white;
            padding: 12px 24px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background: var(--secondary);
            transform: translateY(-2px);
        }
        
        .btn-accent {
            background: var(--accent);
        }
        
        .btn-accent:hover {
            background: #ff5252;
        }
        
        section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 15px;
        }
        
        .section-title p {
            font-size: 1.1rem;
            color: #666;
            max-width: 700px;
            margin: 0 auto;
        }
        
        /* Header Styles */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
        }
        
        .logo span {
            color: var(--accent);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 30px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s ease;
        }
        
        nav ul li a:hover {
            color: var(--primary);
        }
        
        .mobile-menu-btn {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(74, 111, 165, 0.8), rgba(22, 96, 136, 0.8)), url('https://images.unsplash.com/photo-1501504905252-473c47e087f8?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            align-items: center;
            color: white;
            text-align: center;
            margin-top: 80px;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
        }
        
        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }
        
        /* Services Section */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
        }
        
        .service-icon {
            background: var(--primary);
            color: white;
            font-size: 2.5rem;
            padding: 30px;
            text-align: center;
        }
        
        .service-content {
            padding: 25px;
        }
        
        .service-content h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--secondary);
        }
        
        /* Tutors Section */
        .tutors-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }
        
        .tutor-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        
        .tutor-img {
            height: 250px;
            background-size: cover;
            background-position: center;
        }
        
        .tutor-info {
            padding: 20px;
        }
        
        .tutor-info h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .tutor-subject {
            color: var(--accent);
            font-weight: 600;
            margin-bottom: 15px;
        }
        
        /* Testimonials */
        .testimonials {
            background-color: #f1f7fd;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .testimonial-card {
            background: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
            position: relative;
        }
        
        .testimonial-text:before {
            content: """;
            font-size: 4rem;
            color: var(--primary);
            opacity: 0.2;
            position: absolute;
            top: -20px;
            left: -10px;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-size: cover;
            background-position: center;
            margin-right: 15px;
        }
        
        .author-info h4 {
            font-size: 1.1rem;
            margin-bottom: 5px;
        }
        
        /* Contact Section */
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }
        
        .contact-item {
            display: flex;
            align-items: flex-start;
            gap: 15px;
        }
        
        .contact-icon {
            background: var(--primary);
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
        }
        
        .contact-form {
            background: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 60px 0 30px;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-col h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-col h3:after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 50px;
            height: 2px;
            background: var(--accent);
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 12px;
        }
        
        .footer-links a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-links a:hover {
            color: white;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-links a {
            color: white;
            background: rgba(255, 255, 255, 0.1);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* Responsive Styles */
        @media (max-width: 992px) {
            .hero-content h1 {
                font-size: 2.8rem;
            }
        }
        
        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            nav {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background: white;
                transition: all 0.3s ease;
            }
            
            nav.active {
                left: 0;
            }
            
            nav ul {
                flex-direction: column;
                padding: 30px;
            }
            
            nav ul li {
                margin: 15px 0;
            }
            
            .hero-content h1 {
                font-size: 2.3rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }
        
        @media (max-width: 576px) {
            .hero-content h1 {
                font-size: 2rem;
            }
            
            .hero-content p {
                font-size: 1rem;
            }
            
            .btn {
                padding: 10px 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <a href="#" class="logo">Edu<span>Mentor</span></a>
            <div class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#tutors">Our Tutors</a></li>
                    <li><a href="#testimonials">Testimonials</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li><a href="#" class="btn btn-accent">Book a Session</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container hero-content">
            <h1>Unlock Your Academic Potential</h1>
            <p>Personalized one-on-one tutoring to help you succeed in any subject, at any level.</p>
            <a href="#contact" class="btn">Get Started Today</a>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services">
        <div class="container">
            <div class="section-title">
                <h2>Our Services</h2>
                <p>We offer comprehensive tutoring services tailored to each student's unique learning needs.</p>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-calculator"></i>
                    </div>
                    <div class="service-content">
                        <h3>Mathematics</h3>
                        <p>From basic arithmetic to advanced calculus, our math tutors make numbers make sense.</p>
                        <a href="#" class="btn">Learn More</a>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-flask"></i>
                    </div>
                    <div class="service-content">
                        <h3>Science</h3>
                        <p>Biology, chemistry, physics - our experts break down complex scientific concepts.</p>
                        <a href="#" class="btn">Learn More</a>
                    </div>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-language"></i>
                    </div>
                    <div class="service-content">
                        <h3>Languages</h3>
                        <p>Master English, Spanish, French and more with our experienced language tutors.</p>
                        <a href="#" class="btn">Learn More</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Tutors Section -->
    <section id="tutors" style="background-color: #f1f7fd;">
        <div class="container">
            <div class="section-title">
                <h2>Meet Our Tutors</h2>
                <p>Our team of expert educators is passionate about helping students succeed.</p>
            </div>
            <div class="tutors-grid">
                <div class="tutor-card">
                    <div class="tutor-img" style="background-image: url('https://images.unsplash.com/photo-1560250097-0b93528c311a?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80');"></div>
                    <div class="tutor-info">
                        <h3>Michael Johnson</h3>
                        <div class="tutor-subject">Mathematics Specialist</div>
                        <p>10+ years experience teaching algebra, geometry, and calculus to high school students.</p>
                    </div>
                </div>
                <div class="tutor-card">
                    <div class="tutor-img" style="background-image: url('https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80');"></div>
                    <div class="tutor-info">
                        <h3>Sarah Williams</h3>
                        <div class="tutor-subject">Science Expert</div>
                        <p>PhD in Chemistry with a passion for making science accessible and fun for all ages.</p>
                    </div>
                </div>
                <div class="tutor-card">
                    <div class="tutor-img" style="background-image: url('https://images.unsplash.com/photo-1519085360753-af0119f7cbe7?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80');"></div>
                    <div class="tutor-info">
                        <h3>David Chen</h3>
                        <div class="tutor-subject">Language Arts</div>
                        <p>Former English teacher specializing in reading comprehension and writing skills.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section id="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>What Our Students Say</h2>
                <p>Hear from students and parents who have experienced our tutoring services.</p>
