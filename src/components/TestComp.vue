<script>
export default {
  data() {
    return {
		isAuth: true,
	}
  },
  methods: {
    toggle1: function() {
      this.isAuth= !this.isAuth; 
    },

  },
};
// нет, ну тебя совесть не мучает ?)
</script>

<template>
  <div>
	<p v-if="isAuth">Вы действительно администратор</p>
	<p v-else>Nonono, mr. fish, попробуйте зайти с ролью Администратор</p>
	<button @click="toggle1">Выйти/Зайти</button>
  </div>
</template>	