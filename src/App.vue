<script>
import Employee from './components/Employee.vue';
import TestComp from './components/TestComp.vue';
	
export default {
	data() {
		return {		
	}
		},
		methods: {
    handleMyEvent(param1, param2) {
      console.log('Получены данные:', param1, param2);
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
<Employee  @my-event="handleMyEvent" /> 
</template>


