<script>
import Employee from './components/Employee.vue';
import TestComp from './components/TestComp.vue';
	
export default {
	data() {
		return {
			users: [
			{
				id: 1,
				name: 'name1',
				surn: 'surn1'
			},
			{
				id: 2,
				name: 'name2',
				surn: 'surn2'
			},
			{
				id: 3,
				name: 'name3',
				surn: 'surn3'
			},
		],		
	}
		},
		methods: {
			remove(id) {
		this.users = this.users.filter((user) => {
			return user.id !== id;
		})
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
<Employee  v-for   ="user in users"
		:id     ="user.id"
		:name   ="user.name"
		:surn   ="user.surn"
		@remove ="remove"
		:key    ="user.id"
	/>
</template>


