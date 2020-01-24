<template>
  <div class="landing-wrapper">
    <div class="left">
    <BookDetail />
    </div>
    <div class="right">
    <ReviewListing v-bind:reviewList = "reviewList" />
    </div>
    <div class="lower">
    <AddReviewBtn v-on:show-add-review="addReview=true" v-if="!addReview" />
    <AddReviewForm v-on:submit-add-review="object = $event;reviewList.push($event); addReview = false;" v-on:hide-add-review="addReview=false" v-if="addReview" />
    </div>
  </div>
</template>

<script>

import BookDetail from "@/components/BookDetail.vue";
import ReviewListing from "@/components/ReviewListing.vue";
import AddReviewBtn from "@/components/AddReviewBtn.vue";
import AddReviewForm from "@/components/AddReviewForm.vue";
export default {
  name: "LandingPage",
  components: {
    BookDetail,
    ReviewListing,
    AddReviewBtn,
    AddReviewForm
  },
  data() {
    return {
      welcomeMsg: "Welcome to Mini Good Read",
      appDesc:
        "A sample app developed to serve the purpose of learning Vue at VueFest 2020",
      addReview:false,
      object: {},
      reviewList: [
        { title: "Rating 1", review: "Description of rating 1", rating: 1 },
        { title: "Rating 2", review: "Description of rating 2", rating: 2 },
        { title: "Rating 3", review: "Description of rating 3", rating: 3 },
        { title: "Rating 4", review: "Description of rating 4", rating: 4 },
        { title: "Rating 5", review: "Description of rating 5", rating: 5 },
        { title: "Rating 6", review: "Description of rating 6", rating: 6 }
      ]
    };
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

.left{
margin-top: 100px;
width: 50%;
float: left}

.right{
width: 50%;
float: left
}

.lower{
width:100%}

</style>
