<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gul Zehra | Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Roboto:wght@400;500&display=swap" rel="stylesheet">
<style>
  /* Global Styles */
  * { margin:0; padding:0; box-sizing:border-box; }
  body { font-family: 'Roboto', sans-serif; background: #fef6fb; color: #333; overflow-x: hidden; position: relative; }
  a { text-decoration: none; color: inherit; }

/* Things I Love Section */
.likes { 
  background: linear-gradient(135deg, #ffe6f2, #fff0f6); /* stronger pastel background */
  padding: 80px 20px; 
  text-align: center; 
  position: relative; 
  z-index: 1; 
}
.likes h2 { 
  margin-bottom: 40px; 
  font-size: 2.5rem; 
  color: #ff5aa5; 
  font-family: 'Pacifico', cursive; 
}

/* Make cards bigger and visible */
.like-card {
  position: relative;
  background: linear-gradient(135deg, #ffd1dc, #ffb3d9);
  border-radius: 25px;
  padding: 30px 20px;
  width: 220px;
  height: 140px;
  font-size: 1.2rem;
  font-weight: 500;
  box-shadow: 0 15px 25px rgba(0,0,0,0.15);
  transition: transform 0.4s, box-shadow 0.4s, background 0.4s;
  cursor: pointer;
  overflow: hidden;
}
.like-card:hover { 
  transform: scale(1.1) rotate(-3deg); 
  box-shadow: 0 20px 30px rgba(0,0,0,0.25); 
  background: linear-gradient(135deg, #ffb3d9, #ffd1dc); 
}

/* Grid layout */
.likes-grid { 
  display: flex; 
  flex-wrap: wrap; 
  justify-content: center; 
  gap: 30px; 
}

  /* Floating Background Shapes */
  .floating {
    position: absolute;
    font-size: 2rem;
    opacity: 0.4;
    animation: floatAnim calc(8s + var(--i)*1s) infinite ease-in-out;
    z-index: 0;
    pointer-events: none;
  }
  @keyframes floatAnim {
    0% { transform: translateY(0) rotate(0deg); opacity: 0.4; }
    50% { transform: translateY(-50px) rotate(180deg); opacity: 0.7; }
    100% { transform: translateY(0) rotate(360deg); opacity: 0.4; }
  }

  section { position: relative; z-index: 1; }

  /* Hero Section */
  .hero {
    position: relative;
    background: linear-gradient(135deg, #fbc2eb, #a6c1ee);
    color: white; padding: 100px 20px; text-align: center; overflow: hidden;
  }
  .hero h1 { font-family: 'Pacifico', cursive; font-size: 3rem; margin-bottom: 10px; }
  .hero p { font-size: 1.3rem; margin-bottom: 20px; }
  .hero .btn { padding: 10px 25px; background: #ff7eb9; border-radius: 30px; color: white; font-weight: 500; transition: 0.3s; }
  .hero .btn:hover { background: #ff5aa5; }

  /* About Section */
  .about { background: #fff0f6; padding: 60px 20px; text-align: center; }
  .about img { width: 150px; border-radius: 50%; margin-bottom: 20px; border: 5px solid #ffb3d9; }

  /* Projects Section */
  .projects-section { background: #f0f7ff; padding: 60px 20px; text-align: center; }
  .projects { display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; margin-top: 30px; }
  .project-card {
    background: linear-gradient(135deg, #ffecd2, #fcb69f);
    border-radius: 20px; padding: 20px; width: 250px;
    box-shadow: 0 10px 20px rgba(0,0,0,0.1); transition: transform 0.4s, box-shadow 0.4s;
  }
  .project-card:hover { transform: translateY(-10px) rotate(-2deg); box-shadow: 0 15px 25px rgba(0,0,0,0.2); }
  .project-card img { width: 100%; border-radius: 15px; margin-bottom: 15px; }
  .project-card h3 { font-weight: 500; margin-bottom: 10px; }
  .project-card p { font-size: 0.9rem; color: #555; }

  /* Things I Love Section */
  .likes { background: #fff0f6; padding: 60px 20px; text-align: center; }
  .likes h2 { margin-bottom: 30px; font-size: 2rem; color: #ff5aa5; font-family: 'Pacifico', cursive; }
  .likes-grid { display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; }

  .like-card {
    position: relative;
    background: linear-gradient(135deg, #ffd1dc, #ffb3d9);
    border-radius: 20px;
    padding: 25px 20px;
    width: 200px;
    font-size: 1.1rem;
    font-weight: 500;
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
    transition: transform 0.4s, box-shadow 0.4s, background 0.4s;
    cursor: pointer;
    overflow: hidden;
  }
  .like-card:hover { transform: scale(1.1) rotate(-3deg); box-shadow: 0 15px 25px rgba(0,0,0,0.2); background: linear-gradient(135deg, #ffb3d9, #ffd1dc); }

  /* Floating Animations inside Cards */
  @keyframes floatUp {
    0% { transform: translateY(0); opacity: 1; }
    50% { transform: translateY(-15px); opacity: 0.8; }
    100% { transform: translateY(0); opacity: 1; }
  }

  /* Programming card */
  .code-icon { position: absolute; font-size: 0.8rem; animation: floatUp 2s infinite; }
  #programming .code-icon:nth-child(2) { left: 10px; top: 10px; animation-delay: 0.5s; }
  #programming .code-icon:nth-child(3) { right: 10px; top: 15px; animation-delay: 1s; }

  /* Baking card */
  .sprinkle { position: absolute; font-size: 1rem; animation: floatUp 2.5s infinite; }
  #baking .sprinkle:nth-child(2) { left: 20px; top: 5px; animation-delay: 0.3s; }
  #baking .sprinkle:nth-child(3) { right: 15px; top: 10px; animation-delay: 0.8s; }

  /* Cats card */
  .paw { position: absolute; font-size: 1rem; animation: floatUp 1.8s infinite; }
  #cats .paw:nth-child(2) { left: 15px; bottom: 10px; animation-delay: 0.4s; }
  #cats .paw:nth-child(3) { right: 10px; bottom: 15px; animation-delay: 0.7s; }

  /* Anime & Cartoons card */
  .star { position: absolute; font-size: 0.9rem; animation: floatUp 2s infinite; }
  #anime .star:nth-child(2) { left: 15px; top: 5px; animation-delay: 0.2s; }
  #anime .star:nth-child(3) { right: 15px; top: 10px; animation-delay: 0.6s; }

  /* Social Links */
  .socials { margin-top: 20px; display: flex; justify-content: center; gap: 15px; }
  .socials a {
    display: flex; align-items: center; justify-content: center; width: 50px; height: 50px;
    border-radius: 50%; background: #ffb3d9; color: white; font-size: 1.5rem;
    transition: transform 0.3s, background 0.3s;
  }
  .socials a:hover { transform: scale(1.3) rotate(-10deg); background: #ff7eb9; }

  /* Contact */
  .contact { background: #f0f7ff; padding: 60px 20px; }
  .contact form { max-width: 400px; margin: auto; display: flex; flex-direction: column; gap: 15px; }
  .contact input, .contact textarea { padding: 10px; border-radius: 15px; border: none; outline: none; }
  .contact button { padding: 12px; border-radius: 25px; border: none; background: #ff7eb9; color: white; font-weight: 500; cursor: pointer; transition: 0.3s; }
  .contact button:hover { background: #ff5aa5; }

  /* Footer */
  footer { padding: 20px; background: #ffe6f2; text-align: center; }
</style>
</head>
<body>

<!-- Floating Background Elements -->
<div class="floating" style="--i:0; left:10%; top:5%;">💻</div>
<div class="floating" style="--i:1; left:80%; top:20%;">🧁</div>
<div class="floating" style="--i:2; left:30%; top:70%;">🐱</div>
<div class="floating" style="--i:3; left:50%; top:40%;">⭐</div>
<div class="floating" style="--i:4; left:70%; top:80%;">💻</div>
<div class="floating" style="--i:5; left:20%; top:30%;">🧁</div>

<!-- Hero Section -->
<section class="hero">
  <h1>Gule Zehra</h1>
  <p>Creative Programmer, Developer & Baker Who Loves Cats and Anime!</p>
  <a href="#projects" class="btn">See My Work</a>
</section>

<!-- About Section -->
<section class="about">
  <img src="https://via.placeholder.com/150" alt="Your Avatar">
  <h2>About Me</h2>
  <p>Hello! I'm a creative programmer and developer who loves baking, cats, and watching anime & cartoons. I enjoy making colorful, fun, and interactive projects!</p>
</section>

<!-- Projects Section -->
<section id="projects" class="projects-section">
  <h2>My Projects</h2>
  <div class="projects">
    <div class="project-card">
      <img src="https://via.placeholder.com/250x150" alt="Project 1">
      <h3>Project 1</h3>
      <p>Short description of this cute project.</p>
    </div>
    <div class="project-card">
      <img src="https://via.placeholder.com/250x150" alt="Project 2">
      <h3>Project 2</h3>
      <p>Short description of another project.</p>
    </div>
    <div class="project-card">
      <img src="https://via.placeholder.com/250x150" alt="Project 3">
      <h3>Project 3</h3>
      <p>A fun and colorful project showcase.</p>
    </div>
  </div>
</section>

<!-- Things I Love Section -->
<section class="likes">
  <h2>Things I Love 💖</h2>
  <div class="likes-grid">
    <div class="like-card" id="programming">💻 Programming & Development
      <span class="code-icon">{};</span>
      <span class="code-icon"><>;</span>
    </div>
    <div class="like-card" id="baking">🧁 Baking
      <span class="sprinkle">✨</span>
      <span class="sprinkle">🍬</span>
    </div>
    <div class="like-card" id="cats">🐱 Cats
      <span class="paw">🐾</span>
      <span class="paw">🐾</span>
    </div>
    <div class="like-card" id="anime">🎨 Anime & Cartoons
      <span class="star">⭐</span>
      <span class="star">✨</span>
    </div>
  </div>
</section>

<!-- Social Links -->
<section>
  <h2>Connect with Me</h2>
  <div class="socials">
    <a href="mailto:your@email.com">📧</a>
    <a href="tel:+1234567890">📞</a>
    <a href="https://github.com/yourusername" target="_blank">🐱</a>
    <a href="https://linkedin.com/in/yourusername" target="_blank">🔗</a>
  </div>
</section>

<!-- Contact Section -->
<section class="contact">
  <h2>Contact Me</h2>
  <form>
    <input type="text" placeholder="Your Name" required>
    <input type="email" placeholder="Your Email" required>
    <textarea placeholder="Your Message" rows="4" required></textarea>
    <button type="submit">Send Message</button>
  </form>
</section>

<!-- Footer -->
<footer>
  <p>&copy; 2025 Gule Zehra. All Rights Reserved.</p>
</footer>

</body>
</html>
