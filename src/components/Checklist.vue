<script>
export default {
  data() {
    return {
      newTask: '',
      tasks: [],
      nextId: 1,
    };
  },
  methods: {
    addTask() {
      if (this.newTask.trim() !== '') {
        this.tasks.push({ id: this.nextId++, text: this.newTask, completed: false });
        this.newTask = '';
      }
    },
    toggleTask(task) {
      task.completed = !task.completed;
    },
    editTask(task) {
      const updatedText = prompt('Обновите дело:', task.text);
      if (updatedText !== null) {
        task.text = updatedText;
      }
    },
    removeTask(id) {
      this.tasks = this.tasks.filter(task => task.id !== id);
    },
  },
};

// я же узнаю, что ты у меня взял
</script>

<template>
  <div class="checklist">
    <h1>Чеклист</h1>
    <input v-model="newTask" @keyup.enter="addTask" placeholder="Введите дело, которое вы запланировали..." />
    <ol>
        <li v-for="task in tasks" :key="task.id">
        <div class="task-item">
        <span @click="toggleTask(task)" :class="{ done: task.completed }">{{ task.text }}</span>
            <div class="button-group">
                <button @click="editTask(task)">Редактировать</button>
                <button @click="removeTask(task.id)">Удалить</button>
            </div>
        </div>
        </li>
    </ol>
  </div>
</template>

<style>
h1 {
  text-align: center;
  font-size: 50px;
}
input {
  margin-top: 20px;
  width: calc(100% - 20px);
  padding: 20px;
  margin-bottom: 10px;
  border-radius: 4px;
  border: 1px solid #ccc;
  margin-left: auto;
  margin-right: auto;
  font-size: 15px;
}

ol {
  padding: 0;
  margin-bottom: 20px; 
  border-radius: 3px;
  background-color: aliceblue;
  width: 1590px;
}

li {
  font-size: 20px;  
  border-radius: 5px;
}
.task-item {
  display: flex;
  justify-content: space-between; 
  align-items: center;
  border-bottom: 1px solid #eee;
  padding: 10px 0;
  padding-left: 10px;
}

.button-group {
  display: flex;
  gap: 10px; 
  padding-right: 10px;
}

.done {
  text-decoration: line-through;
}
.body{
	background-color: beige;
}

button{
    border: 2px solid transparent;
    border-radius: 6px;
    font-size: 17px;
    background-color:darkgray;
}
</style>