<template>
  <svg-icon
    class="mdi-icon"
    id="mdi-{{mdiIconName}}"
    type="mdi"
    :path="mdiIconName"
  ></svg-icon>
</template>

<script lang="ts">
import SvgIcon from '@jamescoyle/vue-icon'

export default {
  name: 'my-cool-component',
  components: {
    SvgIcon,
  },
  props: ['mdiIconName'],
  setup() {
    return {}
  },
}
</script>
<style>
.mdi-icon {
  height: 36px;
  width: 36px;
  color: var(--color-theme);
  border-radius: 50%;
}
@media (hover: hover) {
  .mdi-icon:hover {
    box-shadow: 0 0 30px 25px var(--color-shadow);
  }
}
</style>
