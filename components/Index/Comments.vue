<template>
  <client-only>
    <v-layout row wrap justify-center>
      <v-flex xs12>
        <div
          data-aos-once="true"
          data-aos-duration="700"
          data-aos="fade-down"
          data-aos-delay="400"
        >
          <p
            class="text-center mt-5"
            :style="{
              color: 'white',
              'font-family': 'DB Helvethaica X',
              'font-weight': 750,
              'font-size': '50px'
            }"
          >
            สร้างเควสของคุณวันนี้ เพื่อความสะดวกสบายในชีวิต โหลดเลย
          </p>
        </div>
      </v-flex>
      <v-flex xs12 class="mt-3 mb-5">
        <v-layout row wrap justify-center>
          <v-flex xs3>
            <div
              data-aos-once="true"
              data-aos-duration="700"
              data-aos="fade-right"
              data-aos-delay="400"
            >
              <v-img contain :src="require('~/assets/logo/app-store.svg')" />
            </div>
          </v-flex>
          <v-flex xs3>
            <div
              data-aos-once="true"
              data-aos-duration="700"
              data-aos="fade-left"
              data-aos-delay="400"
            >
              <v-img contain :src="require('~/assets/logo/google-play.svg')" />
            </div>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex xs12>
        <div
          data-aos-once="true"
          data-aos-duration="700"
          data-aos="zoom-in"
          data-aos-delay="400"
        >
          <p
            class="text-center mt-5 mb-0"
            :style="{
              color: 'white',
              'line-height': '80%',
              'font-family': 'DB Helvethaica X',
              'font-weight': 350,
              'font-size': '50px'
            }"
          >
            เพิ่มข้อคิดเห็น
          </p>
        </div>
      </v-flex>
      <v-flex xs12>
        <div
          data-aos-once="true"
          data-aos-duration="700"
          data-aos="zoom-in"
          data-aos-delay="400"
        >
          <p
            class="text-center mt-0"
            :style="{
              color: 'white',
              'font-family': 'DB Helvethaica X',
              'font-weight': 150,
              'font-size': '32px'
            }"
          >
            เพื่อไปสู่การเป็นแอปพลิเคชันที่ดีที่สุดของทุกคน
          </p>
        </div>
      </v-flex>
      <v-flex xs6 align-self-end>
        <div
          data-aos-once="true"
          data-aos-duration="700"
          data-aos="zoom-in"
          data-aos-delay="400"
        >
          <v-text-field
            dark
            type="email"
            color="grey"
            :style="{
              color: 'white',
              'font-family': 'DB Helvethaica X',
              'font-weight': 350,
              'font-size': '26px'
            }"
            name="input-7-1"
            hide-details
            placeholder="อีเมลของคุณ"
          ></v-text-field>
          <v-textarea
            dark
            color="grey"
            hide-details
            auto-grow
            rows="6"
            :style="{
              'border-bottom': '1px solid red',
              color: 'white',
              'font-family': 'DB Helvethaica X',
              'font-weight': 350,
              'font-size': '22px'
            }"
            name="input-7-1"
            placeholder="เพิ่มข้อคิดเห็น..."
          ></v-textarea>
          <v-layout row wrap justify-end>
            <v-btn
              :style="{
                color: 'white',
                'font-family': 'DB Helvethaica X',
                'font-weight': 350,
                'font-size': '22px'
              }"
              color="white"
              class="mt-5"
              rounded
              outlined
              >ส่งข้อคิดเห็น</v-btn
            >
          </v-layout>
        </div>
      </v-flex>
    </v-layout>
  </client-only>
</template>

<script>
export default {}
</script>

<style></style>
