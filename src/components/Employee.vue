<script>
	export default {
	props: {
		name: String, 
		lastName: String,  
		age: Number,       
		position: String,  
		salary: Number,     
		isFullTime: Boolean 
	},
	data() {
		return {
			
		}
	}
}
</script>

<template>
	<div>
	  <h2>{{ name }}</h2>
	  <p>Salary: {{ salary }}</p>
	  <p>Age: {{ age }}</p>
	</div>
  </template>