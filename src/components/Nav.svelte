<!--<nav class="bg-white shadow-lg">
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
</nav> -->

<script>
	let hiddenEl;
	function openButton () {
		hiddenEl.classList.toggle("hidden");
	}
</script>


<nav class="bg-white border-gray-200 px-2 sm:px-4 py-2.5 rounded dark:bg-gray-900">
  <div class="container flex flex-wrap justify-between items-center mx-auto">
    <a href="/" class="flex items-center">
        <!-- <img src="" class="mr-3 h-6 sm:h-9" alt=""> -->
        <span class="self-center text-xl font-semibold whitespace-nowrap dark:text-white"> PlasthicSlash </span>
    </a>
    <button on:click={openButton} data-collapse-toggle="navbar-default" type="button" class="inline-flex items-center p-2 ml-3 text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600" aria-controls="navbar-default" aria-expanded="false">
      <span class="sr-only">Open main menu</span>
      <svg class="w-6 h-6" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z" clip-rule="evenodd"></path></svg>
    </button>
    <div bind:this={hiddenEl} class="hidden w-full md:block md:w-auto" id="navbar-default">
      <ul class="flex flex-col p-4 mt-4 bg-gray-50 rounded-lg border border-gray-100 md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">
        <li>
          	<a href="#" class="font-semibold hover:text-purple-500 transition duration-300 block py-2 pr-4 pl-3 text-white bg-blue-700 rounded md:bg-transparent md:text-blue-700 md:p-0 dark:text-white" aria-current="page">
				Home
			</a>
        </li>
        <li>
          	<a href="about" class="nav-elements">
				About
			</a>
        </li>
        <li>
          	<a href="discography" class="nav-elements">
				Discography
			</a>
        </li>
        <li>
          	<a href="news" class="nav-elements">
				News
			</a>
        </li>
        <li>
          	<a href="contact" class="nav-elements">
				Contact
			</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
