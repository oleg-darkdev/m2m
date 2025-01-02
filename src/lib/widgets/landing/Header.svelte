<script lang="ts">
	// import {  } from '$shared';
	// import {  } from '$widgets';
	// import {  } from '$entities';
	import { navigationMenu } from '$sharedData';

	let { showMenu } = $state(false);
</script>

<header class="page-nav-header overflow-hidden">
	<!-- nav-header-wrap -->
	<div class="flex w-full justify-between">
		<div class="nav-header-wrap">
			<a href="/" target="_blank" class="minim-link w-inline-block fixed left-0 top-0 z-40"
				><img src="images/logo-header.svg" loading="lazy" class=" h-20 w-20 lg:h-40 lg:w-40" /></a
			>
			<!-- width="120" alt="" sizes="120px" -->
			<a href="/" target="_blank" class="ml-20 h-12 w-40 md:ml-32 lg:ml-32"
				><img src="images/text-logo-light.svg" loading="lazy" alt="" /></a
			>
			<!-- <h1 class="simple-nav-header pl-32">Минута в минуту</h1> -->
		</div>

		<!-- <div class="top-navigation">
			<div class="app-nav-btn" onclick={() => (showMenu = !showMenu)}>
				{#if showMenu}
					<div class="div-block-20">
						<div class="div-block-21"></div>
						<div class="div-block-21-copy"></div>
					</div>
				{:else}
					<div class="div-block-18">
						<div class="div-block-19"></div>
						<div class="div-block-19-copy"></div>
						<div class="div-block-19-copy-copy"></div>
					</div>
				{/if}
			</div>
			{#if showMenu}
				<div class="app-nav-menu">
					<div class="app-menu-link-wrap">
						{#each navigationMenu as { title, link }}
							<a href={link} target="_blank" class="app-menu-link">{title}</a>
						{/each}
					</div>
				</div>
			{/if}
		</div> -->
	</div>
</header>

<style lang="postcss">
	.top-navigation {
		z-index: 20;
		position: static;
	}
	.page-nav-header {
		position: absolute;
		left: 0%;
		top: 0%;
		right: 0%;
		bottom: auto;
		z-index: 10;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		width: 100vw;
		height: 13vh;
		padding-right: 2.4rem;
		padding-left: 2.4rem;
		-webkit-box-pack: justify;
		-webkit-justify-content: space-between;
		-ms-flex-pack: justify;
		justify-content: space-between;
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
		border-bottom: 1px solid #313131;
		background-color: #000;
	}

	.nav-header-wrap {
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		/* width: 100vw; */
		-webkit-box-align: center;
		-webkit-align-items: center;
		-ms-flex-align: center;
		align-items: center;
	}

	.app-menu-link {
		color: var(--mid-gray);
		margin-bottom: 20px;
		font-size: 2rem;
		transition:
			transform 0.2s,
			opacity 0.2s;
	}

	.app-menu-link:hover {
		color: var(--white);
		transform: scale(1.05);
	}

	.app-menu-link-wrap {
		flex-direction: column;
		justify-content: flex-end;
		align-items: flex-end;
		display: flex;
	}

	.app-nav-menu {
		z-index: 98;
		background-color: #000;
		flex-direction: column;
		justify-content: center;
		align-items: flex-end;
		width: 50vw;
		height: 100vh;
		padding-left: 7%;
		padding-right: 7%;
		display: flex;
		position: fixed;
		top: 0%;
		bottom: 0%;
		left: auto;
		right: 0%;
	}
	.div-block-21 {
		background-color: #fff;
		width: 100%;
		height: 3px;
		position: absolute;
		transform: rotate(0);
	}
	.div-block-21-copy {
		background-color: #fff;
		width: 3px;
		height: 100%;
		position: absolute;
		transform: rotate(0);
	}

	.div-block-19-copy-copy {
		background-color: #fff;
		width: 100%;
		height: 3px;
		position: relative;
	}

	.div-block-19-copy {
		background-color: #fff;
		width: 65%;
		height: 3px;
		position: relative;
	}

	.div-block-18 {
		flex-direction: column;
		justify-content: space-between;
		align-items: flex-end;
		display: flex;
		position: absolute;
		top: 0%;
		bottom: 0%;
		left: 0%;
		right: 0%;
	}

	.div-block-19 {
		background-color: #fff;
		width: 35%;
		height: 3px;
		position: relative;
	}

	.div-block-20 {
		justify-content: center;
		align-items: center;
		width: auto;
		height: auto;
		display: flex;
		position: absolute;
		top: 0%;
		bottom: 0%;
		left: 0%;
		right: 0%;
		transform: rotate(45deg);
	}
	.app-nav-btn {
		z-index: 99;
		cursor: pointer;
		justify-content: center;
		align-items: center;
		width: 30px;
		height: 30px;
		transition: transform 0.2s;
		display: flex;
		position: relative;
	}

	.app-nav-btn:hover {
		transform: scale(0.9);
	}

	@media screen and (max-width: 991px) {
		.app-nav-btn {
			width: 25px;
			height: 25px;
		}
		.app-nav-menu {
			width: 65vw;
		}
	}

	@media screen and (max-width: 767px) {
		.app-nav-btn {
			top: 2%;
			right: 4%;
		}
		.app-nav-menu {
			width: 100vw;
		}

		.app-menu-link {
			font-size: 2.5rem;
		}
		.page-nav-header {
			height: 72px;
		}
	}

	@media screen and (max-width: 479px) {
		.app-nav-btn {
			width: 20px;
			height: 20px;
		}
		.page-nav-header {
			padding-right: 1rem;
			padding-left: 1rem;
		}
		.nav-header-wrap {
			display: -webkit-box;
			display: -webkit-flex;
			display: -ms-flexbox;
			display: flex;
			-webkit-box-align: center;
			-webkit-align-items: center;
			-ms-flex-align: center;
			align-items: center;
		}
		.app-nav-menu {
			transform: translate(100%);
		}
	}
</style>
