<template>
  <div class="container">
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
  </div>
</template>

<script setup lang="ts">
import { RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue'
</script>

<style scoped>
.container {
  width: 100vw;
  height: 100vh;
  position: fixed;
  text-align: center;
}
header {
  margin: 0 0 2%;
}

@media (max-width: 512px) {
}
</style>
