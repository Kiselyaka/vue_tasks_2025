<script>
export default {
  data() {
	return {
	  inputText: '',
	  displayedText: ''
	};
  },
  methods: {
	updateText() {
	  this.displayedText = this.inputText;
	  this.inputText = ''; 
	},
	handleClick(event) {
      if (event.ctrlKey) {
        this.displayedText = 'Клавиша Ctrl была зажата';
      }
    },
	handleMouseDown(event) {
      if (event.button === 0) {
        this.displayedText = 'left';  
      } else if (event.button === 2) {
        this.displayedText = 'right'; 
      } else if (event.button === 1) {
        this.displayedText = 'middle'; 
      }
    }
  }
};
</script>

<template>
	<div>
		Задача 1:
	  <input v-model="inputText" @keyup.enter="updateText" placeholder="Введите текст"/>
	  <p>{{ displayedText }}</p>
	</div>
	<div>
		Задача 2:
    <a href="#" @click.prevent="handleClick">Нажмите здесь</a>
    <p>{{ displayedText }}</p>
  </div>
  <div>
		Задача 3:
    <a href="#" 
       @mousedown="handleMouseDown">Нажмите на меня</a>
    <p>{{ displayedText }}</p>
  </div>
  </template>
  