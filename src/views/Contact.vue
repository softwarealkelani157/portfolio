<template>
  <main class="contact-page">
    <h1>Contact Me</h1>
    <ContactForm />
  </main>
</template>

<script setup>
import ContactForm from '@/components/ContactForm.vue'
</script>

<style scoped lang="scss">
.contact-page {
  padding: 3rem 1rem;
  max-width: 600px;
  margin: auto;

  h1 {
    text-align: center;
    margin-bottom: 2rem;
    color: $dark-color;
  }
}
</style>
