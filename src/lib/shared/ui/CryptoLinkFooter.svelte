<script lang="ts">
	// import {  } from '$shared';
	// import {  } from '$widgets';
	// import {  } from '$entities'

	import { fade } from 'svelte/transition';

	function copyToClipboard(data) {
		navigator.clipboard
			.writeText(data)
			.then(() => {
				// добавить появление карточки уведомляющий о скопированном или об ошибке
				console.log(data);
			})
			.catch((err) => {
				console.error('Ошибка при копировании: ', err);
			});
	}

	let { link } = $props();

	let { copiedInfo } = $state(false);
</script>

<button
	class="long-button w-inline-block"
	on:click={() => {
		copyToClipboard(link.shortUrl);
		copiedInfo = !copiedInfo;
		setTimeout(() => {
			copiedInfo = false;
		}, 2000);
	}}
>
	<div class="long-button-underlay"></div>
	<div class="long-button-info">
		{#if copiedInfo}
			<div class="long-button-title" in:fade>Сcылка скопирована</div>
		{:else}
			<div class="long-button-title" in:fade>{link.platform}</div>
			<div class="long-button-link-wrap" in:fade>
				<div class="long-button-link-txt truncated-shorturl">{link.shortUrl}</div>
				<img src="images/icons/replicate.svg" loading="lazy" alt="copy" class="long-button-icon" />
			</div>
		{/if}
	</div>
</button>

<style lang="postcss">
	
</style>
