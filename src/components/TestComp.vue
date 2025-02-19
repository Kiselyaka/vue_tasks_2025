
<script>
export default {
  data() {
	return {
		obj: {
			done: true,
			selected:  false,
		},
  }
  }
};

// а ты все еще копируешь, да?

</script>

<template>
	<p :class="obj">text</p>
</template>
