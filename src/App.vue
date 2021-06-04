<template>
  <v-app>
    <header class="img-header">
      <v-container style="height: 100%;">
        <div class="img-logo">
          <v-img eager :src="require('./assets/logo-eye.png')" max-width="150"></v-img>
        </div>
        <div class="section-title pt-16">
          <div class="scrolls">
            <h4 class="header-title-name">Hello, I'm Kenneth,</h4>
            <h1 class="header-title">A Front-End Web Developer</h1>
          </div>
        </div>
      </v-container>
    </header>
    <v-main>
      <section class="section-intro">
        <v-container>
          <div class="scrolls">
            <h1 class="heading-secondary">About Me</h1>
            <p class="paragraph-primary">
              Hi I'm Kenneth Ivan P. Pineda, {{ new Date().getFullYear() - 1998 }} years old and currently living in Angeles City Pampanga,
              Philippines. I graduated Bachelor of Science in Information Technology at System Plus College Foundation. I love designs and creating
              something interesting. I'm very passionate about this field and I always strive forward to enhance my knowledge about Web development to
              be able to excel in this field.
            </p>
          </div>
        </v-container>
      </section>
      <section class="section-skills">
        <v-container>
          <div class="scrolls">
            <h1 class="heading-secondary">My Stacks</h1>
            <p class="skill-paragraph">My Programming Languages and web technologies that I using.</p>
          </div>
          <!-- GRID CARD -->
          <v-row>
            <v-col lg="2" md="3" sm="4" xs="6" cols="auto" v-for="stack in stacks" :key="stack.id" class="sm-m-auto">
              <div class="scrolls-1">
                <v-card
                  max-width="170"
                  class="ma-auto"
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
              </div>
            </v-col>
          </v-row>
        </v-container>
      </section>
      <section class="section-project">
        <v-container>
          <h1 class="heading-secondary text-center">Recent Projects</h1>
          <p class="text-center pt-5" style="font-size: 1.3rem">2 Websites developed and still growing...</p>
        </v-container>
      </section>
      <v-row class="section-project-list">
        <v-col>
          <v-hover v-slot:default="{ hover }">
            <v-card class="mx-auto" max-width="500" dark color="grey darken-4" href="https://gamespot-app.netlify.app/" target="_blank">
              <v-card-title style="font-family: 'Skranji', cursive; font-size: 1.25rem;">~GameSpot~</v-card-title>
              <v-img eager class="white--text align-end" contain :src="require('@/assets/project-section-1.jpg')"></v-img>
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
              <v-img eager class="white--text align-end" contain :src="require('@/assets/project-section-2.jpg')"></v-img>
              <v-fade-transition>
                <div v-if="hover" class="d-flex flex-column bg-color v-card-reveal" style="height: 100%">
                  <div style="font-family: 'Skranji', cursive; font-size: 2rem;">PCLINK</div>
                  <div style="width: 75%" class="text-center">
                    PC Link is a E-commerce website, a computer components store and my finals project in Human-Computer Interaction developed with
                    Vuejs and Vuetify
                  </div>
                </div>
              </v-fade-transition>
            </v-card>
          </v-hover>
        </v-col>
        <v-col>
          <v-hover v-slot:default="{ hover }">
            <v-card class="mx-auto" max-width="500" dark color="grey darken-4" href="https://ryxmovie.herokuapp.com/" target="_blank">
              <v-card-title style="font-family: 'Skranji', cursive; font-size: 1.25rem;">RYX MOVIE APP</v-card-title>
              <v-img eager class="white--text align-end" contain :src="require('@/assets/project-section-3.jpg')"></v-img>
              <v-fade-transition>
                <div v-if="hover" class="d-flex flex-column grey darken-4 v-card-reveal" style="height: 100%">
                  <div style="font-family: 'Skranji', cursive; font-size: 2rem;">RYX MOVIE APP</div>
                  <div style="width: 75%" class="text-center">
                    RXYMOVIE is a movie information website using Vue.js, Vuetify, and TMDB API
                  </div>
                </div>
              </v-fade-transition>
            </v-card>
          </v-hover>
        </v-col>
      </v-row>
      <v-footer dark padless style="margin-top: 100px">
        <v-card width="100%" flat tile color="#201e1f" class="white--text text-center py-10">
          <v-row style="height: 150px;" align-content="center" justify="center">
            <v-img :src="require('@/assets/logo-eye.png')" max-width="150"></v-img>
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
            <h4 class="body-1">All right reserved {{ new Date().getFullYear() }}</h4>
          </v-card-text>
        </v-card>
      </v-footer>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    show: true,
    stacks: [
      {
        id: 1,
        img: require("@/assets/vue.png"),
        title: "VueJS",
        position: "to top right",
        colorTop: "#62dba7",
        colorBottom: "#fff",
      },
      {
        id: 2,
        img: require("@/assets/javascript.png"),
        title: "Javascript",
        position: "to top right",
        colorTop: "#ffef5e",
        colorBottom: "#fff",
      },
      {
        id: 3,
        img: require("@/assets/vuetify.png"),
        title: "Vuetify",
        position: "to top right",
        colorTop: "#aeddff",
        colorBottom: "#fff",
      },
      {
        id: 4,
        img: require("@/assets/html5.png"),
        title: "Html5",
        position: "to top right",
        colorTop: "#f19982",
        colorBottom: "#fff",
      },
      {
        id: 5,
        img: require("@/assets/css3.png"),
        title: "Css3",
        position: "to top right",
        colorTop: "#cceff8",
        colorBottom: "#fff",
      },
      {
        id: 6,
        img: require("@/assets/sass.png"),
        title: "Sass",
        position: "to top right",
        colorTop: "#d7b1bd",
        colorBottom: "#fff",
      },
      {
        id: 7,
        img: require("@/assets/bootstrap.png"),
        title: "Bootstrap",
        position: "to top right",
        colorTop: "#c8abf2",
        colorBottom: "#fff",
      },
      {
        id: 8,
        img: require("@/assets/laravel.png"),
        title: "Laravel",
        position: "to top right",
        colorTop: "#ff350094",
        colorBottom: "#fff",
      },
      {
        id: 9,
        img: require("@/assets/php.png"),
        title: "Php",
        position: "to top right",
        colorTop: "#6181b6",
        colorBottom: "#fff",
      },
      {
        id: 10,
        img: require("@/assets/vscode.png"),
        title: "VSCode",
        position: "to top right",
        colorTop: "#78bae2",
        colorBottom: "#fff",
      },
      {
        id: 11,
        img: require("@/assets/figma.png"),
        title: "Figma",
        position: "to top right",
        colorTop: "#a259ff",
        colorBottom: "#fff",
      },
    ],
  }),

  methods: {
    scrollTrigger() {
      const scrolls = document.querySelectorAll(".scrolls");

      const observer = new IntersectionObserver((entries) => {
        // console.log(entries);
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            entry.target.className = "animate__animated animate__slideInLeft";
          } else {
            entry.target.className = "";
          }
        });
      });

      scrolls.forEach((scroll) => {
        observer.observe(scroll);
      });
    },

    scrollTrigger1() {
      const scrolls = document.querySelectorAll(".scrolls-1");

      const observer = new IntersectionObserver((entries) => {
        // console.log(entries);
        entries.forEach((entry) => {
          if (entry.intersectionRatio > 0) {
            entry.target.className = "animate__animated animate__fadeInUp animate__delay-0.5s";
          }
        });
      });

      scrolls.forEach((scroll) => {
        observer.observe(scroll);
      });
    },
  },

  mounted() {
    this.scrollTrigger();
    this.scrollTrigger1();
  },
};
</script>

<style scoped>
:root {
  --animate-delay: 0.5s;
}
</style>
