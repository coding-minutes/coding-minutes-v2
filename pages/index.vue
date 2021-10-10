<template>
  <div>
    <div class="landing-page">
      <Navbar />
      <Hero />
      <ExploreCourses />
      <Reviews />
      <Benefits />
      <CampusCaptain />
      <MeetTheTeam />
      <FAQs />
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import ExploreCourses from "@/components/ExploreCourses.vue";
import Reviews from "@/components/Reviews.vue";
import Benefits from "@/components/Benefits.vue";
import CampusCaptain from "@/components/CampusCaptain.vue";
import MeetTheTeam from "@/components/MeetTheTeam.vue";
import FAQs from "@/components/FAQs.vue";

export default {
  components: {
    Navbar,
    Hero,
    ExploreCourses,
    Reviews,
    Benefits,
    CampusCaptain,
    MeetTheTeam,
    FAQs
  }
};
</script>

<style scoped></style>
