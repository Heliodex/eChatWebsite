<script lang="ts">
	import "./global.sass"
</script>

<header class="grid">
	<div class="left">
		<img class="headerlogo" src="white.svg" alt="White eChat logo"/>
	</div>
	<div class="right">
		<a href="/">Home</a>
		<a href="/about">About</a>
	</div>
</header>

<main>
	<slot />
</main>
