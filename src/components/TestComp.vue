  <script>
  export default {
	data() {
	  return {
		text: '',
		text2: '',
		words: [],
	  };
	},
	methods: {
		// не работает, переделать
    generateWordList() {
		this.words = this.text2.trim().split(/s+/);
    },
  },
  };
  </script>

<template>
	<div>
		Задание 1:
	  <textarea v-model="text" placeholder="Введите текст"></textarea>
	  <p>{{ text }}</p>
	</div>
	<div>
		Задание 2:
    <textarea v-model="text2" placeholder="Введите текст"></textarea>
    <button @click="generateWordList">Сгенерировать список слов</button>
    <ul>
      <li v-for="(word, index) in words" :key="index">{{ word }}</li>
    </ul>
  </div>
  </template>