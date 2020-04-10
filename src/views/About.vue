<template>
  <div class="about">
    <h1 class="about__title">This is an about page</h1>
    <div class="todos">
      <form class="todos__form" action="">
        <label for="inp">Добавить задачу</label>
        <input v-model="newTodoText" id="inp" class="todos__input" type="text">
        <button v-on:click.prevent="addTodo">Добавить</button>
        <p>Введенное сообщение: {{ newTodoText }}</p>
      </form>
      <ul>
        <li class="todo-item"
          v-for="(item, index) in todoList"
          :key="item.id">
          {{ item.text }}
            <button @click="deleteTodo(index)">delete</button>
          </li>
      </ul>
    </div>
  </div>
</template>

<script>
import anime from 'animejs/lib/anime.es.js'
export default {
  data: () => ({
    newTodoText: '',
    newTodoId: 1,
    todoList: [
      // { id: 1, text: 'Купить хлеб' },
      // { id: 2, text: 'Поработать' }
    ]
  }),
  methods: {
    addTodo () {
      this.todoList.push({
        id: this.newTodoId++,
        text: this.newTodoText
      })
      this.newTodoText = ''
    },
    deleteTodo (index) {
      this.todoList.splice(index, 1)
    }
  },
  mounted () {
    // eslint-disable-next-line no-unused-vars
    const tl = anime.timeline({
      easing: 'linear',
      duration: 1500
    }).add({
      targets: '.page-header',
      translateY: ['-100%', 0],
      opacity: [0, 1]
    }, 0).add({
      targets: '.about',
      translateX: [-100, 0],
      opacity: [0, 1]
    }, 0)
  },
  beforeRouteLeave (to, from, next) {
    // eslint-disable-next-line no-unused-vars
    const tl = anime.timeline({
      easing: 'linear',
      duration: 1500
    }).add({
      targets: '.page-header',
      translateY: [0, '-100%'],
      opacity: [1, 0]
    }, 0).add({
      targets: '.about',
      translateX: [0, -100],
      opacity: [1, 0]
    }, 0)
    tl.finished.then(next)
  }
}
</script>

<style lang="scss">
  .about {
    height: 500px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
  .about__title {
    margin-bottom: 50px;
  }
  .todo-item {
    animation: showTodo 0.6s forwards;
  }
  @keyframes showTodo {
    0% {
      transform: translateX(-20px);
      opacity: 0;
    }
    100% {
      transform: translateX(0);
      opacity: 1;
    }
  }
</style>
