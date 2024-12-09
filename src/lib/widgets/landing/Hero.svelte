<script lang="ts">
	// import {  } from '$shared';
	// import {  } from '$widgets';
	// import {  } from '$entities'
	import { navigationLanding } from '$sharedData';
</script>

<!-- <div class="page-nav-header">
	<div class="nav-header-wrap">
		<img
			src="images/613f6eeb93991a11547e7d6d_Wht%20Logo.png"
			loading="lazy"
			sizes="(max-width: 479px) 50px, 60px"
			srcset="
						images/613f6eeb93991a11547e7d6d_Wht%2520Logo-p-500.png   500w,
						images/613f6eeb93991a11547e7d6d_Wht%2520Logo-p-800.png   800w,
						images/613f6eeb93991a11547e7d6d_Wht%2520Logo-p-1080.png 1080w,
						images/613f6eeb93991a11547e7d6d_Wht%2520Logo-p-1600.png 1600w,
						images/613f6eeb93991a11547e7d6d_Wht%20Logo.png          2000w
					"
			alt=""
			class="header-logo"
		/>
		<h1 class="simple-nav-header">SCROLL N SHOW<br /></h1>
	</div>
</div> -->

<!-- <div class="section">
	<div class="wrapper">
		<div class="hero-info-column">
			<h1 class="large-hero-text">WE ARE</h1>
			<h1 class="large-hero-text">YOUR</h1>
			<h1 class="large-hero-text">BRIDGE</h1>
			<h1 class="large-hero-text">TO�&nbsp;</h1>
			<h1 class="large-hero-text outline">BLOCK</h1>
			<h1 class="large-hero-text outline">CHAIN</h1>
			<h1 class="large-hero-text">TECH</h1>
		</div>
		<div class="hero-coin-wrap frosted">
			<img src="images/613f715b25c79153be11bb81_Crypto%20A%202.png" alt="" class="coin-logo" />
		</div>
	</div>
</div> -->

<section style='overflow: hidden;'>
	<!-- -->
	<div class="hero-coin-section  overflow-hidden">
		<!--  -->
		<div class="w-container">
			<!--  -->
			<div class="sticky-info-column">
				<!--  -->
				<div class="hero-info-column  mb-20">
					<h1 class="large-hero-text">С разницей</h1>
					<h1 class="large-hero-text outline-text">в десятки лет,</h1>
					<h1 class="large-hero-text outline-text">с точностью</h1>
					<h1 class="large-hero-text outline-text">до минуты.</h1>
				</div>
				<!-- footer-columns smell-footer  bg-white -->
				<div class="p-8 pl-20">
					<div class="footer-column">
						<h5 class="footer-column-header">Навигация</h5>
						<div class="long-button-wrap">
							{#each navigationLanding as { title, link }}
								<a href={link} class="long-button w-inline-block">
									<div class="long-button-underlay"></div>
									<div class="long-button-info">
										<div class="long-button-title">{title}</div>
										<div class="long-button-link-wrap">
											<!-- <div class="long-button-link-txt">{link}</div> -->
											<img
												src="images/icons/link.svg"
												loading="lazy"
												alt=""
												class="long-button-icon"
											/>
										</div>
									</div>
								</a>
							{/each}
						</div>
					</div>
				</div>
			</div>
			<!-- <div class="sticky-header-column">
			<div class="hero-coin-wrap frosted">
				<img
					src="images/hero.svg"
					sizes="(max-width: 479px) 190px, (max-width: 767px) 238px, (max-width: 991px) 270px, 223.1875px"
					alt=""
					class="coin-logo"
				/>
			</div>
		</div> -->
		</div>
	</div>
</section>



<section class="section-dose">
	<a name="about"></a>
	<div class="summary-wrapper">
		<div class="about-text-wrap">
			<h1 class="about-text-large ">
				
				Реконструкция <br /> событий  с  точностью до минуты. 
			</h1>
			<h6 class="heading-4">
				Dating is hard when you're a dude in your momma's basement. Take second to think about how
				you could get a leg up on the pile and refinance your dreams. We'll get you there!
			</h6>
			<div class="event-video-btn-wrap">
				<div class="pulse-button-text-wrap">
					<div class="pulse-button-wrap">
						<div class="pulsing-play-button">
							<img src="images/icons/play.svg" loading="lazy" alt="" class="play-button-img" />
						</div>
						<div class="play-button-pulse"></div>
					</div>
					<div class="play-button-text">Watch Promo</div>
				</div>
			</div>
		</div>



		<div class="profile-wrap">
			<div class="outline"></div>
			<img
				src=""
				loading="lazy"
				sizes="(max-width: 479px) 75vw, (max-width: 991px) 256px, 320px"
				alt=""
				class="profile-image"
			/>
		</div>
		<div class="profile-wrap _2">
			<div class="outline"></div>
			<img
				src=""
				loading="lazy"
				sizes="(max-width: 479px) 78vw, (max-width: 991px) 256px, 320px"
				alt=""
				class="profile-image"
			/>
		</div>
	</div>
</section>



<!-- <div class="video-modal">
	<div style="padding-top: 56.17021276595745%" class="video-2 w-video w-embed">
		<iframe
			class="embedly-embed"
			src="//cdn.embedly.com/widgets/media.html?src=https%3A%2F%2Fwww.youtube.com%2Fembed%2F87T6jIK9QZg%3Ffeature%3Doembed&amp;display_name=YouTube&amp;url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3D87T6jIK9QZg&amp;image=https%3A%2F%2Fi.ytimg.com%2Fvi%2F87T6jIK9QZg%2Fhqdefault.jpg&amp;key=96f1f04c5f4143bcb0f2e68c87d65feb&amp;type=text%2Fhtml&amp;schema=youtube"
			scrolling="no"
			title="YouTube embed"
			frameborder="0"
			allow="autoplay; fullscreen"
			allowfullscreen="true"
		></iframe>
	</div>
	<a href="#" class="video-modal-close-button w-inline-block"
		><div class="underline-button-wrap-2">
			<div class="top-line-wrap-2"><div class="top-line"></div></div>
			<div class="button-text-2">Close</div>
			<div style="width: 0%" class="underline"></div>
		</div></a
	>
</div> -->

<style lang="postcss">
	.hero-coin-section {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		overflow: hidden;
		width: 90vw;
		height: 120vh;
		/* margin-right: auto;
		margin-left: auto; */
		/* padding-right: 0rem;
		padding-left: 0rem; */
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-ms-flex-pack: center;
		justify-content: center;
		-webkit-box-align: start;
		-webkit-align-items: flex-start;
		-ms-flex-align: start;
		align-items: flex-start;
		text-align: center;
	}

	.large-hero-text {
		position: static;
		bottom: 290.609375px;
		/* z-index: 20; */
		margin-top: 0px;
		margin-bottom: 0rem;
		font-size: 6em;
		line-height: 1;
		font-weight: 700;
		text-align: center;
	}

	.large-hero-text._2 {
		font-weight: 900;
	}

	.large-hero-text.outline-text {
		font-weight: 700;
	}
	.hero-info-column {
		/* z-index: 11; */
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		-webkit-box-orient: vertical;
		-webkit-box-direction: normal;
		-webkit-flex-direction: column;
		-ms-flex-direction: column;
		flex-direction: column;
		-webkit-box-pack: start;
		-webkit-justify-content: flex-start;
		-ms-flex-pack: start;
		justify-content: flex-start;
		-webkit-box-align: end;
		-webkit-align-items: flex-end;
		-ms-flex-align: end;
		align-items: flex-end;
	}
	.sticky-info-column {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 100%;
		z-index: 12;
		/* position: relative; */
		/* padding-top: 4vh; */
		/* padding-left: 30vh; */

		padding-top: 18vh;
		padding-left: 10vh;
		-webkit-box-orient: vertical;
		-webkit-box-direction: normal;
		-webkit-flex-direction: column;
		-ms-flex-direction: column;
		flex-direction: column;
		-webkit-box-pack: start;
		-webkit-justify-content: flex-start;
		-ms-flex-pack: start;
		justify-content: flex-start;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
	}

	@media screen and (max-width: 991px) {
		.hero-info-column {
			margin-right: 0.4rem;
		}
		.sticky-info-column {
			width: 50%;
			padding-right: 30px;
			padding-left: 30px;
		}
	}
	@media screen and (max-width: 479px) {
		.hero-info-column {
			margin-right: 0rem;
		}
		.sticky-info-column {
			width: 100%;
		}

		.hero-coin-section {
			-webkit-box-orient: vertical;
			-webkit-box-direction: normal;
			-webkit-flex-direction: column;
			-ms-flex-direction: column;
			flex-direction: column;
		}
	}
</style>
