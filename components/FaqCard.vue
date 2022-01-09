<template>
  <div class="faq-card">
    <strong>{{ faq.question }}</strong>
    <p>{{ faq.answer }}</p>
  </div>
</template>
<script>
export default {
  props: ["faq"]
};
</script>
<style>
.faq-card {
  border: 1px solid #d8d8d8;
  padding: 2.5rem 1.5rem 1.5rem 1.5rem;
  margin: 2rem 2rem;
  border-radius: 1rem;
}

.faq-card strong {
  color: #151518;
  font-size: 1.2rem;
}

.faq-card p {
  margin-top: 2rem;
  color: #5b5b5d;
  font-size: 1rem;
  font-family: "Nexa Light";
}
</style>
