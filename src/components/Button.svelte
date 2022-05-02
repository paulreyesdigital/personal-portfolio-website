<script lang="ts">
	export let style: string = '';
	export let type: string = 'button';
</script>

{#if style === 'outline'}
	<button type={type}
		class={`w-full border-orange-400 border-2  px-6 py-2 rounded transition-all hover:bg-orange-400 hover:text-white`}
		><slot /></button
	>
{:else if style === 'disabled'}
	<button type={type} class={`w-full bg-orange-200 border-orange-200 border-2 text-white px-6 py-2 rounded`} disabled
		><slot /></button
	>
{:else}
	<button type={type}
		class={`w-full bg-orange-400 border-orange-400 border-2 text-white px-6 py-2 rounded transition-transform hover:-translate-y-2`}
		><slot /></button
	>
{/if}
