<template>
  <div>
    <img :src="dataList.icons.x32"><br>
    <div
      v-for="(index, key) in dataList"
      :key="index"
    >
      {{ key }} 
    </div>

    <br>
    <button @click="back()">
      Homeページへ
    </button>
  </div>
</template>

<script>
export default {
  name: 'TestApi',
  data() {
    return {
      dataList: {},
    }
  },
  async mounted() {
    this.dataList = await this.$store.dispatch('test/callDiscoveryApi');
  },
  methods: {
    back() {
      this.$router.push({ path: '/home' });
    },
  }
}
</script>

<style lang="scss" scoped>
</style>
