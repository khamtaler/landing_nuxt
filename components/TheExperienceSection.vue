<template>
	<div class="experience">
		<BaseSection>
			<header
				class="experience-section--header"
				:style="{ backgroundImage: `url(${courseExperienceImg})` }"
			>
				<h2 class="experience-section--header-main">Course Experience</h2>
			</header>
			<ul class="experience-section--list">
				<li
					class="experience-section--list-item"
					:class="active === index ? 'active' : ''"
					v-for="(tab, index) in tabList"
					:key="index"
					@click="
						() => {
							active = index;
						}
					"
				>
					{{ tab }}
				</li>
			</ul>
		</BaseSection>
	</div>
</template>

<script setup>
import BaseSection from './BaseSection.vue';
import courseExperienceImg from '~/assets/images/Experience.png';
import { ref } from 'vue';
let active = ref(2);
const tabList = ['After attending the course', 'During the period', 'Before attending the course'];
</script>

<style lang="scss" scoped>
.experience {
	height: 1000px;
}
.experience-section--header {
	display: block;
	max-width: 615px;
	max-height: 145px;
	height: 100%;
	width: 100%;
	margin: 0 auto;
	background-size: cover;
	background-position: center center;
	background-repeat: no-repeat;
}
.experience-section--header-main {
	font-size: 32px;
	line-height: 39px;
	font-weight: bold;
	padding-top: 67px;
	padding-left: 177px;
	padding-bottom: 39px;
}
.experience-section--list {
	display: flex;
	align-items: stretch;
	justify-content: center;
	max-width: 1016px;
	width: 100%;
	margin: 0 auto;

	border-radius: 16px;
}
.active.experience-section--list-item {
	background: #000;
	color: #fff;
}
.experience-section--list-item {
	font-size: 18px;
	line-height: 22px;
	padding: 19px 4.15em;
	border-top: 1px solid #000000;
	border-right: 1px solid #000000;
	border-bottom: 1px solid #000000;
	text-align: center;
}

.experience-section--list-item:first-child {
	border-left: 1px solid #000000;
	border-top-left-radius: 16px;
	border-bottom-left-radius: 16px;
}
.experience-section--list-item:last-child {
	border-top-right-radius: 16px;
	border-bottom-right-radius: 16px;
}
.experience-section--list-item {
	list-style: none;
}
.experience-section--list-item:hover {
	cursor: pointer;
}

@media (max-width: 768px) {
	.experience-section--list {
		flex-direction: column;
	}
	.experience-section--list-item {
		border-left: 1px solid #000;
		border-bottom: none;
	}
	.experience-section--list-item:first-child {
		border-top-left-radius: 16px;
		border-top-right-radius: 16px;
		border-bottom-left-radius: 0px;
	}
	.experience-section--list-item:last-child {
		border-bottom: 1px solid #000;
		border-bottom-left-radius: 16px;
		border-bottom-right-radius: 16px;
		border-top-left-radius: 0px;
		border-top-right-radius: 0px;
	}
}
@media (min-width: 768px) and (max-width: 1024px) {
	.experience-section--list-item {
		font-size: 16px;
		line-height: 20px;
		padding: 19px 1em;
	}
}
@media (min-width: 1025px) and (max-width: 1460px) {
	.experience-section--list-item {
		font-size: 16px;
		line-height: 20px;
		padding: 19px 3em;
	}
}
@media (min-width: 1460px) {
	.experience-section--list-item {
		font-size: 18px;
		line-height: 22px;
		padding: 19px 4.15em;
	}
}
</style>
