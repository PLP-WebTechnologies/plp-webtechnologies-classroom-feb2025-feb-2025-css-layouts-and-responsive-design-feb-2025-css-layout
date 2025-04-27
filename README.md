# CSS Layouts and Responsive Design
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Flexbox Layout</title>
  <style>
    /* Base styles */
    body {
      margin: 0;
      font-family: Arial, sans-serif;
    }

    header {
      background-color: #333;
      color: #fff;
      padding: 1rem;
    }

    nav {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
      background-color: #444;
    }

    nav a {
      color: white;
      text-decoration: none;
      padding: 1rem;
    }

    nav a:hover {
      background-color: #666;
    }

    .container {
      display: flex;
      flex-direction: row;
      padding: 1rem;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .sidebar, .main-content {
      background: #f4f4f4;
      padding: 1rem;
      border: 1px solid #ddd;
    }

    .sidebar {
      flex: 1 1 20%;
    }

    .main-content {
      flex: 3 1 75%;
    }

    footer {
      text-align: center;
      padding: 1rem;
      background-color: #eee;
    }

    /* Tablet (768px and below) */
    @media (max-width: 768px) {
      .container {
        flex-direction: column;
      }

      .sidebar, .main-content {
        flex: 1 1 100%;
      }

      nav {
        flex-direction: column;
      }
    }

    /* Mobile (480px and below) */
    @media (max-width: 480px) {
      nav a {
        padding: 0.5rem;
        text-align: center;
        flex: 1 1 100%;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>My Responsive Page</h1>
  </header>

  <nav>
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Services</a>
    <a href="#">Contact</a>
  </nav>

  <div class="container">
    <aside class="sidebar">Sidebar content</aside>
    <main class="main-content">Main content area</main>
  </div>

  <footer>
    <p>&copy; 2025 My Website</p>
  </footer>

</body>
</html>

