<script>
	import * as animateScroll from "svelte-scrollto";

	export let open = false

	const navigate = (val) => {
		open = !open;
		animateScroll.scrollTo({element: val, delay: 350})
	}
</script>

<aside class="absolute w-full h-full z-10 bg-white border-r-2 shadow-lg" class:open>
	<nav class="flex flex-col justify-center items-center p-12 text-xl">
		<button on:click={() => navigate("#about")} class="mr-5 hover:text-gray-900">About</button>
        <button on:click={() => navigate("#pricing")} class="mr-5 hover:text-gray-900">Pricing</button>
        <button on:click={() => navigate("#services")} class="mr-5 hover:text-gray-900">Services</button>
        <button on:click={() => navigate("#testimonials")} class="mr-5 hover:text-gray-900">Testimonials</button>
	</nav>
</aside>

<style>
	aside {
		left: -100%;
		transition: left 0.3s ease-in
	}
	
	.open {
		left: 0;
	}
</style>