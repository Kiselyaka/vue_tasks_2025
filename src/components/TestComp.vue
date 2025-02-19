<script>
    export default {
	data() {
	  return {
		isValid: true,    
		isDisabled: false, 
	  };
	},
  };
  </script>

<template>
	<div>
		Задание 1:
		<p :style="{color: 'green', 'background-color': 'yellow'}">
		text
	</p>
	</div>
	<div><br />
		Задание 2:
		<p :style="{'font-weight': 'bold', 'font-style': 'italic'}">
		text
	</p>
	</div>
  </template>

