<template>
  <Header />
  <div class="container my-3">
    <div class="input-group">
      <form @submit.prevent="addTodo()">
        <input
          v-model="todo.title"
          type="text"
          class="form-control"
          placeholder="Walk the dog..."
        />
        <button
          class="btn btn-outline-secondary"
          type="submit"
          id="button-addon2"
        >
          Add Todo
        </button>
      </form>
    </div>
  </div>
  <div class="container">
    <Card v-bind:todos="todos" />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Card from './components/Card.vue';

export default {
  name: 'App',
  components: {
    Header,
    Card,
  },

  data() {
    return {
      todo: {
        title: '',
      },
      todos: [
        {
          title: 'hello',
        },
      ],
    };
  },

  methods: {
    addTodo() {
      this.todos.push({
        title: this.todo.title,
      });
      this.todo.title = '';
    },
  },
};
</script>

<style>
</style>
