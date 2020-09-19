<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      temporary
      right
      app
    >
      <div
        class="d-flex justify-space-between align-center"
      >
        <div
          style="margin-left: 5px"
        >
          Dark Theme
        </div>
        <div>
          <v-switch
            v-model="$vuetify.theme.dark"
            inset
            dense
          />
        </div>
      </div>
      <v-divider />
      <v-list
        style="height: 90%"
        class="d-flex flex-column align-center"
      >
        <v-list-item
          v-for="(item, i) in routes"
          :key="i"
          :to="item.path"
          style="width: 100%"
          router
          exact
        >
          <v-list-item-content
            class="justify-center"
          >
            {{ item.title }}
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      id="appBar"
      elevate-on-scroll
      app
      dense
    >
      <v-toolbar-title>
        <nuxt-link to="/" tag="span" style="cursor: pointer">
          {{ appTitle }}
        </nuxt-link>
      </v-toolbar-title>
      <v-spacer />
      <v-toolbar-items class="hidden-sm-and-down">
        <v-switch
          v-model="$vuetify.theme.dark"
          hide-details
          inset
          dense
          class="align-center"
        />
        <v-btn
          v-for="(item, i) in routes"
          :key="i"
          :to="item.path"
          text
          small
        >
          {{ item.title }}
        </v-btn>
      </v-toolbar-items>
      <v-app-bar-nav-icon class="hidden-md-and-up" @click.stop="drawer = !drawer" />
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer
      absolute
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      routes: [
        { title: 'Home', path: '/' },
        { title: 'About', path: '/about' },
        { title: 'Services', path: '/services' },
        { title: 'Clients', path: '/Clients' },
        { title: 'Exports', path: '/exports' },
        { title: 'Contact', path: '/contact' }
      ],
      appTitle: 'Aura LaserFab'
    }
  }
}
</script>

<style lang="scss">
#appBar {
  background-color: transparent;
}
.v-toolbar .v-btn--active:hover, .v-toolbar .v-btn--active::before {
  background-color: #ff8040;
}
.v-toolbar .v-btn:hover {
  background-color: #ff8040;
}
// #appBar.theme--dark.v-app-bar--is-scrolled {
//   background-color:rgba(223, 12, 12, 0.9);
// }
#appBar.v-app-bar--is-scrolled {
  background-color:rgba(66, 66, 66, .9);
}
.v-input--switch {
  font-family: 'Material Icons';
}
.theme--dark.v-input--switch .v-input--switch__thumb:before {
  content: 'brightness_4';
  color: rgba(255, 255, 255, .87) !important;
}
.theme--light.v-input--switch .v-input--switch__thumb:before {
  content: 'brightness_4';
  color: rgba(0, 0, 0, .87) !important;
}
</style>
