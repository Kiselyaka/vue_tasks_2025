<script>
export default {
  data() {
    return {
		selected: '',
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
	Выберите город, в котором вы живете:
	<select v-model="selected">
		<option>Москва</option>
		<option>Симферополь</option>
		<option>Санкт-Петербург</option>
	</select>
	<br />
	<p>Вы выбрали: {{ selected }}</p>
</template>