<script lang="ts">
import slash from "images/slash-03.jpg";
</script>

<style>
	.entrance-image {
		/* background: url("images/slash-02.jpg");  */
		position: relative;
		text-align: right;
		color: white;
	}

	.social-links {
		position: absolute;
		top: 50%;
		left: 93%;
		/* transform: translate(-50%, -90%); */
	}
</style>

<svelte:head>
	<title>PlasthicSlash Landing Page</title>
</svelte:head>

<div></div>
<section class="entrance-msg hidden md:block w-full md:w-1/2 p-5 md:text-left">
	Lorem ipsum dolor sit amet consectetur, adipisicing elit. Repudiandae nisi, dignissimos vero natus exercitationem explicabo laborum quasi saepe quis dolores unde repellendus officia officiis repellat laudantium quaerat totam, veritatis dolore sed non porro. Assumenda aspernatur nihil iusto est molestias qui.
</section>

<section class="entrance-image h-screen hidden md:block w-full md:w-1/2 p-5">
	<img 
		src={slash} 
		class="max-w-full"
	/>
	<div class="social-links">
		<div>
			<a href="https://www.facebook.com/plasthic.plasthic.3">
				<img 
					src="https://github.com/devicons/devicon/blob/master/icons/facebook/facebook-original.svg"
				/>
			</a>
			<!-- twitter-->
			<a href="https://www.twitter.com/plasthic.plasthic.3">
				<img 
					src="https://github.com/devicons/devicon/blob/master/icons/facebook/facebook-original.svg"
				/>
			</a>
			<!-- instagram-->
			<a href="https://www.instagram.com/plasthic.plasthic.3">
				<img 
					src="https://github.com/devicons/devicon/blob/master/icons/facebook/facebook-original.svg"
				/>
			</a>
		</div>
	</div>
</section>