
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
	<p>
		1
	</p> <br />
	<p>
		2
	</p>
</template>

<style>
p {
	color: red;
}
</style>