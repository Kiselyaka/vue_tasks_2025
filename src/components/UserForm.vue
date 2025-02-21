<script>
	export default {
    data() {
	return {
		newName: '',
		newSurn: '',
	}
},
    props: {
	id:     Number,
	name:   String,
	surn:   String,
},
emits: ['add']['change'],
methods: {
	save() {
		this.$emit('add', this.newName, this.newSurn);
	}
},
}
</script>

<template>
    <div>
	<input v-model="newName">
	<input v-model="newSurn">
	
	<button @click="save">
		save
	</button>
    </div>
</template>