<script lang="ts">
	import Input from '$lib/components/forms/Input.svelte';
	import type { SettingsValues } from '$lib/stores/settings.store';
	import { _, dictionary } from 'svelte-i18n';

	export let values: SettingsValues;
</script>

<div
	class="grid grid-cols-[1fr_min-content] justify-items-start place-items-center gap-4 text-zinc-400 pb-2"
>
	<h1
		class="font-medium text-xl text-zinc-200 tracking-wide col-span-2 border-b border-zinc-800 justify-self-stretch pb-2 mt-8"
	>
		{$_('settings.library.library')}
	</h1>

	<h2>
		{$_('settings.library.imageBackdropQuality')}
	</h2>
	<Input type="number" bind:value={values.libraryImageBackdropQuality} />
</div>
