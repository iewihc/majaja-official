<template>
  <div id="product">
    <v-expansion-panels v-model="panel" :disabled="disabled" multiple>
      <Fragment v-bind:key="i.title" v-for="i in items">
        <v-expansion-panel>
          <v-expansion-panel-header>{{ i.title }}</v-expansion-panel-header>
          <v-expansion-panel-content class="pa-5">
            <Fragment v-bind:key="pic" v-for="pic in i.src">
              <v-img max-width="1000" max-height="qq" :src="pic"></v-img>
            </Fragment>
            <iframe
              v-if="i.videos"
              width="95%"
              :src="i.videos"
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </Fragment>
    </v-expansion-panels>
  </div>
</template>

<script>
import { Fragment } from 'vue-fragment'

export default {
  components: { Fragment },
  data: () => ({
    panel: [0, 1, 2, 3],
    disabled: false,
    readonly: false,
    items: [
      {
        title: '某公司委託公司網站開發',
        src: ['project-img/w1.png'],
      },
      {
        title: '外包統計程式開發',
        src: ['project-img/w2.png'],
      },
      {
        title: '碩士論文程式-數據調整介面開發',
        src: ['project-img/w3.png'],
        videos: 'https://www.youtube.com/embed/kbSUkmYqmuA',
      },
      {
        title: '畢業專題-學生學習資料統計-預測學習結果網站',
        src: ['project-img/w4.png'],
      },
      {
        title: '學生論文網站-仿製訂房網站開發',
        src: ['project-img/w5.png'],
      },
      {
        title: '外包部屬程式開發',
        src: ['project-img/w6.png', 'project-img/w61.png'],
      },
      {
        title: '外包監控指定區域開罰單程式開發',
        src: [
          'project-img/w7.png',
          'project-img/w71.png',
          'project-img/w72.png',
        ],
      },
      {
        title: '外包多益測試系統',
        src: [
          'project-img/w8.png',
          'project-img/w81.png',
          'project-img/w82.png',
        ],
      },
      {
        title: '外包模擬人為搜尋指定關鍵字網頁程式',
        src: [],
        videos: 'https://www.youtube.com/embed/QFhlASUjwRQ',
      },
      {
        title: '外包POST圖片程式Client端、接收圖片WebAPI程式',
        src: [],
        videos: 'https://www.youtube.com/embed/bhs9IKbd2EE',
      },
      {
        title: '外包快捷鍵程式開發',
        src: [],
        videos: 'https://www.youtube.com/embed/zCFr_1f1WRk',
      },
      {
        title: '某補習班委託電子白板程式開發',
        src: [],
        videos: 'https://www.youtube.com/embed/Iuzo6r1exwE',
      },
      {
        title: '監控指定區域程式開發',
        src: [],
        videos: 'https://www.youtube.com/embed/8GI2g8Pc_1g',
      },
      {
        title: '某公司外包ERP系統',
        src: [
          'project-img/w9.png',
          'project-img/w91.png',
          'project-img/w94.png',
        ],
      },
    ],
  }),
}
</script>

<style scoped>
</style>
