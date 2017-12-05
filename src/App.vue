<template>
  <div id="app" class="fluid container">
    <NavigationBar></NavigationBar>
    <div id="content" class="ui middle aligned center aligned grid">
      <router-view/>
    </div>
    <Footer></Footer>
  </div>
</template>

<script>
  import NavigationBar from "./components/NavigationBar"
  import Footer from './components/Footer'

  export default {
    name: "app",
    components: {
      NavigationBar,
      Footer
    }
  };

</script>

<style>
  #app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 10px;
    height: 100vh;
  }

  #content {
    display: flex;
    align-items: center;
    justify-content: space-around;
    height: 100%;
  }

</style>
