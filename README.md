<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>My Achievements</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      background-color: #111;
      color: white;
      font-family: Arial, sans-serif;
    }

    header {
      text-align: center;
      padding: 20px;
    }

    header h1 {
      font-size: 2.5rem;
    }

    .hero {
      text-align: center;
      background: linear-gradient(90deg, #6a11cb 0%, #2575fc 100%);
      padding: 40px 20px;
    }

    .hero h2 {
      font-size: 2.2rem;
      margin-bottom: 10px;
    }

    .hero p {
      font-size: 1.1rem;
      color: #ddd;
    }

    .container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      align-items: flex-start;
      gap: 20px;
      max-width: 1200px;
      margin: 40px auto;
      padding: 20px;
    }

    .card {
      background-color: #1e1e1e;
      border-radius: 15px;
      padding: 20px;
      flex: 1 1 300px; /* 👈 THIS allows wrapping + flexible growth */
      max-width: 300px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
      text-align: center;
      transition: transform 0.2s ease;
    }

    .card img {
      width: 100%;
      height: 150px;
      object-fit: cover;
      border-radius: 10px;
      margin-bottom: 15px;
    }

    .card h2 {
      font-size: 1.5rem;
      margin-bottom: 10px;
    }

    .card p {
      font-size: 1rem;
      color: #ccc;
    }

    .card:hover {
      transform: scale(1.03);
    }

    /* Tablet */
    @media (max-width: 768px) {
      .hero h2 {
        font-size: 1.8rem;
      }
      .hero p {
        font-size: 1rem;
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
    <hr />
  </header>

  <section class="hero">
    <h2>Welcome to My Achievements</h2>
    <p>Explore milestones that define my journey.</p>
    <hr />
  </section>

  <section class="container">
    <div class="card">
      <img src="https://via.placeholder.com/300x150?text=Milestone+1" alt="Milestone 1" />
      <h2>Milestone 1</h2>
      <p>Description of milestone 1</p>
    </div>
    <div class="card">
      <img src="https://via.placeholder.com/300x150?text=Milestone+2" alt="Milestone 2" />
      <h2>Milestone 2</h2>
      <p>Description of milestone 2</p>
    </div>
    <div class="card">
      <img src="https://via.placeholder.com/300x150?text=Milestone+3" alt="Milestone 3" />
      <h2>Milestone 3</h2>
      <p>Description of milestone 3</p>
    </div>
  </section>

</body>
</html>
