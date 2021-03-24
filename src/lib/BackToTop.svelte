<script>
    import * as animateScroll from "svelte-scrollto";
    import { fade } from 'svelte/transition';
    let scroll;
</script>

<svelte:window bind:scrollY={scroll}/>

{#if scroll > 10}
    <button transition:fade class="fixed z-10 bottom-0 right-0 m-6 md:m-10 py-3 px-4 rounded bg-indigo-500 hover:bg-indigo-600 text-white border-0 focus:outline-none text-base" on:click={() => animateScroll.scrollToTop()}>
        <i class="fas fa-arrow-up"></i>
    </button>
{/if}
