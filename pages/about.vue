<template>
  <v-layout
    column
    justify-center
    align-center
    style="width: 100%; padding: 0; margin: 0"
  >
    <main-carousel />
    <div
      style="width: 100%; padding: 3%; margin: 2%"
    >
      <carousel />
      <v-flex
        xs12
        sm8
        md6
      >
        <div class="heading">
          <h1><p>About Aura LaserFab</p></h1>
        </div>
      </v-flex>
      <div class="container" style="display: flex; height: 100%;">
        <div
          class="textstyle"
          style="width: 60%; text-align: justify;"
        >
          Situated near Pune, the engineering Capital of India, Aura LaserFab offers both
          manufacturing and job shopping services in the field of CNC Laser Cutting Services.
          <br><br>
          Equipped with the latest machines of CNC Laser Cutting, Bending and Fabrication
          Aura manufactures a large variety of components with a mix of volumes. With the
          use of contemporary techniques of operations management we can deliver components
          in shorter lead time meeting universally acceptable quality standards.
          We manufacture products ranging from a precise laser cut–bent component to a
          complex welded and painted assembly using a variety of raw materials like carbon steel,
          stainless steel, aluminium, and special steels.
          <br><br>
          The team of Aura, comprising of 100+ qualified engineers & technicians,
          possesses a strong experience in the domains of development, marketing,
          engineering operations, projects and quality assurance.
          <br><br>
          Aura Laser has presently spearheaded a major up scaling of its capacity in
          Metal Cutting & fabrication with addition of workspace area, machineries like
          CNC Plasma Cutting, CNC Straightening, CNC Rolling and Robotic Welding to support
          its multi segmental growth.
        </div>
        <div
          class="textstyle"
          style="flex-grow: 1;margin-left: 30px;margin-top: 25px;"
        >
          <iframe width="450" height="315" src="https://www.youtube.com/embed/h-YrFdEpSq8"></iframe>
        </div>
      </div>
      <div class="heading">
        <h1><p>History</p></h1>
      </div>
      <div>
        <v-timeline
          :reverse="reverse"
          :dense="$vuetify.breakpoint.smAndDown"
        >
          <v-timeline-item>
            <span class="largefont" slot="opposite">Established in 2016</span>
            <v-card class="elevation-2">
              <v-card-title class="headline">
                Incubation Plant Bhosri
              </v-card-title>
              <v-img
                src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
                height="100px"
              ></v-img>
              <v-card-text>
                Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.
              </v-card-text>
            </v-card>
          </v-timeline-item>
          <v-timeline-item>
            <span class="largefont" slot="opposite">Pune Plant</span>
            <v-card class="elevation-2">
              <v-card-title class="headline">
                Lorem ipsum
              </v-card-title>
              <v-img
                src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
                height="200px"
              ></v-img>
              <v-card-text>
                Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.
              </v-card-text>
            </v-card>
          </v-timeline-item>
          <v-timeline-item>
            <span class="largefont" slot="opposite">Nashik Plant</span>
            <v-card class="elevation-2">
              <v-card-title class="headline">
                Lorem ipsum
              </v-card-title>
              <v-card-text>
                Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.
              </v-card-text>
            </v-card>
          </v-timeline-item>
          <v-timeline-item>
            <span class="largefont" slot="opposite">Established as a Brand</span>
            <v-card class="elevation-2">
              <v-card-title class="headline">
                Lorem ipsum
              </v-card-title>
              <v-card-text>
                Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.
              </v-card-text>
            </v-card>
          </v-timeline-item>
          <v-timeline-item>
            <span class="largefont" slot="opposite">Present & Future</span>
            <v-card class="elevation-2">
              <v-card-title class="headline">
                Lorem ipsum
              </v-card-title>
              <v-card-text>
                Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.
              </v-card-text>
            </v-card>
          </v-timeline-item>
        </v-timeline>
      </div>
      <div class="heading">
        <h1><p>Leadership</p></h1>
      </div>
      <div
          class="textstyle"
          style="width: 100%; text-align: justify;"
      >
        A dedicated Product Development Team ensures the development of components in the shortest possible time. With the use of advanced design softwares like AutoCAD and Sigma Nest - we offer quick support during product development.
        Aura Laser offers innovative Value Analysis And Value Engineering (VAVE) proposals without affecting quality & durability of product directly helping customers reduce cost of their products.
      </div>
    </div>
  </v-layout>
</template>

<script>
export default {
  head () {
    return { title: 'About' }
  }
}
</script>
<style>
          p::first-letter {
          text-decoration: underline;
          text-decoration-thickness: 1%;
          text-decoration-color: orange;
          border-radius: 10px;
          float: left;
         }
          .heading {
          font-family: Sans-serif;
          font-weight: normal;
          text-decoration-style: solid;
          margin-top: 25px;
          }
          .textstyle {
          font-weight: normal;
          text-align: justify;
          }
          .largefont {
          font-family:arial;
          font-weight: bold;
          font-size: 20px;
          }
</style>
