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
			<div v-if="active === 0" class="experience-section--tab">
				<figure class="experience-section--figure">
					<img class="experience-section--img" src="../assets/images/productFactory.png" />
				</figure>
				<div class="experience-section--text-container">
					<p class="experience-section--text">
						This course has been attempted by zero people who are eager to learn product design,
						especially user experience and user interface, so it is not a prerequisite, but due to
						the limited capacity of the priority course with early enrolled people, others can
						participate in future courses. . <br />
						 Obviously, the ability to use tools like Adobe Photoshop and Adobe Illustrator as well
						as Microsoft Word, Excel tools, and of course a lot of enthusiasm and energy,
					</p>
				</div>
			</div>
			<div v-if="active === 1" class="experience-section--tab">
				<div class="experience-section--text-container">
					<p class="experience-section--text">
						This course has been attempted by zero people who are eager to learn product design,
						especially user experience and user interface, so it is not a prerequisite, but due to
						the limited capacity of the priority course with early enrolled people, others can
						participate in future courses. . <br />
						 Obviously, the ability to use tools like Adobe Photoshop and Adobe Illustrator as well
						as Microsoft Word, Excel tools, and of course a lot of enthusiasm and energy,
					</p>
				</div>
				<figure class="experience-section--figure">
					<img class="experience-section--img" src="../assets/images/productFactory.png" />
				</figure>
			</div>
			<div v-if="active === 2" class="experience-section--tab">
				<figure class="experience-section--figure">
					<img class="experience-section--img" src="../assets/images/productFactory.png" />
				</figure>
				<div class="experience-section--text-container">
					<p class="experience-section--text">
						This course has been attempted by zero people who are eager to learn product design,
						especially user experience and user interface, so it is not a prerequisite, but due to
						the limited capacity of the priority course with early enrolled people, others can
						participate in future courses. . <br />
						 Obviously, the ability to use tools like Adobe Photoshop and Adobe Illustrator as well
						as Microsoft Word, Excel tools, and of course a lot of enthusiasm and energy,
					</p>
				</div>
			</div>
		</BaseSection>
	</div>
</template>

<script setup>
import { ref } from 'vue';
import BaseSection from './BaseSection.vue';
import courseExperienceImg from '~/assets/images/Experience.png';

let active = ref(2);
const tabList = ['After attending the course', 'During the period', 'Before attending the course'];
</script>

<style lang="scss" scoped>
.experience {
	margin-bottom: 100px;
}
.experience-section--header {
	display: block;
	max-width: 615px;
	max-height: 145px;
	height: 100%;
	width: 100%;
	margin: 55px auto 65px;
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
	margin: 0px auto 71px;
	border-radius: 16px;
}
.active.experience-section--list-item {
	background: #000;
	color: #fff;
}
.experience-section--list-item {
	font-size: 18px;
	line-height: 22px;
	padding: 18px 4.15em;
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
.experience-section--tab {
	display: flex;
	align-items: center;
	justify-content: space-between;
	width: 100%;
	max-width: 1174px;
	margin: 0 auto;
	padding-bottom: 109px;
}
.experience-section--image {
	height: 281px;
	width: auto;
}
.experience-section--text-container {
	width: 65%;
}
.experience-section--text {
	font-size: 20px;
	line-height: 48px;
}
@media (max-width: 768px) {
	.experience-section--header {
		background-size: contain;
	}
	.experience-section--header-main {
		width: 100%;

		padding: 2em 0px;
		text-align: center;
	}
	.experience-section--list {
		flex-direction: column;
	}
	.experience-section--list-item {
		border-left: 1px solid #000;
		border-bottom: none;
		padding: 18px 1em;
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

	.experience-section--tab {
		flex-direction: column;
	}
	.experience-section--text-container {
		text-align: center;
		margin-top: 50px;
		width: 100%;
	}
}
@media (min-width: 768px) and (max-width: 1024px) {
	.experience-section--list-item {
		font-size: 16px;
		line-height: 20px;
		padding: 18px 1em;
	}
}
@media (min-width: 1025px) and (max-width: 1460px) {
	.experience-section--list-item {
		font-size: 16px;
		line-height: 20px;
		padding: 18px 3em;
	}
}
@media (max-width: 1460px) {
	.experience-section--img,
	.experience-section--text {
		padding: 0px 10px;
	}
}
@media (min-width: 1461px) {
	.experience-section--list-item {
		font-size: 18px;
		line-height: 22px;
		padding: 18px 4.15em;
	}
}
</style>
