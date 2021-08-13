<template>
  <div class="app">
    <Navbar />
    <router-view></router-view>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar";
export default {
  components: {
    Navbar,
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  max-width: 960px;
  margin: 0 auto;
}
</style>
