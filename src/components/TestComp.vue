
  <script>
  export default {
	data() {
	  return {
		arr: ['a', 'b', 'c'],
	  };
	},
	methods: {
	  add() {
		this.arr.push('xxx');
	  },
	  sortArray() {
      this.arr.sort();
    	},
		removeSecondLast() {
      if (this.arr.length > 1) {
        this.arr.splice(this.arr.length - 2, 1);
      }
      },	
	  removeFirst() {
      this.arr.shift();
    },
	  removeLast() {
      this.arr.pop();
      },
	  reverseArray() {
      this.arr.reverse();
      },
	},
  };
  </script>

<template>
	<div>
		Задание 1:
	  <ul>
		<li v-for="(elem, index) in arr" :key="index">{{ elem }}</li>
	  </ul>
	  <button @click="add">Add</button>
	</div>
	<div>
		Задание 2:
    <ul>
      <li v-for="(elem, index) in arr" :key="index">{{ elem }}</li>
    </ul>
    <button @click="removeFirst">Remove First</button>
  </div>
  <div>
	Задание 3:
    <ul>
      <li v-for="(elem, index) in arr" :key="index">{{ elem }}</li>
    </ul>
    <button @click="removeLast">Remove Last</button>
  </div>
  <div>
	Задание 4:
    <ul>
      <li v-for="(elem, index) in arr" :key="index">{{ elem }}</li>
    </ul>
    <button @click="removeSecondLast">Remove Second Last</button>
  </div>
  <div>
	Задание 5:
    <ul>
      <li v-for="(elem, index) in arr" :key="index">{{ elem }}</li>
    </ul>
    <button @click="sortArray">Sort</button>
  </div>
  <div>
	Задание 6:
    <ul>
      <li v-for="(elem, index) in arr" :key="index">{{ elem }}</li>
    </ul>
    <button @click="reverseArray">Reverse</button>
  </div>
  </template>