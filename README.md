# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨


index.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Kakuma Music Production</title>
  <link rel="stylesheet" href="style.css"/>
</head>
<body>

  <nav class="navbar">
    <div class="logo"></div>
    <ul class="nav-links">
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <main class="container">
    <section class="content">
      <h2>Welcome To Kakuma Music Production</h2>
      <p>Step into a creative space where talent meets technology. At Kakuma Music Production, we empower aspiring artists and producers to bring their musical visions to life. Whether you're recording your first track, mixing beats, or exploring audio editing, our studio is your launchpad. Join a growing community of creators and let your sound be heard—loud, clear, and uniquely yours.</p>
    </section>
    <aside class="sidebar">
      <h3>check it out</h3>
      <p>Curious to hear more? Check it out and dive into the sound!.</p>
    </aside>
  </main>

</body>
</html>


style.css

/* Base Reset and Fonts */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  
  body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
  }
  
  /* Navbar */
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #333;
    padding: 1rem;
    color: white;
  }
  
  .navbar .logo {
    font-size: 1.5rem;
    font-weight: bold;
  }
  
  .nav-links {
    list-style: none;
    display: flex;
    gap: 1rem;
  }
  
  .nav-links a {
    color: white;
    text-decoration: none;
  }
  
  /* Layout using Flexbox */
  .container {
    display: flex;
    padding: 20px;
    gap: 20px;
  }
  
  .content {
    flex: 2;
  }
  
  .sidebar {
    flex: 1;
    background: #f4f4f4;
    padding: 15px;
    border: 1px solid #ccc;
  }
  
  /* Responsive Design */
  @media (max-width: 768px) {
    .container {
      flex-direction: column;
    }
  
    .nav-links {
      flex-direction: column;
      gap: 0.5rem;
    }
  
    .navbar {
      flex-direction: column;
      align-items: flex-start;
    }
  }
  
  @media (max-width: 480px) {
    body {
      font-size: 14px;
    }
  
    .navbar .logo {
      font-size: 1.2rem;
    }
  
    .nav-links a {
      font-size: 14px;
    }
  }
  

