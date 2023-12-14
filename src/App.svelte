<script>
  import TailwindCss from './lib/TailwindCSS.svelte';
	import Router, {location, link} from 'svelte-spa-router';
	import Home from './lib/pages/Home.svelte';
	import Sala2 from './lib/pages/Sala2.svelte';
	import Documentos from './lib/pages/Documentos.svelte';
</script>

<!-- <nav class="sticky top-0 z-50 flex">
  <p class="pr-10">UFF</p>
	<a href="/">Home</a>
	<a href="/#/documentos">Documentos</a>
	<a href="/#/sala2">Sala2</a>
	<a href="/#/blog/colors">Colors</a> 
</nav> -->

<Router routes={{
	'/': Home,
	'/sala2': Sala2,
	'/documentos': Documentos,
	// '/blog/:blogName': Blog
}} />

<!-- /#{$location} -->