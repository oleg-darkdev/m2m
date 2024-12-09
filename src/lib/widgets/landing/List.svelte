<script lang="ts">
	import { promoDates, allDates } from '$sharedData';
	// import {  } from '$widgets';
	import { DateCard } from '$entitiesLanding';
</script>

<a name="dates"></a>

<section class="overflow-hidden">
	<div class="calendar-section">
		<div
			class="flex max-w-6xl flex-wrap content-center items-center justify-center md:flex-nowrap md:justify-center lg:flex-nowrap lg:justify-start"
		>
			<h1 class="outline-title-list mb-4">{allDates.length} События</h1>

			<div class="">
				<!-- <h3 class="media-footer-header">HEY!</h3> -->
				<h4 class="footer-subheading mb-4">
					<div class="empty-state w-dyn-empty">
						<div class="empty-collection-text">Полный список событий</div>
					</div>
				</h4>
				<div class="footer-button-wrap">
					<a
						href="https://t.me/minutavminutu"
						target="_blank"
						class="icon-button-2 rotate-icon w-inline-block"
					>
						<div class="button-icon-outline-2">
							<img src="images/icons/telegram.svg" width="58" alt="" class="button-icon-2" />
						</div>
						<div class="icon-button-text-2">в телеграме</div>
					</a>
					<a href="/app" target="_blank" class="icon-button-2 rotate-icon w-inline-block">
						<div class="button-icon-outline-2">
							<img src="images/icons/devices.svg" width="58" alt="" class="button-icon-2" />
						</div>
						<div class="icon-button-text-2 address">в веб-приложении</div>
					</a>
				</div>
			</div>
			<!-- <div class=" event-collection w-dyn-list">
			<div class="empty-state w-dyn-empty">
				<div class="empty-collection-text">Полный список событий</div>
			</div>
			<a href="" target="_blank" class="secondary-button w-button dark mx-2 mt-1.5 flex flex-row">
				в телеграме <img
					src="images/icons/arrow-right-top.svg"
					loading="lazy"
					alt=""
					class="long-button-icon"
				/>
			</a>
			<span class="mr-2">и</span>
			<a href="/app" target="_blank" class="secondary-button w-button dark mt-1.5 flex flex-row"
				>в приложении <img
					src="images/icons/arrow-right-top.svg"
					loading="lazy"
					alt=""
					class="long-button-icon"
				/>
			</a>
		</div> -->
		</div>
		<div class="event-collection w-dyn-list mt-6">
			<div role="list" class="event-list w-dyn-items">
				{#each promoDates as date}
					<DateCard {date} />
				{/each}
			</div>
		</div>

		<!-- <button class="secondary-button w-button light">Показать все фотографии</button> -->
	</div>
</section>

<!-- <div class="mt-20">
	<h1 class="outline-title-list">Lorem impsum</h1>

	<div class="event-collection w-dyn-list">
		<div class="empty-state w-dyn-empty">
			<div class="empty-collection-text">Nothing at this time.</div>
		</div>
	</div>
</div> -->

<style lang="postcss">
	.empty-collection-text {
		text-align: center;
	}
	.empty-state {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 300px;
		padding-right: 18px;
		padding-left: 18px;
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-ms-flex-pack: center;
		justify-content: center;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
		border-radius: 20px;
		background-color: #6ed59b;
	}

	.duplicate-me {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		overflow: hidden;
		width: 100vw;
		min-height: 50vh;
		padding: 2% 22px;
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

	.outline-title-list {
		-webkit-text-fill-color: transparent;
		-webkit-background-clip: text;
		-webkit-text-stroke: 0.01em #fff;
		margin-top: 76px;
		/* margin-bottom: 73px; */

		border-color: #a5a5a5;
		font-size: 8rem;
		line-height: 1;
		font-weight: 900;
		text-transform: uppercase;
	}
	.event-collection {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
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
	}
	.calendar-section {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		overflow: hidden;
		width: 100vw;
		min-height: 50vh;
		padding: 2% 22px;
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

	@media screen and (max-width: 991px) {
		.calendar-section {
			padding-right: 6%;
			padding-left: 6%;
		}

		.duplicate-me {
			padding-right: 6%;
			padding-left: 6%;
		}
		.outline-title-list {
			-webkit-text-fill-color: transparent;
			-webkit-background-clip: text;
			-webkit-text-stroke: 0.01em #fff;
			margin-top: 161px;
			margin-bottom: 18px;

			border-color: #a5a5a5;
			font-size: 8rem;
			line-height: 1;
			font-weight: 900;
			text-transform: uppercase;
		}
	}

	@media screen and (max-width: 767px) {
		.calendar-section {
			padding-right: 11px;
			padding-left: 11px;
		}
		.duplicate-me {
			padding-right: 11px;
			padding-left: 11px;
		}
		.outline-title-list {
			-webkit-text-fill-color: transparent;
			-webkit-background-clip: text;
			-webkit-text-stroke: 0.01em #fff;
			margin-top: 172px;
			font-size: 6rem;

			border-color: #a5a5a5;
			line-height: 1;
			font-weight: 900;
			text-transform: uppercase;
		}
	}

	@media screen and (max-width: 479px) {
		.calendar-section {
			padding-right: 4px;
			padding-left: 4px;
		}
		.outline-title-list {
			-webkit-text-fill-color: transparent;
			-webkit-background-clip: text;
			-webkit-text-stroke: 0.01em #fff;
			margin-top: 173px;
			margin-bottom: 18px;
			font-size: 3rem;

			border-color: #a5a5a5;
			line-height: 1;
			font-weight: 900;
			text-transform: uppercase;
		}
		.duplicate-me {
			padding-right: 4px;
			padding-left: 4px;
		}
	}
</style>
