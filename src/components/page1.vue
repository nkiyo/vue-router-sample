<template>
  <div>
    <p>
      ここはページ１です。
    </p>
    <router-link to="/page2">Go to page2</router-link>
  </div>
</template>

<script>
export default {
  mounted() {
    console.log(`${this.$route.query.test}`);
  },
};
</script>

<style>
</style>
