<template>
  <v-footer id="footer" light color="white" class="text-xs-center">
    <v-layout row justify-center wrap align-center>
      <v-flex class="my-5" xs12>
        <v-img
          max-height="125"
          contain
          :src="require('../assets/logo/logo-dark.svg')"
        />
        <v-layout row wrap justify-center></v-layout>
      </v-flex>
      <v-flex class="my-5" xs12>
        <v-layout row wrap justify-center>
          <v-flex xs3>
            <v-layout row wrap justify-space-around>
              <v-flex xs2>
                <v-img
                  max-height="50"
                  contain
                  :src="require('../assets/logo/facebook.svg')"
                />
              </v-flex>
              <v-divider
                :style="{ 'border-left': '2px solid grey' }"
                vertical
              ></v-divider>
              <v-flex xs2>
                <v-img
                  max-height="50"
                  contain
                  :src="require('../assets/logo/line.svg')"
                />
              </v-flex>
              <v-divider
                :style="{ 'border-left': '2px solid grey' }"
                vertical
              ></v-divider>
              <v-flex xs2>
                <v-img
                  max-height="50"
                  contain
                  :src="require('../assets/logo/ig.svg')"
                />
              </v-flex>
            </v-layout>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex class="mt-5" xs5 align-self-center>
        <v-layout row wrap justify-center>
          <v-flex xs10>
            <v-layout row wrap justify-space-around>
              <v-flex xs4>
                <v-layout column wrap justify-center>
                  <span
                    v-for="(i, index) in itemsLeft"
                    :key="index"
                    :style="{
                      color: '#112D4E',
                      'font-family': i.font,
                      'font-size': '23px'
                    }"
                    >{{ i.text }}</span
                  >
                </v-layout>
              </v-flex>
              <v-divider
                :style="{ 'border-left': '1px solid #112D4E' }"
                vertical
              ></v-divider>
              <v-flex xs4>
                <v-layout column wrap justify-center>
                  <span
                    v-for="(i, index) in itemsRight"
                    :key="index"
                    :style="{
                      color: '#112D4E',
                      'font-family': i.font,
                      'font-size': '22px'
                    }"
                    >{{ i.text }}</span
                  >
                </v-layout>
              </v-flex>
            </v-layout>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex xs10 class="mt-5">
        <!-- <v-layout row wrap justify-center>
          <v-flex xs2>
            <v-img :src="require('../assets/logo/app-store.svg')" />
          </v-flex>
          <v-flex xs2>
            <v-img :src="require('../assets/logo/google-play.svg')" />
          </v-flex>
        </v-layout> -->
      </v-flex>
      <v-flex xs11>
        <hr class="mt-3" />
      </v-flex>
      <v-flex xs12 class="my-2">
        <v-layout row wrap justify-center>
          <span
            class="no"
            :style="{
              color: '#112D4E',
              'font-family': 'SF Pro Display',
              'font-weight': 350
            }"
            >Copyright &copy; 2019 Quester co., ltd All rights reserved</span
          >
        </v-layout>
      </v-flex>
    </v-layout>
  </v-footer>
</template>
<style scoped>
span:hover {
  cursor: pointer;
  text-decoration: underline;
}
span.no:hover {
  cursor: text;
  text-decoration: none;
}
</style>
<script>
export default {
  components: {},
  data() {
    return {
      itemsLeft: [
        { text: 'Quester', font: 'SF Pro Display' },
        { text: 'เกี่ยวกับเรา', font: 'DB Helvethaica X' },
        { text: 'ทําไมต้อง Quester?', font: 'DB Helvethaica X' },
        { text: 'วิธีการใช้งาน', font: 'DB Helvethaica X' },
        { text: 'รีวิวจากผู้ใช้งาน', font: 'DB Helvethaica X' },
        { text: 'แจ้งปัญหา/เพิ่มข้อคิดเห็น', font: 'DB Helvethaica X' }
      ],
      itemsRight: [
        { text: 'คําถามที่พบบ่อย', font: 'DB Helvethaica X' },
        { text: 'เงื่อนไขการใช้บริการ', font: 'DB Helvethaica X' },
        { text: 'ข้อกําหนดในการให้บริการ', font: 'DB Helvethaica X' },
        { text: 'นโยบายความเป็นส่วนตัว', font: 'DB Helvethaica X' },
        { text: 'ร่วมงานกับเรา', font: 'DB Helvethaica X' },
        { text: 'คู่มือการใช้งาน', font: 'DB Helvethaica X' }
      ]
    };
  }
};
</script>
