<script>
import First from '@/components/First.vue'
import Second from '@/components/Second.vue'


export default {
  name: 'App',
  components: { First, Second },
  data() {
    return {
      answer: false
    }
  },
  methods:{
    onChange(answer) {
      this.answer = answer;
    }
  }
}

</script>

<template>
  <div class="wrapper">
    <h1>Привет. Тут есть пару фото, в тестовом задании сказали выложить и сделать приложение из этого. Чтобы посмотреть, отгадай загадку:</h1>
    <h3>Не лёд, а тает, не лодка, а уплывает.</h3>
    <ul @click="onChange(true)" class="answer">
      <li>Что за ерунда? Не хочу, показывай фото!</li>
      <li>Зарплата.</li>
    </ul>
    <div v-if="answer">
      <First />
      <Second />
    </div>
    <h2>Почему программирование?</h2>
    <p>С детства любил и люблю задачки на сообразительность, достаточно неплохо играю в шахматы (там нужно решать шахматные задачи, чтобы научиться играть лучше), просто однажды захотел научиться решать задачи на языке программирования JavaScript, а не на шахматной доске. Мне понравилось.</p>
  </div>
  <button @click="onChange(false)">Скрыть фото</button>
  <h2>Ссылка на репозиторий с исходным кодом
    <a href="https://v3.ru.vuejs.org/">тут</a>
  </h2>
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
