<template>
  <div class="skill-bar">
    <div class="skill-info">
   <div class="label">
        <i v-if="skill.iconClass" :class="skill.iconClass"></i>
        <!-- <img v-if="skill.icon" :src="skill.icon" :alt="skill.name" /> -->
        <span>{{ skill.name }}</span>
      </div>
      <span>{{ skill.level }}%</span>
    </div>
    <div class="bar-bg">
      <div class="bar-fill" :style="{ width: skill.level + '%' }"></div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  skill: Object
})
</script>

<style scoped lang="scss">
@import '@/assets/styles/variables';

.skill-bar {
  margin-bottom: 1.2rem;

  .skill-info {
    display: flex;
    justify-content: space-between;
    font-weight: 600;
    color: $dark-color;
    margin-bottom: 0.25rem;

    .label {
  display: flex;
  align-items: center;
  gap: 0.5rem;

  i {
    font-size: 1.5rem;
  }
}   
  }

  .bar-bg {
    width: 100%;
    height: 12px;
    background-color: transparentize($primary-color,.9);
    border-radius: 9999px;
    overflow: hidden;
    // height:20px
  }

  .bar-fill {
    height: 100%;
    background: $primary-color;
    border-radius: 9999px;
    transition: width 0.5s ease;
  }
}
</style>
