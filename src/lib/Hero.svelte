<script>
	import ArrowDown from '$lib/ArrowDown.svelte';
</script>

<section
	class="relative md:flex flex-col items-center justify-center w-full px-8 bg-base-200 bg-cover min-w-screen "
>
	<div
		class="flex flex-col items-center justify-center mx-auto sm:p-6 xl:p-8 lg:flex-row lg:max-w-6xl lg:p-0 md:mt-16"
	>
		<div
			class="container relative z-20 flex flex-col w-full px-5 pb-1 md:mb-16 text-2xl lg:w-1/2 xl:pr-10 sm:items-center lg:items-start lg:mb-0  "
		>
			<h1
				class="relative z-20 text-5xl text-accent font-extrabold leading-none xl:text-6xl sm:text-center lg:text-left"
			>
				Hello there.
			</h1>
			<p
				class="relative z-20 block mt-6 text-base xl:text-xl sm:text-center lg:text-left"
			>
				I'm Max, a computer science student with a focus on full-stack
				development. My portfolio showcases my work and skills. I'm always
				looking to improve and take on new challenges. Thanks for visiting my
				portfolio!
			</p>
			<div class="relative flex flex-col md:flex-row mt-4 justify-center">
				<a
					href="/"
					class="p-5 flex light:text-white flex-1 w-full items-center self-start justify-center md:px-5 md:py-2 mt-5 text-base leading-tight transition duration-150 ease-in-out bg-primary font-semibold text-white border border-transparent rounded-full shadow lg:py-4 focus:outline-none focus:shadow-gray-NaN md:text-lg xl:text-xl xl:px-10 hover:bg-primary-focus"
					>Resume</a
				>
			</div>
		</div>
		<a href="https://github.com/zoolooalpaca/order-in">
			<div
				class="card flex-shrink-0 w-full max-w-lg shadow-2xl bg-base-100 transition duration-150 ease-in-out hover:scale-105 cursor-pointer hidden md:block"
			>
				<div class="absolute flex items-center justify-center w-full h-full">
					<span
						class="flex items-center justify-center w-20 h-20 bg-base-300 rounded-full shadow-2xl text-white"
					>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							class="h-6 w-6"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							stroke-width="2"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"
							/>
						</svg>
					</span>
				</div>
				<img
					src="https://cdn.discordapp.com/attachments/1034424462323490866/1063529439058735166/Capture.PNG"
					class="max-w-lg rounded-lg shadow-2xl "
					alt="default"
				/>
			</div>
		</a>
	</div>
	<div class="pt-8 flex justify-center">
		<button class="animate-bounce cursor-default">
			<ArrowDown />
		</button>
	</div>
	<!-- <hr class="w-[80rem] rounded border-1 border-base-content" /> -->
</section>
