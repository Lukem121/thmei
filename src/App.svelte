<script>
  import './lib/TailwindCSS.svelte'
  import Navbar from './lib/Navbar.svelte'
  import Sidebar from './lib/Sidebar.svelte'
  import BackToTop from './lib/BackToTop.svelte'
  import Main from './sections/Main.svelte';
  import Services from './sections/Services.svelte';
  import Pricing from './sections/Pricing.svelte';
  import Statistics from './sections/Statistics.svelte';
  import Footer from './sections/Footer.svelte';

  // Images
  import startup from './assets/startup.jpg';

  let open = false
</script>

<BackToTop />
<Sidebar bind:open/>
<Navbar bind:sidebar={open}/>
<Main />
<div class="mt-16">
  <img src={startup} class="object-cover object-top h-44 w-full" alt="">
</div>
<Services />
<Pricing />
<Statistics />
<Footer />