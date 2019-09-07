<template>
  <div>
    <v-card class="text-xs-center py-5 mt-5 blue-grad" flat tile outlined>
      <v-card-title class="justify-center">
        <p
          class="mb-1"
          :style="{ color: 'white','font-family': 'DB Helvethaica X','font-weight': 750,'font-size':'70px'  }"
        >รีวิวจากผู้ใช้งาน</p>
      </v-card-title>
    </v-card>
    <v-layout row wrap justify-center>
      <v-flex xs11>
        <v-layout row wrap>
          <v-flex xs3 v-for="i in 4" :key="i">
            <v-img
              max-height="500"
              contain
              class="mt-5 mb-1"
              :src="require('~/assets/photo/review/1.svg')"
            />
            <p
              class="mb-0 text-center"
              :style="{ color: '#443D3D','font-family': 'DB Helvethaica X','font-weight': 'bold','font-size':'30px'  }"
            >หัวข้อ {{i}}</p>
            <p
              class="mb-1 text-center"
              :style="{ color: '#443D3D','font-family': 'DB Helvethaica X','font-weight': 'normal','font-size':'30px'  }"
            >รายละเอียด</p>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex xs12>
        <p
          class="mb-0 text-center"
          :style="{ color: 'black','font-family': 'DB Helvethaica X','font-weight': 'bold','font-size':'70px'  }"
        >ขณะนี้มีเควสเตอร์ในระบบทั้งหมด</p>
        <p
          class="mb-0 text-center"
          :style="{ display:'inline',color: 'black','font-family': 'DB Helvethaica X','font-weight': 'bold','font-size':'70px'  }"
        >
          <client-only>
            <div
              data-aos-once="true"
              data-aos="fade-up"
              data-aos-id="currentQuest"
              data-aos-delay="200"
            >
              <ICountUp
                class="iCountUp"
                :delay="delay"
                :endVal="currentQuester"
                :options="options"
                @ready="onReady"
              />
              {{' '}}คน
            </div>
          </client-only>
        </p>
        <p
          class="mb-0 text-center"
          :style="{ color: 'black','font-family': 'DB Helvethaica X','font-weight': 'bold','font-size':'70px'  }"
        >และมีเควสที่สำเร็จไปแล้วทั้งหมด</p>
        <p
          class="mb-0 text-center"
          :style="{ color: 'black','font-family': 'DB Helvethaica X','font-weight': 'bold','font-size':'70px'  }"
        >
          <client-only>
            <div
              data-aos-once="true"
              data-aos="fade-up"
              data-aos-id="doneQuest"
              data-aos-delay="200"
            >
              <ICountUp
                :style="{ color: '#112D4E','line-height': '80%','font-family': 'DB Helvethaica X','font-weight': 'bold','font-size':'170px'  }"
                :delay="delay"
                :endVal="doneQuest"
                :options="options"
                @ready="onReady2"
              />
              {{' '}}เควส
            </div>
          </client-only>
        </p>
      </v-flex>
    </v-layout>
  </div>
</template>

<script >
export default {
  mounted() {
    this.$nextTick(() => {
      document.addEventListener('aos:in:currentQuest', ({ detail }) => {
        this.instanceCurrentQuest == null
          ? (this.currentQuester = 200000)
          : this.instanceCurrentQuest.update(200000)
      })
      document.addEventListener('aos:in:doneQuest', ({ detail }) => {
        this.instanceDoneQuest == null
          ? (this.doneQuest = 1000000)
          : this.instanceDoneQuest.update(1000000)
      })
    })
  },
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
    }
  },
  methods: {
    onReady: function(instance, CountUp) {
      const that = this
      this.instanceCurrentQuest = instance
    },
    onReady2: function(instance, CountUp) {
      const that = this
      this.instanceDoneQuest = instance
    }
  }
}
</script>

<style scoped>
.iCountUp {
  display: inline;
  color: #3f72af;
  line-height: 80%;
  font-family: 'DB Helvethaica X';
  font-weight: bold;
  font-size: 170px;
}
</style>
