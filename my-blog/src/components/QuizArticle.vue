<template>
    <h2>{{question}}</h2>
    <div v-for="(answer, index) in answers" :key="index">
      <b-button @click="checkAnswer(index)" variant="outline-primary">{{answer}}</b-button>
    </div>
</template>

<script>
export default {
  name: 'QuizArticle',
  props: ['question','answers','correct'],
  methods: {
    checkAnswer(index) {
      alert("Du klickade på svar nummer : " + index)
      // To-Do: kolla om index är samma som correct! 
      // Rätta svaret importerar vi ju som prop!
      this.$emit("answered", index+2 )
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
