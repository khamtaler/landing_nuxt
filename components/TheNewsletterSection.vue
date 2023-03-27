<template>
	<section class="newsletter-section" :style="{ backgroundImage: `url(${requestHeadingsImg})` }">
		<div class="newsletter-section--container">
			<Newsletter class="newsletter-container--newsletter" />
			<!-- <figure class="newsletter-section--figure">
				<img class="newsletter-section--image" src="../assets/images/NewsletterBg.png" />
			</figure> -->
		</div>
	</section>
</template>

<script setup>
import Newsletter from './Newsletter.vue';
import requestHeadingsImg from '~/assets/images/NewsletterBg.png';
</script>

<style lang="scss" scoped>
.newsletter-section {
	min-height: 603px;
	width: 100%;
	background: #000000;
	background-position: 91%;
	background-repeat: no-repeat;
	background-size: 40%;
	display: flex;
	align-items: center;
	justify-content: flex-start;
}

.newsletter-section--container {
	display: flex;
	align-items: center;
	max-width: 1500px;
	padding: 0px 20px;
	height: 100%;
	width: 100%;
	margin: 0 auto;
}
.newsletter-container--newsletter {
	margin-right: auto;
}
@media (max-width: 768px) {
	.newsletter-section {
		background-position: 110% 0%;
	}
}
@media (min-width: 1461px) {
	.newsletter-section--container {
		height: 100%;
	}
}
// @media (max-width: 1480px) {
// 	.newsletter-section--container {

// 	}
// }
</style>
