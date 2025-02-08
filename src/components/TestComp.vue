<script>
export default {
  data() {
    return {
		items: [1, 2, 3],
    };
  },
  methods: {
        click: function(){
			this.hide_swap = !this.hide_swap;
		}
  },
};

</script>

<template>
	<div>
	Задача 1:
		<div v-for="(elem, key) in items">
    	<p>{{ elem }}</p>
    	<p class="divider"></p>
  		</div>
		  <ul>
	Задача 2:
		<template v-for="(elem, key) in items">
      	<li>{{ elem }}</li>
      	<li class="divider"></li>
    	</template>
  	</ul>
	</div>
  </template>