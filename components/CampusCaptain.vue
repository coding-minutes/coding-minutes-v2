<template>
  <RocketCircles>
    <h3>
      Campus Captain 🏁
      <span class="badge">
        NEW
      </span>
    </h3>
    <p>
      Become a Campus Captain for your campus, win swags, Coding T-Shirts & cash
      incentives!
    </p>
    <a
      href="https://codingminutes.com/"
      target="_blank"
      rel="noopener noreferrer"
    >
      <button class="btn btn-purple">
        Join as Campus Captain
      </button>
    </a>
  </RocketCircles>
</template>

<script>
import RocketCircles from "@/components/RocketCircles.vue";

export default {
  components: {
    RocketCircles
  }
};
</script>
<style>
.badge {
  background: linear-gradient(90deg, #e73c3c 0%, #ff5b37 100%);
  border-radius: 10px;
  color: white;
  padding: 0.5rem 0.5rem;
  font-size: 22px;
}
</style>
