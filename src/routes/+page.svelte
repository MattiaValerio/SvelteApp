<script>
	function scrolldiv() {
		var elem = document.getElementById('works-page');

		elem !== null ? elem.scrollIntoView({ block: 'end', behavior: 'smooth' }) : null;
	}
</script>

<svelte:head>
	<title>MattiaValerio</title>
</svelte:head>

<div class="h-full w-full bg-slate-500 overflow-auto">
	<div id="landing-page" class="section active flex flex-col items-center justify-center h-full">
		<div class="flex flex-col items-center gap-5">
			<h1 class="text-6xl font-bold text-center text-slate-100">Mattia Valerio</h1>
			<h2 class="text-2xl font-bold text-center text-slate-100">Full Stack Web Developer</h2>
			<button
				class="border px-3 rounded shadow-slate-700 shadow-xl py-3 flex items-center gap-6 text-white font-bold"
				on:click={() => scrolldiv()}
			>
				<p>View my works</p>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="24"
					height="24"
					viewBox="0 0 24 24"
					class="fill-white"
				>
					<polygon
						points="13 17.586 13 4 11 4 11 17.586 4.707 11.293 3.293 12.707 12 21.414 20.707 12.707 19.293 11.293 13 17.586"
					/>
				</svg>
			</button>
		</div>
	</div>

	<div id="about" class="flex flex-col items-center justify-center h-full bg-slate-500">
		<h1 class="text-6xl font-bold text-center text-slate-100">Lorem Ipsum</h1>
		<h2 class="text-2xl font-bold text-center text-slate-100">Full Stack Developer</h2>
	</div>

	<div id="works-page" class="flex flex-col items-center justify-center h-full bg-slate-500">
		<h1 class="text-6xl font-bold text-center text-slate-100">Lorem Ipsum</h1>
		<h2 class="text-2xl font-bold text-center text-slate-100">Full Stack Developer</h2>
	</div>

	<div id="contacts" class=" flex flex-col items-center justify-center h-full bg-slate-500">
		<h1 class="text-6xl font-bold text-center text-slate-100">Lorem Ipsum</h1>
		<h2 class="text-2xl font-bold text-center text-slate-100">Full Stack Developer</h2>
	</div>
</div>

<style>
	*::-webkit-scrollbar {
		display: none;
	}
</style>
