<template>
  
  <div class="body">
    <div class="main">
      <div class="container">
        <div class="heading">
          <h1>Todo App</h1>
        </div>
        <div class="add_todo_container">
          <h2 class="todo_label">Add Todo</h2>
          <div class="add_todo">
            <input type="text" class="titles" v-model="newTodoText" placeholder="Todo Title"/>
            <button @click="addTodo" class="add_button">Add New</button>
          </div>
        </div>
        <div class="todo_list_container">
          <h2 class="list_label">List of Todos</h2>
          <ul class="todo" v-if="todoList.length">
            <li class="todo_inner" v-for="(todo, index) in todoList" :key="index">
              <div>{{ todo.title }}</div>
              <div class="buttons">
                <div class="edit_button" @click="editTodo(index)" >&#9998; </div>
                <div class="remove_button" @click="removeTodo(index)" >&#x2716;</div>
              </div>
            </li>
          </ul>
          <div v-else>No todos yet</div>
        </div>
      </div>
    </div>
  </div>

</template>

<script setup>
  import { ref } from 'vue';
  const todoList =ref(JSON.parse(localStorage.getItem('todoData')) || []);
  const newTodoText =ref('');

  function addTodo() {
    newTodoText.value && todoList.value.push({ title: newTodoText.value });
    newTodoText.value = "";
    localStorage.setItem('todoData', JSON.stringify(todoList.value));
  }
  function removeTodo(index) {
    todoList.value.splice(index, 1);
    localStorage.setItem('todoData', JSON.stringify(todoList.value));
  }
  function editTodo(index) {
    todoList.value[index].title = prompt("Edit Todo", todoList.value[index].title);
    localStorage.setItem('todoData', JSON.stringify(todoList.value));
  }

</script>                                                                                                                                                                                                                                             
<<<<<<< HEAD

=======
>>>>>>> 9807fa7c7b2cd1d2cdf6dfc96f3fe2d2d247713c
<style>
.container {
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
  border-radius: 10px;
  width: 100%;
  padding: 20px;
  background-color: rgba(0, 189, 126, 0.5);
}
.heading {
  text-align: center;
  font-size: larger;
}
.titles{
  width: 70%;
  padding: 5px;
}
.add_button {
  background-color: #2c3e50;
  color: aliceblue;
  border: none;
  border-radius: 15px;
  padding: 8px;
  font-weight: bold;
}
.todo_list_container{
  margin-top: 20px;
}
.add_todo{
  display: flex;
  justify-content: space-between;
}
.todo_inner, .buttons {
  display: flex;
  justify-content: space-between;
}
.remove_button, .edit_button {
  font-size: 20px;
  cursor: pointer;
  margin-left: 20px;
}
</style>