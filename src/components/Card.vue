<template>
  <div class="card text-white bg-primary mb-3" style="max-width: 20rem">
    <div class="card-header">Todo</div>
    <div v-for="todo in todos" :key="todo.title" class="card-body">
      <h4 class="card-title">{{ todo.title }}</h4>
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
    };
  },
  props: {
    todos: [],
  },
};
</script>
