<template>
  <div class="Review review-box">
    <h1>{{title}}</h1>
    <h4>{{desc}}</h4>
  </div>
</template>

<script>
export default {
  name: "Review",
  props: ["title", "desc", "rating"],
  data() {
    return {};
  }
};
</script>
<style>
.review-box{
border: 1px solid #bfbfbf;
padding: 5px;
margin: 5px;
}
</style>
