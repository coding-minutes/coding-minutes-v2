<template>
  <div class="perk-card">
    <img :src="require(`@/assets/images/${image}`)" />
    <h3>{{ heading }}</h3>
    <p>
      {{ content }}
    </p>
  </div>
</template>
<script>
export default {
  props: ["heading", "image", "content"]
};
</script>
<style>
.perk-card {
  border: 1px solid #d8d8d8;
  border-radius: 20px;
}
.perk-card {
  margin: 0.8rem;
  padding: 1.5rem 2rem;
}
.perk-card img {
  height: 60px;
}
.perk-card h3 {
  font-size: 22px;
  line-height: 160%;
  color: #5b5b5d;
}
.perk-card p {
  font-family: "Nexa Light";
  font-size: 16px;
  line-height: 160%;
  color: rgba(21, 21, 24, 0.8);
}
</style>
