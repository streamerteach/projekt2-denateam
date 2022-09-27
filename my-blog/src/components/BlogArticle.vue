<template>
    <h2>{{title}}</h2>
    <p>{{content}}</p>
</template>

<script>
export default {
  name: 'BlogArticle',
  props: ['title','content']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
