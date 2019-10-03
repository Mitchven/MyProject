<template>
  <div>
    <b-navbar toggleable="lg" type="dark" class="bg-secondary" variant="secondary">
      <b-navbar-brand href="#" class="text text-light" id="title">EASAKAY</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-navbar-nav>
            <b-nav-item v-on:click="redirect('/Login')" class="text text-light" id="login" v-if="auth.user === null">Login</b-nav-item>
            <b-nav-item v-on:click="redirect('/Register')" class="text text-light" id="signup" v-if="auth.user === null">Register</b-nav-item>
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
