<template>
  <div id="login-page">
    <div class="column">
      <h2 class="ui teal image header">
        <img src="../assets/applogo.png" class="image">
        <div class="content">
          Log-in to your account
        </div>
      </h2>
      <form class="ui large form">
        <div class="ui stacked segment">
          <div class="field">
            <div class="ui left icon input">
              <i class="user icon"></i>
              <input v-model="user.email" type="text" name="email" placeholder="E-mail address">
            </div>
          </div>
          <div class="field">
            <div class="ui left icon input">
              <i class="lock icon"></i>
              <input v-model="user.password" type="password" name="password" placeholder="Password">
            </div>
          </div>
          <div @click="login()" class="ui fluid large teal submit button">Login</div>
        </div>

        <div class="ui error message"></div>

      </form>

      <div class="ui message">
        New to us?
        <a href="#">Sign Up</a>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "LoginPage",
    data() {
      return {
        user: {
          email: "",
          password: ""
        }
      }
    },
    methods: {
      login: function () {

        console.log(this.user.email);
        this.$http.get("https://jsonplaceholder.typicode.com/users")
          .then(res => {

          })
      }
    }
  };

</script>

<style>


</style>
