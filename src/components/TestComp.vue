<script>
  export default {
	data() {
	return {
		cost: 100,
		amount: 5,
	}
},
computed: {
	price: function() {
		return this.cost * this.amount;
	}
},
methods:{
	change: function(){
		this.cost = 120;
	}
}
};
</script>

<template>
	<p>Задание 1: Стоимость {{ amount }}-ти морковок с ценой в размере {{ cost }} составляет: {{ price }}</p>
	<div>Задание 2: <button @click="change">смена цены</button></div>
</template>