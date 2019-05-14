<template>
	<main>
		<section class="about">
			<div class="row center">
				<div class="column small-full medium-two-third large-half">
					<div class="content">
						<h3>Hi! My name is Bassel</h3>
						<h4>I'm a developer from Rotterdam and I build all kinds of websites and apps.</h4>
						<p>
							Using React, Magento and other things. Because I'm almost just as wide as I am high, I fit perfectly everywhere.
						</p>
						<p>
							At the moment I'm building websites and parts of apps for a brand which sells glasses, I don't need them yet, but
							I do know a lot about glasses, shops and digital tools.
						</p>
						<p>
							My girlfriend, is really cool. We everything together, she cooks, I ate... I make a mess, she cleans. We are
							perfect together :)
						</p>
						<hr />
						<p>
							At the moment I'm not really looking for work, but if you have anything interesting, you can always
							<nuxt-link to="contact">
								contact
							</nuxt-link>
							me ofcourse!
						</p>
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

.about {
	background-color: color(Green);
	color: color(White);
	padding: grid(4 0);
	min-height: 100vh;
	width: 100vw;
	display: flex;
	align-items: center;
	justify-content: center;
}
</style>
