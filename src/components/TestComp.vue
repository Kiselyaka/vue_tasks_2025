<script>
export default {
  data() {
    return {
		hide_swap: true,
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
	<div v-if="hide_swap">
		<p>+++</p>
		<p>+++</p>
		<p>+++</p>
	</div>
	<button @click="click">Показать / Сккрыть</button>	
	</div>
  </template>