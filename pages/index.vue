<template>
<div id="index">
  <v-carousel cycle interval="6000">
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
  <h1>服務項目</h1>
<v-card>
      <v-card-text>
        <v-row>
          <v-col cols="12" lg="7">
            <v-img :aspect-ratio="16/9" src="https://images.pexels.com/photos/1148820/pexels-photo-1148820.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260"></v-img>
          </v-col>
          <v-col cols="12" lg="5">
            <h1>爬蟲程式開發</h1>
            <v-divider class="my-5"></v-divider>
            依照需求針對指定網站開發爬蟲程式，可匯出成多種格式，或發送line、簡訊、電子郵件通知，依照網站難度報價，平均開發金額約3000。
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
    <v-card>
      <v-card-text>
        <v-row>
          <v-col cols="12" lg="5">
            <h1>專題、論文程式製作</h1>
            <v-divider class="my-5"></v-divider>
            依照需求開發指定程式，可協助撰寫文件、架設環境、簡單教育訓練，依需求難度報價平均金額約25,000，憑學生證可分期付款。
          </v-col>
          <v-col cols="12" lg="7">
            <v-img :aspect-ratio="16/9" src="https://images.pexels.com/photos/2004161/pexels-photo-2004161.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260"></v-img>
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
    <v-card>
      <v-card-text>
        <v-row>
          <v-col cols="12" lg="7">
            <v-img :aspect-ratio="16/9" src="https://images.pexels.com/photos/40185/mac-freelancer-macintosh-macbook-40185.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"></v-img>
          </v-col>
          <v-col cols="12" lg="5">
            <h1>提高網站SEO</h1>
            <v-divider class="my-5"></v-divider>
            調整網站架構、增加網站自然流量
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
    <v-card>
      <v-card-text>
        <v-row>
          <v-col cols="12" lg="5">
            <h1>客製化程式開發</h1>
            <v-divider class="my-5"></v-divider>
            開發客製化程式，可協助規劃程式功能，依照需求報價。
          </v-col>
          <v-col cols="12" lg="7">
            <v-img :aspect-ratio="16/9" src="https://images.pexels.com/photos/669615/pexels-photo-669615.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"></v-img>
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
    <v-card>
      <v-card-text>
        <v-row>
          <v-col cols="12" lg="7">
            <v-img :aspect-ratio="16/9" src="https://images.pexels.com/photos/38519/macbook-laptop-ipad-apple-38519.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"></v-img>
          </v-col>
          <v-col cols="12" lg="5">
            <h1>自動增加網站內容</h1>
            <v-divider class="my-5"></v-divider>自動增加網站指定關鍵字相關內容，省下高額寫手費用
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
    <v-card>
      <v-card-text>
        <v-row>
          <v-col cols="12" lg="5">
            <h1>增加網站流量</h1>
            <v-divider class="my-5"></v-divider>
            增加網站google台灣真人流量，可指定關鍵字、停留時間，可客製化行為
          </v-col>
          <v-col cols="12" lg="7">
            <v-img :aspect-ratio="16/9" src="https://images.pexels.com/photos/270637/pexels-photo-270637.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"></v-img>
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
    <v-card>
      <v-card-text>
        <v-row>
          <v-col cols="12" lg="7">
            <v-img :aspect-ratio="16/9" src="https://images.pexels.com/photos/330771/pexels-photo-330771.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"></v-img>
          </v-col>
          <v-col cols="12" lg="5">
            <h1>ERP系統開發</h1>
            <v-divider class="my-5"></v-divider>
            進銷存系統規劃、電子發票相關、企業SOP自動化
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
    <v-card>
      <v-card-text>
        <v-row>
          <v-col cols="12" lg="5">
            <h1>顧問服務</h1>
            <v-divider class="my-5"></v-divider>
            軟體架構諮詢、開發教學，導入測試、CICD、Azure，協助架設環境，讓您省下許多寶貴的時間
          </v-col>
          <v-col cols="12" lg="7">
            <v-img :aspect-ratio="16/9" src="https://images.pexels.com/photos/5380642/pexels-photo-5380642.jpeg?auto=compress&cs=tinysrgb&dpr=3&h=750&w=1260"></v-img>
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
</div>
  
</template>
<script>
export default {
  data: () => ({
    items: [
      {
        src: 'carousel-img/example-slide-1.jpg',
      },
      {
        src: 'carousel-img/example-slide-2.jpg',
      },
      {
        src: 'carousel-img/example-slide-3.jpg',
      },
      {
        src: 'carousel-img/example-slide-4.jpg',
      },
    ],
  }),
  methods: {
  },
}
</script>
<style>
.bg-pic{
  background-image: url('https://images.pexels.com/photos/220201/pexels-photo-220201.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260');
  background-repeat: no-repeat;
  background-position: center center;
  background-attachment: fixed;
  background-size: cover;
}
</style>
