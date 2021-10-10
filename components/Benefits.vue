<template>
  <div>
    <h2>Udemy + Coding minutes advantage</h2>
    <h4>Now spend less than a Pizza 🍕, Learn more than ever💡</h4>

    <div class="benefits-list">
      <BenefitCard
        v-for="benefit in Benefits"
        :key="benefit.title"
        :benefit="benefit"
      />
    </div>
  </div>
</template>
<script>
import Benefits from "@/data/benefits.json";
import BenefitCard from "@/components/BenefitCard";

export default {
  components: {
    BenefitCard
  },
  data() {
    return {
      Benefits
    };
  }
};
</script>
<style>
.benefits-list {
  display: grid;
  grid-template-columns: 2;
}
</style>
