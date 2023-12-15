<script>
  import Section from "../components/Section.svelte";
  import { onMount, tick } from "svelte";
  import ImageBanner from "../components/ImageBanner.svelte";
  import { slide, fade, blur } from "svelte/transition";
  import * as animateScroll from "svelte-scrollto";
  import { content } from "../utils/content";

  const section = content["sala7"];
  let element;
  onMount(() => {
    // animateScroll.scrollTo({
    //   element: "#scrollable",
    //   duration: 2000,
    //   delay: 400,
    // });
  });
</script>

<div in:fade={{ duration: 1000 }} class="bg-indigo-800 w-screen">
  <Section {section} />
  <div id="scrollable" class="bg-[#0e0308] h-full">
    <div class="text-white">
      <div class="px-5 flex flex-col items-center h-screen-80">
        <h2
          class="transition delay-50
            text-3xl tracking-wide font-quickbold py-10"
        ></h2>
        <h2
          class="transition delay-50
            text-3xl tracking-wide font-quickbold py-10"
        >
          Em construção
        </h2>
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
