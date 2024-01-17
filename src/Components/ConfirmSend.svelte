<script lang="ts">
	export let open = false;
	export let msg = '';
</script>

{#if open}
	<div
		class="h-full w-full bg-black bg-opacity-60 flex items-center justify-center absolute top-0 bottom-0 left-0 right-0"
	>
		<div
			class="bg-slate-500 h-72 w-full sm:w-full md:w-[50%] lg:w-[25%] xl:w-[25%] m-12 border rounded-lg flex items-center justify-around flex-col px-4"
		>
			<h1 class="text-4xl text-center text-slate-100">{msg}</h1>
			<div class="flex justify-center">
				<button
					on:click={() => (open = !open)}
					class="border shadow-slate-700 shadow-xl px-3 py-1 rounded-md bg-slate-500 text-2xl text-slate-100"
				>
					Close
				</button>
			</div>
		</div>
	</div>
{/if}
