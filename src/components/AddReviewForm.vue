<template>
  <div class="AddReview">
  <form>
    <h3>Score</h3>
    <input type="text" v-model="score" required>
    <h3>Title</h3>
    <input type="text" v-model="title" required>
    <h3>Review</h3>
    <input type="text" v-model="review" required>
    <button
      v-on:submit="
        $emit('submit-add-review', {
          score: score,
          title: title,
          review: review
        })
      "
    >
      Submit
    </button>
    <button v-on:reset="$emit('hide-add-review')">Close</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "AddReview",
  data() {
    return {
        score: 0,
        title: "rating",
        review: "desc"
    };
  }
};
</script>
<style>
</style>
