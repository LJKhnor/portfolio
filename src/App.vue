<template>
  <header>
    <div class="wrapper">
      <NavBar msg="Lejeune Joachim" />
    </div>
  </header>
  <main>
    <div class="main"><RouterView /></div>
  </main>
  <footer class="footer">
    <div class="footer-wrapper">This site is designed by me</div>
  </footer>
</template>

<script setup lang="ts">
import { RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue'

import IconMdi from '@/components/icons/IconMdi.vue'
</script>

<style scoped>
.footer {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  background-color: var(--color-background);
  color: var(--color-text);
  text-align: center;
}

@media (min-width: 1024px) {
  .logo {
    /* margin: 0 2rem 0 0; */
  }

  header .wrapper {
    /* display: flex;
    place-items: flex-start;
    flex-wrap: wrap; */
  }

  nav {
    /* text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem; */
  }
}
@media (max-width: 1024px) {
  .footer {
    /* align-content: flex-end;
    height: 45vh;
    text-align: center;
    padding: 10px; */
  }
}
</style>
