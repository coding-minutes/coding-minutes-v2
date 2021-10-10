<template>
  <div>
    <div
      :style="{
        backgroundImage: `url('@/assets/images/team_backdrops/${mentor.backdrop}')`
      }"
    >
      <strong>{{ mentor.name }}</strong>
      <span>{{ mentor.company }}</span>
    </div>
    <div>
      <p>
        {{ mentor.description }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["mentor"]
};
</script>
<style></style>
