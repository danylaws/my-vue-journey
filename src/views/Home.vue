<template>
  <div class="home">
    
    <div>
      <button>Create Todo</button>
    </div>
    <div v-for="todo in todos" :key="todo.id">
      <div class="todo" :class="{done: todo.isDone}">
        <div class="title">{{ todo.title }}</div>
        <div class="schedulefor">Scheduled for: {{ todo.scheduledFor }}</div>
        <div class="actions">
          <span class="edit">Edit</span>
          <span class="delete">delete</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
// @ is an alias to /src


export default {
  name: 'Home',
  components: {},
  setup(){
    
    let todos = ref([ 
      {"id": 1,"title": "Learn Vue","scheduledFor": "07/28/2023","isDone": false},
      {"id": 2, "title": "Wash dishes","scheduledFor": "07/25/2023","isDone": true}
    ])

    return {todos}
  }
}
</script>

<style>

.todo {
  display:flex; 
  align-items: center;
  justify-content: space-between;
  border-radius: 10px;
  padding: 8px 12px;
  margin : 10px 0;
  background-color:rgb(190, 190, 190);
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}
.done {
  color: green;
  background-color:rgb(198, 240, 198)
}


/* CSS for the action buttons */
.todo .actions {
  display: flex;
  gap: 10px;
}

/* Styling for the edit and delete buttons */
.edit, .delete {
  padding: 8px 12px;
  border: none;
  border-radius: 5px;
  color: #fff;
  cursor: pointer;
}

/* Edit button styling */
.edit {
  background-color: #4caf50;
}

/* Delete button styling */
.delete {
  background-color: #f44336;
}

</style>
