<template>
  <section class="projects">
    <h1>My Projects</h1>
    <div class="grid">
      <ProjectCard v-for="project in projects" :key="project.slug" :project="project" />
    </div>
  </section>
</template>

<script setup>
import ProjectCard from '@/components/ProjectCard.vue'

const projects = [
  {
    slug: 'portfolio-site',
    title: 'Portfolio Website',
    short: ' build  portfolio for company  with Vue and Sass.',
    path: '/images/portfolio/1.png'
  },
  {
    slug: 'ServiceSystem-app',
    title: 'ServiceSystem-app',
    short: 'An admin dashboard with chart widgets.',
    path: '/images/SSystem/sys1.png'
  },
  {
    slug: 'states-site',
    title: 'states-site',
    short: 'detentions states by wibsite , fast and secure',
    path: '/images/states/2.png'
  }
  ,
  {
    slug: 'gym',
    title: 'gym',
    short: 'subscribing in gym and trainee  by website ',
    path: '/images/gym/1.png'
  }
]
</script>

<style scoped lang="scss">
.projects {
  padding: 3rem 1rem;
  max-width: 1200px;
  margin: auto;

  h1 {
    text-align: center;
    font-size: 2rem;
    margin-bottom: 2rem;
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 2rem;
  }
}
</style>
