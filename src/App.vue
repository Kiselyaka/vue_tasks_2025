<script>
	import Employee from './components/Employee.vue';
  import TestComp from './components/TestComp.vue';

	
	export default {
		data() {
			return {
				name: 'john',
		    salary: '50000',
        age: '28'
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
  <Employee :arg1="name" :arg2="salary" :arg3="age" />
</template>


