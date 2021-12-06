<template>
  <div>
    <HomeHero />
    <HomeCarousel title="NEW EPISODES" />
    <HomeCarousel title="LIVE NOW" />
    <HomeCarousel title="UP NEXT" />
    <HomeCarousel title="TRENDING" />
    <HomeCarousel title="RECOMMENDED FOR YOU" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import HomeHero from '~/components/HomeHero.vue'
import HomeCarousel from '~/components/HomeCarousel.vue'

export default Vue.extend({
  components: { HomeHero, HomeCarousel },
})
</script>
