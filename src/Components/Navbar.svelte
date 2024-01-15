<script>
	let links = [
		{ name: 'Home', url: '/' },
		{ name: 'Projects', url: '/projects' },
		{ name: 'About', url: '/about' },
		{ name: 'Contact', url: '/contact' }
	];
</script>

<nav class="h-full w-full">
	<ul class="flex justify-between h-full w-full items-center p-4">
		{#each links as link}
			<li class="mr-4"><a href={link.url} class="text-white">{link.name}</a></li>
		{/each}
	</ul>
</nav>
