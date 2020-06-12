<template>
  <div>
    <div v-for="image in images" :key="image.id">
      <img width="200" height="200" :src="image.url" alt="">
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'CatImage'
}
</script>

<style>

</style>