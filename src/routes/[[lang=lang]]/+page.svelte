<script lang="ts">
	// import {} from '$sharedData';
	// import {} from '$sharedUi';
	// import { } from '$widgetsLanding';

	import { Header, Footer, Faq, WebApp, Hero, List, Newspapers } from '$widgetsLanding';
	// import { SEO } from '$sharedUtils';
	// import { } from '$widgetsLanding';
</script>

<svelte:head>
	<title>Минута в минуту | Home</title>
	<meta name="description" content="" />
</svelte:head>

<!-- <SEO title="Home" /> -->

<div class="" style='overflow: hidden;'>
	<Header />

	<!-- горизонтальная полоса прокрутки в каждом блоке -->
	<Hero />

	<List />

	<WebApp />

	<Newspapers />

	<Faq />

	<div class="page-hero-section">
		<div class="hero-info-wrap">
			<div class="page-hero-tag white">A REaL SWELL</div>
			<h1 class="large-page-heading outline">Footer</h1>
		</div>
		<div class="text-block">scroll down</div>
	</div>

	<Footer />
</div>

<style lang="postcss">
	
</style>
