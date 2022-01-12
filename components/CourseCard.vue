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
        {{ instructors.join(", ") }}
      </span>
      <div class="review-explore-box">
        <!-- TODO: Star rating here -->
        <span class="rating">
          {{ course.rating }}
        </span>
        <NuxtLink :to="'/' + course.slug">
          <button class="explore-now">
            Explore now
          </button>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>
<script>
import Team from "@/data/team.json";

export default {
  props: ["course"],
  data() {
    const mentors = this.course.mentors;
    const instructors = mentors.map(mentor => {
      return Team.find(member => member.username === mentor).name;
    });
    return {
      instructors
    };
  }
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
