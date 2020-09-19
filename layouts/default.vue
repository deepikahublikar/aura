<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      temporary
      right
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in routes"
          :key="i"
          :to="item.path"
          router
          exact
        >
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      id="appBar"
      elevate-on-scroll
      app
      dense
      hide-shadow
    >
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-toolbar-items class="hidden-sm-and-down">
        <v-switch
          v-model="$vuetify.theme.dark"
          hide-details
          inset
          dense
          style="align-items: center"
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
      title: 'Aura LaserFab'
    }
  }
}
</script>

<style lang="scss">
</style>
