<template>
  <v-app dark>
    <!-- navigation sidebar/drawer start -->
    <v-navigation-drawer
      v-model="drawer"
      temporary
      right
      app
    >
      <!-- logo and title -->
      <nuxt-link to="/" tag="span" style="cursor: pointer">
        <div class="logo d-flex justify-center align-center" style="color:blue;padding:5px">
          <img width="36px" src="~/assets/images/aura_logo.png" alt="aura-logo">
          <span style="padding-left: 10px;font-family: serif;font-size:1.25rem">{{ appTitle }}</span>
        </div>
      </nuxt-link>
      <v-divider />
      <!-- theme switcher -->
      <div
        class="d-flex justify-space-between align-center"
      >
        <div
          style="margin-left: 5px; font-size:12px;"
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
      <!-- navigation list -->
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
    <!-- navigation sidebar/drawer end -->
    <!-- top app navigation bar start -->
    <v-app-bar
      id="appBar"
      elevate-on-scroll
      app
      dense
    >
      <!-- app logo/title -->
      <v-toolbar-title>
        <nuxt-link to="/" tag="span" style="cursor: pointer">
          <div class="logo" style="display:flex; align-items:center; color:blue;">
            <img width="36px" src="~/assets/images/aura_logo.png" alt="aura-logo">
            <span style="padding-left: 10px;font-family: serif;">{{ appTitle }}</span>
          </div>
        </nuxt-link>
      </v-toolbar-title>
      <v-spacer />
      <!-- navbar links -->
      <v-toolbar-items class="hidden-sm-and-down">
        <v-switch
          v-model="$vuetify.theme.dark"
          hide-details
          inset
          dense
          class="align-center"
        />
        <v-list
          class="d-flex align-center justify-center"
        >
          <v-list-item
            v-for="(item, i) in routes"
            :key="i"
            :to="item.path"
            :ripple="false"
          >
            <v-menu v-if="item.menu" open-on-hover offset-y>
              <template v-slot:activator="{ on }">
                <v-btn
                  text
                  tile
                  small
                  v-on="on"
                >
                  {{ item.title }}
                </v-btn>
              </template>
              <v-list>
                <v-list-item>aaaaaaaaaa</v-list-item>
                <v-list-item>bbbbbbbbbb</v-list-item>
              </v-list>
            </v-menu>
            <v-btn v-else text tile small>
              {{ item.title }}
            </v-btn>
          </v-list-item>
        </v-list>
      </v-toolbar-items>
      <!-- drawer open close button -->
      <v-app-bar-nav-icon class="hidden-md-and-up" @click.stop="drawer = !drawer" />
    </v-app-bar>
    <!-- top app navbar end -->
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
        { title: 'Contact', path: '/contact' },
        { title: 'test', path: '/test' }
      ],
      appTitle: 'Aura'
    }
  }
}
</script>

<style lang="scss">
body {
  overflow: hidden;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.container {
  margin: 0;
  padding: 0;
  width: 100%;
  max-width: 100%;
}
.v-main {
  padding: 0 0 0 0;
  display: flex;
  align-self: center;
  justify-self: center;
  // width: 100%;
}
.v-toolbar,
.v-toolbar .v-list,
.v-toolbar .v-list-item {
  background-color: transparent;
  padding: 0;
}
.v-toolbar .v-btn:before,
.v-toolbar .v-btn:hover,
.v-toolbar .v-btn--active:hover,
.v-toolbar .v-btn--active:before {
  background-color: transparent;
}
.v-toolbar .v-btn,
.v-toolbar .v-btn:before {
  min-height: 48px;
}

.v-toolbar .v-list-item--link,
.v-navigation-drawer .v-list-item--link {
  text-transform: uppercase;
  font-size: 0.9em;
  font-weight: 500;
}
.v-toolbar .v-btn--active:hover,
.v-toolbar .v-btn--active:before,
.v-toolbar .v-list-item--active:before {
  opacity: 1;
  border-bottom: 5px solid var(--v-primary-base);
  background-color: transparent;
}
.v-toolbar .v-btn:hover,
.v-toolbar .v-list-item:hover {
  background-color: var(--v-primary-base);
}
.v-toolbar .v-list {
  background-color: transparent;
}

#appBar.v-app-bar--is-scrolled {
  background-color:rgba(202, 202, 202, 0.9);
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
