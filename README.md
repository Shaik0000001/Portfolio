<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Portfolio</title>

  <style>
    /* RESET */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, Helvetica, sans-serif;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background-color: #0f172a;
      color: #e5e7eb;
    }

    section {
      padding: 80px 10%;
    }

    h1, h2 {
      margin-bottom: 20px;
    }

    /* HERO */
    .hero {
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .hero h1 {
      font-size: 3rem;
    }

    .hero span {
      color: #38bdf8;
    }

    .hero p {
      font-size: 1.2rem;
      margin-top: 10px;
    }

    .btn {
      margin-top: 25px;
      display: inline-block;
      width: fit-content;
      padding: 12px 24px;
      background-color: #38bdf8;
      color: #000;
      text-decoration: none;
      border-radius: 8px;
      font-weight: bold;
      transition: transform 0.3s ease;
    }

    .btn:hover {
      transform: translateY(-3px);
    }

    /* ABOUT */
    .about p {
      max-width: 700px;
      line-height: 1.6;
    }

    /* PROJECTS */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }

    .project-card {
      background-color: #1e293b;
      padding: 20px;
      border-radius: 10px;
      transition: transform 0.3s ease;
      opacity: 0;
      transform: translateY(40px);
    }

    .project-card:hover {
      transform: translateY(-10px);
    }

    /* CONTACT */
    .contact p {
      margin-bottom: 10px;
    }

    /* FOOTER */
    footer {
      text-align: center;
      padding: 20px;
      background-color: #020617;
      font-size: 0.9rem;
    }

    /* RESPONSIVE */
    @media (max-width: 768px) {
      section {
        padding: 60px 6%;
      }

      .hero h1 {
        font-size: 2.2rem;
      }
    }
  </style>
</head>

<body>

  <!-- HERO -->
  <section class="hero">
    <h1>Hi, I'm <span>Shaik MahaboobBasha</span></h1>
    <p>B.tech Data Science student</p>
    <a href="#projects" class="btn">View My Work</a>
  </section>

  <!-- ABOUT -->
  <section class="about">
    <h2>About Me</h2>
    <p>
      I’m a passionate and detail-oriented developer with a strong interest in building modern, responsive, and user-friendly web applications. I enjoy turning ideas into clean, functional interfaces using HTML, CSS, JavaScript, and modern tools.

Currently pursuing my B.Tech, I focus on continuously improving my skills, learning new technologies, and creating real-world projects that solve practical problems. I value clean code, thoughtful design, and performance-focused development.
    </p>
  </section>

  <!-- PROJECTS -->
  <section class="projects" id="projects">
    <h2>Projects</h2>
    <div class="projects-grid">
      <div class="project-card"> My PortFolio</div>
      <div class="project-card">House Price Prediction</div>
      <div class="project-card">More</div>
    </div>
  </section>

  <!-- CONTACT -->
  <section class="contact">
    <h2>Contact</h2>
    <p>Email: mahaboobbashashaik671@gmail.com</p>
    <p>LinkedIn: https://www.linkedin.com/in/mahaboobbashashaik01</p>
  </section>

  <!-- FOOTER -->
  <footer>
    © 2026 Shaik MahaboobBasha. All rights reserved.
  </footer>

  <script>
    // SCROLL ANIMATION
    const cards = document.querySelectorAll(".project-card");

    window.addEventListener("scroll", () => {
      cards.forEach(card => {
        const top = card.getBoundingClientRect().top;
        if (top < window.innerHeight - 100) {
          card.style.opacity = "1";
          card.style.transform = "translateY(0)";
        }
      });
    });
  </script>

</body>
</html>
