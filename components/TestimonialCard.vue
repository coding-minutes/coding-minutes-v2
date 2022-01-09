<template>
  <div class="testimonial-card">
    <img class="picture " :src="require(`@/assets/images/${picture}.jpg`)" />
    <p class="quote">
      {{ quote }}
    </p>
    <b class="name">{{ name }}</b>
    <div class="institute">{{ institute }}</div>
  </div>
</template>
<script>
export default {
  props: ["picture", "quote", "name", "institute"]
};
</script>
<style></style>
