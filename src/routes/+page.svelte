<script>
	import Beneficios from './Beneficios.svelte';
	import Canal from './Canal.svelte';
	import Hero from './Hero.svelte';
	import Productos from './Productos.svelte';
	import { getContext } from 'svelte';

	const openDialog = getContext('openDialog');
</script>

<section class="min-h-screen content-end bg-blue py-8 text-cream md:py-16">
	<div class="mx-auto flex max-w-7xl flex-col gap-6 px-6 md:items-start">
		<p class="text-xl font-bold md:text-2xl">BIENVENIDO A RINDE+</p>
		<h1
			class="max-w-2xl text-5xl leading-[0.9] tracking-tight text-pretty sm:text-6xl md:text-7xl lg:text-8xl"
		>
			Donde tu esfuerzo rinde
		</h1>
		<p class="max-w-md md:text-xl">
			Aquí, el esfuerzo se reconoce y las metas se cumplen. ¿Te animas a intentarlo?
		</p>
		<button type="button" onclick={openDialog} class="btn">Postula aquí</button>
	</div>
</section>
<Hero />
<Beneficios />
<Canal />
<Productos />

<style>
	section {
		background-image: url('/bg.avif');
		background-position: center;
		background-size: cover;
		background-repeat: no-repeat;
	}
</style>
