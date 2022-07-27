<template>
  <div id="app">
    <global-nav />
    <router-view />
  </div>
</template>
<script>
import GlobalNav from "./components/GlobalNav";
export default {
  components: {
    GlobalNav,
  },
};
</script>

<style lang="scss"></style>
