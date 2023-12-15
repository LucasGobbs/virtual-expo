<script>
  import Section from "../components/Section.svelte";
  import { link } from "svelte-spa-router";
  import { onMount } from "svelte";
  import AOS from "aos";
  import { content } from "../utils/content";
  import * as animateScroll from "svelte-scrollto";
  const sections = Object.values(content);

  onMount(() => {
    AOS.init();
  });
</script>

<svelte:head>
  <link rel="stylesheet" href="https://unpkg.com/aos@next/dist/aos.css" />
</svelte:head>

<div class="h-screen w-full bg-black">
  <div class="text-white bg-black">
    <div
      class="bg-purple-800 bg-gradient-to-r from-indigo-950 pt-28 pb-8 px-5 h-screen-95 justify-center flex"
    >
      <div class="w-2/3 flex flex-col justify-between items-center">
        <div>
          <h2
            class="transition delay-50
            md:text-4xl lg:text-44xl tracking-wide font-mont font-bold leading-tight"
          >
            Mulheres e intolerância religiosa na Idade Moderna
          </h2>

          <h3
            class="transition delay-50
            md:text-2xl text-4xl tracking-wide font-mont py-1"
          >
            Exposição Virtual | UFF
          </h3>
          <p class="md:text-xl lg:text-2xl pt-16">
            Exposição sobre tasdoaskd saokdoask doask odsak odask odk
            asdokasodkasokdkasokdasokdk oaskdokasok oaksdo kaos dokaso d
            asdkasokdoaskd asaodkasok asokdoas kosako dkasokd oaskod
          </p>
        </div>
        <i class="w-12">
          <img
            on:click={() =>
              animateScroll.scrollTo({
                element: "#index_0",
                duration: 1000,
                delay: 50,
              })}
            class="invert animate-bounce"
            src="./images/icons/004-mouse-cursor.png"
            alt="video"
          />
        </i>
      </div>
    </div>

    {#each sections as section, index}
      <div
        id="index_{index}"
        class="bg-black flex flex-col justify-center align-middle items-center"
      >
        <Section {section} />
        {#if index < sections.length - 1}
          <i class="w-12 opacity-40">
            <img
              on:click={() =>
                animateScroll.scrollTo({
                  element: `#index_${index + 1}`,
                  duration: 1000,
                  delay: 50,
                })}
              class="invert animate-bounce"
              src="./images/icons/004-mouse-cursor.png"
              alt="video"
            />
          </i>
        {/if}
      </div>
    {/each}
    <div class="h-80"></div>
  </div>
</div>

<style>
  .h-screen-80 {
    height: 80vh;
  }
  .h-screen-95 {
    height: 95vh;
  }

  .picker {
    background-color: rgb(118, 47, 165);
  }
</style>
