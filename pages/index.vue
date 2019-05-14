<template>
	<main class="page page--home">
		<section class="intro">
			<WebicomLogo />
		</section>
	</main>
</template>

<script>
import WebicomLogo from '~/components/webicom.vue';
export default {
	components: {
		WebicomLogo
	}
};
</script>

<style lang="scss">
@import '~tools';

.page {
	// general page styles
	&--home {
		// specific home styles
	}
}

.intro {
	display: flex;
	justify-content: center;
	align-items: center;
	width: 100vw;
	min-height: 100vh;
	background-color: color(White);
	padding: grid(4 0);
}
</style>
