<template>
  <div :style="{'width':'100%'}">
    <v-layout :style="{'height':'50px'}"></v-layout>
    <v-layout id="index" row wrap justify-center align-center>
      <v-flex xs8>
        <Intro />
      </v-flex>
    </v-layout>
    <v-layout id="why" row wrap justify-center align-start>
      <v-flex xs12 class="mt-5">
        <Why />
      </v-flex>
    </v-layout>
    <v-layout id="how" row wrap justify-center align-start>
      <v-flex xs12 class="pt-5">
        <How class="pt-5" />
      </v-flex>
    </v-layout>
    <v-layout id="news" row wrap justify-center align-start>
      <v-flex xs12 class="mt-5">
        <News />
      </v-flex>
    </v-layout>
    <v-layout id="what" row wrap justify-center align-start>
      <v-flex xs12 class="mt-5">
        <!-- <What /> -->
      </v-flex>
    </v-layout>
    <v-layout class="blue-grad-bot" id="comment" wrap justify-center align-start>
      <v-flex>
        <Comment class="pt-5" />
      </v-flex>
    </v-layout>
    <v-layout id="contact" row wrap justify-center align-start>
      <v-flex xs12>
        <!-- <Contact /> -->
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue';
import VuetifyLogo from '~/components/VuetifyLogo.vue';
import Intro from '~/components/Index/Intro';
import Why from '~/components/Index/Why';
import How from '~/components/Index/How';
import News from '~/components/Index/News';
import What from '~/components/Index/WhatIsPage';
import Comment from '~/components/Index/Comments';
import Contact from '~/components/Index/Contact';
export default {
  components: {
    Logo,
    VuetifyLogo,
    Intro,
    Why,
    How,
    News,
    What,
    Comment,
    Contact
  },
  data() {
    return {
      screenHeight: null
    };
  },
  beforeMount() {
    this.screenHeight = `${window.innerHeight}px`;
  }
};
</script>

<style>
</style>
