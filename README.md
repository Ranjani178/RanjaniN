# RanjaniN
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Ranjani N | Computer Science Student</title>
<meta name="description" content="Portfolio of Ranjani N, B.E. Computer Science and Engineering student skilled in Java and web development.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;700&family=JetBrains+Mono:wght@400;500&family=Playfair+Display:wght@600;800&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #f4f5f7;
    --paper: #ffffff;
    --ink: #20232b;
    --muted: #5b6070;
    --line: #d9dce3;
    --accent: #2f4bd8;
    --serif: "Playfair Display", Georgia, serif;
    --sans: "DM Sans", system-ui, sans-serif;
    --mono: "JetBrains Mono", Consolas, monospace;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body { font-family: var(--sans); background: var(--bg); color: var(--ink); line-height: 1.65; }
  a { color: var(--accent); }
  a:focus-visible, button:focus-visible { outline: 3px solid var(--accent); outline-offset: 3px; }
  .wrap { max-width: 1040px; margin: 0 auto; padding: 0 24px; }

  /* Navigation */
  header { border-bottom: 1px solid var(--line); background: var(--paper); position: sticky; top: 0; z-index: 10; }
  nav { display: flex; justify-content: space-between; align-items: center; padding: 14px 0; }
  .logo { font-family: var(--serif); font-weight: 800; font-size: 1.25rem; text-decoration: none; color: var(--ink);
          border: 2px solid var(--ink); border-radius: 50%; width: 42px; height: 42px; display: grid; place-items: center; }
  nav ul { display: flex; gap: 22px; list-style: none; }
  nav ul a { color: var(--muted); text-decoration: none; font-weight: 500; font-size: .95rem; }
  nav ul a:hover { color: var(--accent); }

  /* Hero */
  .hero { display: grid; grid-template-columns: 1.1fr 1fr; gap: 48px; align-items: center; padding: 88px 0 72px; }
  .hero h1 { font-family: var(--serif); font-weight: 800; font-size: clamp(2.8rem, 7vw, 4.6rem); line-height: 1.05; letter-spacing: -.01em; }
  .hero p.role { margin: 18px 0 28px; font-size: 1.15rem; color: var(--muted); max-width: 30em; }
  .btns { display: flex; gap: 12px; flex-wrap: wrap; }
  .btn { display: inline-block; padding: 12px 22px; border-radius: 6px; font-weight: 700; text-decoration: none; border: 2px solid var(--ink); }
  .btn.primary { background: var(--ink); color: #fff; }
  .btn.primary:hover { background: var(--accent); border-color: var(--accent); }
  .btn.ghost { color: var(--ink); }
  .btn.ghost:hover { background: var(--ink); color: #fff; }

  .code { background: #1b1e27; color: #d6dae6; border-radius: 10px; font-family: var(--mono); font-size: .88rem;
          padding: 22px 24px; line-height: 1.8; overflow-x: auto; box-shadow: 8px 8px 0 var(--accent); }
  .code .k { color: #8fa2ff; } .code .t { color: #7fd6c2; } .code .s { color: #f2c27b; } .code .c { color: #727a90; }

  /* Sections */
  section { padding: 64px 0; border-top: 1px solid var(--line); }
  h2 { font-family: var(--serif); font-size: 2rem; margin-bottom: 28px; }
  .about p { max-width: 42em; font-size: 1.1rem; }

  .skill-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 20px; }
  .skill-grid div { background: var(--paper); border: 1px solid var(--line); border-radius: 8px; padding: 22px; }
  .skill-grid h3 { font-size: 1rem; margin-bottom: 12px; }
  .chips { display: flex; flex-wrap: wrap; gap: 8px; list-style: none; }
  .chips li { font-family: var(--mono); font-size: .85rem; background: var(--bg); border: 1px solid var(--line); border-radius: 4px; padding: 3px 10px; }

  .projects { display: grid; gap: 20px; }
  .project { background: var(--paper); border: 1px solid var(--line); border-left: 5px solid var(--accent); border-radius: 8px; padding: 26px 28px; }
  .project h3 { font-family: var(--serif); font-size: 1.35rem; margin-bottom: 4px; }
  .project .stack { font-family: var(--mono); font-size: .82rem; color: var(--accent); margin-bottom: 12px; }
  .project ul { padding-left: 20px; color: var(--muted); }
  .project li { margin-bottom: 4px; }
  .project .links { margin-top: 14px; font-weight: 700; font-size: .95rem; display: flex; gap: 18px; }

  .edu { background: var(--paper); border: 1px solid var(--line); border-radius: 8px; padding: 26px 28px; max-width: 640px; }
  .edu h3 { font-size: 1.15rem; }
  .edu p { color: var(--muted); }
  .edu .gpa { margin-top: 10px; font-weight: 700; color: var(--ink); }
  .langs { margin-top: 20px; }

  .contact p { max-width: 36em; margin-bottom: 20px; font-size: 1.1rem; }
  .contact dl { display: grid; grid-template-columns: max-content 1fr; gap: 8px 22px; }
  .contact dt { font-weight: 700; }

  footer { border-top: 1px solid var(--line); padding: 26px 0; color: var(--muted); font-size: .9rem; }

  @media (max-width: 760px) {
    .hero { grid-template-columns: 1fr; padding: 56px 0 48px; }
    nav ul { gap: 14px; }
    nav ul a { font-size: .85rem; }
  }
  @media (prefers-reduced-motion: reduce) { html { scroll-behavior: auto; } }
</style>
</head>
<body>

<header>
  <div class="wrap">
    <nav aria-label="Main">
      <a class="logo" href="#top" aria-label="Back to top">RN</a>
      <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#education">Education</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </div>
</header>

<main id="top">
  <div class="wrap">

    <div class="hero">
      <div>
        <h1>Ranjani N</h1>
        <p class="role">Computer Science and Engineering student who builds user-friendly applications with Java and the web. Looking for an internship.</p>
        <div class="btns">
          <a class="btn primary" href="#projects">See my projects</a>
          <a class="btn ghost" href="#contact">Contact me</a>
        </div>
      </div>

      <pre class="code" aria-label="A short Java class describing Ranjani"><code><span class="k">public class</span> <span class="t">Ranjani</span> {
  <span class="t">String</span> degree  = <span class="s">"B.E. CSE"</span>;
  <span class="t">String</span> college = <span class="s">"JNN Institute of Engineering"</span>;
  <span class="t">String</span>[] skills = {<span class="s">"Java"</span>, <span class="s">"HTML"</span>, <span class="s">"CSS"</span>};
  <span class="t">boolean</span> seekingInternship = <span class="k">true</span>;

  <span class="c">// always learning</span>
  <span class="k">void</span> learn() { }
}</code></pre>
    </div>

    <section id="about" class="about">
      <h2>About me</h2>
      <p>I am a Computer Science and Engineering student with a strong foundation in Java and web development. I enjoy learning new technologies, solving real-world problems, and building user-friendly applications. I am looking for an internship where I can grow my technical skills and gain practical industry experience.</p>
    </section>

    <section id="skills">
      <h2>Skills</h2>
      <div class="skill-grid">
        <div>
          <h3>Programming languages</h3>
          <ul class="chips"><li>Java</li><li>C</li><li>C++</li></ul>
        </div>
        <div>
          <h3>Web technologies</h3>
          <ul class="chips"><li>HTML</li><li>CSS</li></ul>
        </div>
        <div>
          <h3>Tools</h3>
          <ul class="chips"><li>VS Code</li><li>GitHub</li></ul>
        </div>
      </div>
    </section>

    <section id="projects">
      <h2>Projects</h2>
      <div class="projects">

        <article class="project">
          <h3>Personal Portfolio Website</h3>
          <p class="stack">HTML, CSS</p>
          <ul>
            <li>Designed and developed a responsive personal portfolio website.</li>
            <li>Showcased personal profile, skills, education, and project details.</li>
            <li>Focused on clean UI and mobile-friendly design.</li>
          </ul>
          <!-- TODO: replace # with your GitHub repo link -->
          <div class="links"><a href="#">View code</a></div>
        </article>

        <article class="project">
          <h3>Calculator Application</h3>
          <p class="stack">Java</p>
          <ul>
            <li>Built a simple calculator using Java.</li>
            <li>Performed basic arithmetic operations: addition, subtraction, multiplication, and division.</li>
            <li>Improved understanding of Java methods and control statements.</li>
          </ul>
          <!-- TODO: replace # with your GitHub repo link -->
          <div class="links"><a href="#">View code</a></div>
        </article>

        <article class="project">
          <h3>Sign Up Page</h3>
          <p class="stack">HTML, CSS</p>
          <ul>
            <li>Designed and developed a responsive Sign Up page.</li>
            <li>Created a clean, user-friendly interface with input fields and form validation elements.</li>
            <li>Improved front-end design and layout using CSS styling.</li>
          </ul>
          <!-- TODO: replace # with your GitHub repo link -->
          <div class="links"><a href="#">View code</a></div>
        </article>

      </div>
    </section>

    <section id="education">
      <h2>Education</h2>
      <div class="edu">
        <h3>B.E. Computer Science and Engineering</h3>
        <p>JNN Institute of Engineering, 2025 to 2029</p>
        <p class="gpa">CGPA: 8.9 (First Year)</p>
      </div>
      <div class="langs">
        <h3>Languages</h3>
        <ul class="chips" style="margin-top:10px"><li>Tamil</li><li>English</li></ul>
      </div>
    </section>

    <section id="contact" class="contact">
      <h2>Contact</h2>
      <p>I am open to internship opportunities. Send me a message and I will get back to you.</p>
      <dl>
        <dt>Email</dt><dd><a href="mailto:nranjani523@gmail.com">nranjani523@gmail.com</a></dd>
        <dt>Phone</dt><dd><a href="tel:+917604951562">7604951562</a></dd>
        <dt>LinkedIn</dt><dd><a href="https://www.linkedin.com/in/ranjani-n17" target="_blank" rel="noopener">linkedin.com/in/ranjani-n17</a></dd>
        <dt>Location</dt><dd>Chennai, Tamil Nadu</dd>
      </dl>
    </section>

  </div>
</main>

<footer>
  <div class="wrap">&copy; 2026 Ranjani N</div>
</footer>

</body>
</html>
