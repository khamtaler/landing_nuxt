<template>
	<section class="section">
		<div class="section-wrapper">
			<slot />
		</div>
	</section>
</template>

<script setup></script>

<style lang="scss" scoped>
.section {
	max-width: 1500px;
	width: 100%;
	padding: 0px 20px;
	margin: auto;
}
.section-wrapper {
	background: #fff;
	border-radius: 30px;
	max-width: 1460px;
	min-height: 100%;
	padding: 0px 20px;
}
@media (min-width: 768px) {
	.section-wrapper {
		display: grid;
	}
}
</style>
