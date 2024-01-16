<script lang="ts">
	type link = {
		name: string;
		url: string;
	};

	let links: link[] = [
		{ name: 'Home', url: 'landing-page' },
		{ name: 'About me', url: 'about' },
		{ name: 'Projects', url: 'works-page' },
		{ name: 'Contact', url: 'contacts' }
	];

	function scrollTo(link: link) {
		var elem = document.getElementById(link.url);
		elem !== null ? elem.scrollIntoView({ block: 'end', behavior: 'smooth' }) : null;
	}
</script>

<nav class="h-full w-full">
	<ul class="flex justify-between h-full w-full items-center px-4 sm:px-6 xl:px-10">
		{#each links as link}
			<li class="mr-4">
				<button class="text-white" on:click={() => scrollTo(link)}> {link.name}</button>
			</li>
		{/each}
	</ul>
</nav>
