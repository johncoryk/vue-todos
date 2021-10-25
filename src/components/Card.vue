<template>
  <div class="card text-white bg-primary mb-3" style="max-width: 20rem">
    <div class="card-header">Todo</div>
    <div class="card-body">
      <h4 class="card-title">{{ todoTitle }}Title</h4>
      <p class="card-text">
        {{ todoDescription }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    todoTitle: String,
    todoDescription: String,
  },
};
</script>
