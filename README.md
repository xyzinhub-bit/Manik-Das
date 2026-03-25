# Manik-Das
To be continued 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Forge & Hammer Blacksmith Shop - Custom Hand-Forged Metalwork</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #2c1810 0%, #4a2c1a 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            background: rgba(0,0,0,0.9);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.5);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 2rem;
            font-weight: bold;
            color: #d4a574;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: #fff;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #d4a574;
        }

        .hero {
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect fill="%232c1810" width="1200" height="600"/><path fill="%234a2c1a" d="M0 400 Q300 200 600 350 Q900 250 1200 400 L1200 600 L0 600 Z"/><circle fill="%23d4a574" cx="200" cy="250" r="80"/><circle fill="%23d4a574" cx="1000" cy="280" r="60"/><rect fill="%23663300" x="500" y="320" width="200" height="150" rx="10"/></svg>') center/cover;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0,0,0,0.6);
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            text-shadow: 3px 3px 6px rgba(0,0,0,0.8);
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { text-shadow: 3px 3px 6px rgba(0,0,0,0.8), 0 0 20px #d4a574; }
            to { text-shadow: 3px 3px 6px rgba(0,0,0,0.8), 0 0 30px #d4a574; }
        }

        .hero p {
            font-size: 1.5rem;
            margin-bottom: 2rem;
        }

        .cta-button {
            display: inline-block;
            background: #d4a574;
            color: #2c1810;
            padding: 1rem 2.5rem;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.2rem;
            border-radius: 50px;
            transition: all 0.3s;
            box-shadow: 0 5px 15px rgba(212, 165, 116, 0.4);
        }

        .cta-button:hover {
            background: #b88c5a;
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(212, 165, 116, 0.6);
        }

        section {
            padding: 5rem 0;
        }

        .section-title {
            text-align: center;
            font-size: 3rem;
            color: #d4a574;
            margin-bottom: 3rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: #d4a574;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .card {
            background: rgba(255,255,255,0.95);
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.4);
        }

        .card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 10px;
            margin-bottom: 1rem;
        }

        .about {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            color: white;
        }

        .contact {
            background: rgba(0,0,0,0.8);
            color: white;
        }

        .contact form {
            max-width: 600px;
            margin: 0 auto;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: bold;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            border: 2px solid #d4a574;
            border-radius: 10px;
            background: rgba(255,255,255,0.9);
            font-family: inherit;
            font-size: 1rem;
        }

        footer {
            background: #1a0f0a;
            color: #ccc;
            text-align: center;
            padding: 2rem 0;
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <a href="#home" class="logo">🔨 Forge & Hammer</a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#gallery">Gallery</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Hand-Forged Masterpieces</h1>
            <p>Traditional blacksmithing with modern precision. Custom knives, tools, and art from our forge to your hands.</p>
            <a href="#contact" class="cta-button">Get Your Custom Order</a>
        </div>
    </section>

    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title">The Blacksmith's Craft</h2>
            <div class="grid">
                <div class="card">
                    <div style="background: linear-gradient(45deg, #d4a574, #b88c5a); height: 200px; border-radius: 10px; display: flex; align-items: center; justify-content: center; margin-bottom: 1rem; font-size: 4rem;">🔨</div>
                    <h3>Traditional Methods</h3>
                    <p>Every piece is hand-forged using centuries-old techniques passed down through generations of master blacksmiths.</p>
                </div>
                <div class="card">
                    <div style="background: linear-gradient(45deg, #d4a574, #b88c5a); height: 200px; border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 4rem;">⚒️</div>
                    <h3>Custom Work</h3>
                    <p>From kitchen knives to architectural ironwork, we create exactly what you envision with unmatched quality.</p>
                </div>
                <div class="card">
                    <div style="background: linear-gradient(45deg, #d4a574, #b88c5a); height: 200px; border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 4rem;">🔥</div>
                    <h3>Premium Materials</h3>
                    <p>Only the finest high-carbon steels, Damascus patterns, and exotic metals go into our creations.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="services">
        <div class="container">
            <h2 class="section-title">Our Services</h2>
            <div class="grid">
                <div class="card">
                    <h3>Custom Knives</h3>
                    <p>Hand-forged chef's knives, hunting knives, and EDC blades with custom handles and engraving.</p>
                </div>
                <div class="card">
                    <h3>Tools & Hardware</h3>
                    <p>Axes, hammers, chisels, hinges, and latches built to last generations.</p>
                </div>
                <div class="card">
                    <h3>Art & Decor</h3>
                    <p>Wall art, sculptures, fireplace tools, and architectural elements that become family heirlooms.</p>
                </div>
                <div class="card">
                    <h3>Restoration</h3>
                    <p>Bring your family heirlooms back to life with expert repair and refinishing services.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="gallery">
        <div class="container">
            <h2 class="section-title">Gallery</h2>
            <div class="grid">
                <div class="card">
                    <div style="background: linear-gradient(45deg, #666, #333); height: 200px; border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 4rem; color: #d4a574;">🔪</div>
                    <h3>Damascus Chef Knife</h3>
                </div>
                <div class="card">
                    <div style="background: linear-gradient(45deg, #444, #222); height: 200px; border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 4rem; color: #d4a574;">🪓</div>
                    <h3>Hand Axe</h3>
                </div>
                <div class="card">
                    <div style="background: linear-gradient(45deg, #555, #111); height: 200px; border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 4rem; color: #d4a574;">🛠️</div>
                    <h3>Custom Hammer</h3>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title">Let's Forge Something Great</h2>
            <form>
                <div class="form-group">
                    <label for="name">Name</label>
                    <input type="text" id="name" name="name" required>
                </div>
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="project">Project Description</label>
                    <textarea id="project" name="project" rows="5" placeholder="Tell us about your custom project..." required></textarea>
                </div>
                <button type="submit" class="cta-button" style="width: 100%; font-size: 1.3rem;">Send Inquiry</button>
            </form>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2024 Forge & Hammer Blacksmith Shop. Crafted with fire and iron. All rights reserved.</p>
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

        // Form submission (demo)
        document.querySelector('form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your inquiry! We\'ll contact you within 24 hours to discuss your project.');
        });

        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(0,0,0,0.95)';
            } else {
                header.style.background = 'rgba(0,0,0,0.9)';
            }
        });
    </script>
</body>
</html>
