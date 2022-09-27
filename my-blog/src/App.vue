<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <BlogHeader></BlogHeader>
  <!-- Dynamiska attribut, vi kan skicka in data till komponenten -->
  <!--<BlogArticle :title="post.title" :content="post.content"></BlogArticle>-->
  
  <!-- Generating components from a data object using v-for -->
  <div v-for="(post, index) in posts" :key="index">
    <!-- Binding multiple properties using an object-->
    <BlogArticle v-bind="post"></BlogArticle>
  </div>
</template>

<script>
import BlogHeader from "./components/BlogHeader.vue";
import BlogArticle from "./components/BlogArticle.vue";


export default {
  name: 'App',
  data: function() {
    return {
      posts: [{
        title: "Min första rubrik",
        content: "Mitt första blogginlägg"
      },
      {
        title: "Min andra rubrik",
        content: "Mitt andra blogginlägg"
      }]
    }
  },
  components: {
    BlogHeader,
    BlogArticle
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
