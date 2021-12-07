<template>
  <div class="hero section">
    <div class="hero-content">
      <h1>Kickstart your</h1>
      <h1 class="purple">Coding Career in Minutes</h1>
      <p>
        <strong> Pocket friendly courses</strong> with interactive content,
        top-notch instructors, TA support, Projects & Assignments.
      </p>
      <div>
        <button class="btn btn-purple">Explore courses</button>
        <button class="btn btn-white">
          <!-- TODO: Insert play icon here -->
          Learn more
        </button>
      </div>
    </div>
    <img src="https://codingminutes.com/imgs/model.png" />
  </div>
</template>
<script>
export default {};
</script>

<style>
.hero {
  display: flex;
}
.hero-content {
  margin-top: 2rem;
  margin-right: 4rem;
}
.hero p {
  font-size: 1.5rem;
  font-family: "Nexa Light";
}
.hero p strong {
  font-family: "Nexa Bold";
}
.hero h1 {
  font-size: 2.4rem;
  margin: 0.3rem 0;
}
.purple {
  color: #5848ea;
}
.btn {
  padding: 0.8rem 1.4rem;
  font-size: 1rem;
  border-radius: 2rem;
  cursor: pointer;
}
.btn-purple {
  background: linear-gradient(90deg, #5848ea 0%, #9549eb 100%);
  font-size: 1rem;
  color: white;
  border: none;
}
.btn-white {
  color: #5848ea;
  border: 1px solid;
  outline: linear-gradient(90deg, #5848ea 0%, #9549eb 100%);
  margin: 0 1rem;
}
</style>
