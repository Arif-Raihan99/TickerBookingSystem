<template>
  <div class="container">
    <div class="row">
      <div class="card">
        <div class="card-title">User Register Form</div>
        <div class="card-body">
          <label for="name">Full Name</label><br>
          <input id="name" type="text" v-model="formData.name" placeholder="Inter your full name"><br><br>
          <label for="email">Email</label><br>
          <input id="email" type="email" v-model="formData.email" placeholder="Inter your email"><br><br>
          <label for="pass1">Password</label><br>
          <input id="pass1" type="password" v-model="formData.password1" placeholder="Inter password"><br><br>
          <label for="pass2">Confirm Password</label><br>
          <input id="pass2" type="password" v-model="formData.password2" placeholder="Retype password"><br><br>
          <button class="submit-btn">Register</button>
          <br>
        </div>
        <div class="card-footer">Have a account? <span>Login</span></div>
      </div>
    </div>
  </div>
  <div class="container">
    <hr>
    <div class="card">
      <div class="card-body">
        <div v-for="(value, key) in formData" :key="key">
          <strong>{{ key }}: </strong>{{ value }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data () {
    return {
      formData: {
        name: '',
        email: '',
        password1: '',
        password2: ''
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
}
input{
  padding: 5px 11px;
  width: 80%;
}
.card-body label{
  padding: 5px 0;
}
.container{
  margin: 0 60px;
  padding: 10px;
}
.row{
  display: flex;
  margin-bottom: 5px;
}
.card{
  width: 30%;
  margin: 10px auto;
  min-height: 100px;
  border: 1px solid gray;
  padding: 8px;
}
.card-title{
  width: 100%;
  background-color: #202e41;
  color: white;
  padding: 8px 0;
}
.card-body{
  padding: 10px 10px;
  background-color: aliceblue;
  text-align: left;
}
.card-footer{
  width: 100%;
  background-color: #1f3f41;
  color: white;
  padding: 5px 0;
}
.submit-btn{
  padding: 6px 8px;
  background-color: #2c4cf0;
  color: white;
  border-radius: 5px;
}
</style>
