<template>
  <div>
    <v-card class="text-xs-center py-5 blue-grad mt-5" tile outlined>
      <v-card-title class="justify-center">
        <div data-aos="fade-bottom" data-aos-delay="200" data-aos-once="true">
          <p
            class="text-center"
            :style="{
              color: 'white',
              'font-family': 'DB Helvethaica X Bd',
              'font-size': '2em'
            }"
          >จะดีกว่าไหม ถ้าคุณจะได้เป็นทั้งผู้รับจ้างและจ้างเองในเวลาเดียวกัน</p>
        </div>
      </v-card-title>
    </v-card>
    <v-row class="d-flex align-center">
      <v-col md="6" sm="12">
        <div data-aos-once="true" data-aos="fade-up" data-aos-id="label1" data-aos-delay="200">
          <p
            class="text-center mb-0"
            :style="{
                color: '#0f2f55',
                'font-family': 'DB Helvethaica X Bd',
                'font-weight': 750,
                'font-size': '40px'
              }"
          >จ้างคนมาทําอะไรให้ก็ได้</p>
          <p
            class="text-center mb-0"
            :style="{
                color: '#0f2f55',
                'font-family': 'DB Helvethaica X Bd',
                'font-weight': 750,
                'font-size': '40px'
              }"
          >เพียงแค่สร้าง "เควส"</p>
          <p
            class="text-center mb-0"
            :style="{
                color: '#0f2f55',
                'font-family': 'DB Helvethaica X Bd',
                'font-weight': 750,
                'font-size': '40px'
              }"
          >เพื่อหาผู้ที่จะทําเควสให้คุณได้สําเร็จ</p>
        </div>
      </v-col>
      <v-col
        md="6"
        sm="12"
        class="my-3 align-self-end"
        data-aos-once="true"
        data-aos="fade-left"
        data-aos-delay="200"
      >
        <v-img contain :src="require('~/assets/photo/sushi.svg')" />
      </v-col>
    </v-row>
    <v-row>
      <v-col
        md="6"
        sm="12"
        class="my-3"
        data-aos="fade-right"
        data-aos-once="true"
        data-aos-delay="200"
      >
        <v-img contain :src="require('~/assets/photo/sushi.svg')" />
      </v-col>
      <v-col md="6" sm="12" class="d-flex justify-center align-center">
        <div data-aos-once="true" data-aos="fade-up" data-aos-id="label2" data-aos-delay="200">
          <p
            class="text-center mb-0"
            :style="{
                color: '#0f2f55',
                'font-family': 'DB Helvethaica X Bd',
                'font-weight': 750,
                'font-size': '40px'
              }"
          >รับงานที่อยู่ในรูปแบบ"เควส"</p>
          <p
            class="text-center mb-0"
            :style="{
                color: '#0f2f55',
                'font-family': 'DB Helvethaica X Bd',
                'font-weight': 750,
                'font-size': '40px'
              }"
          >สนุกเหมือนได้เล่นเกม แต่ได้เงินจริง!</p>
        </div>
      </v-col>
    </v-row>

    <v-card class="text-xs-center py-5 mt-2 blue-grad" flat tile outlined>
      <v-card-title class="justify-center">
        <client-only>
          <div data-aos-once="true" data-aos="fade-down" data-aos-delay="200">
            <p
              class="mb-1 text-center"
              :style="{
                color: 'white',
                'font-family': 'DB Helvethaica X Bd',
                'font-size': '2em'
              }"
            >อิสรภาพในการจ้างงาน</p>
          </div>
        </client-only>
      </v-card-title>
    </v-card>
    <v-layout row wrap justify-center class="pb-3" :style="{ 'border-bottom': '2px solid grey' }">
      <v-flex xs10>
        <v-row class="d-flex justify-center">
          <v-col v-for="i in 3" :key="i" md="4" sm="12" class="align-self-start">
            <div
              data-aos-once="true"
              data-aos="zoom-out"
              data-aos-duration="700"
              data-aos-delay="300"
            >
              <v-img
                height="300"
                contain
                class="mt-5 mb-1"
                :src="require(`~/assets/photo/freedom/${i}.svg`)"
              />

              <p
                class="py-3 text-center"
                :style="{
                    color: '#0F2F55',
                    'line-height': '80%',
                    'font-family': 'DB Helvethaica X Bd',
                    'font-weight': 'bold',
                    'font-size': '3em'
                  }"
              >{{ heads[i - 1] }}</p>
              <p
                class="mb-1 text-center px-5"
                :style="{
                    color: '#0F2F55',
                    'font-family': 'DB Helvethaica X Bd',
                    'font-weight': 'normal',
                    'font-size': '24px'
                  }"
              >{{ details[i - 1] }}</p>
            </div>
          </v-col>
        </v-row>
      </v-flex>
      <v-flex xs10>
        <client-only></client-only>
      </v-flex>
    </v-layout>
    <v-card class="text-xs-center py-5" color="white" tile>
      <v-card-title class="justify-center">
        <client-only>
          <div data-aos-once="true" data-aos="fade-down" data-aos-delay="200">
            <p
              class="mb-1"
              :style="{
                color: '#112D4E',
                'font-family': 'DB Helvethaica X Bd',
                'font-size': '2em'
              }"
            >อิสรภาพในการทำงาน</p>
          </div>
        </client-only>
      </v-card-title>
    </v-card>
    <div class="sky-grad">
      <v-row class="d-flex justify-center pa-10">
        <v-col v-for="i in 3" :key="i" md="4" sm="12">
          <div
            data-aos-once="true"
            data-aos="zoom-out"
            data-aos-duration="700"
            data-aos-delay="300"
          >
            <v-img
              max-height="300"
              min-height="300"
              contain
              class="mt-5 mb-1"
              :src="require(`~/assets/photo/freedom/${i + 3}.svg`)"
            />
            <p
              class="mb-3 text-center"
              :style="{
                    color: 'white',
                    'line-height': '80%',
                    'font-family': 'DB Helvethaica X Bd',
                    'font-weight': 'bold',
                    'font-size': '3em'
                  }"
            >{{ heads[i + 2] }}</p>
            <p
              class="mb-1 text-center px-5"
              :style="{
                    color: 'white',
                    'font-family': 'DB Helvethaica X Bd',
                    'font-weight': 'normal',
                    'font-size': '24px'
                  }"
            >{{ details[i + 2] }}</p>
          </div>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      heads: [
        'หาคนมาทำอะไรก็ได้',
        '(ไม่ใช่)ใครก็ได้',
        '(ไม่ใช่)ที่ไหนก็ได้',
        'มีงานทุกประเภท',
        'งานใกล้ตัว',
        'เสนอเงินเพิ่มได้'
      ],
      details: [
        'เรื่องเล็กๆน้อยๆของผู้อื่น อาจจะเป็นเรื่องที่คุณต้องการความช่วยเหลือ เช่น การจับสัตว์ที่คุณไม่ชอบให้ออกไปจากห้องของคุณ เราเข้าใจและพร้อมช่วยหาคนมาช่วยเหลือคุณ',
        'เบื่อไหม กับการที่จะจ้างใครแล้วไม่มั่นใจว่าจะทำได้หรือไม่ หรืออยากจะเลือกด้วยตัวเอง เราให้คุณเลือกผู้ที่จะมาทำงานให้คุณได้เต็มที่',
        'เราพร้อมหาคนที่อยู่ใกล้ๆกับคุณ มาช่วยเหลือคุณได้ เพื่อความสะดวกทั้งคุณและผู้รับจ้าง เราเชื่อว่าคุณก็อยากได้คนที่มาทำงานให้คุณได้เร็วที่สุด',
        'งานในแอพนี้มีความอิสระสูง มีทั้งงานง่ายสุดๆ ทำเอาสนุก ไปจนถึงงานที่ต้องใช้ความสามารถเฉพาะ ให้เลือกตามความถนัด และความต้องการได้แน่นอน ',
        'เราพร้อมหางานที่ใกล้กับตัวคุณมากที่สุด ทำให้คุณไม่ต้องเสียเวลาเดินทางไกลๆ ให้คุณเอาเวลาไปทำงานอื่นเพิ่มดีกว่า',
        'เราเชื่อว่ามีหลายงานที่เหมาะสมกับคุณ แต่ราคากลับไม่ถูกใจคุณ เราไม่อยากให้คุณและผู้จ้างเสียโอกาสที่จะทำงานดีๆไป คุณสามารถเสนอเงินที่ต้องการให้ผู้จ้างเพื่อพิจารณาต่อไปได้'
      ]
    };
  }
};
</script>

<style></style>
