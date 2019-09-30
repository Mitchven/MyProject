<template>
    <div>
        <div class="jumbotron">
            <h3>Edit Personal Information</h3>
        </div>
        <div class="row">
            <!-- left column -->
            <div class="card">
                <div class="text-center">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcS5ew6psjgnkJHXT40tf3ub7YJWUr9VuVHkzeBe2g5sgzlIcc3f" class="avatar img-circle" alt="avatar">
                    <h6>Upload a different photo...</h6>

                    <input type="file" class="form-control">
                    <form class="form-horizontal" role="form">
                        <div class="form-group">
                            <label class="col-lg-6 control-label">First name:</label>
                            <div class="col-lg-12">
                                <input class="form-control" type="text" v-model = "input.firstname" placeholder = "Edit your Firstname">
                            </div>
                        </div>
                        <div class="form-group">
                            <label class="col-lg-6 control-label">Last name:</label>
                            <div class="col-lg-12">
                                <input class="form-control" type="text" v-model = "input.lastname" placeholder = "Edit your Lastname">
                            </div>
                        </div>
                        <div class="form-group">
                            <label class="col-lg-6 control-label">Email Address:</label>
                            <div class="col-lg-12">
                                <input class="form-control" type="text" v-model = "input.email" placeholder = "Edit your Email Address">
                            </div>
                        </div>
                        <div class="form-group">
                            <label class="col-md-6 control-label">Username:</label>
                            <div class="col-md-12">
                                <input class="form-control" type="text" v-model = "input.username" placeholder = "Edit your username">
                            </div>
                        </div>
                        <div class="form-group">
                            <label class="col-md-6 control-label">Password:</label>
                            <div class="col-md-12">
                                <input class="form-control" type="password" v-model = "input.password" placeholder = "New Password">
                            </div>
                        </div>
                        <div class="form-group">
                            <label class="col-md-6 control-label">Confirm password:</label>
                            <div class="col-md-12">
                                <input class="form-control" type="password" v-model = "input.cpassword" placeholder = "Confirm New Password">
                            </div>
                        </div>
                        <div class="form-group">
                            <label class="col-md-6 control-label"></label>
                            <div class="col-md-12">
                                <button type="button" class="btn btn-outline-success register-btn" id="btnRegister" v-on:click = "submit">Save Changes</button>
                                <span></span>
                                <input type="reset" class="btn btn-default" value="Cancel">
                            </div>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.card {
  margin-top: 30px;
  width: 80%;
  margin-left: 100px;
  background-color: gray;
}
.avatar {
  vertical-align: middle;
  width: 50px;
  height: 50px;
  border-radius: 50%;
}
.jumbotron{
    padding:20px;
    text-align: center;
}
#image {
  width: 250px;
  height: 220px;
}
</style>
<script>
// import ROUTER from "router";
import AUTH from "services/auth";
export default {
  data() {
    return {
      auth: AUTH,
      input: {
        firstname: "",
        lastname: "",
        email: "",
        username: "",
        password: "",
        cpassword: ""
      }
    };
  },
  methods: {
    submit: function(e) {
      e.preventDefault();
      sessionStorage.setItem("Firstname", this.input.firstname),
        sessionStorage.setItem("Lastname", this.input.lastname),
        sessionStorage.setItem("Email", this.input.email),
        sessionStorage.setItem("Username", this.input.username),
        sessionStorage.setItem("Password", this.input.password),
        AUTH.edit(this.input.email, this.input.password);
    }
  }
};
</script>