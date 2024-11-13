<template>
  <div class="container-wheel">
    <div class="satellite"></div>
    <div class="sun"></div>
    <div class="wheel">
      <div
        class="info info1"
        @mouseover="updateCenterContent('Age')"
        @mouseout="clearContent"
      >
        <IconMdi class="icon" :mdiIconName="mdiCakeVariant" />
      </div>
      <div
        class="info info2"
        @mouseover="updateCenterContent('Maried')"
        @mouseout="clearContent"
      >
        <IconMdi class="icon" :mdiIconName="mdiRing" />
      </div>
      <div
        class="info info3"
        @mouseover="updateCenterContent('Dad')"
        @mouseout="clearContent"
      >
        <IconMdi class="icon" :mdiIconName="mdiAccountChild" />
      </div>
      <div
        class="info info4"
        @mouseover="updateCenterContent('Experience')"
        @mouseout="clearContent"
      >
        <IconMdi class="icon" :mdiIconName="mdiDesktopClassic" />
      </div>
      <div
        class="info info5"
        @mouseover="updateCenterContent('Illustrator')"
        @mouseout="clearContent"
      >
        <IconMdi class="icon" :mdiIconName="mdiPalette" />
      </div>
      <div
        class="info info6"
        @mouseover="updateCenterContent('Brewer')"
        @mouseout="clearContent"
      >
        <IconMdi class="icon" :mdiIconName="mdiBeer" />
      </div>
      <div
        class="info info7"
        @mouseover="updateCenterContent('Hobbies')"
        @mouseout="clearContent"
      >
        <IconMdi class="icon" :mdiIconName="mdiDiceD20" />
      </div>
      <div class="info8 center-content">
        {{ centerContent }}
      </div>
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
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 75vh;
}

.sun {
  width: 50vh;
  height: 50vh;
  background: linear-gradient(-90deg, var(--color-theme), #f9dd62);
  box-shadow: 0 0 30px 12px var(--color-shadow);
  border-radius: 50%;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}

.wheel {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  transform: rotate(0deg); /* Cette rotation peut être animée si nécessaire */
}

.info {
  width: 15vh; /* ajuster selon la taille que tu veux */
  height: 15vh;
  font-size: 20px;
  text-align: center;
  line-height: 15vh; /* Centrer le texte à l'intérieur de l'élément */
  border-radius: 50%;
  cursor: pointer;
  position: absolute; /* Permet de positionner ces éléments autour du cercle */
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 2;
}

.info1 {
  top: 0;
}

.info2 {
  top: 0;
}

.info3 {
  top: 0;
}

.info4 {
  top: 0;
}

.info5 {
  top: 0;
}

.info6 {
  top: 0;
}

.info7 {
  top: 0;
}

.center-content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 10;
  font-size: 18px;
  font-weight: bold;
  color: white;
}
@media (max-width: 768px) {
  .sun {
  }
}
@media (min-width: 768px) and (max-width: 1284px) {
  /* Adapter la taille des éléments pour les écrans plus larges */
  .sun {
    width: 40vh;
    height: 40vh;
  }

  .info {
    width: 12vh;
    height: 12vh;
  }

  .info1,
  .info3,
  .info5,
  .info7 {
    font-size: 22px; /* Agrandir les icônes pour les écrans plus larges */
  }
}

@media (min-width: 1284) {
  /* Adapter encore plus pour les écrans très larges */
  .sun {
    width: 35vh;
    height: 35vh;
  }

  .info {
    width: 10vh;
    height: 10vh;
  }
}
</style>
