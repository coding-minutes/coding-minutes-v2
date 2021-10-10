<template>
  <div>
    <strong>{{ faq.question }}</strong>
    <p>{{ faq.answer }}</p>
  </div>
</template>
<script>
export default {
  props: ["faq"]
};
</script>
<style lang=""></style>
