<template>
  <footer class="footer">
    <div class="container">
      <p>&copy; {{ year }} Omran Alkelani. All rights reserved...</p>
      <div class="socials">
        <a href="https://github.com/softwarealkelani157" aria-label="GitHub" target="_blank" rel="noopener noreferrer">
          <svg viewBox="0 0 24 24" fill="currentColor" class="icon">
            <path
              d="M12 0C5.37 0 0 5.37 0 12a12 12 0 008.21 11.43c.6.11.82-.26.82-.58 0-.29-.01-1.05-.02-2.06-3.34.73-4.04-1.61-4.04-1.61-.54-1.38-1.32-1.75-1.32-1.75-1.08-.74.08-.73.08-.73 1.2.08 1.83 1.23 1.83 1.23 1.06 1.82 2.78 1.3 3.46.99.11-.78.42-1.3.76-1.6-2.66-.3-5.46-1.33-5.46-5.91 0-1.3.46-2.37 1.22-3.21-.12-.3-.53-1.52.12-3.17 0 0 .99-.32 3.24 1.22a11.3 11.3 0 015.9 0c2.25-1.54 3.24-1.22 3.24-1.22.65 1.65.24 2.87.12 3.17.76.84 1.22 1.91 1.22 3.21 0 4.59-2.8 5.61-5.47 5.9.43.37.82 1.1.82 2.22 0 1.6-.01 2.9-.01 3.3 0 .32.22.7.82.58A12 12 0 0024 12c0-6.63-5.37-12-12-12z"
            />
          </svg>
        </a>
        <a href="https://www.linkedin.com/in/omran-alkelani-6b2bb82ab/" aria-label="LinkedIn" target="_blank" rel="noopener noreferrer">
          <svg viewBox="0 0 24 24" fill="currentColor" class="icon">
            <path
              d="M19 0h-14c-2.76 0-5 2.24-5 5v14c0 2.76 2.24 5 5 5h14c2.76 0 5-2.24 5-5v-14c0-2.76-2.24-5-5-5zm-11 19h-3v-10h3v10zm-1.5-11.5c-.97 0-1.75-.78-1.75-1.75S5.53 4 6.5 4s1.75.78 1.75 1.75S7.47 7.5 6.5 7.5zm13.5 11.5h-3v-5.5c0-1.32-1.07-2.5-2.5-2.5s-2.5 1.18-2.5 2.5v5.5h-3v-10h3v1.5c.7-1.15 2.01-1.5 3.13-1.5 2.39 0 4.37 2.14 4.37 4.5v5.5z"
            />
          </svg>
        </a>
      </div>
    </div>
  </footer>
</template>

<script setup>
const year = new Date().getFullYear()
</script>

<style scoped lang="scss">
@import '@/assets/styles/variables';

.footer {
  background: $primary-color;
  color: white;
  padding: 0.6rem 1rem;
  font-weight: 600;

  .container {
    max-width: 1200px;
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 1rem;
  }

  .socials {
    display: flex;
    gap: 1.5rem;

    a {
      color: white;
      transition: color 0.3s;
      font-size: 1.25rem;

      &:hover {
        color: lighten($primary-color, 30%);
      }

      .icon {
        width: 24px;
        height: 24px;
      }
    }
  }

  @media (max-width: 600px) {
    .container {
      flex-direction: column;
      text-align: center;
    }
  }
}
</style>
