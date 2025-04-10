<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive Cards</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: sans-serif;
      background: #111;
      color: #fff;
      overflow-x: hidden;
    }

    .container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      padding: 20px;
    }

    .card {
      background: #222;
      border-radius: 12px;
      padding: 20px;
      flex: 1 1 300px;      /* 📱 Auto-resize */
      max-width: 300px;     /* 💻 Looks good on desktop */
      width: 100%;          /* ✅ Shrinks on mobile */
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.4);
    }

    .card img {
      width: 100%;
      height: auto;
      border-radius: 8px;
      margin-bottom: 10px;
    }

    .card h2 {
      font-size: 1.3rem;
      margin-bottom: 8px;
    }

    .card p {
      font-size: 1rem;
      color: #ccc;
    }

    @media (max-width: 768px) {
      .card {
        max-width: 100%;  /* 🔥 Full width on smaller screens */
      }
    }
  </style>
</head>
<body>

  <div class="container">
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
  </div>

</body>
</html>
