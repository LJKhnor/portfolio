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

.center-content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 10;
  font-size: 20px;
  color: black;
  width: 20%;
}
@media (max-width: 768px) {
  .sun {
    display: none;
  }
  .container-wheel {
    position: relative;
    margin-top: 10vh;
    height: 50vh;
  }
  .wheel {
    position: relative;
    display: grid;
    grid-template-columns: 1fr auto 1fr;
    grid-template-rows: 0.25fr 3.5fr 0.25fr;
    grid-template-areas:
      'info1 info2 info3'
      'info4 center-content info5'
      'info6 info7 info8';
    gap: 4px;
    column-gap: 1px;
    pointer-events: all;
    align-items: center;
    height: 100%;
  }
  .center-content {
    position: relative;
    color: var(--color-text);
    width: 50vw;
    z-index: 0;
    align-self: baseline;
  }
  .info {
    margin-top: 0;
    position: relative;
    transform: none;
    width: auto;
    z-index: 1;
    animation: fadein 1s;
  }
  .info1 {
    grid-area: info1;
  }
  .info2 {
    grid-area: info2;
  }
  .info3 {
    grid-area: info3;
  }
  .info4 {
    grid-area: info4;
  }
  .info5 {
    grid-area: info5;
  }
  .info6 {
    grid-area: info6;
  }
  .info7 {
    grid-area: info7;
  }
  .info8 {
    grid-area: center-content;
  }
}
@media (min-width: 768px) and (max-width: 1280px) {
  /* Adapter la taille des éléments pour les écrans plus larges */
  .sun {
    width: 40vh;
    height: 40vh;
    transition: 1s;
  }

  .info {
    width: 12vh;
    height: 12vh;
  }
  .info1 {
    top: 0;
  }

  .info2 {
    top: 0;
    transform: translate(125%, 25%);
  }

  .info3 {
    top: 0;
    transform: translate(215%, 110%);
  }

  .info4 {
    top: 0;
    transform: translate(250%, 250%);
  }

  .info5 {
    top: 0;
    transform: translate(215%, 385%);
  }

  .info6 {
    top: 0;
    transform: translate(125%, 475%);
  }

  .info7 {
    top: 0;
    transform: translate(0%, 500%);
  }
}

@media (min-width: 1280px) {
  /* Adapter encore plus pour les écrans très larges */
  .sun {
    width: 40vh;
    height: 40vh;
    transition: 1s;
  }
  .container-wheel {
    height: 55vh;
  }
  .wheel {
    height: 135%;
  }
  .info {
    width: 12vh;
    height: 12vh;
  }
  .info1 {
    top: 0;
  }

  .info2 {
    top: 0;
    transform: translate(125%, 25%);
  }

  .info3 {
    top: 0;
    transform: translate(215%, 110%);
  }

  .info4 {
    top: 0;
    transform: translate(250%, 250%);
  }

  .info5 {
    top: 0;
    transform: translate(215%, 385%);
  }

  .info6 {
    top: 0;
    transform: translate(125%, 475%);
  }

  .info7 {
    top: 0;
    transform: translate(0%, 500%);
  }
}
</style>
