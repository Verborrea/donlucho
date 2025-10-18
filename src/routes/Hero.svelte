<script>
	import hero from '$lib/assets/hero.avif';
	import { Megaphone } from 'lucide-svelte';
	import { getContext } from 'svelte';

	const openDialog = getContext('openDialog');
</script>

<article class="relative grid items-end bg-orange text-cream md:grid-cols-2">
	<img
		src={hero}
		alt="Bodega de alimentos"
		class="order-2 aspect-square h-full w-full md:order-1 md:aspect-auto md:h-[100svh]"
	/>
	<div class="order-1 flex flex-col gap-6 px-6 py-8 md:order-2 md:items-start md:gap-8 md:p-12">
		<h1 class="text-4xl leading-[0.9] tracking-tight sm:text-5xl md:text-6xl lg:text-[100px]">
			Sobre el Trabajo
		</h1>
		<p class="max-w-130 leading-[1.5] text-pretty text-blue sm:text-[19px] md:text-[20px]">
			Estamos en busca de <strong class="font-semibold text-cream">vendedores motorizados</strong>
			para unirte a nuestro equipo comercial. Es un trabajo de
			<strong class="font-semibold text-cream">medio tiempo con horario flexible</strong>, ideal
			para quienes buscan generar ingresos extra o estabilidad
			<strong class="font-semibold text-cream">sin necesidad de experiencia</strong> previa.Nosotros
			te capacitamos y te damos una cartera de clientes lista para empezar.
		</p>
		<button type="button" onclick={openDialog} class="btn bg-blue hover:text-white">Postular</button
		>
	</div>
	<section
		class="absolute right-6 bottom-12 left-0 rounded-r-2xl bg-cream p-4 text-blue md:max-w-1/2 md:rounded-r-full md:p-6"
	>
		<div class="hidden items-center gap-6 md:flex">
			<Megaphone class="shrink-0 text-orange md:size-20" />
			<div class="space-y-2">
				<h1 class="text-xl text-orange md:text-2xl">Requisito importante:</h1>
				<p class="md:text-lg">
					Para este puesto necesitas tener tu <strong class="text-orange">propia moto</strong>. Es
					lo único que pedimos… ¡del resto ya nos encargamos nosotros!
				</p>
			</div>
		</div>
		<div class="flex flex-col gap-2 text-sm md:hidden">
			<div class="flex items-center gap-2">
				<Megaphone class="size-4 shrink-0 text-orange" strokeWidth={2.5} />
				<h1 class="text-base text-orange">Requisito importante:</h1>
			</div>
			<p>
				Para este puesto necesitas tener tu <strong class="text-orange">propia moto</strong>. Es lo
				único que pedimos… ¡del resto nos encargamos nosotros!
			</p>
		</div>
	</section>
</article>
