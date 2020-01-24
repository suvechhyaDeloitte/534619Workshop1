<template>
  <div class="BookDetail">
  <div class="image">
    <img v-bind:src="image" />
    </div>
    <h1>{{title}}</h1>
    <h4>{{desc}}</h4>
  </div>
</template>

<script>
export default {
  name: "BookDetail",
  data() {
    return {
      image: "./assets/book-cover.png",
      title: "You don't know JS - part 2",
      desc:
        "The book is a series of books which explore Javascript types in greater depth."
    };
  }
};
</script>
<style>
.image{
height: 200px;
border: 1px solid black;
}
</style>
