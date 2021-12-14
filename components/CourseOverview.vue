<template>
  <div class="section course-overview row">
    <div class="left-section">
      <div class="learnings sub-section">
        <h3>What you'll learn</h3>
        <ul>
          <li v-for="learning in course.learnings" :key="learning">
            {{ learning }}
          </li>
        </ul>
      </div>

      <!-- Course Overview -->
      <div class="overview sub-section">
        <div class="heading row">
          <h3>Course Overview</h3>
          <button class="btn btn-white">Learn more</button>
        </div>
        <p v-for="overview_para in course.overview" :key="overview_para">
          {{ overview_para }}
        </p>
        <ul>
          <li v-for="topic in course.topics" :key="topic">
            {{ topic }}
          </li>
        </ul>
      </div>

      <!-- What makes us special -->
      <div class="speciality">
        <h3>What makes us special?</h3>
        <div class="speciality-list">
          <div class="sub-section row card">
            <img :src="require('@/assets/images/speech-bubble.png')" />
            Unlimited doubt support
          </div>
          <div class="sub-section row card">
            <img :src="require('@/assets/images/dart.png')" />
            Industry vetted curriculum
          </div>
          <div class="sub-section row card">
            <img :src="require('@/assets/images/web-design.png')" />
            Practice codes, get feedback
          </div>
          <div class="sub-section row card">
            <img :src="require('@/assets/images/problem-solve.png')" />
            Intuitive & Details courses
          </div>
        </div>
      </div>
    </div>

    <div class="right-section meet-the-instructors">
      <!-- Meet the instructors -->
      <h3>Meet the instructors</h3>
      <MentorCard
        v-for="mentor in mentors"
        :key="mentor.name"
        :mentor="mentor"
      />
    </div>
  </div>
</template>
<script>
import Team from "@/data/team.json";
import MentorCard from "@/components/MentorCard";

export default {
  props: ["course"],
  components: {
    MentorCard
  },
  data() {
    const course = this.course;
    const mentors = course.mentors.map(mentor =>
      Team.find(member => member.username === mentor)
    );
    return { mentors };
  }
};
</script>
<style>
.course-overview {
  margin: 4rem 0;
}
.sub-section {
  background: #ffffff;
  border: 1px solid #d8d8d8;
  box-sizing: border-box;
  border-radius: 18px;
  padding-left: 2rem;
  padding-right: 2rem;
  margin-bottom: 2rem;
}

.sub-section h3 {
  font-size: 27px;
  line-height: 160%;
}
.sub-section .row {
  align-items: center;
}
.sub-section .btn {
  height: 100%;
}
.sub-section ul {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: repeat(6, 1fr);
  grid-auto-flow: column;
  color: #5b5b5d;
  font-family: "Nexa Light";
  font-size: 16px;
  line-height: 200%;
}

.course-overview .overview ul {
  grid-template-rows: repeat(5, 1fr);
}

.course-overview .overview p {
  font-family: "Nexa Light";
  font-size: 16px;
  line-height: 26px;
  color: #151518;
}

.course-overview .meet-the-instructors {
  width: 40vw;
  margin-left: 2vw;
}
.course-overview .speciality h3 {
  font-size: 1.7rem;
}
.course-overview .speciality .speciality-list {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}
.course-overview .speciality .speciality-list .card {
  width: 45%;
  align-items: center;
  height: 130px;
  justify-content: space-around;
  color: #5b5b5d;
  font-weight: bold;
  font-size: 1.3rem;
  gap: 20px;
}
.course-overview .speciality .speciality-list .card img {
  height: 50%;
}
</style>
