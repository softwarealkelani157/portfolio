<template>
  <form @submit.prevent="submitForm" class="contact-form" novalidate>
    <label>
      Name
      <input type="text" v-model="form.name" required />
    </label>
    <label>
      Email
      <input type="email" v-model="form.email" required />
    </label>
    <label>
      Message
      <textarea v-model="form.message" required></textarea>
    </label>
    <button type="submit" :disabled="!isValid">Send Message</button>
    <p v-if="success" class="success-msg">Thanks! Your message has been sent.</p>
  </form>
</template>

<script setup>
import { reactive, computed, ref } from 'vue'

const form = reactive({
  name: '',
  email: '',
  message: ''
})

const success = ref(false)

const isValid = computed(() => {
  return form.name.trim() && /\S+@\S+\.\S+/.test(form.email) && form.message.trim()
})

function submitForm() {
  if (!isValid.value) return
  // Simulate sending message
  success.value = true
  form.name = ''
  form.email = ''
  form.message = ''
  setTimeout(() => (success.value = false), 5000)
}
</script>

<style scoped lang="scss">
@import '@/assets/styles/variables';

.contact-form {
  max-width: 500px;
  margin: auto;
  display: flex;
  flex-direction: column;
  gap: 1.25rem;

  label {
    display: flex;
    flex-direction: column;
    font-weight: 600;
    color: $dark-color;

    input,
    textarea {
      margin-top: 0.25rem;
      padding: 0.75rem 1rem;
      border: 1.5px solid $primary-color;
      border-radius: 0.5rem;
      font-size: 1rem;
      font-family: inherit;
      transition: border-color 0.3s;

      &:focus {
        outline: none;
        border-color: darken($primary-color, 15%);
      }
    }

    textarea {
      resize: vertical;
      min-height: 120px;
    }
  }

  button {
    background-color: $primary-color;
    color: white;
    font-weight: 600;
    padding: 0.75rem 2rem;
    border: none;
    border-radius: 9999px;
    cursor: pointer;
    transition: background 0.3s;
    align-self: flex-start;

    &:disabled {
      background-color: lighten($primary-color, 30%);
      cursor: not-allowed;
    }

    &:hover:not(:disabled) {
      background-color: darken($primary-color, 10%);
    }
  }

  .success-msg {
    margin-top: 1rem;
    color: green;
    font-weight: 600;
  }
}
</style>
