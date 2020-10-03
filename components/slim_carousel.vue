<template>
  <v-carousel
    style="margin: 0; padding: 0; width: 1000px; height:250px"
    :show-arrows="false"
    hide-delimiter-background
    hide-delimiters
    cycle
  >
    <v-carousel-item
      v-for="(item, i) in images"
      :key="i"
      :src="item.src"
      reverse-transition="scale-transition"
      transition="scroll-x-reverse-transition"
      style="background-size: 1000px 440px; height: 440px"
      class="slim-carousel"
    >
      <!-- <v-img :src="item.src" /> -->
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  data () {
    return {
      images: [
        { src: require('~/assets/images/slim_carousel/banner01a.jpg') },
        { src: require('~/assets/images/slim_carousel/banner02a.jpg') },
        { src: require('~/assets/images/slim_carousel/banner03a.jpg') },
        { src: require('~/assets/images/slim_carousel/banner04a.jpg') },
        { src: require('~/assets/images/slim_carousel/banner05a.jpg') },
        { src: require('~/assets/images/slim_carousel/banner06a.jpg') },
        { src: require('~/assets/images/slim_carousel/banner07a.jpg') },
        { src: require('~/assets/images/slim_carousel/banner08a.jpg') }
      ]
    }
  }
}
</script>

<style>
.slim-carousel .v-image.v-responsive.v-carousel__item {
  height: 250px !important;
}
.slim-carousel .v-image__image--cover {
  background-size: 1000px 250px;
}
</style>
