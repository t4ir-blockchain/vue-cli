<template>
  <div>
    <button @click="dogClicked">멍뭉이 이미지 가져오기</button>
    <button @click="catClicked">냥이 이미지 가져오기</button>
  </div>
</template>

<script>
export default {
  name: 'Buttons',
  methods: {
    dogClicked() {
      this.$emit('dogButtonClicked')
    },
    catClicked() {
      this.$emit('catButtonClicked')
    }
  }
}
</script>

<style>

</style>