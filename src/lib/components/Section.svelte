<script>
  import { slide, fade } from 'svelte/transition';
  import Carousel from 'svelte-carousel'
  import { link } from "svelte-spa-router";

  export let image;
  export let title = "Default Title";
  export let text = ["Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum."]
  export let tint = "rgb(90, 19, 14)"
  export let filter = '';
  export let url;

  let showText = true;
  function disableText() {
    showText = !showText;
  }
  import SwipeDown from "svelte-material-icons/EyeOutline.svelte"
  import ImageArea from "svelte-material-icons/ImageOutline.svelte"
  import VideoArea from "svelte-material-icons/VideoOutline.svelte"
  
</script>
<!-- data-aos="zoom-out" -->
<!-- data-aos-anchor-placement="center"  -->
<div class="relative flex align-middle justify-center h-screen-80">
  <div class="transition delay-100 parallax 
      w-full h-full absolute bg-cover md:bg-contain" 
      style="background-image: url({image}); filter: {filter}; background-color: {showText? tint:''}">
  </div>

  <div class="text-white relative h-full w-1/3 ">
    
    <div class="p-5 {showText? 'opacity-95': 'opacity-5'}">
      <h2 data-aos="zoom-out" class="transition delay-50  
        text-6xl tracking-wide font-quickbold py-5">
        {title.toUpperCase()}
      </h2>
      <div class="flex">
        <a class="hover:scale-125 transition ease-in-out delay-75" href={`/${url}`} use:link>
          <ImageArea color={showText? 'white':'red'} width={40} height={40}/>
        </a>
        <a class="hover:scale-125 transition ease-in-out delay-75" href={`/${url}`} use:link>
          <VideoArea color={showText? 'white':'red'} width={40} height={40}/>
        </a>
      
      </div>
      <!-- <Carousel> -->

        {#each text as line}
          <p data-aos="zoom-out" class="transition delay-50 text-justify
            first-letter:text-lg font-mont 
            text-md py-10 whitespace-pre-line
            ">
            {line}
          </p>
        {/each}
      <!-- </Carousel> -->
    </div>
  
    
  </div>

</div>
<style>
   .h-screen-80 {
    height: 80vh;
  }

  .parallax {
    /* filter: grayscale(100%); */
    /* background-color: rgb(158, 157, 157); */
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-blend-mode: multiply;

  }
</style>
