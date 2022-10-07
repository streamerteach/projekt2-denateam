<template>
    <h2>{{question}}</h2>
    <div v-for="(answer, index) in answers" :key="index">
      <b-button variant="outline-primary">{{answer}}</b-button>
    </div>
</template>

<script>
export default {
  name: 'QuizArticle',
  props: ['question','answers','correct']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
