<script>
  export default {
	data() {
	  return {
		notes: [],
		currentNote: { title: '', content: '', id: null },
		searchTerm: '',
		filteredNotes: [],
	  };
	},
	methods: {
	  saveNote() {
		if (this.currentNote.id === null) {
		  const newNote = { ...this.currentNote, id: Date.now() };
		  this.notes.push(newNote);
		} else {
		  const index = this.notes.findIndex(note => note.id === this.currentNote.id);
		  this.notes[index] = { ...this.currentNote };
		}
		this.resetCurrentNote();
		this.filterNotes();
	  },
	  selectNote(note) {
		this.currentNote = { ...note };
	  },
	  deleteNote(index) {
		this.notes.splice(index, 1);
		this.resetCurrentNote();
		this.filterNotes(); 
	  },
	  filterNotes() {
		this.filteredNotes = this.notes.filter(note =>
		  note.title.toLowerCase().includes(this.searchTerm.toLowerCase())
		);
		if (this.filteredNotes.length === 0) {
		  this.resetCurrentNote();
		}
	  },
	  resetCurrentNote() {
		this.currentNote = { title: '', content: '', id: null };
		this.searchTerm = '';
		this.filteredNotes = this.notes;
	  }
	},
	mounted() {
	  this.filteredNotes = this.notes;
	}
  };
  </script>

<template>
	<div id="app">
	  <h1>Блокнот</h1>
	  <div class="wrapper">
		<div class="menu">
		  <input
			type="text"
			v-model="searchTerm"
			placeholder="Поиск записей..."
			@input="filterNotes"
		  />
		  <ul>
			<li v-for="(note, index) in filteredNotes" :key="note.id">
			  <span @click="selectNote(note)">{{ note.title }}</span>
			  <button @click="deleteNote(index)">Удалить</button>
			</li>
		  </ul>
		</div>
		<div class="editor">
		  <input v-model="currentNote.title" placeholder="Заголовок записи" />
		  <textarea
			v-model="currentNote.content"
			placeholder="Ваш текст..."
		  ></textarea>
		  <div class="save_or_add">
		  <button @click="saveNote">{{ currentNote.id ? 'Сохранить' : 'Добавить' }}</button>
		  </div>
		</div>
	  </div>
	</div>
  </template>

<style>
.wrapper {
  display: flex;
}
.menu {
  flex: 1;
  margin-left: 10px;
  margin-right: 20px;
  background-color: greenyellow;
  border-radius: 10px;
}
.menu input{
	border-radius: 5px;
}
.editor {
  flex: 2;
}
.editor input{
	padding-bottom: 5px;
	margin-bottom: 10px;
	border-radius: 5px;
	font-size: 15px;
}
.editor textarea{
	border-radius: 5px;
	width: 1000px;
}
textarea {
  width: 100%;
  height: 200px;
}
.menu ul li span {
  margin-left: 10px;
}
h1 {
  text-align: center;
  font-size: 40px;
  padding-bottom: 20px;
}
.menu input {
  margin-left: 120px;
  margin-top: 10px;
  display: flex;
  width: 300px;
  height: 30px;
}
.menu li {
  margin-top: 10px;
  font-size: 15px;
  background-color: beige;
  width: 490px;
  border-radius: 5px;
}
li button {
  margin-left: 10px; 
  border-radius: 5px;
  background-color: azure;
}
.save_or_add button{
	width: 100px;
	height: 25px;
	border-radius: 5px;
	background-color: antiquewhite;
}
body {
  background-color: gainsboro;
}
</style>