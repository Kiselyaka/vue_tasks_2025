<script>
	export default {
        props: ['arg'],
		data() {
			return {
				
			}
		}
	}
</script>

<template>
    <ul>
	<li>{{ arg[0] }}</li>
	<li>{{ arg[1] }}</li>
    <li>{{ arg[2] }}</li>
    </ul>
</template>