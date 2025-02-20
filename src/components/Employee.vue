<script>
	export default {
	props: {
		firstName: String, 
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
    <ul>
	<li>{{ arg1 }}</li>
	<li>{{ arg2 }}</li>
    <li>{{ arg3 }}</li>
    </ul>
</template>