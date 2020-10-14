<template>
  <section class="section-intro">
    <v-container ref="sectionintro">
      <transition appear enter-active-class="animate__animated animate__slideInDown">
        <h1 v-show="show" class="heading-secondary">About Me</h1>
      </transition>
      <transition appear enter-active-class="animate__animated animate__slideInRight">
        <p v-show="show" class="paragraph-primary">
          Hi I'm Kenneth Ivan P. Pineda, {{ new Date().getFullYear() - 1998 }} years old and currently living in Angeles City Pampanga, Philippines. I
          graduated Bachelor of Science in Information Technology at System Plus College Foundation. I love designs and creating something
          interesting. I'm very passionate about this field and I always strive forward to enhance my knowledge about Web development to be able to
          excel in this field.
        </p>
      </transition>
    </v-container>
  </section>
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

      observer.observe(this.$refs.sectionintro);
    },
  },

  mounted() {
    this.scrollTrigger();
  },
};
</script>

<style scoped lang="scss">
.section-intro {
  background-color: #201e1f;
  color: #fff;
  padding: 10rem 0;
  clip-path: polygon(0 0, 100% 12rem, 100% 100%, 0 75%);

  .heading-secondary {
    font-size: 3rem;
  }

  .paragraph-primary {
    font-size: 1.2rem;
    line-height: 1.4;
    font-weight: 300;
    width: 70%;
  }
}

@media screen and (max-width: 900px) {
  .section-intro {
    padding: 2rem 50px;
    clip-path: none;

    .paragraph-primary {
      width: 80%;
    }
  }
}

@media screen and (max-width: 500px) {
  .paragraph-primary {
    width: 100%;
  }
}
</style>
