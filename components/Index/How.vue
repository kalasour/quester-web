<template>
  <div class="mt-5 pa-4">
    <div data-aos-once="true" data-aos-duration="400" data-aos="fade-down" data-aos-delay="200">
      <p
        class="mb-3 text-center"
        :style="{
            color: '#0F2F55',
            'line-height': '80%',
            'font-family': 'DB Helvethaica X Bd',
            'font-weight': 'bold',
            'font-size': '3em'
          }"
      >
        หาคนมาทำอะไรให้ ง่ายๆ เพียง
        <span
          :style="{
              color: 'white',
              '-webkit-text-stroke': '3px #0F2F55',
              'font-family': 'DB Helvethaica X Bd',
              'font-size': '1.5em'
            }"
        >3</span>
        ขั้นตอน
      </p>
    </div>
    <v-row>
      <v-col v-for="i in 3" :key="i" md="4">
        <div
          data-aos-once="true"
          data-aos-duration="400"
          :data-aos="animate[i - 1]"
          data-aos-delay="200"
        >
          <p
            class="mb-3 text-center"
            :style="{
                        color: '#0F2F55',
                        'line-height': '80%',
                        'font-family': 'DB Helvethaica X Bd',
                        'font-weight': 'bold',
                        'font-size': '130px'
                      }"
          >{{ i }}</p>
          <div
            data-aos-once="true"
            data-aos-duration="400"
            :data-aos="animate[i + 2]"
            data-aos-delay="200"
          >
            <v-img
              max-height="600"
              min-height="600"
              contain
              class="mb-1"
              :src="require(`~/assets/photo/step/${i}.svg`)"
            />
          </div>
        </div>
        <div
          data-aos-once="true"
          data-aos-duration="400"
          :data-aos="animate[i - 1]"
          data-aos-delay="200"
        >
          <p class="mb-3 text-center how-to-text">{{ steps[i] }}</p>
        </div>
        <v-divider class="d-md-none mt-12"></v-divider>
      </v-col>
    </v-row>

    <v-divider class="my-10"></v-divider>

    <div
      class="mt-5"
      data-aos-once="true"
      data-aos-duration="400"
      data-aos="fade-down"
      data-aos-delay="200"
    >
      <p
        class="mb-3 text-center"
        :style="{
            color: '#0F2F55',
            'line-height': '80%',
            'font-family': 'DB Helvethaica X Bd',
            'font-weight': 'bold',
            'font-size': '3em'
          }"
      >
        หางานทํา ง่ายๆ เพียง
        <span
          :style="{
              color: 'white',
              '-webkit-text-stroke': '3px #0F2F55',
              'font-family': 'DB Helvethaica X Bd',
              'font-size': '1.5em'
            }"
        >3</span>
        ขั้นตอน
      </p>
    </div>

    <v-row>
      <v-col v-for="i in 3" :key="i" md="4">
        <div
          data-aos-once="true"
          data-aos-duration="400"
          :data-aos="animate[i + 2]"
          data-aos-delay="200"
        >
          <p
            class="text-center"
            :style="{
                        color: '#0F2F55',
                        'line-height': '80%',
                        'font-family': 'DB Helvethaica X Bd',
                        'font-weight': 'bold',
                        'font-size': '130px'
                      }"
          >{{ i }}</p>
        </div>
        <div
          data-aos-once="true"
          data-aos-duration="400"
          :data-aos="animate[i + 2]"
          data-aos-delay="200"
        >
          <v-img
            max-height="600"
            min-height="600"
            contain
            class="mb-1"
            :src="require(`~/assets/photo/step/${i + 3}.svg`)"
          />
        </div>

        <div
          data-aos-once="true"
          data-aos-duration="400"
          :data-aos="animate[i + 2]"
          data-aos-delay="200"
        >
          <p class="mb-3 text-center how-to-text">{{ steps[i + 2] }}</p>
        </div>

        <v-divider class="d-md-none mt-12"></v-divider>
      </v-col>
    </v-row>
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

<style>
.how-to-text {
  color: #0f2f55;
  line-height: 80%;
  font-family: 'DB Helvethaica X Bd';
  font-weight: bold;
  font-size: 60px;
}
</style>
