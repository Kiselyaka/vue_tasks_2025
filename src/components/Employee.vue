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
	<li>{{ this.arg[0] }}</li>
	<li>{{ this.arg[1] }}</li>
    <li>{{ this.arg[2] }}</li>
    </ul>
</template>