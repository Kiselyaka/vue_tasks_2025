<script>
	export default {
		data() {
	return {
		arr2: [1, 2, 3],	
		arr1: ['x', 'y', 'z'],
}
}
}

</script>

<template>
	<div>{{arr2[0]+arr2[1]+arr2[2] }}</div>
	<p><br>{{ arr1[0] }} <br> 
	{{ arr1[1] }} <br>
	{{ arr1[2] }} </p>
</template>