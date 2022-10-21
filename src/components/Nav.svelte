<script lang="ts">
	export let segment: string;
	let overlayEl;
	let mobileMenuEl;

	function closeOverlay () {
		// overlayEl.style.height = "0%";
		overlayEl.classList.remove("w-0", "h-0", "opacity-0");
		overlayEl.classList.add("w-screen", "h-screen", "opacity-95");
	}

	function openOverlay () {
		mobileMenuEl.classList.toggle("hidden");
		// overlayEl.style.height = "100%";
		overlayEl.classList.add("w-0", "h-0", "opacity-0");
		overlayEl.classList.remove("w-screen", "h-screen", "opacity-95");
	}	
</script>

<style>
/*
	.overlay-nav {
		height: 100vh;
		width: 0;
		position: fixed;
		z-index: 1;
		left: 0;
		top: 0;
		background-color: rgb(0, 0, 0);
		background-color: rgba(0, 0, 0, .9);
		overflow-x: hidden;
		transition: .5s;
	}

	.overlay-nav-content {
		position: relative;
		top: 25%;
		width: 100%;
		text-align: center;
		margin-top: 30px;
	}

	.overlay-nav a {
		padding: 8px;
		text-decoration: none;
		font-size: 36px;
		color: #818181;
		display: block;
		transition: .3s;
	}

	.overlay-nav a:hover, .overlay-nav a:focus {
		color: #f1f1f1;
	}

	.overlay-nav .close-overlay {
		position: absolute;
		top: 20px;
		right: 45px;
		font-size: 60px;
	} 

	@media screen and (max-height: 450px) {
		.overlay-nav a { font-size: 20px; }
		.overlay-nav .close-overlay {
			font-size: 40px;
			top: 15px;
			right: 35px;
		}
	}
	*/
	
</style>

<nav class="bg-white shadow-lg">
	<div class="max-w-6xl mx-auto px-4">
		<div class="flex justify-between">
			<div class="flex space-x-7">
				<a href="/" class="flex items-center py-4 px-2">
					/\
				</a>
			</div>
			<div class="hidden md:flex items-center space-x-1">
				<a href="/" class="py-4 px-2 text-gray-500 border-b-4 border-purple-500 font-semibold">
					Home
				</a>
				<a href="about" class="py-4 px-2 text-gray-500 font-semibold hover:text-purple-500 transition duration-300">
					About
				</a>
				<a href="discography" class="py-4 px-2 text-gray-500 font-semibold hover:text-purple-500 transition duration-300">
					Discography
				</a>
				<a href="contact" class="py-4 px-2 text-gray-500 font-semibold hover:text-purple-500 transition duration-300">
					Contact
				</a>
			</div>

			<div class="md:hidden flex items-center">
				<button class="outline-none menu-button px-5 bg-white-400 text-amber-500 text-xl duration-300" on:click={openOverlay}>
					<span class="text-2xl"> &#9776; </span>
				</button>
			</div>

			<div class="hidden mobile-menu" bind:this={mobileMenuEl}>
				<div id="overlay-nav" bind:this={overlayEl} class="fixed z-90 w-0 h-0 flex justify-center items-center bg-gray-900 opacity-o duration-700">

					<a href="javascript:void(0)" class="close-overlay fixed top-6 right-8 text-white hover:text-amber-600 text-7xl font-semibold-duration-300" on:click={closeOverlay}>
						&times;
					</a>
					<div class="overlay-nav-content flex flex-col text-white text-center text-xl font-light space-y-3">
						<a href="about" class=" hover:text-amber-500 duration-300">about</a>
						<a href="discography" class="uppercase hover:text-amber-500 duration-300">discography</a>
						<a href="contact" class="uppercase hover:text-amber-500 duration-300">contact</a>
						<a href="links" class=" hover:text-amber-500 duration-300">Links</a>
					</div>
				</div>
			</div>
		</div>
	</div>
</nav>