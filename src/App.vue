<script>
import Employee from './components/Employee.vue';
import TestComp from './components/TestComp.vue';
	
export default {
	data() {
		return {		
	}
		},
	methods: {
    handle(name) {
      console.log(name);
    },
    handleWithSalary(name, salary) {
      console.log(name, salary);
    },
},
		components: {
			TestComp,
      Employee
		}
	}
</script>

<template>
	<TestComp />
  <Employee  @show="handle" @show2="handleWithSalary" />
</template>


