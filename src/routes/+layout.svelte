<script>
	import '../styles.css';
	import Footer from './Footer.svelte';
	import Header from './Header.svelte';
	export const prerender = true;
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

<style>
</style>
