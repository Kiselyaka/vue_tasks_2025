<script>
export default {
  data() {
    return {
      visible: true, 
    };
  },
  methods: {
    click: function() {
      this.visible = !this.visible; 
      console.log('Текущее значение visible:', this.visible);
    },
  },
};
</script>

<template>
  <div>
    <p v-if="visible">Абзац 1: Этот текст виден, когда visible равно true.</p>
    <p v-else>Абзац 2: Этот текст виден, когда visible равно false.</p>
    <button @click="click">Переключить видимость</button>
  </div>
</template>