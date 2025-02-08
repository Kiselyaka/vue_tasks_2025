<script>
export default {
  data() {
    return {
		arr: ['x', 'y', 'z'],
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
		<li v-for="(elem, key) in arr">
		 {{ key }}
	    </li>
	</div>
  </template>