<template>
  <main class="skills-page">
    <h1>My Skills</h1>
    <div class="skills-list">
      <SkillBar v-for="skill in skills" :key="skill.name" :skill="skill" />
    </div>
  </main>
</template>

<script setup>
import SkillBar from '@/components/SkillBar.vue'

const skills = [
 { name: 'JavaScript', level: 90, iconClass: 'devicon-javascript-plain colored' },
  { name: 'TypeScript', level: 80, iconClass: 'devicon-typescript-plain colored' },
  { name: 'Laravel', level: 80, iconClass: 'devicon-laravel-plain colored' },
  { name: 'Angular', level: 70, iconClass: 'devicon-angularjs-plain colored' },
  { name: 'React', level: 90, iconClass: 'devicon-react-original colored' },
  { name: 'Vue.js', level: 85, iconClass: 'devicon-vuejs-plain colored' },
  { name: 'MySQL', level: 90, iconClass: 'devicon-mysql-plain colored' },
  { name: 'Flutter', level: 70, iconClass: 'devicon-flutter-plain colored' },
  { name: 'Vuetify', level: 90, iconClass: 'devicon-vuejs-plain colored' }, // fallback: no Vuetify icon, using Vue
  { name: 'Tailwind CSS', level: 90, iconClass: 'devicon-tailwindcss-plain colored' },
  { name: 'Bootstrap', level: 90, iconClass: 'devicon-bootstrap-plain colored' },
  { name: 'HTML & CSS', level: 95, iconClass: 'devicon-html5-plain colored' },
  { name: 'Sass', level: 90, iconClass: 'devicon-sass-original colored' },
  { name: 'Git', level: 90, iconClass: 'devicon-git-plain colored' },
  { name: 'C#', level: 60, iconClass: 'devicon-csharp-plain colored' },
  { name: 'ASP.NET', level: 50, iconClass: 'devicon-dot-net-plain colored' },
  { name: 'Vuex', level: 90, iconClass: 'devicon-vuejs-plain colored' }, // fallback for Vuex
  { name: 'Redux', level: 90, iconClass: 'devicon-redux-original colored' },
  { name: 'Material UI', level: 90, iconClass: 'devicon-materialui-plain colored' }]
</script>

<style scoped lang="scss">
.skills-page {
  max-width: 1000px;
  margin: auto;
  padding: 1rem 2rem;

  h1 {
    text-align: center;
    margin-bottom: 2rem;
    color: $dark-color;
  }
   .skills-list {
    display: grid;
    gap: 1.5rem;

    grid-template-columns: repeat(1, 1fr); // default: mobile

    @media (min-width: 600px) {
      grid-template-columns: repeat(2, 1fr); // tablets
    }

    @media (min-width: 1024px) {
      grid-template-columns: repeat(3, 1fr); // laptops & desktops
    }
  }
}
</style>
