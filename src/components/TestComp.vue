<script>
export default {
  data() {
    return {
		choice: '',
		choice2: ''
    }
  },
  computed: {
    result() {
      return this.arr.length > 0 ? this.arr.join(', ') : 'Нет выбранных языков';
    }
  }
};
</script>

<template>
	Задача 1:
	Выберите язык, который для вас является родным: <br />
	<div>
	русский - <input name="radio" type="radio" v-model="choice" value="русский">;
	украинский - <input name="radio" type="radio" v-model="choice" value="украинский">;
	крымскотатарский - <input name="radio" type="radio" v-model="choice" value="крымскотатарский">;
	</div>	
	<div>
		<p>Вы выбрали: {{ choice }} </p> <br />
	</div>
	<div>
		<br />
		Задача 2:
		Выберите ваш родной язык:
		английский: <p><input name="radio" type="radio" v-model="choice2" value="английский"></p>
		<p v-if="choice2 == 'английский'"> Oh, hello my dear friend</p>
		русский: <p><input name="radio" type="radio" v-model="choice2" value="русский"></p>
		<p v-if="choice2 == 'русский'"> Привет, мой дорогой друг</p>
		белорусский: <p><input name="radio" type="radio" v-model="choice2" value="белорусский"></p>
		<p v-if="choice2== 'белорусский'"> Прывітанне, мой дарагі сябар</p>
	</div>
</template>