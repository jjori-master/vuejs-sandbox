<template>
  <div>
    <h1>Jobs</h1>
    <div v-for="(job, index) in jobs" :key="index">{{ job.title }}</div>
  </div>
</template>

<script>
import { fetchJobsList } from '../api/index.js';
export default {
  data() {
    return {
      jobs: [],
    };
  },
  created() {
    fetchJobsList()
      .then(res => {
        this.jobs = res.data;
      })
      .catch(err => {
        console.error(err);
      });
  },
};
</script>

<style></style>
