<template>
  <main class="about-page">
    <section class="intro animate__animated animate__fadeInUp">
      <h1>Omran Alkelani</h1>
      <p>Full Stack Developer — 2+ years experience</p>
      <p class="location"> Damascus, Syria</p>
    </section>

    <section class="summary">
      <h2>Summary</h2>
      <p>
        I am a full stack developer with 2 years of experience. I have worked with both Syrian and Iraqi companies
        (Fullstack & Frontend). I specialize in building secure, efficient single-page apps and REST APIs. I analyze small to mid-scale projects such as e-commerce and educational systems.
      </p>
    </section>

    <section class="experience">
      <h2>Experience</h2>
      <ul>
        <li> 1 year as Fullstack developer (Syrian company)</li>
        <li> 9 months as Frontend developer (Iraqi company)</li>
      </ul>
    </section>

    <section class="skills">
      <h2>Skills</h2>
      <div class="tags">
        <span>HTML/CSS</span>
        <span>JavaScript</span>
        <span>TypeScript</span>
        <span>Vue.js / Vuetify</span>
        <span>React / Ant Design</span>
        <span>PHP / Laravel</span>
        <span>Flutter</span>
        <span>SASS / Tailwind</span>
        <span>MySQL / SQL</span>
        <span>Authentication / Authorization</span>
        <span>REST APIs</span>
        <span>Project Analysis</span>
      </div>
    </section>

    <section class="education">
      <h2>Education</h2>
      <ul>
        <li> High School – Damascus</li>
        <li> Technical Institute for Computer Science</li>
        <li> Applied College – Computer Science</li>
        <li> Computer Technics University</li>
      </ul>
    </section>

    <section class="projects">
      <h2>Projects</h2>
      <ul>
        <li> School Management System</li>
        <li> E-commerce App</li>
        <li> ERP Module Participation</li>
        <li> Services Marketplace</li>
      </ul>
    </section>
    <section class="download">
  <a
    href="/OmranAlkelani.pdf"
    download
    class="download-btn"
    target="_blank"
    rel="noopener"
  >
     Download My CV
  </a>
</section>
  </main>
</template>

<script setup>
// Optional: import animate.css
import 'animate.css'
</script>

<style scoped lang="scss">
@import '@/assets/styles/variables';

.download-btn {
  display: inline-block;
  margin-top: 1rem;
  background: $primary-color;
  color: white;
  padding: 0.75rem 1.5rem;
  border-radius: 9999px;
  text-decoration: none;
  font-weight: 600;
  transition: background 0.3s;

  &:hover {
    background: darken($primary-color, 10%);
  }
}

.about-page {
  padding: 3rem 2rem;
  max-width: 900px;
  margin: auto;
  color: $dark-color;

  h1 {
    font-size: 2.5rem;
    color: $primary-color;
    margin-bottom: 0.25rem;
  }

  .location {
    color: #666;
    margin-top: 0.5rem;
  }

  section {
    margin-bottom: 2.5rem;

    h2 {
      font-size: 1.5rem;
      margin-bottom: 1rem;
      color: $primary-color;
    }

    p, li {
      font-size: 1rem;
      line-height: 1.6;
    }

    ul {
      list-style: none;
      padding-left: 0;

      li {
        margin-bottom: 0.5rem;
      }
    }

    .tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;

      span {
        background: lighten($primary-color, 30%);
        color: $primary-color;
        font-weight: 600;
        padding: 0.5rem 1rem;
        border-radius: 999px;
        font-size: 0.9rem;
      }
    }
  }
}
</style>
