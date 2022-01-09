<template>
  <div>
    <Navbar />
    <CourseDetails :course="course" :category="category" />
    <CourseOverview :course="course" />
    <RocketCircles>
      <h3>
        Ready to take your Coding Skills to Next Level
      </h3>
      <p>
        Join the Course Now!
      </p>
      <a :href="course.udemy" target="_blank" rel="noopener noreferrer">
        <button class="btn btn-purple">
          Enroll now on Udemy
        </button>
      </a>
    </RocketCircles>
    <FAQs />
    <Footer />
  </div>
</template>
<script>
import Navbar from "@/components/Navbar.vue";
import CourseDetails from "@/components/CourseDetails.vue";
import CourseOverview from "@/components/CourseOverview.vue";
import Courses from "@/data/courses.json";
import RocketCircles from "@/components/RocketCircles.vue";
import FAQs from "@/components/FAQs.vue";
import Footer from "@/components/Footer.vue";

export default {
  components: {
    Navbar,
    CourseDetails,
    CourseOverview,
    RocketCircles,
    FAQs,
    Footer
  },
  asyncData({ params, redirect }) {
    const slug = params.slug;
    const courses = Courses.reduce((acc, curr) => {
      return [...acc, ...curr.courses];
    }, []);

    const course = courses.find(
      course => course.slug.toLowerCase() == slug.toLowerCase()
    );

    const category = Courses.find(category =>
      category.courses.find(item => item.title == course.title)
    );

    return {
      slug,
      course,
      category: {
        icon: category.icon,
        category: category.category
      }
    };
  }
};
</script>
<style></style>
