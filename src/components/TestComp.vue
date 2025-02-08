<script>
export default {
  data() {
    return {
      hidden: true, 
    };
  },
  methods: {
    click: function() {
      this.hidden = !this.hidden; 
      console.log('Текущее значение hidden:', this.hidden);
    },
  },
};
// не копируй, хорошо -_-
</script>

<template>
  <div>
    <p v-if="hidden">text, когда hidden = true</p>
    <button @click="click">Инвертировать условие</button>
  </div>
</template>