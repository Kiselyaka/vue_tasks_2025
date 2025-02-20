<script>
export default {
  data() {
    return {
      arr: [],
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
    <div>
      Знаете ли вы JavaScript: <input type="checkbox" v-model="arr" value="JavaScript">
    </div>
    <div>
      Знаете ли вы C++: <input type="checkbox" v-model="arr" value="C++">
    </div>
    <div>
      Знаете ли вы Dart: <input type="checkbox" v-model="arr" value="Dart">
    </div>
    
    <div>
      <h3>Выбранные языки:</h3>
      <ul>
        <li v-for="(language, index) in arr" :key="index">{{ language }}</li>
      </ul>
    </div>

    <div>
      {{ result }}
    </div>
  </div>
</template>