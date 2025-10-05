<script>
	import { page } from '$app/state';
	import logo from '$lib/assets/logo.avif';
	import { fly } from 'svelte/transition';

	let { openDialog } = $props();

	const links = [
		{
			name: 'Inicio',
			href: '/'
		},
		{
			name: 'Beneficios',
			href: '/#beneficios'
		},
		{
			name: 'Canal',
			href: '/#canal'
		},
		{
			name: 'Productos',
			href: '/#productos'
		}
	];

	let opened = $state(false);

	function onclick() {
		opened = !opened;
		if (opened) {
			document.documentElement.style.overflow = 'hidden';
			document.body.style.overflow = 'hidden';
		} else {
			document.documentElement.style.overflow = '';
			document.body.style.overflow = '';
		}
	}
</script>

<header class="fixed top-0 right-0 left-0 z-20 bg-black/75 text-white backdrop-blur-[8px]">
	<div class="mx-auto flex max-w-7xl items-center justify-between gap-4 p-6 font-serif">
		<img src={logo} alt="Logo de Don Luciano" class="w-28 hd:w-40" />
		<nav class="hidden items-center gap-8 hd:flex">
			{#each links as link}
				<a href={link.href} class="text-xl font-bold hover:text-yellow-300">{link.name}</a>
			{/each}
			<button
				type="button"
				class="btn"
				onclick={() => {
					openDialog();
				}}>Postular</button
			>
		</nav>
		<button
			type="button"
			class="flex cursor-pointer flex-col gap-1.5 py-2.5 hd:hidden"
			aria-label="Menú"
			class:opened
			{onclick}
		>
			<div id="bb1" class="h-[2px] w-7 rounded-full bg-cream transition"></div>
			<div id="bb2" class="h-[2px] w-7 rounded-full bg-cream transition"></div>
			<div id="bb3" class="h-[2px] w-7 rounded-full bg-cream transition"></div>
		</button>
	</div>
</header>

{#if opened}
	<nav
		in:fly={{ y: '-100svh', duration: 400, opacity: 1 }}
		out:fly={{ y: '-100svh', duration: 400, opacity: 1, delay: 300 }}
		class="fixed top-0 right-0 left-0 z-15 flex min-h-[100svh] flex-col justify-end gap-6 bg-black/75 p-5.5 font-serif font-bold text-cream backdrop-blur-[8px] hd:hidden"
	>
		{#each links as link, index}
			<a
				{onclick}
				class="text-3xl"
				href={link.href}
				in:fly|global={{ y: -20, duration: 400, opacity: 0, delay: index * 35 + 250 }}
				out:fly|global={{
					y: -20,
					duration: 200,
					opacity: 0,
					delay: (links.length - index) * 15 + 15
				}}
				aria-current={page.url.pathname === link.href}>{link.name}</a
			>
		{/each}
		<button
			onclick={() => {
				onclick();
				openDialog();
			}}
			in:fly|global={{ y: -20, duration: 400, opacity: 0, delay: links.length * 35 + 250 }}
			out:fly|global={{ y: -20, duration: 200, opacity: 0, delay: 0 }}
			class="btn rounded-[28px] pb-3 text-3xl hover:rounded-[8px]"
			type="button">Postular</button
		>
	</nav>
{/if}

<style>
	.opened > #bb1 {
		transform: translateY(8px) rotate(-45deg);
	}
	.opened > #bb2 {
		opacity: 0;
		transform: scaleX(1.5);
	}
	.opened > #bb3 {
		transform: translateY(-8px) rotate(45deg);
	}
	.opened > * {
		fill: white;
		transition: all 200ms;
	}
</style>
