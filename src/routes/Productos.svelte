<script>
	import pisco from '$lib/assets/pisco.avif';
	import grappa from '$lib/assets/grappa.avif';
	import vino1 from '$lib/assets/vino1.avif';
	import vino2 from '$lib/assets/vino2.avif';

	const products = [
		{
			img: pisco,
			name: 'Pisco Don Luciano',
			details: 'Acholado - 750ml'
		},
		{
			img: grappa,
			name: 'Grappa Don Luciano',
			details: '750ml'
		},
		{
			img: vino1,
			name: 'Vino Don Luciano',
			details: 'Acholado - 750ml'
		},
		{
			img: vino2,
			name: 'Vino Don Luciano',
			details: 'Higo - 750ml'
		}
	];
</script>

<article id="productos" class="scroll-mt-14 py-12 text-cream sm:py-18 md:py-24 hd:scroll-mt-8">
	<div class="mx-auto flex max-w-7xl flex-col gap-6 px-6 md:gap-12">
		<h1 class="text-center text-4xl sm:text-5xl md:text-6xl lg:text-8xl">Nuestros productos</h1>
		<div class="grid gap-4 text-center sm:grid-cols-2 md:grid-cols-4">
			{#each products as product}
				<section>
					<div
						class="group flex items-center justify-center rounded-2xl bg-white/15 py-5 backdrop-blur-[2px]"
					>
						<img
							src={product.img}
							alt="Chico levantando una billetera"
							class="h-100 transition group-hover:scale-106"
							height="400"
						/>
					</div>
					<div class="flex grow flex-col">
						<p class="text-xl font-bold">{product.name}</p>
						<p>{product.details}</p>
					</div>
				</section>
			{/each}
		</div>
	</div>
</article>

<style>
	article {
		background-image: url('/paisaje.avif');
		background-position: center;
		background-size: cover;
		background-repeat: no-repeat;
	}
	section {
		display: flex;
		flex-direction: column;
		gap: 16px;
	}
</style>
