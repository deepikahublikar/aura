<template>
  <v-layout
    column
    justify-center
    align-center
    style="width: 100%; padding: 0; margin: 0"
  >
    <v-flex
      xs12
      sm8
      md6
    >
      About Page
    </v-flex>
    <div
      style="width: 100%; padding: 0; margin: 0"
    >
      <carousel />
    </div>
    <!-- <carousel /> -->
  </v-layout>
</template>

<script>
export default {
  head () {
    return { title: 'About' }
  }
}
</script>
