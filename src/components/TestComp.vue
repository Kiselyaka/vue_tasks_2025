<script>
export default {
  data() {
    return {
      num: 0,
      res: 0,
	  num1: 0,
      num2: 0,
      sum: 0,
	  text1: '',
      text2: '',
	  fullName: '',
      lastName: '',
      firstName: '',
      middleName: '',
    };
  },
  methods: {
    calc() {
      this.res = Math.sqrt(this.num);
    },
	calculateSum() {
      this.sum = this.num1 + this.num2;
    },
	swapText() {
      const temp = this.text1;
      this.text1 = this.text2;
      this.text2 = temp;
    },
	splitName() {
      const names = this.fullName.split(' ');
      this.lastName = names[0] || '';
      this.firstName = names[1] || '';
      this.middleName = names[2] || '';
    },
  },
};
</script>

<template>
	<div>
		Задача 1:
	  <p>{{ res }}</p>
	  <input v-model.number="num" type="number" placeholder="Введите число">
	  <button @click="calc">work</button>
	</div>
	<div>
		Задача 2:
    <p>{{ sum }}</p>
    <input v-model.number="num1" type="number" placeholder="Введите первое число">
    <input v-model.number="num2" type="number" placeholder="Введите второе число">
    <button @click="calculateSum">Сложить</button>
  </div>
  <div>
		Задача 3:
    <input v-model="text1" placeholder="Введите текст 1">
    <input v-model="text2" placeholder="Введите текст 2">
    <button @click="swapText">Обменять</button>
    <p>Текст 1: {{ text1 }}</p>
    <p>Текст 2: {{ text2 }}</p>
  </div>
  <div>
		Задача 4:
    <input v-model="fullName" placeholder="Введите ФИО">
    <button @click="splitName">Разделить</button>
    <p>Фамилия: {{ lastName }}</p>
    <p>Имя: {{ firstName }}</p>
    <p>Отчество: {{ middleName }}</p>
  </div>
  </template>