<template>
  <div class="MovieHome">
    <RecommentPlay></RecommentPlay>
  </div>
</template>

<script>
import RecommentPlay from "./RecommentPlay";
export default {
  name: "",
  data() {
    return {};
  },
  components: {
    RecommentPlay
  }
};
</script>

<style scoped>
.MovieHome {
  display: flex;
  margin: auto 10%;
}
</style>
