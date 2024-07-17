<template>
<div>
  <h1>영화정보</h1>
  <div v-for="movie in data" :key="movie">
    <h3 class="bg-yellow" :style="textRed">{{ movie.title }}</h3>
    <p>개봉: {{ movie.year }}</p>
    <p>장르: {{ movie.category }}</p>
  </div>
  <div>
    <p v-for="(item, i) in foods" :key="i">{{item}}</p>
  </div>
</div>
</template>

<script>
  export default {
    name: 'App',
    data() {
      return {
        foods: ["김밥", "순대", "만두", "떡국"],
        data: [
          {
            title: "노량",
            year: 2023,
            category: "액션, 드라마",
            textRed: "color: red"
          },
          {
            title: "아쿠아맨과 로스트 킹덤",
            year: 2023,
            category: "액션, 판타지, 어드벤쳐",
          },
          {
            title: "3일의 휴가",
            year: 2023,
            category: "액션, 판타지, 어드벤쳐",
          },
        ]
      }
    },
  }
</script>

<style>
  .bg-yellow{
    background: yellow;
    padding: 10px;
  }
</style>
