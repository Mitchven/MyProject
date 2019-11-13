<template>
  <div class="card">
    <!-- <div class="summary text-danger" id = "errors" v-if="$v.form.$error">Form has errors</div> -->
    <form @submit.prevent="submit">
      <div class="flex justify-center my-6">
        <div class="px-4" :class="{ 'hasError': $v.form.name.$error }">
          <label class="mr-2 font-bold text-grey">Fullname</label>
          <input type="text" class="input" v-model="form.name" />
        </div>
        <div class="px-4" :class="{ 'hasError': $v.form.name.$error }">
          <label class="mr-2 font-bold text-grey">Username</label>
          <input type="text" class="input" v-model="form.uname" />
        </div>
        <div class="px-4" :class="{ 'hasError': $v.form.email.$error }">
          <label class="mr-2 font-bold text-grey">Email</label>
          <input type="email" class="input" v-model="form.email" />
        </div>
        <div class="px-4" :class="{ 'hasError': $v.form.email.$error }">
          <label class="mr-2 font-bold text-grey">Password</label>
          <input type="password" class="input" v-model="form.password" />
        </div>
      </div>

      <div class="text-center">
        <button type="submit" class="button" id = "btnRegister">Submit</button>
      </div>
    </form>
  </div>
</template>

<script>
import AUTH from "services/auth";
import { required, email, minLength } from "vuelidate/lib/validators";

export default {
  name: "Register",

  data() {
    return {
      form: {
        name: "",
        uname: "",
        email: "",
        password: ""
      }
    };
  },
  validations: {
    form: {
      name: { required, min: minLength(10) },
      email: { required, email },
      password: { required, min: minLength(8)}
    }
  },

  methods: {
    submit() {
      sessionStorage.setItem("Fullname", this.form.name),
        sessionStorage.setItem("Email", this.form.email),
        sessionStorage.setItem("Username", this.form.uname),
        sessionStorage.setItem("Password", this.form.password);

      this.$v.form.$touch();
      
      
      if (this.$v.form.$error) return alert("You need to fill in the field!");
      // to form submit after this
      alert("Form submitted");
      AUTH.register(this.form.email,this.form.password);
    }
  }
 
};
</script>

<style>
.card {
  background-color: gray;
  margin-top: 2%;
  margin-right: 30%;
  margin-left: 30%;
  padding: 0px;
  border-radius: 20px;
}

/* .h3 {
  margin-left: 500px;
  margin-top: 300px;
  font-size: 40px;
  font-family: Times new;
}
.nav {
  margin-block: auto;
}

.card-header {
  text-align: center;
  font-weight: bold;
  font-size: 30px;
  letter-spacing: 5px;
  border-radius: 50px;
  color: white;
} */

label {
  font-weight: bold;
}

input {
  border: 2px solid black;
}

#btnRegister {
  color: black;
  border: 2px solid black;
  margin-top: 5px;
  padding: 12px 30px;
}
</style>