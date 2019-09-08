<template>
  <div>
    <v-card class="text-xs-center py-5 mt-5 blue-grad" flat tile outlined>
      <v-card-title class="justify-center">
        <client-only>
          <div data-aos-once="true" data-aos="fade-down" data-aos-delay="200">
            <p
              class="mb-1"
              :style="{
                color: 'white',
                'font-family': 'DB Helvethaica X',
                'font-weight': 750,
                'font-size': '70px'
              }"
            >
              รีวิวจากผู้ใช้งาน
            </p>
          </div>
        </client-only>
      </v-card-title>
    </v-card>
    <v-layout row wrap justify-center>
      <v-flex xs11>
        <client-only>
          <div
            data-aos-once="true"
            data-aos="zoom-out"
            data-aos-duration="700"
            data-aos-delay="300"
          >
            <v-layout row wrap>
              <v-flex v-for="i in 4" :key="i" xs3>
                <v-img
                  max-height="500"
                  contain
                  class="mt-5 mb-1"
                  :src="require('~/assets/photo/review/1.svg')"
                />
                <p
                  class="mb-0 text-center"
                  :style="{
                    color: '#443D3D',
                    'font-family': 'DB Helvethaica X',
                    'font-weight': 'bold',
                    'font-size': '30px'
                  }"
                >
                  หัวข้อ {{ i }}
                </p>
                <p
                  class="mb-1 text-center"
                  :style="{
                    color: '#443D3D',
                    'font-family': 'DB Helvethaica X',
                    'font-weight': 'normal',
                    'font-size': '30px'
                  }"
                >
                  รายละเอียด
                </p>
              </v-flex>
            </v-layout>
          </div>
        </client-only>
      </v-flex>
      <v-flex xs12>
        <client-only>
          <div
            data-aos-once="true"
            data-aos="fade-up"
            data-aos-id="currentQuest"
            data-aos-delay="300"
          >
            <p
              class="mb-0 text-center"
              :style="{
                color: 'black',
                'font-family': 'DB Helvethaica X',
                'font-weight': 'bold',
                'font-size': '70px'
              }"
            >
              ขณะนี้มีเควสเตอร์ในระบบทั้งหมด
            </p>
            <p
              class="mb-0 text-center"
              :style="{
                color: 'black',
                'font-family': 'DB Helvethaica X',
                'font-weight': 'bold',
                'font-size': '70px'
              }"
            >
              <ICountUp
                class="iCountUp"
                :delay="delay"
                :end-val="currentQuester"
                :options="options"
                @ready="onReady"
              />
              {{ ' ' }}คน
            </p>
          </div>
        </client-only>
        <client-only>
          <div
            data-aos-once="true"
            data-aos="fade-up"
            data-aos-id="doneQuest"
            data-aos-delay="300"
          >
            <p
              class="mb-0 text-center"
              :style="{
                color: 'black',
                'font-family': 'DB Helvethaica X',
                'font-weight': 'bold',
                'font-size': '70px'
              }"
            >
              และมีเควสที่สำเร็จไปแล้วทั้งหมด
            </p>
            <p
              class="mb-0 text-center"
              :style="{
                color: 'black',
                'font-family': 'DB Helvethaica X',
                'font-weight': 'bold',
                'font-size': '70px'
              }"
            >
              <ICountUp
                :style="{
                  color: '#112D4E',
                  'line-height': '80%',
                  'font-family': 'DB Helvethaica X',
                  'font-weight': 'bold',
                  'font-size': '170px'
                }"
                :delay="delay"
                :end-val="doneQuest"
                :options="options"
                @ready="onReady2"
              />
              {{ ' ' }}เควส
            </p>
          </div>
        </client-only>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {
  data() {
    return {
      delay: 0,
      instanceCurrentQuest: null,
      currentQuester: 0,
      doneQuest: 0,
      instanceDoneQuest: null,
      options: {
        useEasing: true,
        useGrouping: true,
        separator: ',',
        decimal: '.',
        prefix: '',
        suffix: ''
      }
    };
  },
  mounted() {
    this.$nextTick(() => {
      document.addEventListener('aos:in:currentQuest', ({ detail }) => {
        this.instanceCurrentQuest == null
          ? (this.currentQuester = 200000)
          : this.instanceCurrentQuest.update(200000);
      });
      document.addEventListener('aos:in:doneQuest', ({ detail }) => {
        this.instanceDoneQuest == null
          ? (this.doneQuest = 1000000)
          : this.instanceDoneQuest.update(1000000);
      });
    });
  },
  methods: {
    onReady(instance, CountUp) {
      this.instanceCurrentQuest = instance;
    },
    onReady2(instance, CountUp) {
      this.instanceDoneQuest = instance;
    }
  }
};
</script>

<style scoped>
.iCountUp {
  color: #3f72af;
  line-height: 80%;
  font-family: 'DB Helvethaica X';
  font-weight: bold;
  font-size: 170px;
}
</style>
