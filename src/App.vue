<template>
  <div id="app">
    <h1>
      Find the best <br />
      Coffee for you
    </h1>
    <Search />
    <CoffeeContent />
  </div>
</template>

<script>
import Search from "./components/Search";
import CoffeeContent from "./components/CoffeeContent";

export default {
  name: "App",
  components: {
    Search,
    CoffeeContent,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Nunito:wght@200;300;400;600;700&display=swap");
* {
  padding: 0;
  margin: 0;
  list-style: none;
  text-align: left;
}

html {
  background: #0c1015;
  margin: 30px;
}

#app {
  padding: 0;
  font-family: "Nunito";
  text-align: center;
  width: 360px;
  max-width: 100%;
  margin: auto;
  background: #0c1015;
}

h1 {
  padding-bottom: 30px;
  color: white;
  font-family: "Nunito";
  text-align: left;
  margin: auto;
}
</style>
