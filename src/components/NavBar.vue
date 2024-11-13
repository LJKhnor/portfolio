<template>
  <div class="greetings">
    <h1 class="color-theme">{{ msg }}</h1>
    <nav>
      <RouterLink to="/">Home</RouterLink> |
      <RouterLink to="/project">IT Projects</RouterLink> |
      <RouterLink to="/other_project">Other Projects</RouterLink> |
      <!-- <RouterLink to="/skills">Skills</RouterLink> |
      <RouterLink to="/cv">CV</RouterLink> | -->
      <RouterLink to="/contact">Contact</RouterLink>
      <!-- <RouterLink to="/about">About</RouterLink> -->
    </nav>
  </div>
</template>

<script setup lang="ts">
import { RouterLink } from 'vue-router'
defineProps<{
  msg: string
}>()
</script>

<style scoped>
.greetings {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
nav {
  margin: 0 0 1%;
}

nav a {
  margin: 0 15px;
}

h1 {
  /* font-weight: 500; */
  font-size: 2.6rem;
  /* position: relative; */
  /* top: -10px; */
}

@media (min-width: 1024px) {
}
</style>
