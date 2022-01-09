<template>
  <div class="section">
    <div class="section rocket-circles row">
      <div class="content">
        <slot />
      </div>
      <img :src="require(`@/assets/images/rocket-man.png`)" />
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style>
.rocket-circles {
  height: 350px;
  background: #f9f9f9;
  border-radius: 20px;
  background-size: contain;
  background-position: right bottom;
  background-repeat: no-repeat;
  background-image: url(@/assets/images/circles.png);
}
.rocket-circles .content {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  width: 40%;
  padding-bottom: 2rem;
}
.rocket-circles .content h3 {
  color: #151518;
  font-size: 2rem;
}
.rocket-circles .content p {
  color: rgba(21, 21, 24, 0.8);
  font-size: 20px;
  line-height: 160%;
  font-family: "Nexa Light";
}
.rocket-circles .content a {
  width: max-content;
}
</style>
