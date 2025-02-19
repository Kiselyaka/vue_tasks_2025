<script>
export default {
  data() {
    return {
		products: [
			{
				id: 1,
				name: 'product1',
			},
			{
				id: 2,
				name: 'product2',
			},
			{
				id: 3,
				name: 'product3',
			},
		]
    };
  },
};
</script>

<template>
  <ul>
	<li v-for="prod in products" :key="prod.id">
		{{ prod.name }}
	</li>
	</ul>
</template>