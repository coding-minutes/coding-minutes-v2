<template>
  <div class="section row footer">
    <div class="details">
      <img :src="require(`@/assets/images/cm_logo.png`)" />
      <p>
        Coding Minutes was started with a mission to provide affordable & high
        quality education for everyone. With Udemy as our technology partner, we
        wish to bring all our courses with top-notch content to our students at
        pocket friendly prices with lifetime access.
      </p>
      <div class="copyright">©2021 Coding Minutes. All rights reserved</div>
    </div>
    <div class="links">
      <a href="" class="footer-link">About us</a>
      <a href="" class="footer-link">Events</a>
      <a href="" class="footer-link">Courses</a>
      <a href="" class="footer-link">Campus Captain</a>
      <a
        href="https://ide.codingminutes.com/"
        class="footer-link"
        target="_blank"
        rel="noopener noreferrer"
      >
        Online IDE
      </a>
      <a href="" class="footer-link">Contact Us</a>
      <a href="" class="footer-link">Get in touch</a>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style>
.footer.section {
  padding-top: 3rem;
  background: #f9f9f9;
  height: 30vh;
}
.footer .details {
  width: 40%;
}
.footer .details img {
  height: 1.5rem;
}
.footer .details p {
  margin-top: 2rem;
  color: #151518cc;
  font-size: 1rem;
  font-family: "Nexa Light";
}
.footer .copyright {
  margin-top: 2.5rem;
  color: rgba(21, 21, 24, 0.8);
  font-size: 0.9rem;
}
.footer .links {
  width: 50%;
  font-family: "Nexa Light";
  display: grid;
  grid-template-columns: 1fr 1fr;
}
.footer-link {
  text-decoration: none;
  color: #151518;
  font-size: 1rem;
}
</style>
