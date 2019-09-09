<template>
  <v-container class="screen-height">
    <v-row :justify="justify-center" :align="align-center">
      <v-col md="6" sm="12" class="d-flex align-center text-center">
        <div data-aos="fade-right" data-aos-delay="500">
          <p
            class="display-2"
            :style="{
                'font-family': 'SF Pro Display',
                'font-weight': 700,
                color: '#112D4E'
              }"
          >REAL QUEST</p>
          <p
            class="display-2 mb-3"
            :style="{
                'font-family': 'SF Pro Display',
                'font-weight': 700,
                color: '#112D4E'
              }"
          >IN REAL LIFE</p>
          <p
            class="subtitle-1 mt-2"
            :style="{
                'font-family': 'SF Pro Display',
                'font-weight': 300,
                color: 'grey'
              }"
          >Lorem ipsum dolor sit amet, consectetur</p>
          <p
            class="subtitle-1"
            :style="{
                'font-family': 'SF Pro Display',
                'font-weight': 300,
                color: 'grey'
              }"
          >adipiscing elit. Suspendisse a felis felis. Aliquam</p>
          <p
            class="subtitle-1"
            :style="{
                'font-family': 'SF Pro Display',
                'font-weight': 300,
                color: 'grey'
              }"
          >erat volutpat. Duis tincidunt pretium odio, et</p>
          <p
            class="subtitle-1"
            :style="{
                'font-family': 'SF Pro Display',
                'font-weight': 300,
                color: 'grey'
              }"
          >vestibulum elit molestie ut.</p>
        </div>
      </v-col>
      <v-col md="6" sm="12">
        <div data-aos="fade-up" data-aos-delay="500">
          <v-img max-height="500" contain :src="require('~/assets/photo/phone_2.svg')" />
        </div>
        <div>
          <v-row class="d-flex justify-center align-self-center">
            <v-col md="6" sm="12" class="d-flex justify-center">
              <v-img :src="require('~/assets/logo/app-store.svg')" />
            </v-col>
            <v-col md="6" sm="12" class="d-flex justify-center">
              <v-img :src="require('~/assets/logo/google-play.svg')" />
            </v-col>
          </v-row>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {};
</script>

<style scoped>
.screen-height {
  min-height: 100%;
}

p {
  margin-bottom: 0px !important;
}
</style>
