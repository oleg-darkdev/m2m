<script lang="ts">
	import '../../../app/app.css';

	let { children } = $props();
</script>

<main class="overflow-hidden">
	{@render children()}
</main>

<style lang="postcss">
</style>
