<script>
	import logo from '$lib/assets/logo.avif';

	let { openDialog } = $props();
</script>

<footer class="relative flex h-[100svh] flex-col bg-black px-6 text-white">
	<div class="flex grow flex-col items-center justify-center gap-6 text-center md:gap-12">
		<h1 class="text-3xl text-balance sm:text-4xl md:text-6xl">¡Únete a nuestro equipo!</h1>
		<button type="button" class="btn" onclick={openDialog}>Postula aquí</button>
	</div>
	<div
		class="absolute inset-0 top-auto flex flex-col items-center justify-between gap-6 p-8 sm:flex-row"
	>
		<img src={logo} alt="Logo de Don Luciano" width="200" />
		<p class="sm:text-lg md:text-xl">&copy; 2025 Don Luciano</p>
	</div>
</footer>

<style>
	footer {
		background-image: url('/footer.avif');
		background-position: center;
		background-size: cover;
		background-repeat: no-repeat;
	}
</style>
