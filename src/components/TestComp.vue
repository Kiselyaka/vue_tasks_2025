<script>
  export default {
	data() {
	  return {
		message: 'hello',
		number: 0,
	  };
	},
	computed: {
    upperCaseMessage() {
      return this.message.toUpperCase();
    },
	squaredNumber() {
      return this.number * this.number;
    },
  },
  };
  </script>

<template>
	<div>
		Задача 1:
	  <input v-model="message">
	  <p>{{ message }}</p>
	</div>
	<div>
		Задача 2:
    <input v-model="message">
    <p>{{ upperCaseMessage }}</p>
  </div>
  <div>
	Задача 3:
    <input type="number" v-model.number="number">
    <p>{{ squaredNumber }}</p>
  </div>
  </template>