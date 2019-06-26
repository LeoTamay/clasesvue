<template>
  <div>
    <Navbar v-on:search-movie-title="searchMovie"></Navbar>
    <Content v-bind:movie-title="movieTitleToSearch"></Content>
  </div>
</template>


<script>
import HelloWorld from "./components/HelloWorld";
import Navbar from "./components/Navbar.vue";
import Content from "./components/Content.vue";

export default {
  name: "app",
  components: {
    Navbar,
    Content
  },
  data() {
    return {
      titulo: "my movies app",
      movieTitleToSearch: ""
    };
  },
  methods: {
    searchMovie: function(title) {
      this.movieTitleToSearch = title;
    }
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
}
</style>
