<script>
import FirstImg from '@/components/FirstImg.vue'
import SecondImg from '@/components/SecondImg.vue'


export default {
  name: 'App',
  components: { FirstImg, SecondImg },
  data() {
    return {
      answer: false
    }
  },
  methods: {
    onChange(answer) {
      this.answer = answer;
    }
  }
}

</script>

<template>
  <div class="wrapper">
    <h1>Привет. Тут есть пару фото, в тестовом задании сказали выложить и сделать приложение из этого. Чтобы посмотреть,
      отгадай загадку:</h1>
    <hr>
    <h2>Не лёд, а тает, не лодка, а уплывает.</h2>
    <ul @click="onChange(true)" class="answer">
      <li>Зарплата.</li>
      <li>Что за ерунда? Не хочу, показывай фото!</li>
    </ul>
    <div v-if="answer">
      <FirstImg />
      <SecondImg />
      <button @click="onChange(false)">Скрыть фото</button>
    </div>
    <hr>
    <h2>Почему программирование?</h2>
    <p>С детства любил и люблю задачки на сообразительность, достаточно неплохо играю в шахматы (там нужно решать
      шахматные задачи, чтобы научиться играть лучше), просто однажды захотел научиться решать задачи на языке
      программирования JavaScript, а не на шахматной доске. Мне понравилось.</p>
  </div>
  <hr>
  <h2>Ссылка на репозиторий с исходным кодом
    <a href="https://github.com/Grebnik89/testQuiz/tree/master">тут</a>
  </h2>
  <hr>
  <h2>А здесь скринкаст с интересной фишкой на CSS:</h2>
  <iframe width="560" height="315" src="https://www.youtube.com/embed/5z6BNnpoK_0?si=UxKgBwUOyzcufyuU"
    title="YouTube video player" frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    allowfullscreen></iframe>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.wrapper {
  background-color: #fcfcfc;
  margin: 0 10px;
}

.answer {
  list-style: none;
}

.answer li {
  width: auto;
  border: 1px solid #2c3e50;
  margin: 5px;
  cursor: pointer;
}

.answer li:hover {
  background-color: aquamarine;
}
</style>
