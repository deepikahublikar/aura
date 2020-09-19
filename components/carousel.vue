<template>
  <v-carousel
    style="margin: 0; padding: 0; width: 100%"
  >
    <v-carousel-item
      v-for="(item, i) in images"
      :key="i"
      reverse-transition="fade-transition"
      transition="fade-transition"
    >
      <v-img max-height="500px" :src="item.src">
        <v-row
          style="padding: 10px;display:flex; align-content: flex-end;background-color: rgba(66, 66, 66, 0.8)"
        >
          <v-col>
            <h1>
              {{ item.heading }}
            </h1>
            <h4
              class="subheading"
            >
              {{ item.text }}
            </h4>
          </v-col>
        </v-row>
      </v-img>
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  data () {
    return {
      images: [
        {
          src: require('~/assets/carousel_imgs/img1.jpg'),
          heading: 'Image 1',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Est, quam.'
        },
        {
          src: require('~/assets/carousel_imgs/img2.jpg'),
          heading: 'Image 2',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Est, quam.'
        },
        {
          src: require('~/assets/carousel_imgs/img3.jpg'),
          heading: 'Image 3',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Est, quam.'
        },
        {
          src: require('~/assets/carousel_imgs/img4.jpg'),
          heading: 'Image 4',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Est, quam.'
        },
        {
          src: require('~/assets/carousel_imgs/img5.jpg'),
          heading: 'Image 5',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Est, quam.'
        },
        {
          src: require('~/assets/carousel_imgs/img6.jpg'),
          heading: 'Image 6',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Est, quam.'
        }
      ]
    }
  }
}
</script>
