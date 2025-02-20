<script>
	export default {
	emits: ['my-event'],
	methods: {
    emitEvent() {
      this.$emit('my-event', 'bim-bim', 'bam-bam');
    }
	// код не копируй, хорошо -_-
  },
}
</script>

<template>
	<div>
		<button @click="emitEvent">
      Кликни меня
    </button>
  </div>
	
  </template>