<template>
  <div class="main-section hero">
    <div class="wrapper">
      <div class="row no-gutters align-items-center justify-content-between position-relative">
        <div class="hero-content flex-1">
          <div class="mega-title">Kickstart your</div>
          <div class="mega-title gradient-text-purple">Coding Career in Minutes</div>
          <div class="mt-5 main-section__core-text">
             <!--TODO: Remove this above main-section__core-text class after creating standard font-size classes-->
            <strong> Pocket friendly courses</strong> with interactive content,
            top-notch instructors, TA support, Projects & Assignments.
          </div>
          <div class="mt-5">
            <button class="button-core button-primary mr-5">Explore courses</button>
            <button class="button-core button-secondary">
              <!-- TODO: Insert play icon here -->
              Learn more
            </button>
          </div>
        </div>
        <img src="https://codingminutes.com/imgs/model.png" class="hero-image"/>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>

<style>
.hero-content {
  padding-right: 30vw;
}
.hero p {
  font-size: 1.5rem;

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
  border: unset;
}
.btn-purple {
  background: linear-gradient(90deg, #5848ea 0%, #9549eb 100%);
  font-size: 1rem;
  color: white !important;
  border: none;
}
.btn-white {
  color: #5848ea;
  border: 1px solid;
  outline: linear-gradient(90deg, #5848ea 0%, #9549eb 100%);
  margin: 0 1rem;
  background: white;
}

.hero-image {
  position: absolute;
  right: 0;
  bottom: -14rem;
}
</style>
