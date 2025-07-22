<template>
  <section class="project-detail" v-if="project">
    <h1>{{ project.title }}</h1>
    <p>{{ project.description }}</p>
    <div class="images">
      <img v-for="(img, i) in project.images" :key="i" :src="img" />
    </div>
  </section>
</template>

<script setup>
import { useRoute } from 'vue-router'
import { computed } from 'vue'

const route = useRoute()

const projects = {
  'portfolio-site': {
    title: 'Portfolio Website',
    description: 'A modern responsive portfolio site with Vue 3, Vite, and SCSS.',
    images: [
      '/images/portfolio/1.png',
      '/images/portfolio/2.png',
      '/images/portfolio/3.png',
      '/images/portfolio/4.png',
      '/images/portfolio/5.png',
      '/images/portfolio/6.png',
    ]
  },
  'ServiceSystem-app': {
    title: 'ServiceSystem-app',
    description: 'A dashboard with charts, filters, and user stats.',
    images: [
      '/images/SSystem/sys1.png',
      '/images/SSystem/sys4.png',
      '/images/SSystem/sys5.png',
      '/images/SSystem/sys2.png',
      '/images/SSystem/sys3.png',
    ]
  },
  'states-site': {
    title: 'states-site',
    description: 'detentions states by wibsite , fast and secure',
    images: [
      '/images/states/2.png',
      '/images/states/3.png',
      '/images/states/4.png',
      '/images/states/5.png',
      '/images/states/7.png',
    ]
  },
  'gym': {
    title: 'gym-site',
    description: 'subscribing in gym and trainee  by website also coaches and employees',
    images: [
      '/images/gym/1.png',
      '/images/gym/2.png',
      '/images/gym/3.png',
      '/images/gym/4.png',
      '/images/gym/5.png',
      '/images/gym/6.png',
    ]
  }
}

const project = computed(() => projects[route.params.slug])
</script>

<style scoped lang="scss">
.project-detail {
  padding: 3rem 1rem;
  max-width: 900px;
  margin: auto;

  h1 {
    font-size: 2rem;
    color: $dark-color;
  }

  p {
    font-size: 1.1rem;
    margin-bottom: 2rem;
  }

  .images {
    display: flex;
    flex-direction: column;
    gap: 1rem;

    img {
      width: 100%;
      border-radius: 1rem;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.08);
    }
  }
}
</style>
