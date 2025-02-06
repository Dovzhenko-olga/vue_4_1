<template>
<comparison-comp/>
<last-rewieved-list/>
</template>

<script>
import ComparisonComp from "./components/ComparisonComp.vue";
import LastRewievedList from "./components/LastRewievedList.vue";

export default {
  name: 'App',
  components: {
    ComparisonComp,
    LastRewievedList,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
