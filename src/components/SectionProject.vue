<template>
  <section class="section-project">
    <v-container>
      <h1 class="heading-secondary text-center">Recent Projects</h1>
      <p class="text-center pt-5" style="font-size: 1.3rem">2 Websites developed and still growing...</p>
    </v-container>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.section-project {
  background-color: #7b1fa2;
  color: #fff;
  padding: 10rem 0;
  clip-path: polygon(0 0, 100% 12rem, 100% 100%, 0 75%);
}

@media screen and (max-width: 900px) {
  .section-project {
    padding: 2rem 50px;
    clip-path: none;
  }
}
</style>
