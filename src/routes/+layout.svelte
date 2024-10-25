<script>
	import { browser } from '$app/environment';
	import { page } from '$app/stores';
	import { webVitals } from '$lib/vitals';
	import './App.css';

	/** @type {import('./$types').LayoutServerData} */
	export let data;

	$: if (browser && data?.analyticsId) {
		webVitals({
			path: $page.url.pathname,
			params: $page.params,
			analyticsId: data.analyticsId
		});
	}
</script>

<div class="app">
	<main>
		<div class="body-container">
		  <header class="header-container">
			<div class="logo-container">
				  <img src="./Image/logo.svg" alt="logo">
				  <h3 class="logo-text">Logo</h3>
			</div>
			<div class="header-burger">
			  <!-- svelte-ignore a11y-click-events-have-key-events -->
			  <!-- svelte-ignore a11y-no-static-element-interactions -->
			  <div class="menu-btn" on:click={toggleMenu}>
				<span class="bar"></span>
				<span class="bar"></span>
				<span class="bar"></span>
			  </div>
			</div>
	  
			<!-- Correct class binding without using template literals -->
			<div class="header__nav">
			  <nav class="nav">
				<ul class="nav__list">
				  <li class="nav__list_item"><a class="nav__link" href="/About">About</a></li>
				  <li class="nav__list_item"><a class="nav__link" href="/Services">Services</a></li>
				  <li class="nav__list_item"><a class="nav__link" href="/Team">Team</a></li>
				  <li class="nav__list_item"><a class="nav__link" href="/Contact">Contact</a></li>
				</ul>
			  </nav>
			</div>
		  </header>
		  <div class="main-body-container">
			<div class="body-container-first">
				<div class="container-first-main-text">The dawn of a new era in health is here</div>
				<div class="conteiner-first-info-text">Lorem ipsum dolor sit amet consectetur. Quam ut consequat at a. Diam lacus platea orci vel elit blandit facilisis </div>
				<div class="container-first-button">Join now</div>
			</div>
			<div class="body-container-second">
				<div class="container-second-images first" ></div>
				<div class="container-second-images second" ></div>
			</div>
		  </div>
		</div>
		<div class="information-container-section">
			<div class="info-main-container">
				<div class="info-box-first">
					<div class="info-box-text-container">
						<div class="text-container-info">Wellbeing is well doing</div>
					</div>
					<div class="info-box-first-infos-container">
						<div class="infos-container-first">
							<img class="info-image" src="./Image/info-image.svg" alt="">
							<div class="infos-container-text">Lorem ipsum dolor sit amet consectetur. Quam ut consequat at a. Diam lacus platea orci vel elit.</div>
						</div>
						<div class="infos-container-first">
							<img class="info-image" src="./Image/info-image.svg" alt="">
							<div class="infos-container-text">Lorem ipsum dolor sit amet consectetur. Quam ut consequat at a. Diam lacus platea orci vel elit.</div>
						</div>
					</div>
				</div>
				<div class="info-box-second">
					<img src="./Image/girl-joga.svg" alt="girl">
				</div>
			</div>
		</div>
		<div class="flovers-section-container">
			<div class="flover-section-first">
				<div class="flover-image"></div>
			</div>
			<div class="flover-section-second">
				<div class="section-second-first-block">
					<h1 class="second-first-block-name">Fresh organic produce</h1>
					<h3 class="second-first-block-text">Lorem ipsum dolor sit amet consectetur. Quam ut consequat at a. Diam lacus platea orci vel elit blandit facilisis enim risus. Ut tristique eget integer odio nec vulputate consequat. Elit mattis ac in amet sit viverra.</h3>
				</div>
				<div class="section-second-second-block">
					<div class="second-block-box">
						<div class="block-help-box">
							<img src="./Image/flover-image.svg" alt="" class="box-img">
							<h3 class="box-text">Lorem ipsum dolor sit amet consectetur. Quam ut consequat at a. Diam lacus platea</h3>
						</div>
						<div class="block-help-box">
							<img src="./Image/flover-image.svg" alt="" class="box-img">
							<h3 class="box-text">Lorem ipsum dolor sit amet consectetur. Quam ut consequat at a. Diam lacus platea</h3>
						</div>
						<div class="block-help-box">
							<img src="./Image/flover-image.svg" alt="" class="box-img">
							<h3 class="box-text">Lorem ipsum dolor sit amet consectetur. Quam ut consequat at a. Diam lacus platea</h3>
						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="information-container-section">
			<div class="info-main-container eat">
				<div class="info-box-second eat">
					<img src="./Image/coctail-image.svg" alt="coctail">
				</div>
				<div class="info-box-first">
					<div class="info-box-text-container">
						<div class="text-container-info">You are what you eat</div>
					</div>
					<div class="info-box-first-infos-container">
						<div class="infos-container-first">
							<img class="info-image" src="./Image/eat-image.svg" alt="eat">
							<div class="infos-container-text eat">Lorem ipsum dolor sit amet consectetur. Quam ut consequat at a. Diam lacus platea orci vel elit.</div>
						</div>
						<div class="infos-container-first">
							<img class="info-image" src="./Image/eat-image.svg" alt="eat">
							<div class="infos-container-text eat">Lorem ipsum dolor sit amet consectetur. Quam ut consequat at a. Diam lacus platea orci vel elit.</div>
						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="link-section-container">
			<div class="link-section-block">
				<img src="./Image/white-icon-eat-section.svg" alt="eat" class="link-section-image">
				<h1 class="link-section-name">Wellbeing starts with well doing</h1>
				<h3 class="link-section-text">Lorem ipsum dolor sit amet consectetur. Quam ut consequat at a. Diam lacus platea orci vel elit blandit facilisis enim risus. Ut tristique eget integer odio nec.</h3>
				<div class="link-section-button">Join now</div>
			</div>
		</div>
		<div class="icons-section-container">
			<div class="icons-container-box">
				<img src="./Image/icons-section-image.svg" alt="icons" class="icons-image-set">
				<img src="./Image/icons-section-image.svg" alt="icons" class="icons-image-set">
				<img src="./Image/icons-section-image.svg" alt="icons" class="icons-image-set">
				<img src="./Image/icons-section-image.svg" alt="icons" class="icons-image-set">
			</div>
		</div>
		<div class="footer-section-container">
			<div class="footer-main-container">
				<h3 class="logo-text footer"><img src="./Image/footer-logo.svg" alt=" "class="footer-logo">Logo</h3>
				<div class="services-section">
					<li class="nav__list_item footer"><a class="nav__link footer">About</a></li>
					<li class="nav__list_item"><a class="nav__link footer">Services</a></li>
					<li class="nav__list_item"><a class="nav__link footer">Team</a></li>
					<li class="nav__list_item"><a class="nav__link footer">Contact</a></li>
				</div>
				<div class="logos-section">
					<img class="logos-icons first" src="./Image/twitter.svg" alt="icons">
					<img class="logos-icons second" src="./Image/insta.svg" alt="icons">
					<img class="logos-icons third" src="./Image/in.svg" alt="icons">
					<img class="logos-icons fourth" src="./Image/facebook.svg" alt="icons">
				</div>
			</div>
		</div>
	  </main>
</div>


