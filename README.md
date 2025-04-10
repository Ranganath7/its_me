<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Responsive Achievements</title>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap">
  <style>
    body {
      font-family: 'Inter', sans-serif;
      margin: 0;
      padding: 0;
      background: #121212;
      color: #ffffff;
    }
    header {
      position: sticky;
      top: 0;
      background: #1a1a1a;
      padding: 15px;
      text-align: center;
      z-index: 10;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.4);
    }
    header h1 {
      margin: 0;
      font-size: 1.8rem;
    }
    .hero {
      text-align: center;
      background: linear-gradient(135deg, #6200ea, #00bcd4);
      padding: 50px 20px;
    }
    .hero h2 {
      font-size: 2.5rem;
      margin: 0 0 10px;
    }
    .hero p {
      font-size: 1.1rem;
    }
    .container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      padding: 20px;
      max-width: 1200px;
      margin: auto;
    }
    .card {
      background: #1f1f1f;
      border-radius: 12px;
      padding: 20px;
      text-align: center;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
      transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
    }
    .card:hover {
      transform: scale(1.05);
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.5);
    }
    .card img {
      width: 100%;
      max-width: 260px;
      border-radius: 10px;
      margin: 0 auto 15px;
    }
    .card h2 {
      font-size: 1.5rem;
      margin-bottom: 10px;
    }
    .card p {
      font-size: 1rem;
      line-height: 1.5;
    }
    footer {
      text-align: center;
      background: #1a1a1a;
      padding: 20px;
      color: #999999;
      margin-top: 30px;
    }
    footer p {
      margin: 0;
    }
  </style>
</head>
<body>
  <header>
    <h1>My Achievements</h1>
  </header>
  <section class="hero">
    <h2>Welcome to My Achievements</h2>
    <p>Explore the milestones that define my journey.</p>
  </section>
  <div class="container" id="achievement-container">
    <!-- JavaScript dynamically adds cards here -->
  </div>
  <footer>
    <p>&copy; 2025 My Responsive Achievements</p>
  </footer>
  <script>
    const achievements = [
      { title: "Milestone 1", description: "Description of achievement 1", image: "path-to-image1.jpg" },
      { title: "Milestone 2", description: "Description of achievement 2", image: "path-to-image2.jpg" },
      { title: "Milestone 3", description: "Description of achievement 3", image: "path-to-image3.jpg" }
    ];

    const container = document.getElementById('achievement-container');
    achievements.forEach(achievement => {
      const card = document.createElement('div');
      card.className = 'card';
      card.innerHTML = `
        <img src="${achievement.image}" alt="${achievement.title}">
        <h2>${achievement.title}</h2>
        <p>${achievement.description}</p>
      `;
      container.appendChild(card);
    });
  </script>
</body>
</html>
