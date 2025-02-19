<script>
export default {
  data() {
	return {
	  obj: {
		hidden: true,
	  },
	};
  },
  methods: {
	show() {
	  this.obj.hidden = false; 
	},
	hide() {
	  this.obj.hidden = true; 
	},
	toggle() {
	  this.obj.hidden = !this.obj.hidden; 
	},
  },
};
</script>

<template>
	<div>
	  <p :class="{ hidden: obj.hidden }">text</p>
	  <div>
		<button @click="show">Show</button>
		<button @click="hide">Hide</button>
		<button @click="toggle">Toggle</button>
	  </div>
	</div>
  </template>
  
<style>
  p.hidden {
	display: none;
  }
</style>
  