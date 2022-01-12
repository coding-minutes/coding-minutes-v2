<template>
  <div class="section meet-the-team">
    <h1>Meet the team 😎</h1>
    <div class="row">
      <MentorCard v-for="mentor in team" :key="mentor.name" :mentor="mentor" />
    </div>
  </div>
</template>

<script>
import team from "@/data/team.json";
import MentorCard from "@/components/MentorCard";

export default {
  components: {
    MentorCard
  },
  data() {
    return {
      team
    };
  }
};
</script>
<style>
.meet-the-team {
  min-height: 75vh;
}
.meet-the-team h1 {
  text-align: center;
  margin-bottom: 2.5rem;
}
</style>
