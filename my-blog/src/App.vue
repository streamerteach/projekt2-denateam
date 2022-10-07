<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <QuizHeader :currentQ="currentQ" :score="score"></QuizHeader>
  
  <QuizArticle v-bind="questions[currentQ]"></QuizArticle>

</template>

<script>
import QuizHeader from "./components/QuizHeader.vue";
import QuizArticle from "./components/QuizArticle.vue";


export default {
  name: 'App',
  data: function() {
    return {
      currentQ: 0,
      score: 0,
      questions: [{
        question: "Hur går det?",
        answers: ["Bra","Dåligt","Semi"],
        correct: 1
      },
      {
        question: "Är fem myror fler än fyra elefanter",
        answers: ["Sant","Falskt"],
        correct: 1
      }]
    }
  },
  components: {
    QuizHeader,
    QuizArticle
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
