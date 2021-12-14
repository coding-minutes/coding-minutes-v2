<template>
  <div class="section course-details row">
    <div class="details">
      <div class="row heading">
        <img
          :src="require(`@/assets/images/${category.icon}`)"
          v-if="category.icon"
          v-bind:alt="category.icon"
        />
        <h2>
          {{ category.category }}, <br />
          {{ course.title }}
        </h2>
      </div>
      <p class="description">
        {{ course.description }}
      </p>
      <div class="pricing row">
        <span class="current">₹ {{ courseMeta.currentprice }}</span>
        <span class="oldprice">₹ {{ courseMeta.oldprice }}</span>
        <span class="discountcoupon btn" v-if="courseMeta.discountcoupon">
          Use code: {{ courseMeta.discountcoupon }}
        </span>
      </div>
      <div class="udemy-ratings-box row">
        <a :href="courseMeta.udemy" target="_blank" rel="noopener noreferrer">
          <button class="btn btn-purple">
            Enroll now on Udemy
          </button>
        </a>
        <span class="star-rating"> {{ course.rating }} / 5.0 </span>
      </div>
    </div>
    <div class="youtube-video">
      <iframe
        :src="course.youtube"
        title="YouTube video player"
        frameborder="0"
        width="100%"
        height="100%"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
    </div>
  </div>
</template>
<script>
import CourseMeta from "@/data/courses_meta.json";

export default {
  props: ["course", "category"],
  data() {
    const courseMetadata = CourseMeta.find(
      item => item.slug === this.course.slug
    );
    return {
      courseMeta: courseMetadata
    };
  }
};
</script>
<style>
html,
button {
  font-family: "Nexa Bold", "Verdana", "Helvetica", "sans-serif";
}
.section {
  padding: 0.2rem 5vw;
}
.course-details {
  background: #f9f9f9;
  min-height: 40vh;
  padding-top: 4rem;
  padding-bottom: 4rem;
}
.course-details .youtube-video {
  width: 100%;
  min-height: 25vh;
}
.course-details .heading {
  height: 10vh;
  gap: 2rem;
  line-height: 2rem;
  justify-content: start;
}
.course-details .heading h2 {
  font-size: 30px;
}
.course-details .description {
  font-family: "Nexa Light";
  font-family: 1.3rem;
  color: rgba(21, 21, 24, 0.8);
  width: 75%;
  margin-top: 3rem;
}
.course-details .pricing {
  width: 60%;
  margin: 3.5rem 0;
}
.course-details .pricing .current {
  font-size: 25px;
}
.course-details .pricing .oldprice {
  font-size: 25px;
  color: #b9b9c0;
  text-decoration: line-through;
}
.course-details .pricing .discountcoupon {
  background: linear-gradient(90deg, #f77b26 0%, #f55a47 100%);
  border-radius: 3px;
  color: white;
  font-size: 1rem;
}
.course-details .udemy-ratings-box {
  width: 75%;
  color: #151518;
}
</style>
