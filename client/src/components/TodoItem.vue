<template>
  <div>
    <li>
      <span :class="{done: todo.completed}">
        <input type="checkbox" v-on:change="todo.completed=!todo.completed">
        <strong>{{todo.id}}.</strong>
        {{todo.title}}
      </span>
      <button class="bm">&times;</button>
    </li>
  </div>
</template>

<script>
export default {
  props: {
    todo: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
li{
  border: 1px solid #ccc;
  display: flex;
  justify-content: space-between;
  padding: .5rem 2rem;
  margin-bottom: 1rem;
}

.bm{
  background: rgb(255, 2, 2);
  color: #fff;
  border-radius: 50%;
  font-weight: bold;
}
input{
  margin-right: 1rem;
}

.done{
  text-decoration: line-through;
}
</style>