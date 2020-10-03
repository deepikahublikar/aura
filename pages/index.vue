<template>
  <v-layout
    column
    justify-center
    align-center
    style="width: 100%; padding: 0; margin: 0"
  >
    <main-carousel />
    <h1>An ISO 9001:2008 certified company</h1>
    <p>
      Situated near Pune, the engineering Capital of India, Aura LaserFab offers both manufacturing and job shopping services in the field of CNC Laser Cutting Services.
    </p>
    <div class="d-flex">
      <img src="~/assets/images/factory.jpg" alt="">
      <p class="justify-space-between align-center" style="padding: 3px;">
        Equipped with the latest machines of CNC Laser Cutting, Bending and Fabrication Aura manufactures a large variety of components with a mix of volumes. With the use of contemporary techniques of operations management we can deliver components in shorter lead time meeting universally acceptable quality standards. We manufacture products ranging from a precise laser cut –bent component to a complex welded and painted assembly using a variety of raw materials like carbon steel, stainless steel, aluminium, and special steels.
      </p>
    </div>
    <p>
      <br>
      The team of Aura, comprising of 100+ qualified engineers and technicians, possesses a strong experience in the domains of development, marketing, engineering operations, projects and quality assurance.
    </p>
    <p>
      Aura Laser has presently spearheaded a major up scaling of its capacity in Metal Cutting & fabrication with addition of workspace area, machineries like CNC Plasma Cutting, CNC Straightening, CNC Rolling and Robotic Welding to support its multi segmental growth.
    </p>
  </v-layout>
</template>

<script>
export default {
  head () {
    return { title: 'Home' }
  }
}
</script>
