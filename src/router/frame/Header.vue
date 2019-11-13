<template>
  <div>
    <b-navbar toggleable="lg" type="dark" class="bg-secondary" variant="secondary">
      <b-navbar-brand href="#" class="text text-light" id="title">EASAKAY</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-navbar-nav>
            <button v-on:click="redirect('/Login')" class="text text-light" id="login" v-if="auth.user === null">Login</button>
            <button v-on:click="redirect('/Register')" class="text text-light" id="register" v-if="auth.user === null">Register</button>
          </b-navbar-nav>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>
<style scoped lang="scss">
@import "assets/colors.scss";
#title {
  color: $info !important;
}
#login ,#register{
  background-color: skyblue;

}
</style>
<script>
import ROUTER from "router";
import AUTH from 'services/auth'
export default {
  data(){
    return{
      auth:AUTH
    }
  },
  methods: {
    redirect(router) {
      ROUTER.push(router);
    }
  }
};
</script>
