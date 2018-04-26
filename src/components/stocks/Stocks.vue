<template>
  <div>
    <h1>Stocks</h1>
    <app-stock v-for="(stock,i) in stocks" :stock="stock" :key="'stock-'+i"></app-stock>
  </div>
</template>

<script>
import Stock from "./Stock";
export default {
  components: {
    appStock: Stock
  },
  computed: {
    stocks() {
      return this.$store.getters.stocks;
    }
  },
  data() {
    return {};
  }
};
</script>
