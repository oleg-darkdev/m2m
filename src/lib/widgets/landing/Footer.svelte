<script lang="ts">
	// import Copy from "carbon-icons-svelte/lib/Copy.svelte";

	import { socialLinks, donateLinks, cryptoLinks, navigationLanding } from '$sharedData';
	import { CryptoLinkFooter } from '$sharedUi';
	// import {  } from '$entities'
</script>

<footer class="swell-footer">
	<div class="media-footer-wrap">
		<!-- 			class="footer-logo"
 -->
		<img src="images/text-logo-light.svg" alt="logotype" class="mt-20 md:mt-0 lg:mt-0" />
		<div class="footer-top-section">
			<h3 class="media-footer-header">ПРИВЕТ!</h3>
			<h4 class="footer-subheading">Поддержи нас</h4>
			<!-- <div class="footer-button-wrap">
				<a href="tel:" class="icon-button-2 rotate-icon w-inline-block">
					<div class="button-icon-outline-2">
						<img src="images/icons/phone.svg" width="58" alt="" class="button-icon-2" />
					</div>
					<div class="icon-button-text-2">000.000.00.00</div>
				</a>
				<a href="mailto:" class="icon-button-2 rotate-icon w-inline-block">
					<div class="button-icon-outline-2">
						<img src="images/icons/envelope-alt.svg" width="58" alt="" class="button-icon-2" />
					</div>
					<div class="icon-button-text-2 address">loremimpsum@mail.com</div>
				</a>
			</div> -->
		</div>
		<div class="footer-columns">
			<!-- <div class="footer-column">
				<h5 class="footer-column-header">Навигация</h5>
				<div class="long-button-wrap">
					{#each navigationLanding as { title, link }}
						<a href={link} class="long-button w-inline-block">
							<div class="long-button-underlay"></div>
							<div class="long-button-info">
								<div class="long-button-title">{title}</div>
								<div class="long-button-link-wrap"> -->
			<!-- <div class="long-button-link-txt">{link}</div> -->
			<!-- <img src="images/icons/link.svg" loading="lazy" alt="" class="long-button-icon" />
								</div>
							</div>
						</a>
					{/each}
				</div>
			</div> -->
			<div id="donate" class="footer-column">
				<div class="mb-10">
					<h5 class="footer-column-header">Поддержать проект</h5>
					<div class="long-button-wrap">
						{#each donateLinks as { platform, url, shortUrl }}
							<a href={url} target="_blank" class="long-button w-inline-block">
								<div class="long-button-underlay"></div>
								<div class="long-button-info">
									<div class="long-button-title">{platform}</div>
									<div class="long-button-link-wrap">
										<div class="long-button-link-txt truncated-shorturl">{shortUrl}</div>
										<img
											src="images/icons/arrow-right-top.svg"
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

				<!-- <div>
					<h5 class="footer-column-header">Для криптовалют</h5>
					<div id="donate-crypto" class="long-button-wrap">
						{#each cryptoLinks as link (link.id)}
							<CryptoLinkFooter {link} />
						{/each}
					</div>
				</div> -->
			</div>
			<div class="footer-column">
				<div>
					<h5 class="footer-column-header">Для криптовалют</h5>
					<div id="donate-crypto" class="long-button-wrap">
						{#each cryptoLinks as link (link.id)}
							<CryptoLinkFooter {link} />
						{/each}
					</div>
				</div>
			</div>

			<div class="footer-column" id="contact">
				<h5 class="footer-column-header">Оффициальные аккаунты</h5>
				<div class="long-button-wrap">
					{#each socialLinks as { platform, url, shortUrl }}
						<a href={url} target="_blank" class="long-button w-inline-block">
							<div class="long-button-underlay"></div>
							<div class="long-button-info">
								<div class="long-button-title">{platform}</div>
								<div class="long-button-link-wrap">
									<div class="long-button-link-txt truncated-shorturl">{shortUrl}</div>
									<img
										src="images/icons/arrow-right-top.svg"
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
		<div class="footer-copyright-section">
			<a href="/" class="bleh-img-link w-inline-block"></a>
			<div class="footer-copyright">
				© <span id="year">2020-2025</span>
				Минута в минуту
			</div>
		</div>
	</div>
</footer>

<style lang="postcss">
	.media-footer-header {
		-webkit-text-fill-color: transparent;
		-webkit-background-clip: text;
		-webkit-text-stroke: 1px #fff;
	}
</style>
