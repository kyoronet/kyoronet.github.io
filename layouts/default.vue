<template>
  <v-app :dark="dark">
    <v-navigation-drawer
      :mini-variant="miniVariant"
      :clipped="clipped"
      v-model="drawer"
      fixed
      app
    >
      <v-list>
        <v-list-tile
          v-for="(item, i) in items"
          :to="item.to"
          :href="item.href"
          :key="i"
          router
          exact
        >
          <v-list-tile-action>
            <v-icon v-html="item.icon" />
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title v-text="item.title" />
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar
      :clipped-left="clipped"
      fixed
      app
    >
      <v-toolbar-side-icon @click="drawer = !drawer" />
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-list-tile>
        <v-list-tile-action>
          <v-switch
            v-model="dark"
            hide-details
            label="夜間モード"
          />
        </v-list-tile-action>
      </v-list-tile>
    </v-toolbar>
    <nuxt />

  </v-app>
</template>

<script>
export default {
  data() {
    return {
      dark: false,
      clipped: true,
      drawer: true,
      fixed: true,
      items: [
        { icon: 'apps', title: 'Welcome', to: '/' },
        { icon: 'create', title: 'Blog', href: 'https://blog.kyoro.net' }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'キョロの紹介'
    }
  }
}
</script>
