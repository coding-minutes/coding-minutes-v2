<template>
  <div class="course-card">
    <div class="backdrop"></div>
    <div class="details">
      <span class="level">
        <template v-if="course.level == 1">
          BEGINNER 🔥
        </template>
        <template v-if="course.level == 2">
          INTERMEDIATE 🔥🔥
        </template>
        <template v-if="course.level == 3">
          ADVANCED 🔥🔥🔥
        </template>
      </span>
      <span class="title">{{ course.title }}</span>
      <span class="mentors">
        Mentors:
        <span v-for="mentor in course.mentors" :key="mentor">
          {{ mentor }}
        </span>
      </span>
      <span class="rating">
        {{ course.rating }}
      </span>
      <button class="explore-now">
        Explore now
      </button>
    </div>
  </div>
</template>
<script>
export default {
  props: ["course"]
};
</script>
<style>
.course-card {
  border: 1px solid black;
  margin: 10px;
  padding: 10px;
  width: 30vw;
}
.course-card .details > span {
  display: block;
}
</style>
