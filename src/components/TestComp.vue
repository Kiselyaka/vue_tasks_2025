<script>
export default {
  data() {
    return {
      visible1: false, 
	  visible2: false,
	  visible3: false,
    };
  },
  methods: {
    toggle1: function() {
      this.visible1= !this.visible1; 
    },
	toggle2: function(){
		this.visible2= !this.visible2; 
	},
	toggle3: function(){
		this.visible3= !this.visible3; 
	},
  },
};

</script>

<template>
  <div>
  <div>
	<button @click="toggle1">toggle</button>
	<p v-if="visible1">text</p>
  </div>
  <div>
	<button @click="toggle2">toggle</button>
	<p v-if="visible2">text</p>
  </div>
  <div>
	<button @click="toggle3">toggle</button>
	<p v-if="visible3">text</p>
  </div>
  </div>
</template>	