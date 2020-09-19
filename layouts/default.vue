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
      elevate-on-scroll
      app
    >
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
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
      title: 'Vuetify.js'
    }
  }
}
</script>
