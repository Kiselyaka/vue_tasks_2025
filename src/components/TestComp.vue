<script>
  export default {
	data() {
	  return {
		currentDate: new Date().toLocaleDateString(),
	  };
	},
	methods: {
	  showDate() {
		alert(this.currentDate);
	  },
	},
  }
</script>

<template>
	<p>Текущая дата:</p>
	<button @mouseover="showDate">Показать дату</button>
</template>