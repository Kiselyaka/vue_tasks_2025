<script>
export default {
  data() {
	return {
		newItem: '',
		items: ['a', 'b', 'c', 'd', 'e']
	};
  },
  methods: {
	addItem: function() {
	this.items.push(this.newItem);
	},
	addItem_in_end: function() {
	this.items.unshift(this.newItem);
	}
  }
};
</script>

<template>
	<div>
		Задача 1:
	<input v-model="newItem">
	<button @click="addItem">add</button>
	<ul>
		<li v-for="(item, index) in items" :key="index">
			{{ item }}
		</li>
	</ul>
	</div>
	<div>
		Задача 2:
		В начало списка списка
		<button @click="addItem_in_end">add</button>
	</div>
</template>
  