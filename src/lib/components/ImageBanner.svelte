<script>
  import { Svroller } from "svrollbar";
  import { Modal, Content, Trigger } from "sv-popup";
  import Carousel from "svelte-carousel";

  import VideoPlayer from "svelte-video-player";

  export let wrapper = "";
  export let style = "";
  export let title;
  export let data;
  export let thumbnail;
  export let colored = false;

  export let text;
  const isArr = Array.isArray(data);

  const isImg = (str) => str.includes(".png") || str.includes(".jpg");
  const isVideo = (str) => str.includes(".mp4");
  const isYt = (str) => str.includes("youtube");
  let viewport;
  let contents;
</script>

<div class={wrapper}>
  <Modal>
    <Content>
      <div
        class="bg-black text-white font-mont border-4 flex flex-col h-screen-90 text-center"
      >
        {#if isArr}
          <!-- content here -->
          <div class="h-5/6">
            <Carousel class="h-28">
              {#each data as image, index}
                <!-- content here -->

                {#if isImg(image)}
                  <img
                    alt="teste"
                    class="transition ease-in delay-150 h-[25rem] object-contain"
                    src="./images/{image}"
                  />
                {:else}
                  <VideoPlayer
                    timeDisplay="true"
                    poster="./images/{thumbnail}"
                    source="./images/{data}"
                    loop
                  />
                {/if}
              {/each}
            </Carousel>
          </div>
        {:else if isImg(data)}
          <img
            alt="teste"
            class="transition ease-in delay-150 max-h-5-6 object-contain"
            src="./images/{data}"
          />
        {:else if isVideo(data)}
          <VideoPlayer
            timeDisplay="true"
            poster="./images/{thumbnail}"
            source="./images/{data}"
            loop
          />
        {:else if isYt(data)}
          <iframe
            height="380px"
            src={data}
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            allowfullscreen
          ></iframe>
        {/if}

        <div class="h-2/6 overflow-hidden scroll-container">
          <Svroller width="100%" height="100%" alwaysVisible="true">
            <h1 class="text-2xl mt-2">{title}</h1>

            <div class="text-justify p-4">
              <slot name="text">
                <span class="missing">Unknown name</span>
              </slot>
            </div>
          </Svroller>
        </div>
      </div>
    </Content>
    <Trigger>
      <div class="group flex">
        <img
          alt="teste"
          class="gropu-hover:border-2 hover:scale-105 border-white {colored
            ? ''
            : 'hover:grayscale-0 grayscale'}
        transition ease-in-out delay-50 object-cover w-full h-full {style}"
          src="./images/{thumbnail ?? (Array.isArray(data) ? data[0] : data)}"
        />
      </div>
    </Trigger>
  </Modal>
</div>

<style>
  .max-h-5-6 {
    max-height: 60.33333%;
  }

  .h-screen-80 {
    height: 80vh;
  }
  .h-screen-90 {
    height: 90vh;
  }

  .h-screen-95 {
    height: 95vh;
  }

  .picker {
    background-color: rgb(118, 47, 165);
  }

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

  .scroll-container {
    --svrollbar-track-width: 15px;

    --svrollbar-thumb-width: 10px;
  }
</style>
