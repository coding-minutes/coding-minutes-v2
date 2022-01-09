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
<style>
.testimonial-card {
  border: 1px solid #d8d8d8;
  box-sizing: border-box;
  border-radius: 20px;
  margin: 12px;
  padding: 14px;
}
.testimonial-card .picture {
  border-radius: 50%;
  height: 75px;
}
.testimonial-card .quote {
  font-family: "Nexa Light";
  font-size: 15px;
  line-height: 160%;
  color: rgba(21, 21, 24, 0.7);
}
.testimonial-card .name {
  font-size: 18px;
  line-height: 160%;
}
.testimonial-card .institute {
  font-size: 14px;
  line-height: 160%;
  font-family: "Nexa Light";
  color: #5b5b5d;
}
</style>
