<script>
	export default {
		emits: ['show1', 'show2'],
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
	},
	methods: {
	handle1() {
		this.$emit('show1');
	},
	handle2() {
		this.$emit('show2');
	}
}
}
</script>

<template>
	<div>
		<button @click="handle1">btn1</button>
		<button @click="handle2">btn2</button>
	</div>
  </template>