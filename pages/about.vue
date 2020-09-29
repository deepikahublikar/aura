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
        <style>
          p::first-letter {
          text-decoration: underline;
          text-decoration-thickness: 1%;
          text-decoration-color: orange;
          border-radius: 10px;
          float: left;
         }
          .heading {
          font-weight: normal;
          text-decoration-style: solid;
          }
          .textstyle {
          font-weight: normal;
          text-align: justify;
          }
        </style>
      </v-flex>
      <v-container class="white lighten-5">
        <v-row no-gutters>
          <v-col
            cols="5"
            sm="6"
            md="8"
          >
            <v-card
              class="pa-2"
              flat
              tile
            >
              <div
                class="textstyle"
                style="width: 100%; padding: 2%; margin: 0"
              >
                Situated near Pune, the engineering Capital of India, Aura LaserFab offers both manufacturing and job shopping services in the field of CNC Laser Cutting Services.
                <br><br>
                Equipped with the latest machines of CNC Laser Cutting, Bending and Fabrication Aura manufactures a large variety of components with a mix of volumes. With the use of contemporary techniques of operations management we can deliver components in shorter lead time meeting universally acceptable quality standards. We manufacture products ranging from a precise laser cut–bent component to a complex welded and painted assembly using a variety of raw materials like carbon steel, stainless steel, aluminium, and special steels.
                <br><br>
                The team of Aura, comprising of 100+ qualified engineers & technicians, possesses a strong experience in the domains of development, marketing, engineering operations, projects and quality assurance.
                <br><br>
                Aura Laser has presently spearheaded a major up scaling of its capacity in Metal Cutting & fabrication with addition of workspace area, machineries like CNC Plasma Cutting, CNC Straightening, CNC Rolling and Robotic Welding to support its multi segmental growth.
              </div>
            </v-card>
          </v-col>
          <v-col
            cols="6"
            md="4"
          >
            <v-card
              class="mx-auto"
              flat
              max-width="400"
            >
              <!--<v-img
                class="white--text align-end"
                height="300px"
                src="https://img2.exportersindia.com/product_images/bc-full/2019/8/6546166/industrial-shed-designing-1566472136-5051322.jpeg"
              >-->
              <iframe width="400" height="315" src="https://www.youtube.com/embed/h-YrFdEpSq8"></iframe>
              <!--<v-card-title>An ISO 9001:2008 certified company</v-card-title>-->
              <!--</v-img>-->
              <!--<v-card-subtitle class="pb-0">
                Gat No. 1021, Pune - Bangalore Highway
              </v-card-subtitle>
              <v-card-text class="text--primary">
                <div>Near Pune, Shirwal.</div>
                <div>Dist. Satara - 412801, Maharashtra, India.</div>
                <div>Phone : +91 2169 244545, +91 2169 244546</div>
              </v-card-text>-->
            </v-card>
          </v-col>
        </v-row>
      </v-container>
      <div class="heading">
        <h1><p>Who We Are</p></h1>
      </div>
      <div
        class="textstyle"
        style="width: 100%; padding: 2%; margin: 0"
      >
        A dedicated Product Development Team ensures the development of components in the shortest possible time. With the use of advanced design softwares like AutoCAD and Sigma Nest - we offer quick support during product development.
        Aura Laser offers innovative Value Analysis And Value Engineering (VAVE) proposals without affecting quality & durability of product directly helping customers reduce cost of their products.
      </div>
      <v-container fluid>
        <v-row>
          <v-col cols="12">
            <v-row
              :align="alignment"
              :justify="justify"
              class="grey lighten-5"
              style="height: 300px;"
            >
              <v-card
                class="mx-auto"
                width="300px"
              >
                <v-img
                  class="white--text align-end"
                  height="150px"
                  src="~/assets/images/aura_logo.png"
                >
                  <v-card-title>
                    Leadership
                  </v-card-title>
                </v-img>
              </v-card>
              <v-card
                class="mx-auto"
                width="300px"
              >
                <v-img
                  class="white--text align-end"
                  height="150px"
                  src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
                >
                  <v-card-title>
                    Strategy & Purpose
                  </v-card-title>
                </v-img>
              </v-card>
              <v-card
                class="mx-auto"
                width="300px"
              >
                <v-img
                  class="white--text align-end"
                  height="150px"
                  src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
                >
                  <v-card-title>
                    History
                  </v-card-title>
                </v-img>
              </v-card>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
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
