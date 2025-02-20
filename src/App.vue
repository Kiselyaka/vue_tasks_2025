<script>
import Employee from './components/Employee.vue';
import TestComp from './components/TestComp.vue';
	
export default {
	data() {
		return {		
	}
		},
		methods: {
	func1() {
		alert('первая функция');
	},
	func2(){
		alert('вторая функция')
	}
},
		components: {
			TestComp,
      Employee
		}
	}
</script>

<template>
	<TestComp />
  <Employee @show1="func1" @show2="func2"/>
</template>


