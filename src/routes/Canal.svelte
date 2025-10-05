<script>
	import bodega from '$lib/assets/bodega.avif';
</script>

<article id="canal" class="grid items-end bg-cream md:grid-cols-2">
	<div class="order-2 flex flex-col gap-6 px-6 py-12 md:order-1 md:gap-12 md:p-12">
		<h1
			class="text-4xl leading-[0.9] tracking-tight text-orange sm:text-5xl md:text-6xl lg:text-9xl"
		>
			Nuestro Canal
		</h1>
		<p class="max-w-130 leading-[1.5] text-pretty text-blue sm:text-[19px] md:text-[21px]">
			Trabajarás en el <strong class="text-orange">canal tradicional</strong>, atendiendo clientes
			de una ruta asignada. Para hacerlo fácil y organizado, tendrás una
			<strong class="text-orange">app que te muestra tu recorrido diario</strong>, con cada punto
			que debes visitar. Así, no tienes que preocuparte por buscar clientes: tú solo sigues la ruta
			y te enfocas en vender, mientras nosotros te damos todas las herramientas.
		</p>
	</div>
	<img
		src={bodega}
		alt="Bodega de alimentos"
		class="order-1 aspect-square w-full md:order-2 md:aspect-auto md:h-[100svh]"
	/>
</article>
