<template>
  <div>
    <div class="jumbotron">
      <h1>Subjects</h1>
    </div>
    <center>
      <b-card text-align id="card" img-top tag="article" style="max-width: 30rem;" class="mb-2">
        <b-form-group label-size="lg" label-for="input-lg">
          <label id="Subject">Subject:</label>
          <b-form-input v-model="content.subject" id="input-lg" size="lg"></b-form-input>
          <label id="teacher">Teacher:</label>
          <br>
          <b-form-input v-model="content.teacher" id="input-lg" size="lg"></b-form-input>
          <br>
          <label id="time">Time:</label>
          <b-form-input v-model="content.time" id="input-lg" size="lg"></b-form-input>
          <label id="time">Day:</label>
          <b-form-input v-model="content.day" id="input-lg" size="lg"></b-form-input>
          <label id="venue">Venue:</label>
          <b-form-input v-model="content.venue" id="input-lg" size="lg"></b-form-input>
          <br>
          <b-button variant="primary" @click="click">Add Subject</b-button>
        </b-form-group>
      </b-card>
      <b-card text-align id="card1" img-top tag="article" style="max-width: 40rem;" class="mb-2">
        <table class="table">
          <thead>
            <tr>
              <th scope="col">SUBJECT</th>
              <th scope="col">TEACHER</th>
              <th scope="col">TIME</th>
              <th scope="col">DAY</th>
              <th scope="col">VENUE</th>
            </tr>
          </thead>
          <tbody></tbody>
        </table>
      </b-card>
    </center>
  </div>
</template>


<style>
#card {
  margin-top: 20px;
}
.jumbotron {
  padding: 20px;
  text-align: center;
}
</style>

<script>
export default {
  data() {
    return {
      content: {
          subject:'',
          teacher: '',
    
      }
    }
  },
  methods: {
        click: function() {
        console.log("pangit!!!");
        }
      }
};
</script>