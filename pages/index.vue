<template>
  <div>
    <article class="pa3 pa5-ns">
      <h1 class="f4 bold center mw6">Todos</h1>
      <ul class="list pl0 ml0 center mw6 ba b--light-silver br2">
        <li v-for="todo of todos" class="ph3 pv3 bb b--light-silver">
          {{todo.task}}
        </li>
      </ul>
    </article>
    <!-- {{counter}}
          <button @click="increment">+</button>
          <button @click="decrement">-</button> -->
  </div>
</template>
<script>
import { mapState, mapMutations } from 'vuex'
// import { axios } from 'axios'

export default {
  computed: {
    ...mapState({
      // counter: (state) => state.counter
      todos: (state) => state.todos
    })
  },
  methods: {
    ...mapMutations([
      'increment',
      'decrement'])
  }
}
</script>