<template>
  <div class="home">
    <h1>C'est la page de présentation rapide</h1>
  </div>
  <div class="wheel">
    <div class="info" style="transform: rotate(0deg)">
      <IconMdi :mdiIconName="mdiCakeVariant" />
    </div>
    <div class="info" style="transform: rotate(30deg)">
      <IconMdi :mdiIconName="mdiAccountArrowUp" />
    </div>
    <div class="info" style="transform: rotate(60deg)">
      <IconMdi :mdiIconName="mdiAccountMultipleOutline" />
    </div>
    <div class="info" style="transform: rotate(90deg)">
      <IconMdi :mdiIconName="mdiAccountMultipleOutline" />
    </div>
    <div class="info" style="transform: rotate(120deg)">
      <IconMdi :mdiIconName="mdiAccountMultipleOutline" />
    </div>
    <div class="info" style="transform: rotate(150deg)">
      <IconMdi :mdiIconName="mdiAccountMultipleOutline" />
    </div>
    <div class="info" style="transform: rotate(180deg)">
      <IconMdi :mdiIconName="mdiAccountMultipleOutline" />
    </div>
    <div class="info" style="transform: rotate(210deg)">
      <IconMdi :mdiIconName="mdiAccountMultipleOutline" />
    </div>
    <div class="info" style="transform: rotate(240deg)">
      <IconMdi :mdiIconName="mdiAccountMultipleOutline" />
    </div>
    <div class="info" style="transform: rotate(270deg)">
      <IconMdi :mdiIconName="mdiAccountMultipleOutline" />
    </div>
    <div class="info" style="transform: rotate(300deg)">
      <IconMdi :mdiIconName="mdiAccountMultipleOutline" />
    </div>
    <div class="info" style="transform: rotate(330deg)">
      <IconMdi :mdiIconName="mdiAccountMultipleOutline" />
    </div>
  </div>
</template>

<script setup lang="ts">
import IconMdi from '@/components/icons/IconMdi.vue'

import {
  mdiCakeVariant,
  mdiAccountArrowUp,
  mdiAccountMultipleOutline,
} from '@mdi/js'
</script>

<style>
.wheel {
  position: relative;
  width: 50vh;
  height: 50vh;
  margin: 50px auto;
  border-radius: 50%;
  background: linear-gradient(-90deg, #f9dd62, var(--color-theme));
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
}

.info {
  align-content: space-evenly;
  position: absolute;
  width: 5vh;
  height: 10vh;
  font:
    bold 20px Arial,
    sans-serif;
  color: #fff;
  text-align: center;
  border-radius: 50%;
  background-color: #333;
  transform-origin: 50% 35vh;
}
@keyframes spin {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
</style>
