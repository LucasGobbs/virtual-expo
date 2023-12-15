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
    // animateScroll.scrollTo({
    //   element: "#scrollable",
    //   duration: 2000,
    //   delay: 400,
    // });
  });
</script>

<div in:fade={{ duration: 1000 }} class="bg-indigo-800">
  <Section {section} />
  <div id="scrollable" class="bg-[#0e0308] h-full">
    <div class="text-white">
      <div class="px-5 flex flex-col items-center h-screen-80">
        <h2
          class="transition delay-50
            text-3xl tracking-wide font-quickbold py-10"
        >
          Acervo
        </h2>

        <!-- <div>Icons made by <a href="https://www.flaticon.com/authors/ilham-fitrotul-hayat" title="Ilham Fitrotul Hayat">Ilham Fitrotul Hayat</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div><div>Icons made by <a href="https://www.flaticon.com/authors/pixel-perfect" title="Pixel perfect">Pixel perfect</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div><div>Icons made by <a href="https://www.flaticon.com/authors/bomsymbols" title="BomSymbols">BomSymbols</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div> -->
        <div class="w-2/3 justify-center">
          <h2 class="text-1xl tracking-wide font-quickbold py-10 text-center">
            Imagens
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <ImageBanner
              title="Cortejo da Rainha Negra na Festa de Reis"
              data="sala4/cortejo_rainha_negra.jpg"
            >
              <p slot="text">
                Cortejo da Rainha Negra na Festa de Reis, de Carlos Julião.
                Fonte: Acervo iconográfico Biblioteca Nacional Entre as
                ilustrações de Carlos Julião (1740-1811), destaque para a
                representação da cerimônia da rainha já coroada, com
                instrumentos de matriz africana.
              </p>
            </ImageBanner>
            <ImageBanner title="Teste" data="sala4/quem_tem_medo.jpg">
              <p slot="text">
                Em Quem tem medo de macumba?, Pai Rodney relembra os
                ensinamentos da avó, Dona Aparecida: “Não mexa, não pegue nada
                nem pise. Antes de passar, peça licença e não olhe para trás.”
                Quando dizíamos que tínhamos visto uma “macumba”, ela
                imediatamente nos corrigia: “Uma entrega, meu filho”. Foto:
                Fernanda Procópio <a
                  href="https://www.flickr.com/photos/fernandaprocopio/7104086425/in/album-72157629513462180/"
                  >Link
                </a>  Instrumento musical muito antigo, macumba era parecido com
                um reco-reco, Macumbeiro, esclarece Pai Rodney de Oxóssi, era
                aquele que sabia tocá-lo. Na infância, a avó do também
                antropólogo, babalorixá e doutor em Ciências Sociais, Dona
                Aparecida, evitava o termo. Mais tarde ele descobriria que a
                expressão usada genericamente para referir-se às religiões
                afro-brasileiras tinha uma conotação pejorativa. "Era usada como
                sinônimo de feitiço, malefício ou bruxaria, por isso que vovó o
                evitava." Em Quem tem medo de macumba?, artigo escrito para a
                revista Capital em 2018, ele descreve práticas e crenças de
                longa data, trazendo memórias e relatos de quando criança.
              </p>
            </ImageBanner>
            <ImageBanner title="Macumba" data="sala4/macumba.jpg">
              <p slot="text">
                Do quimbundo, ma'kôba, macumba é uma árvore e um instrumento de
                percussão de origem africana. Utilizado em cerimônias de
                religiões afro-brasileiras, como o candomblé e a umbanda,
                macumba é desses nomes enfeitiçados. Variante do candomblé que
                só existe no Rio de Janeiro, ma cum ba, além de transfigurar-se
                de árvore e de música, passou a vestir-se de preconceito no
                início do século XX, quando igrejas neopentecostais e alguns
                outros grupos cristãos taxaram como profanas práticas de
                religiões que não fossem as suas. As africanas principalmente.
                Tempo passou e o danado do nome ainda hoje é mal dito por quem
                não dialoga com o diferente.
              </p>
            </ImageBanner>

            <ImageBanner
              title={'"Um defeito de Cor"'}
              data="sala4/defeito_de_cor_1.jpg"
            >
              <p slot="text">
                "Um defeito de cor", Museu de Arte do Rio de Janeiro (2023).
              </p>
            </ImageBanner>
            <ImageBanner
              title={'"Um defeito de Cor"'}
              data="sala4/defeito_de_cor_2.jpg"
            >
              <p slot="text">
                "Um defeito de cor", Museu de Arte do Rio de Janeiro (2023).
              </p>
            </ImageBanner>
            <ImageBanner
              title={'"Um defeito de Cor"'}
              data="sala4/defeito_de_cor_3.jpg"
            >
              <p slot="text">
                "Um defeito de cor", Museu de Arte do Rio de Janeiro (2023).
              </p>
            </ImageBanner>
            <div />
            <ImageBanner
              title={'"Um defeito de Cor"'}
              data="sala4/defeito_de_cor_4.jpg"
            >
              <p slot="text">
                "Um defeito de cor", Museu de Arte do Rio de Janeiro (2023).
              </p>
            </ImageBanner>
          </div>

          <h2
            class="text-1xl tracking-wide font-quickbold py-10 mt-10 text-center"
          >
            Casos
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <div />
            <ImageBanner title="Jornal" data="sala4/jornal.jpg" colored="true">
              <p slot="text">
                Falsa relação de religiões de matriz africana com bruxaria
                estampa a manchete do Jornal de Alagoas, 4 fev. 1912, quando 150
                xangôs foram destruídos naquele que entraria para a história
                como o maior ato de intolerância religiosa do Brasil. Fonte:
                Acervo do Instituto Histórico e Geográfico de Alagoas. <br />
                <br />“Xangô em acção — A oligarchia e o O povo invade os covis
                — Documentos preciosos — Um bode sacrificado — Exposição de
                ídolos e bugigangas” , acompanha o título da reportagem BRUXARIA
                na capa do Jornal de Alagoas de 4 de fevereiro de 1912.<br /><br
                /> A resistência da religiosidade de matriz africana em Alagoas -
                Jornalismo Júnior (jornalismojunior.com.br)
              </p>
            </ImageBanner>
          </div>
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
