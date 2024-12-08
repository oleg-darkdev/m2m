<script lang="ts">
	// import {  } from '$shared';
	// import {  } from '$widgets';
	// import {  } from '$entities'

	let { faqItem } = $props();
</script>

<div class="small-accordion-item">
	<div class="accordion-tab-button-dark">
		<!-- {faqItem.icon} -->
		<img src="images/icons/person.svg" loading="lazy" width="20" alt="" class="accordion-icon" />
		<h1 class="small-accordion-header with-icon">{faqItem.a}</h1>
		<div class="accordion-arrow-wrap">
			<img
				src="images/icons/chevron-down.svg"
				loading="lazy"
				alt=""
				class="simple-accordion-arrow"
			/>
		</div>
	</div>

	<div class="small-accordion-pane">
		<div class="accordion-pane-content">
			<div class="small-accordion-text">{faqItem.q}</div>
		</div>
	</div>
</div>

<style lang="postcss">
</style>
