

<template>
<div>
  <h3> DataSet </h3>
  <div>
    <button type="button" @click = "printName"> Print LocalData</button>

    <div v-for = "x in local_data">
    		<input type="text" v-model="x.name" placeholder="name">
    		<input type="text" v-model="x.email" placeholder="name">

    		<div>Local Data: {{x.name}} - {{x.email}}</div>
    </div>

  </div>
</div>
</template>

<script>
export default {
  name : 'Test',
  props: ["data"],
  data() {
    return {
      local_data: Object.assign({}, this.data)
    };
  },

  methods:{
    printName(){
      console.log('Local Data', this.local_data)
    }
  }
};
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
