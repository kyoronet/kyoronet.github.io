<template>
  <v-app :dark="dark">
    <!-- サイドバー -->
    <v-navigation-drawer v-model="drawer" :mini-variant="miniVariant" :clipped="clipped" fixed app>
      <v-list>
        <v-list-tile
          v-for="(item, i) in items"
          :key="i"
          router
          exact
          @click="$vuetify.goTo(item.to, options)"
        >
          <v-list-tile-action>
            <v-icon v-html="item.icon"/>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title v-text="item.title"/>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>

    <!-- ナビバー -->
    <v-toolbar :clipped-left="clipped" fixed app>
      <!-- サイドバー表示/非表示切替ボタン -->
      <v-toolbar-side-icon @click="drawer = !drawer"/>
      <!-- タイトル -->
      <v-toolbar-title v-text="title"/>
    </v-toolbar>
    <nuxt/>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      duration: 300,
      offset: 0,
      easing: 'easeInOutCubic',
      dark: false,
      clipped: true,
      drawer: false,
      fixed: true,
      items: [
        {
          icon: 'apps',
          title: 'Portfolio',
          to: '#portfolio'
        },
        {
          icon: 'message',
          title: 'Contact us',
          to: '#contact'
        }
      ],
      miniVariant: false,
      title: 'キョロの紹介'
    }
  },
  computed: {
    options() {
      return {
        duration: this.duration,
        offset: this.offset,
        easing: this.easing
      }
    }
  }
}
</script>
