<template>
  <v-carousel
    style="margin: 0; padding: 0; width: 100%"
    cycle
    show-arrows-on-hover
    hide-delimiter-background
  >
    <v-carousel-item
      v-for="(item, i) in images"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
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
