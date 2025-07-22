<template>
  <section class="hero">
    <div class="overlay">
      <div class="content">
        <h1>Hi, I'm <span class="highlight">Omran Alkelani</span></h1>
        <p class="subtitle">
          Full Stack Developer — Vue, Laravel, React, Tailwind
        </p>
        <router-link to="/projects" class="cta">View My Projects</router-link>
      </div>
    </div>
  </section>
</template>

<script setup>
// Optional: global import in main.js already covers this
import 'animate.css'
</script>

<style scoped lang="scss">
@import '@/assets/styles/variables';

.hero {
  position: relative;
  background-image: url('/images/home.png'); 
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;

  .overlay {
    background-color: rgba(0, 0, 0, 0.6); // 👈 adjust opacity here (0.5–0.7 recommended)
    width: 100%;
    height: 100%;
    padding: 4rem 1rem;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
  }

  .content {
    max-width: 800px;
    margin: auto;
  }

  h1 {
    font-size: 3rem;
    font-weight: 800;

    .highlight {
      color: $primary-color;
    }
  }

  .subtitle {
    font-size: 1.25rem;
    margin: 1.5rem 0;
    color: #f3f4f6;
  }

  .cta {
    background: $primary-color;
    color: white;
    padding: 0.75rem 1.5rem;
    border-radius: 9999px;
    font-weight: 600;
    text-decoration: none;
    transition: background 0.3s;

    &:hover {
      background: darken($primary-color, 10%);
    }
  }
}

</style>
