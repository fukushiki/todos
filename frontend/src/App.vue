<template>
  <div>
    <section class="todoapp" v-cloak>
      <header class="header">
        <h1>todos</h1>
        <input class="new-todo" autofocus autocomplete="off" placeholder="What needs to be done?">
      </header>
            <section class="main" v-show="todos.length">
        <ul class="todo-list">
          <li class="todo" v-for="todo in todos" :key="todo.id" :class="{completed: todo.completed}">
            <div class="view">
              <input class="toggle" type="checkbox" v-model="todo.completed">
              <label>{{ todo.title }}</label>
            </div>
          </li>
        </ul>
      </section>
    </section>
  </div>
</template>

<script>
import "./assets/css/base.css";
import "./assets/css/app.css";
export default {
  name: "app",
  data(){
    return {
      todos: [
        {
          id: 0,
          title: "My test todo item",
          completed: false
        }
      ],
    }
  }
};
</script>