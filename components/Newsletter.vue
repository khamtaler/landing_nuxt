<template>
	<div class="newsletter">
		<header class="newsletter--header">
			<h3 class="newsletter--header-main">Request a list of headings</h3>
		</header>
		<p class="newsletter--desc">
			Please enter your email address to receive course titles, the topics will be emailed to you.
		</p>
		<input class="newsletter--email-input" type="email" placeholder="AfshinT2Y@gmail.com" />
		<button class="newsletter--send-button" v-if="!send"></button>
		<p class="newsletter--confirmation-box">
			<CheckIcon class="newsletter--confirmation-icon" /><span class="newsletter--confirmation-text"
				>Your email has been successfully registered, headlines will be sent to you soon.</span
			>
		</p>
	</div>
</template>

<script setup>
import CheckIcon from './icons/CheckIcon.vue';
let send = ref(true);
</script>

<style lang="scss" scoped>
.newsletter--header {
	margin-bottom: 25px;
}
.newsletter--header-main {
	color: #fff;
	font-size: 34px;
	line-height: 42px;
	font-weight: bold;
}
.newsletter--desc {
	color: #fff;
	font-size: 20px;
	line-height: 40px;
	max-width: 571px;
}
.newsletter--email-input {
	width: 100%;
	max-width: 557px;
	height: 62px;
	letter-spacing: 0.5px;
	margin: 42px 0px 47px 0px;
	background: rgba(255, 255, 255, 0.15);
	border: none;
	border-radius: 16px;
	font-size: 22px;
	line-height: 27px;
	padding: 0px 40px 0px 40px;
	color: #fff;
	&:focus-visible {
		border: none;
		outline: none;
	}
}
.newsletter--confirmation-box {
	display: flex;
	align-items: center;
}
.newsletter--confirmation-icon {
	width: 27px;
	margin-right: 15px;
	flex-shrink: 0;
}
.newsletter--confirmation-text {
	color: #acacac;
	font-size: 20px;
	line-height: 40px;
}
@media (max-width: 768px) {
	.newsletter--confirmation-text {
		line-height: 27px;
	}
}
</style>
