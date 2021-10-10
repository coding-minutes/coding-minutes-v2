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
  border: 1px solid black;
  height: 10rem;
  width: 10rem;
  padding: 2rem;
}
</style>
