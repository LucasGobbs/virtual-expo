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
    <div class="bg-[#310b2a] pt-28 pb-8 px-5 h-screen-95 justify-center flex">
      <div class="w-2/3 flex flex-col justify-between items-center">
        <div>
          <h2
            class="transition delay-50 text-[#d05d50]
            md:text-4xl lg:text-4xl tracking-wide font-mont font-bold leading-tight"
          >
            Mulheres e Bruxaria:<br /> Um casamento indissolúvel na Idade Moderna
          </h2>

          <h3
            class="transition delay-50 text-[#c34739] opacity-80
            md:text-xl text-3xl tracking-wide font-mont py-1"
          >
            Exposição Virtual | UFF
          </h3>
          <h3
            class="transition delay-50 opacity-60
            md:text-md text-sm tracking-wide font-mont py-1"
          >
            Curadouras: Ariel de Oliveira, Karen da Silva, Mairá Gomes, Mariana
            Chaves, Millena Delfino e Nathália Rouxinol
          </h3>
          <p class="md:text-lg lg:text-xl pt-8 text-justify">
            Historicamente, mulheres e suas práticas religiosas estiveram na
            mira dos olhos julgadores, seja para criminalizá-las ou
            desprezá-las. <br /> <br />Nesta exposição, viajamos em alguns
            momentos históricos, onde práticas de religiosidade femininas foram
            e/ou ainda são associadas a práticas como feitiçaria/bruxaria, mesmo
            quando sequer eram.
          </p>
        </div>
        <div class="h-20"></div>
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
        class="flex flex-col justify-center align-middle items-center"
      >
        <Section overview={true} {section} />
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
