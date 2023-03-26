<template>
	<div :class="toggle ? 'mobile' : ''">
		<button type="button" @click="() => (toggle = true)">
			<img src="../assets/images/Hamburger_icon.svg" />
		</button>
		<button type="button" @click="() => (toggle = false)">
			<img src="../assets/images/close-icon.svg" />
		</button>
		<NuxtLink to="/"><img src="../assets/images/logo.png" /></NuxtLink>
		<TheMenu />
		<button type="button">Register</button>
	</div>
</template>

<script setup>
import TheMenu from './TheMenu.vue';
import { ref } from 'vue';

let toggle = ref(false);
</script>

<style lang="scss" scoped></style>
