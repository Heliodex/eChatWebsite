<script lang="ts">
	import { page } from "$app/stores"
</script>

<svelte:head>
	<title>eChat - Error {$page.status}</title>
</svelte:head>

<div class="thinpage">
	<div class="thintext">
		<br />
		<h1>
			Error {$page.status}
		</h1>
		{$page.error.message}
	</div>
</div>
