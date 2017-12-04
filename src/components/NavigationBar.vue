<template>
  <div class="ui secondary  menu">
    <a class="active item">
      Home
    </a>
    <a class="item">
      Messages
    </a>
    <a class="item">
      Friends
    </a>
    <div class="right menu">
      <SearchBar></SearchBar>
      <a class="ui item">
        Logout
      </a>
    </div>
  </div>
</template>

<script>
  import SearchBar from './SearchBar'

  export default {
    name: "NavigationBar",
    data() {
      return {
        links: ["Previous Moments", "Moment of the Day", ""]
      };
    },
    components: {
      SearchBar
    }
  };

</script>
