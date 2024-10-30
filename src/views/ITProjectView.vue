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
            <li>+ 250h of work (ongoing)</li>
          </ul>
        </dd>
        <p class="explications">
          PediMed is a web and mobile application that allows specialized
          medical pedicures to manage their google calendar and patient files.
          Anonymized data is visually accessible through a map that highlights
          proximity to patients.
        </p>
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
            <li>+ 250h of work (ongoing)</li>
          </ul>
        </dd>
        <p class="explications">
          PediMed is a web and mobile application that allows specialized
          medical pedicures to manage their google calendar and patient files.
          Anonymized data is visually accessible through a map that highlights
          proximity to patients.
        </p>
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
            <li>80 hours of work</li>
          </ul>
        </dd>
        <p class="explications">
          This portfolio is a showcase of my achievements as a worker since I
          was 21. Not just as a developer.
        </p>
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
            <li>80 hours of work</li>
          </ul>
        </dd>
        <p class="explications">
          Elo Ranking System is a web application that allows you to create
          Magic the gathering league for several players and encode their games,
          their decks. As the results are integrated, statistics are calculated
          and accessible in a dashboard.
        </p>
      </div>
      <div class="div-project">
        <dt class="dt">
          Iotrack (<a href="https://www.actia.be/fr"
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
        </dd>
        <p>
          Telematics application for business analysis and vehicle fleet
          management.
        </p>
      </div>
      <div class="div-project">
        <dt class="dt">
          Telefleet (<a href="https://www.actia.be/fr"
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
        </dd>
        <p>
          Telematics application for business analysis and vehicle fleet
          management.
        </p>
      </div>
    </dl>
  </div>
</template>
<script lang="ts"></script>
<style>
.project-view {
  position: relative;
  margin: 10vh;
}
.dt {
  color: var(--color-theme);
  font-size: x-large;
  margin-top: 2vh;
}
.dd {
  text-indent: 2vh;
  margin-top: 2vh;
  display: none;
}
p {
  margin-top: 2vh;
}
.div-project {
  margin-top: 4vh;
  padding: 1vh;
  box-shadow: -2vh 2vh 12px var(--color-shadow);
}
@media (min-width: 1024px) {
  .project-view {
    position: relative;
    margin: 10vh 25vh 0 25vh;
  }
}
@media (hover: hover) {
  .dt :hover {
    display: flex;
  }
}
</style>
