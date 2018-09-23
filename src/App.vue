
<template>
  <div id="app">
    <User :user="user" />
    <div>App's user: {{user}}</div>

    <Test :data = "data" />

     <div v-for = "x in data">
          App's Data : {{x.name}} - {{x.email}}
     </div>
  </div>
</template>

<script>
import User from "./components/User";
import data from './data_set/data.json';
import Test from './components/Test';

export default {
  name: "App",
  components: {
    User, Test
  },
  data() {
    return {
      user: {
        name: "John Doe"
      },
      data: data
    };
  }
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
