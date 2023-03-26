<template>
	<div class="menu">
		<nav>
			<ul class="menu--list">
				<li class="menu-item">
					<NuxtLink class="menu-item--link" to="/">Projects</NuxtLink>
				</li>
				<li class="menu-item">
					<NuxtLink class="menu-item--link" to="/">Partners</NuxtLink>
				</li>
				<li class="menu-item">
					<NuxtLink class="menu-item--link" to="/">FAQ</NuxtLink>
				</li>
				<li class="menu-item">
					<NuxtLink class="menu-item--link" to="/">Masters</NuxtLink>
				</li>
				<li class="menu-item">
					<NuxtLink class="menu-item--link" to="/">Classes</NuxtLink>
				</li>
				<li class="menu-item">
					<NuxtLink class="menu-item--link" to="/">Course experience</NuxtLink>
				</li>
				<li class="menu-item">
					<NuxtLink class="menu-item--link" to="/">About us</NuxtLink>
				</li>
			</ul>
		</nav>
		<button class="button button-menu--register" type="button">Register</button>
	</div>
</template>

<script setup></script>
<style lang="scss">
.menu {
	display: flex;
	flex-direction: row;
	height: 52px;
	align-items: center;
	width: 100%;
}
.mobile {
	.menu {
		display: flex;
		flex-direction: column;
		position: absolute;
		top: 100%;
		left: 0;
		width: 100%;
		height: calc(100vh - 100%);
		background: #111111;
		align-items: center;
		justify-content: center;
	}
}

.menu--list {
	list-style: none;
	display: flex;
	gap: 35px;
}
.menu-item--link {
	color: #fff;
	text-decoration: none;
	font-size: 19px;
	line-height: 26px;
}
.button-menu--register {
	background: rgba(255, 255, 255, 0.1);
	color: #fff;
	font-size: 19px;
	line-height: 23px;
	padding: 14px 40px;
	border-radius: 30px;
	margin-left: auto;
	border: none;
}
@media (max-width: 1024px) {
	.menu--list {
		flex-direction: column;
		text-align: center;
	}
	.button-menu--register {
		margin: 30px auto;
	}
}
@media (max-width: 1024px) {
	.menu {
		display: none;
	}
}

@media (min-width: 1025px) {
	.menu--list {
		gap: 30px;
	}
	.button-menu--register {
		padding: 14px 20px;
	}
	.menu-item--link {
		font-size: 17px;
	}
}
@media (min-width: 1460px) {
	.menu-item--link {
		font-size: 19px;
	}
	.menu--list {
		gap: 70px;
	}
	.button-menu--register {
		padding: 14px 40px;
	}
}
</style>
