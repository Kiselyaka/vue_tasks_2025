<script>
import Employee from './components/Employee.vue';
import TestComp from './components/TestComp.vue';
import UserForm from './components/UserForm.vue';
import Checklist from './components/Checklist.vue';

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
			add(name, surn) {
		let id = this.users.length + 1;
		this.users.push({
			id,
			name,
			surn
		});
	},
	change(id, name, surn) {
		this.users = this.users.map((user) => {
			if (user.id === id) {
				user.name = name;
				user.surn = surn;
			}
			return user;
		});
	}
  	},
		components: {
			TestComp,
      		Employee,
			UserForm,
			Checklist
		}
	}
// я же узнаю, что ты у меня взял
</script>

<template>	
	<Checklist></Checklist>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, sans-serif; 
  background-color: #f5f5dc; 
  color: #2c3e50;
  text-align: left;
  padding: 20px;
}

body{
	background-color: beige;
}
</style>


