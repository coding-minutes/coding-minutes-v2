<template>
  <nav class="top-navbar">
    <div class="wrapper">
      <div class="row no-gutters align-items-center justify-content-between">
        <NuxtLink to="/">
          <img :src="require(`@/assets/images/cm_logo.png`)" class="logo" />
        </NuxtLink>
        <div
          class="link-box d-md-block order-12 order-2-md flex-row"
          v-bind:class="isActive ? 'toggle' : ''"
        >
          <div class="links" v-on:click="toggleMenu">
            <nuxt-link
              :to="{
                path: '/',
                hash: '#courses'
              }"
              class="nav-link"
            >
              Courses
            </nuxt-link>
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
        <div
          v-bind:class="isActive ? 'toggle' : ''"
          class="hamburger d-block d-md-none"
          v-on:click="toggleMenu"
        >
          <div class="line line1"></div>
          <div class="line line2"></div>
          <div class="line line3"></div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data: () => ({
    isActive: false
  }),
  methods: {
    toggleMenu() {
      this.isActive = !this.isActive;
    }
  }
};
</script>

<style>
.top-navbar {
  border-bottom: 1px solid #eaeaea;
  width: 100%;
  overflow: hidden;
  position: fixed;
  z-index: 100;
  background: white;
}

.link-box {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  transition: all 0.5s ease-in-out;
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
.link-box .links .nav-link:hover {
  color: #5848ea;
}

.login-button {
  white-space: nowrap;
  background-color: white;
}

.top-navbar .logo {
  height: 100%;
  max-height: 20px;
}
.hamburger {
  transform: translate(-35%, 20%);
  z-index: 3;
  cursor: pointer;
  min-height: 5rem;
}

.hamburger .line {
  width: 30px;
  height: 3px;
  margin: 5px;
  background: linear-gradient(90deg, #5848ea 0%, #9549eb 100%);
  transition: all 0.3s ease;
}

.toggle .line1 {
  transform: rotate(-45deg) translate(-5px, 6px);
}
.toggle .line2 {
  opacity: 0;
}

.toggle .line3 {
  transform: rotate(45deg) translate(-5px, -6px);
}

@media screen and (max-width: 768px) {
  .link-box {
    display: none;
    bottom: 0;
    left: 0;
    top: 5rem;
    right: 0;
    z-index: 50;
  }
  .link-box .links {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    gap: 12rem;
  }
  .link-box.toggle {
    display: block;
    position: fixed;
    background: white;
  }
  .link-box .links .nav-link {
    font-size: 2.3rem;
  }
}
</style>
