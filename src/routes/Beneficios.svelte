<script>
	import b3 from '$lib/assets/b1.avif';
	import b1 from '$lib/assets/b2.avif';
	import b2 from '$lib/assets/b3.avif';
	import b4 from '$lib/assets/b4.avif';
</script>

<article id="beneficios" class="scroll-mt-14 bg-blue py-12 sm:py-18 md:py-24 hd:scroll-mt-24">
	<div class="mx-auto flex max-w-7xl flex-col gap-6 px-6 md:gap-12">
		<h1 class="text-center text-5xl text-cream sm:text-start md:text-6xl lg:text-8xl">
			Beneficios
		</h1>
		<div class="grid gap-4 text-center md:grid-cols-2 lg:grid-cols-4">
			<section class="bg-cream p-4.5 shadow-lg transition hover:rotate-5">
				<img src={b3} alt="Chico levantando una billetera" class="aspect-square" />
				<p class="grow">Sueldo fijo + comisiones</p>
			</section>
			<section class="bg-cream p-4.5 shadow-lg transition hover:rotate-5">
				<img src={b1} alt="Chico levantando una billetera" class="aspect-square" />
				<p class="grow">Horario flexible</p>
			</section>
			<section class="bg-cream p-4.5 shadow-lg transition hover:rotate-5">
				<img src={b2} alt="Chico levantando una billetera" class="aspect-square" />
				<p class="grow">Capacitación y cartera de clientes</p>
			</section>
			<section class="bg-cream p-4.5 shadow-lg transition hover:rotate-5">
				<img src={b4} alt="Chico levantando una billetera" class="aspect-square" />
				<p class="grow">Bono de gasolina para tu moto</p>
			</section>
		</div>
	</div>
</article>

<style>
	section {
		display: flex;
		flex-direction: column;
		gap: 16px;
		color: #000;
	}
	p {
		align-content: center;
		font-style: italic;
		line-height: 1.2;
		text-wrap: balance;
		font-size: 20px;
	}
</style>
