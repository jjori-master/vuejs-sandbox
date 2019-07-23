<template>
  <div>
    <h1>Ask</h1>
    <div v-for="(ask, index) in asks" :key="index">{{ ask.title }}</div>
  </div>
</template>

<script>
import { fetchAskList } from '../api/index.js';
export default {
  data() {
    return {
      asks: [],
    };
  },
  created() {
    fetchAskList()
      .then(res => {
        this.asks = res.data;
      })
      .catch(err => {
        console.error(err);
      });
  },
};
</script>

<style></style>
