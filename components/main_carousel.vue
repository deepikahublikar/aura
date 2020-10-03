<template>
  <v-carousel
    style="margin: 0; padding: 0; max-width: 1000px; max-height:440px"
    show-arrows-on-hover
    hide-delimiter-background
    justify-center
    align-center
    cycle
  >
    <v-carousel-item
      v-for="(item, i) in images"
      :key="i"
      :src="item.src"
      reverse-transition="scale-transition"
      transition="scroll-x-reverse-transition"
      style="background-size: 1000px 440px; max-height: 440px"
      class="main-carousel"
    />
  </v-carousel>
</template>

<script>
export default {
  data () {
    return {
      images: [
        { src: require('~/assets/images/main_carousel/banner01.jpg') },
        { src: require('~/assets/images/main_carousel/banner02.jpg') },
        { src: require('~/assets/images/main_carousel/banner03.jpg') },
        { src: require('~/assets/images/main_carousel/banner04.jpg') },
        { src: require('~/assets/images/main_carousel/banner05.jpg') },
        { src: require('~/assets/images/main_carousel/banner06.jpg') },
        { src: require('~/assets/images/main_carousel/banner07.jpg') },
        { src: require('~/assets/images/main_carousel/banner08.jpg') }
      ]
    }
  }
}
</script>

<style lang="scss">
.main-carousel .v-image.v-responsive.v-carousel__item {
  max-width: 1000px;
  max-height: 440px;
}
.main-carousel .v-image__image--cover {
  background-size: 1000px 440px;
}
</style>
