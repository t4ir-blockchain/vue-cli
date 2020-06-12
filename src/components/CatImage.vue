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
  name: 'CatImage',
  data() {
    return {
      title: 'Dog Image Generator',
      source: '',
      images: []
    }
  },
  methods: {
    getCat() {
      axios.get('https://api.thecatapi.com/v1/images/search')
        .then(response => {
          console.log(response.data[0].url)
          this.images.push({
            id: Date.now(),
            url: response.data[0].url
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