<script>
	import Footer from '../../lib/Footer.svelte';
	import Header from '../../lib/Header.svelte';
</script>

<body>
	<div class="app">
		<Header />
		<main>
			<slot />
		</main>
		<Footer />
	</div>
</body>
<!-- <Header />
<slot/>
<Footer /> -->
