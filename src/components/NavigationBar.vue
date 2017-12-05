<template>
  <div class="ui secondary  menu">
    <NavItem :NavData="{title:'Home',link:'/'}"></NavItem>
    <NavItem :NavData="{title:'Previous Moments',link:'/'}"></NavItem>
    <NavItem :NavData="{title:'Moment of the Day',link:'/'}"></NavItem>
    <div class="right menu">
      <SearchBar></SearchBar>
      <NavItem :NavData="{title:'Login',link:'/login'}"></NavItem>
    </div>
  </div>
</template>

<script>
  import SearchBar from './SearchBar'
  import NavItem from './NavItem'

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
