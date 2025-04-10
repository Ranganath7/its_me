<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Mobile Cards with Scroll Animation</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: sans-serif;
      background-color: #111;
      color: #fff;
      overflow-x: hidden;
      padding: 20px;
    }

    .card {
      background-color: #222;
      border-radius: 12px;
      padding: 15px;
      width: 100%;
      margin-bottom: 20px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.4);
      opacity: 0;
      transform: translateY(40px);
      transition: opacity 0.6s ease, transform 0.6s ease;
    }

    .card.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .card:hover {
      transform: scale(1.02);
      box-shadow: 0 6px 16px rgba(0, 0, 0, 0.6);
    }

    .card img {
      width: 100%;
      height: auto;
      border-radius: 8px;
      margin-bottom: 10px;
    }

    .card h2 {
      font-size: 1.2rem;
      margin-bottom: 8px;
    }

    .card p {
      font-size: 1rem;
      color: #ccc;
    }
  </style>
</head>
<body>

  <div class="card">
    <img src="https://via.placeholder.com/300x150" alt="Image 1" />
    <h2>Title 1</h2>
    <p>Description for box 1</p>
  </div>

  <div class="card">
    <img src="https://via.placeholder.com/300x150" alt="Image 2" />
    <h2>Title 2</h2>
    <p>Description for box 2</p>
  </div>

  <div class="card">
    <img src="https://via.placeholder.com/300x150" alt="Image 3" />
    <h2>Title 3</h2>
    <p>Description for box 3</p>
  </div>

  <script>
    // Simple scroll reveal effect
    const cards = document.querySelectorAll('.card');

    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    }, {
      threshold: 0.1
    });

    cards.forEach(card => {
      observer.observe(card);
    });
  </script>

</body>
</html>
