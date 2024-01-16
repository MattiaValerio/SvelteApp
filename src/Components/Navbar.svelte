<script>
	let links = [
		{ name: 'Home', url: 'landig-page' },
		{ name: 'Tecs', url: 'tec' },
		{ name: 'Projects', url: 'works-page' },
		{ name: 'About', url: 'about' },
		{ name: 'Contact', url: 'contacts' }
	];

	function scrollHome() {
		var elem = document.getElementById('landing-page');

		elem !== null ? elem.scrollIntoView({ block: 'end', behavior: 'smooth' }) : null;
	}

	function scrollHome() {
		var elem = document.getElementById('landing-page');

		elem !== null ? elem.scrollIntoView({ block: 'end', behavior: 'smooth' }) : null;
	}
</script>

<nav class="h-full w-full">
	<ul class="flex justify-between h-full w-full items-center p-4">
		{#each links as link}
			<li class="mr-4"><a href={link.url} class="text-white">{link.name}</a></li>
		{/each}
	</ul>
</nav>
