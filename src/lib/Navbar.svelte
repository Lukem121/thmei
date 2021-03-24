<script>
	import Hamburger from './Hamburger.svelte'
    import logo from '../assets/logo-light.svg';
	export let sidebar = false
</script>

<header class="text-gray-600 body-font">
    <div class="container md:mx-auto px-6 mt-6 flex justify-between items-center  md:flex-wrap">
        <a href="/" class="flex justify-center items-center  md:mb-0">
            <img src={logo} alt="">
            <span class="ml-3 text-gray-900 font-bold text-3xl">Thmei</span>
        </a>
        <nav class="hidden md:mr-auto md:ml-4 md:py-1 md:pl-4 md:border-l md:border-gray-400 md:flex flex-wrap  items-center text-base justify-center">
            <a href="#services" class="mr-5 hover:text-gray-900">Services</a>
            <a href="#pricing" class="mr-5 hover:text-gray-900">Pricing</a>
            <a href="#about" class="mr-5 hover:text-gray-900">About</a>
            <a href="#testimonials" class="mr-5 hover:text-gray-900">Testimonials</a>
        </nav>
        <div class="md:hidden flex justify-center items-center">
            <Hamburger bind:open={sidebar}/>
        </div>
        <a href="#contact" class="hidden md:inline-flex items-center bg-gray-100 border-0 py-1 px-3 focus:outline-none hover:bg-gray-200 rounded text-base mt-4 md:mt-0">Get in touch
            <svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 ml-1" viewBox="0 0 24 24">
              <path d="M5 12h14M12 5l7 7-7 7"></path>
            </svg>
        </a>
    </div>
  </header>