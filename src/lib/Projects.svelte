<script>
	const projects = [
		{
			title: 'Talingchan Fertilizer',
			description: 'Talingchan Fertilizer',
			image:
				'https://cdn.discordapp.com/attachments/1034424462323490866/1063526215014690938/Screenshot_50.png',
			link: '',
		},
		{
			title: 'My Portfolio',
			description: 'My Portfolio',
			image:
				'https://media.discordapp.net/attachments/1034424462323490866/1063495470481158184/Screenshot_46.png?width=1202&height=676',
			link: '',
		},
		{
			title: 'McStore',
			description: 'McStore',
			image:
				'https://cdn.discordapp.com/attachments/1034424462323490866/1063498231335616605/Screenshot_48.png',
			link: '',
		},
		{
			title: 'Zoolooalpaca',
			description: 'Zoolooalpaca',
			image:
				'https://cdn.discordapp.com/attachments/1034424462323490866/1063529439058735166/Capture.PNG',
			link: '',
		},
	];
</script>

<section class="bg-base-100">
	<div
		class="px-8 lg:px-16 pt-0 pb-12 mx-auto lg:max-w-screen-xl sm:max-w-xl md:max-w-full sm:px-12 md:pb-24"
	>
		<div
			class="grid gap-x-8 gap-y-12 sm:gap-y-16 md:grid-cols-2 lg:grid-cols-3"
		>
			{#each projects as project}
				<!-- Card -->
				<div class="relative hover:scale-105 transition-all">
					<a href={project.link} class="block overflow-hidden group">
						<img
							src={project.image}
							class="max-w-full rounded-lg shadow-2xl "
							alt="default"
						/>
					</a>
					<div class="relative mt-5 text-center">
						<a href={project.link} class="block mb-4">
							<h2
								class="text-2xl font-bold leading-5transition-colors duration-200 hover:text-deep-purple-accent-700"
							>
								{project.title}
							</h2>
						</a>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>
