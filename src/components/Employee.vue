<script>
	export default {
        props: ['arg1', 'arg2', 'arg3'],
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