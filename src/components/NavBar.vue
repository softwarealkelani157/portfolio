<template>
  <header class="header">
    <div class="container">
      <div class="logo" @click="goHome"><img src="/images/logo.png" alt="logo" height="100"></div>
      <nav :class="{ open: mobileMenuOpen }">
        <router-link to="/" exact-active-class="active" @click="closeMenu">Home</router-link>
        <router-link to="/projects" exact-active-class="active" @click="closeMenu">Projects</router-link>
        <router-link to="/skills" exact-active-class="active" @click="closeMenu">Skills</router-link>
        <router-link to="/contact" exact-active-class="active" @click="closeMenu">Contact</router-link>
        <router-link to="/about" exact-active-class="active" @click="closeMenu">About</router-link>
      </nav>
      <button class="burger" @click="toggleMenu" aria-label="Toggle menu">
        <span></span><span></span><span></span>
      </button>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'
import { useRouter } from 'vue-router'

const mobileMenuOpen = ref(false)
const router = useRouter()

function toggleMenu() {
  mobileMenuOpen.value = !mobileMenuOpen.value
}

function closeMenu() {
  mobileMenuOpen.value = false
}

function goHome() {
  router.push('/')
  closeMenu()
}
</script>

<style scoped lang="scss">
@import '@/assets/styles/variables';

.header {
  background: white;
  box-shadow: 0 2px 10px rgb(0 0 0 / 0.05);
  position: sticky;
  top: 0;
  z-index: 100;
  font-weight: 600;

  .container {
    max-width: 1200px;
    margin: auto;
    padding: 0 1.5rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    align-items: center;
    height: 60px;
  }

  .logo {
    font-size: 1.5rem;
    color: $primary-color;
    cursor: pointer;
    user-select: none;
  }

  nav {
    display: flex;
    gap: 2rem;

    a {
      color: $dark-color;
      text-decoration: none;
      position: relative;
      transition: color 0.3s;

      &.active,
      &:hover {
        color: $primary-color;
      }

      &.active::after {
        content: '';
        position: absolute;
        bottom: -6px;
        left: 0;
        width: 100%;
        height: 3px;
        background-color: $primary-color;
        border-radius: 2px;
      }
    }
  }

  .burger {
    display: none;
    flex-direction: column;
    justify-content: space-around;
    width: 24px;
    height: 20px;
    background: transparent;
    border: none;
    cursor: pointer;
    padding: 0;

    span {
      width: 100%;
      height: 3px;
      background: $primary-color;
      border-radius: 2px;
      transition: all 0.3s;
      transform-origin: 1px;
    }
  }

  // Mobile styles
  @media (max-width: 768px) {
    .burger {
      display: flex;
    }

    nav {
      position: fixed;
      top: 60px;
      left: 0;
      background: white;
      height: calc(100% - 60px);
      width: 200px;
      flex-direction: column;
      gap: 1.5rem;
      padding: 2rem 1rem;
      box-shadow: -2px 0 8px rgb(0 0 0 / 0.1);
      transform: translateX(-100%);
      transition: transform 0.3s ease-in-out;

      &.open {
        transform: translateX(0);
      }

      a {
        font-size: 1.1rem;
      }
    }
  }
}
</style>
