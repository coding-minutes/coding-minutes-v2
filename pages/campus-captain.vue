<template>
  <div class="campus-captain-page">
    <Navbar />
    <!-- Campus captain hero section -->
    <div class="hero section">
      <div class="hero-content">
        <h1 class="heading">Campus Captain 🏁</h1>
        <h2 class="subheading">Join Coding Minutes Family</h2>
        <p>
          Become a Campus Captain for your campus, win swags, Coding T-Shirts &
          cash incentives!
        </p>
        <div>
          <button class="btn btn-purple">Join as Campus captain</button>
        </div>
      </div>
      <div class="campus-hero-images">
        <img
          :src="require('@/assets/images/captain_heroes.png')"
          class="heroes"
        />
        <img
          :src="require('@/assets/images/yellow_money.png')"
          class="yellow-money floating"
        />
        <img
          :src="require('@/assets/images/red_gift.png')"
          class="red-gift floating"
        />
        <img
          :src="require('@/assets/images/green_chat.png')"
          class="green-chat floating"
        />
        <img
          :src="require('@/assets/images/pink_star.png')"
          class="pink-star floating"
        />
      </div>
    </div>

    <section class="section about-the-program row">
      <div class="content">
        <h3>About the program</h3>
        <p>
          At Coding Minutes, we call our Campus Ambassadors as Campus Captains.
          Our captains are highly skilled, motivated individuals and leaders in
          their own campus.
        </p>
        <p>
          If you think you are someone who is curious to learn new skills, make
          new friends, spread knowledge and believes in getting things done,
          then this program is just perfect for you.
        </p>
      </div>
      <div class="highlights">
        <div class="highlight">
          <h1 class="title">100K+</h1>
          <div class="label">Cash Incentives Given</div>
        </div>

        <div class="highlight">
          <h1 class="title">10K+</h1>
          <div class="label">Campus Captains</div>
        </div>

        <div class="highlight">
          <h1 class="title">4K+</h1>
          <div class="label">Colleges Covered</div>
        </div>

        <div class="highlight">
          <h1 class="title">10K+</h1>
          <div class="label">Campus Captains</div>
        </div>
      </div>
    </section>

    <section class="section perks">
      <h1>Perks of a Campus Captain 🔥</h1>
      <h2>
        Some of the benefits that you will enjoy exclusively as Campus Captain!
      </h2>
      <div class="perks-list">
        <PerkCard
          heading="Course Giveaways"
          image="gift_hand.png"
          content="Based upon your performance, Campus Captains will be eligible for free online courses & LIVE mentoring in coding gyms."
        />
        <PerkCard
          heading="Networking"
          image="world.png"
          content="Becoming a Campus Captain, will help you broaden your reach and build your campus coding community. Overall you will grow your network a lot."
        />
        <PerkCard
          heading="Leadership"
          image="boxing.png"
          content="Here is your chance to improve your Leadership & Communication skills, which is often tested in interviews and in every sphere of life too."
        />
        <PerkCard
          heading="Cash Incentives"
          image="money-bag.png"
          content="Our referal program entitles you to win huge cash incentives for every successful referal. Top performers will win extra bonus."
        />
        <PerkCard
          heading="Goodies & Swags"
          image="surprise.png"
          content="Completing 6 months successfully in the program, unlocks your Swagkit containing supercool T-Shirt, Sipper, Stickers & swags."
        />
        <PerkCard
          heading="Excellence Certificate"
          image="tattoo-studio.png"
          content="Completing 6 months successfully in the program, unlocks your Swagkit containing supercool T-Shirt, Sipper, Stickers & swags."
        />
      </div>
    </section>

    <section class="section application-timeline">
      <h1>Application Timeline 👋</h1>
      <div class="container row">
        <div class="timeline">
          <div class="row">
            <img :src="require(`@/assets/images/pencil.png`)" />
            <div class="timeline-step">
              <h3>1. Apply on the given link</h3>
              <p>
                Fill our your details in the Google Form attached below and wait
                for ~1 week for us to review your application.
              </p>
            </div>
          </div>
          <div class="row">
            <img :src="require(`@/assets/images/telephone.png`)" />
            <div class="timeline-step">
              <h3>2. Telephonic Interview</h3>
              <p>
                Once your application is accepted, we will schedule a phone call
                with you to learn about you and your experiences.
              </p>
            </div>
          </div>
          <div class="row">
            <img :src="require(`@/assets/images/police-badge.png`)" />
            <div class="timeline-step">
              <h3>3. Get Offer Letter</h3>
              <p>
                Once we are convinced that you are good fit for this role, you
                will get your offer letter in about ~1-2 weeks and you can start
                working.
              </p>
            </div>
          </div>
        </div>
        <img :src="require(`@/assets/images/rocket-man.png`)" />
      </div>
    </section>

    <section class="section captain-testimonials">
      <h4>What our Captains Say? ❤️</h4>
      <div class="row">
        <TestimonialCard
          v-for="testimonial in TestimonialList1"
          :picture="testimonial.picture"
          :quote="testimonial.quote"
          :name="testimonial.name"
          :institute="testimonial.institute"
          :key="testimonial.name"
        />
      </div>
      <div class="row">
        <TestimonialCard
          v-for="testimonial in TestimonialList2"
          :picture="testimonial.picture"
          :quote="testimonial.quote"
          :name="testimonial.name"
          :institute="testimonial.institute"
          :key="testimonial.name"
        />
      </div>
    </section>

    <section class="section">
      <div class="section row start-your-journey ">
        <div class="content">
          <h3>
            Start your journey now 🏁
          </h3>
          <p>
            Campus Captain Applications are currently open. Complete the
            application form to hear back from us.
          </p>
          <a href="#" target="_blank" rel="noopener noreferrer">
            <button class="btn btn-purple">
              Join as Campus captain
            </button>
          </a>
        </div>
        <img :src="require(`@/assets/images/captain_heroes.png`)" />
      </div>
    </section>

    <FAQs />
    <Footer />
  </div>
</template>
<script>
import Navbar from "@/components/Navbar.vue";
import PerkCard from "@/components/PerkCard.vue";
import TestimonialCard from "@/components/TestimonialCard.vue";
import FAQs from "@/components/FAQs.vue";
import Footer from "@/components/Footer.vue";
import TestimonialList from "@/data/captain_testimonials.json";
export default {
  components: {
    Navbar,
    PerkCard,
    TestimonialCard,
    FAQs,
    Footer
  },
  data() {
    const TestimonialList1 = TestimonialList.slice(0, 3);
    const TestimonialList2 = TestimonialList.slice(-3);
    return {
      TestimonialList1,
      TestimonialList2
    };
  }
};
</script>
<style>
.campus-captain-page .hero .heading {
  font-size: 40px;
}
.hero .subheading {
  font-size: 32px;
  font-family: "Nexa Light";
}
.campus-captain-page .hero p {
  font-size: 24px;
  font-family: "Nexa Light";
  margin: 4rem 0;
  color: rgba(21, 21, 24, 0.8);
  line-height: 160%;
}
.campus-captain-page .hero button {
  font-size: 18px;
}
.campus-hero-images {
  width: 50vw;
  margin-left: 5vw;
  position: relative;
}
.campus-hero-images .floating {
  position: absolute;
  height: 5rem;
}
.campus-hero-images .yellow-money {
  top: 4rem;
  left: -6rem;
}
.campus-hero-images .red-gift {
  top: 3rem;
  right: 2rem;
}
.campus-hero-images .green-chat {
  bottom: 8rem;
  left: -2rem;
}
.campus-hero-images .pink-star {
  bottom: 10rem;
  right: 1rem;
}

.about-the-program {
  background: #f9f9f9;
  padding-bottom: 4rem;
  margin-bottom: 2rem;
}
.about-the-program .content h3 {
  font-size: 32px;
  line-height: 160%;
}
.about-the-program .content p {
  font-family: "Nexa Light";
  padding-right: 9rem;
  font-size: 18px;
  line-height: 160%;
  color: #444446;
}
.highlights {
  width: 60vw;
  margin-left: 4rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
}
.highlights .highlight .title {
  font-size: 45px;
  line-height: 160%;
  font-weight: bold;
  margin-bottom: 0rem;
}
.highlights .highlight .label {
  font-family: "Nexa Light";
  font-size: 22px;
  line-height: 160%;
  margin-top: 0.2rem;
}

.perks h1 {
  text-align: center;
  font-size: 40px;
  line-height: 160%;
}
.perks h2 {
  font-family: "Nexa Light";
  font-size: 24px;
  line-height: 28px;
  text-align: center;
  color: rgba(21, 21, 24, 0.8);
}
.perks .perks-list {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: repeat(2, 1fr);
  grid-auto-flow: row;
}
.application-timeline h1 {
  text-align: center;
  font-size: 37px;
  line-height: 160%;
}
.application-timeline .container {
  min-height: 523px;
  background: #f9f9f9;
  border-radius: 20px;
}
.application-timeline .container .timeline {
  width: 50%;
  margin-top: 2rem;
  margin-left: 3.5rem;
}
.application-timeline .container .timeline .row {
  margin-bottom: 1rem;
  gap: 1rem;
  align-items: center;
}
.application-timeline .container .timeline .row p {
  font-family: "Nexa Light";
  font-size: 16px;
  line-height: 160%;
  color: rgba(21, 21, 24, 0.6);
}
.timeline img {
  width: 56px;
  height: 56px;
}
.captain-testimonials h4 {
  text-align: center;
  font-size: 37px;
  line-height: 160%;
}
.start-your-journey {
  background: #f9f9f9;
  border-radius: 20px;
  height: 412px;
  overflow-y: hidden;
}
.start-your-journey .content {
  padding: 4rem 3rem;
}
.start-your-journey h3 {
  font-size: 37px;
  line-height: 160%;
}
.start-your-journey p {
  font-family: "Nexa Light";
  font-size: 24px;
  line-height: 160%;
  color: rgba(21, 21, 24, 0.8);
  margin-right: 9rem;
}
.start-your-journey button {
  font-size: 18px;
  margin-top: 2rem;
}
.start-your-journey img {
  height: 560px;
}
</style>
