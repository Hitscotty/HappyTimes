<template>
  <div class="ui fluid container" id="header">
    <div class="row">
      <div class="ui fluid secondary menu">
        <NavItem :NavData="{title:'Home',link:'/'}"></NavItem>
        <NavItem :NavData="{title:'Previous Moments',link:'/'}"></NavItem>
        <NavItem :NavData="{title:'Moment of the Day',link:'/'}"></NavItem>
        <div class="right menu">
          <SearchBar></SearchBar>
          <NavItem :NavData="{title:'Login',link:'/login'}"></NavItem>
        </div>
      </div>
    </div>
    <div class="row">
      <div id="home-banner" class="ui fluid container">
      </div>
    </div>
  </div>
</template>

<script>
  import SearchBar from "./SearchBar";
  import NavItem from "./NavItem";

  export default {
    name: "NavigationBar",
    data() {
      return {
        links: ["Previous Moments", "Moment of the Day", ""]
      };
    },
    components: {
      SearchBar,
      NavItem
    }
  };

</script>

<style scoped>
  #header {
    top: 0;
    margin: 10px;
    position: fixed;
  }

  #home-banner {
    background-image: url("../assets/globe.gif");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    height: 250px;
    margin: 20px;
  }

</style>
