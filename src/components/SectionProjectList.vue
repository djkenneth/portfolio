<template>
  <v-row class="section-project-list">
    <v-col>
      <v-hover v-slot:default="{ hover }">
        <v-card class="mx-auto" max-width="500" dark color="grey darken-4" href="https://gamespot-app.netlify.app/" target="_blank">
          <v-card-title style="font-family: 'Skranji', cursive; font-size: 1.25rem;">~GameSpot~</v-card-title>
          <v-img class="white--text align-end" contain :src="require('../assets/project-section-1.jpg')"></v-img>
          <v-fade-transition>
            <div v-if="hover" class="d-flex flex-column grey darken-4 v-card-reveal" style="height: 100%">
              <div style="font-family: 'Skranji', cursive; font-size: 2rem;">~GameSpot~</div>
              <div style="width: 75%" class="text-center">
                GameSpot is a video gaming website using Vuejs and Vuetify
              </div>
            </div>
          </v-fade-transition>
        </v-card>
      </v-hover>
    </v-col>
    <v-col>
      <v-hover v-slot:default="{ hover }">
        <v-card class="mx-auto" max-width="500" dark color="bg-color" href="https://pclinkshop.netlify.app/" target="_blank">
          <v-card-title style="font-family: 'Skranji', cursive; font-size: 1.25rem;">PCLINK</v-card-title>
          <v-img class="white--text align-end" contain :src="require('../assets/project-section-2.jpg')"></v-img>
          <v-fade-transition>
            <div v-if="hover" class="d-flex flex-column bg-color v-card-reveal" style="height: 100%">
              <div style="font-family: 'Skranji', cursive; font-size: 2rem;">PCLINK</div>
              <div style="width: 75%" class="text-center">
                PC Link is a E-commerce website, a computer components store and my finals project in Human-Computer Interaction developed with Vuejs
                and Vuetify
              </div>
            </div>
          </v-fade-transition>
        </v-card>
      </v-hover>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    show: true,
  }),
};
</script>

<style scoped lang="scss">
.section-project-list {
  margin-top: -100px;

  .v-card-reveal {
    align-items: center;
    bottom: 0;
    justify-content: center;
    /* opacity: 0.5; */
    position: absolute;
    width: 100%;
  }

  .bg-color {
    background-color: #fca311;
  }
}

@media screen and (max-width: 900px) {
  .section-project-list {
    margin-top: 0;
  }
}
</style>
