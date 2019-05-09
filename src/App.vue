<template>
  <div id="app">
    <MovieMenu></MovieMenu>
    <MovieHome></MovieHome>

    <router-view />
  </div>
</template>

<script>
import MovieMenu from "./components/home/MovieMenu";
import MovieHome from "./components/home/MovieHome";
export default {
  name: "App",
  components: {
    MovieMenu,
    MovieHome
  }
};
</script>

<style></style>
