<template>
  <div>
    <v-card class="text-xs-center py-5 blue-grad mt-5" tile outlined>
      <v-card-title class="justify-center">
        <span
          data-aos="fade-bottom"
          data-aos-delay="200"
          :style="{ color: 'white','font-family': 'DB Helvethaica X','font-weight': 750,'font-size':'40px' }"
        >จะดีกว่าไหม ถ้าคุณจะได้เป็นทั้งผู้รับจ้างและจ้างเองในเวลาเดียวกัน</span>
      </v-card-title>
    </v-card>
    <v-layout row wrap fill-height align-center>
      <v-flex xs5 data-aos="fade-bottom" data-aos-delay="200">
        <p
          class="text-center mb-0"
          :style="{ color: '#0f2f55','font-family': 'DB Helvethaica X','font-weight': 750,'font-size':'40px' }"
        >จ้างคนมาทําอะไรให้ก็ได้</p>
        <p
          class="text-center mb-0"
          :style="{ color: '#0f2f55','font-family': 'DB Helvethaica X','font-weight': 750,'font-size':'40px' }"
        >เพียงแค่สร้าง "เควส"</p>
        <p
          class="text-center mb-0"
          :style="{ color: '#0f2f55','font-family': 'DB Helvethaica X','font-weight': 750,'font-size':'40px' }"
        >เพื่อหาผู้ที่จะทําเควสให้คุณได้สําเร็จ</p>
      </v-flex>
      <v-flex xs7 align-self-end class="my-3" data-aos="fade-right" data-aos-delay="200">
        <v-img contain :src="require('~/assets/photo/sushi.svg')" />
      </v-flex>
      <v-flex xs7 class="my-3" data-aos="fade-left" data-aos-delay="200">
        <v-img contain :src="require('~/assets/photo/pizza.png')" />
      </v-flex>
      <v-flex xs5 data-aos="fade-bottom" data-aos-delay="200">
        <p
          class="text-center mb-0"
          :style="{ color: '#0f2f55','font-family': 'DB Helvethaica X','font-weight': 750,'font-size':'40px' }"
        >รับงานที่อยู่ในรูปแบบ"เควส"</p>
        <p
          class="text-center mb-0"
          :style="{ color: '#0f2f55','font-family': 'DB Helvethaica X','font-weight': 750,'font-size':'40px' }"
        >สนุกเหมือนได้เล่นเกม แต่ได้เงินจริง!</p>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {}
</script>

<style>
</style>