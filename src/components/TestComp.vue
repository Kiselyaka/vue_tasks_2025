<script>
export default {
  data() {
	const today = new Date();
    const currentYear = today.getFullYear();
    const currentMonthIndex = today.getMonth(); 
    const currentDate = today.getDate();

    const years = Array.from({ length: 101 }, (_, i) => currentYear - 50 + i);  
    return {
		selected: '',
		week: ['понедельник', 'вторник', 'среда', "четверг", "пятница", "суббота", "воскресенье"],
		selectedDay: currentDate.toString(),
      	selectedMonth: ['Январь', 'Февраль', 'Март', 'Апрель', 'Май', 'Июнь', 'Июль', 'Август', 'Сентябрь', 'Октябрь', 'Ноябрь', 'Декабрь'][currentMonthIndex],
      	selectedYear: currentYear,
      	days: Array.from({ length: 31 }, (_, i) => i + 1).map(String), 
      	months: ['Январь', 'Февраль', 'Март', 'Апрель', 'Май', 'Июнь', 'Июль', 'Август', 'Сентябрь', 'Октябрь', 'Ноябрь', 'Декабрь'],
      	years
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
	<div>
		Задача 1:
	<p>
	Выберите день недели: 
	<select v-model="selected">
		<option v-for="option in week">{{ option }}</option>
	</select> 
	<br />
	</p>
	<p>Выбранный день недели: {{ selected }}</p> </div>
	<div>
		Задача 2-3:
    <select v-model="selectedDay">
      <option v-for="day in days" :key="day">{{ day }}</option>
    </select>
    
    <select v-model="selectedMonth">
      <option v-for="month in months" :key="month">{{ month }}</option>
    </select>

    <select v-model="selectedYear">
      <option v-for="year in years" :key="year">{{ year }}</option>
    </select>

    <p>Выбранная дата: {{ selectedDay }} {{ selectedMonth }} {{ selectedYear }}</p>
  </div>
</template>