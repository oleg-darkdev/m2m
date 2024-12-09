<script lang="ts">
	import { faq } from '$sharedData';
	// import {  } from '$widgets';
	import { FaqCard } from '$entitiesLanding';
</script>

<a name="faq"></a>
<section class="small-accordion-section">
	<div class="section-header-wrapper no-pad-left">
		<div class="large-header-wrap invert">
			<!-- <div class="heading-overflow">
				<h1 class="big-split-header outline">A</h1>
				<h1 class="big-split-header outline">C</h1>
			</div> -->
			<div class="heading-overflow">
				<h1 class="big-split-header">ВОПРОС / ОТВЕТ</h1>
			</div>
		</div>
	</div>

	{#each faq as faqItem}
		<FaqCard {faqItem} />
	{/each}
</section>

<style lang="postcss">
	.section-header-wrapper.no-pad-left {
		padding-left: 0rem;
	}
	.heading-overflow {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		padding-top: 0px;
	}
	.big-split-header {
		margin-top: 0px;
		margin-right: 0px;
		margin-bottom: 0px;
		padding-top: 10px;
		padding-bottom: 6px;
		color: #fcfcfc;
		font-size: 9rem;
		line-height: 0.8;
		font-weight: 900;
		text-transform: uppercase;
	}
	.large-header-wrap {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		padding-top: 3px;
		padding-bottom: 7px;
		-webkit-box-orient: horizontal;
		-webkit-box-direction: normal;
		-webkit-flex-direction: row;
		-ms-flex-direction: row;
		flex-direction: row;
		-webkit-box-pack: start;
		-webkit-justify-content: flex-start;
		-ms-flex-pack: start;
		justify-content: flex-start;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
		-webkit-perspective: 1000px;
		perspective: 1000px;
	}
	.large-header-wrap.invert {
		-webkit-filter: invert(100%);
		filter: invert(100%);
	}
	.small-accordion-section {
		position: relative;
		z-index: 5;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 100vw;
		min-height: 40vh;
		padding-top: 8.8rem;
		padding-bottom: 4.5rem;
		padding-left: 3rem;
		-webkit-box-orient: vertical;
		-webkit-box-direction: normal;
		-webkit-flex-direction: column;
		-ms-flex-direction: column;
		flex-direction: column;
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-ms-flex-pack: center;
		justify-content: center;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
		background-color: #fcfcfc;
	}
	.section-header-wrapper {
		position: relative;
		overflow: hidden;
		width: 100%;
		margin-bottom: 2rem;
		padding-left: 3rem;
	}
	@media screen and (min-width: 1920px) {
		.big-split-header {
			font-size: 10rem;
			line-height: 1;
		}
	}
	@media screen and (min-width: 1440px) {
		.section-header-wrapper {
			padding-left: 5.1rem;
		}
		.big-split-header {
			border: 1px solid transparent;
			font-size: 9rem;
		}
	}
	@media screen and (max-width: 991px) {
		.big-split-header {
			font-size: 5.5rem;
		}
	}
	@media screen and (max-width: 767px) {
		.small-accordion-section {
			padding-left: 1.8rem;
			-webkit-box-align: start;
			-webkit-align-items: flex-start;
			-ms-flex-align: start;
			align-items: flex-start;
		}
		.heading-overflow {
			margin-bottom: -0.4rem;
			padding-top: 0px;
		}
	}
	@media screen and (min-width: 479px) {
		.small-accordion-section {
			padding: 3rem 1rem 0.1rem;
		}
		.section-header-wrapper {
			padding-left: 1.2rem;
		}
		.big-split-header {
			margin-top: 0px;
			font-size: 3.2rem;
		}
		.big-split-header.outline {
			padding-bottom: 3px;
		}
		.large-header-wrap {
			-webkit-box-orient: vertical;
			-webkit-box-direction: normal;
			-webkit-flex-direction: column;
			-ms-flex-direction: column;
			flex-direction: column;
			-webkit-box-align: start;
			-webkit-align-items: flex-start;
			-ms-flex-align: start;
			align-items: flex-start;
		}
	}
</style>
