<template>
	<header id="header" class="header">
		<nuxt-link to="/" class="header__logo">
			<img src="/images/svg_webicon-logo-long.svg" />
		</nuxt-link>
		<nav class="navigation">
			<ul class="navigation__list">
				<li class="navigation__item">
					<nuxt-link class="navigation__link" to="about">
						<span class="navigation__text">About</span>
					</nuxt-link>
				</li>
				<li class="navigation__item">
					<nuxt-link class="navigation__link" to="/work">
						<span class="navigation__text">Work</span>
					</nuxt-link>
				</li>
				<li class="navigation__item">
					<nuxt-link class="navigation__link" to="/contact">
						<span class="navigation__text">Contact</span>
					</nuxt-link>
				</li>
			</ul>
		</nav>
	</header>
</template>

<script>
import project from '~/package.json';
export default {
	data() {
		return {
			projectName: project.name
		};
	}
};
</script>

<style lang="scss">
@import '~tools';

.header {
	// Header styles
	position: fixed;
	top: 0;
	left: 0;
	z-index: 100;
	width: 100%;
	text-align: center;
	display: flex;
	justify-content: space-between;
	&__logo {
		padding: grid(0.5);
		display: block;
		img {
			height: 3rem;
		}
		@media #{$small-only} {
			width: 100px;
			overflow: hidden;
		}
	}
}
.navigation {
	padding: grid(0.5);
	&__list {
		display: flex;
	}
	&__link {
		position: relative;
		display: block;
		padding: grid(0.5) grid(0.25);
		text-decoration: none;
		@media #{$medium-down} {
			padding: 1rem;
		}
		&:hover {
			.navigation__text {
				@include linerIn();
			}
		}
		&.nuxt-link-exact-active {
			.navigation__text {
				@include linerIn();
				--line-color: #{color(Red)};
			}
		}
	}
	&__text {
		position: relative;
		font-size: rem(20);
		transition: clip-path 0.5s;
		color: color(White);
		--line-color: #{color(Yellow)};
		@include linerOut;
		.page--index & {
			color: color(Black);
		}
		&::before {
			height: 2px;
		}
	}
}
</style>
