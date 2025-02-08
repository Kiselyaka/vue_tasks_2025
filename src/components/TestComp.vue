<script>
export default {
  data() {
    return {
      day: this.getDay(),
    };
  },
  methods: {
    getDay() {
      const days = ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'];
      const currentDate = new Date();
      return days[currentDate.getDay()];
    }
  },
};

</script>

<template>
	<div>
	  <p v-if="day === 'Monday'">Понедельник</p>
	  <p v-if="day === 'Tuesday'">Вторник</p>
	  <p v-if="day === 'Wednesday'">Среда</p>
	  <p v-if="day === 'Thursday'">Четверг</p>
	  <p v-if="day === 'Friday'">Пятница</p>
	  <p v-if="day === 'Saturday'">Суббота</p>
	  <p v-if="day === 'Sunday'">Воскресенье</p>
	</div>
  </template>