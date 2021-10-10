<template>
  <div>
    <h1>Loved by students across the world ❤️</h1>

    <div class="review-card">
      <h3>500+</h3>
      <p>
        Colleges covered
      </p>
    </div>

    <div class="review-card">
      <div>
        <h3>4.7 (10K ratings)</h3>
        <p>
          Average rating
        </p>
        <img :src="require(`@/assets/images/star.png`)" />
      </div>
    </div>

    <div class="review-card">
      <img :src="require(`@/assets/images/user1.jpg`)" />
      <p>
        This course by Prateek Bhaiya is actually amazing, IF you are someone
        who has done the basics of DS that is till Arrays and Recursion. This is
        the best course you could have asked for, interesting problems and way
        more interesting discussions on them. Have not found any course like
        this. Much love to prateek bhaiya for doing this!
      </p>
      <h3>Hermione Granger</h3>
    </div>

    <div class="review-card">
      <p>
        This is a masterpiece and if you are one who wants to level up your
        programming and problem solving skills.
      </p>
      <h3>Harry Potter</h3>
    </div>

    <div class="review-card">
      <h2>50+</h2>
      <h3>
        Countries covered
      </h3>
    </div>

    <div class="review-card">
      <img :src="require(`@/assets/images/user2.jpg`)" />
      <p>
        I was preparing DS and Algorithms since few years now on and off. But
        this is well structured and upon proper practice of all the patterns
        explained in this videos curriculum one can definitely crack a coding
        interview and develop a good problem solving nature (by practice).
        Thanks you Coding Minutes. Thank you prateek bhaiya.
      </p>
      <h3>Ron Weasley</h3>
    </div>

    <div class="review-card">
      <div>
        <h2>60,000+</h2>
        <h3>Students taught</h3>
      </div>
      <img :src="require(`@/assets/images/thumbs_up.png`)" />
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style>
.review-card {
  border: 1px solid black;
  padding: 2rem;
  border-radius: 2rem;
  margin: 2rem;
}
</style>
