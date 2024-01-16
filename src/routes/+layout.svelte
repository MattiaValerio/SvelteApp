<script>
	import '../app.css';
	import Navbar from '../Components/Navbar.svelte';
	import Footer from '../Components/Footer.svelte';
</script>

<div class="h-full w-full">
	<div class="bg-black fixed top-0 left-0 right-0 h-[70px]">
		<Navbar />
	</div>
	<div class="fixed bottom-[70px] top-[70px] w-full">
		<slot />
	</div>

	<div class="fixed bottom-0 right-0 left-0 block h-[70px]">
		<Footer />
	</div>
</div>
