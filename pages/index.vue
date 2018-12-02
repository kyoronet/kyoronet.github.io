<template>
  <v-content>
    <section>
      <v-parallax
        src="https://picsum.photos/1350/805?random"
        height="600"
      >
        <v-layout
          column
          align-center
          justify-center
          class="white--text"
        >
          <v-avatar size="200">
            <img src="img/icon_400x400.jpg">
          </v-avatar>
        </v-layout>
      </v-parallax>
    </section>

    <section>
      <v-layout
        row
        wrap
        justify-center
        class="my-5"
      >
        <v-flex
          xs12
          sm4
          offset-sm1
        >
          <v-card class="elevation-0 transparent">
            <v-card-title
              primary-title
              class="layout justify-center"
            >
              <div class="headline">
                <span>Links</span>
              </div>
            </v-card-title>
            <v-list class="transparent">
              <v-list-tile>
                <v-list-tile-action>
                  <v-icon class="blue--text text--lighten-2">mdi-github-circle</v-icon>
                </v-list-tile-action>
                <v-list-tile-content>
                  <v-list-tile-title><a href="https://github.com/kyoronet">Github</a></v-list-tile-title>
                </v-list-tile-content>
              </v-list-tile>
              <v-list-tile>
                <v-list-tile-action>
                  <v-icon class="blue--text text--lighten-2">mdi-twitter</v-icon>
                </v-list-tile-action>
                <v-list-tile-content>
                  <v-list-tile-title><a href="https://twitter.com/kyoro_net">Twitter</a></v-list-tile-title>
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
</script>
