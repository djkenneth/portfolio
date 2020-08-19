<template>
  <v-app>
    <header class="img-header">
      <v-container>
        <div class="img-logo">
          <v-img :src="require('./assets/logo-eye.png')" max-width="150"></v-img>
        </div>
        <section class="section-title d-flex justify-space-between" style="margin-top: 100px">
          <div class="section-title-left">
            <transition appear enter-active-class="animate__animated animate__slideInLeft">
              <div v-if="show">
                <h4 class="header-title-name">Hello, I'm Kenneth,</h4>
                <h1 class="header-title">A Front-End Web Developer</h1>
              </div>
            </transition>
          </div>
          <div class="section-title-right" style="width: 50%"></div>
        </section>
      </v-container>
    </header>
    <v-main>
      <section class="section-intro">
        <v-container>
          <transition appear enter-active-class="animate__animated animate__slideInDown">
            <h1 v-if="show" class="heading-secondary">About Me</h1>
          </transition>
          <transition appear enter-active-class="animate__animated animate__slideInRight">
            <p v-if="show" class="paragraph-primary">
              Hi I'm Kenneth Ivan P. Pineda, {{ new Date().getFullYear() - 1998 }} years old and currently living in
              Angeles City Pampanga, Philippines. I graduated Bachelor of Science in Information Technology at System
              Plus College Foundation. I love designs and creating something interesting. I'm very passionate about this
              field and I always strive forward to enhance my knowledge about Web development to be able to excel in
              this field.
            </p>
          </transition>
        </v-container>
      </section>
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
                    <v-img class="white--text ma-auto" width="80" :src="stack.img"></v-img>
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
      <section class="section-project">
        <v-container>
          <h1 class="heading-secondary text-center">Recent Projects</h1>
          <p class="text-center pt-5" style="font-size: 1.3rem">5 Websites developed and still growing...</p>
        </v-container>
      </section>
      <v-row class="section-project-list">
        <v-col>
          <v-hover v-slot:default="{ hover }">
            <v-card
              class="mx-auto"
              max-width="500"
              dark
              color="grey darken-4"
              href="https://gamispot-app.netlify.app/"
              target="_blank"
            >
              <v-card-title style="font-family: 'Skranji', cursive; font-size: 1.25rem;">~GameSpot~</v-card-title>
              <v-img class="white--text align-end" contain :src="require('./assets/project-section-1.png')"></v-img>
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
      </v-row>
      <v-footer dark padless style="margin-top: 100px">
        <v-card width="100%" flat tile color="#201e1f" class="white--text text-center py-10">
          <v-row style="height: 150px;" align-content="center" justify="center">
            <v-img :src="require('./assets/logo-eye.png')" max-width="150"></v-img>
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
            <!-- <v-btn class="mx-4 white--text" icon>
              <v-icon size="3rem">mdi-linkedin</v-icon>
            </v-btn> -->
            <v-btn class="mx-4 white--text" icon href="https://www.instagram.com/pinedakenneth98/" target="_blank">
              <v-icon size="3rem">mdi-instagram</v-icon>
            </v-btn>
          </v-card-text>
          <v-card-text class="white--text pt-12" style="font-size: 1rem; font-weight: 400;">
            Designed and developed with ❤️ by Kenneth Ivan Pineda
            <h4 class="body-1">All right reserved 2020</h4>
          </v-card-text>
        </v-card>
      </v-footer>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {
    //
  },

  data: () => ({
    show: true,
    stacks: [
      {
        id: 1,
        img: require("./assets/vue.png"),
        title: "VueJS",
        position: "to top right",
        colorTop: "#62dba7",
        colorBottom: "#fff",
      },
      {
        id: 2,
        img: require("./assets/javascript.png"),
        title: "Javascript",
        position: "to top right",
        colorTop: "#ffef5e",
        colorBottom: "#fff",
      },
      {
        id: 3,
        img: require("./assets/vuetify.png"),
        title: "Vuetify",
        position: "to top right",
        colorTop: "#aeddff",
        colorBottom: "#fff",
      },
      {
        id: 4,
        img: require("./assets/html5.png"),
        title: "Html5",
        position: "to top right",
        colorTop: "#f19982",
        colorBottom: "#fff",
      },
      {
        id: 5,
        img: require("./assets/css3.png"),
        title: "Css3",
        position: "to top right",
        colorTop: "#cceff8",
        colorBottom: "#fff",
      },
      {
        id: 6,
        img: require("./assets/bootstrap.png"),
        title: "Bootstrap",
        position: "to top right",
        colorTop: "#c8abf2",
        colorBottom: "#fff",
      },
      {
        id: 7,
        img: require("./assets/laravel.png"),
        title: "Laravel",
        position: "to top right",
        colorTop: "#ff350094",
        colorBottom: "#fff",
      },
      {
        id: 8,
        img: require("./assets/php.png"),
        title: "Php",
        position: "to top right",
        colorTop: "#6181b6",
        colorBottom: "#fff",
      },
      {
        id: 9,
        img: require("./assets/vscode.png"),
        title: "VSCode",
        position: "to top right",
        colorTop: "#78bae2",
        colorBottom: "#fff",
      },
      {
        id: 10,
        img: require("./assets/figma.png"),
        title: "Figma",
        position: "to top right",
        colorTop: "#a259ff",
        colorBottom: "#fff",
      },
    ],
  }),
};
</script>

<style>
.header-title-name {
  font-size: 2.5rem;
  font-weight: 400;
}

.header-title {
  font-size: 4.5rem;
}

.section-title {
  padding-bottom: 40px;
}

.section-intro {
  background-color: #201e1f;
  color: #fff;
  padding: 10rem 0;
  clip-path: polygon(0 0, 100% 12rem, 100% 100%, 0 75%);
}

.heading-secondary {
  font-size: 3rem;
}

.paragraph-primary {
  font-size: 1.2rem;
  line-height: 1.4;
  font-weight: 300;
  width: 70%;
}

.section-skills {
  padding-top: 3rem;
  padding-bottom: 5rem;
}

.skill-paragraph {
  font-size: 1.2rem;
  color: #413f3f;
}

.section-project {
  background-color: #7b1fa2;
  color: #fff;
  padding: 10rem 0;
  clip-path: polygon(0 0, 100% 12rem, 100% 100%, 0 75%);
}

.section-project-list {
  margin-top: -100px;
}

.footer-qoutes {
  width: 40%;
  margin: 0 auto;
  font-size: 1rem;
  font-weight: 400;
}

.v-card-reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  /* opacity: 0.5; */
  position: absolute;
  width: 100%;
}

@media screen and (max-width: 900px) {
  .img-logo,
  .header-title,
  .header-title-name {
    padding: 0 50px;
  }

  header.img-header {
    background-image: linear-gradient(rgba(255, 255, 255, 0.4), rgba(255, 255, 255, 0.4)),
      url("./assets/imageBackground.jpg");
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    height: 500px;
  }

  .header-title {
    font-size: 4.5rem;
  }

  .section-intro,
  .section-project {
    padding: 2rem 50px;
    clip-path: none;
  }

  .paragraph-primary {
    width: 80%;
  }

  .section-skills {
    padding: 0 50px;
  }

  .section-project-list {
    margin-top: 0;
  }
}

@media screen and (max-width: 600px) {
  .header-title {
    font-size: 3.8rem;
  }
}

@media screen and (max-width: 500px) {
  .img-logo {
    max-width: 200px;
  }

  .header-title-name {
    font-size: 1.5rem;
  }

  .header-title {
    font-size: 2.5rem;
  }

  .paragraph-primary {
    width: 100%;
  }
}
</style>
