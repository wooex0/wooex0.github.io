<html lang="en-US">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BINGHATTI PROPERTIES | Official Portfolio</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">

    <style>
        /* ==========================================================================
           GLOBAL VARIABLES & RESET
           ========================================================================== */
        :root {
            --color-bg-dark: #111111;
            --color-bg-light: #ffffff;
            --color-text-main: #000000;
            --color-text-muted: #666666;
            --color-btn-gray: #9ca3af; 
            --color-btn-submit: #0f172a; 
            --color-whatsapp: #22c55e;
            --font-primary: 'Montserrat', sans-serif;
            --transition-speed: 0.3s ease-in-out;
            --container-max-width: 1300px;
        }

        *, *::before, *::after {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: var(--font-primary);
            background-color: var(--color-bg-light);
            color: var(--color-text-main);
            line-height: 1.5;
            -webkit-font-smoothing: antialiased;
        }

        /* ==========================================================================
           DARK HEADER NAVIGATION
           ========================================================================== */
        .site-header {
            background-color: var(--color-bg-dark);
            width: 100%;
            height: 80px;
            display: flex;
            align-items: center;
            position: fixed;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .header-container {
            width: 100%;
            max-width: var(--container-max-width);
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 40px;
        }

        .brand-logo {
            color: #ffffff;
            font-size: 20px;
            font-weight: 900;
            letter-spacing: 2px;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .brand-logo::before {
            content: '';
            display: inline-block;
            width: 30px;
            height: 20px;
            border: 2px solid #fff;
            transform: skewX(-20deg);
        }

        .main-nav ul {
            list-style: none;
            display: flex;
            gap: 25px;
        }

        .main-nav ul li a {
            color: #ffffff;
            text-decoration: none;
            font-size: 12px;
            font-weight: 600;
            text-transform: capitalize;
            transition: color var(--transition-speed);
        }

        .main-nav ul li a:hover {
            color: #cccccc;
        }

        /* ==========================================================================
           HERO SECTION
           ========================================================================== */
        .hero-section {
            margin-top: 80px;
            height: 60vh;
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.4)), url('https://images.unsplash.com/photo-1582407947304-fd86f028f716?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat;
            display: flex;
            align-items: center;
            padding-left: 10%;
        }

        .hero-section h1 {
            color: #ffffff;
            font-size: clamp(3rem, 6vw, 4.5rem);
            font-weight: 900;
            letter-spacing: 2px;
            text-transform: uppercase;
            text-shadow: 0 4px 10px rgba(0,0,0,0.5);
        }

        /* ==========================================================================
           MAIN CONTENT GRID LAYOUT
           ========================================================================== */
        .portfolio-wrapper {
            max-width: var(--container-max-width);
            margin: 0 auto;
            padding: 80px 40px;
            display: flex;
            flex-direction: column;
            align-items: flex-end;
        }

        .section-title {
            width: 100%;
            text-align: center;
            font-size: 18px;
            font-weight: 900;
            text-transform: uppercase;
            margin-bottom: 40px;
            letter-spacing: 1px;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 30px 20px;
            width: 100%;
        }

        .project-card {
            background-color: var(--color-bg-light);
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .project-image {
            width: 100%;
            aspect-ratio: 4/3;
            overflow: hidden;
            margin-bottom: 15px;
            background-color: #f3f4f6; /* Clean light gray fallback */
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .project-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
            transition: transform 0.5s ease;
        }

        .project-card:hover .project-image img {
            transform: scale(1.05);
        }

        .project-card h3 {
            font-size: 14px;
            font-weight: 800;
            margin-bottom: 10px;
            color: var(--color-text-main);
        }

        .project-details {
            font-size: 10px;
            color: var(--color-text-muted);
            line-height: 1.8;
            margin-bottom: 15px;
        }

        .project-details strong {
            color: var(--color-text-main);
            font-weight: 700;
        }

        .btn-download {
            background-color: var(--color-btn-gray);
            color: #ffffff;
            font-size: 9px;
            font-weight: 700;
            text-transform: uppercase;
            text-decoration: none;
            padding: 8px 20px;
            border-radius: 2px;
            transition: background-color var(--transition-speed);
        }

        .btn-download:hover {
            background-color: #6b7280;
        }

        /* ==========================================================================
           CONTACT US SECTION 
           ========================================================================== */
        .contact-section {
            background-color: #ffffff;
            padding: 80px 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .contact-title {
            font-size: 22px;
            font-weight: 800;
            color: var(--color-btn-submit);
            margin-bottom: 30px;
        }

        .contact-form {
            width: 100%;
            max-width: 600px;
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }

        .form-input {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #d1d5db;
            border-radius: 3px;
            font-family: var(--font-primary);
            font-size: 12px;
            color: #333;
            outline: none;
            transition: border-color 0.3s;
        }

        .form-input:focus {
            border-color: var(--color-btn-submit);
        }

        textarea.form-input {
            resize: vertical;
            min-height: 100px;
        }

        .recaptcha-box {
            border: 1px solid #d1d5db;
            background: #f9fafb;
            padding: 15px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            width: 250px;
            border-radius: 3px;
            margin-top: 10px;
        }

        .recaptcha-left {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 12px;
            color: #555;
        }

        .recaptcha-checkbox {
            width: 24px;
            height: 24px;
            background: #fff;
            border: 2px solid #c1c1c1;
            border-radius: 2px;
        }

        .recaptcha-logo {
            font-size: 10px;
            text-align: center;
            color: #999;
        }

        .btn-submit {
            background-color: var(--color-btn-submit);
            color: #ffffff;
            border: none;
            padding: 15px;
            font-size: 14px;
            font-weight: 700;
            border-radius: 3px;
            cursor: pointer;
            margin-top: 10px;
            transition: background-color 0.3s;
        }

        .btn-submit:hover {
            background-color: #1e293b;
        }

        /* ==========================================================================
           WHATSAPP BOX
           ========================================================================== */
        .whatsapp-box {
            margin-top: 50px;
            border: 1px solid #e5e7eb;
            border-radius: 10px;
            padding: 30px;
            text-align: center;
            width: 100%;
            max-width: 500px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.02);
        }

        .whatsapp-box p {
            font-size: 13px;
            font-weight: 600;
            color: #333;
            margin-bottom: 20px;
        }

        .btn-whatsapp {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            background-color: var(--color-whatsapp);
            color: #ffffff;
            text-decoration: none;
            font-weight: 700;
            font-size: 14px;
            padding: 12px 30px;
            border-radius: 5px;
            transition: transform 0.3s;
        }

        .btn-whatsapp:hover {
            transform: translateY(-2px);
        }

        /* ==========================================================================
           FOOTER
           ========================================================================== */
        .site-footer {
            background-color: #000000;
            color: #9ca3af;
            text-align: center;
            padding: 20px;
            font-size: 9px;
            letter-spacing: 0.5px;
        }

        /* ==========================================================================
           RESPONSIVE DESIGN
           ========================================================================== */
        @media (max-width: 1024px) {
            .project-grid {
                grid-template-columns: repeat(3, 1fr);
            }
        }

        @media (max-width: 768px) {
            .project-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            .form-row {
                grid-template-columns: 1fr;
            }
            .main-nav ul {
                gap: 15px;
            }
            .hero-section h1 {
                font-size: 2.5rem;
            }
        }

        @media (max-width: 480px) {
            .project-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <header class="site-header">
        <div class="header-container">
            <a href="#" class="brand-logo">BINGHATTI</a>
            <nav class="main-nav">
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#contact">Contact Us</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero-section">
        <h1>BINGHATTI PROPERTIES</h1>
    </section>

    <main class="portfolio-wrapper">
        <h2 class="section-title">BINGHATTI PROPERTIES FOR SALE</h2>
        
        <div class="project-grid">
            
            <article class="project-card">
                <div class="project-image">
                    <img src="https://binghattiproperties.ae/wp-content/uploads/2025/05/Hills-300x235-1.jpeg" alt="Bugatti Residences">
                </div>
                <h3>Bugatti Residences</h3>
                <div class="project-details">
                    <strong>Types:</strong> 2-4 BR Mansions<br>
                    <strong>Prices:</strong> from AED 19,000,000<br>
                    <strong>Location:</strong> Business Bay
                </div>
                <a href="#contact" class="btn-download">Download Brochure</a>
            </article>

            <article class="project-card">
                <div class="project-image">
                    <img src="https://images.unsplash.com/photo-1618221195710-dd6b41faaea6?auto=format&fit=crop&w=800&q=80" alt="Mercedes-Benz Places">
                </div>
                <h3>Mercedes-Benz Places</h3>
                <div class="project-details">
                    <strong>Types:</strong> 2-5 BR Penthouses<br>
                    <strong>Prices:</strong> from AED 8,800,000<br>
                    <strong>Location:</strong> Downtown Dubai
                </div>
                <a href="#contact" class="btn-download">Download Brochure</a>
            </article>

            <article class="project-card">
                <div class="project-image">
                    <img src="https://images.unsplash.com/photo-1512453979798-5ea266f8880c?auto=format&fit=crop&w=800&q=80" alt="Jacob & Co">
                </div>
                <h3>Burj Binghatti</h3>
                <div class="project-details">
                    <strong>Types:</strong> Hyper-Tower Villas<br>
                    <strong>Prices:</strong> from AED 8,200,000<br>
                    <strong>Location:</strong> Business Bay
                </div>
                <a href="#contact" class="btn-download">Download Brochure</a>
            </article>

            <article class="project-card">
                <div class="project-image">
                    <img src="https://images.unsplash.com/photo-1545324418-cc1a3fa10c00?auto=format&fit=crop&w=800&q=80" alt="Binghatti Skyrise">
                </div>
                <h3>Binghatti Skyrise</h3>
                <div class="project-details">
                    <strong>Types:</strong> Studio, 1-3 BR<br>
                    <strong>Prices:</strong> from AED 975,000<br>
                    <strong>Location:</strong> Business Bay
                </div>
                <a href="#contact" class="btn-download">Download Brochure</a>
            </article>

            <article class="project-card">
                <div class="project-image">
                    <img src="https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?auto=format&fit=crop&w=800&q=80" alt="Binghatti Hills">
                </div>
                <h3>Binghatti Hills</h3>
                <div class="project-details">
                    <strong>Types:</strong> Studio, 1-2 BR<br>
                    <strong>Prices:</strong> from AED 800,000<br>
                    <strong>Location:</strong> Dubai Science Park
                </div>
                <a href="#contact" class="btn-download">Download Brochure</a>
            </article>

        </div>
    </main>

    <section class="contact-section" id="contact">
        <h2 class="contact-title">Contact Us</h2>
        
        <form class="contact-form" onsubmit="event.preventDefault();">
            <div class="form-row">
                <input type="text" class="form-input" placeholder="First Name *" required>
                <input type="text" class="form-input" placeholder="Last Name *" required>
            </div>
            
            <div class="form-row">
                <input type="email" class="form-input" placeholder="Email *" required>
                <input type="tel" class="form-input" placeholder="Phone *" required>
            </div>

            <select class="form-input" required>
                <option value="" disabled selected>Country of Residence *</option>
                <option value="UAE">United Arab Emirates</option>
                <option value="KSA">Saudi Arabia</option>
                <option value="KSA">Egypt</option>
                <option value="OTHER">Other</option>
            </select>

            <textarea class="form-input" placeholder="Message" rows="4"></textarea>

            
            <button type="submit" class="btn-submit">Submit</button>
        </form>

        <div class="whatsapp-box">
            <p>For further details, feel free to reach out to us via<br>WhatsApp</p>
            <a href="https://wa.me/01069460625" class="btn-whatsapp" target="_blank">
                <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.245 2.248 3.481 5.236 3.48 8.414-.003 6.557-5.338 11.892-11.893 11.892-1.99-.001-3.951-.5-5.688-1.448l-6.305 1.654zm6.597-3.807c1.676.995 3.276 1.591 5.392 1.592 5.448 0 9.886-4.434 9.889-9.885.002-5.462-4.415-9.89-9.881-9.892-5.452 0-9.887 4.434-9.889 9.884-.001 2.225.651 3.891 1.746 5.634l-.999 3.648 3.742-.981zm11.387-5.464c-.074-.124-.272-.198-.57-.347-.297-.149-1.758-.868-2.031-.967-.272-.099-.47-.149-.669.149-.198.297-.768.967-.941 1.165-.173.198-.347.223-.644.074-.297-.149-1.255-.462-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.297-.347.446-.521.151-.172.2-.296.3-.495.099-.198.05-.372-.025-.521-.075-.148-.669-1.611-.916-2.206-.242-.579-.487-.501-.669-.51l-.57-.01c-.198 0-.52.074-.792.372s-1.04 1.016-1.04 2.479 1.065 2.876 1.213 3.074c.149.198 2.095 3.2 5.076 4.487.709.306 1.263.489 1.694.626.712.226 1.36.194 1.872.118.571-.085 1.758-.719 2.006-1.413.248-.695.248-1.29.173-1.414z"/>
                </svg>
                +201069460625
            </a>
        </div>
    </section>

    <footer class="site-footer">
        <p>Disclaimer: This website is owned and managed by an authorized partner. It is not managed by nor directly affiliated with the primary developer.</p>
    </footer>

</body>
</html>
