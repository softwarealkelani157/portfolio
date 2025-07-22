<template>
  <Navbar />
  <div class="main">

  <router-view />
  </div>
  <Footer />
</template>

<script setup>
import Navbar from './components/NavBar.vue'
import Footer from './components/Footer.vue'
</script>
<style scoped>
.main{
  min-height: calc(100vh - 110px);
}
</style>