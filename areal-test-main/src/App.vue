<template>
  <div id="app">
    <th>ID:</th>
    <th>Имя: </th>
    <th>Фамилия: </th>
    <th>Email: </th>
    <hr>
    <ListApi v-for="list in listparam" :key="list" :list="list"/>
  </div>
</template>

<script>
import ListApi from '@/components/ListApi'
export default {
  name: 'App',
  data(){
    return{
      listparam:[]
    }
  },
  mounted() {
    fetch('https://my.api.mockaroo.com/test_api.json?key=91233870')
        .then(response => response.json())
        .then(json => {this.listparam = json})
  },
  components: {
    ListApi
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
  margin-top: 60px;
}
th{
  text-align: center;
  font-size: 18px;
  padding: 15px;
}
</style>
