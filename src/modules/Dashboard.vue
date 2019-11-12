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

