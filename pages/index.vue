<template>
  <div>
    <Navbar />
    <div class="landing-page">
      <Hero />
      <ExploreCourses />
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import ExploreCourses from "@/components/ExploreCourses.vue";

export default {
  components: {
    Navbar,
    Hero,
    ExploreCourses
  }
};
</script>

<style scoped>
.landing-page {
  margin-top: 10vh;
}
</style>
