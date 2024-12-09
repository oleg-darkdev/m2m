<script lang="ts">
	// import {  } from '$shared';
	// import {  } from '$widgets';
	// import {  } from '$entities'
</script>

<!-- <div class="scrolling-section">
	<div class="scrolling-collection-wrap w-dyn-list">
		<div role="list" class="scrolling-list w-dyn-items"> -->

<!-- <div class="case-studies-section mt-10">

<div class="cards-wrap">
	<div class="wrapper">
		<div class="scroll-list">
			{#each date.gallery as { img, figcaption, alt }}
				<div class="scroll-item">
				<div class="project-card w-inline-block">
					<img {alt} loading="eager" src="/images/{img}" class="cs-photo" />
					<div class="project-overlay">
						<div class="project-content">
							<h3 class="project-t	title">{figcaption}</h3>
							<p class="cs-card-category">
								{figcaption}
							</p>
						</div>
					</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
	<div class="button-wrapper">
		<a href={date.telegramLink} target="_blank" class=" mx-4 secondary-button w-button dark"
			>В телеграме </a
		>
		<a href="/app" target="_blank" class="mx-4 secondary-button w-button dark"
			>В приложении

			</a
		>

		<button class="secondary-button w-button dark">Показать все фотографии</button>
	</div>
</div>
</div> -->

<div style="background-image:url()" role="listitem" class="card-item w-dyn-item max-w-sm">
	<a href="/event/nesara-gesara" target="_blank" class="card-link scrolling-item w-inline-block">
		<div class="card-logo-wrapper">
			<img
				width="222"
				alt=""
				src="images/656e9994a83a4b2f90ff3437_Minim%20Logo%20Wht.png"
				sizes="(max-width: 479px) 21vw, (max-width: 767px) 14vw, (max-width: 991px) 13vw, 160px"
				class="card-logo-img"
			/>
		</div>
		<div class="card-date-tag blue">
			<div>Dec 25</div>
		</div>
		<img
			alt=""
			loading="lazy"
			src="images/unsplash.jpg"
			sizes="(max-width: 479px) 33vw, (max-width: 767px) 24vw, (max-width: 991px) 25vw, 20vw"
			class="card-bg-image"
		/>
	</a>
</div>

<!-- </div>
	</div>
</div> -->

<style lang="postcss">
	.card-logo-img {
		width: 10rem;
		margin-bottom: 30px;
	}

	.card-bg-image {
		z-index: 1;
		filter: brightness(60%);
		object-fit: cover;
		border-radius: 10px;
		width: 100%;
		height: 100%;
		position: absolute;
		top: 0%;
		bottom: 0%;
		left: 0%;
		right: 0%;
	}

	.card-logo-wrapper {
		z-index: 3;
		perspective: 2000px;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		width: 100%;
		display: flex;
		position: relative;
	}

	.scrolling-item {
		border-radius: 100px;
		padding: 15px;
	}

	.scrolling-item.gallery-item {
		flex: none;
		justify-content: center;
		align-items: center;
		width: 800px;
		height: 500px;
		display: flex;
	}

	.card-item {
		border: 0.15rem solid #fff;
		border-radius: 10px;
		justify-content: center;
		align-items: center;
		height: 360px;
		margin-top: 3%;
		margin-bottom: 3%;
		margin-right: 3%;
		transition: transform 0.2s;
		display: flex;
		position: relative;
		overflow: hidden;
	}

	.card-item:active {
		box-shadow: none;
		transform: none;
	}

	.card-item.scroll-item {
		background-image: url('../images/background-image.svg');
		background-position: 50%;
		background-repeat: no-repeat;
		background-size: cover;
		flex: none;
		width: 20vw;
		height: 35vh;
	}

	.card-date-tag {
		z-index: 10;
		background-color: var(--white-smoke);
		color: var(--black);
		border-radius: 100rem;
		padding: 7px 11px;
		font-size: 0.8rem;
		font-weight: 400;
		line-height: 1.2;
	}

	.card-date-tag.blue {
		color: var(--dark-borders);
		background-color: #fff;
		border-radius: 100rem;
		padding: 0.2rem 0.7rem;
		font-size: 0.8rem;
		font-weight: 400;
	}

	.card-link {
		color: #f8f8f8;
		border-radius: 10px;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		width: 100%;
		height: 100%;
		display: flex;
		position: relative;
	}

	.scrolling-section {
		width: 100vw;
		height: 100%;
		padding-top: 0;
		padding-bottom: 20px;
		position: relative;
	}
	.scrolling-list::-webkit-scrollbar {
		display: none;
	}

	.scrolling-list {
		flex-wrap: nowrap;
		justify-content: flex-start;
		align-items: center;
		padding-left: 5vw;
		padding-right: 1vw;
		display: flex;
		overflow: scroll;
	}

	.scrolling-list.pad-top-10px {
		margin-top: 10px;
	}

	@media screen and (min-width: 1920px) {
		.scrolling-item.gallery-item {
			width: 1200px;
			height: 700px;
		}
	}

	@media screen and (max-width: 991px) {
		.card-item.scroll-item {
			width: 25vw;
			height: 30vh;
		}

		.card-date-tag {
			font-size: 0.8rem;
		}
	}

	@media screen and (max-width: 767px) {
		.card-logo-img {
			width: 70%;
		}

		.scrolling-item.gallery-item {
			width: 320px;
			height: 300px;
		}

		.card-item {
			width: 220px;
			height: 320px;
		}

		.card-item.scroll-item {
			height: 45vh;
		}
	}

	@media screen and (max-width: 479px) {
		.scrolling-item {
			margin-left: 3px;
			margin-right: 3px;
			padding: 7px;
		}

		.scrolling-item.gallery-item {
			width: 280px;
			height: 220px;
		}

		.scrolling-list {
			align-content: flex-start;
			padding-top: 0;
			padding-left: 14px;
		}
		.card-item {
			width: 130px;
			height: 220px;
			margin: 9px;
		}

		.card-item:hover {
			transform: none;
			box-shadow: 0 9px 19px 2px rgba(0, 0, 0, 0.1);
		}

		.card-item.scroll-item {
			border-width: 0.15rem;
			width: 35vw;
			height: 25vh;
			margin-left: 10px;
			margin-right: 10px;
		}

		.card-date-tag {
			font-size: 0.7rem;
			line-height: 1.5;
		}

		.card-link {
			flex-direction: column;
			width: 100%;
			display: flex;
		}
	}
</style>
