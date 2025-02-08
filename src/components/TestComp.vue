<script>
export default {
  data() {
    return {
		items: [1, 2, 3, 4, 5],
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
		Задание 1:
		<div v-for="elem in items">{{ elem }}</div>
		Задание 2:
		<div v-for="elem in items">{{ elem*elem }}</div>
		Задание 3:
		<ul><li v-for="elem in items">{{ elem}}</li></ul>
	</div>
  </template>