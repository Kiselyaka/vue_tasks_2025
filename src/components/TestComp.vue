<script>
  export default {
	data() {
	  return {
		daysOfWeek: ['Воскресенье', 'Понедельник', 'Вторник', 'Среда', 'Четверг', 'Пятница', 'Суббота'],
	  };
	},
	methods: {
	  getDayName(dayNumber) {
		if (dayNumber < 0 || dayNumber > 6) {
		  return 'Некорректный номер дня'; 
		}
		return this.daysOfWeek[dayNumber];
	  },
	  showCurrentDay() {
		const currentDayNumber = new Date().getDay();
		const currentDayName = this.getDayName(currentDayNumber); 
		alert(currentDayName);
	  },
	},
  }
  </script>

<template>
	<div>
	  <button @click="showCurrentDay">Показать текущий день недели</button>
	</div>
</template>