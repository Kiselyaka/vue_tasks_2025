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
	<p :class="{ valid: isValid, disabled: isDisabled }">
	  text
	</p>
  </template>

<style>
  .valid {
	color: green;
  }
  
  .disabled {
	color: gray; 
	text-decoration: line-through; 
  }
</style>