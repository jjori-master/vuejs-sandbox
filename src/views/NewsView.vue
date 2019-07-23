<template>
  <div>
    <h1>News</h1>
    <div :key="index" v-for="(user, index) in users">{{ user.title }}</div>
  </div>
</template>

<script>
import { fetchNewsList } from '../api/index.js';
export default {
  data() {
    return {
      users: [],
    };
  },
  created() {
    fetchNewsList()
      .then(res => {
        this.users = res.data;
      })
      .catch(err => {
        console.error(err);
      });
  },
};
</script>

<style></style>
