<template>
  <div id="app">
    <b-row id="header" align-h="center">
      <b-col sm="5"
        ><b-img
          src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/74/Kotlin_Icon.png/1024px-Kotlin_Icon.png"
          height="75px"
          width="75px"
          fluid
          alt="Kotlin"
        ></b-img
      ></b-col>
      <b-col sm="2"><h1>Kotlin to Swift</h1></b-col>
      <b-col sm="5"
        ><b-img
          src="http://assets.stickpng.com/images/58482ce4cef1014c0b5e4a4c.png"
          height="75px"
          width="75px"
          fluid
          alt="Swift"
        ></b-img
      ></b-col>
    </b-row>
    <Home />
  </div>
</template>

<script>
import Home from "./views/Home.vue";

export default {
  name: "App",
  components: {
    Home,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff;
  padding-top: 2em;
  background-color: #2c3e50;
  background-size: cover;
  height: 99vh;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.row {
  margin-bottom: 2em;
}
</style>
