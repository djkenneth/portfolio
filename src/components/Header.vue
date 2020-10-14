<template>
  <header class="img-header">
    <v-container style="height: 100%;">
      <div class="img-logo">
        <v-img eager :src="require('../assets/logo-eye.png')" max-width="150"></v-img>
      </div>
      <div ref="headertitle" class="section-title d-flex align-center">
        <transition enter-active-class="animate__animated animate__slideInLeft" leave-active-class="animate__animated animate__slideOutLeft">
          <div v-show="show">
            <h4 class="header-title-name">Hello, I'm Kenneth,</h4>
            <h1 class="header-title">A Front-End Web Developer</h1>
          </div>
        </transition>
      </div>
    </v-container>
  </header>
</template>

<script>
export default {
  data: () => ({
    show: false,
  }),

  methods: {
    scrollTrigger() {
      const observer = new IntersectionObserver((entries) => {
        // console.log(entries);
        if (entries[0].intersectionRatio > 0) {
          this.show = true;
        } else {
          this.show = false;
        }
      });

      observer.observe(this.$refs.headertitle);
    },
  },

  mounted() {
    this.scrollTrigger();
  },
};
</script>

<style lang="scss" scoped>
.img-header {
  height: 90vh;

  .section-title {
    width: 60%;
    height: 85%;

    .header-title-name {
      font-size: 2.5rem;
      font-weight: 400;
    }

    .header-title {
      font-size: 5rem;
    }
  }
}

@media screen and (max-width: 900px) {
  header.img-header {
    background-image: linear-gradient(rgba(255, 255, 255, 0.4), rgba(255, 255, 255, 0.4)), url("../assets/imageBackground.jpg");
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    height: 100vh;

    .section-title {
      width: 100vw;
    }

    .img-logo,
    .header-title,
    .header-title-name {
      margin: 0 50px;
    }

    .header-title {
      font-size: 4.5rem;
    }
  }
}

@media screen and (max-width: 600px) {
  header.img-header {
    .section-title {
      .header-title {
        font-size: 4rem;
      }
    }
  }
}

@media screen and (max-width: 500px) {
  header.img-header {
    .img-logo {
      width: 130px;
    }

    .section-title {
      .header-title-name {
        font-size: 1.5rem;
      }

      .header-title {
        font-size: 3.5rem;
      }
    }
  }
}
</style>
