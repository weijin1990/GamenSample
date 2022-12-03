<template>
  <div>
    <h3>ホームページ</h3>
    <br>
    <a
      href="javascript:void(0)"
      @click="link('/login')"
    >ログイン</a>
    <br>
    <a
      href="javascript:void(0)"
      @click="link('/testapi')"
    >TestApi</a>
  </div>
</template>

<script>
export default {
  name: 'TopPage',
  mounted() {
  },
  methods: {
    link(url) {
      this.$router.push({ path: url });
      // window.location.href = url;
    },
  }
}
</script>

<style lang="scss" scoped>
</style>
