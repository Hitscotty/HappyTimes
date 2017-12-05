<template>
  <div class="hello">


    <div id="home-banner" class="ui fluid container">
    </div>

    <SlapButton></SlapButton>

    <h1>{{ msg }}</h1>

  </div>
</template>

<script>
  import SlapButton from "./SlapButton";

  export default {
    name: "HomePage",
    data() {
      return {
        msg: "Welcome to Happy Times"
      };
    },
    components: {
      SlapButton
    }
  };

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #home-banner {
    background-image: url("../assets/globe.gif");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    height: 350px;
    margin: 20px;
  }

  #home-banner img {
    height: 550px;
    width: 100%;
    margin-bottom: 20px;
  }

</style>
