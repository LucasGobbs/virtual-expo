<script>
  import Section from "../components/Section.svelte";
  import { onMount, tick } from "svelte";
  import ImageBanner from "../components/ImageBanner.svelte";
  import { slide, fade, blur } from "svelte/transition";
  import * as animateScroll from "svelte-scrollto";
  import { content } from "../utils/content";

  const section = content["sala6"];
  let element;
  onMount(() => {
    animateScroll.scrollTo({
      element: "#scrollable",
      duration: 2000,
      delay: 400,
    });
  });
</script>

<div in:fade={{ duration: 1000 }} class="bg-[#0e0308]">
  <Section {section} />
  <div id="scrollable" class="bg-[#0e0308] h-full">
    <div class="text-white">
      <div class="px-5 flex flex-col items-center h-screen-80">
        <h2
          class="transition delay-50
            text-3xl tracking-wide font-quickbold py-10"
        >
          Formulário
        </h2>

        <div class="w-full flex justify-center">
          <a
            class="ml-5 hover:scale-125 transition ease-in-out delay-75mr-2 w-20"
            href="https://docs.google.com/forms/d/e/1FAIpQLSehWHZPoeo_vLqbF7382guwW6KS_BV4N1fhVM2-LGUAyNESlQ/viewform?usp=sf_link"
          >
            <img
              class="invert"
              src="./images/icons/007-contact-form.png"
              alt="video"
            />
          </a>
        </div>

        <!-- <div>Icons made by <a href="https://www.flaticon.com/authors/ilham-fitrotul-hayat" title="Ilham Fitrotul Hayat">Ilham Fitrotul Hayat</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div><div>Icons made by <a href="https://www.flaticon.com/authors/pixel-perfect" title="Pixel perfect">Pixel perfect</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div><div>Icons made by <a href="https://www.flaticon.com/authors/bomsymbols" title="BomSymbols">BomSymbols</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div> -->
        <div class="w-2/3 justify-center">
          <div class="h-80"></div>
        </div>
      </div>
    </div>
  </div>
  <div class="h-80"></div>
</div>

<style>
  .viewport {
    position: relative;
    overflow: scroll;
    border: 1px solid gray;
    box-sizing: border-box;

    /* hide scrollbar */
    -ms-overflow-style: none;
    scrollbar-width: none;
  }

  .viewport::-webkit-scrollbar {
    /* hide scrollbar */
    display: none;
  }
</style>
