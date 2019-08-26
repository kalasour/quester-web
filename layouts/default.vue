<template>
  <v-app>
    <Navbar />
    <v-content :style="{'background-color':'#F9F7F7'}" >
      <v-layout class="py-0">
        <nuxt />
      </v-layout>
    </v-content>
    <Footer />
  </v-app>
</template>
<script>
import Footer from '../components/Footer'
import Navbar from '../components/Navbar'
export default {
  components: {
    Footer,
    Navbar
  },
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
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
