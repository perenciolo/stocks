<template>
  <div class="container">
    <app-Header></app-header>
    <div class="row">
      <div class="col-xs-12">
        <router-view></router-view>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";

export default {
  name: "app",
  components: {
    appHeader: Header
  },
  data() {
    return {};
  },
  created() {
    this.$store.dispatch("initStocks");
  }
};
</script>

<style lang="scss">
body {
  padding: 30px;
}
</style>
