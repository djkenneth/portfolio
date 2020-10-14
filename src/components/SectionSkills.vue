<template>
  <section class="section-skills">
    <v-container>
      <transition appear enter-active-class="animate__animated animate__slideInUp">
        <h1 v-if="show" class="heading-secondary">My Stacks</h1>
      </transition>
      <transition appear enter-active-class="animate__animated animate__slideInUp">
        <p v-if="show" class="skill-paragraph">My Programming Languages and web technologies that I using.</p>
      </transition>
      <v-row>
        <v-col lg="2" md="3" sm="4" cols="6" v-for="stack in stacks" :key="stack.id">
          <transition-group appear enter-active-class="animate__animated animate__slideInUp">
            <v-card
              :key="stack.id"
              v-if="show"
              max-width="150"
              :style="{
                backgroundImage: `linear-gradient(${stack.position}, ${stack.colorBottom}, ${stack.colorTop})`,
              }"
            >
              <v-card-text class="pa-7">
                <v-img eager class="white--text ma-auto" :src="stack.img"></v-img>
              </v-card-text>
              <v-card-title>
                {{ stack.title }}
              </v-card-title>
            </v-card>
          </transition-group>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data: () => ({
    show: true,
    stacks: [
      {
        id: 1,
        img: require("../assets/vue.png"),
        title: "VueJS",
        position: "to top right",
        colorTop: "#62dba7",
        colorBottom: "#fff",
      },
      {
        id: 2,
        img: require("../assets/javascript.png"),
        title: "Javascript",
        position: "to top right",
        colorTop: "#ffef5e",
        colorBottom: "#fff",
      },
      {
        id: 3,
        img: require("../assets/vuetify.png"),
        title: "Vuetify",
        position: "to top right",
        colorTop: "#aeddff",
        colorBottom: "#fff",
      },
      {
        id: 4,
        img: require("../assets/html5.png"),
        title: "Html5",
        position: "to top right",
        colorTop: "#f19982",
        colorBottom: "#fff",
      },
      {
        id: 5,
        img: require("../assets/css3.png"),
        title: "Css3",
        position: "to top right",
        colorTop: "#cceff8",
        colorBottom: "#fff",
      },
      {
        id: 6,
        img: require("../assets/sass.png"),
        title: "Sass",
        position: "to top right",
        colorTop: "#d7b1bd",
        colorBottom: "#fff",
      },
      {
        id: 7,
        img: require("../assets/bootstrap.png"),
        title: "Bootstrap",
        position: "to top right",
        colorTop: "#c8abf2",
        colorBottom: "#fff",
      },
      {
        id: 8,
        img: require("../assets/laravel.png"),
        title: "Laravel",
        position: "to top right",
        colorTop: "#ff350094",
        colorBottom: "#fff",
      },
      {
        id: 9,
        img: require("../assets/php.png"),
        title: "Php",
        position: "to top right",
        colorTop: "#6181b6",
        colorBottom: "#fff",
      },
      {
        id: 10,
        img: require("../assets/vscode.png"),
        title: "VSCode",
        position: "to top right",
        colorTop: "#78bae2",
        colorBottom: "#fff",
      },
      {
        id: 11,
        img: require("../assets/figma.png"),
        title: "Figma",
        position: "to top right",
        colorTop: "#a259ff",
        colorBottom: "#fff",
      },
    ],
  }),
};
</script>

<style scoped lang="scss">
.section-skills {
  padding-top: 3rem;
  padding-bottom: 5rem;

  .heading-secondary {
    font-size: 3rem;
  }

  .skill-paragraph {
    font-size: 1.2rem;
    color: #413f3f;
  }
}

@media screen and (max-width: 900px) {
  .section-skills {
    padding: 0 50px;
  }
}
</style>
