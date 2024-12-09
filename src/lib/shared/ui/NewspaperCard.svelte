<script lang="ts">
	// import {  } from '$shared';
	// import {  } from '$widgets';
	// import {  } from '$entities'
</script>

<div class="expand-card-wrap">
	<div class="card-1">
		<div class="team-member-shot"></div>
		<div>
			<h3 class="no-margin-bottom">Lorem Ipsum</h3>
			<h5 class="no-margin-top">Lorem Ipsum has been the industry's standard</h5>
		</div>
	</div>
	<div class="card-2">
		<p class="team-card-paragraph">
			Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse varius enim in eros
			elementum tristique. Duis cursus, mi quis viverra ornare, eros dolor interdum nulla, ut
			commodo diam libero vitae erat. Aenean faucibus nibh et justo cursus id rutrum lorem
			imperdiet. Nunc ut sem vitae risus tristique posuere.
		</p>
	</div>
	<div class="card-3">
		<div class="flex flex-row">
			<div class="flex flex-col">
				<a href="#" class="card-contact-link w-inline-block"
					><img src="images/icons/phone.svg" alt="" /></a
				>
			</div>
		</div>
	</div>
</div>

<style lang="postcss">
	.team-card-paragraph::-webkit-scrollbar {
		display: none;
	}
	.card-3 {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		overflow: hidden;
		height: 70px;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
		border-bottom-left-radius: 2px;
		border-bottom-right-radius: 2px;
		background-color: #d4d4d4;
		-webkit-backface-visibility: hidden;
		backface-visibility: hidden;
		-webkit-transform: perspective(1800px);
		transform: perspective(1800px);
		-webkit-transform-origin: 50% 0%;
		-ms-transform-origin: 50% 0%;
		transform-origin: 50% 0%;
		text-align: center;
		-webkit-transform-style: preserve-3d;
		transform-style: preserve-3d;
	}
	.team-card-paragraph {
		-ms-overflow-style: none; /* IE and Edge */
		scrollbar-width: none; /* Firefox */
	}

	.team-card-paragraph {
		overflow: scroll;
		max-height: 150px;
		margin-top: 15px;
		margin-bottom: 1px;
		color: #1f1f1f;
		font-size: 0.85rem;
		line-height: 1.4;
	}
	.no-margin-bottom {
		margin-bottom: 0px;
		color: #1f1f1f;
		font-size: 1.2rem;
		line-height: 1.1;
	}

	.no-margin-top {
		margin-top: 0px;
		color: #1f1f1f;
		font-weight: 400;
	}

	.card-contact-link {
		width: 2.5rem;
		height: 2.5rem;
		margin-right: 10px;
		padding: 11px;
		border-radius: 100rem;
		background-color: #3a3a3a;
		-webkit-transition: -webkit-transform 300ms ease;
		transition: -webkit-transform 300ms ease;
		transition: transform 300ms ease;
		transition:
			transform 300ms ease,
			-webkit-transform 300ms ease;
	}

	.card-contact-link:hover {
		-webkit-transform: scale(1.1);
		-ms-transform: scale(1.1);
		transform: scale(1.1);
	}

	.card-2 {
		overflow: scroll;
		padding-right: 15px;
		padding-left: 15px;
		background-color: #ededed;
		-webkit-backface-visibility: hidden;
		backface-visibility: hidden;
		-webkit-perspective-origin: 50% 50%;
		perspective-origin: 50% 50%;
		-webkit-transform: perspective(1800px);
		transform: perspective(1800px);
		-webkit-transform-origin: 50% 0%;
		-ms-transform-origin: 50% 0%;
		transform-origin: 50% 0%;
		-webkit-transform-style: preserve-3d;
		transform-style: preserve-3d;
	}

	.expand-card-wrap {
		max-width: 300px;
		margin: 10px;
		-webkit-perspective: 1800px;
		perspective: 1800px;
		-webkit-transition: -webkit-transform 200ms ease;
		transition: -webkit-transform 200ms ease;
		transition: transform 200ms ease;
		transition:
			transform 200ms ease,
			-webkit-transform 200ms ease;
	}
	.team-member-shot {
		width: 100px;
		height: 100px;
		margin-right: 20px;
		border-top-left-radius: 2px;
		border-bottom-left-radius: 2px;
		background-image: url('../images/63c19346651016427af35392_alvin-mahmudov-9_XfcBxf_uo-unsplash.jpg');
		background-position: 0px 0px;
		background-size: cover;
		background-repeat: no-repeat;
	}

	.team-member-shot.caper {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		margin-right: 15px;
		-webkit-box-flex: 0;
		-webkit-flex: 0 0 auto;
		-ms-flex: 0 0 auto;
		flex: 0 0 auto;
		background-image: url('../images/63c193903eb65926ca2888be_foto-sushi-128246%20%281%29.jpg');
		background-position: 55% 43%;
		background-size: cover;
		background-repeat: no-repeat;
	}
	.expand-card-wrap:hover {
		-webkit-transform: scale(1.03);
		-ms-transform: scale(1.03);
		transform: scale(1.03);
	}
	.card-1 {
		position: relative;
		z-index: 999;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		padding-right: 11px;
		-webkit-box-pack: start;
		-webkit-justify-content: flex-start;
		-ms-flex-pack: start;
		justify-content: flex-start;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
		border-radius: 2px;
		background-color: #ededed;
		cursor: pointer;
	}
	@media screen and (min-width: 1280px) {
		.expand-card-wrap {
			max-width: 360px;
		}
	}

	@media screen and (max-width: 479px) {
		.card-1 {
			-webkit-box-align: center;
			-webkit-align-items: center;
			-ms-flex-align: center;
			align-items: center;
		}
		.team-member-shot {
			height: auto;
			-webkit-align-self: stretch;
			-ms-flex-item-align: stretch;
			-ms-grid-row-align: stretch;
			align-self: stretch;
		}
		.card-2 {
			padding-right: 5px;
			padding-left: 11px;
		}
	}
</style>
