<template lang="">
  <div>
    <h1>Explore learning paths 🔥</h1>
    <span>
      Begin the journey for your dream job with these industry vetted learning
      paths.
    </span>
    <div class="explore-buttons">
      <button class="all-courses">All courses</button>
      <button v-for="category in Courses" :key="category.category">
        <img
          :src="require(`@/static/${category.icon}`)"
          v-if="category.icon"
          v-bind:alt="category.icon"
        />
        {{ category.category }}
      </button>
    </div>

    <section v-for="category in Courses" :key="category.category">
      <h3>{{ category.category }}</h3>
      <CourseCard v-for="course in category.courses" course="course" />
    </section>
  </div>
</template>

<script>
import Courses from "@/data/courses.json";

export default {
  methods: {
    getImgUrl(img) {
      return "require(`@/static/${img}`)";
    }
  },
  data() {
    return {
      Courses
    };
  }
};
</script>

<style lang=""></style>
