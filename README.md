## Hi there 👋

<!--
**Fashion-mart/Fashion-Mart** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>FASHION MART</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Montserrat', sans-serif;
    }
    body {
      background: #fff;
      color: #333;
    }
    header {
      background-color: #000;
      color: #fff;
      padding: 1rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    header h1 {
      font-size: 1.5rem;
    }
    nav a {
      color: #fff;
      margin: 0 1rem;
      text-decoration: none;
    }
    .banner {
      background: url('https://via.placeholder.com/1400x400') no-repeat center center/cover;
      height: 400px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 2rem;
      font-weight: bold;
    }
    .categories, .products, .scanner, .contact {
      padding: 2rem;
    }
    .categories h2, .products h2, .scanner h2, .contact h2 {
      margin-bottom: 1rem;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 1.5rem;
    }
    .card {
      border: 1px solid #ddd;
      padding: 1rem;
      border-radius: 10px;
      text-align: center;
    }
    .card img {
      width: 100%;
      height: auto;
      border-radius: 8px;
    }
    .footer {
      background: #000;
      color: #fff;
      text-align: center;
      padding: 1rem;
      margin-top: 2rem;
    }
    form input, form textarea, form button {
      display: block;
      width: 100%;
      margin-bottom: 1rem;
      padding: 0.75rem;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    form button {
      background: #000;
      color: #fff;
      border: none;
      cursor: pointer;
    }
    #scanner-output {
      margin-top: 1rem;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <header>
    <h1>FASHION MART</h1>
    <nav>
      <a href="#">Home</a>
      <a href="#">Men</a>
      <a href="#">Women</a>
      <a href="#">Kids</a>
      <a href="#">Offers</a>
      <a href="#">Login</a>
    </nav>
  </header>  <section class="banner">
    Trending Styles for You
  </section>  <section class="categories">
    <h2>Shop by Category</h2>
    <div class="grid">
      <div class="card">
        <img src="https://via.placeholder.com/200" alt="Men">
        <p>Men</p>
      </div>
      <div class="card">
        <img src="https://via.placeholder.com/200" alt="Women">
        <p>Women</p>
      </div>
      <div class="card">
        <img src="https://via.placeholder.com/200" alt="Kids">
        <p>Kids</p>
      </div>
    </div>
  </section>  <section class="products">
    <h2>Trending Products</h2>
    <div class="grid">
      <div class="card">
        <img src="https://via.placeholder.com/200" alt="Product 1">
        <p>Stylish T-Shirt</p>
        <p><strong>$19.99</strong></p>
      </div>
      <div class="card">
        <img src="https://via.placeholder.com/200" alt="Product 2">
        <p>Summer Dress</p>
        <p><strong>$29.99</strong></p>
      </div>
      <div class="card">
        <img src="https://via.placeholder.com/200" alt="Product 3">
        <p>Casual Shoes</p>
        <p><strong>$39.99</strong></p>
      </div>
    </div>
  </section>  <section class="scanner">
    <h2>QR Code Scanner</h2>
    <p>Scan product QR codes for quick access.</p>
    <video id="preview" width="100%"></video>
    <div id="scanner-output"></div>
    <script src="https://unpkg.com/html5-qrcode" type="text/javascript"></script>
    <script>
      function onScanSuccess(decodedText, decodedResult) {
        document.getElementById("scanner-output").innerText = "Scanned: " + decodedText;
      }
      const html5QrCode = new Html5Qrcode("preview");
      Html5Qrcode.getCameras().then(devices => {
        if (devices && devices.length) {
          html5QrCode.start(
            { facingMode: "environment" },
            {
              fps: 10,
              qrbox: 250
            },
            onScanSuccess
          );
        }
      });
    </script>
  </section>  <section class="contact">
    <h2>Contact Us</h2>
    <form>
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea rows="4" placeholder="Your Message"></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>  <footer class="footer">
    &copy; 2025 FASHION MART. All rights reserved.
  </footer>
</body>
</html>
