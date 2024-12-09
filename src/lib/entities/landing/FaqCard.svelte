<script lang="ts">
	// import {  } from '$shared';
	// import {  } from '$widgets';
	// import {  } from '$entities'

	let { faqItem } = $props(),
		showAnswer = $state(false);
</script>

<div class="small-accordion-item" on:click={() => (showAnswer = !showAnswer)}>
	<div class="accordion-tab-button-dark">
		<!-- {faqItem.icon} -->
		<img src="images/icons/{faqItem.icon}" loading="lazy" width="20" alt="" class="accordion-icon" />
		<h1 class="small-accordion-header with-icon">{faqItem.q}</h1>
		<div class="accordion-arrow-wrap">
			<img
				src="images/icons/{showAnswer ? 'chevron-up.svg' : 'chevron-down.svg'}"
				loading="lazy"
				alt=""
				class="simple-accordion-arrow"
			/>
		</div>
	</div>

	{#if showAnswer}
		<div class="small-accordion-pane">
			<div class="accordion-pane-content">
				{#each faqItem.a as aswer}
					<div class="small-accordion-text">{aswer}</div>
				{/each}
			</div>
		</div>
	{/if}
</div>

<style lang="postcss">
</style>
