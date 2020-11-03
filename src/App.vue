<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  created() {
    // failed...https://stackoverflow.com/a/35916241
    console.log(`${this.$route.query.test}`);
    console.log(`${JSON.stringify(this.$route.query)}`);

    // query string から値を取得する https://stackoverflow.com/a/48122942
    console.log(`${window.location.search.substring(1)}`);
    const params = new URLSearchParams(window.location.search.substring(1));
    console.log(`${params.get('test')}`);
    console.log(`${params.get('hoge')}`);
    console.log(`${params.get('hage')}`);
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
