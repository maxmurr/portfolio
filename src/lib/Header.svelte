<!-- svelte-ignore a11y-missing-attribute -->
<script>
	import AnimatedHamburger from '../lib/AnimatedHamburger.svelte';
	
	export let open = false;
	export const onClick = () => {
		open = !open;
	};

	let previousY = 0
	let currentY = 0
	let y = 0
	let clientHeight = 1

	const deriveDiretion = ( y = 1) => {
		const direction = !previousY || previousY < y ? 'down' : 'up'
		previousY = y

		return direction
	}

	$: scrollDirection = deriveDiretion(currentY)
	$: offscreen = scrollDirection === 'down' && currentY > clientHeight * 4
</script>

<svelte:window bind:scrollY={y} />

<section class="bg-base-200/90 z-50 sticky top-0 backdrop-blur-sm transition-transform ease-in" class:motion-safe:-translate-y-full={offscreen}
bind:clientHeight={clientHeight}
>
	<nav
		class="relative py-6 md:py-3 px-6 mx-auto md:px-0 max-w-7xl md:flex md:justify-between md:items-center"
	>
		<div class="relative z-20 flex items-center justify-between">
			<div>
				<a
					class="text-xl font-bold md:text-2xl md:ml-4"
					href="/"
				>
					maxmurr
				</a>
			</div>

			<div class="flex">
				<button
					type="button"
					class="focus:outline-none focus:text-white md:hidden"
					aria-label="toggle menu"
				>
					<AnimatedHamburger width={40} {open} {onClick} />
				</button>
			</div>
		</div>
		<div
			class="left-0 z-10 items-center hidden justify-center w-full font-semibold select-none md:flex lg:absolute"
		>
			<div
				class="flex flex-col justify-center w-full mt-4 space-y-2 md:mt-0 md:flex-row md:space-x-6 lg:space-x-10 xl:space-x-16 md:space-y-0"
			>
				<a href="/" class="py-3 cursor-pointer hover:text-white">Home</a>
				<a href="#portfolio" class="py-3 cursor-pointer hover:text-white">Portfolio</a>
				<a href="/" class="py-3 cursor-pointer hover:text-white">Contact</a>
			</div>
		</div>
		<div
			class="relative z-20 flex-col justify-center pr-5 mt-4 space-y-8 md:pr-3 lg:pr-0 md:flex-row md:space-y-0 md:items-center md:space-x-6 md:mt-0 hidden md:flex"
		>
			<a href="/"
				class="py-3 btn bg-white rounded-full border-none transition ease-in-out hover:bg-white hover:text-black text-black flex-shrink-0 w-auto text-base font-semibold leading-5 text-left capitalize md:text-sm md:py-3 md:px-8 md:font-medium md:text-center md:mr-4"
				>Hire me</a
			>
		</div>
		{#if open}
			<div
				class="left-0 z-10 items-center justify-center w-full font-semibold select-none md:hidden lg:absolute flex"
			>
				<div
					class="flex flex-col justify-center w-full mt-4 space-y-2 md:mt-0 md:flex-row md:space-x-6 lg:space-x-10 xl:space-x-16 md:space-y-0"
				>
					<a href="/"class="py-3 cursor-pointer hover:text-white">Home</a>
					<a href="#portfolio"class="py-3 cursor-pointer hover:text-white">Portfolio</a>
					<a href="/" class="py-3 cursor-pointer hover:text-white">Contact</a>
					<a
						href="/"class="py-3 cursor-pointe btn bg-white capitalize hover:bg-white border-none rounded-full transition ease-in-out text-black"
						>Hire me</a
					>
				</div>
			</div>
		{/if}
	</nav>
</section>

<style>
</style>
