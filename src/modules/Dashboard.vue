<template>
  <div>
    <div class="jumbotron">
      <h1>Dashboard</h1>
    </div>
    <div id="card">
      <b-card no-body class="overflow-hidden" style="max-width: 540px;">
        <center>
          <b-card-img id="image" :src="require('assets/user.png')" class="rounded-0"></b-card-img>
          <b-row no-gutters>
            <b-card-body>
              <h2>Hi {{username}}</h2>
              <h3>Welcome to EASAKAY</h3>
            </b-card-body>
          </b-row>
        </center>
      </b-card>
    </div>
  </div>
</template>

<style scoped>
#card {
  margin-top: 30px;
  margin-left: 400px;
}
.jumbotron{
    padding:20px;
    text-align: center;
    background-color:gray;
}
#image {
  width: 250px;
  height: 220px;
}
h2 {
  font:bold 50px Times New Roman;
  color: magenta;
}
h3 {
  font: italic bold 40px Georgia, serif;
  color: yellowgreen;
}
</style>

<script>
export default {
  name: "card",
  data() {
    return {
      username: sessionStorage.getItem("Username"),
    };
  },
};
</script>

