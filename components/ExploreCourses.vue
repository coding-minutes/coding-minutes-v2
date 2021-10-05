<template>
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
      <div class="category-courses-list">
        <CourseCard
          v-for="course in category.courses"
          :key="course.title"
          :course="course"
        />
      </div>
    </section>
  </div>
</template>

<script>
import Courses from "@/data/courses.json";
import CourseCard from "@/components/CourseCard";

export default {
  components: {
    CourseCard
  },
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

<style>
.category-courses-list {
  display: flex;
  justify-content: flex-start;
  flex-direction: row;
  width: 100%;
}
</style>
