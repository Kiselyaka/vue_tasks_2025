  <script>
  export default {
	data() {
	  return {
		checked: true,
	  }
  },
  };
  </script>

<template>
	<input type="checkbox" v-model="checked">
	<p v-if="checked">{{ checked ? 'yes' : 'no' }}</p>
</template>