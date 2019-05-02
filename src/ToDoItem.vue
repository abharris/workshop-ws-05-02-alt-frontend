<template>
  <div  class="ToDoItem">
    <p class="ToDoItem-Text">{{todo.text}}</p>
    <div class="ToDoItem-Delete" @click="deleteItem(todo)">-
    <input type="text" v-model="todo"  v-on:keyup.enter="createNewToDoItem"/>
    <div  class="ToDo-Add"  @click="createNewToDoItem()">+</div>    
	</div>
  </div>
</template>

<script>
  export  default  {
  name: "to-do-item",
    props: ['todo'],
    methods: {
  deleteItem(todo) {
    this.$emit('delete', todo)
  }
}
  }
</script>