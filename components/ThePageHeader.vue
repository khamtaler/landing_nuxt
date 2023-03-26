<template>
	<header class="header" :class="toggle ? 'mobile' : ''">
		<button class="button button-mobile--open" type="button" @click="() => (toggle = true)">
			<HamburgerIcon class="button-mobile--open-icon" />
		</button>
		<button class="button button-mobile--close" type="button" @click="() => (toggle = false)">
			<CloseIcon class="button-mobile--close-icon" />
		</button>
		<NuxtLink class="header-logo" to="/"><img src="../assets/images/logo.png" /></NuxtLink>
		<TheMenu />
	</header>
</template>

<script setup>
import TheMenu from './TheMenu.vue';
import { ref } from 'vue';
import CloseIcon from './icons/CloseIcon.vue';
import HamburgerIcon from './icons/HamburgerIcon.vue';
let toggle = ref(false);
</script>

<style lang="scss" scoped>
.header {
	display: flex;
	max-width: 1500px;
	padding: 0px 20px;
	width: 100%;
	height: 52px;
	margin: 50px auto;
	position: absolute;
	top: 0;
	z-index: 2;
	left: 50%;
	transform: translateX(-50%);
}
.header-logo {
	height: 100%;
}
.button-mobile--open,
.button-mobile--close {
	display: none;
	padding: 0px;
	background: none;
	border: none;
	position: absolute;
	left: 20px;
	top: 50%;
	transform: translateY(-50%);
	width: 30px;
	z-index: 3;
}
.button-mobile--open-icon,
.button-mobile--close-icon {
	height: 50%;
	width: auto;
	margin: auto 0;
}
.button-mobile--open-icon,
.button-mobile--close-icon {
	filter: invert(94%) sepia(6%) saturate(24%) hue-rotate(305deg) brightness(107%) contrast(106%);
}
@media (max-width: 768px) {
	.header {
		display: flex;
	}
	.header-logo {
		margin: 0px;
	}
}
@media (min-width: 1025px) {
	.header-logo {
		margin-right: 30px;
	}
}
@media (min-width: 1460px) {
	.header-logo {
		margin-right: 76px;
	}
}

@media (max-width: 1024px) {
	.button-mobile--open {
		display: block;
	}
	.header-logo {
		position: absolute;
		left: 50%;
		top: 50%;
		transform: translate(-50%, -50%);
		margin: 0px;
	}
	.mobile {
		.button-mobile--open {
			display: none;
		}
		.button-mobile--close {
			display: block;
		}
	}
}
</style>
