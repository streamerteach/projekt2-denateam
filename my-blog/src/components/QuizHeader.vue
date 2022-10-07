<template>
    <h1>Time for question {{currentQ + 1}}</h1>
    <p>Your current score is: {{ score }}</p>
</template>

<script>
export default {
  name: 'QuizHeader',
  props: ["currentQ", "score"]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
