<template>
  <div class="section faq-section">
    <h1>
      Frequently asked questions 👋
    </h1>
    <div class="faq-container">
      <FaqCard v-for="faq in faqs" :key="faq.question" :faq="faq" />
    </div>
  </div>
</template>
<script>
import FaqCard from "@/components/FaqCard.vue";
import faqs from "@/data/faqs";

export default {
  components: {
    FaqCard
  },
  data() {
    return {
      faqs
    };
  }
};
</script>
<style scoped>
.faq-section {
  margin: 0 auto;
}
.faq-section h1 {
  text-align: center;
}
.faq-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
</style>
