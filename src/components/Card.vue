<template>
  <div class="card text-white bg-primary mb-3" style="max-width: 20rem">
    <div class="card-header">Todo</div>
    <div
      v-for="(todo, i) in todosArray"
      :key="todo.title"
      class="card-body d-flex justify-content-between"
    >
      <h4 class="card-title">{{ todo.title }}</h4>
      <button @click="removeTodo(i)" type="button" class="btn btn-dark">
        Delete
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  data() {
    return {
      todo: {
        title: '',
        isDone: false,
      },
      todosArray: this.todos,
    };
  },
  props: {
    todos: Array,
  },
  methods: {
    removeTodo(index) {
      this.todosArray.splice(index, 1);
    },
  },
};
</script>
