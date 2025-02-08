<script>
export default {
  data() {
    return {
      hidden: true, 
	  z2: false,
	  hidden_z3: true,
    };
  },
  methods: {
    click: function() {
      this.hidden = !this.hidden; 
      console.log('Текущее значение hidden:', this.hidden);
    },
	click1: function(){
		this.z2 = true;
	},
	click2: function(){
		this.z2 = false;
	},
	click_z3: function() {
      this.hidden_z3 = !this.hidden_z3; 
    },
  },
};

</script>

<template>
  <div>
    <p v-if="hidden">text, когда hidden = true</p>
    Задание 1: <button @click="click">Инвертировать условие</button>
   <div>Задание 2: <p v-if="z2">Ого, абзац показался</p> 
	<button @click="click1">Показать</button>
	<button @click="click2">Скрыть</button></div>
	<div>Задание 3: <p v-if="hidden_z3">Да ну, снова абзац что-ли. А кто-то все еще копирует мой код</p>
      <button v-if="hidden_z3" @click="click_z3">Скрыть</button>
      <button v-else @click="click_z3">Показать</button>
    </div>
  </div>
</template>	