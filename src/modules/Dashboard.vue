<template>
  <div>
    <div class="input-group">
      <div class="input-group-prepend">
        <label class="input-group-text" for="inputGroupSelect01">From</label>
      </div>
      <input class="form-control" type="text" v-model="from" />
      <div class="input-group-append">
        <button class="btn btn-primary" v-on:click="getPeople">Search</button>
      </div>
    </div>
    <div>
  <b-dropdown id="dropdown" text="Passenger" class="m-md-2">
    <b-dropdown-item>Adult</b-dropdown-item>
    <b-dropdown-item>Senior Citizen</b-dropdown-item>
    <b-dropdown-item>Student</b-dropdown-item>
  </b-dropdown>
</div>
  </div>
</template>

<style scoped>
#card {
  margin-top: 30px;
}
#image {
  width: 10%;
  height: 90%;
}
h2 {
  font: bold 50px Times New Roman;
  color: magenta;
}
h3 {
  font: italic bold 40px Georgia, serif;
  color: yellowgreen;
}
#input {
  margin-left: 30%;
}
</style>

<script>
export default {
  name: "card",
  data() {
    return {
      username: sessionStorage.getItem("Username")
    };
  }
};
</script>

