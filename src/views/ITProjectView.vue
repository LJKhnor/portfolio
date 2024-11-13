<template>
  <div class="project-view">
    <dl class="it-projects">
      <div class="div-project">
        <dt class="dt">GW2 Farming Tracker (coming soon)</dt>
        <dd class="dd">
          <ul>
            <li>
              Backend server made with
              <a
                href="https://en.wikipedia.org/wiki/Spring_Boot"
                target="_blank"
                >Java Spring Boot
                <img src="../assets/icons8-spring-boot-16.png"
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
          </ul>
          <p class="explications">
            GW2 Farming tracker is a web application for tracking and
            statistical calculation of farming sessions on the Guild Wars 2
            mmorpg.
          </p>
        </dd>
      </div>
      <div class="div-project">
        <dt class="dt">PediMed (ongoing)</dt>
        <dd class="dd">
          <ul>
            <li>
              Backend server made with
              <a
                href="https://en.wikipedia.org/wiki/Spring_Boot"
                target="_blank"
                >Java Spring Boot
                <img src="../assets/icons8-spring-boot-16.png"
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
            <li>+ 150h of work (ongoing)</li>
          </ul>
          <p class="explications">
            PediMed is a web and mobile application that allows specialized
            medical pedicures to manage their google calendar and patient files.
            Anonymized data is visually accessible through a map that highlights
            proximity to patients.
          </p>
        </dd>
      </div>

      <div class="div-project">
        <dt class="dt">Portfolio</dt>
        <dd class="dd">
          <ul>
            <li>
              Made with Html, CSS, Javascript and
              <a href="https://vuejs.org/" target="_blank"
                >Vue.js <img src="../assets/icons8-vue-js-16.png"
              /></a>
            </li>
            <li>20 hours of work</li>
          </ul>
          <p class="explications">
            This portfolio is a showcase of my achievements as a worker since I
            was 21. Not just as a developer.
          </p>
        </dd>
      </div>
      <div class="div-project">
        <dt class="dt">
          Elo Ranking System (<a
            href="https://github.com/LJKhnor/EloRankingSystem"
            target="_blank"
            >Github <img src="../assets/icons8-github-16.png" /></a
          >)
        </dt>
        <dd class="dd">
          <ul>
            <li>
              Backend server made with
              <a href="https://vuejs.org/" target="_blank"
                >Python <img src="../assets/icons8-python-16.png"
              /></a>
            </li>
            <li>
              Database made with
              <a href="https://www.sqlite.org/index.html" target="_blank"
                >SQLite <img src="../assets/icons8-sqlite-16.png"
              /></a>
            </li>
            <li>
              Frontend server made with Html, CSS, Javascript and
              <a
                href="https://flask.palletsprojects.com/en/stable/"
                target="_blank"
                >Flask <img src="../assets/icons8-flask-16.png"
              /></a>
            </li>
            <li>40 hours of work</li>
          </ul>
          <p class="explications">
            Elo Ranking System is a web application that allows you to create
            Magic the gathering league for several players and encode their
            games, their decks. As the results are integrated, statistics are
            calculated and accessible in a dashboard.
          </p>
        </dd>
      </div>
      <div class="div-project">
        <dt class="dt">
          Iotrack (<a href="https://www.actia.be/fr" target="_blank"
            >Actia Telematics Services</a
          >)
        </dt>
        <dd class="dd">
          <ul>
            <li>
              Backend server made with
              <a
                href="https://en.wikipedia.org/wiki/Spring_Boot"
                target="_blank"
                >Java Spring Boot
                <img src="../assets/icons8-spring-boot-16.png"
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
          </ul>
          <p>
            Telematics application for business analysis and vehicle fleet
            management.
          </p>
        </dd>
      </div>
      <div class="div-project">
        <dt class="dt">
          Telefleet (<a href="https://www.actia.be/fr" target="_blank"
            >Actia Telematics Services</a
          >)
        </dt>
        <dd class="dd">
          <ul>
            <li>
              Backend server made with
              <a
                href="https://en.wikipedia.org/wiki/Spring_Boot"
                target="_blank"
                >Java Spring Boot
                <img src="../assets/icons8-spring-boot-16.png"
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
              <a href="https://www.sencha.com/products/extjs/" target="_blank"
                >Sencha Ext.js</a
              >
            </li>
          </ul>
          <p>
            Telematics application for business analysis and vehicle fleet
            management.
          </p>
        </dd>
      </div>
    </dl>
  </div>
</template>
<script setup lang="ts"></script>
<style>
.project-view {
  position: relative;
  margin: 10vh;
}
.it-projects {
}
.div-project {
  margin-top: 4vh;
  padding: 1vh;
  text-align: justify;
  box-shadow: -2vh 2vh 12px var(--color-shadow);
}
.dt {
  color: var(--color-theme);
  font-size: x-large;
  margin: auto 4vw;
}
.dd {
}
p {
  margin-top: 2vh;
  text-indent: 0%;
}

@media (hover: hover) {
}
@media (min-width: 1324px) {
  .project-view {
    position: relative;
    margin: 10vh 25vh 0 25vh;
  }
  .dt {
    margin: auto 2vw;
  }
}
@media (min-width: 760px) and (max-width: 1323px) {
}
@media (max-width: 760px) {
  .project-view {
    position: relative;
    margin: 0;
  }
  .dt {
    margin: auto 4vw;
  }
}
</style>
