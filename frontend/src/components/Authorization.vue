<template>
  <section class = "authorization_vue">
    <div class="login-box">
      <div class="row">
        <img
            src="../assets/images/logo.png" alt="Logo"
        />
      </div>
      <form>
        <div class="user-box">
          <input type="text" name="" required=""/>
          <label><i class="Username"></i>
            Username
          </label>
        </div>
        <div class="user-box">
          <input type="password" name="" required=""/>
          <label><i class="Unlock"></i>
            Password
          </label>
        </div>
      </form>
      <router-link :to="{name: 'MainPage'}">
        <button type="submit" class = "submit-button">LogIn</button>
      </router-link>
    </div>
  </section>
</template>


<script>
export default {

  name: "Authorization",
  beforeCreate: function() {
    document.body.className = 'auth';
  }
}
</script>

<style scoped src="../assets/styles/login_style.css">


</style>