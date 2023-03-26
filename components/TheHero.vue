<template>
	<div class="hero">
		<BaseSection class="hero-section">
			<div class="hero-section--container">
				<div>
					<h1>Product Design Course</h1>
					<h2 :style="{ backgroundImage: `url(${HeaderBg})` }">Product Factory</h2>
					<p>
						Learn how design thinking, user research, <br />
						business vision and marketing, and finally designing and creating real digital products
						for real users.
					</p>
					<button type="button">Start Register</button>
				</div>

				<img src="../assets/images/kiauxcourse.png" />
			</div>
		</BaseSection>
	</div>
</template>

<script setup>
import BaseSection from './BaseSection.vue';
import HeaderBg from '~/assets/images/UIUX.png';
</script>

<style lang="scss" scoped>
.hero {
	height: 788px;
	background: #111;
}
.hero-section {
	height: 788px;
	width: 100%;
	max-width: 1460px;
	position: absolute;
	top: 152px;
	left: 50%;
	transform: translateX(-50%);
}
</style>
