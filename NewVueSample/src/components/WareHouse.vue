<template>
  <div>
    <h3>在庫管理画面</h3><br>
    <div
      v-for="index in inputList"
      :key="index"
    >
      商品名<input type="text">&emsp;数量<input
        type="text"
        maxlength="3"
        style="width: 3rem"
      >&emsp;
      <button
        :disabled="inputList.length < 2"
        @click="remove()"
      >
        削除
      </button>&emsp;
      <button
        :disabled="inputList.length > 9"
        @click="add()"
      >
        商品追加
      </button>
    </div>

    <br>
    <button @click="confirm()">
      入庫確認
    </button>&emsp;
    <button @click="back()">
      Homeページへ
    </button>
  </div>
</template>

<script>
export default {
  name: 'WareHouse',
  data() {
    return {
      inputList: [''],
      dataList: {},
    }
  },
  async mounted() {
  },
  methods: {
    add() {
      this.inputList.push('');
    },
    remove() {
      this.inputList.pop();
    },
    confirm() {
      alert('上記入力内容を登録しますが、よろしいですか？※dummy');
    },
    back() {
      this.$router.push({ path: '/home' });
    },
  }
}
</script>

<style lang="scss" scoped>
</style>
