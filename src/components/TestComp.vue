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
	Задача 1:
	<template>
  <table>
    <tr v-for="product in products" :key="product.name">
      <td>{{ product.name }}</td>
      <td>{{ product.price }}</td>
      <td>{{ product.quantity }}</td>
    </tr>
  </table>
</template>
</div>
<div>
	Задача 2:
	<template>
  <ul>
    <li v-for="link in hrefs" :key="link.href">
      <a :href="link.href">{{ link.text }}</a>
    </li>
  </ul>
</template>
	</div>
  </template>