<template>
  <svg-icon id="mdi-{{mdiIconName}}" type="mdi" :path="mdiIconName"></svg-icon>
</template>

<script lang="ts">
import SvgIcon from '@jamescoyle/vue-icon'

export default {
  name: 'my-cool-component',
  components: {
    SvgIcon,
  },
  props: ['mdiIconName'],
  setup(props, ctx) {
    return {}
  },
}
</script>
<style>
.mdi-cake {
  width: 25px;
  height: 25px;
}
</style>
