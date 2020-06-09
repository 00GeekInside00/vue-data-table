<template>
  <div id="app">
    <vDataTable :url="url"/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import vDataTable from "./components/v-data-table";
export default {
  name: "App",
  components: {
    HelloWorld,
    vDataTable
  },
  data() {
    return {
      url: "https://quote-garden.herokuapp.com/api/v2/quotes?page=1&limit=10",
      gridData: [
        {
          name: "Chuck Norris",
          power: Infinity
        },
        {
          name: "Bruce Lee",
          power: 9000
        },
        {
          name: "Jackie Chan",
          power: 7000
        },
        {
          name: "Jet Li",
          power: 8000
        }
      ]
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
