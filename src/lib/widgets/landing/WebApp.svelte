<script lang="ts">
	// import {  } from '$shared';
	// import {  } from '$widgets';
	import { AppCard } from '$entitiesLanding';

	const appData = [
		{
			img: 'images/phone.png',
			title: 'В телеграме',
			subTitle:
				'Lorem Ipsum jest tekstem stosowanym jako przykładowy wypełniacz w przemyśle poligraficznym.',
			shortDesc:
				'Pięć wieków później zaczął być używany przemyśle elektronicznym, pozostając praktycznie niezmienionym. Spopularyzował się w latach 60. XX w. wraz z publikacją arkuszy Letrasetu, zawierających fragmenty Lorem Ipsum.',
			link: 'https://t.me/minutavminutu'
		},
		{
			img: 'images/phone.png',
			title: 'Веб-приложение',
			subTitle:
				'Lorem Ipsum jest tekstem stosowanym jako przykładowy wypełniacz w przemyśle poligraficznym.',
			shortDesc:
				'Pięć wieków później zaczął być używany przemyśle elektronicznym, pozostając praktycznie niezmienionym. Spopularyzował się w latach 60. XX w. wraz z publikacją arkuszy Letrasetu, zawierających fragmenty Lorem Ipsum.',
			link: '/app'
		}
	];
</script>

<!-- <a href="http://bradleycandesign.com" target="_blank" class="minim-link w-inline-block"
	><img
		src="images/60ef005d18142423e7c16946_Minim%20Logo%20Sq.jpg"
		loading="lazy"
		width="120"
		sizes="(max-width: 479px) 80px, (max-width: 991px) 100px, 120px"
		srcset="
					images/60ef005d18142423e7c16946_Minim%2520Logo%2520Sq-p-500.jpeg  500w,
					images/60ef005d18142423e7c16946_Minim%2520Logo%2520Sq-p-800.jpeg  800w,
					images/60ef005d18142423e7c16946_Minim%20Logo%20Sq.jpg            1000w
				"
		alt=""
		class="minim-logo-img"
	/></a
> -->

<a name="about-app"></a>
<section class="app-hero-wrap">
	<h1 class="hero-header">Веб-приложение</h1>
	<p class="hero-tag">Lorem Ipsum is simply dummy text.</p>
</section>
<section class="apps-section">
	<AppCard appData={appData[0]} />
	<AppCard appData={appData[1]} />
</section>

<style lang="postcss">
	.apps-section {
		position: relative;
		z-index: 1;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		overflow: hidden;
		width: 100vw;
		min-height: 100vh;
		margin-bottom: 5%;
		padding-top: 1%;
		-webkit-box-orient: horizontal;
		-webkit-box-direction: normal;
		-webkit-flex-direction: row;
		-ms-flex-direction: row;
		flex-direction: row;
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-ms-flex-pack: center;
		justify-content: center;
		-webkit-box-align: start;
		-webkit-align-items: flex-start;
		-ms-flex-align: start;
		align-items: flex-start;
	}

	.hero-header {
		display: inline;
		margin-bottom: 5px;
		padding-right: 0px;
		padding-left: 0px;
		opacity: 0.45;
		font-family: Integralcf, sans-serif;
		color: #fff;
		font-size: 12em;
		line-height: 1em;
		font-weight: 900;
	}

	.app-hero-wrap {
		position: relative;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		overflow: visible;
		width: 100vw;
		min-height: 45vh;
		padding-top: 4.1rem;
		padding-bottom: 4.1rem;
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
	}

	.hero-tag {
		position: absolute;
		margin-bottom: 0px;
		font-family: Integralcf, sans-serif;
		font-size: 1.4rem;
		font-weight: 400;
		letter-spacing: 3px;
	}

	@media screen and (max-width: 991px) {
		.hero-header {
			font-size: 12em;
		}
	}

	@media screen and (max-width: 767px) {
		.app-hero-wrap {
			background-position: 61% 50%;
		}
		.hero-header {
			font-size: 10em;
		}
		.app-split-wrap {
			padding-right: 3px;
		}
	}

	@media screen and (max-width: 479px) {
		.app-hero-wrap {
			height: 30vh;
			min-height: 30vh;
			padding-top: 1.9rem;
			padding-bottom: 1.9rem;
		}
		.hero-header {
			width: auto;
			font-size: 5em;
		}
		.hero-tag {
			margin-top: 26px;
			font-size: 0.7rem;
		}
		.app-split-wrap {
			width: 99%;
			margin-bottom: 10%;
		}
		.apps-section {
			min-height: 70vh;
			padding-top: 40px;
			-webkit-box-orient: vertical;
			-webkit-box-direction: normal;
			-webkit-flex-direction: column;
			-ms-flex-direction: column;
			flex-direction: column;
		}
	}
</style>
