<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive Achievements</title>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" />
  <style>
    /* Global Styles */
    * {
      box-sizing: border-box;
    }
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
      padding: 12px 20px;
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
      padding: 40px 20px;
    }
    .hero h2 {
      font-size: 2.2rem;
      margin: 0 0 10px;
    }
    .hero p {
      font-size: 1.1rem;
      margin: 0;
    }
    .container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 20px;
      padding: 20px;
      max-width: 1200px;
      margin: auto;
    }
    .card {
      background: #1f1f1f;
      border-radius: 12px;
      padding: 15px;
      text-align: center;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
      transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
    }
    .card:hover {
      transform: scale(1.04);
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.5);
    }
    .card img {
      width: 100%;
      height: auto;
      max-width: 240px;
      border-radius: 10px;
      margin: 0 auto 15px;
      display: block;
      object-fit: cover;
    }
    .card h2 {
      font-size: 1.4rem;
      margin-bottom: 10px;
    }
    .card p {
      font-size: 0.95rem;
      line-height: 1.5;
      margin: 0;
    }
    footer {
      text-align: center;
      background: #1a1a1a;
      padding: 15px;
      color: #999999;
      margin-top: 30px;
    }
    footer p {
      margin: 0;
    }

    /* Tablet */
    @media (max-width: 768px) {
      .hero h2 {
        font-size: 1.8rem;
      }
      .hero p {
        font-size: 1rem;
      }
      .card h2 {
        font-size: 1.2rem;
      }
      .card p {
        font-size: 0.9rem;
      }
    }

    /* Phone */
    @media (max-width: 480px) {
      header h1 {
        font-size: 1.4rem;
      }
      .hero h2 {
        font-size: 1.6rem;
      }
      .container {
        padding: 10px;
        gap: 15px;
      }
      .card img {
        max-width: 180px;
      }
      .card h2 {
        font-size: 1.1rem;
      }
      .card p {
        font-size: 0.85rem;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>My Achievements</h1>
  </header>
  <section class="hero">
    <h2>Welcome to My Achievements</h2>
    <p>Explore milestones that define my journey.</p>
  </section>
  <div class="container" id="achievement-container">
    <!-- Cards dynamically generated via JavaScript -->
  </div>
  <footer>
    <p>&copy; 2025 My Responsive Achievements</p>
  </footer>

  <script>
    // Achievement Data
    const achievements = [
      { title: "Milestone 1", description: "Description of milestone 1", image: "https://via.placeholder.com/300x200" },
      { title: "Milestone 2", description: "Description of milestone 2", image: "https://via.placeholder.com/300x200" },
      { title: "Milestone 3", description: "Description of milestone 3", image: "https://via.placeholder.com/300x200" }
    ];

    const container = document.getElementById('achievement-container');
    achievements.forEach(({ title, description, image }) => {
      const card = document.createElement('div');
      card.className = 'card';
      card.innerHTML = `
        <img src="${image}" alt="${title || 'Achievement Image'}">
        <h2>${title}</h2>
        <p>${description}</p>
      `;
      container.appendChild(card);
    });
  </script>
</body>
</html>
