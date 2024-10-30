<template>
  <div class="project-view">
    <dl class="other-projects">
      <div class="div-project">
        <dt class="dt">
          Logo and banner for
          <a href="https://hb-debouchage.be/" target="_blank"
            >"HB Débouchage"</a
          >
        </dt>
        <dd class="dd">
          <img class="img" src="../assets/logo 5 petit format.svg" />
          <img class="img-xl" src="../assets/ref logo 5 petit format.svg" />
        </dd>
        <p></p>
      </div>
      <div class="div-project">
        <dt class="dt">Logo for "Valériane Pédicure"</dt>
        <dd class="dd">
          <img class="img-val" src="../assets/logo_pedicure_val.png" />
        </dd>
        <p></p>
      </div>
      <div class="div-project">
        <dt class="dt">
          Cover and chapter illustration for the book "Les Chroniques
          d'Ellentride, Tome 1"
        </dt>
        <dd class="dd">
          <img class="img-xxl" src="../assets/1.Couverture logo.png" />
        </dd>
        <p></p>
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
.img {
  vertical-align: top;
  height: 16vh;
  width: 16vh;
}
.img-val {
  height: 24vh;
  width: 24vh;
}
.img-xl {
  height: 25vh;
  width: 35vh;
}
.img-xxl {
  height: 45vh;
  width: 35vh;
}
@media (min-width: 1024px) {
  .project-view {
    position: relative;
    margin: 10vh 25vh 0 25vh;
  }
}
@media (hover: hover) {
  .dt:hover + .dd {
    transition: 100s;
    display: flex;
  }
}
</style>
