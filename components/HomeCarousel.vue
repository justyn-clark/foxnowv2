<template>
  <div id="home-carousel" class="pl-24 pb-12">
    <div class="flex-1 min-w-0">
      <h2
        class="text-2xl font-bold leading-7 text-white sm:text-3xl sm:truncate"
      >
        {{ title }}
      </h2>
    </div>
    <carousel-3d
      :disable3d="true"
      :space="390"
      :clickable="true"
      :controls-visible="true"
    >
      <slide v-for="(event, i) in events" :key="i" :index="i">
        <figure class="rounded-lg">
          <div class="rounded-r-full">
            <img :src="event.images" alt="" class="rounded-lg" />
          </div>
          <p class="rounded-lg number-slide">{{ i + 1 }}</p>
        </figure>
      </slide>
    </carousel-3d>
  </div>
</template>

<script>
export default {
  name: 'HomeCarousel',
  props: ['title'],
  data() {
    return {
      events: [],
    }
  },

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
  height: 168px;
  width: 300px;
}
</style>

<!--<style lang="scss">
#app {
  width: 100%;
  background: url('https://demo-pachi.mikadogames.net/img/bg_content.b7cc7f2b.jpg');

  .carousel-3d-container {
    .carousel-3d-slide {
      padding: 20px;
      background-color: unset;
      border: 0px;
    }
    p {
      font-weight: bold;
      margin-top: -163%;
      margin-left: 45%;
    }

    .prev {
      color: #fff;
    }
    .next {
      color: #fff;
    }
  }

  @media screen and (max-width: 480px) {
    .carousel-3d-container {
      width: 100% !important;
      height: 400px !important;
    }
    .pc {
      display: none;
    }
  }
  @media screen and (min-width: 732px) {
    .carousel-3d-container {
      width: 70% !important;
      height: 400px !important;
    }
    .sp {
      display: none;
    }
  }
}
</style>-->
