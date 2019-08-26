<template >
  <v-layout id="index" :style="{height:screenWidth}" row wrap justify-center align-center>
    <v-flex xs10>
      <v-layout row wrap justify-space-around align-center>
        <v-flex xs5>
          <v-layout column wrap justify-center align-center>
            <span
              class="display-2"
              :style="{ 'font-family': 'SF Pro Display','font-weight':700, 'color':'#112D4E' }"
            >REAL QUEST</span>
            <span
              class="display-2 mb-3"
              :style="{ 'font-family': 'SF Pro Display','font-weight':700, 'color':'#112D4E' }"
            >IN REAL LIFE</span>
            <span
              class="subtitle-1 mt-2"
              :style="{ 'font-family': 'SF Pro Display','font-weight':300, 'color':'grey' }"
            >Lorem ipsum dolor sit amet, consectetur</span>
            <span
              class="subtitle-1"
              :style="{ 'font-family': 'SF Pro Display','font-weight':300, 'color':'grey' }"
            >consectetur adipiscing elit. Suspendisse a felis felis. Aliquam</span>
            <span
              class="subtitle-1"
              :style="{ 'font-family': 'SF Pro Display','font-weight':300, 'color':'grey' }"
            >erat volutpat. Duis tincidunt pretium odio, et</span>
            <span
              class="subtitle-1"
              :style="{ 'font-family': 'SF Pro Display','font-weight':300, 'color':'grey' }"
            >vestibulum elit molestie ut.</span>
          </v-layout>
          <v-layout class="mt-5" row wrap justify-center>
            <v-flex xs4>
              <v-img :src="require('../assets/logo/app-store.svg')" />
            </v-flex>
            <v-flex xs4>
              <v-img :src="require('../assets/logo/google-play.svg')" />
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex xs5 :style="{position:'relative'}">
          <v-img
            max-height="450"
            contain
            :src="require('../assets/logo/iphone.svg')"
            :style="{position:'absolute',left:'45%',top:'5%'
            }"
          />
          <v-img max-height="500" contain :src="require('../assets/logo/iphone.svg')" />
        </v-flex>
      </v-layout>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  beforeMount() {
    this.screenWidth = `${window.innerHeight}px`
  },
  components: {
    Logo,
    VuetifyLogo
  },
  data() {
    return {
      screenWidth: null
    }
  }
}
</script>
<style>
span.SFProDisplay {
  font-style: 'SF Pro Display';
}
</style>
