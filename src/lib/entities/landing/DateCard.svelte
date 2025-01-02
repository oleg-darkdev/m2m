<script lang="ts">
	// import {  } from '$shared';
	// import {  } from '$widgets';
	import { ImgCard } from '$sharedUi';

	let { date } = $props(),
		showInfo = $state(false);
</script>

<!-- {  timeToRead, memos, gallery, wikipediaLink, app,  } -->
<div id={date.anchor} role="listitem" class="calendar-item">
	<!-- h-64 -->
	<div class="event-container-wrap">
		<div class="flex flex-col">
			<div class="event-container">
				<div class="event-date-box">
					<div class="end-date-wrap">
						<!-- <div class="event-date date-decor">-</div> -->
						<div class="event-date secondary">{date.year}</div>
					</div>
					<div class="event-date">{date.day}</div>
					<div class="event-month">{date.shortMouth}.</div>
				</div>
				<div class="event-info-wrapper">
					<h1 class="event-item-header">{date.title}</h1>
					<div class="event-location">{date.location}</div>
					<div class="event-time-wrapper mb-10">
						<div class="event-time">{date.time}</div>
					</div>
					<div class="event-location">{date.shortDesc}</div>
				</div>
				<div class="event-button-wrapper-2 h-full">
					<a href={date.telegramLink} target="_blank" class="event-ticket-button-2 w-button my-3"
						>В телеграме <img
							src="images/icons/arrow-right-top-black.svg"
							loading="lazy"
							alt=""
							class="long-button-icon"
						/></a
					>
					<a href="/app" target="_blank" class="event-ticket-button-2 w-button"
						>В приложении

						<img
							src="images/icons/arrow-right-top-black.svg"
							loading="lazy"
							alt=""
							class="long-button-icon"
						/></a
					>

					<button
						on:click={() => (showInfo = !showInfo)}
						class="event-ticket-button-2 w-button mb-10 mt-10"
						>Подробнее <img
							src="images/icons/chevron-down.svg"
							loading="lazy"
							alt=""
							class="long-button-icon"
						/></button
					>
				</div>
			</div>
			<div class="event-container">
				{#if showInfo}
					<div class="full-desc-wrap mx-auto pb-8">
						{#each date.desc as desc}
							<p class="full-desc mb-2">
								{desc}
							</p>
						{/each}
						<div class="scroll-section-wrapper">
							<!-- <div class="header-wrapper less-top-padding">
								<div class="header-column-left">
								<div class="header-text-wrap">
									<h1 class="header outline">Events <br>
									</h1>
									<h1 data-w-id="890f36ef-b0a7-4584-ce02-5beff8a0be8c" class="scroll-section-header">Coming Up Next <br>
									</h1>
								</div>
								</div>
								<div class="header-column-right">
								<div class="scrolling-top-wrap">
									<a href="/events" class="scroll-arrow w-inline-block w-clearfix">
									<div class="scroll-arrow-txt">SEE�&nbsp;ALL</div>
									<img src="images/656e9994a83a4b2f90ff33d2_arrow-circle-up-right-light.svg" alt="" class="scroll-arrow-img">
									</a>
								</div>
								</div>
							</div> -->
							<ImgCard />
						</div>
						<div class="button-wrapper">
							<!-- <a href={date.telegramLink} target="_blank" class=" mx-4 secondary-button w-button dark"
										>В телеграме </a
									>
									<a href="/app" target="_blank" class="mx-4 secondary-button w-button dark"
										>В приложении

										</a
									> -->

							<button class="secondary-button w-button dark">Показать все фотографии</button>
						</div>
					</div>
				{/if}
			</div>
		</div>
	</div>
	<!-- <div class="profile-wrap">
						<div class="outline"></div>
						<img
							src="/images/dates/{date.avatar}"
							loading="lazy"
							sizes="(max-width: 479px) 75vw, (max-width: 991px) 256px, 320px"
							alt=""
							class="profile-image"
						/>
					</div> -->

	<!-- <div class="profile-wrap _2">
						<div class="outline"></div>
						<img
							src="images/613f9932ba9006efa9a1c61f_dhaya-eddine-bentaleb-6ZLrCWI3Ink-unsplash.jpg"
							loading="lazy"
							sizes="(max-width: 479px) 78vw, (max-width: 991px) 256px, 320px"
							alt=""
							class="profile-image"
						/>
					</div> -->
	<!-- avatar images/dates/{avatar} -->
</div>

<style lang="postcss">
	html.w-mod-js:not(.w-mod-ix) [data-w-id='36812a3d-9122-a1b0-05a9-0f4b6e6a98c8'] {
		filter: grayscale(100%) brightness(75%);
	}

	.long-button {
		position: relative;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		overflow: hidden;
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
		color: #f8f8f8;
	}

	.icon-button-2 {
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
		-webkit-transition: opacity 200ms ease;
		transition: opacity 200ms ease;
		color: #f8f8f8;
		font-size: 0.8rem;
		font-weight: 500;
		text-decoration: none;
	}

	.icon-button-2:hover {
		opacity: 0.65;
	}

	.heading-3 {
		font-size: 1rem;
		font-weight: 400;
		text-align: center;
		letter-spacing: 4px;
	}

	.enjoy-footer {
		position: relative;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 100vw;
		height: 100vh;
		-webkit-box-orient: vertical;
		-webkit-box-direction: normal;
		-webkit-flex-direction: column;
		-ms-flex-direction: column;
		flex-direction: column;
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-ms-flex-pack: center;
		justify-content: center;
	}

	.div-block {
		position: absolute;
		left: 0%;
		top: 0%;
		right: 0%;
		bottom: 0%;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
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

	.button-text-5 {
		position: relative;
		z-index: 20;
	}

	.heading-2 {
		/* background-image: url(''); */
		background-position: 0px 0px;
		background-size: cover;
		font-size: 8rem;
		line-height: 1;
		text-align: center;
		-webkit-background-clip: text;
		background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	.button-hover-circle-2 {
		position: absolute;
		left: -16px;
		top: auto;
		right: auto;
		bottom: -400%;
		z-index: 5;
		width: 125%;
		height: 400%;
		border-radius: 100%;
		background-color: #fff;
	}

	.button-hover-circle-2.dark {
		background-color: #eee;
	}

	.hero-image {
		position: absolute;
		left: -158px;
		top: 0%;
		right: auto;
		bottom: 0%;
		z-index: 1;
		width: 70%;
		height: 100%;
		border-style: none;
		border-width: 1px;
		border-color: #363636;
		opacity: 0.42;
		-o-object-fit: cover;
		object-fit: cover;
		-o-object-position: 50% 15%;
		object-position: 50% 15%;
	}

	.button-primary {
		position: relative;
		z-index: 20;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		overflow: hidden;
		height: 45px;
		margin-right: 1rem;
		padding: 12px 28px 12px 32px;
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-ms-flex-pack: center;
		justify-content: center;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
		border-style: dashed;
		border-width: 1px;
		border-color: #eee;
		border-radius: 100px;
		color: #eee;
		font-size: 0.65rem;
		font-weight: 700;
		letter-spacing: 2px;
		text-decoration: none;
		text-transform: uppercase;
	}

	.button-wrap {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-ms-flex-pack: center;
		justify-content: center;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
	}

	.page-section {
		position: relative;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 100vw;
		height: 100vh;
		padding: 5rem 5vw;
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

	.section-container {
		width: 100%;
		max-width: 1000px;
	}

	.heading {
		/* background-image: url('../images/63b33a8bc0ffbd467de7d505_kevin-young--icmOdYWXuQ-unsplash.jpg'); */
		background-position: 0px 0px;
		background-size: cover;
		font-size: 7rem;
		line-height: 1.2;
		text-align: left;
		-webkit-background-clip: text;
		background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	.paragraph {
		line-height: 1;
	}

	.section-subtitle {
		color: #a19f9f;
		font-size: 0.9rem;
	}

	.case-studies-section {
		/* height: 400vh; */
		padding-top: 0rem;
	}

	.scroll-item {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 40%;
		padding-right: 40px;
		-webkit-box-align: end;
		-webkit-align-items: flex-end;
		-ms-flex-align: end;
		align-items: flex-end;
		-webkit-box-flex: 0;
		-webkit-flex: 0 0 auto;
		-ms-flex: 0 0 auto;
		flex: 0 0 auto;
	}

	.button-wrapper {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		margin-top: 1rem;
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-ms-flex-pack: center;
		justify-content: center;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
	}

	.button-wrapper.case-studies {
		margin-top: 3rem;
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-ms-flex-pack: center;
		justify-content: center;
	}

	.button-icon {
		width: 17px;
	}

	.button-icon.pad-left {
		margin-left: 8px;
		-webkit-filter: invert(100%);
		filter: invert(100%);
	}

	.project-ttitle {
		margin-top: 0px;
		margin-bottom: 10px;
		color: #fff;
		font-size: 2vw;
		font-weight: 300;
		text-transform: capitalize;
	}

	.scroll-section-header {
		margin-top: 1rem;
		margin-bottom: 1rem;
		font-size: 3rem;
		line-height: 1;
		font-weight: 500;
		text-transform: capitalize;
	}

	.scroll-text-message {
		position: absolute;
		left: auto;
		top: 3rem;
		right: 5rem;
		bottom: auto;
		z-index: 50;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		padding: 10px 16px;
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-ms-flex-pack: center;
		justify-content: center;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
		opacity: 0.74;
		font-size: 0.65rem;
		font-weight: 700;
		text-transform: uppercase;
	}

	.cs-photo {
		width: 560px;
		height: 620px;
		-webkit-filter: brightness(75%) grayscale(100%);
		filter: brightness(75%) grayscale(100%);
		-o-object-fit: cover;
		object-fit: cover;
	}

	.project-card {
		position: relative;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		overflow: hidden;
		max-width: 450px;
		height: 30rem;
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-ms-flex-pack: center;
		justify-content: center;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
		-webkit-transition: -webkit-transform 600ms ease;
		transition: -webkit-transform 600ms ease;
		transition: transform 600ms ease;
		transition:
			transform 600ms ease,
			-webkit-transform 600ms ease;
	}

	.project-card:hover {
		-webkit-transform: skew(-2deg, 0deg);
		-ms-transform: skew(-2deg, 0deg);
		transform: skew(-2deg, 0deg);
	}

	.secondary-button {
		padding: 15px 20px;
		border-style: solid;
		border-width: 1px;
		border-color: #b4b4b4;
		border-radius: 30px;
		background-color: transparent;
		background-image: none;
		box-shadow: none;
		-webkit-transition: all 500ms ease;
		transition: all 500ms ease;
		color: #969696;
		font-size: 0.9rem;
		font-weight: 600;
	}

	.secondary-button:hover {
		border-style: solid;
		border-color: transparent;
		box-shadow:
			8px 11px 20px -1px hsla(0, 0%, 60%, 0.59),
			-12px -12px 20px -1px hsla(0, 0%, 100%, 0.77);
		color: #707070;
		text-shadow: none;
	}

	.secondary-button.dark:hover {
		box-shadow:
			8px 11px 20px -1px rgba(85, 85, 85, 0.59),
			-12px -12px 20px -1px rgba(58, 58, 58, 0.77);
	}

	.scroll-list {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		justify-content: space-between;
		width: 100%;
	}

	.project-content {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 100%;
		padding-right: 20px;
		padding-bottom: 2rem;
		padding-left: 20px;
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

	.section-header-wrap {
		position: relative;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 100%;
		margin-bottom: 3rem;
		-webkit-box-orient: vertical;
		-webkit-box-direction: normal;
		-webkit-flex-direction: column;
		-ms-flex-direction: column;
		flex-direction: column;
		-webkit-box-pack: start;
		-webkit-justify-content: flex-start;
		-ms-flex-pack: start;
		justify-content: flex-start;
		-webkit-box-align: start;
		-webkit-align-items: flex-start;
		-ms-flex-align: start;
		align-items: flex-start;
	}

	.cards-wrap {
		/* margin-top: 30px; */
	}

	.scroll-container {
		position: relative;
		z-index: 1;
		max-width: 1200px;
		margin-right: auto;
		margin-left: auto;
		-webkit-box-flex: 1;
		-webkit-flex: 1;
		-ms-flex: 1;
		flex: 1;
	}

	.project-overlay {
		position: absolute;
		left: 0%;
		top: 0%;
		right: 0%;
		bottom: 0%;
		z-index: 2;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		-webkit-box-align: end;
		-webkit-align-items: flex-end;
		-ms-flex-align: end;
		align-items: flex-end;
		background-image: -webkit-gradient(
			linear,
			left bottom,
			left top,
			from(#1f1f1f),
			color-stop(61%, rgba(0, 0, 0, 0.15))
		);
		background-image: linear-gradient(0deg, #1f1f1f, rgba(0, 0, 0, 0.15) 61%);
		opacity: 1;
	}

	.wrapper {
		width: 100%;
	}

	.cs-card-category {
		margin-bottom: 0px;
		color: hsla(0, 0%, 100%, 0.8);
		font-size: 0.75rem;
		font-weight: 600;
		text-align: center;
	}

	.sticky {
		position: -webkit-sticky;
		position: sticky;
		top: 0px;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		overflow: hidden;
		width: 100vw;
		height: 100vh;
		padding-left: 5%;
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-ms-flex-pack: center;
		justify-content: center;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
	}

	@media screen and (min-width: 1280px) {
		.scroll-section-header {
			max-width: 1000px;
		}
	}

	@media screen and (min-width: 1440px) {
		.scroll-text-message {
			font-size: 0.8rem;
		}
	}

	@media screen and (min-width: 1920px) {
		.section-subtitle {
			font-size: 1rem;
		}

		.button-wrapper {
			margin-top: 20px;
		}

		.button-icon {
			width: 1.3rem;
		}

		.scroll-section-header {
			line-height: 1;
		}

		.scroll-text-message {
			font-size: 1.1rem;
		}
	}

	@media screen and (max-width: 991px) {
		.section-subtitle {
			font-size: 0.78rem;
		}

		.case-studies-section {
			height: auto;
		}

		.scroll-item {
			width: 50%;
			padding-right: 0px;
			-webkit-box-flex: 0;
			-webkit-flex: 0 auto;
			-ms-flex: 0 auto;
			flex: 0 auto;
		}

		.button-wrapper {
			margin-top: 0.7rem;
		}

		.project-ttitle {
			margin-bottom: 1px;
			font-size: 22px;
		}

		.scroll-section-header {
			font-size: 2.7rem;
		}

		.scroll-text-message {
			display: none;
		}

		.project-card:hover {
			-webkit-transform: none;
			-ms-transform: none;
			transform: none;
		}

		.scroll-list {
			-webkit-flex-wrap: wrap;
			-ms-flex-wrap: wrap;
			flex-wrap: wrap;
		}

		.project-content {
			padding-bottom: 20px;
			-webkit-box-orient: vertical;
			-webkit-box-direction: normal;
			-webkit-flex-direction: column;
			-ms-flex-direction: column;
			flex-direction: column;
		}

		.project-overlay {
			background-image: -webkit-gradient(
				linear,
				left top,
				left bottom,
				from(hsla(0, 0%, 100%, 0)),
				to(rgba(0, 0, 0, 0.3))
			);
			background-image: linear-gradient(180deg, hsla(0, 0%, 100%, 0), rgba(0, 0, 0, 0.3));
		}

		.sticky {
			position: relative;
			overflow: visible;
			width: auto;
			height: auto;
			padding-top: 50px;
			padding-right: 5%;
			padding-bottom: 50px;
		}
	}

	@media screen and (max-width: 767px) {
		.page-nav-header {
			height: 72px;
		}

		.simple-nav-header {
			font-size: 1rem;
		}

		.hero-image {
			width: 100%;
		}

		.scroll-section-header {
			font-size: 3.5rem;
		}

		.scroll-text-message {
			display: none;
		}

		.project-card {
			margin-right: 9px;
		}
	}

	@media screen and (max-width: 479px) {
		.page-nav-header {
			padding-right: 1rem;
			padding-left: 1rem;
		}

		.simple-nav-header {
			margin-bottom: 3px;
			font-size: 0.8rem;
		}

		.header-logo {
			width: 50px;
			margin-right: 0.5rem;
		}

		.icon-button-2 {
			font-size: 0.75rem;
		}

		.hero-image {
			width: 100%;
			-o-object-position: 50% 0%;
			object-position: 50% 0%;
		}

		.button-primary {
			margin-top: 0.5rem;
			margin-right: 0.8rem;
			margin-bottom: 0.3rem;
			-webkit-align-self: center;
			-ms-flex-item-align: center;
			-ms-grid-row-align: center;
			align-self: center;
		}

		.section-subtitle {
			margin-bottom: 8px;
		}

		.scroll-item {
			width: 100%;
		}

		.scroll-section-header {
			font-size: 2.7rem;
		}

		.project-card {
			margin-bottom: 19px;
		}

		.section-header-wrap {
			margin-bottom: 0.6rem;
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

	.full-desc-wrap {
		width: 90%;
	}

	.full-desc {
		color: #1a1a1a;
		/* font-style: italic; */
		font-weight: 300;
		letter-spacing: 2px;
	}

	.event-container-wrap {
		display: flex;
		width: 80vw;
		-webkit-box-direction: normal;

		-webkit-box-pack: start;
		-webkit-justify-content: flex-start;
		-ms-flex-pack: start;
		justify-content: flex-start;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
		border-radius: 5px;
		-webkit-transition: -webkit-transform 200ms ease;
		transition: -webkit-transform 200ms ease;
		transition: transform 200ms ease;
		transition:
			transform 200ms ease,
			-webkit-transform 200ms ease;
	}

	.calendar-item {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 80vw;
		margin-top: 7px;
		margin-bottom: 7px;
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
		border: 0.15rem solid #000;
		border-radius: 5px;
		background-color: #fff;
		box-shadow: 3px 3px 9px 0 rgba(0, 0, 0, 0.2);
		-webkit-transition:
			box-shadow 200ms ease,
			-webkit-transform 200ms ease;
		transition:
			box-shadow 200ms ease,
			-webkit-transform 200ms ease;
		transition:
			transform 200ms ease,
			box-shadow 200ms ease;
		transition:
			transform 200ms ease,
			box-shadow 200ms ease,
			-webkit-transform 200ms ease;
	}

	.calendar-item:hover {
		box-shadow: 8px 8px 9px 0 rgba(0, 0, 0, 0.2);
		-webkit-transform: scale(1.03);
		-ms-transform: scale(1.03);
		transform: scale(1.03);
	}

	@media screen and (max-width: 991px) {
		.calendar-item {
			width: 85vw;
		}
	}
	@media screen and (max-width: 767px) {
		.calendar-item {
			width: 95vw;
			-webkit-box-align: start;
			-webkit-align-items: flex-start;
			-ms-flex-align: start;
			align-items: flex-start;
		}
		.full-desc {
			font-size: 12px;
		}
	}

	@media screen and (max-width: 479px) {
		.calendar-item {
			width: 300px;
			margin: 10px;
		}

		.full-desc {
			margin-top: 3px;
			margin-bottom: 3px;
			font-size: 14px;
			text-align: center;
		}
	}
	.event-ticket-button-2 {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: auto;
		min-width: 200px;
		height: 40px;
		/* margin: 6px 5px; */
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-ms-flex-pack: center;
		justify-content: center;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
		border-radius: 100px;
		background-color: hsla(0, 0%, 93.3%, 0.9);
		-webkit-transition:
			background-color 200ms ease,
			-webkit-transform 200ms ease;
		transition:
			background-color 200ms ease,
			-webkit-transform 200ms ease;
		transition:
			transform 200ms ease,
			background-color 200ms ease;
		transition:
			transform 200ms ease,
			background-color 200ms ease,
			-webkit-transform 200ms ease;
		color: #333;
		font-weight: 600;
		text-decoration: none;
	}

	.event-ticket-button-2:hover {
		background-color: hsla(0, 0%, 44.7%, 0.28);
		-webkit-transform: translate(0px, -2px);
		-ms-transform: translate(0px, -2px);
		transform: translate(0px, -2px);
	}

	@media screen and (max-width: 767px) {
		.event-ticket-button-2 {
			width: 100px;
			height: 35px;
		}
	}
	@media screen and (max-width: 479px) {
		.event-ticket-button-2 {
			width: 120px;
			height: 40px;
		}
	}

	.event-date {
		color: #494949;
		font-size: 60px;
		line-height: 1em;
		font-weight: 700;
		text-align: center;
	}

	.event-date.date-decor {
		font-size: 20px;
		font-weight: 400;
	}

	.event-date.secondary {
		font-size: 20px;
		font-weight: 600;
	}

	.event-button-wrapper-2 {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 20%;
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

	.event-info-wrapper {
		width: 64%;
	}

	.event-time {
		margin-right: 2px;
		margin-left: 2px;
		font-family: Ubuntu, Helvetica, sans-serif;
		font-weight: 300;
	}

	.event-location {
		color: #1a1a1a;
		font-style: italic;
		font-weight: 400;
		letter-spacing: 2px;
	}

	.event-date-box {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 16%;
		min-height: 160px;
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

	.event-month {
		color: #494949;
		font-weight: 200;
		text-align: center;
		letter-spacing: 10px;
		text-transform: uppercase;
	}

	.event-container {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
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
	}

	.event-time-wrapper {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		-webkit-box-pack: start;
		-webkit-justify-content: flex-start;
		-ms-flex-pack: start;
		justify-content: flex-start;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
		font-weight: 600;
	}

	.event-item-header {
		margin-bottom: 5px;
		color: #494949;
		font-size: 32px;
		line-height: 1.2em;
	}

	.end-date-wrap {
		position: relative;
		left: 26px;
		top: 4px;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
	}

	.event-list {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		padding-bottom: 36px;
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-ms-flex-pack: center;
		justify-content: center;
		-webkit-flex-wrap: wrap;
		-ms-flex-wrap: wrap;
		flex-wrap: wrap;
		-webkit-box-align: start;
		-webkit-align-items: flex-start;
		-ms-flex-align: start;
		align-items: flex-start;
		-webkit-align-content: center;
		-ms-flex-line-pack: center;
		align-content: center;
	}

	.body {
		background-color: #fff;
		font-family: Poppins, sans-serif;
	}

	.hero-heading {
		margin-top: 76px;
		margin-bottom: 73px;
		font-family: Poppins, sans-serif;
		color: rgba(85, 85, 85, 0);
		font-size: 8rem;
		line-height: 1;
		font-weight: 900;
		text-transform: uppercase;
	}

	.minim-link {
		position: fixed;
		left: 0%;
		top: 0%;
		right: auto;
		bottom: auto;
	}

	@media screen and (max-width: 991px) {
		.event-date.date-decor {
			margin-right: 0px;
			font-size: 20px;
			font-weight: 400;
		}

		.event-date.secondary {
			margin-right: 2px;
			font-size: 20px;
		}

		.event-button-wrapper-2 {
			margin-right: 7px;
		}

		.event-container {
			width: 100%;
		}

		.event-item-header {
			font-size: 22px;
		}

		.end-date-wrap {
			position: relative;
			left: 29px;
			top: 7px;
			display: -webkit-box;
			display: -webkit-flex;
			display: -ms-flexbox;
			display: flex;
			margin-bottom: 5px;
		}

		.event-list {
			width: 100vw;
		}

		.hero-heading {
			margin-top: 161px;
			margin-bottom: 18px;
		}
	}

	@media screen and (max-width: 767px) {
		.event-date {
			font-size: 40px;
		}

		.event-date.secondary {
			font-size: 18px;
		}

		.event-button-wrapper-2 {
			margin-right: 13px;
		}

		.event-time {
			font-size: 12px;
		}

		.event-location {
			font-size: 12px;
		}

		.event-date-box {
			margin-right: 20px;
			margin-left: 11px;
		}

		.event-month {
			font-size: 8px;
		}

		.event-container {
			width: 100%;
		}

		.event-item-header {
			font-size: 20px;
		}

		.event-list {
			width: 100vw;
		}

		.hero-heading {
			margin-top: 172px;
			font-size: 6rem;
		}
	}

	@media screen and (max-width: 479px) {
		.event-date {
			font-size: 60px;
		}

		.event-button-wrapper-2 {
			margin-bottom: 22px;
		}

		.event-info-wrapper {
			display: -webkit-box;
			display: -webkit-flex;
			display: -ms-flexbox;
			display: flex;
			width: 93%;
			margin-bottom: 5px;
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

		.event-time {
			font-size: 16px;
		}

		.event-location {
			margin-top: 3px;
			margin-bottom: 3px;
			font-size: 14px;
			text-align: center;
		}

		.event-date-box {
			min-height: auto;
			margin-top: 25px;
			margin-bottom: 8px;
		}

		.event-month {
			font-size: 12px;
		}

		.event-container {
			-webkit-box-orient: vertical;
			-webkit-box-direction: normal;
			-webkit-flex-direction: column;
			-ms-flex-direction: column;
			flex-direction: column;
		}

		.event-item-header {
			margin-bottom: 0px;
			font-size: 22px;
			text-align: center;
		}

		.hero-heading {
			margin-top: 173px;
			margin-bottom: 18px;
			font-size: 3rem;
		}
	}
</style>
