<script lang="ts">
	import { NewspaperCard } from '$sharedUi';
	// import {  } from '$widgets';
	// import {  } from '$entities'

	// взять из телеги инфу о статьях
	const newspapers = [
		{
			author: '',
			title: '',
			desc: ['', ''],
			link: '',
			logo: ''
		}
	];
</script>

<section id='newspapers' class="team-section-fold-out">
	<div class="section-container-2">
		<div class="section-header-wrap">
			<h1 class="header-lg white-text">О нас в новостных изданиях</h1>
			<div class="list-item-subtext">
				Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an
				unknown printer took a galley of type and scrambled it to make a type specimen book.
			</div>
		</div>
		<div class="card-wrapper">
			<NewspaperCard />
		</div>
	</div>
</section>

<style lang="postcss">
	.card-wrapper {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 100%;
		-webkit-flex-wrap: wrap;
		-ms-flex-wrap: wrap;
		flex-wrap: wrap;
	}

	.list-item-subtext {
		color: #a19f9f;
		font-size: 0.9rem;
	}

	.section-header-wrap {
		position: relative;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 100%;
		margin-bottom: 2rem;
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
	.section-container-2 {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 100%;
		max-width: 1200px;
		-webkit-box-orient: vertical;
		-webkit-box-direction: normal;
		-webkit-flex-direction: column;
		-ms-flex-direction: column;
		flex-direction: column;
	}

	.team-section-fold-out {
		position: relative;
		z-index: 1;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		overflow: hidden;
		width: 100vw;
		min-height: 40vh;
		padding: 1.9rem 5vw 5rem;
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
		background-color: #131313;
		color: #ededed;
	}

	@media screen and (min-width: 1920px) {
		.list-item-subtext {
			font-size: 1rem;
		}
	}

	@media screen and (max-width: 991px) {
		.list-item-subtext {
			font-size: 0.78rem;
		}
	}
	@media screen and (max-width: 991px) {
		.team-section-fold-out {
			padding: 5.5rem 5vw;
		}
	}
	@media screen and (max-width: 479px) {
		.team-section-fold-out {
			padding-top: 4rem;
			padding-bottom: 4rem;
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
</style>
