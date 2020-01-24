<template>
  <div class="landing-wrapper">
    <div>
    <ul>
        <li v-for="review in reviewList" v-bind:key="review">
          <Review v-bind:title="review.title" v-bind:desc="review.review"
            v-bind:rating="review.rating" />
        </li>
    </ul>
    
    </div>
  </div>
</template>

<script>

import Review from "@/components/Review.vue";

export default {
  name: "LandingPage",
  props: ["reviewList"],
  components: {
    Review
  },
  data() {
    return {};
  }
};
</script>
<style>
.landing-wrapper {
  padding: 5rem;
  text-align: center;
}

.landing-wrapper h2 {
  font-size: 7rem;
}

.landing-wrapper .app-description {
  padding: 3rem 0;
  font-size: 2rem;
  text-align: center;
  color: #44576e;
}

</style>
