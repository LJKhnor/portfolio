<template>
  <svg-icon id="mdi-cake" type="mdi" :path="path"></svg-icon>
</template>

<script lang="ts">
import SvgIcon from '@jamescoyle/vue-icon'
import { mdiCakeVariant } from '@mdi/js'

export default {
  name: 'my-cool-component',

  components: {
    SvgIcon,
  },
  setup(props, ctx) {
    return {
      path: mdiCakeVariant,
    }
  },
}
</script>
<style>
.mdi-cake {
  width: 25px;
  height: 25px;
}
</style>
