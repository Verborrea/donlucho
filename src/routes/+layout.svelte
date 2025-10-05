<script lang="ts">
	import '../app.css';
	import Footer from '$lib/components/Footer.svelte';
	import Header from '$lib/components/Header.svelte';
	import { onMount } from 'svelte';
	import { X } from 'lucide-svelte';

	let { children } = $props();

	let dialog = $state<HTMLDialogElement | null>(null);

	function openDialog() {
		if (dialog) {
			dialog.showModal();
		}
	}

	function closeDialog() {
		if (dialog) {
			dialog.close();
		}
	}

	onMount(() => {
		openDialog();
	});
</script>

<svelte:head>
	<title>Don Luciano</title>
	<meta name="description" content="" />
</svelte:head>

<Header {openDialog} />
{@render children?.()}
<Footer {openDialog} />

<dialog
	bind:this={dialog}
	onclick={(e) => {
		if (e.target === dialog) {
			closeDialog();
		}
	}}
>
	<button
		class="absolute top-4 right-4 cursor-pointer focus:outline-0"
		type="button"
		aria-label="Cerrar"
		title="Cerrar"
		onclick={closeDialog}
	>
		<X />
	</button>
	<div class="flex flex-col gap-3 px-6 py-8 text-center">
		<h1 class=" text-4xl">¡Únete ahora!</h1>
		<p class="text-xl">Déjanos tus datos y nos pondremos en contacto contigo para la entrevista.</p>
	</div>
</dialog>

<style>
	dialog {
		border-radius: 24px;
		border: 2px solid var(--text);
		width: calc(100% - 48px);
		max-width: 540px;
		position: fixed;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
	}
	dialog:focus {
		outline: none;
	}
	::backdrop {
		background: rgba(0, 0, 0, 0.75);
		backdrop-filter: blur(8px);
	}
</style>
