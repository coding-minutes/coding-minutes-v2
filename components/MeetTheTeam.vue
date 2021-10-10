<template>
  <div>
    <h1>Meet the team 😎</h1>
    <MentorCard v-for="mentor in team" :key="mentor.name" :mentor="mentor" />
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
<style></style>
