<template>
  <v-app dark>
    <!-- <template v-if="['/en/portfolio'].indexOf($route.name) > -1" >
    </template> -->
    <v-container>
      <nuxt/>
    </v-container>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'bubble_chart',
          title: 'Portfolio',
          to: '/portfolio'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
