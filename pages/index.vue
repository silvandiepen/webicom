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
	background-color: color(White);
	padding: grid(4 0);
	min-height: 100vh;
	width: 100vw;
	display: flex;
	align-items: center;
	justify-content: center;
}
</style>
