<script>
	import ContentHeader from '$lib/ContentLastest.svelte';
	import ContentSkill from '$lib/ContentSkill.svelte';
	import Hero from '$lib/Hero.svelte';
	import Projects from '$lib/Projects.svelte';
</script>

<svelte:head>
	<title>maxmurr</title>
	<meta name="description" content="Maxmurr portfolio app" />
	<link rel="icon" type="image/png" href="/favicon.png" />
</svelte:head>

<Hero />
<ContentHeader />
<Projects />
<ContentSkill />
