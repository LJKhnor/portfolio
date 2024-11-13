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
          <img
            class="photo img-normal"
            src="../assets/logo 5 petit format.jpg"
          />
          <img
            class="photo img-xl"
            src="../assets/ref logo 5 petit format.jpg"
          />
        </dd>
      </div>
      <div class="div-project">
        <dt class="dt">Logo for "Valériane Pédicure"</dt>
        <dd class="dd">
          <img class="photo img-val" src="../assets/logo_pedicure_val.jpg" />
        </dd>
      </div>
      <div class="div-project">
        <dt class="dt">
          Cover and chapter illustration for the book
          <a
            href="https://booknode.com/l_ere_des_troubles_tome_1_hiro_02327455"
            target="_blank"
            >"Les Chroniques d'Ellentride, Tome 1"</a
          >
        </dt>
        <dd class="dd">
          <img class="photo img-xxl" src="../assets/Couverture logo.jpg" />
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
.dt {
  color: var(--color-theme);
  font-size: x-large;
  margin-top: 2vh;
}
.dd {
  text-indent: 2vh;
  margin-top: 2vh;

  animation: fadein 1s;
}
p {
  margin-top: 2vh;
}
.div-project {
  margin-top: 4vh;
  padding: 1vh;
  box-shadow: -2vh 2vh 12px var(--color-shadow);
}
.photo {
  border: 2px solid var(--color-theme);
  padding: 4px;
  width: 148px;
  border-radius: 25px;
}
.img-normal {
  height: 16vh;
  width: 16vh;
  margin: 4vh;
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
