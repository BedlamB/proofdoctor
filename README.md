<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Proofdoctor - Professional Proofreading Services UK</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Georgia, 'Times New Roman', serif;
            background-color: #e8e0d5;
            color: #2c2c2c;
            line-height: 1.6;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            background-color: #e8e0d5;
            padding: 40px 0 30px;
            text-align: center;
            border-bottom: 1px solid #c4b5a0;
        }

        .logo-container {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 20px;
            margin-bottom: 10px;
        }

        .logo {
            width: 60px;
            height: 60px;
            border: 3px solid #dc2626;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
        }

        .checkmark {
            color: #dc2626;
            font-size: 36px;
            font-weight: bold;
            transform: rotate(-10deg);
        }

        h1 {
            font-size: 3.5em;
            font-weight: normal;
            color: #2c2c2c;
            letter-spacing: -2px;
        }

        .tagline {
            font-style: italic;
            font-size: 1.1em;
            color: #4a4a4a;
            margin-top: 5px;
        }

        /* Navigation */
        nav {
            background-color: #e8e0d5;
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .nav-links {
            display: flex;
            gap: 0;
            justify-content: flex-start;
            max-width: 600px;
        }

        .nav-link {
            padding: 10px 25px;
            text-decoration: none;
            color: #2c2c2c;
            font-size: 1.05em;
            transition: all 0.3s ease;
            background-color: #f5f2ec;
            border: 1px solid #c4b5a0;
            cursor: pointer;
        }

        .nav-link:first-child {
            border-radius: 4px 0 0 4px;
        }

        .nav-link:last-child {
            border-radius: 0 4px 4px 0;
        }

        .nav-link.active {
            background-color: #4a90a4;
            color: white;
        }

        .nav-link:hover:not(.active) {
            background-color: #ddd5c7;
        }

        /* Main Content */
        main {
            padding: 60px 0;
            min-height: calc(100vh - 300px);
        }

        .content-box {
            background-color: #f5f2ec;
            border: 1px solid #c4b5a0;
            border-radius: 4px;
            padding: 60px;
            margin: 0 auto;
            max-width: 900px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
        }

        .page-title {
            font-size: 3em;
            text-align: center;
            margin-bottom: 40px;
            font-weight: normal;
            letter-spacing: -1px;
        }

        .content-text {
            font-size: 1.15em;
            text-align: center;
            margin-bottom: 30px;
            color: #4a4a4a;
            line-height: 1.8;
        }

        /* Services Grid */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .service-card {
            background: white;
            padding: 30px;
            border-radius: 4px;
            border: 1px solid #c4b5a0;
            text-align: center;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .service-card h3 {
            color: #4a90a4;
            margin-bottom: 15px;
            font-size: 1.4em;
        }

        .service-card p {
            color: #666;
            line-height: 1.6;
        }

        /* Contact Form */
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #4a4a4a;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #c4b5a0;
            border-radius: 4px;
            font-size: 1em;
            font-family: inherit;
            background-color: white;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #4a90a4;
        }

        .form-group textarea {
            min-height: 150px;
            resize: vertical;
        }

        .submit-btn {
            background-color: #4a90a4;
            color: white;
            padding: 14px 40px;
            border: none;
            border-radius: 4px;
            font-size: 1.1em;
            cursor: pointer;
            transition: background-color 0.3s ease;
            display: block;
            margin: 0 auto;
        }

        .submit-btn:hover {
            background-color: #3a7a94;
        }

        /* Features List */
        .features-list {
            list-style: none;
            margin: 30px 0;
        }

        .features-list li {
            padding: 15px 0;
            border-bottom: 1px solid #e0d5c5;
            display: flex;
            align-items: center;
        }

        .features-list li:last-child {
            border-bottom: none;
        }

        .features-list li:before {
            content: "✓";
            color: #dc2626;
            font-weight: bold;
            font-size: 1.2em;
            margin-right: 15px;
        }

        /* Footer */
        footer {
            background-color: #4a4a4a;
            color: #e8e0d5;
            text-align: center;
            padding: 30px 0;
            margin-top: 60px;
        }

        .hidden {
            display: none;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5em;
            }

            .page-title {
                font-size: 2em;
            }

            .content-box {
                padding: 40px 30px;
            }

            .nav-links {
                flex-wrap: wrap;
                gap: 10px;
            }

            .nav-link {
                border-radius: 4px !important;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="logo-container">
                <div class="logo">
                    <span class="checkmark">✓</span>
                </div>
            </div>
            <h1>Proofdoctor</h1>
            <p class="tagline">Because accuracy is of the essence...</p>
        </div>
    </header>

    <!-- Navigation -->
    <nav>
        <div class="container">
            <div class="nav-links">
                <a class="nav-link active" onclick="showPage('home')">Home</a>
                <a class="nav-link" onclick="showPage('overview')">Overview</a>
                <a class="nav-link" onclick="showPage('services')">Services</a>
                <a class="nav-link" onclick="showPage('contact')">Contact</a>
            </div>
        </div>
    </nav>

    <!-- Main Content -->
    <main>
        <div class="container">
            <!-- Home Page -->
            <div id="home" class="page-content">
                <div class="content-box">
                    <h2 class="page-title">Home</h2>
                    <p class="content-text">
                        Proofdoctor is a proofreading and copyediting service for all your needs to ensure professional documents and publications.
                    </p>
                    <p class="content-text">
                        Take a look at our overview for more information.
                    </p>
                    
                    <div style="margin-top: 50px; padding: 30px; background: white; border-radius: 4px;">
                        <h3 style="color: #4a90a4; margin-bottom: 20px; text-align: center;">Why Choose Proofdoctor?</h3>
                        <ul class="features-list">
                            <li>Expert UK-based proofreaders with years of experience</li>
                            <li>Quick turnaround times to meet your deadlines</li>
                            <li>Competitive pricing for all document types</li>
                            <li>100% confidentiality guaranteed</li>
                            <li>Specialised in academic, business, and creative writing</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Overview Page -->
            <div id="overview" class="page-content hidden">
                <div class="content-box">
                    <h2 class="page-title">Overview</h2>
                    <p class="content-text">
                        At Proofdoctor, we understand that clear, error-free communication is essential for success in today's competitive world.
                    </p>
                    
                    <div style="margin: 40px 0;">
                        <h3 style="color: #4a90a4; margin-bottom: 20px;">Our Mission</h3>
                        <p style="margin-bottom: 20px; line-height: 1.8;">
                            We are dedicated to helping individuals and businesses across the UK present their best work through meticulous proofreading and editing services. Whether you're submitting an academic thesis, publishing a novel, or preparing a business proposal, our expert team ensures your message is conveyed with precision and professionalism.
                        </p>
                        
                        <h3 style="color: #4a90a4; margin-bottom: 20px; margin-top: 30px;">Our Process</h3>
                        <p style="margin-bottom: 20px; line-height: 1.8;">
                            Every document undergoes a comprehensive review process. Our proofreaders check for spelling, grammar, punctuation, consistency, and clarity. We preserve your unique voice while enhancing readability and impact. With flexible turnaround times and transparent pricing, we make professional proofreading accessible to everyone.
                        </p>
                        
                        <h3 style="color: #4a90a4; margin-bottom: 20px; margin-top: 30px;">Quality Guarantee</h3>
                        <p style="line-height: 1.8;">
                            We stand behind our work with a 100% satisfaction guarantee. If you're not completely happy with our service, we'll review your document again at no additional charge. Your success is our priority, and we're committed to delivering excellence in every project we undertake.
                        </p>
                    </div>
                </div>
            </div>

            <!-- Services Page -->
            <div id="services" class="page-content hidden">
                <div class="content-box">
                    <h2 class="page-title">Services</h2>
                    <p class="content-text">
                        We offer comprehensive proofreading and editing solutions tailored to your specific needs.
                    </p>
                    
                    <div class="services-grid">
                        <div class="service-card">
                            <h3>Academic Proofreading</h3>
                            <p>Essays, dissertations, theses, and research papers. We ensure your academic work meets the highest standards of clarity and precision.</p>
                        </div>
                        
                        <div class="service-card">
                            <h3>Business Documents</h3>
                            <p>Reports, proposals, presentations, and marketing materials. Make a professional impression with polished, error-free content.</p>
                        </div>
                        
                        <div class="service-card">
                            <h3>Creative Writing</h3>
                            <p>Novels, short stories, scripts, and poetry. We preserve your creative voice while ensuring technical accuracy.</p>
                        </div>
                        
                        <div class="service-card">
                            <h3>Website Content</h3>
                            <p>Web pages, blogs, and online articles. Enhance your digital presence with clear, engaging, SEO-friendly content.</p>
                        </div>
                        
                        <div class="service-card">
                            <h3>CV & Cover Letters</h3>
                            <p>Stand out from the competition with professionally proofread application materials that showcase your strengths.</p>
                        </div>
                        
                        <div class="service-card">
                            <h3>Express Service</h3>
                            <p>Urgent deadline? Our express service delivers quality proofreading within 24 hours for time-sensitive projects.</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Contact Page -->
            <div id="contact" class="page-content hidden">
                <div class="content-box">
                    <h2 class="page-title">Contact</h2>
                    <p class="content-text">
                        Get in touch for a free quote or to discuss your proofreading needs. We typically respond within 2 hours during business hours.
                    </p>
                    
                    <form class="contact-form" onsubmit="handleSubmit(event)">
                        <div class="form-group">
                            <label for="name">Name *</label>
                            <input type="text" id="name" name="name" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="email">Email Address *</label>
                            <input type="email" id="email" name="email" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="phone">Phone Number</label>
                            <input type="tel" id="phone" name="phone">
                        </div>
                        
                        <div class="form-group">
                            <label for="service">Service Required</label>
                            <select id="service" name="service" style="width: 100%; padding: 12px; border: 1px solid #c4b5a0; border-radius: 4px; font-size: 1em; background-color: white;">
                                <option value="">Select a service...</option>
                                <option value="academic">Academic Proofreading</option>
                                <option value="business">Business Documents</option>
                                <option value="creative">Creative Writing</option>
                                <option value="website">Website Content</option>
                                <option value="cv">CV & Cover Letters</option>
                                <option value="express">Express Service</option>
                                <option value="other">Other</option>
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label for="message">Message *</label>
                            <textarea id="message" name="message" required placeholder="Please describe your project, word count, and deadline..."></textarea>
                        </div>
                        
                        <button type="submit" class="submit-btn">Send Message</button>
                    </form>
                    
                    <div style="margin-top: 40px; text-align: center; color: #666;">
                        <p><strong>Email:</strong> info@proofdoctor.co.uk</p>
                        <p><strong>Phone:</strong> 020 7946 0958</p>
                        <p><strong>Hours:</strong> Monday - Friday, 9:00 AM - 6:00 PM GMT</p>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2024 Proofdoctor.co.uk - Professional Proofreading Services</p>
            <p style="margin-top: 10px; font-size: 0.9em;">Registered in England & Wales | All Rights Reserved</p>
        </div>
    </footer>

    <script>
        // Page navigation
        function showPage(pageName) {
            // Hide all pages
            const pages = document.querySelectorAll('.page-content');
            pages.forEach(page => page.classList.add('hidden'));
            
            // Show selected page
            document.getElementById(pageName).classList.remove('hidden');
            
            // Update active navigation
            const navLinks = document.querySelectorAll('.nav-link');
            navLinks.forEach(link => link.classList.remove('active'));
            event.target.classList.add('active');
            
            // Scroll to top
            window.scrollTo(0, 0);
        }
        
        // Handle form submission
        function handleSubmit(event) {
            event.preventDefault();
            
            // Get form data
            const formData = new FormData(event.target);
            const data = Object.fromEntries(formData);
            
            // Create mailto link
            const subject = encodeURIComponent('Proofreading Service Inquiry');
            const body = encodeURIComponent(
                `Name: ${data.name}\n` +
                `Email: ${data.email}\n` +
                `Phone: ${data.phone || 'Not provided'}\n` +
                `Service: ${data.service || 'Not specified'}\n\n` +
                `Message:\n${data.message}`
            );
            
            // Open email client
            window.location.href = `mailto:bedlam@gmail.com?subject=${subject}&body=${body}`;
            
            // Show confirmation
            alert('Thank you for your inquiry! Your default email client should now open with your message. If it doesn\'t, please email us directly at info@proofdoctor.co.uk');
            
            // Reset form
            event.target.reset();
        }
    </script>
</body>
</html>
