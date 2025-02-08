<script>
  export default {
	data() {
	return {
		text1: 'xxx',
		text2: 'ggg',
	}
    },
	methods: {
	change1: function() {
		this.text1 = 'yyy';
	},
	change2: function() {
		this.text2 = 'aaa';
	}
    },
};
</script>

<template>
	<div>Задание 1-2: {{ text1 }} <br />
	<button @click="change1">text1</button></div>
	<div style='padding-left: 10px;'>	
	Задание 3: {{ text2 }} <br />
	<button @click="change2">text2</button></div>
</template>