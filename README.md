<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout Example</title>
    <style>
        /* Reset and base styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
        }
        
        /* Navigation Bar - Flexbox */
        nav {
            background-color: #2c3e50;
            padding: 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .logo {
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 1.5rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: #3498db;
        }
        
        /* Main Content - CSS Grid */
        .container {
            display: grid;
            grid-template-columns: 1fr;
            gap: 1.5rem;
            padding: 1.5rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        /* Grid items */
        .card {
            background: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            padding: 1.5rem;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .card h2 {
            margin-bottom: 1rem;
            color: #2c3e50;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #3498db, #2c3e50);
            color: white;
            padding: 3rem 1.5rem;
            text-align: center;
            grid-column: 1 / -1;
            border-radius: 8px;
        }
        
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }
        
        /* Footer */
        footer {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 1.5rem;
            margin-top: 1.5rem;
        }
        
        /* Media Queries for Responsive Design */
        
        /* Tablet View (600px and up) */
        @media (min-width: 600px) {
            .container {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .hero h1 {
                font-size: 3rem;
            }
        }
        
        /* Desktop View (900px and up) */
        @media (min-width: 900px) {
            .container {
                grid-template-columns: repeat(3, 1fr);
            }
            
            .featured {
                grid-column: span 2;
            }
            
            .nav-links {
                gap: 2rem;
            }
        }
        
        /* Mobile Navigation */
        @media (max-width: 500px) {
            nav {
                flex-direction: column;
                padding: 1rem 0;
            }
            
            .nav-links {
                margin-top: 1rem;
                flex-direction: column;
                align-items: center;
                width: 100%;
            }
            
            .nav-links li {
                margin: 0.5rem 0;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <nav>
        <div class="logo">MySite</div>
        <ul class="nav-links">
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Portfolio</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>
    
    <div class="container">
        <section class="hero card">
            <h1>Welcome to Our Website</h1>
            <p>Discover amazing features and services tailored just for you.</p>
        </section>
        
        <article class="card">
            <h2>Web Development</h2>
            <p>We create responsive, user-friendly websites that work across all devices and platforms.</p>
        </article>
        
        <article class="card">
            <h2>UI/UX Design</h2>
            <p>Our design team focuses on creating intuitive interfaces that enhance user experience.</p>
        </article>
        
        <article class="card featured">
            <h2>Featured Service</h2>
            <p>Our featured service combines cutting-edge technology with innovative design to deliver exceptional results.</p>
        </article>
        
        <article class="card">
            <h2>Mobile Apps</h2>
            <p>We develop native and cross-platform mobile applications for iOS and Android.</p>
        </article>
        
        <article class="card">
            <h2>SEO Optimization</h2>
            <p>Improve your search engine rankings and increase organic traffic to your website.</p>
        </article>
    </div>
    
    <footer>
        <p>&copy; 2023 MySite. All rights reserved.</p>
    </footer>
</body>
</html>
