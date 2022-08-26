<script lang="ts" context="module">
	throw new Error("@migration task: Replace error load function (https://github.com/sveltejs/kit/discussions/5774#discussioncomment-3293209)");

	// export function load({ error, status }: { error: object; status: number }) {
	// 	return {
	// 		props: {
	// 			status: status,
	// 			error: error,
	// 		},
	// 	}
	// }
	// // copied straight from kit.svelte.dev
</script>

<script lang="ts">
	export let status: number
	export let error: any
</script>

<div class="thinpage">
	<div class="thintext">
		<br />
		<h1>
			Error {status}
		</h1>
		{error["message"]}
	</div>
</div>