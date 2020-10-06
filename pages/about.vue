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
            <span slot="opposite" class="largefont">Established in 2006</span>
            <v-card class="elevation-2" width="80%">
              <v-card-title class="headline">
                Incubation Plant Bhosri
              </v-card-title>
              <v-img
                class="center"
                :src="require('~/assets/images/factory.jpg')"
              >
              </v-img>
              <v-card-actions>
                <v-btn
                  color="orange lighten-2"
                  text
                >
                  Explore
                </v-btn>
                <v-spacer />
                <v-btn
                  icon
                  @click="show = !show"
                >
                  <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                </v-btn>
              </v-card-actions>
              <v-expand-transition>
                <div v-show="show">
                  <v-divider />
                  <v-card-text>
                    Lorem ipsum dolor sit amet, no nam oblique veritus. Commune
                    scaevola imperdiet nec ut, sed euismod convenire principes at.
                    Est et nobis iisque percipit, an vim zril disputando voluptatibus,
                    vix an salutandi sententiae.
                  </v-card-text>
                </div>
              </v-expand-transition>
            </v-card>
          </v-timeline-item>
          <v-timeline-item>
            <span slot="opposite" class="largefont">Pune Plant 2010</span>
            <v-card class="elevation-2" width="80%">
              <v-card-title class="headline">
                Started Factory at Shirwal
              </v-card-title>
              <v-img
                class="center"
                :src="require('~/assets/images/factory.jpg')"
              >
              </v-img>
              <v-card-actions>
                <v-btn
                  color="orange lighten-2"
                  text
                >
                  Explore
                </v-btn>
                <v-spacer />
                <v-btn
                  icon
                  @click="show = !show"
                >
                  <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                </v-btn>
              </v-card-actions>
              <v-expand-transition>
                <div v-show="show">
                  <v-divider />
                  <v-card-text>
                    Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.
                  </v-card-text>
                </div>
              </v-expand-transition>
            </v-card>
          </v-timeline-item>
          <v-timeline-item>
            <span slot="opposite" class="largefont">Nashik Plant</span>
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
            <span slot="opposite" class="largefont">Established as a Brand</span>
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
            <span slot="opposite" class="largefont">Present & Future</span>
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
        <h1><p>Our Team</p></h1>
      </div>
      <div
        class="textstyle"
        style="width: 100%; text-align: justify;"
      >
        Coming together is the beginning,
        Staying together is progress, Working together is success.
        A dedicated Product Development Team ensures the development of components
        in the shortest possible time. With the use of advanced design softwares like
        AutoCAD and Sigma Nest - we offer quick support during product development.
        Aura Laser offers innovative Value Analysis And Value Engineering (VAVE) proposals
        without affecting quality & durability of product directly helping customers reduce
        cost of their products.
      </div>
      <div class="container" style="display: flex; height: 100%;margin-top: 25px;">
        <div
          class="textstyle"
          style="width: 20%; text-align: justify;"
        >
          <v-card
            class="mx-auto"
            width="250"
          >
            <v-img
              class="photo"
              :src="require('~/assets/images/Unmesh.jpg')"
            ></v-img>
            <v-card-title>
              Unmesh Mahajani
            </v-card-title>
            <v-card-subtitle>
              Board of Director.
            </v-card-subtitle>
            <v-card-text>
              B.E. (Mech) from NIT Durgapur.
              35 years of experience in Mechanical/Production Engineering,
              Engineering Materials.One of the pioneer in Laser Cutting industry in India.
            </v-card-text>
          </v-card>
        </div>
        <div
          class="textstyle"
          style="margin-left: 5%;"
        >
          <v-card
            class="mx-auto"
            width="250"
          >
            <v-img
              class="photo"
              :src="require('~/assets/images/Unmesh.jpg')"
            ></v-img>
            <v-card-title>
              Abhay Paranjpe
            </v-card-title>
            <v-card-subtitle>
              Board of Director.
            </v-card-subtitle>
            <v-card-text>
              B.E. (Mech) from NIT Durgapur.
              35 years of experience in Mechanical / Production Engineering,
              Engineering Materials.One of the pioneer in Laser Cutting industry in India.
            </v-card-text>
          </v-card>
        </div>
        <div
          class="textstyle"
          style="margin-left: 5%;"
        >
          <v-card
            class="mx-auto"
            width="250"
          >
            <v-img
              class="photo"
              :src="require('~/assets/images/Unmesh.jpg')"
            ></v-img>
            <v-card-title>
              Ananya Mahajani
            </v-card-title>
            <v-card-subtitle>
              Board of Director.
            </v-card-subtitle>
            <v-card-text>
              B.E. (Mech) from NIT Durgapur.
              35 years of experience in Mechanical / Production Engineering,
              Engineering Materials.One of the pioneer in Laser Cutting industry in India.
            </v-card-text>
          </v-card>
        </div>
        <div
          class="textstyle"
          style="margin-left: 5%;"
        >
          <v-card
            class="mx-auto"
            width="250"
          >
            <v-img
              class="photo"
              :src="require('~/assets/images/Unmesh.jpg')"
            ></v-img>
            <v-card-title>
              Vivek Peshwe
            </v-card-title>
            <v-card-subtitle>
              Board of Director.
            </v-card-subtitle>
            <v-card-text>
              B.E. (Mech) from NIT Durgapur.
              35 years of experience in Mechanical / Production Engineering,
              Engineering Materials.One of the pioneer in Laser Cutting industry in India.
            </v-card-text>
          </v-card>
        </div>
      </div>
      <div class="container" style="display: flex; height: 100%;margin-top: 25px;">
        <div
          class="textstyle"
          style="width: 20%; text-align: justify;"
        >
          <v-card
            class="mx-auto"
            width="250"
          >
            <v-img
              class="photo"
              :src="require('~/assets/images/Unmesh.jpg')"
            ></v-img>
            <v-card-title>
              Unmesh Mahajani
            </v-card-title>
            <v-card-subtitle>
              Board of Director.
            </v-card-subtitle>
            <v-card-text>
              B.E. (Mech) from NIT Durgapur.
              35 years of experience in Mechanical/Production Engineering,
              Engineering Materials.One of the pioneer in Laser Cutting industry in India.
            </v-card-text>
          </v-card>
        </div>
        <div
          class="textstyle"
          style="margin-left: 5%;"
        >
          <v-card
            class="mx-auto"
            width="250"
          >
            <v-img
              class="photo"
              :src="require('~/assets/images/Unmesh.jpg')"
            ></v-img>
            <v-card-title>
              Abhay Paranjpe
            </v-card-title>
            <v-card-subtitle>
              Board of Director.
            </v-card-subtitle>
            <v-card-text>
              B.E. (Mech) from NIT Durgapur.
              35 years of experience in Mechanical / Production Engineering,
              Engineering Materials.One of the pioneer in Laser Cutting industry in India.
            </v-card-text>
          </v-card>
        </div>
        <div
          class="textstyle"
          style="margin-left: 5%;"
        >
          <v-card
            class="mx-auto"
            width="250"
          >
            <v-img
              class="photo"
              :src="require('~/assets/images/Unmesh.jpg')"
            ></v-img>
            <v-card-title>
              Ananya Mahajani
            </v-card-title>
            <v-card-subtitle>
              Board of Director.
            </v-card-subtitle>
            <v-card-text>
              B.E. (Mech) from NIT Durgapur.
              35 years of experience in Mechanical / Production Engineering,
              Engineering Materials.One of the pioneer in Laser Cutting industry in India.
            </v-card-text>
          </v-card>
        </div>
        <div
          class="textstyle"
          style="margin-left: 5%;"
        >
          <v-card
            class="mx-auto"
            width="250"
          >
            <v-img
              class="photo"
              :src="require('~/assets/images/Unmesh.jpg')"
            ></v-img>
            <v-card-title>
              Vivek Peshwe
            </v-card-title>
            <v-card-subtitle>
              Board of Director.
            </v-card-subtitle>
            <v-card-text>
              B.E. (Mech) from NIT Durgapur.
              35 years of experience in Mechanical / Production Engineering,
              Engineering Materials.One of the pioneer in Laser Cutting industry in India.
            </v-card-text>
          </v-card>
        </div>
      </div>
    </div>
  </v-layout>
</template>

<script>
export default {
  data: () => ({
    show: false
  }),
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
          .center {
          display: block;
          /*margin-left: 3%;
          margin-right: auto;*/
          width: 100%;
          }
          .photo {
          display: block;
          /*margin-left: 3%;
          margin-right: auto;*/
          height : 210px;
          width : 100%;
          }
</style>
