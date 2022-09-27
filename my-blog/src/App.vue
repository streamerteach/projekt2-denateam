<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <BlogHeader></BlogHeader>
  <BlogArticle title="Min första statiska prop rubrik" content="Ett inlägg"></BlogArticle>
  <BlogArticle title="Min andra rubrik" content="Mitt andra inlägg"></BlogArticle>
</template>

<script>
import BlogHeader from "./components/BlogHeader.vue";
import BlogArticle from "./components/BlogArticle.vue";


export default {
  name: 'App',
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
