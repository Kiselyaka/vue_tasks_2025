<script>
	export default {
	props: {
	id:     Number,
	name:   String,
	surn:   String,
  },
  emits: ['remove'],
	methods: {
    emitEvent() {
      this.$emit('my-event', 'bim-bim', 'bam-bam');
    }
	// код не копируй, хорошо -_-
  },
}
</script>

<template>
	{{ name }}
	{{ surn }}
	
	<button @click="$emit('remove', id)">
		remove
	</button>
</template>