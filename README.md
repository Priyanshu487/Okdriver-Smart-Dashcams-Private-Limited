<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    
    <title>OkDriver - Your Road Safety Companion</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Montserrat:wght@700;800&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #1a73e8;
            --primary-light: #4285f4;
            --secondary: #34a853;
            --accent: #fbbc05;
            --light: #f8f9fa;
            --dark: #202124;
            --gray: #5f6368;
            --transition: all 0.3s ease;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f5f8ff;
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            background: linear-gradient(135deg, #ffffff 0%, #e6f0ff 100%);
            box-shadow: 0 2px 15px rgba(0, 0, 150, 0.08);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo-icon {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-light) 100%);
            width: 50px;
            height: 50px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 12px rgba(26, 115, 232, 0.25);
        }

        .logo-icon i {
            font-size: 24px;
            color: white;
        }

        .logo-text {
            font-family: 'Montserrat', sans-serif;
            font-weight: 800;
            font-size: 28px;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--gray);
            font-weight: 500;
            transition: var(--transition);
            position: relative;
            padding: 5px 0;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: var(--transition);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            padding: 100px 0 70px;
            display: flex;
            align-items: center;
            gap: 50px;
        }

        .hero-content {
            flex: 1;
        }

        .hero h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 3.2rem;
            line-height: 1.2;
            margin-bottom: 20px;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero p {
            font-size: 1.2rem;
            color: var(--gray);
            margin-bottom: 30px;
            max-width: 600px;
        }

        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
        }

        .phone-mockup {
            width: 280px;
            height: 550px;
            background: linear-gradient(135deg, #1a73e8 0%, #34a853 100%);
            border-radius: 40px;
            position: relative;
            box-shadow: 0 20px 40px rgba(26, 115, 232, 0.3);
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .phone-screen {
            width: 92%;
            height: 96%;
            background-color: white;
            border-radius: 32px;
            overflow: hidden;
            position: relative;
        }

        .phone-screen img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* Section Common Styles */
        .section {
            padding: 100px 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.5rem;
            margin-bottom: 15px;
            color: var(--dark);
        }

        .section-subtitle {
            color: var(--gray);
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto;
        }

        /* Features Section */
        .features {
            background-color: white;
            border-radius: 30px;
            padding: 50px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .feature-card {
            background: var(--light);
            border-radius: 20px;
            padding: 30px;
            transition: var(--transition);
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(26, 115, 232, 0.1);
        }

        .feature-icon {
            width: 70px;
            height: 70px;
            border-radius: 18px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 25px;
            font-size: 28px;
        }

        .feature-icon.capture {
            background: linear-gradient(135deg, #4285f4 0%, #1a73e8 100%);
            color: white;
        }

        .feature-icon.sos {
            background: linear-gradient(135deg, #ea4335 0%, #d93025 100%);
            color: white;
        }

        .feature-icon.gps {
            background: linear-gradient(135deg, #34a853 0%, #0f9d58 100%);
            color: white;
        }

        .feature-icon.voice {
            background: linear-gradient(135deg, #fbbc05 0%, #f9ab00 100%);
            color: white;
        }

        .feature-icon.locator {
            background: linear-gradient(135deg, #673ab7 0%, #5e35b1 100%);
            color: white;
        }

        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--dark);
        }

        .feature-card p {
            color: var(--gray);
        }

        /* Safety Experience Section */
        .safety-experience {
            background: linear-gradient(135deg, #e6f0ff 0%, #f0f7ff 100%);
            border-radius: 30px;
            padding: 60px 50px;
        }

        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .benefit-card {
            background: white;
            border-radius: 20px;
            padding: 40px 30px;
            text-align: center;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.03);
        }

        .benefit-number {
            font-family: 'Montserrat', sans-serif;
            font-size: 3rem;
            font-weight: 700;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 15px;
        }

        .benefit-card h3 {
            font-size: 1.6rem;
            margin-bottom: 15px;
            color: var(--dark);
        }

        /* Download Section */
        .download-options {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
        }

        .download-card {
            background: white;
            border-radius: 20px;
            padding: 40px;
            text-align: center;
            width: 280px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
        }

        .download-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(26, 115, 232, 0.15);
        }

        .download-icon {
            font-size: 50px;
            margin-bottom: 20px;
        }

        .download-icon.apple {
            color: #000000;
        }

        .download-icon.android {
            color: #34a853;
        }

        .download-icon.web {
            color: var(--primary);
        }

        .download-card h3 {
            font-size: 1.8rem;
            margin-bottom: 15px;
        }

        .btn {
            display: inline-block;
            padding: 14px 32px;
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-light) 100%);
            color: white;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 1rem;
            box-shadow: 0 5px 15px rgba(26, 115, 232, 0.3);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(26, 115, 232, 0.4);
        }

        /* Languages Section */
        .languages {
            background: white;
            border-radius: 30px;
            padding: 60px;
            text-align: center;
        }

        .language-badges {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 40px;
        }

        .language-badge {
            background: var(--light);
            border-radius: 50px;
            padding: 15px 30px;
            font-weight: 500;
            transition: var(--transition);
        }

        .language-badge:hover {
            background: var(--primary);
            color: white;
            transform: translateY(-5px);
        }

        /* Footer */
        footer {
            background: linear-gradient(135deg, var(--dark) 0%, #000000 100%);
            color: white;
            padding: 80px 0 30px;
            margin-top: 100px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 50px;
        }

        .footer-column h3 {
            font-size: 1.5rem;
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--primary);
            border-radius: 3px;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 15px;
        }

        .footer-links a {
            color: #b0b0b0;
            text-decoration: none;
            transition: var(--transition);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .footer-links a:hover {
            color: white;
            padding-left: 5px;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
            color: #b0b0b0;
        }

        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-icon {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
            color: white;
            font-size: 18px;
            text-decoration: none;
        }

        .social-icon:hover {
            background: var(--primary);
            transform: translateY(-5px);
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #b0b0b0;
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .hero {
                flex-direction: column;
                text-align: center;
            }
            
            .hero p {
                margin-left: auto;
                margin-right: auto;
            }
            
            .hero-image {
                margin-top: 40px;
            }
            
            .section-title {
                font-size: 2.2rem;
            }
        }

        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
                gap: 20px;
            }
            
            .nav-links {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .features, .safety-experience, .languages {
                padding: 40px 20px;
            }
            
            .phone-mockup {
                width: 240px;
                height: 470px;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .section {
                padding: 70px 0;
            }
            
            .download-card {
                width: 100%;
                max-width: 280px;
            }
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="container">
            <nav class="navbar">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-car"></i>
                    </div>
                    <div class="logo-text">OkDriver</div>
                </div>
                <div class="nav-links">
                    <a href="#about">About</a>
                    <a href="#features">Features</a>
                    <a href="#safety">Safety</a>
                    <a href="#download">Download</a>
                    <a href="#languages">Languages</a>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero/About Section -->
    <section id="about">
        <div class="container">
            <div class="hero">
                <div class="hero-content">
                    <h1>Drive Safely with OkDriver</h1>
                    <p>OkDriver is your ultimate road safety companion, designed to prevent accidents, provide emergency assistance, and guide you to your destination safely and efficiently.</p>
                    <a href="https://www.okdrive.in/" class="btn" target="_blank">Visit Our Website</a>
                </div>
                <div class="hero-image">
                    <div class="phone-mockup">
                        <div class="phone-screen">
                            <img src="image1.jpg" alt="OkDriver App">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="section">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Advanced Features</h2>
                <p class="section-subtitle">Discover the powerful features that make OkDriver your essential driving companion</p>
            </div>
            <div class="features">
                <div class="features-grid">
                    <div class="feature-card">
                        <div class="feature-icon capture">
                            <i class="fas fa-video"></i>
                        </div>
                        <h3>Capture Movement</h3>
                        <p>Continuously monitors and records your vehicle's movement to detect unusual patterns and potential risks.</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon sos">
                            <i class="fas fa-bell"></i>
                        </div>
                        <h3>Emergency SOS</h3>
                        <p>Instant one-touch emergency alert system that notifies authorities and your emergency contacts.</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon gps">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <h3>GPS Tracking</h3>
                        <p>Real-time location tracking with optimized routes to help you reach your destination safely and on time.</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon voice">
                            <i class="fas fa-volume-up"></i>
                        </div>
                        <h3>Voice Guided Safety Tips</h3>
                        <p>Context-aware safety instructions delivered through voice prompts to keep your eyes on the road.</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon locator">
                            <i class="fas fa-wrench"></i>
                        </div>
                        <h3>Nearby Service Locator</h3>
                        <p>Find the nearest fuel stations, mechanics, hospitals, and other essential services with a single tap.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Safety Experience Section -->
    <section id="safety" class="section">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Experience the Future of Safety</h2>
                <p class="section-subtitle">How OkDriver revolutionizes your driving experience and safety on the road</p>
            </div>
            <div class="safety-experience">
                <div class="benefits-grid">
                    <div class="benefit-card">
                        <div class="benefit-number">01</div>
                        <h3>Accident Prevention</h3>
                        <p>Advanced algorithms detect potential hazards and alert you before accidents happen.</p>
                    </div>
                    <div class="benefit-card">
                        <div class="benefit-number">02</div>
                        <h3>Time Optimization</h3>
                        <p>Smart routing technology helps you avoid traffic and reach your destination faster.</p>
                    </div>
                    <div class="benefit-card">
                        <div class="benefit-number">03</div>
                        <h3>Community Alerts</h3>
                        <p>Real-time updates from other drivers about road conditions, hazards, and police checks.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Download Section -->
    <section id="download" class="section">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Download OkDriver Now</h2>
                <p class="section-subtitle">Available on all platforms to keep you safe wherever you drive</p>
            </div>
            <div class="download-options">
                <div class="download-card">
                    <div class="download-icon android">
                        <i class="fab fa-google-play"></i>
                    </div>
                    <h3>Play Store</h3>
                    <p>Download for Android devices</p>
                    <a href="#" class="btn">Get It Now</a>
                </div>
                <div class="download-card">
                    <div class="download-icon apple">
                        <i class="fab fa-apple"></i>
                    </div>
                    <h3>Apple Store</h3>
                    <p>Download for iOS devices</p>
                    <a href="#" class="btn">Download</a>
                </div>
                <div class="download-card">
                    <div class="download-icon web">
                        <i class="fas fa-globe"></i>
                    </div>
                    <h3>OkDrive.com</h3>
                    <p>Access via web browser</p>
                    <a href="https://www.okdrive.in/" class="btn">Visit Website</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Languages Section -->
    <section id="languages" class="section">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Available in Multiple Languages</h2>
                <p class="section-subtitle">OkDriver speaks your language for a personalized safety experience</p>
            </div>
            <div class="languages">
                <div class="language-badges">
                    <div class="language-badge">English</div>
                    <div class="language-badge">Hindi</div>
                    <div class="language-badge">Marathi</div>
                    <div class="language-badge">Bengali</div>
                    <div class="language-badge">Tamil</div>
                    <div class="language-badge">Telugu</div>
                    <div class="language-badge">Kannada</div>
                    <div class="language-badge">Gujarati</div>
                    <div class="language-badge">Punjabi</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>OkDriver</h3>
                    <p>Your trusted companion for road safety and efficient driving experiences.</p>
                    <div class="social-icons">
                        <a href="#" class="social-icon"><i class="fab fa-facebook-f"></i></a>
                        <a href="#" class="social-icon"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="social-icon"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="social-icon"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#about"><i class="fas fa-chevron-right"></i> About Us</a></li>
                        <li><a href="#features"><i class="fas fa-chevron-right"></i> Features</a></li>
                        <li><a href="#safety"><i class="fas fa-chevron-right"></i> Safety Benefits</a></li>
                        <li><a href="#download"><i class="fas fa-chevron-right"></i> Download</a></li>
                        <li><a href="#languages"><i class="fas fa-chevron-right"></i> Languages</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Information</h3>
                    <ul class="footer-links">
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Privacy Policy</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Terms of Service</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> FAQ</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Support Center</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contact Us</h3>
                    <div class="contact-info">
                        <div class="contact-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <span>123 Safety Lane, Roadville, IN 400001</span>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-envelope"></i>
                            <span>support@okdrive.in</span>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-phone"></i>
                            <span>+91 98765 43210</span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 OkDriver. All rights reserved. Designed for safer roads.</p>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add scroll animation to sections
        const observerOptions = {
            root: null,
            rootMargin: '0px',
            threshold: 0.1
        };

        const observer = new IntersectionObserver((entries, observer) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animated');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.section, .hero').forEach(section => {
            observer.observe(section);
        });
    </script>
</body>
</html>
