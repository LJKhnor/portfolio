<template>
  <svg-icon
    class="mdi-icon"
    id="mdi-{{mdiIconName}}"
    type="mdi"
    :path="mdiIconName"
  ></svg-icon>
</template>

<script lang="ts">
import SvgIcon from '@jamescoyle/vue-icon'

export default {
  name: 'my-cool-component',
  components: {
    SvgIcon,
  },
  props: ['mdiIconName'],
  setup() {
    return {}
  },
}
document.addEventListener('DOMContentLoaded', () => {
  const icons = document.querySelectorAll('.mdi-icon')

  icons.forEach(icon => {
    icon.addEventListener('click', () => {
      // Supprime la classe des autres icônes
      icons.forEach(i => i.classList.remove('highlight'))
      // Ajoute la classe à l'icône cliquée
      icon.classList.add('highlight')
    })
    icon.addEventListener('touchstart', () => {
      icons.forEach(i => i.classList.remove('highlight'))
      icon.classList.add('highlight')
    })
  })
})
// Supprime le highlight si on clique en dehors des icônes
document.addEventListener('click', event => {
  const icons = document.querySelectorAll('.mdi-icon')
  const wheel = document.querySelector('.wheel')
  // Vérifie si le clic est en dehors de la roue
  if (!wheel!.contains(event.target as Node)) {
    icons.forEach(icon => icon.classList.remove('highlight'))
  }
})
</script>
<style>
.mdi-icon {
  height: 50px;
  width: 50px;
  color: var(--color-theme);
  border-radius: 50%;
}
@media (hover: hover) {
  .mdi-icon:hover {
    box-shadow: 0 0 30px 25px var(--color-shadow);
  }
}
@media (max-width: 786px) {
  .highlight {
    transform: scale(1.2); /* Agrandit légèrement l'icône */
    box-shadow: 0 0 50px 10px var(--color-theme); /* Met en évidence avec un effet lumineux */
    transition:
      transform 0.3s,
      box-shadow 0.3s; /* Ajoute une animation douce */
  }
}
</style>
