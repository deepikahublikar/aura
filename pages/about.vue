<template>
  <v-layout
    column
    justify-center
    align-center
    style="width: 100%; padding: 0; margin: 0"
  >
    <slim-carousel />
    <v-flex
      xs12
      sm8
      md6
    >
      <h1>About Page</h1>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  head () {
    return { title: 'About' }
  }
}
</script>
