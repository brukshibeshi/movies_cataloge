<template lang="pug">
.page
  section-header(
    title="Nuxt blog"
    subtitle="The best blog you can find on the global internet"
  )

  app-options

  post-list
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'SwitcherColorMode',

  computed: {
    icon() {
      return (this as any).$colorMode.value === 'light'
        ? 'assets/icons/sun.svg'
        : 'assets/icons/moon.svg'
    },
  },

  methods: {
    changeColorMode() {
      ;(this as any).$colorMode.preference =
        (this as any).$colorMode.value === 'light' ? 'dark' : 'light'
    },
  },
})
</script>

<style lang="scss" scoped>
.app-options {
  display: flex;
  margin-top: 24px;
}
</style>