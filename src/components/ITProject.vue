<template>
  <div class="div-project">
    <dt class="dt">
      PediMed (
      <a :href="link" target="_blank"
        >Site <img :src="pathLogoLink" width="20em" height="20rem" alt=""
      /></a>
      )
    </dt>
    <dd class="dd">
      <ul>
        <li>
          Backend server made with
          <a href="https://en.wikipedia.org/wiki/Spring_Boot" target="_blank"
            >Java Spring Boot <img src="../assets/icons8-spring-boot-16.png"
          /></a>
        </li>
        <li>
          Database made with
          <a href="https://www.postgresql.org/" target="_blank"
            >PostgreSql <img src="../assets/icons8-postgresql-16.png"
          /></a>
        </li>
        <li>
          Frontend server made with Html, CSS, Javascript and
          <a href="https://vuejs.org/" target="_blank"
            >Vue.js <img src="../assets/icons8-vue-js-16.png"
          /></a>
        </li>
        <!-- <li>+ 150h of work (ongoing)</li> -->
      </ul>
      <p class="explications">
        PediMed is a web and mobile application that allows specialized medical
        pedicures to manage their google calendar and patient files. Anonymized
        data is visually accessible through a map that highlights proximity to
        patients.
      </p>
    </dd>
  </div>
</template>

<script setup lang="ts">
const props = defineProps({
  link: String,
  pathLogoLink: String,
})
console.log(props.pathLogoLink)
</script>

<style></style>
