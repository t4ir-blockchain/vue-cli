<template>
  <div>
    <span v-for="image in dogImages" :key="image.id">
      <img width="200" height="200" :src="image.url" alt="">
    </span>
  </div>
</template>

<script>
export default {
  name: 'DogImage',
  props: {
    dogImages: Array
  }
}
</script>

<style>

</style>