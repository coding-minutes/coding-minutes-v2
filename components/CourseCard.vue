<template>
  <div class="course-card">
    <div class="backdrop">
      <img
        class="course-card-backdrop"
        :src="require(`@/assets/images/courses_backdrops/${course.backdrop}`)"
      />
    </div>
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
      <div class="review-explore-box">
        <!-- TODO: Star rating here -->
        <span class="rating">
          {{ course.rating }}
        </span>
        <button class="explore-now">
          Explore now
        </button>
      </div>
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
  margin: 10px;
  width: 30vw;
  border-radius: 0.5rem;
  background: white;
}
.course-card .details > span {
  display: block;
}
.course-card .details .level {
  padding: 0.2rem 1rem;
  border: 1px solid #eaeaea;
  width: min-content;
  white-space: nowrap;
  border-radius: 1rem;
  margin-bottom: 1rem;
}
.course-card .details .title {
  color: #151518;
  font-weight: bold;
  font-size: 1.5rem;
}
.course-card .details .mentors {
  color: rgba(21, 21, 24, 0.6);
  font-size: 16px;
  line-height: 160%;
  margin-bottom: 1.5rem;
  font-family: "Nexa Light";
}
.course-card .details .rating {
  font-weight: bold;
  font-size: 1rem;
}
.course-card .review-explore-box {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.course-card-backdrop {
  width: 100%;
}
.course-card .details {
  padding: 2rem 1.8rem;
}
.course-card .explore-now {
  background: linear-gradient(90deg, #5848ea 0%, #9549eb 100%);
  border-radius: 1.4rem;
  height: 2.5rem;
  border: none;
  outline: none;
  color: white;
  padding: 0.5rem 1.2rem;
  cursor: pointer;
}
</style>
