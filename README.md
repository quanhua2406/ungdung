<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TechCorp - Innovative Solutions</title>
    <link rel="stylesheet" href="css/ungdung.css">
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="header-content">
            <div class="logo">TechCorp</div>
            <nav>
                <ul class="nav">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
            <button class="mobile-menu">☰</button>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Innovative Technology Solutions</h1>
            <p>Transform your business with cutting-edge technology and expert consulting services</p>
            <a href="#contact" class="cta-button">Get Started Today</a>
        </div>
    </section>

    <!-- Main Content -->
    <section class="main-content">
        <div class="container">
            <h2 class="section-title fade-in">Our Services</h2>
            <div class="features">
                <div class="feature-card fade-in">
                    <div class="feature-icon">⚡</div>
                    <h3>Fast Performance</h3>
                    <p>Lightning-fast solutions optimized for maximum performance and user experience across all platforms and devices.</p>
                </div>
                <div class="feature-card fade-in">
                    <div class="feature-icon">🔒</div>
                    <h3>Secure & Reliable</h3>
                    <p>Enterprise-grade security measures and reliable infrastructure to protect your data and ensure 99.9% uptime.</p>
                </div>
                <div class="feature-card fade-in">
                    <div class="feature-icon">🚀</div>
                    <h3>Scalable Solutions</h3>
                    <p>Future-proof technology that grows with your business, from startup to enterprise-level requirements.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <div class="container">
            <div class="stats-grid">
                <div class="stat-item fade-in">
                    <h3>500+</h3>
                    <p>Happy Clients</p>
                </div>
                <div class="stat-item fade-in">
                    <h3>1000+</h3>
                    <p>Projects Completed</p>
                </div>
                <div class="stat-item fade-in">
                    <h3>99.9%</h3>
                    <p>Uptime Guarantee</p>
                </div>
                <div class="stat-item fade-in">
                    <h3>24/7</h3>
                    <p>Support Available</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer" id="contact">
        <div class="footer-content">
            <div class="footer-links">
                <a href="#privacy">Privacy Policy</a>
                <a href="#terms">Terms of Service</a>
                <a href="#support">Support</a>
                <a href="#careers">Careers</a>
            </div>
            <div class="copyright">
                <p>&copy; 2025 TechCorp. All rights reserved. | Email: info@techcorp.com | Phone: +84 123 456 789</p>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Fade in animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });

        // Mobile menu toggle (basic functionality)
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            const nav = document.querySelector('.nav');
            nav.style.display = nav.style.display === 'flex' ? 'none' : 'flex';
        });
    </script>
</body>
</html>
