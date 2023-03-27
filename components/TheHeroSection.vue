<template>
	<div class="hero">
		<BaseSection class="hero-section">
			<div class="hero-section--container">
				<div class="hero-section--welcome">
					<header>
						<h1 class="hero-section--header-main">Product Design Course</h1>
						<h2
							class="hero-section--header-secondary"
							:style="{ backgroundImage: `url(${HeaderBg})` }"
						>
							Product Factory
						</h2>
					</header>

					<p class="hero-section--text">
						Learn how design thinking, user research, business&nbsp;vision and marketing, and
						finally designing and&nbsp;creating real digital products for real users.
					</p>
					<button class="button hero-section--button" type="button">Start Register</button>
				</div>

				<figure class="hero-section--figure">
					<img class="hero-section--image" src="../assets/images/hero.png" alt="factory image" />
				</figure>
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
	margin-bottom: 152px;
}
.hero-section {
	height: 100%;
	width: 100%;
	position: absolute;
	top: 152px;
	left: 50%;
	transform: translateX(-50%);
}
.hero-section--container {
	height: 100%;
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: space-between;
}
.hero-section--welcome {
	max-width: 564px;
	width: 100%;
	margin-right: auto;
	flex: 1;
}
.hero-section--header-main {
	font-size: 50px;
	line-height: 61px;
	font-weight: bold;
}
.hero-section--header-secondary {
	font-size: 38px;
	line-height: 46px;
	font-weight: 400;
	color: #8d8d8d;
	padding: 20px 0px 80px 0px;
	background-position: center center;
	background-size: contain;
	background-repeat: no-repeat;
}
.hero-section--text {
	margin: 35px 0px 25px;
	font-size: 23px;
	line-height: 55px;
}
.hero-section--button {
	width: 390px;
	height: 72px;
	margin-top: 50px;
	color: #fff;
	text-align: center;
	font-size: 24px;
	line-height: 27px;
	font-weight: 700;
	background: #f46632;
	border: none;
	border-radius: 16px;
}
.hero-section--figure {
	flex: 1;
}
.hero-section--image {
	max-width: 530px;
	width: 100%;
}
@media (max-width: 768px) {
	.hero-section--text {
		margin: 15px 0px;
	}
}
@media (max-width: 1024px) {
	.hero-section--header-main {
		font-size: 35px;
		line-height: 44px;
	}
	.hero-section--header-secondary {
		font-size: 25px;
		line-height: 34px;
	}
	.hero-section--text {
		font-size: 17px;
		line-height: 40px;
	}
	.hero-section--welcome {
		margin: 30px auto 0px;
	}
	.hero-section--button {
		display: block;
		width: 70%;
		margin: 20px auto;
		font-size: 20px;
		height: 55px;
	}
	.hero-section--image {
		display: block;
		margin: 0px auto;
	}
}
@media (max-width: 1024px) {
	.hero-section--welcome {
		padding-right: 0px;
	}
}
@media (min-width: 1025px) {
	.hero-section--container {
		padding: 50px;
		flex-direction: row;
	}
	.hero-section--image {
		float: right;
	}
}

@media (min-width: 1460px) {
	.hero-section--container {
		padding: 0px 134px;
	}
	.hero-section--header-secondary {
		margin-right: 14px;
	}
}
@media (min-width: 1025px) and (max-width: 1459px) {
	.hero-section--welcome {
		padding-right: 20px;
	}
}
</style>
