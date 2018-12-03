<template>
  <v-app :dark="dark">
    <!-- サイドバー -->
    <v-navigation-drawer v-model="drawer" :mini-variant="miniVariant" :clipped="clipped" fixed app>
      <v-list>
        <v-list-group
          v-for="item in items"
          v-model="item.active"
          :key="item.title"
          :prepend-icon="item.icon"
          no-action
        >
          <v-list-tile slot="activator">
            <v-list-tile-content>
              <v-list-tile-title>{{ item.title }}</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>

          <v-list-tile v-for="subItem in item.items" :key="subItem.title">
            <v-list-tile-content>
              <v-list-tile-title>{{ subItem.title }}</v-list-tile-title>
            </v-list-tile-content>

            <v-list-tile-action>
              <v-icon>{{ subItem.icon }}</v-icon>
            </v-list-tile-action>
          </v-list-tile>
        </v-list-group>
      </v-list>
    </v-navigation-drawer>

    <!-- ナビバー -->
    <v-toolbar :clipped-left="clipped" fixed app>
      <!-- サイドバー表示/非表示切替ボタン -->
      <v-toolbar-side-icon @click="drawer = !drawer"/>
      <!-- タイトル -->
      <v-toolbar-title v-text="title"/>
      <v-spacer/>
      <!-- 夜間モード切替ボタン -->
      <v-list-tile>
        <v-list-tile-action>
          <v-switch v-model="dark" hide-details label="夜間モード"/>
        </v-list-tile-action>
      </v-list-tile>
    </v-toolbar>
    <nuxt/>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      dark: false,
      clipped: true,
      drawer: false,
      fixed: true,
      items: [
        {
          icon: 'apps',
          title: 'Welcome',
          to: '/',
          items: [
            {
              icon: 'link',
              title: 'Link',
              to: '#link'
            }
          ]
        }
      ],
      miniVariant: false,
      title: 'キョロの紹介'
    }
  }
}
</script>
