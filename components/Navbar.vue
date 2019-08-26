<template>
  <div>
    <v-app-bar
      fixed
      flat
      class="py-1 pr-5"
      color="#112D4E"
      dark
      
    >
      <v-img
        max-width="100"
        max-height="50"
        contain
        :src="require('../assets/logo/quester-logo-trans.svg')"
      />
      <v-toolbar-title>
        <span
          :style="{ 'font-family': 'SF Pro Display','font-weight': 750,'font-size':'30px' }"
        >Quester</span>
      </v-toolbar-title>

      <div class="flex-grow-1"></div>

      <v-btn text v-for="(item,index) in items" :key="index">
        <span :style="{ 'font-family': item.font ,'font-size':'28px' }">{{item.text}}</span>
      </v-btn>
    </v-app-bar>
  </div>
</template>
<style scoped>
span:hover {
  cursor: pointer;
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
      items: [
        { text: 'เกี่ยวกับเรา', font: 'DB Helvethaica X' },
        { text: 'Why Quester?', font: 'DB Helvethaica X' },
        { text: 'วิธีใช้', font: 'DB Helvethaica X' },
        { text: 'ข่าวสาร', font: 'DB Helvethaica X' },
        { text: 'หน้านี้คืออะไร', font: 'DB Helvethaica X' },
        { text: 'ข้อคิดเห็น', font: 'DB Helvethaica X' },
        { text: 'ติดต่อเรา', font: 'DB Helvethaica X' }
      ]
    }
  }
}
</script>