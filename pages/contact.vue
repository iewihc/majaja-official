<template>
  <div id="contact">
    <v-row>
      <v-col cols='12' lg='6' class='d-block overflow-hidden pa-0 pb-16'>
        <div class='googlemap-rwd'>
          <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2575.99888048127!2d120.54456217371308!3d24.06586246907794!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x34693889ccfecec9%3A0xb5bda217882b977e!2zNTAw5b2w5YyW57ij5b2w5YyW5biC5aSn5Z-U6LevNTc15be3MuiZnw!5e0!3m2!1szh-TW!2stw!4v1636511454673!5m2!1szh-TW!2stw" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
        </div>
      </v-col>
      <v-col cols='12' lg='6'>
        <v-card >
          <v-card-text>
            <div class="text-h4 text--primary">聯絡我們</div>
            <div class="text-h6 text--primary ml-3 my-5">
              信箱：majajastudio@gmail.com
            </div>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
    <form>
      <v-text-field id="email" v-model="email" label="留下您的信箱" autocomplete="true" required></v-text-field>
      <v-textarea outlined label="留言給我們" v-model="message"></v-textarea>
      <v-btn class="mr-4" color="success" @click="send">送出</v-btn>
      <v-btn color="warning" @click="clear">清除</v-btn>
    </form>
  </div>
</template>

<script>
export default {
  data: () => ({
    email: '',
    message: '',
  }),
  methods: {
    send() {
      this.$mail.send({
        from: this.email,
        subject: 'Contact form message',
        text: this.message,
      })
    },
    clear () {
      this.email = ''
      this.message = ''
    }
  }
}
</script>
<style>
.googlemap-rwd {
  position:relative;
  height:0;
  padding-bottom:75%;
  overflow:hidden
}
.googlemap-rwd iframe,
.googlemap-rwd object,
.googlemap-rwd embed {
  position:absolute;
  top:0;
  left:0;
  width:100%;
  height:100%
}
</style>
