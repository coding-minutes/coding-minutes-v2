<template>
  <nav class="top-navbar">
    <div class="wrapper">
      <div class="row no-gutters align-items-center justify-content-between">
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
              class="nav-link blue"
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
      </div>
    </div>
  </nav>
</template>

<script></script>

<style>
.top-navbar {
  border-bottom: 1px solid #eaeaea;
  width: 100%;
}

.link-box {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

.link-box .links {
  display: flex;
  align-items: center;
}

.link-box .links .nav-link {
  text-decoration: none;
  color: #151518;
  font-size: 1.6rem;
  padding: 2rem;
}

.link-box .links .nav-link.home {
  font-family: inherit;
}

.login-button {
  white-space: nowrap;
  background-color: white;
}

.top-navbar .logo {
  height: 100%;
  max-height: 20px;
}
</style>
