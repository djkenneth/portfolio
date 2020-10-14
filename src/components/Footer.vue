<template>
  <v-footer dark padless style="margin-top: 100px">
    <v-card width="100%" flat tile color="#201e1f" class="white--text text-center py-10">
      <v-row style="height: 150px;" align-content="center" justify="center">
        <v-img :src="require('../assets/logo-eye.png')" max-width="150"></v-img>
      </v-row>
      <h3 class="white--text footer-qoutes">
        Never stop learning, We don't come here just to lose! Keep fighting for your dreams.
      </h3>
      <v-card-text>
        <v-btn class="mx-4 white--text" icon href="https://www.facebook.com/Kenneth.Pineda.1998" target="_blank">
          <v-icon size="3rem">mdi-facebook</v-icon>
        </v-btn>
        <v-btn class="mx-4 white--text" icon href="https://twitter.com/PinedaKenneth98" target="_blank">
          <v-icon size="3rem">mdi-twitter</v-icon>
        </v-btn>
        <v-btn class="mx-4 white--text" icon href="https://www.instagram.com/pinedakenneth98/" target="_blank">
          <v-icon size="3rem">mdi-instagram</v-icon>
        </v-btn>
        <v-btn class="mx-4 white--text" icon href="https://github.com/djkenneth" target="_blank">
          <v-icon size="3rem">mdi-github</v-icon>
        </v-btn>
      </v-card-text>
      <v-card-text class="white--text pt-12" style="font-size: 1rem; font-weight: 400;">
        Designed and developed with ❤️ by Kenneth Ivan Pineda
        <h4 class="body-1">All right reserved 2020</h4>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {};
</script>

<style scoped>
.footer-qoutes {
  width: 40%;
  margin: 0 auto;
  font-size: 1rem;
  font-weight: 400;
}
</style>
