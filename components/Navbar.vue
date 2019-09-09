<template>
  <div>
    <v-app-bar fixed class="py-1 custom-nav" color="#FAFAFA" dark>
      <v-img max-height="50" contain :src="require('~/assets/logo/quester-logo-trans.svg')" />
      <v-toolbar-title>
        <!-- <span
          :style="{ 'font-family': 'SF Pro Display','font-weight': 750,'font-size':'30px','color':'#112D4E' }"
        >Quester</span>-->
      </v-toolbar-title>
      <div class="flex-grow-1"></div>
      <v-app-bar-nav-icon class="primary--text hidden-lg-and-up" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <scrollactive class="hidden-md-and-down" v-on:itemchanged="onItemChanged">
        <v-btn text v-for="(item,index) in items" :key="index" @click="$vuetify.goTo(item.id)">
          <span
            :style="{
              'font-family': item.font,
              'font-size': '28px',
              color: '#0F2F55',
              'font-weight': 650
            }"
          >{{ item.text }}</span>
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
      <v-app-bar-nav-icon class="hidden-lg-and-up" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <scrollactive class="hidden-md-and-down" v-on:itemchanged="onItemChanged">
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
          >{{ item.text }}</span>
        </v-btn>
      </scrollactive>
    </v-app-bar>
    <v-navigation-drawer class="blue-grad" fixed v-model="drawer" right temporary>
      <v-list nav dense>
        <scrollactive v-on:itemchanged="onItemChanged">
          <v-list-item
            @click="$vuetify.goTo(item.id); drawer=false"
            v-for="(item,index) in items"
            :key="index"
            link
          >
            <v-btn class="scrollactive-item" :href="item.id" text>
              <span
                :style="{ 'font-family': item.font ,'font-size':'28px' ,'color':'#FAFAFA','font-weight':650}"
              >{{item.text}}</span>
            </v-btn>
          </v-list-item>
        </scrollactive>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>
<style scoped>
.is-active {
  border-bottom: 5px solid white;
}
.custom-nav {
  /* background: transparent !important; */
  -moz-transition: opacity 0.25s ease-in-out;
  -webkit-transition: opacity 0.25s ease-in-out;
  -o-transition: opacity 0.25s ease-in-out;
  transition: opacity 0.25s ease-in-out;
  opacity: 1;
  /* background: #0d5ab2; */
  background: linear-gradient(to right, #0d5ab2, #0f2f55);
  box-shadow: 0px 0px 0px;
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
  background: linear-gradient(to right, #0d5ab2, #0f2f55);
  box-shadow: 0px 2px 4px -1px rgba(0, 0, 0, 0.2),
    0px 4px 5px 0px rgba(0, 0, 0, 0.14), 0px 1px 10px 0px rgba(0, 0, 0, 0.12);
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
      drawer: false,
      items: [
        { text: 'เกี่ยวกับเรา', font: 'DB Helvethaica X Bd', id: '#index' },
        { text: 'Why Quester?', font: 'DB Helvethaica X Bd', id: '#why' },
        { text: 'วิธีใช้', font: 'DB Helvethaica X Bd', id: '#how' },
        { text: 'ข่าวสาร', font: 'DB Helvethaica X Bd', id: '#news' },
        { text: 'หน้านี้คืออะไร', font: 'DB Helvethaica X Bd', id: '#what' },
        { text: 'ข้อคิดเห็น', font: 'DB Helvethaica X Bd', id: '#comment' },
        { text: 'ติดต่อเรา', font: 'DB Helvethaica X Bd', id: '#contact' }
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
