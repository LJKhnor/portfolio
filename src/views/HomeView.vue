<template>
  <div class="container-wheel">
    <div class="satellite"></div>
    <div class="sun"></div>
    <div class="wheel">
      <div
        class="info"
        @mouseover="updateCenterContent('Age')"
        @mouseout="clearContent"
        style="transform: rotate(0deg)"
      >
        <IconMdi class="icon" :mdiIconName="mdiCakeVariant" />
      </div>
      <div
        class="info"
        @mouseover="updateCenterContent('Maried')"
        @mouseout="clearContent"
        style="transform: rotate(30deg)"
      >
        <IconMdi class="icon" :mdiIconName="mdiRing" />
      </div>
      <div
        class="info"
        @mouseover="updateCenterContent('Dad')"
        @mouseout="clearContent"
        style="transform: rotate(60deg)"
      >
        <IconMdi class="icon" :mdiIconName="mdiAccountChild" />
      </div>
      <div
        class="info"
        @mouseover="updateCenterContent('Experience')"
        @mouseout="clearContent"
        style="transform: rotate(90deg)"
      >
        <IconMdi class="icon" :mdiIconName="mdiDesktopClassic" />
      </div>
      <div
        class="info"
        @mouseover="updateCenterContent('Illustrator')"
        @mouseout="clearContent"
        style="transform: rotate(120deg)"
      >
        <IconMdi class="icon" :mdiIconName="mdiPalette" />
      </div>
      <div
        class="info"
        @mouseover="updateCenterContent('Brewer')"
        @mouseout="clearContent"
        style="transform: rotate(150deg)"
      >
        <IconMdi class="icon" :mdiIconName="mdiBeer" />
      </div>
      <div
        class="info"
        @mouseover="updateCenterContent('Hobbies')"
        @mouseout="clearContent"
        style="transform: rotate(180deg)"
      >
        <IconMdi class="icon" :mdiIconName="mdiDiceD20" />
      </div>
      <div class="center-content">{{ centerContent }}</div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import IconMdi from '@/components/icons/IconMdi.vue'

import {
  mdiCakeVariant,
  mdiAccountChild,
  mdiDesktopClassic,
  mdiRing,
  mdiDiceD20,
  mdiPalette,
  mdiBeer,
  // mdiAccountMultipleOutline,
} from '@mdi/js'

const centerContent = ref('Who am I ?')

function updateCenterContent(content: string) {
  const endDate = new Date()
  const birthDate = new Date('18 December 1987')
  const startDevCarrierDate = new Date('6 May 2023')
  const startMarriageDate = new Date('12 April 2012')
  const startDadDate = new Date('18 Jully 2017')
  switch (content) {
    case 'Age': {
      const ageYear = processCorrectNbYear(endDate, birthDate)
      centerContent.value = "I'm " + ageYear + ' years old.'
      break
    }
    case 'Experience': {
      const xpYear = processCorrectNbYear(endDate, startDevCarrierDate)
      const xpMonth = endDate.getMonth() - startDevCarrierDate.getMonth()
      centerContent.value =
        'I am a software developper for ' +
        xpYear.toString() +
        (xpMonth > 0 ? ' years and ' + xpMonth + ' months' : ' year')
      break
    }
    case 'Maried': {
      const mariageYear = processCorrectNbYear(endDate, startMarriageDate)
      const xpMonth = endDate.getMonth() - startMarriageDate.getMonth()
      centerContent.value =
        "I'm married for " +
        mariageYear.toString() +
        (xpMonth > 0 ? ' years and ' + xpMonth + ' months' : ' year')
      break
    }
    case 'Dad': {
      const dadYear = processCorrectNbYear(endDate, startDadDate)
      const dadMonth = endDate.getMonth() - startDadDate.getMonth()
      centerContent.value =
        "I'm a twin dad for " +
        dadYear.toString() +
        (dadMonth > 0 ? ' years and ' + dadMonth + ' months' : ' year')
      break
    }
    case 'Illustrator': {
      centerContent.value =
        'I have made the cover artwork of one book and the logo and banner of two company to date'
      break
    }
    case 'Brewer': {
      centerContent.value = 'I brewed my own beer.'
      break
    }
    case 'Hobbies': {
      centerContent.value =
        'I like to do Wargame, role-playing games with my friends or my children, drawing, watching movies and series with my wife, playing video games and keep fit by playing sports.'
      break
    }
    default: {
      centerContent.value = 'Nope'
      break
    }
  }
}
function clearContent() {
  centerContent.value = 'Who am I ?'
}
function processCorrectNbYear(endDate: Date, starDate: Date) {
  let nbYear = endDate.getFullYear() - starDate.getFullYear()
  if (
    endDate.getMonth() < starDate.getMonth() ||
    (endDate.getMonth() === starDate.getMonth() &&
      endDate.getDate() < starDate.getDate())
  ) {
    nbYear--
  }
  return nbYear
}
</script>

<style>
.container-wheel {
  position: relative;
  margin-top: 10vh;
  margin-left: 25vh;
}
.sun {
  position: absolute;
  width: 50vh;
  height: 50vh;
  margin: 50px auto;
  border-radius: 50%;
  background: linear-gradient(-90deg, var(--color-theme), #f9dd62);
  box-shadow: 0 0 30px 12px var(--color-shadow);
  /* background-image: url('../assets/photo_jojo_cv.jpg'); */
  /* background-size: 75%; */
  background-position: center;
  background-repeat: no-repeat;
  background-color: transparent;
}
.satellite {
  position: absolute;
  width: 20vh;
  height: 20vh;
  margin: 50px -15vh;
  border-radius: 100%;
  background-image: url('../assets/photo_jojo_cv.jpg');
  background-size: 100%;
  background-repeat: no-repeat;
  background-color: transparent;
  box-shadow: 0 0 30px 12px #f9dd62;
  z-index: 3;
  animation: fadein 1s;
}
.wheel {
  position: absolute;
  z-index: 1;
}
.info {
  position: absolute;
  align-content: space-evenly;
  width: 50vh;
  font:
    bold 20px Arial,
    sans-serif;
  color: #fff;
  text-align: center;
  border-radius: 50%;
  transform-origin: 50% 30vh;
  cursor: pointer;
  z-index: 2;

  animation: fadein 1s;
}

.info:nth-child(2) .icon {
  transform: rotate(-30deg); /* Rotation inverse pour garder l'icône droite */
}

.info:nth-child(3) .icon {
  transform: rotate(-60deg);
}
.info:nth-child(4) .icon {
  transform: rotate(-90deg);
}
.info:nth-child(5) .icon {
  transform: rotate(-120deg);
}
.info:nth-child(6) .icon {
  transform: rotate(-150deg);
}
.info:nth-child(7) .icon {
  transform: rotate(-180deg);
}
.center-content {
  align-content: center;
  position: absolute;
  width: 50vh;
  height: 60vh;
  /* transform: translate(22vh, 26vh); */
  text-align: center;
  font-size: 1.5em;
  color: var(--color-background);
  background-color: transparent;
  padding: 10px;
  border-radius: 10px;
  z-index: 1;
}
@media (min-width: 1024px) {
  .container-wheel {
    position: relative;
    margin-top: 10vh;
    margin-left: 40vh;
  }
}
/* @keyframes spin {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
} */
@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
