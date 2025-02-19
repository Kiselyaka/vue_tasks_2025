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
	  <p :class="{active: true, valid: false}">text</p>
	</div>
  </template>
  
<style>
  p.hidden {
	display: none;
  }
</style>
  