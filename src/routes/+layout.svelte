<script lang="ts">
	import "./global.sass"
</script>

<header>
	<div class="headerContainer">
		<a class="headerlogo" href="/">
			<img src="/white.svg" alt="White eChat logo" />
		</a>
		<div class="right">
			<a href="/">Home</a>
			<a href="/about">About</a>
			<a href="/privacy">Privacy</a>
		</div>
	</div>
</header>

<main>
	<slot />
</main>

<style lang="sass">
	.headerlogo
		visibility: hidden

	header
		width: 100%
		font-size: 1.2rem
		top: 0
		height: 65px
		position: fixed
		align-content: center
		justify-content: center
		display: flex
		z-index: 1

		background-color: #31a47e

		.headerContainer
			width: 100%
			max-width: 1200px

			display: flex
			justify-content: space-between
			align-items: center
			align-content: center

			.right
				margin-right: 7rem
				padding: 0
				display: flex
				float: left
				justify-content: flex-end
				right: 1rem

			.headerlogo
				margin-left: min(8vw, 7rem)
				img
					height: 33px

			a
				min-width: 10%
				margin: 0 1.5rem
				color: white
				text-decoration: none
				transition: filter 0.2s
				&:hover
					transition: filter 0.2s
					filter: opacity(80%)
	
	.right
		text-align: right
		padding: 0 7rem

	@media screen and (max-width: 599px)

		header
			grid-template-columns: 0fr 1fr
			justify-content: center

		.right
			width: 100%
			a
				min-width: 2rem

	@media screen and (min-width: 600px)

		.headerlogo
			visibility: visible
			margin-left: 3rem
</style>
