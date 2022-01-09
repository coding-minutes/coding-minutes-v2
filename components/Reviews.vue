<template>
  <div class="section reviews">
    <h1>Loved by students across the world ❤️</h1>
    <div class="row">
      <div class="left-section">
        <div class="row">
          <div class="review-card">
            <h3>500+</h3>
            <p>
              Colleges covered
            </p>
          </div>

          <div class="review-card average-rating row">
            <div>
              <h3>4.7 (10K ratings)</h3>
              <p>
                Average rating
              </p>
            </div>
            <img :src="require(`@/assets/images/star.png`)" />
          </div>
        </div>
        <div class="row">
          <div class="review-card user-review">
            <img :src="require(`@/assets/images/user1.jpg`)" />
            <p>
              This course by Prateek Bhaiya is actually amazing, IF you are
              someone who has done the basics of DS that is till Arrays and
              Recursion. This is the best course you could have asked for,
              interesting problems and way more interesting discussions on them.
              Have not found any course like this. Much love to prateek bhaiya
              for doing this!
            </p>
            <div class="name">Hermione Granger</div>
          </div>
          <div>
            <div class="review-card user-review">
              <p>
                This is a masterpiece and if you are one who wants to level up
                your programming and problem solving skills.
              </p>
              <div class="name">Harry Potter</div>
            </div>

            <div class="review-card">
              <h2 class="plus-50">50+</h2>
              <div class="countries-covered">
                Countries covered
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="right-section">
        <div class="review-card user-review">
          <img :src="require(`@/assets/images/user2.jpg`)" />
          <p>
            I was preparing DS and Algorithms since few years now on and off.
            But this is well structured and upon proper practice of all the
            patterns explained in this videos curriculum one can definitely
            crack a coding interview and develop a good problem solving nature
            (by practice). Thanks you Coding Minutes. Thank you prateek bhaiya.
          </p>
          <div class="name">Ron Weasley</div>
        </div>

        <div class="review-card students-taught row">
          <div>
            <h2>60,000+</h2>
            <h3>Students taught</h3>
          </div>
          <img :src="require(`@/assets/images/thumbs_up.png`)" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style>
.reviews {
  margin-top: 5rem;
}
.reviews h1 {
  text-align: center;
}
.review-card {
  border: 1px solid #d8d8d8;
  padding: 0.6rem 2rem;
  border-radius: 2rem;
  margin: 2rem;
  padding-bottom: 2.5rem;
}
.review-card p {
  font-family: "Nexa Light";
  color: rgba(21, 21, 24, 0.7);
  font-size: 1.2rem;
}
.review-card .name {
  font-size: 1.5rem;
}
.row {
  display: flex;
  justify-content: space-between;
}
.row .review-card {
  width: 100;
}
.review-card.average-rating {
  background: linear-gradient(90deg, #5848ea 0%, #9549eb 100%);
  border-radius: 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: white;
  border: none;
  width: 400px;
  height: 150px;
  font-size: 1.5rem;
}
.review-card.average-rating p {
  color: inherit;
}
.review-card h3 {
  font-size: 2.1rem;
  margin-bottom: 0;
}
.review-card img {
  border-radius: 50%;
  height: 4rem;
}
.review-card.average-rating img {
  border-radius: 0;
}
.review-card.user-review img {
  padding-top: 1rem;
}
.review-card h2.plus-50 {
  font-size: 1.8rem;
}
.review-card .countries-covered {
  font-size: 1.5rem;
  color: #151518b2;
  white-space: nowrap;
}
.review-card.students-taught {
  background: linear-gradient(90deg, #f77b26 0%, #f55a47 100%);
  border-radius: 20px;
  color: white;
}
.review-card.students-taught img {
  border-radius: 0;
}
.review-card.students-taught h2 {
  font-size: 1.8rem;
}
.review-card.students-taught h3 {
  font-size: 1.5em;
}
</style>
