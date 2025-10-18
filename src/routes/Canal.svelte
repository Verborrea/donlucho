<script>
	import bodega from '$lib/assets/bodega.avif';
	import { getContext } from 'svelte';

	const openDialog = getContext('openDialog');
</script>

<article id="canal" class="grid items-end bg-cream md:grid-cols-2">
	<div class="order-2 flex flex-col gap-6 px-6 py-12 md:order-1 md:items-start md:gap-10 md:p-12">
		<h1
			class="text-4xl leading-[0.9] tracking-tight text-orange sm:text-5xl md:text-6xl lg:text-8xl"
		>
			Nuestro Canal
		</h1>
		<p class="max-w-130 leading-[1.5] text-pretty text-blue sm:text-[19px] md:text-[21px]">
			Trabajarás en el <strong class="text-orange">canal tradicional</strong>, visitando a los
			clientes de una ruta asignada. Cada punto de tu recorrido estará en una
			<strong class="text-orange">app que te guía paso a paso</strong>, para que puedas concentrarte
			en lo más importante: construir una relación sólida con cada detallista. Tu labor no es solo
			vender, sino fortalecer el vínculo entre ellos y <strong class="text-orange">Rinde+</strong>,
			asegurando que se sientan acompañados, escuchados y atendidos. Nosotros te damos las
			herramientas; tú haces que la conexión suceda.
		</p>
		<button type="button" onclick={openDialog} class="btn">Postular</button>
	</div>
	<img
		src={bodega}
		alt="Bodega de alimentos"
		class="order-1 aspect-square w-full md:order-2 md:aspect-auto md:h-[100svh]"
	/>
</article>
