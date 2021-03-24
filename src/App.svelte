<script>
  import './lib/TailwindCSS.svelte'
  import Navbar from './lib/Navbar.svelte'
  import Sidebar from './lib/Sidebar.svelte'
  import BackToTop from './lib/BackToTop.svelte'
  import Main from './sections/Main.svelte';
  import Pricing from './sections/Pricing.svelte';
  import Statistics from './sections/Statistics.svelte';

  let open = false
</script>

<BackToTop />
<Sidebar bind:open/>
<Navbar bind:sidebar={open}/>
<Main />
<Pricing />
<Statistics />