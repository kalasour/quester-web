<template>
  <div class="mt-5">
    <client-only>
      <div
        data-aos-once="true"
        data-aos-duration="700"
        data-aos="fade-down"
        data-aos-delay="400"
      >
        <p
          class="mb-3 text-center"
          :style="{
            color: '#0F2F55',
            'line-height': '80%',
            'font-family': 'DB Helvethaica X',
            'font-weight': 'bold',
            'font-size': '70px'
          }"
        >
          หาคนมาทำอะไรให้ ง่ายๆ เพียง
          <span
            :style="{
              color: 'white',
              '-webkit-text-stroke': '3px #0F2F55',
              'font-family': 'DB Helvethaica X',
              'font-weight': 750,
              'font-size': '130px'
            }"
            >3</span
          >
          ขั้นตอน
        </p>
      </div>
      <v-layout row wrap justify-center>
        <v-flex xs10>
          <v-layout row wrap justify-space-between>
            <v-flex v-for="i in 3" :key="i" xs4>
              <div
                data-aos-once="true"
                data-aos-duration="700"
                :data-aos="animate[i - 1]"
                data-aos-delay="400"
              >
                <v-layout row wrap>
                  <v-flex xs4>
                    <p
                      class="mb-3 text-right"
                      :style="{
                        color: '#0F2F55',
                        'line-height': '80%',
                        'font-family': 'DB Helvethaica X',
                        'font-weight': 'bold',
                        'font-size': '130px'
                      }"
                    >
                      {{ i }}
                    </p>
                  </v-flex>
                  <v-flex xs8>
                    <v-img
                      max-height="600"
                      min-height="600"
                      contain
                      class="mt-5 mb-1"
                      :src="require(`~/assets/photo/step/${i}.svg`)"
                    />
                  </v-flex>
                </v-layout>
              </div>
              <div
                data-aos-once="true"
                data-aos-duration="700"
                :data-aos="animate[i - 1]"
                data-aos-delay="400"
              >
                <p
                  class="mb-3 text-center"
                  :style="{
                    color: '#0F2F55',
                    'line-height': '80%',
                    'font-family': 'DB Helvethaica X',
                    'font-weight': 'bold',
                    'font-size': '60px'
                  }"
                >
                  {{ steps[i - 1] }}
                </p>
              </div>
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
    </client-only>

    <client-only>
      <div
        class="mt-5"
        data-aos-once="true"
        data-aos-duration="700"
        data-aos="fade-down"
        data-aos-delay="400"
      >
        <p
          class="mb-3 text-center"
          :style="{
            color: '#0F2F55',
            'line-height': '80%',
            'font-family': 'DB Helvethaica X',
            'font-weight': 'bold',
            'font-size': '70px'
          }"
        >
          หางานทํา ง่ายๆ เพียง
          <span
            :style="{
              color: 'white',
              '-webkit-text-stroke': '3px #0F2F55',
              'font-family': 'DB Helvethaica X',
              'font-weight': 750,
              'font-size': '130px'
            }"
            >3</span
          >
          ขั้นตอน
        </p>
      </div>
      <v-layout row wrap justify-center>
        <v-flex xs10>
          <v-layout row wrap justify-space-between>
            <v-flex v-for="i in 3" :key="i" xs4>
              <div
                data-aos-once="true"
                data-aos-duration="700"
                :data-aos="animate[i + 2]"
                data-aos-delay="400"
              >
                <v-layout row wrap>
                  <v-flex xs4>
                    <p
                      class="mb-3 text-right"
                      :style="{
                        color: '#0F2F55',
                        'line-height': '80%',
                        'font-family': 'DB Helvethaica X',
                        'font-weight': 'bold',
                        'font-size': '130px'
                      }"
                    >
                      {{ i }}
                    </p>
                  </v-flex>
                  <v-flex xs8>
                    <v-img
                      max-height="600"
                      min-height="600"
                      contain
                      class="mt-5 mb-1"
                      :src="require(`~/assets/photo/step/${i + 3}.svg`)"
                    />
                  </v-flex>
                </v-layout>
              </div>
              <div
                data-aos-once="true"
                data-aos-duration="700"
                :data-aos="animate[i + 2]"
                data-aos-delay="400"
              >
                <p
                  class="mb-3 text-center"
                  :style="{
                    color: '#0F2F55',
                    'line-height': '80%',
                    'font-family': 'DB Helvethaica X',
                    'font-weight': 'bold',
                    'font-size': '60px'
                  }"
                >
                  {{ steps[i + 2] }}
                </p>
              </div>
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
    </client-only>
  </div>
</template>

<script>
export default {
  data() {
    return {
      animate: [
        'fade-right',
        'zoom-out',
        'fade-left',
        'zoom-in',
        'zoom-in',
        'zoom-in'
      ],
      steps: [
        'สร้างเควส',
        'กรอกรายละเอียด',
        'เลือกคนทำเควส',
        'เลือกเควส',
        'กรอกรายละเอียด',
        'ยืนยันทำเควส'
      ]
    };
  }
};
</script>

<style></style>
