<template>
  <div>
    <v-app-bar fixed class="py-1 pr-5 custom-nav2" color="#FAFAFA" dark>
      <v-img
        max-width="100"
        max-height="50"
        contain
        :src="require('~/assets/logo/quester-logo-trans.svg')"
      />
      <v-toolbar-title>
        <!-- <span
          :style="{ 'font-family': 'SF Pro Display','font-weight': 750,'font-size':'30px','color':'#112D4E' }"
        >Quester</span>-->
      </v-toolbar-title>
      <div class="flex-grow-1"></div>
      <scrollactive @itemchanged="onItemChanged">
        <v-btn
          v-for="(item, index) in items"
          :key="index"
          text
          @click="$vuetify.goTo(item.id)"
        >
          <span
            :style="{
              'font-family': item.font,
              'font-size': '28px',
              color: '#0F2F55',
              'font-weight': 650
            }"
            >{{ item.text }}</span
          >
        </v-btn>
      </scrollactive>
    </v-app-bar>
    <v-app-bar fixed class="py-1 pr-5 custom-nav" color="#FAFAFA" dark>
      <v-img
        max-width="100"
        max-height="50"
        contain
        :src="require('~/assets/logo/quester-logo-trans.svg')"
      />
      <v-toolbar-title>
        <!-- <span
          :style="{ 'font-family': 'SF Pro Display','font-weight': 750,'font-size':'30px','color':'#112D4E' }"
        >Quester</span>-->
      </v-toolbar-title>
      <div class="flex-grow-1"></div>
      <scrollactive @itemchanged="onItemChanged">
        <!-- <a href="#why" class="scrollactive-item">Home</a> -->
        <v-btn
          v-for="(item, index) in items"
          :key="index"
          class="scrollactive-item"
          :href="item.id"
          text
          @click="$vuetify.goTo(item.id)"
        >
          <span
            :style="{
              'font-family': item.font,
              'font-size': '28px',
              color: '#FAFAFA',
              'font-weight': 650
            }"
            >{{ item.text }}</span
          >
        </v-btn>
      </scrollactive>
    </v-app-bar>
  </div>
</template>
<style scoped>
.is-active {
  border-bottom: 5px solid white;
}
.custom-nav2.v-app-bar--is-scrolled {
  -moz-transition: opacity 0.25s ease-in-out;
  -webkit-transition: opacity 0.25s ease-in-out;
  -o-transition: opacity 0.25s ease-in-out;
  transition: opacity 0.25s ease-in-out;
  opacity: 0;
}
.custom-nav2 {
  -moz-transition: opacity 0.25s ease-in-out;
  -webkit-transition: opacity 0.25s ease-in-out;
  -o-transition: opacity 0.25s ease-in-out;
  transition: opacity 0.25s ease-in-out;
  opacity: 1;
}
.custom-nav {
  /* background: transparent !important; */
  -moz-transition: opacity 0.25s ease-in-out;
  -webkit-transition: opacity 0.25s ease-in-out;
  -o-transition: opacity 0.25s ease-in-out;
  transition: opacity 0.25s ease-in-out;
  opacity: 0;
}
.v-btn::before {
  background-color: transparent;
}
.v-btn:enabled {
  background-color: transparent;
}
.v-btn::after {
  background-color: transparent;
}
.custom-nav.v-app-bar--is-scrolled {
  -moz-transition: opacity 0.25s ease-in-out;
  -webkit-transition: opacity 0.25s ease-in-out;
  -o-transition: opacity 0.25s ease-in-out;
  transition: opacity 0.25s ease-in-out;
  opacity: 1;
  background: linear-gradient(to bottom right, #0d5ab2, #0f2f55);
}
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
        { text: 'เกี่ยวกับเรา', font: 'DB Helvethaica X', id: '#index' },
        { text: 'Why Quester?', font: 'DB Helvethaica X', id: '#why' },
        { text: 'วิธีใช้', font: 'DB Helvethaica X', id: '#how' },
        { text: 'ข่าวสาร', font: 'DB Helvethaica X', id: '#news' },
        { text: 'หน้านี้คืออะไร', font: 'DB Helvethaica X', id: '#what' },
        { text: 'ข้อคิดเห็น', font: 'DB Helvethaica X', id: '#comment' },
        { text: 'ติดต่อเรา', font: 'DB Helvethaica X', id: '#contact' }
      ]
    };
  },
  methods: {
    onItemChanged(event, currentItem, lastActiveItem) {
      // console.log(currentItem)
    }
  }
};
</script>
