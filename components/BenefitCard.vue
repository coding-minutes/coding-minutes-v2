<template>
  <div class="benefit-card">
    <img :src="require(`@/assets/images/${benefit.icon}`)" height="80" />
    <h5>
      {{ benefit.title }}
    </h5>
  </div>
</template>
<script>
export default {
  props: ["benefit"]
};
</script>
<style>
.benefit-card {
  background: white;
  border: none;
  border-radius: 20px;
  height: 10rem;
  width: 10rem;
  padding: 2rem;
}
.benefit-card h5 {
  font-size: 18px;
  color: #5b5b5d;
}
.benefit-card img {
  height: 3.6rem;
}
</style>
