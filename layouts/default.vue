



<template >

  <v-app :dark="dark">
    <v-layout row wrap align-center v-if="preloader==true" fill-height>
  <v-flex justify-center>
    <center>
    <svg width="140" height="64" viewBox="0 0 140 64" xmlns="http://www.w3.org/2000/svg" fill="red">
        <path d="M30.262 57.02L7.195 40.723c-5.84-3.976-7.56-12.06-3.842-18.063 3.715-6 11.467-7.65 17.306-3.68l4.52 3.76 2.6-5.274c3.717-6.002 11.47-7.65 17.305-3.68 5.84 3.97 7.56 12.054 3.842 18.062L34.49 56.118c-.897 1.512-2.793 1.915-4.228.9z" fill-opacity=".5">
            <animate attributeName="fill-opacity"
                begin="0s" dur="1.4s"
                values="0.5;1;0.5"
                calcMode="linear"
                repeatCount="indefinite" />
        </path>
        <path d="M105.512 56.12l-14.44-24.272c-3.716-6.008-1.996-14.093 3.843-18.062 5.835-3.97 13.588-2.322 17.306 3.68l2.6 5.274 4.52-3.76c5.84-3.97 13.592-2.32 17.307 3.68 3.718 6.003 1.998 14.088-3.842 18.064L109.74 57.02c-1.434 1.014-3.33.61-4.228-.9z" fill-opacity=".5">
            <animate attributeName="fill-opacity"
                begin="0.7s" dur="1.4s"
                values="0.5;1;0.5"
                calcMode="linear"
                repeatCount="indefinite" />
        </path>
        <path d="M67.408 57.834l-23.01-24.98c-5.864-6.15-5.864-16.108 0-22.248 5.86-6.14 15.37-6.14 21.234 0L70 16.168l4.368-5.562c5.863-6.14 15.375-6.14 21.235 0 5.863 6.14 5.863 16.098 0 22.247l-23.007 24.98c-1.43 1.556-3.757 1.556-5.188 0z" />
    </svg>
    </center>
  </v-flex>
</v-layout>  
    <v-layout v-else>

    
    <v-navigation-drawer
      :mini-variant.sync="miniVariant"
      :clipped="clipped"
      v-model="drawer"
      fixed
      app
    >
    <v-toolbar flat>
      <v-list>
        <v-list-tile>
          <v-list-tile-title class="title">
            Меню сайта
          </v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-toolbar>

    <v-divider></v-divider>
      <v-list class="">
       
        <v-list-tile
          router
          :to="item.to"
          :key="i"
          v-for="(item, i) in items"
          exact>
          <v-list-tile-action>
            <v-icon v-html="item.icon"></v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title v-text="item.title"></v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-divider></v-divider>
        <v-list-tile class="mt-5">
          <v-list-content>Ночной режим</v-list-content>
          <v-spacer></v-spacer>
          <v-switch v-model="dark"></v-switch>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar fixed app :clipped-left="clipped">
      <v-btn icon @click="drawer = !drawer">
        <v-icon>
          mdi-menu
        </v-icon>

      </v-btn>
      
      <v-toolbar-title v-text="title"></v-toolbar-title>
      
      
    </v-toolbar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer :fixed="fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
    </v-layout>
  </v-app>
</template>

<script>
  export default {
    data () {
      return {
        clipped: true,
        drawer: true,
        fixed: false,
        items: [
          { icon: 'mdi-human-male', title: 'Рамазан', to: '/' },
          { icon: 'mdi-human-female', title: 'Озода', to: '/inspire' }
        ],
        miniVariant: false,
        right: true,
        rightDrawer: false,
        title: 'Ramazan+Ozoda',
        dark: false,
        preloader: true
      }
    },
  mounted() {
    this.preloader=false
  },
  }
</script>
