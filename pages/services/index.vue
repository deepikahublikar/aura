<template>
  <div>
    <h1>Services Page</h1>
    <v-menu open-on-hover offset-y>
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          dark
          v-bind="attrs"
          v-on="on"
        >
          Dropdown
        </v-btn>
      </template>
      <v-list>
        <v-list-item>aaaaaa</v-list-item>
        <v-list-item>bbbbbb</v-list-item>
      </v-list>
    </v-menu>
  </div>
</template>

<script>
export default {
  data () {
    return {
      servicesRoutes: [
        { title: 'CNC Laser Cutting', path: '/services/CNC_laser_cutting' },
        { title: 'CNC Plasma Cutting', path: '/services/CNC_plasma_cutting' },
        { title: 'CNC Bending', path: '/services/CNC_bending' },
        { title: 'CNC Rolling', path: '/services/CNC_rolling' },
        { title: 'Metal Fabrication', path: '/services/metal_fabrication' },
        { title: 'Surface Treatment', path: '/services/surface_treatment' }
      ]
    }
  },
  head () {
    return { title: 'Services' }
  }
}
</script>

<style>

</style>
