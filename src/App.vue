<script>
	import Employee from './components/Employee.vue';
  import TestComp from './components/TestComp.vue';

	
	export default {
		data() {
			return {
				
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
  <Employee />
  <Employee :arg="[1, 2, 3]" />
</template>


