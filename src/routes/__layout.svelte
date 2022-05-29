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
