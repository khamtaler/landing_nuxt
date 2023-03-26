<template>
	<div class="section">
		<slot />
	</div>
</template>

<script setup></script>

<style lang="scss" scoped>
.section {
	background: #fff;
	border-radius: 30px;
	padding: 20px;
}

@media (min-width: 1025px) {
	.section {
		padding: 50px;
	}
}
@media (min-width: 1460px) {
	.section {
		padding: 134px;
	}
}
</style>
