<script>
	const items = [
		{
			src: '/icons/html.svg',
			alt: 'HTML5',
		},
		{
			src: '/icons/css.svg',
			alt: 'CSS3',
		},
		{
			src: '/icons/js.svg',
			alt: 'JS',
		},
		{
			src: '/icons/ts.svg',
			alt: 'TS',
		},
		{
			src: '/icons/python.svg',
			alt: 'PYTHON',
		},
		{
			src: '/icons/node.svg',
			alt: 'NODE',
		},
		{
			src: '/icons/svelte.svg',
			alt: 'SvELTE',
		},
	];
</script>

<section class="h-auto bg-base-300">
	<div
		class="max-w-7xl mx-auto py-16 px-4 sm:py-24 sm:px-6 lg:px-8 text-center"
	>
		<p
			class="mt-1 text-4xl font-extrabold sm:text-5xl text-accent sm:tracking-tight lg:text-6xl"
		>
			My Skills
		</p>
		<p class="mt-2 text-lg text-center py-4">
			Check out a list of the coding languages I'm proficient in.
		</p>
		<div class="flex items-center justify-center">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				width="1em"
				height="1em"
				preserveAspectRatio="xMidYMid meet"
				viewBox="0 0 24 24"
				class="mt-1"
				><path
					fill="currentColor"
					d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm-.4 4.25l-7.07 4.42c-.32.2-.74.2-1.06 0L4.4 8.25a.85.85 0 1 1 .9-1.44L12 11l6.7-4.19a.85.85 0 1 1 .9 1.44z"
				/></svg
			>
			<h2 class="text-base font-semibold tracking-wide px-2">
				<a href="/" class="link link-hover text-info-content">maxmurr.m@gmail.com</a>
			</h2>
		</div>

		<div
			class="mb-8 md:mb-0 flex flex-row flex-wrap justify-center items-center col-span-3 px-8 py-12 sm:rounded-xl"
		>
			{#each items as item}
				<div
					class="p-1 m-8 rounded-full shadow-xl transition duration-150 ease-in-out hover:scale-105 cursor-pointer"
				>
					<img src={item.src} alt={item.alt} />
				</div>
			{/each}
		</div>
	</div>
</section>

<style></style>
