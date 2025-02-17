<script>
export default {
  data() {
    return {
		hrefs: [
			{href: '1.html', text: 'text1'},
			{href: '2.html', text: 'text2'},
			{href: '3.html', text: 'text3'},
		],
		products: [
			{
				name: 'product1',
				price: 100,
				quantity: 5
			},
			{
				name: 'product2',
				price: 200,
				quantity: 4
			},
			{
				name: 'product3',
				price: 300,
				quantity: 3
			},
		]
    };
  },
};

</script>

<template>
	<div>
		<p v-for="num in 30">
		{{ num }}
		</p>
	</div>
  </template>