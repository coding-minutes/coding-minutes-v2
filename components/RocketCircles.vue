<template>
  <div class="section">
    <div class="section rocket-circles row">
      <div class="content">
        <h3>
          {{ heading }}
          <span class="badge" v-if="new_badge">
            NEW
          </span>
        </h3>
        <p>{{ description }}</p>
        <a :href="button_url" target="_blank" rel="noopener noreferrer">
          <button class="btn btn-purple">
            {{ button_content }}
          </button>
        </a>
      </div>
      <img :src="require(`@/assets/images/rocket-man.png`)" />
    </div>
  </div>
</template>
<script>
export default {
  props: ["heading", "description", "new_badge", "button_content", "button_url"]
};
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

}
.rocket-circles .content a {
  width: max-content;
}
.badge {
  background: linear-gradient(90deg, #e73c3c 0%, #ff5b37 100%);
  border-radius: 10px;
  color: white;
  padding: 0.5rem 0.5rem;
  font-size: 22px;
}
</style>
