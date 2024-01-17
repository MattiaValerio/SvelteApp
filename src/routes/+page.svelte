<script>
	import ConfirmPopup from '../Components/ConfirmSend.svelte';
	let confirm = false;

	function scrolldiv() {
		var elem = document.getElementById('works-page');

		elem !== null ? elem.scrollIntoView({ block: 'end', behavior: 'smooth' }) : null;
	}

	function scrolldiv2() {
		var elem = document.getElementById('works-list');

		if (elem !== null) {
			var topPos = elem.offsetTop;
			elem.scrollTo({
				top: 0,
				left: topPos,
				behavior: 'smooth'
			});

			console.log(elem.offsetTop);
		}
	}
</script>

<svelte:head>
	<title>MattiaValerio</title>
</svelte:head>

<ConfirmPopup open={confirm} msg="Thak you !" />

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

	<div
		id="works-page"
		class="flex flex-col gap-4 items-center justify-around h-full w-full py-2 bg-slate-500 overflow-y-auto"
	>
		<div class="w-full flex items-center justify-around">
			<button class="border px-2 rounded-md font-bold text-slate-100">Left</button>
			<h1 class="text-4xl md:lg:text-6xl font-bold text-center text-slate-100">My works</h1>
			<button class="border px-2 rounded-md font-bold text-slate-100" on:click={() => scrolldiv2()}
				>Right</button
			>
		</div>

		<div id="works-list" class="flex overflow-x-scroll h-full w-full gap-10 p-3">
			<div
				id="work-1"
				class="flex flex-shrink-0 flex-col items-center h-full w-full md:w-[45%] bg-slate-100 justify-center gap-5 rounded-md"
			>
				<h2 class="text-2xl font-bold text-center text-slate-700">Lorem Ipsum</h2>
				<p class="text-center text-slate-700">
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.
				</p>
			</div>

			<div
				id="work-2"
				class="flex md:w-[50%] border flex-shrink-0 w-full flex-col items-center justify-center gap-5"
			>
				<h2 class="text-2xl font-bold text-center text-slate-100">Lorem Ipsum</h2>
				<p class="text-center text-slate-100">
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.
				</p>
			</div>

			<div
				id="work-3"
				class="flex md:w-[50%] border flex-col flex-shrink-0 w-full items-center justify-center gap-5"
			>
				<h2 class="text-2xl font-bold text-center text-slate-100">Lorem Ipsum</h2>
				<p class="text-center text-slate-100">
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.
				</p>
			</div>

			<div
				id="work-4"
				class="flex md:w-[50%] border flex-col flex-shrink-0 w-full items-center justify-center gap-5"
			>
				<h2 class="text-2xl font-bold text-center text-slate-100">Lorem Ipsum</h2>
				<p class="text-center text-slate-100">
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.
				</p>
			</div>

			<div
				id="work-5"
				class="flex md:w-[50%] border flex-col flex-shrink-0 w-full items-center justify-center gap-5"
			>
				<h2 class="text-2xl font-bold text-center text-slate-100">Lorem Ipsum</h2>
				<p class="text-center text-slate-100">
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.
				</p>
			</div>

			<div
				id="work-6"
				class="flex md:w-[50%] border flex-col items-center flex-shrink-0 w-full justify-center gap-5"
			>
				<h2 class="text-2xl font-bold text-center text-slate-100">Lorem Ipsum</h2>
				<p class="text-center text-slate-100">
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis
				</p>
			</div>
		</div>
	</div>

	<div id="contacts" class=" flex flex-col items-center justify-center h-full bg-slate-500 gap-5">
		<h1 class="text-6xl font-bold text-center text-slate-100">Contact Me</h1>
		<div class="flex flex-col gap-5 w-full px-3 justify-center">
			<input type="text" placeholder="Name" class="px-2 py-1" />
			<input type="text" placeholder="your@email.com" class="px-2 py-1" />
			<textarea placeholder="Message" class="h-40 px-2 py-1" />
			<div class="w-full flex justify-center">
				<button
					class="text-white py-3 border shadow-slate-700 shadow-xl flex justify-center gap-1 rounded-md w-[40%] font-bold"
					on:click={() => (confirm = !confirm)}
				>
					<p>Send Message</p>
					<svg
						xmlns="http://www.w3.org/2000/svg"
						width="24"
						height="24"
						viewBox="0 0 24 24"
						class="fill-white rotate-[-90deg]"
					>
						<polygon
							points="13 17.586 13 4 11 4 11 17.586 4.707 11.293 3.293 12.707 12 21.414 20.707 12.707 19.293 11.293 13 17.586"
						/>
					</svg>
				</button>
			</div>
		</div>
	</div>
</div>

<style>
	*::-webkit-scrollbar {
		display: none;
	}
</style>
