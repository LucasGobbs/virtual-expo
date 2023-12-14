<script>
  import { slide, fade } from 'svelte/transition';
  import Carousel from 'svelte-carousel'
  import { Modal, Content, Trigger } from "sv-popup"
  let show = false
  function handleClick(){
    show = !show;
    console.log("AAAAA")
  }
</script>


<div class="bg-[#420f27] h-full">
  <div class="text-white">
    <div class="px-5 h-screen-80 flex flex-col items-center">
      <h2 class="transition delay-50  
        text-3xl tracking-wide font-quickbold py-10">
        Textos e Imagens
      </h2>
      <div class="w-2/3 justify-center">
        <div class="w-full grid grid-cols-3 gap-1">
          <Modal>
            <Content>
              <div class="bg-black text-white">
                <h1>Hello</h1>
                <img class=" transition ease-in delay-150  object-cover w-full h-full" on:click={handleClick} src="./images/calundu.png">
                <p>
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas

                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas

                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasda
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas

                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasda
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas

                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasda
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas

                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdas
                  asdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasdasasdasdasda
                </p>
              </div>
              
            </Content>
            <Trigger>
              <img class="hover:grayscale-0 transition ease-in delay-150 grayscale object-cover w-full h-full" on:click={handleClick} src="./images/calundu.png">

            </Trigger>
          </Modal>
          <img class="hover:grayscale-0 transition ease-in delay-150 grayscale object-cover w-full h-full"  src="./images/ilustracao_kleber_sales_1.png">

          <img class="hover:grayscale-0 transition ease-in delay-150 grayscale object-cover w-full h-full"  src="./images/ilustracao_kleber_sales_2.png">
          <img class="col-span-2 hover:grayscale-0 transition ease-in delay-150 grayscale object-cover w-full h-full"  src="./images/tela_debret.png">
          <img class="hover:grayscale-0 transition ease-in delay-150 grayscale self-stretch w-full"  src="./images/tela_rugendas.png">
         

        </div>
    

      </div>
     
    
    </div>
    
   
  </div>
</div>