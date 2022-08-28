<svelte:head>
	<title>eChat</title>
</svelte:head>

<div class="grid">
	<div>
		<img class="eccb" src="eccb.webp" alt="eChat on a Chromebook 11 3189" />
	</div>
	<div class="homepageInfoContainer">
		<div class="homepageInfo">
			<img class="mainLogo" src="green.svg" alt="Green eChat logo" />
			<p>
				A simple chat extension.<br />
				Chat in groups, or one on one.<br />
			</p>
		</div>
	</div>
</div>

<style lang="sass">
	.eccb
		position: absolute
		object-fit: contain
		height: 80vh
		margin-top: 3%
		right: 50%
		max-width: 80vh
	
	.grid
		width: 100%
		display: grid
		grid-template-columns: 1fr 1fr
		column-gap: 0.7rem

	.eccb
		visibility: hidden

	.homepageInfo
		margin-left: 2rem
		display: flex
		flex-direction: column

	.mainLogo
		width: 30vw
		max-width: 20rem
		margin-top: 30vh

	@media screen and (max-width: 599px)

		.grid
			grid-template-columns: 0fr 1fr
			justify-content: center

		.mainLogo
			width: 60vw
			max-width: 28rem

		.homepageInfo
			margin: 0
		.homepageInfoContainer
			display: flex
			justify-content: center

	@media screen and (min-width: 600px)

		.eccb
			visibility: visible

		.headerlogo
			margin-left: 3rem
</style>