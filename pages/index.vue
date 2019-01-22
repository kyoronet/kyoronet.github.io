<template>
  <v-content>
    <section>
      <v-parallax
        src="https://kyoronet.github.io/image-storage/www.kyoro.net/hero.jpg"
        height="600"
      >
        <v-layout column align-center justify-center class="white--text">
          <v-avatar size="200">
            <img src="img/icon_400x400.jpg">
          </v-avatar>
        </v-layout>
      </v-parallax>
    </section>

    <section>
      <v-layout row wrap justify-center class="my-5">
        <v-flex xs12 sm4>
          <v-card class="elevation-0">
            <v-card-title primary-title class="layout justify-center">
              <div class="headline">
                <v-icon>message</v-icon>
                <span>Contact us</span>
              </div>
            </v-card-title>
            <v-list>
              <v-list-tile v-for="(item, i) in links" :key="i">
                <v-list-tile-action>
                  <v-icon class="blue--text text--lighten-2">{{ item.icon }}</v-icon>
                </v-list-tile-action>
                <v-list-tile-content>
                  <v-list-tile-title>
                    <a :href="item.href">{{ item.title }}</a>
                  </v-list-tile-title>
                </v-list-tile-content>
              </v-list-tile>
            </v-list>
          </v-card>
        </v-flex>
      </v-layout>
    </section>
  </v-content>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          icon: 'mdi-twitter',
          title: 'Twitter',
          href: 'https://twitter.com/kyoro_net'
        },
        {
          icon: 'mdi-github-circle',
          title: 'Github',
          href: 'https://github.com/kyoronet'
        },
        {
          icon: 'create',
          title: 'Blog',
          href: 'https://blog.kyoro.net'
        }
      ]
    }
  }
}
</script>
