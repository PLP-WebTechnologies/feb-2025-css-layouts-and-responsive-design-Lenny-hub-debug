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
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Responsive Layout</title>
  <link rel="stylesheet" href="styles.css"/>
</head>
<body>
  <header>
    <nav class="navbar">
      <div class="logo">MySite</div>
      <ul class="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Projects</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main class="container">
    <section class="content">
      <h1>Welcome to My Responsive Page</h1>
      <p>This layout adapts to mobile, tablet, and desktop views.</p>
    </section>
    <aside class="sidebar">
      <h2>Sidebar</h2>
      <p>Additional info or links go here.</p>
    </aside>
  </main>

  <footer class="footer">
    <p>&copy; 2025 MySite</p>
  </footer>
</body>
</html>
/* General Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: sans-serif;
  line-height: 1.6;
}

/* Navigation Bar */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #333;
  color: white;
  padding: 1rem;
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 1.5rem;
}

.nav-links a {
  color: white;
  text-decoration: none;
}

/* Layout */
.container {
  display: flex;
  padding: 2rem;
  gap: 2rem;
}

.content {
  flex: 2;
}

.sidebar {
  flex: 1;
  background: #f4f4f4;
  padding: 1rem;
}

.footer {
  text-align: center;
  padding: 1rem;
  background: #333;
  color: white;
}

/* Media Queries */
@media (max-width: 768px) {
  .container {
    flex-direction: column;
  }

  .nav-links {
    flex-direction: column;
    gap: 1rem;
    text-align: center;
  }
}

@media (max-width: 480px) {
  .navbar {
    flex-direction: column;
  }

  .container {
    padding: 1rem;
  }

  .nav-links {
    gap: 0.5rem;
  }
}
