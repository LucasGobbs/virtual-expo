<script>
  import TailwindCss from "./lib/TailwindCSS.svelte";
  import Router, { location, link } from "svelte-spa-router";
  import Home from "./lib/pages/Home.svelte";
  import Sala2 from "./lib/pages/Sala2.svelte";
  import Sala3 from "./lib/pages/Sala3.svelte";
  import Sala4 from "./lib/pages/Sala4.svelte";
  import Sala5 from "./lib/pages/Sala5.svelte";
  import Sala6 from "./lib/pages/Sala6.svelte";
  import Sala7 from "./lib/pages/Sala7.svelte";
  // import Documentos from "./lib/pages/Documentos.svelte";
</script>

<!-- <nav class="sticky top-0 z-50 flex">
  <p class="pr-10">UFF</p>
	<a href="/">Home</a>
	<a href="/#/documentos">Documentos</a>
	<a href="/#/sala2">Sala2</a>
	<a href="/#/blog/colors">Colors</a> 
</nav> -->

<Router
  routes={{
    "/": Home,
    "/sala2": Sala2,
    "/sala3": Sala3,
    "/sala4": Sala4,
    "/sala5": Sala5,
    "/sala6": Sala6,
    "/sala7": Sala7,
    // "/documentos": Documentos,
    // '/blog/:blogName': Blog
  }}
  restoreScrollState={true}
/>

<!-- /#{$location} -->
