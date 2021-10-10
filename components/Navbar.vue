<template>
  <nav class="navbar">
    <img src="https://minio.codingminutes.com/assets/cm-logo-oneline.svg" />
    <div class="link-box">
      <div class="links">
        <a href="" class="nav-link">Home</a>
        <a href="" class="nav-link">Courses</a>
        <a href="" class="nav-link">Events</a>
        <a href="" class="nav-link">Online IDE</a>
        <a href="" class="nav-link">Campus Captain</a>
        <a href="" class="nav-link">About us</a>
        <a href="" class="nav-link">Contact Us</a>
      </div>
      <button class="login-button">
        Login now
      </button>
    </div>
  </nav>
</template>

<script></script>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-around;
  height: 10vh;
  /* position: fixed;
    top: 0;
    left: 0;
    right: 0; */
  padding: 0.5em 2em;
}

.link-box {
  display: flex;
  justify-content: space-around;
}

.login-button {
  height: 4em;
  width: 7em;
}
</style>
