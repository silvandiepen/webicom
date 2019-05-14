<template>
	<main>
		<section class="contact">
			<div class="row center">
				<div class="column small-full medium-two-third large-half">
					<div class="content">
						<h3>Contact</h3>
						<h4>Forms are annoying!</h4>
						<p>So just click here, and your mailbox will open so you can send me an email!</p>
						<a class="button" href="mailto:info@webicom.nl">E-mail me!</a>
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
.contact {
	display: flex;
	justify-content: center;
	align-items: center;
	width: 100vw;
	min-height: 100vh;
	background-color: color(Skyblue);
	color: color(White);
	padding: grid(4 0);
}
</style>
