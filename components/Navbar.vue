<template>
  <nav class="navbar section">
    <NuxtLink to="/">
      <img :src="require(`@/assets/images/cm_logo.png`)" class="logo" />
    </NuxtLink>
    <div class="link-box">
      <div class="links">
        <nuxt-link
          :to="{
            path: '/',
            hash: '#courses'
          }"
          class="nav-link"
          >Courses</nuxt-link
        >
        <a
          href="https://www.scaler.com/"
          class="nav-link"
          target="_blank"
          rel="noopener noreferrer"
        >
          Live Courses
        </a>
        <a
          href="https://ide.codingminutes.com/"
          class="nav-link"
          target="_blank"
          rel="noopener noreferrer"
        >
          Online IDE
        </a>
        <a href="" class="nav-link">Campus Captain</a>
        <!-- <a href="" class="nav-link">About us</a>
        <a href="" class="nav-link">Contact Us</a> -->
      </div>
      <!-- <button class="login-button btn btn-white">
        Login now
      </button> -->
    </div>
  </nav>
</template>

<script></script>

<style>
.navbar {
  display: flex;
  justify-content: space-around;
  align-items: center;
  height: 8vh;
  border-bottom: 1px solid #eaeaea;
}

.link-box {
  display: flex;
  justify-content: end;
  align-items: center;
  width: 74vw;
}

.link-box .links {
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 70%;
}

.link-box .links .nav-link {
  text-decoration: none;
  color: #151518;
  font-family: "Nexa Light";
}

.link-box .links .nav-link.home {
  font-family: inherit;
}

.login-button {
  white-space: nowrap;
  background-color: white;
}

.navbar .logo {
  height: 2vh;
}
</style>
