<template>
  <div class="header">
    <router-link to="/news">News</router-link>
    <span class="line">|</span>
    <router-link to="/ask">Ask</router-link>
    <span class="line">|</span>
    <router-link to="/jobs">Jobs</router-link>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.header {
  color: white;
  background-color: #42b883;
  display: flex;
  padding: 8px;
}

.header span.line {
  display: inline-block;
  margin: 0 3px;
  color: #02251a;
}

.header .router-link-exact-active {
  color: #35495e;
}

.header a {
  color: white;
}
</style>
