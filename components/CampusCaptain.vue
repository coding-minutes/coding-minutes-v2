<template>
  <div class="section campus-captain-section row">
    <div>
      <h1>
        Campus Captain 🏁
        <span class="orange-new"> NEW </span>
      </h1>
      <p class="subheading">
        Become a Campus Captain for your campus, win swags, Coding T-Shirts &
        cash incentives!
      </p>
      <button class="btn btn-purple">
        Join as Campus captain
      </button>
    </div>
    <div>
      <img :src="require('@/assets/images/rocket-man.png')" height="250px" />
    </div>
  </div>
</template>

<script></script>
<style>
.campus-captain-section {
  background: #f9f9f9;
  border-radius: 20px;
  margin: 5rem;
  padding-top: 3rem;
  padding-bottom: 3rem;
}
.orange-new {
  background: linear-gradient(90deg, #e73c3c 0%, #ff5b37 100%);
  border-radius: 10px;
  color: white;
  font-size: 1rem;
  padding: 8px 15px;
}
.campus-captain-section .subheading {
  color: #151518cc;
}
</style>
