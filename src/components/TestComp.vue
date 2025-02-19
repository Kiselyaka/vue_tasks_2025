
<script>
export default {
  data() {
	return {
	  cssClasses: ['active', 'valid'],
  }
  }
};

// а ты все еще копируешь, да?

</script>

<template>
  <div> <br />	
  <p :class="cssClasses">
	  1
  </p> <br />
  <p :class="cssClasses">
	  2
  </p>
  </div>
</template>

<style>
.active {
color: green;
}

.valid {
font-weight: bold;
}
</style>