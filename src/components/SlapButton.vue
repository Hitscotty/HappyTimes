<template>
  <div class="container">
    <button @click="getDecision()" class="ui primary button">Discover</button>
    <p id="results-box">
      {{choice}}
    </p>
  </div>
</template>


<script>
  export default {
    name: "SlapButton",
    data() {
      return {
        choice: null,
        decisions: [
          "Shave your head bald",
          "Smoke a pack of cigarettes",
          "Skydiving without a parachute",
          "Join a gang",
          "Take expired medicine pills",
          "Join a biker gang"
        ]
      }
    },
    methods: {
      getDecision: function () {

        var randNum = Math.floor((Math.random() * this.decisions.length) + 0);
        var randChoice = this.decisions[randNum];
        this.choice = randChoice;
        console.log(randChoice);
      }
    }
  }

</script>
