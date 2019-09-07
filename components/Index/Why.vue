<template>
  <div>
    <v-card class="text-xs-center py-5 blue-grad mt-5" tile outlined>
      <v-card-title class="justify-center">
        <div data-aos="fade-bottom" data-aos-delay="200" data-aos-once="true">
          <span
            :style="{ color: 'white','font-family': 'DB Helvethaica X','font-weight': 750,'font-size':'40px' }"
          >จะดีกว่าไหม ถ้าคุณจะได้เป็นทั้งผู้รับจ้างและจ้างเองในเวลาเดียวกัน</span>
        </div>
      </v-card-title>
    </v-card>
    <v-layout row wrap fill-height align-center>
      <v-flex xs5>
        <client-only>
          <div data-aos-once="true" data-aos="fade-up" data-aos-id="label1" data-aos-delay="200">
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
          </div>
        </client-only>
      </v-flex>
      <client-only>
        <v-flex
          xs7
          align-self-end
          class="my-3"
          data-aos-once="true"
          data-aos="fade-left"
          data-aos-delay="200"
        >
          <v-img contain :src="require('~/assets/photo/sushi.svg')" />
        </v-flex>
      </client-only>
      <client-only>
        <v-flex xs7 class="my-3" data-aos="fade-right" data-aos-once="true" data-aos-delay="200">
          <v-img contain :src="require('~/assets/photo/sushi.svg')" />
        </v-flex>
      </client-only>
      <v-flex xs5>
        <client-only>
          <div data-aos-once="true" data-aos="fade-up" data-aos-id="label2" data-aos-delay="200">
            <p
              class="text-center mb-0"
              :style="{ color: '#0f2f55','font-family': 'DB Helvethaica X','font-weight': 750,'font-size':'40px' }"
            >รับงานที่อยู่ในรูปแบบ"เควส"</p>
            <p
              class="text-center mb-0"
              :style="{ color: '#0f2f55','font-family': 'DB Helvethaica X','font-weight': 750,'font-size':'40px' }"
            >สนุกเหมือนได้เล่นเกม แต่ได้เงินจริง!</p>
          </div>
        </client-only>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {}
</script>

<style>
</style>