<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Desmond | Fullstack Designer</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Segoe UI', sans-serif;
      background: #111;
      color: #eee;
      scroll-behavior: smooth;
    }
    header {
      background: linear-gradient(90deg, #0f0f0f, #1a1a1a);
      padding: 2rem 0;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 999;
    }
    header h1 {
      font-size: 2.5rem;
      color: #00ffcc;
    }
    nav ul {
      display: flex;
      justify-content: center;
      list-style: none;
      margin-top: 1rem;
    }
    nav ul li {
      margin: 0 1rem;
    }
    nav ul li a {
      color: #fff;
      text-decoration: none;
      font-weight: bold;
      transition: color 0.3s ease;
    }
    nav ul li a:hover {
      color: #00ffcc;
    }
    .hero {
      height: 100vh;
      background: linear-gradient(to bottom right, #0f2027, #203a43, #2c5364);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 2rem;
    }
    .hero h2 {
      font-size: 3rem;
      animation: fadeInDown 1s ease-out;
    }
    .hero p {
      margin-top: 1rem;
      font-size: 1.25rem;
      color: #ccc;
      animation: fadeInUp 1s ease-out;
    }
    .btn {
      margin-top: 2rem;
      padding: 12px 24px;
      background: #00ffcc;
      color: #000;
      border: none;
      border-radius: 5px;
      font-weight: bold;
      cursor: pointer;
      transition: background 0.3s ease;
    }
    .btn:hover {
      background: #00bfa6;
    }
    .section {
      padding: 5rem 2rem;
    }
    .projects {
      background: #1a1a1a;
    }
    .project {
      background: #222;
      padding: 2rem;
      border-radius: 10px;
      margin-bottom: 2rem;
      animation: fadeIn 0.8s ease forwards;
      transform: translateY(20px);
      opacity: 0;
    }
    .project h3 {
      margin-bottom: 1rem;
      color: #00ffcc;
    }
    .project p {
      color: #aaa;
    }
    footer {
      background: #000;
      text-align: center;
      padding: 2rem;
      color: #666;
    }
    @keyframes fadeInDown {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes fadeIn {
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <header>
    <h1>Desmond - Fullstack Designer</h1>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#projects">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section class="hero" id="home">
    <h2>I Build Stunning Web Experiences</h2>
    <p>From frontend finesse to backend power – I do it all.</p>
    <a href="#projects" class="btn">ABOUT US</a>
  </section>

  <section class="section projects" id="projects">
    <div class="project">
      <h3> Website Creation</h3>
      <p>We Create Responsive Layouts For Our Costumers</p>
    </div>
    <div class="project">
      <h3>How We Go About It?</h3>
      <p>Our Sites Are Built With Ideas Based On Experience</p>
    </div>
    <div class="project">
      <h3>We Are Second To None In Our Programming And Intellect</h3>
      <p>We Are Experts In Our Field</p>
    </div>
  </section>

  <section class="section" id="contact">
    <h2>Let's Work Together</h2>
    <p>Email me: <a href="ezikev3@gmail.com" style="color:#00ffcc">ezikev3@gmail.com</a></p>
  </section>

  <footer>
    <p>&copy; 2025 Desmond. All rights reserved.</p>
  </footer>

  <script>
    // Animate on scroll
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.animation = 'fadeIn 1s ease forwards';
        }
      });
    }, { threshold: 0.1 });

    document.querySelectorAll('.project').forEach(project => {
      observer.observe(project);
    });
  </script>
</body>
</html>
