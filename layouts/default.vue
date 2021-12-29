<template>
  <v-app dark>
    <v-navigation-drawer v-model="drawer" :mini-variant="miniVariant" fixed app>
      <v-list>
        <v-list-item v-for="(item, i) in items" :key="i" :to="item.to" router exact>
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar fixed app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title v-text="title" />
      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer dark padless >
      <v-card flat tile width="100%" class="white--text text-center">
        <v-card-text>
          <v-btn v-for="icon in icons" :key="icon" class="mx-4 white--text" icon>
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-text class="white--text">
          &copy;{{ new Date().getFullYear() }} — <strong>Studio</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      items: [
        {
          icon: 'mdi-apps',
          title: '首頁',
          to: '/'
        },
        {
          title: '作品集',
          to: '/product'
        },
        // {
        //   title: 'About',
        //   to: '/about'
        // },
        {
          title: '聯繫我們',
          to: '/contact'
        }
      ],
      icons: [
        'mdi-facebook',
        'mdi-github',
        'mdi-linkedin',
        'mdi-instagram',
      ],
      miniVariant: false,
      title: 'Majaja Studio',
      fab: false,
    }
  }
}
</script>
<style>
.v-speed-dial {
  position: absolute;
}

.v-btn--floating {
  position: relative;
}
</style>
