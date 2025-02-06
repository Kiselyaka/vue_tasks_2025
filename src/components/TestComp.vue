<script>
  export default {
	methods: {
	  show(str) {
		alert(str); 
	  },
	  square(number) {
		return number * number;
	  },
	},
  };
</script>

<template>
	<div>
	  <button @click="show('Квадрат числа 2 равен ' + square(2))">Квадрат 2</button>
	  <button @click="show('Квадрат числа 3 равен ' + square(3))">Квадрат 3</button>
	</div>
  </template>