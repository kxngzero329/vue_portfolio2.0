<template>
  <section class="hero" ref="hero">
    <div class="overlay">
      <div class="content">
        <h1 class="name">Hey! I'm <span class="highlight">Mogamat Smith</span></h1>
        <h2 class="title">
          <span id="typingText" class="typed-text"></span><span class="cursor">|</span>
        </h2>
        <h3>I create <span class="highlight">responsive websites</span> and <span class="highlight">powerful
            digital</span> solutions that makes a difference.</h3>
        <a href="#about" class="btn">Learn More</a>
      </div>
    </div>
  </section>

  <!-- About -->
  <section id="about" class="about-section" ref="about">
    <div class="about-container">
      <!-- Left: Profile Image -->
      <div class="about-left">
        <img src="../assets/smith.jpg" alt="Mogamat Smith" class="profile-img" />
      </div>

      <!-- Right: About Content -->
      <div class="about-right">
        <h2>About Me</h2>
        <p>
          I'm <strong>Mogamat Smith</strong>, a passionate and driven junior web developer based in Cape Town.
          I specialize in building clean, responsive, and modern websites using technologies like HTML, CSS,
          JavaScript, and frameworks like Vue.js. I love solving problems, learning new things, and bringing ideas
          to life through code.
        </p>
        <p>
          I completed a Web Development course at CodeSpace in 2023, followed by MSiTA Web Dev at College of Cape Town
          in 2024,
          and I’m currently enrolled in the Software Development program at LifeChoices Academy.
        </p>

        <h2>Details</h2>
        <p><strong>Name:</strong> Mogamat Smith</p>
        <p><strong>Email:</strong> <a href="mailto:suhairsmith17@gmail.com" class="email">suhairsmith17@gmail.com</a>
        </p>
        <p><strong>Location:</strong> Cape Town, South Africa</p>

        <div class="about-icons">
          <a href="https://www.linkedin.com/in/suhair-smith-kxngzero329/" target="_blank">
            <i class="fab fa-linkedin-in"></i>
          </a>
          <a href="https://github.com/kxngzero329" target="_blank">
            <i class="fab fa-github"></i>
          </a>
        </div>
      </div>
    </div>
  </section>


  <!-- Education & Experience Timeline -->
  <section id="timeline" class="timeline-section" ref="timeline">
    <h2 class="section-title">Education & Experience</h2>
    <div class="timeline-container">

      <!-- Timeline Item -->
      <div class="timeline-item">
        <div class="timeline-icon education">
          <i class="fas fa-graduation-cap"></i>
        </div>
        <div class="timeline-content">
          <span class="timeline-date">2021</span>
          <h3>Matric - Bachelor's Pass</h3>
          <p>Graduated from high school with a Bachelor's pass.</p>
        </div>
      </div>

      <div class="timeline-item">
        <div class="timeline-icon education">
          <i class="fas fa-laptop-code"></i>
        </div>
        <div class="timeline-content">
          <span class="timeline-date">2023</span>
          <h3>CodeSpace – Web Development</h3>
          <p>Completed a full-stack web dev bootcamp with hands-on HTML, CSS, JS, and Git.</p>
        </div>
      </div>

      <div class="timeline-item">
        <div class="timeline-icon education">
          <i class="fas fa-code"></i>
        </div>
        <div class="timeline-content">
          <span class="timeline-date">2024</span>
          <h3>College of Cape Town – MSiTA Web Dev</h3>
          <p>Focused on Microsoft web development technologies including C# and ASP.NET.</p>
        </div>
      </div>

      <div class="timeline-item">
        <div class="timeline-icon education">
          <i class="fas fa-school"></i>
        </div>
        <div class="timeline-content">
          <span class="timeline-date">2025</span>
          <h3>LifeChoices Academy – Software Dev</h3>
          <p>Currently enrolled in software development covering full-stack dev, UX, and more.</p>
        </div>
      </div>
    </div>
  </section>
  <!-- End -->

  <!-- Skills -->
  <section id="skills" class="skills-section" ref="skills">
    <h2 class="section-title" data-aos="fade-up">Skills</h2>
    <div class="skills-container">

      <div class="skill" v-for="skill in skills" :key="skill.name" data-aos="fade-right">
        <div class="skill-header">
          <i :class="skill.icon"></i>
          <span>{{ skill.name }}</span>
          <span class="percentage">{{ skill.level }}%</span>
        </div>
        <div class="progress-bar">
          <div class="progress-fill" :style="{ width: skill.level + '%' }"></div>
        </div>
      </div>

    </div>
  </section>
  <!-- End -->


  <!-- Projects -->
  <section id="projects" class="projects-section" ref="projects">
    <div class="container">
      <h2 data-aos="fade-up">Projects</h2>
      <div class="projects-grid">
        <div class="project-card" v-for="(project, index) in projects" :key="index">
          <img :src="project.image" alt="Project image" />
          <div class="project-info">
            <h3>{{ project.title }}</h3>
            <p>{{ project.description }}</p>
          </div>
          <div class="project-overlay">
            <a :href="project.link" target="_blank" class="view-btn">View Project</a>
          </div>
        </div>
      </div>
    </div>
  </section>


  <!-- End -->

  <!-- Contact -->
  <section id="contact" class="contact-section" ref="contact">
    <h2 class="main-section-title">Contact</h2>
    <div class="contact-card">
      <!-- Left Side -->
      <div class="contact-left">
        <h5 class="card-title">Get in Touch</h5>
        <ul class="contact-info">
          <li><i class="fas fa-envelope"></i> <a href="mailto:suhairsmith17@gmail.com">Email Me</a></li>
          <li><i class="fas fa-phone"></i> <a href="tel:+27747862736">Phone</a></li>
          <li><i class="fas fa-map-marker-alt"></i> Cape Town, South Africa</li>
          <li><i class="fab fa-whatsapp"></i> <a href="https://wa.me/+27747862736" target="_blank">Message Me</a></li>
        </ul>
      </div>

      <!-- Right Side -->
      <div class="contact-right">
        <h5 class="card-title">Send a Message</h5>
        <form method="POST" action="https://api.web3forms.com/submit">
          <input type="hidden" name="access_key" value="b3307c26-c802-4c0c-979e-8b5d26d64afa" />

          <label>Name</label>
          <input type="text" name="name" placeholder="Your Name" required />

          <label>Email</label>
          <input type="email" name="email" placeholder="Your Email" required />

          <label>Message</label>
          <textarea name="message" rows="5" placeholder="Your Message" required></textarea>

          <button type="submit">Send Message</button>
        </form>

      </div>
    </div>
  </section>

  <!-- End -->

  <!-- footer -->

  <!-- Footer Section -->
  <footer class="footer-section">
    <div class="footer-content">
      <p>&copy; {{ new Date().getFullYear() }} Mogamat Smith. All rights reserved.</p>
      <div class="footer-icons">
        <a href="https://www.linkedin.com/in/suhair-smith-kxngzero329/" target="_blank">
          <i class="fab fa-linkedin-in"></i>
        </a>
        <a href="https://github.com/kxngzero329" target="_blank">
          <i class="fab fa-github"></i>
        </a>
        <!-- instagram -->
        <a href="https://www.instagram.com/officialsmithson18?igsh=MXJid2FwejRhdjhpMg==" target="_blank">
          <i class="fab fa-instagram"></i>
        </a>
        <!-- tiktok -->
        <a href="https://www.tiktok.com/@officialsmithson18?is_from_webapp=1&sender_device=pc" target="_blank">
          <i class="fab fa-tiktok"></i>
        </a>
      </div>
    </div>
  </footer>

  <!-- end -->
</template>

<script>
export default {
  name: "Home",
  emits: ['updateSection'],

  data() {
    return {
      skills: [
        { name: "HTML", level: 96, icon: "fab fa-html5" },
        { name: "CSS", level: 94, icon: "fab fa-css3-alt" },
        { name: "JavaScript", level: 94, icon: "fab fa-js-square" },
        { name: "React.js", level: 92, icon: "fab fa-react" },
        { name: "Bootstrap", level: 95, icon: "fab fa-bootstrap" },
        { name: "Vue.js", level: 92, icon: "fab fa-vuejs" },
        { name: "PHP", level: 93, icon: "fab fa-php" },
        { name: "MySQL", level: 94, icon: "fas fa-database" },
        { name: "C#", level: 86, icon: "fas fa-code" },
        { name: "Python", level: 97, icon: "fab fa-python" },
        { name: "Photoshop", level: 92, icon: "fas fa-image" },
        { name: "Figma", level: 92, icon: "fab fa-figma" },
      ],
      projects: [
        {
          image: require('../assets/lyrics.png'),
          title: "Lyric Snatcher",
          description: "Online Lyric Search Engine.",
          link: "https://lyric-snatcher-by-msmith.netlify.app/",
        },
        {
          image: require('../assets/client1.png'),
          title: "Beauty By Geraldine",
          description: "Online Nail Specialist.",
          link: "https://beauty-by-geraldine.netlify.app/",
        },
        {
          image: require('../assets/mts.png'),
          title: "ModernTech Solutions",
          description: "HR Management System. (Vue.js)",
          link: "https://mtshr.netlify.app/#/login",
        },
        {
          image: require('../assets/sky-seeker.png'),
          title: "Sky Seeker",
          description: "Simple Weather Website.",
          link: "https://sky-seeker-a2bda1.netlify.app/",
        },
        {
          image: require('../assets/podhut.png'),
          title: "Pod Hut",
          description: "Podcast App. (React.js)",
          link: "https://pod-hut-kxngzero.netlify.app/",
        },
        {
          image: require('../assets/book.png'),
          title: "Book Connect",
          description: "Online Book Library. (Javascript, API)",
          link: "https://book-connect-by-msmith.netlify.app/",
        },
      ]
    };
  },

  mounted() {
    // Typing animation
    const texts = ["Creative thinker", "Web developer", "Web designer"];
    const typingElement = document.getElementById("typingText");
    const cursor = document.querySelector(".cursor");

    let charIndex = 0;
    let textIndex = 0;
    let isDeleting = false;

    function type() {
      const currentText = texts[textIndex];
      if (!isDeleting) {
        typingElement.textContent = currentText.substring(0, charIndex + 1);
        charIndex++;
        if (charIndex === currentText.length) {
          isDeleting = true;
          setTimeout(type, 1200);
        } else {
          setTimeout(type, 100);
        }
      } else {
        typingElement.textContent = currentText.substring(0, charIndex - 1);
        charIndex--;
        if (charIndex === 0) {
          isDeleting = false;
          textIndex = (textIndex + 1) % texts.length;
          setTimeout(type, 300);
        } else {
          setTimeout(type, 60);
        }
      }
    }

    type();

    // Scrollspy listener
    window.addEventListener("scroll", this.onScroll);
  },

  beforeUnmount() {
    window.removeEventListener("scroll", this.onScroll);
  },

  methods: {
    onScroll() {
      const sections = ['about', 'timeline', 'skills', 'projects', 'contact'];
      for (const id of sections) {
        const el = this.$refs[id];
        if (el) {
          const rect = el.getBoundingClientRect();
          if (rect.top <= 120 && rect.bottom >= 120) {
            this.$emit('updateSection', id);
            break;
          }
        }
      }
    }
  }
};
</script>


<style scoped>
/* hero section start */
.hero {
  height: 100vh;
  background-image: url('https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=1470&q=80');
  /* Replace with your image */
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}

.overlay {
  backdrop-filter: blur(5px);
  background: rgba(0, 0, 0, 0.68);
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.content {
  text-align: center;
  color: #f8f8f8;
  text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.8);
}

.name {
  font-size: 3rem;
  font-weight: bold;
  font-family: 'Playfair Display', serif;
  text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.8);
}

.title {
  font-size: 1.8rem !important;
  margin-top: 25px;
  margin-bottom: 25px;
  letter-spacing: 1px;
  text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.8);

}

.highlight {
  color: #488ded;
  /* frosted blue accent */

}

h3 {
  font-family: 'Inter', sans-serif;
  text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.8);
  font-size: 1.2rem !important;
}

.typed-text {
  color: #e8f8ff;
  /* frosted blue accent */
  font-weight: 600;
  font-family: 'JetBrains Mono', monospace !important;
}

.cursor {
  display: inline-block;
  width: 1px;
  background: #00aeff;
  animation: blink 0.7s steps(2, start) infinite;
}

.btn {
  margin-top: 15px;
  border: 1px solid #00aeff !important;
  background-color: transparent !important;
  padding: 10px 30px !important;
  color: #00aeff;
  font-weight: 600;
  border-radius: 20px;
  transition: 0.3s ease;
}

.btn:hover {
  background: linear-gradient(45deg, #00205a, #00aeff, #002a3d) !important;
  border: 1px solid #0059ff !important;
  color: #000000 !important;
  box-shadow: 0 0 8px rgba(140, 242, 255, 0.736);
  border-bottom-left-radius: 0 !important;
  border-top-right-radius: 0 !important;
}

@keyframes blink {
  to {
    visibility: hidden;
  }
}

/* hero section end */

/* about section start */
.about-section {
  padding: 100px 20px;
  background: #0e1018;
  color: #ffffff;
}

.about-container {
  display: flex;
  max-width: 1200px;
  margin: auto;
  align-items: flex-start;
  gap: 60px;
  flex-wrap: wrap;
}

.about-left {
  flex: 1 1 300px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.profile-img {
  margin-top: 100px;
  width: 100%;
  max-width: 280px;
  height: 280px;
  border-radius: 20px;
  object-fit: cover;
  border: none;
  box-shadow: 0 0 20px rgba(0, 187, 212, 0.736);
}

.about-right {
  flex: 1 1 600px;
}

.about-right h2 {
  font-size: 2rem;
  margin-bottom: 20px;
  color: #c2e9fb;
  font-family: 'Playfair Display', serif;
}

.about-right p {
  font-size: 1.1rem;
  margin-bottom: 16px;
  line-height: 1.6;
}

.email {
  color: #ffffff;
  text-decoration: none;
  transition: color 0.3s;
}

.email:hover {
  color: #2578dd;
}

.about-icons a {
  color: #f0f0f0;
  margin: 0 10px;
  font-size: 24px;
  transition: transform 0.3s ease, color 0.3s ease;
}

.about-icons a:hover {
  color: #00bcd4;
  transform: scale(1.2);
}

/* Responsive */
@media (max-width: 768px) {
  .about-container {
    flex-direction: column;
    text-align: center;
    gap: 40px;
  }

  .about-right h2 {
    text-align: center;
  }

  .about-left {
    order: -1;
  }
}

/* about section end */

/* timeline */
.timeline-section {
  padding: 5rem 2rem;
  background: #0f2027;
  color: #e0f7fa;
}

.section-title {
  text-align: center;
  font-size: 2.2rem;
  margin-bottom: 3rem;
  color: #c2e9fb;
}

.timeline-container {
  position: relative;
  max-width: 50%;
  margin: auto;
  padding-left: 20px;
  border-left: 3px solid #4fc3f7;
}

.timeline-item {
  position: relative;
  margin-bottom: 3rem;
  padding-left: 2rem;
}

.timeline-icon {
  position: absolute;
  left: -18px;
  top: 0;
  background: #4fc3f7;
  color: #fff;
  width: 32px;
  height: 32px;
  border-radius: 50%;
  border: 4px double #4fc3f7;
  ;
  display: flex;
  align-items: center;
  justify-content: center;
}

.timeline-date {
  font-size: 0.9rem;
  color: #81d4fa;
}

.timeline-content h3 {
  margin: 0.3rem 0;
  font-size: 1.2rem;
  color: #ffffff;
}

.timeline-content p {
  margin: 0;
  font-size: 0.95rem;
  color: #cfd8dc;
}

/* timeline end */

/* skills */
.skills-section {
  padding: 4rem 2rem;
  background: #0e1018;

}

.section-title {
  text-align: center;
  font-size: 2.2rem;
  color: #c2e9fb;
  margin-bottom: 2rem;
  font-family: 'Playfair Display', serif;
}

.skills-container {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  max-width: 900px;
  margin: 0 auto;
}

.skill {
  width: 100%;
}

.skill-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #e3f3fd;
  font-weight: 500;
  margin-bottom: 6px;
  font-size: 1rem;
}

.skill-header i {
  font-size: 1.2rem;
  margin-right: 0.5rem;
  color: #8fd3f4;
}

.progress-bar {
  background-color: #2c3e50;
  border-radius: 50px;
  height: 10px;
  overflow: hidden;
}

.progress-fill {
  height: 100%;
  background: linear-gradient(90deg, #8fd3f4, #84fab0);
  width: 0%;
  border-radius: 50px;
  animation: fill 2s forwards;
}

@keyframes fill {
  from {
    width: 0%;
  }
}

/* skills end */

/* projects */
.projects-section {
  background: #0f2027;
  color: #fff;
  padding: 60px 20px;
}

.projects-section h2 {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 40px;
  color: #c2e9fb;
  font-family: 'Playfair Display', serif;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 30px;
}

.project-card {
  position: relative;
  overflow: hidden;
  border-radius: 20px;
  background: #1a1a1a;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
}

.project-card img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  display: block;
  border-radius: 20px 20px 0 0;
}

.project-info {
  padding: 20px;
}

.project-info h3 {
  margin: 0;
  font-size: 1.4rem;
  color: #fff;
}

.project-info p {
  margin-top: 10px;
  color: #bbb;
  font-size: 0.95rem;
}

.project-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  backdrop-filter: blur(6px);
  background-color: rgba(0, 0, 0, 0.753);
  opacity: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: opacity 0.4s ease;
  border-radius: 20px;
}

.project-card:hover .project-overlay {
  opacity: 1;
}

.project-overlay a {
  text-decoration: none;
}

.view-btn {
  padding: 10px 20px;
  background: #c2e9fb;
  border: none;
  border-radius: 30px;
  color: #06122c;
  font-weight: bold;
  cursor: pointer;
  transition: 0.3s ease;
  box-shadow: 0 0 20px #50c8ff;
  font-family: 'Inter', sans-serif;
}

.view-btn:hover {
  background: #0a1750;
  box-shadow: 0 0 20px #5070ff;
  color: #c2e9fb;
}

/* projects end */


/* contact */
.contact-section {
  padding: 60px 20px;
  background-color: #0e1018;
}

.main-section-title {
  text-align: center;
  margin-bottom: 30px;
  font-size: 2.5rem;
  font-family: 'Playfair Display', serif;
  color: #8fd3f4;
}

.contact-card {
  display: flex;
  background: #f8f8f8;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  flex-wrap: wrap;
  max-width: 980px;
  max-height: 560px;
  margin: 0 auto;
}

.contact-left {
  background-color: #0f2027;
  color: white;
  flex: 1;
  padding: 40px 30px;
  min-width: 300px;
}

.contact-left .card-title {
  font-size: 1.8rem;
  margin-bottom: 25px;
}

.contact-info {
  list-style: none;
  padding: 0;
}

.contact-info li {
  margin-bottom: 20px;
  font-size: 1.1rem;
}

.contact-info i {
  margin-right: 10px;
}

.contact-info a {
  color: white;
  text-decoration: none;
  font-weight: 500;
}

.contact-info a:hover {
  color: #8fd3f4;
}

.contact-right {
  flex: 1;
  padding: 40px 30px;
  min-width: 300px;
}

.contact-right .card-title {
  font-size: 1.8rem;
  margin-bottom: 25px;

}

.card-title {
  font-family: 'Playfair Display', serif;
}

.contact-right form {
  display: flex;
  flex-direction: column;
}

.contact-right label {
  margin-bottom: 5px;
  font-weight: 500;
}

.contact-right input,
.contact-right textarea {
  padding: 12px;
  margin-bottom: 20px;
  border-radius: 10px;
  border: 1px solid #ccc;
  background-color: #f9f9f9;
  font-size: 1rem;
}

.contact-right button {
  background-color: #007bff;
  color: white;
  padding: 14px;
  border: none;
  border-radius: 30px;
  font-size: 1rem;
  cursor: pointer;
  transition: 0.3s ease;
}

.contact-right button:hover {
  background-color: #092653;
  transform: translateY(-2px);
}

.contact-right input:focus,
.contact-right textarea:focus {
  outline: none;
  border-color: #007bff;
  box-shadow: 0 0 5px rgba(0, 123, 255, 0.5);
}

@media (max-width: 768px) {
  .contact-card {
    flex-direction: column;
  }
}

/* contact end */

/* footer */
.footer-section {
  background-color: #0f2027;
  /* dark frosted tone */
  color: #f0f0f0;
  padding: 40px 20px;
  text-align: center;
  font-family: 'Inter', sans-serif;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
}

.footer-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 15px;
}

.footer-icons a {
  color: #f0f0f0;
  margin: 0 10px;
  font-size: 24px;
  transition: transform 0.3s ease, color 0.3s ease;
}

.footer-icons a:hover {
  color: #00bcd4;
  transform: scale(1.2);
}
</style>
