<template>
  <div class="container">
    <header>
      <div class="wrapper">
        <NavBar msg="Lejeune Joachim" />
      </div>
    </header>
    <main>
      <div class="router-view"><RouterView /></div>
    </main>
    <footer class="footer">
      <div class="footer-wrapper">
        This site is designed by
        <a href="https://github.com/LJKhnor" target="_blank">Lejeune Joachim</a>
      </div>
    </footer>
  </div>
</template>

<script setup lang="ts">
import { RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue'
</script>

<style scoped>
.container {
  width: 100%;
  height: 100%;
  text-align: center;
}
header {
  margin: 0 0 2%;
}
main {
  margin: 0 0 2%;
}
.router-view {
  margin: 5vw;
}
</style>
