<template>
  <div>
    <button @click="getDog">이미지 가져오기</button>
    <div v-for="image in images" :key="image.id">
      <img width="200" height="200" :src="image.url" alt="">
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'DogImage',
  data() {
    return {
      title: 'Dog Image Generator',
      source: '',
      images: []
    }
  },
  methods: {
    getDog() {
      axios.get('https://dog.ceo/api/breeds/image/random')
        .then(response => {
          console.log(response.data.message)
          this.images.push({
            id: Date.now(),
            url: response.data.message
          })
        })
      // 1. dog.ceo API에 요청을 보내어 JSON 응답 받아 
      // 2. image url를 가져와 
      // 3. <img src=""> 데이터 바인딩
      // (추가미션) -> 이미지가 계속 추가
    }
  }
}
</script>

<style>

</style>