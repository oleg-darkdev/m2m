<script lang="ts">
	// import {  } from '$shared';
	// import {  } from '$widgets';
	// import {  } from '$entities';

	let { appData } = $props();
</script>

<div class="app-split-wrap">
	<a href="/" target="_blank" class="w-inline-block"
		><img
			src={appData.img}
			loading="lazy"
			style="
							-webkit-transform: translate3d(0, 50px, 0) scale3d(1, 1, 1) rotateX(0) rotateY(30deg)
								rotateZ(0) skew(0, 0);
							-moz-transform: translate3d(0, 50px, 0) scale3d(1, 1, 1) rotateX(0) rotateY(30deg)
								rotateZ(0) skew(0, 0);
							-ms-transform: translate3d(0, 50px, 0) scale3d(1, 1, 1) rotateX(0) rotateY(30deg)
								rotateZ(0) skew(0, 0);
							transform: translate3d(0, 50px, 0) scale3d(1, 1, 1) rotateX(0) rotateY(30deg)
								rotateZ(0) skew(0, 0);
							transform-style: preserve-3d;
						"
			sizes="(max-width: 479px) 98vw, (max-width: 767px) 43vw, (max-width: 991px) 40vw, (max-width: 3231px) 41vw, 1325px"
			alt=""
			class="hero-mockup"
		/></a
	>
	<div class="app-info-wrap">
		<h1 class="paragraph-heading">{appData.title}</h1>
		<h5 class="paragraph-subheading">
			{appData.subTitle}
		</h5>
		<p class="paragraph">
			{appData.shortDesc}
		</p>
		<a href={appData.link} target="_blank" class="icon-button icon-falls w-inline-block"
			><div class="button-icon-outline">
				<img src="images/icons/arrow-down.svg" width="58" alt="" class="button-icon" />
			</div>
			<div>Download Now</div></a
		>
	</div>
</div>

<style lang="postcss">
	.app-split-wrap {
		width: 43%;
		padding-right: 27px;
		-webkit-perspective: 1000px;
		perspective: 1000px;
	}

	@media screen and (max-width: 767px) {
		.app-split-wrap {
			padding-right: 3px;
		}
	}

	@media screen and (max-width: 479px) {
		.app-split-wrap {
			width: 99%;
			margin-bottom: 10%;
		}
	}

	.icon-button {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		margin-right: 15px;
		margin-bottom: 10px;
		-webkit-box-orient: horizontal;
		-webkit-box-direction: normal;
		-webkit-flex-direction: row;
		-ms-flex-direction: row;
		flex-direction: row;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
		-webkit-box-flex: 0;
		-webkit-flex: 0 0 auto;
		-ms-flex: 0 0 auto;
		flex: 0 0 auto;
		-webkit-transition: all 200ms ease;
		transition: all 200ms ease;
		color: #f8f8f8;
		font-size: 0.8rem;
		font-weight: 500;
		text-decoration: none;
	}

	.icon-button:hover {
		font-weight: 700;
	}

	.icon-button.rotate-icon.top-right {
		margin-right: 0px;
		margin-bottom: 0px;
	}

	.button-icon-outline {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 40px;
		height: 40px;
		margin-right: 10px;
		-webkit-box-orient: horizontal;
		-webkit-box-direction: normal;
		-webkit-flex-direction: row;
		-ms-flex-direction: row;
		flex-direction: row;
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-ms-flex-pack: center;
		justify-content: center;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
		border: 1px solid #f8f8f8;
		border-radius: 100px;
	}

	.button-icon {
		width: 20px;
	}

	.header-logo {
		width: 60px;
		margin-right: 0.8rem;
	}

	.body {
		padding-bottom: 3rem;
		color: #eee;
	}

	.paragraph-subheading {
		margin-top: 20px;
		margin-bottom: 20px;
		line-height: 1.4;
	}

	.paragraph-heading {
		margin-top: 0px;
		margin-bottom: 0px;
		font-size: 3.5rem;
		line-height: 1;
		font-weight: 500;
	}

	.paragraph-heading.padding-bottom {
		margin-bottom: 20px;
	}

	.minim-link {
		position: fixed;
		left: 0%;
		top: 0%;
		right: auto;
		bottom: auto;
		width: 120px;
	}

	.paragraph {
		margin-bottom: 20px;
		padding-right: 48px;
	}

	.heading {
		margin-top: 21px;
		margin-bottom: 21px;
	}

	.paragraph-2 {
		margin-bottom: 37px;
	}

	@media screen and (max-width: 991px) {
		.paragraph-heading {
			font-size: 3.2rem;
		}

		.minim-link {
			width: 100px;
		}
	}

	@media screen and (max-width: 767px) {
		.icon-button.rotate-icon.top-right {
			top: 19px;
			right: 71px;
		}

		.page-nav-header {
			height: 72px;
		}

		.button-icon-outline {
			width: 35px;
			height: 35px;
		}

		.simple-nav-header {
			font-size: 1rem;
		}

		.paragraph-heading {
			font-size: 2.8rem;
		}

		.minim-logo-img {
			width: 100px;
		}
	}

	@media screen and (max-width: 479px) {
		.icon-button {
			font-size: 0.75rem;
		}

		.icon-button.rotate-icon.top-right {
			top: 21px;
			right: 80px;
			padding-right: 0rem;
		}

		.page-nav-header {
			padding-right: 1rem;
			padding-left: 1rem;
		}

		.button-icon-outline {
			margin-right: 6px;
		}

		.simple-nav-header {
			margin-bottom: 3px;
			font-size: 0.8rem;
		}

		.header-logo {
			width: 50px;
			margin-right: 0.5rem;
		}

		.hero-mockup {
			width: 100%;
		}

		.app-info-wrap {
			padding-right: 0rem;
			padding-left: 1.7rem;
		}

		.paragraph-subheading {
			margin-bottom: 10px;
		}

		.minim-logo-img {
			width: 80px;
		}
	}
</style>
