<template>
  <div class="project-card" @click="goToProject">
    <img :src="project.path" :alt="project.title" />
    <h3>{{ project.title }}</h3>
    <p>{{ project.short }}</p>
  </div>
</template>

<script setup>
import { useRouter } from 'vue-router'
const props = defineProps({ project: Object })

const router = useRouter()
function goToProject() {
  console.log('hello');
  router.push(`/projects/${props.project.slug}`)
}
</script>

<style scoped lang="scss">
@import "@/assets/styles/variables";

.project-card {
  cursor: pointer;
  border-radius: 1rem;
  overflow: hidden;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.06);
  transition: transform 0.3s;

  &:hover {
    transform: translateY(-4px);
  }

  img {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }

  h3 {
    font-size: 1.25rem;
    padding: 1rem;
    margin: 0;
    color: $dark-color;
  }

  p {
    padding: 0 1rem 1rem;
    color: #666;
  }
}
</style>
