<script>
	export let open = false
</script>

<button class="text-gray-800 hover:text-black cursor-pointer mr-4 border-none focus:outline-none" class:open on:click={() => open = !open}>
	<svg width=32 height=24>
		<line id="top"    x1=3 y1=3  x2=29 y2=3  />
		<line id="middle" x1=3 y1=12 x2=29 y2=12 />
		<line id="bottom" x1=3 y1=21 x2=29 y2=21 />
	</svg>
</button>

<style>
	svg {
		min-height: 24px;
		transition: transform 0.3s ease-in-out;
	}
	
	svg line {
		stroke: black;
        stroke-linecap: round;
		stroke-width: 5;
		transition: transform 0.3s ease-in-out
	}
	
	button {
		z-index: 20;
	}
	
	.open svg {
		transform: scale(0.9)
	}
	
	.open #top {
		transform: translate(6px, 0px) rotate(45deg)
	}
	
	.open #middle {
		opacity: 0;
	}
	
  	.open #bottom {
		transform: translate(-12px, 9px) rotate(-45deg)
	}
</style>