<template>
  <div>
    <span v-for="image in catImages" :key="image.id">
      <img width="200" height="200" :src="image.url" alt="">
    </span>
  </div>
</template>

<script>
export default {
  name: 'CatImage',
  props: {
    catImages: Array
  }
}
</script>

<style>

</style>