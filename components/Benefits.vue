<template>
  <div class="section benefits">
    <h2 class="heading">
      <img :src="require('@/assets/images/udemy.png')" />
      Udemy + Coding minutes advantage
    </h2>
    <h4 class="subheading">
      Now spend less than a Pizza 🍕, Learn more than ever💡
    </h4>

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
.benefits {
  margin-top: 5rem;
}
.benefits-list {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  align-items: end;
  background: #f9f9f9;
  border-radius: 20px;
  padding: 4rem 4rem;
  gap: 45px;
}
.benefits .heading {
  text-align: center;
  font-size: 2.4rem;
}
.benefits .heading img {
  height: 2rem;
}
.benefits .subheading {
  color: #151518cc;
  text-align: center;
  font-size: 1.4rem;
}
</style>
