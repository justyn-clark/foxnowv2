<template>
  <div id="main">
    <app-header />
    <Nuxt />
  </div>
</template>

<script lang="ts">
import { defineComponent, useAsync } from '@nuxtjs/composition-api'
import appHeader from './appHeader.vue'

export default defineComponent({
  name: 'Default',
  components: {
    appHeader,
  },
  setup() {
    useAsync(() => {
      if (process.server) {
        return false
      }

      const token = window.localStorage.getItem('token')

      if (token) {
        // retryLogin(token)
      }
    })
  },
})
</script>
