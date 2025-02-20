<script>
	export default {
	emits: ['show', 'show2'],
	methods: {
    sendName() {
      const name = 'Работник 1'; 
      this.$emit('show', name);
    },
	sendNameAndSalary() {
      const name = 'Работник 2'; 
      const salary = '50000'; 
      this.$emit('show2', name, salary);
    },
  },
}
</script>

<template>
	<div>
		Задача 1:
		<button @click="sendName">Отправить имя работника</button>
	</div>
		<div>
			Задача 2:
    <button @click="sendName">Отправить имя работника</button>
    <button @click="sendNameAndSalary">Отправить имя и зарплату работника</button>
  </div>
	
  </template>