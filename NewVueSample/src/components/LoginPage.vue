<template>
  <div>
    <h3>ユーザー情報を入力してください</h3><br>
    ユーザーID：<input type="text"><br>
    パスワード：<input type="password"><br>
    <button @click="confirm()">
      確認
    </button>
  </div>
</template>

<script>
export default {
  name: 'LoginPage',
  mounted() {
  },
  methods: {
    confirm() {
      this.$router.push({ path: '/warehouse' });
    },
  }
}
</script>

<style lang="scss" scoped>
</style>
