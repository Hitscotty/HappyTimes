<template>
  <div class="ui fluid center aligned container">

    <div id="results-box" :style="{'background-image': 'url(' + choice.img + ')'}">
    </div>
    <button @click="getDecision()" class="ui primary button">Discover</button>
    <h1>{{ choice.title }}</h1>

  </div>
</template>


<script>
  export default {
    name: "SlapButton",
    data() {
      return {
        choice: {
          img: "",
          title: ""
        },
        decisions: [{
            img: "https://media.istockphoto.com/photos/bald-head-picture-id168398099?k=6&m=168398099&s=612x612&w=0&h=K2iJGXxH7lqRM0jSIK4ARdsJGdEwH31IqrsA5elsC4s=",
            title: "Shave your head bald"
          },
          {
            img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQXi6GuN_X_ZSz6FDMtj5aBTD5DaqTBkJ1txQ24okpRCd6EXKPGhA",
            title: "Smoke a pack of cigarettes"
          },
          {
            img: "https://img.grouponcdn.com/deal/9cPfwCFsgGxMTyNckks7QH/tennessee_skydiving_llc-2048x1229.jpg/v1/c700x420.jpg",
            title: "Skydiving without a parachute"
          },
          {
            img: "https://i.ytimg.com/vi/07KY8yS3VKA/maxresdefault.jpg",
            title: "Join a gang"
          },
          {
            img: "https://financialtribune.com/sites/default/files/field/image/17january/04-ff-pharma_104-ab.jpg",
            title: "Take expired medicine pills"
          },
          {
            img: "http://www.bikersfortrump2016.com/uploads/6/9/6/1/6961503/2834809_orig.jpg",
            title: "Join a biker gang"
          },
          {
            img: "https://ichef.bbci.co.uk/images/ic/720x405/p05c8rnm.jpg",
            title: "Become a Trump Supporter"
          }
        ]
      }
    },
    methods: {
      getDecision: function () {

        var randNum = Math.floor((Math.random() * this.decisions.length) + 0);
        var randChoice = this.decisions[randNum];

        if (randChoice.img === this.choice.img) {
          this.getDecision();
        } else {
          this.choice = randChoice;
        }

      }
    },
    computed: {
      resultBoxImage: function () {
        console.log(`computing ${this.choice.img}`)
        return {
          'background-image': 'url(' + this.choice.img +
            ')'
        }
      }
    }
  }

</script>

<style scoped>
  #results-box {
    margin: 20px;
    height: 250px;
    width: 500px;

    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
  }

</style>
