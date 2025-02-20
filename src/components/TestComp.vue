<script>
export default {
  data() {
	return {
		newItem: '',
		items: ['a', 'b', 'c', 'd', 'e']
	};
  },
  methods: {
	removeItem: function(index) {
		this.items.splice(index, 1);
	}
  }
};
</script>

<template>
	<div>
		<ul>
		<li v-for="(item, index) in items" :key="index" @click="removeItem(index)">
			{{ item }}
		</li>
	</ul>
	</div>
</template>
  
  