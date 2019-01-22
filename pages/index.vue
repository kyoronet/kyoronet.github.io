<template>
  <v-content class="mb-5">
    <section id="portfolio">
      <v-parallax
        src="https://kyoronet.github.io/image-storage/www.kyoro.net/hero.jpg"
        height="600"
      >
        <v-layout column align-center justify-center class="white--text">
          <v-avatar size="200">
            <img src="img/icon_400x400.jpg">
          </v-avatar>
          <div class="headline white--text my-3 text-xs-center">
            <span>Portfolio</span>
          </div>
        </v-layout>
      </v-parallax>
    </section>

    <section>
      <v-layout column wrap class="my-5" align-center>
        <v-flex xs12>
          <v-container grid-list-xl>
            <v-layout row wrap align-center>
              <v-flex v-for="(item, i) in portfolio" :key="i" xs12 md4>
                <v-card>
                  <v-img :src="item.img" aspect-ratio="2.75"></v-img>
                  <v-card-title primary-title>
                    <div>
                      <h3 class="headline mb-0">{{ item.title }}</h3>
                      <div>{{ item.details }}</div>
                    </div>
                  </v-card-title>
                  <v-card-actions>
                    <v-tooltip v-for="(link, i) in item.links" :key="i" top>
                      <v-btn
                        slot="activator"
                        :href="link.href"
                        target="_blank"
                        flat
                        icon
                        class="blue--text text--lighten-2"
                      >
                        <v-icon>{{ link.icon }}</v-icon>
                      </v-btn>
                      <span>{{ link.title }}</span>
                    </v-tooltip>
                  </v-card-actions>
                </v-card>
              </v-flex>
            </v-layout>
          </v-container>
        </v-flex>
      </v-layout>
    </section>

    <section id="contact">
      <v-parallax
        src="https://kyoronet.github.io/image-storage/www.kyoro.net/section.jpg"
        height="380"
      >
        <v-layout column align-center justify-center>
          <div class="headline white--text mb-3 text-xs-center">
            <span>Contact us</span>
          </div>
        </v-layout>
      </v-parallax>
    </section>

    <section>
      <v-layout row wrap justify-center class="my-5">
        <v-flex xs12 sm4>
          <v-card class="elevation-0">
            <v-list>
              <v-list-tile v-for="(item, i) in contacts" :key="i">
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
      portfolio: [
        {
          title: '四択問題',
          details: '',
          img: 'https://kyoronet.github.io/image-storage/rails-quiz/check.gif',
          links: [
            {
              icon: 'mdi-web',
              title: 'Web',
              href: 'https://rails-quiz2.herokuapp.com/'
            },
            {
              icon: 'mdi-github-circle',
              title: 'Github',
              href: 'https://github.com/kyoronet/rails-quiz'
            }
          ]
        },
        {
          title: 'ドキュメントバージョン管理',
          details: '',
          img:
            'https://kyoronet.github.io/image-storage/angular-doc-lab/upload.gif',
          links: [
            {
              icon: 'mdi-github-circle',
              title: 'Github',
              href: 'https://github.com/kyoronet/angular-doc-lab'
            }
          ]
        },
        {
          title: '自作コーディングエディタ',
          details: '',
          img:
            'https://kyoronet.github.io/image-storage/qt-code-editor/menu.gif',
          links: [
            {
              icon: 'mdi-github-circle',
              title: 'Github',
              href: 'https://github.com/kyoronet/qt-code-editor'
            }
          ]
        },
        {
          title: '将棋',
          details: '',
          img: 'https://kyoronet.github.io/image-storage/qt-shogi/demo.gif',
          links: [
            {
              icon: 'mdi-github-circle',
              title: 'Github',
              href: 'https://github.com/kyoronet/qt-shogi'
            }
          ]
        },
        {
          title: 'ネット動画プレーヤー',
          details: '',
          img:
            'https://kyoronet.github.io/image-storage/actionscript-netvideo/demo.gif',
          links: [
            {
              icon: 'mdi-github-circle',
              title: 'Github',
              href: 'https://github.com/kyoronet/actionscript-netvideo'
            }
          ]
        },
        {
          title: '簡易掲示板',
          details: '',
          img:
            'https://kyoronet.github.io/image-storage/php-simple-bbs/bbs-demo.gif',
          links: [
            {
              icon: 'mdi-web',
              title: 'Web',
              href: 'https://php-simple-bbs.herokuapp.com/'
            },
            {
              icon: 'mdi-github-circle',
              title: 'Github',
              href: 'https://github.com/kyoronet/php-simple-bbs'
            }
          ]
        }
      ],
      contacts: [
        {
          icon: 'mdi-github-circle',
          title: 'Github',
          href: 'https://github.com/kyoronet'
        },
        {
          icon: 'mdi-twitter',
          title: 'Twitter',
          href: 'https://twitter.com/kyoro_net'
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
