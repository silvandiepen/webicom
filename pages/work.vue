<template>
	<main>
		<section class="work">
			<div class="row center">
				<div class="column small-full medium-two-third large-half">
					<div class="content">
						<h3>Work</h3>
						<h4>Working I do during the day, night and morning.</h4>
						<p>So I do creata lot actually. Here you can find some examples of things I made!</p>
					</div>
				</div>
			</div>
		</section>
	</main>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import '~tools';
.work {
	display: flex;
	justify-content: center;
	align-items: center;
	width: 100vw;
	min-height: 100vh;
	background-color: color(Army);
	color: color(White);
	padding: grid(4 0);
}
</style>
