<script>
	import '../app.css';
</script>

<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous" />
	<link
		href="https://fonts.googleapis.com/css2?family=Manrope:wght@200..800&display=swap"
		rel="stylesheet"
	/>

	<title>Ukasyah • Full Stack Developer</title>
	<meta
		name="description"
		content="Full Stack Developer with a keen interest in solving real-world problems and building high-impact solutions."
	/>
</svelte:head>

<div class="px-5 md:px-6">
	<slot />
</div>
