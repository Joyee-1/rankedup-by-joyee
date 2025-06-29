
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>RankUp by The Joyee Paradox Squad</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(to right, #000000, #2c003e);
      color: #fff;
      scroll-behavior: smooth;
    }

    header {
      background-color: #1a1a1a;
      padding: 20px;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    header h1 {
      color: #8e44ad;
      margin: 0;
      animation: glow 2s ease-in-out infinite alternate;
    }

    @keyframes glow {
      from { text-shadow: 0 0 10px #9b59b6, 0 0 20px #9b59b6; }
      to { text-shadow: 0 0 20px #00aaff, 0 0 30px #00aaff; }
    }

    nav a {
      margin: 0 15px;
      color: #9b59b6;
      text-decoration: none;
      transition: 0.3s;
    }

    nav a:hover {
      color: #00aaff;
    }

    section {
      padding: 60px 20px;
      text-align: center;
      opacity: 0;
      transform: translateY(30px);
      transition: opacity 1.2s ease-out, transform 1.2s ease-out;
    }

    section.show {
      opacity: 1;
      transform: translateY(0);
    }

    .price-card {
      background: #111;
      border: 1px solid #9b59b6;
      border-radius: 15px;
      padding: 20px;
      margin: 20px;
      display: inline-block;
      width: 280px;
      transition: transform 0.3s;
    }

    .price-card:hover {
      transform: scale(1.05);
    }

    .btn {
      padding: 10px 20px;
      background: #9b59b6;
      border: none;
      color: #fff;
      border-radius: 8px;
      cursor: pointer;
      margin-top: 15px;
      transition: 0.3s;
    }

    .btn:hover {
      background: #00aaff;
    }

    .hero-gallery {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
    }

    #review-form {
      margin-top: 30px;
    }

    textarea {
      width: 80%;
      height: 80px;
      border-radius: 10px;
      border: none;
      padding: 10px;
      font-family: inherit;
      resize: none;
    }

    #review-display {
      margin-top: 20px;
    }

    footer {
      background-color: #111;
      padding: 20px;
      text-align: center;
      font-size: 0.9em;
    }
  </style>
  <script>
    function contactNow() {
      alert("📲 To order rank boost, message us on WhatsApp: +8801XXXXXXX");
    }

    function submitReview() {
      const review = document.getElementById("review-text").value;
      if (review.trim() !== "") {
        const container = document.getElementById("review-display");
        const p = document.createElement("p");
        p.textContent = review;
        container.appendChild(p);
        document.getElementById("review-text").value = "";
        alert("Thanks for your feedback!");
      }
    }

    window.addEventListener("scroll", () => {
      document.querySelectorAll("section").forEach(sec => {
        const top = window.scrollY;
        const offset = sec.offsetTop - 400;
        const height = sec.offsetHeight;
        if (top >= offset && top < offset + height) {
          sec.classList.add("show");
        }
      });
    });
  </script>
</head>
<body>

<header>
  <h1>RankUp by The Joyee Paradox Squad</h1>
  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#pricing">Pricing</a>
    <a href="#reviews">Reviews</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<section id="home">
  <h2>Climb the Ranks. Play with Pros. Boosted by Joyee 💜</h2>
  <p>Trusted Squad. Fast Delivery. Real Results.</p>
  <button class="btn" onclick="contactNow()">Order Now</button>
</section>

<section id="about">
  <h2>About Us</h2>
  <p>We are a passionate squad of top-tier MLBB players offering affordable and professional rank boosting services. Led by Joyee, our mission is to help you climb effortlessly with style and speed!</p>
  <p>
    We are a squad led by Joyee, climbing ranks like legends. Want to see the magic? Follow the spark ✨  
    <a href="https://www.youtube.com/@the.joyee.paradox" target="_blank" rel="noopener noreferrer">
  🔮💜 Click only if you're curious 💜🔮
</a>
  </p>
</section>

<section id="pricing">
  <h2>Boosting Packages</h2>
  <div class="price-card">
    <h3>🎮 Regular Package</h3>
    <p>Warrior to Master = 300৳</p>
    <p>Master to Epic = 500৳</p>
    <p>Epic to Mythic = 800৳</p>
    <p>Based on time charge money can increase</p>
    <button class="btn" onclick="contactNow()">Order Now</button>
  </div>
  <div class="price-card">
    <h3>🔥 Combo Offer</h3>
    <p>Warrior → Mythic = 3000৳ (Save 200৳!) and  if you set time then charge money will increase</p>
    <button class="btn" onclick="contactNow()">Order Now</button>
  </div>
</section>



<section id="reviews">
  <h2>Client Reviews</h2>
  <p>“Joyee Squad boosted me from Grandmaster to Mythic in 4 days. Legit service! ⭐⭐⭐⭐⭐” – Samiha</p>
  <p>“Best boosting experience! Fast, friendly, and affordable.” – Zayan</p>
  <div id="review-form">
    <h3>Write your own review!And in the end write your NAME</h3>
    <textarea id="review-text" placeholder="Type your feedback here..."></textarea><br>
    <button class="btn" onclick="submitReview()">Submit</button>
    <div id="review-display"></div>



    <script>
        // Load reviews on page load
        window.addEventListener("DOMContentLoaded", () => {
          loadReviews();
        });
      
        function contactNow() {
          alert("📲 To order rank boost, message us on WhatsApp: +8801XXXXXXX");
        }
      
        function submitReview() {
          const review = document.getElementById("review-text").value.trim();
          if (review !== "") {
            const reviews = JSON.parse(localStorage.getItem("reviews") || "[]");
            reviews.push(review);
            localStorage.setItem("reviews", JSON.stringify(reviews));
            displayReview(review);
            document.getElementById("review-text").value = "";
            alert("Thanks for your feedback! It's saved successfully 💜");
          }
        }
      
        function loadReviews() {
          const reviews = JSON.parse(localStorage.getItem("reviews") || "[]");
          reviews.forEach(r => displayReview(r));
        }
      
        function displayReview(reviewText) {
          const container = document.getElementById("review-display");
          const p = document.createElement("p");
          p.textContent = reviewText;
          container.appendChild(p);
        }
      
        // Scroll animation for sections
        window.addEventListener("scroll", () => {
          document.querySelectorAll("section").forEach(sec => {
            const top = window.scrollY;
            const offset = sec.offsetTop - 400;
            const height = sec.offsetHeight;
            if (top >= offset && top < offset + height) {
              sec.classList.add("show");
            }
          });
        });
      </script>
      



  </div>
</section>

<section id="contact">
  <h2>Contact Us</h2>
  <p>📞 WhatsApp: +8801XXXXXXX</p>
  <p>💸 bKash/Nagad available</p>
  <p>📱 Discord: Joyee#9999</p>
</section>

<footer>
  <p>© 2025 RankUpByTheJoyeeParadoxSquad.com | All Rights Reserved</p>
</footer>

</body>
</html>


