<script>
  import Section from "../components/Section.svelte";
  import { onMount, tick } from "svelte";
  import ImageBanner from "../components/ImageBanner.svelte";
  import { slide, fade, blur } from "svelte/transition";
  import * as animateScroll from "svelte-scrollto";
  import { content } from "../utils/content";

  const section = content["sala4"];
  let element;
  onMount(() => {
    animateScroll.scrollTo({
      element: "#scrollable",
      duration: 2000,
      delay: 400,
    });
  });
</script>

<div in:fade={{ duration: 1000 }} class="bg-indigo-800">
  <Section {section} />
  <div id="scrollable" class="bg-[#0e0308] h-full">
    <div class="text-white">
      <div
        class="px-5 h-screen-80 flex flex-col items-center bg-[#4a261e] {section.acervoTint}"
      >
        <h2
          class="transition delay-50
            text-5xl tracking-wide font-quickbold py-10"
        >
          Acervo
        </h2>

        <!-- <div>Icons made by <a href="https://www.flaticon.com/authors/ilham-fitrotul-hayat" title="Ilham Fitrotul Hayat">Ilham Fitrotul Hayat</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div><div>Icons made by <a href="https://www.flaticon.com/authors/pixel-perfect" title="Pixel perfect">Pixel perfect</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div><div>Icons made by <a href="https://www.flaticon.com/authors/bomsymbols" title="BomSymbols">BomSymbols</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div> -->
        <div class="w-2/3 justify-center">
          <h2
            class="text-3xl tracking-wide font-quickbold pt-10 pb-5 text-center"
          >
            Imagens
          </h2>

          <div class="w-full grid grid-cols-3 gap-4">
            <ImageBanner
              title="Cortejo da Rainha Negra na Festa de Reis"
              data="sala5/cortejo_rainha_negra.jpg"
            >
              <p slot="text">
                Cortejo da Rainha Negra na Festa de Reis, de Carlos Julião.
                Fonte: Acervo iconográfico Biblioteca Nacional Entre as
                ilustrações de Carlos Julião (1740-1811), destaque para a
                representação da cerimônia da rainha já coroada, com
                instrumentos de matriz africana.
              </p>
            </ImageBanner>
            <ImageBanner title="Calundu" data="sala2/calundu.png">
              <p slot="text">
                A maioria dos processos envolvendo feitiçaria tratava de
                práticas individuais ligadas a técnicas mágicas e orações.
                Raramente faziam menção explícita a pactos com o demônio,
                reuniões noturnas ou práticas coletivas de ritos e cerimônias
                religiosas.
              </p>
            </ImageBanner>

            <ImageBanner title="Calundu" data="sala2/calundu_carlos.jpg">
              <p slot="text">Calundu - pintura de Carlos Julião</p>
            </ImageBanner>

            <!-- <ImageBanner
              wrapper="col-span-2"
              title="Documentos de suspeitos de Judaizar"
              data="sala2/documentos_judaizar.jpg"
            >
              <p slot="text">
                Exemplos de documentos que relatam denúncias no Brasil de
                suspeitos de "judaizar"
              </p>
            </ImageBanner> -->
          </div>

          <h2
            class="text-3xl tracking-wide font-quickbold pt-10 pb-5 text-center"
          >
            Casos
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <div />

            <ImageBanner
              wrapper="row-span-2"
              title="Tela de Rugendas (Apenas Ilustrativo)"
              data="sala2/tela_rugendas.png"
            >
              <p slot="text">
                Esse caso ocorreu em São Paulo, no ano de 1749, envolvendo
                Páscoa, uma mulher escravizada acusada de praticar feitiçaria e
                provocar mortes usando esses poderes. Ela pessoalmente prometeu
                à sua dona que curaria a filha dela. A prática de feitiçaria
                incluía a utilização de ossos de animais, unhas, cabelos e
                excrementos, acreditando-se que esses elementos possuíam
                vitalidade. Nas últimas páginas do processo, fica registrado que
                a filha de Maria Serqueira foi curada após esses objetos terem
                sido desenterrados da parede. No entanto, o desfecho final do
                processo não é claro.<br /><br /> É interessante observar que
                nem todas as práticas se relacionavam diretamente aos conflitos
                entre escravos e seus senhores. Muitas delas refletiam
                inimizades e conflitos pessoais, como evidenciado pelo fato de
                que Páscoa foi denunciada por um colega escravo e não por um
                branco. Um testemunho curioso foi dado por Sebastião, um escravo
                de 35 anos vindo do reino de Angola e pertencente a Inácio
                Xavier. Ele relatou ter visto Páscoa proferir palavras
                incompreensíveis perto da casa de dona Maria Cerqueira. Enquanto
                dizia essas palavras, ela se movia em direção à parede, dava um
                salto com a mão aberta e batia na parede. Depois, ela recuava
                sem virar as costas para a parede. Sebastião afirmou que, ao
                perceber que estava sendo observada, Páscoa parou subitamente.
                Ele não sabia o significado desses atos e nunca tinha visto
                Páscoa repeti-los.
                <br /><br />Os registros do processo também incluem o depoimento
                de Antonio Ribeiro Leite, neto de dona Maria Cerqueira. Ele
                relatou que, em uma ocasião, encontrou Páscoa carregando ossos
                de costela de vaca e galinha, além de pequenas bolas semelhantes
                a excrementos. Páscoa foi acusada não apenas por sua dona, mas
                também pelos vizinhos, de proferir palavras contra a Igreja e
                que pareciam invocar o diabo. Esse período colonial evidenciava
                a forte associação com o sobrenatural e as
                tendências demoníacas.
              </p>
            </ImageBanner>
          </div>

          <h2
            class="text-3xl tracking-wide font-quickbold pt-10 pb-5 text-center"
          >
            Videos
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <div />
            <ImageBanner
              title="“O Martelo das Bruxas” (1970)"
              thumbnail="sala2/video_bruxa_thumb.png"
              data="sala2/video_bruxa.mp4"
            >
              <p slot="text"></p>
            </ImageBanner>
          </div>
        </div>
        <div class="h-80"></div>
      </div>
    </div>
  </div>
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
