<template>
  <div class="hello">
    <SlapButton></SlapButton>
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
  #home-banner img {
    height: 550px;
    width: 100%;
    margin-bottom: 20px;
  }

</style>
