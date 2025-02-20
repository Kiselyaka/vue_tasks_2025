<script>
export default {
	data() {
		return {
			isDisabled: true,
		}
	},
	methods: {
		toggleInput() {
			this.isDisabled = !this.isDisabled;
		}
	}
}
</script>

<template>
	<div>
		Задача 1:
		<input type="text" v-bind:disabled="isDisabled" />
		<button @click="toggleInput">{{ isDisabled ? 'Разблокировать' : 'Заблокировать' }}</button>
	</div>
	<div>
		Задача 2:
		<input type="checkbox" v-model="isDisabled" /> Разрешить ввод
		<input type="text" v-bind:disabled="isDisabled" />
	</div>
</template>