<script>
  export default {
	data() {
	return {
		isClick: false,
	}
},

methods:{
	click: function(){
		if (!this.isClick) 
		{
        this.isClick = true;
        this.doThis();
        }
	},
	doThis() {
      console.log('Ссылка была нажата, но перехода не произошло.');
    },
}
}

</script>

<template>
	<div>Задача 1: <a href="https://www.google.com/" @click.prevent="bimbim">Попробуй перейти по ссылке</a></div>
	<div>Задача 2: <a href="https://www.google.com/" @click.prevent="click">Попробуй перейти по ссылке</a></div>
</template>