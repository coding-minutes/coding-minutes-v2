<template>
  <div class="section explore-learning-path">
    <h1>Explore learning paths 🔥</h1>
    <span class="tagline">
      Begin the journey for your dream job with these industry vetted learning
      paths.
    </span>
    <div class="explore-buttons">
      <button class="all-courses">All courses</button>
      <button v-for="category in Courses" :key="category.category">
        <img
          :src="require(`@/assets/images/${category.icon}`)"
          v-if="category.icon"
          v-bind:alt="category.icon"
        />
        {{ category.category }}
      </button>
    </div>

    <section
      v-for="category in Courses"
      :key="category.category"
      class="category"
    >
      <h3 class="category-title">{{ category.category }}</h3>
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
.explore-learning-path {
  background: #f9f9f9;
}
.explore-buttons {
  display: flex;
  width: 100%;
  justify-content: space-between;
}
.explore-buttons button {
  margin: 0.5rem 0;
  padding: 0.2rem 2.5rem;
  height: 3.5rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  white-space: nowrap;
  color: #151518;
  border: 1px solid #e2e2e2;
  background: none;
  border-radius: 1rem;
  font-size: 1rem;
  cursor: pointer;
}
.explore-buttons button:hover {
  background: white;
}
button.all-courses {
  color: #5848ea;
  background: white;
  border: none;
  outline: none;
}
.explore-buttons button img {
  height: 65%;
  margin-right: 2%;
}
.tagline {
  color: #151518cc;
  font-size: 1.3rem;
  font-family: "Nexa Light";
}
.explore-learning-path .category {
  margin-bottom: 3rem;
}
.explore-learning-path .category .category-title {
  font-size: 1.3rem;
}
.explore-learning-path .category .category-courses-list {
  display: flex;
  justify-content: start;
}
</style>
