<template>
  <v-layout row wrap justify-space-around align-center>
    <v-flex xs5>
      <v-layout
        column
        wrap
        justify-center
        align-center
        data-aos="fade-right"
        data-aos-delay="500"
      >
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
        >adipiscing elit. Suspendisse a felis felis. Aliquam</span>
        <span
          class="subtitle-1"
          :style="{ 'font-family': 'SF Pro Display','font-weight':300, 'color':'grey' }"
        >erat volutpat. Duis tincidunt pretium odio, et</span>
        <span
          class="subtitle-1"
          :style="{ 'font-family': 'SF Pro Display','font-weight':300, 'color':'grey' }"
        >vestibulum elit molestie ut.</span>
      </v-layout>
      <v-layout
        data-aos="fade-left"
        data-aos-delay="500"
        class="mt-5"
        row
        wrap
        justify-center
      >
        <v-flex xs4>
          <v-img :src="require('~/assets/logo/app-store.svg')" />
        </v-flex>
        <v-flex xs4>
          <v-img :src="require('~/assets/logo/google-play.svg')" />
        </v-flex>
      </v-layout>
    </v-flex>
    <v-flex
      xs6
      data-aos="fade-up"
      data-aos-delay="500"
    >
      <!-- <v-img
        max-height="450"
        contain
        :src="require('~/assets/logo/iphone.svg')"
        :style="{position:'absolute',left:'45%',top:'5%'
            }"
      /> -->
      <v-img max-height="500" contain :src="require('~/assets/photo/phone_2.svg')" />
    </v-flex>
  </v-layout>
</template>

<script>
export default {}
</script>

<style>
</style>
 