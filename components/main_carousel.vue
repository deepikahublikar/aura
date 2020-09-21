<template>
  <v-carousel
    style="margin: 0; padding: 0; width: 100%;"
    show-arrows-on-hover
    hide-delimiter-background
  >
    <v-carousel-item
      v-for="(item, i) in images"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
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

<style>
</style>
