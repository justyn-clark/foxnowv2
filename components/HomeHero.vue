<template>
  <div id="home-hero">
    <div class="pt-6 mb-24">
      <carousel-3d
        :autoplay="true"
        :autoplay-timeout="5000"
        :perspective="0"
        :space="700"
        :display="3"
        :width="1104"
        :height="330"
        :loop="true"
        :controls-visible="true"
        :controls-prev-html="'&#10092;'"
        :controls-next-html="'&#10093;'"
        :controls-width="30"
        :controls-height="60"
        :clickable="false"
        :count="events.length"
      >
        <slide v-for="(event, i) in events" :index="i" :key="i">
          <figure>
            <img :src="event.images" />
            <p class="number-slide">{{ i + 1 }}</p>
          </figure>
        </slide>
      </carousel-3d>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SomeName',

  data() {
    return {
      events: [],
    }
  }, // End of data

  created() {
    const vm = this
    vm.events = [
      {
        images:
          'https://demo-pachi.mikadogames.net/img/machine_no_tag.57940855.png',
      },
      {
        images: 'https://demo-pachi.mikadogames.net/img/play_1.97899fa7.png',
      },
      {
        images:
          'https://demo-pachi.mikadogames.net/img/machine_no_tag.57940855.png',
      },
      {
        images:
          'https://demo-pachi.mikadogames.net/img/machine_no_tag.57940855.png',
      },
      {
        images: 'https://demo-pachi.mikadogames.net/img/play_8.a7dd8404.png',
      },
      {
        images:
          'https://demo-pachi.mikadogames.net/img/machine_no_tag.57940855.png',
      },
      {
        images:
          'https://demo-pachi.mikadogames.net/img/machine_no_tag.57940855.png',
      },
      {
        images: 'https://demo-pachi.mikadogames.net/img/play_7.cede9514.png',
      },
      {
        images:
          'https://demo-pachi.mikadogames.net/img/machine_no_tag.57940855.png',
      },
      {
        images:
          'https://demo-pachi.mikadogames.net/img/machine_no_tag.57940855.png',
      },
    ]
  },
}
</script>

<style lang="css">
.carousel-3d-container {
  width: 100% !important;
}
.carousel-3d-slide {
  border-radius: 8px;
  border: none;
}
</style>
