<script>
export default {
  data() {
    return {
		obj: {user1: '100$',
		user2: '200$',
		user3: '300$',}	
    };
  },
  methods: {
        click: function(){
			this.hide_swap = !this.hide_swap;
		}
  },
};

</script>

<template>
	<div>
		Задача 1:
		<li v-for="(elem, key, index) in obj">
		 {{ elem }}
	    </li>
		Задача 2:
		<li v-for="(elem, key, index) in obj">
		 {{ key }} - {{ elem }} 
	    </li>
		Задача 3:
		<li v-for="(elem, key, index) in obj">
		 {{ key }} - {{ elem }} - {{ index }} 
	    </li>
		Задача 4:
		<li v-for="(elem, key, index) in obj">
		 {{ key }} - {{ elem }} - {{ index + 1 }} 
	    </li>
	</div>
  </template>