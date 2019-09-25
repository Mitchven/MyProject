<template>
  <div id="background" style="padding-top:20px;">
    <center>
      <div id="divLogin" class="col-sm-3 my-sm-5 border rounded" style="margin-left:0.5%">
        <form class="container">
          <center>
            <h1>Login</h1>
          </center>
          <hr />
          <div class="row">
            <label for="loginUsername">Username:</label>
            <input class="form-control" placeholder="Enter Username" />
            <br />
          </div>
          <br />
          <div class="row">
            <label for="loginPassword">Password:</label>
            <input
              type="password"
              class="form-control"
              id="loginPassword"
              placeholder="Enter Password"
            />
          </div>
          <br />
          <button id="btnLogin" class="btn btn-primary btn-lg btn-block col-sm-5">
            <h4>Login</h4>
          </button>
          <br />
        </form>
      </div>
    </center>
  </div>
</template>
<script>
export default {
  data() {
    return {
      email: "",
      password: ""
    };
  },
  methods: {
    handleSubmit(e) {
      e.preventDefault();
      if (this.password.length > 0) {
        this.$http.post("http://localhost:3000/login", {
          email: this.email,
          password: this.password
        });
      }
    }
  }
};
</script>