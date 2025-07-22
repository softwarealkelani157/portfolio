<template>
<div class="home">

    <Hero/>
    <section class="about-preview animate__animated animate__fadeInUp">
      <div class="content">
        <h2>About Me</h2>
        <p>
          I’m Omran Alkelani — a full stack developer with 2+ years of experience building modern, secure,
          and scalable web applications. I’ve worked with Vue, Laravel, React, and more to deliver
          high-performance solutions.
        </p>
        <router-link to="/about" class="about-btn">Learn more about me →</router-link>
      </div>
    </section>
</div>
</template>
<script setup>
import Hero from '@/components/Hero.vue'
import 'animate.css'
</script>

<style scoped lang="scss">
@import '@/assets/styles/variables';

.home {
  .about-preview {
    padding: 4rem 1rem;
    background-color: #f9fafb;

    .content {
      max-width: 800px;
      margin: auto;
      text-align: center;

      h2 {
        font-size: 2rem;
        margin-bottom: 1rem;
        color: $primary-color;
      }

      p {
        font-size: 1.1rem;
        color: #444;
        line-height: 1.6;
        margin-bottom: 1.5rem;
      }

      .about-btn {
        display: inline-block;
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
  }
}
</style>