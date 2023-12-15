<script>
  import Section from "../components/Section.svelte";
  import { onMount, tick } from "svelte";
  import ImageBanner from "../components/ImageBanner.svelte";
  import { slide, fade, blur } from "svelte/transition";
  import * as animateScroll from "svelte-scrollto";
  import { content } from "../utils/content";

  const section = content["sala3"];
  let element;
  let celebration;
  onMount(() => {
    celebration.play();
    animateScroll.scrollTo({
      element: "#scrollable",
      duration: 2000,
      delay: 400,
    });
  });
</script>

<div in:fade={{ duration: 1000 }} class={section.acervoTint}>
  <Section {section} />
  <audio
    src="./images/sala2/whispers.m4a"
    preload="auto"
    loop
    bind:this={celebration}
  >
    <track kind="captions" />
  </audio>
  <div id="scrollable" class="{section.acervoTint} h-full">
    <div class="text-white bg-[#100c3d]">
      <div class="px-5 flex flex-col items-center h-screen-80">
        <h2
          class="transition delay-50
            text-5xl tracking-wide font-quickbold py-10"
        >
          Acervo
        </h2>

        <!-- <div>Icons made by <a href="https://www.flaticon.com/authors/ilham-fitrotul-hayat" title="Ilham Fitrotul Hayat">Ilham Fitrotul Hayat</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div><div>Icons made by <a href="https://www.flaticon.com/authors/pixel-perfect" title="Pixel perfect">Pixel perfect</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div><div>Icons made by <a href="https://www.flaticon.com/authors/bomsymbols" title="BomSymbols">BomSymbols</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div> -->
        <div class="w-2/3 justify-center">
          <h2
            class="text-3xl tracking-wide font-quickbold pb-5 pt-10 text-center"
          >
            Imagens
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <ImageBanner
              title="A Expulsão dos Judeus"
              data="sala3/expulsao_judeus.png"
            >
              <p slot="text">
                A Expulsão dos Judeus (Roque Gameiro, Quadros da História de
                Portugal, 1917).<br /><br /> Disponível em:
                <a
                  href="https://pt.wikipedia.org/wiki/Ficheiro:A_Expuls%C3%A3o_dos_Judeus_(Roque_Gameiro,_Quadros_da_Hist%C3%B3ria_de_Portugal,_1917).png"
                  >Link
                </a>
              </p>
            </ImageBanner>
            <ImageBanner
              title="Execution des criminels condamnées par l'Inquisition"
              data="sala3/execution_criminals.jpg"
            >
              <p slot="text">
                Execution des criminels condamnées par l'Inquisition (autoria
                desconhecida, século XVIII).<br /><br />
                <!-- <a
                  href="https://pt.wikipedia.org/wiki/Ficheiro:A_Expuls%C3%A3o_dos_Judeus_(Roque_Gameiro,_Quadros_da_Hist%C3%B3ria_de_Portugal,_1917).png"
                  >Link
                </a> -->
              </p>
            </ImageBanner>
            <ImageBanner
              title="Mural de Nuno Saraiva"
              data="sala3/historia_lisboa.png"
            >
              <p slot="text">
                "História de Lisboa", por Nuno Saraiva, mural na Rua Norberto de
                Araújo, Lisboa, Portugal, 8 fev. 2018.<br /><br /> Disponível
                em:
                <a
                  href="https://commons.wikimedia.org/wiki/File:Hist%C3%B3ria_de_Lisboa,_por_Nuno_Saraiva_(Arco_da_Rua_Norberto_de_Ara%C3%BAjo)_02.png"
                  >Link
                </a>
              </p>
            </ImageBanner>
          </div>
          <h2
            class="text-3xl tracking-wide font-quickbold pb-5 pt-10 text-center"
          >
            Mapas
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <ImageBanner
              wrapper="col-span-2"
              title="Countries from which Jews were expelled,"
              data="sala3/mapa1.jpg"
            >
              <p slot="text">
                Countries from which Jews were expelled, 15th-17th Centuries.<br
                /><br /> Disponível em:
                <a
                  href="https://commons.princeton.edu/mg/countries-from-which-jews-were-expelled-15th-17th-centuries/"
                  >Link
                </a>
              </p>
            </ImageBanner>

            <ImageBanner
              title="Expulsion of the Jews from the Iberian Peninsula."
              data="sala3/mapa2.jpg"
            >
              <p slot="text">
                Expulsion of the Jews from the Iberian Peninsula.<br /><br />
                Disponível em:
                <a
                  href="https://commons.princeton.edu/mg/expulsion-of-the-jews-from-the-iberian-peninsula/"
                  >Link
                </a>
              </p>
            </ImageBanner>
          </div>
          <h2
            class="text-3xl tracking-wide font-quickbold pt-10 pb-5 text-center"
          >
            Videos
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <ImageBanner
              colored="true"
              wrapper="col-span-1"
              title="(Trechos do filme 1618 de Luís Ismael)"
              data="sala3/video1.mp4"
              thumbnail="sala3/video_1_thumb.png"
            >
              <p slot="text"></p>
            </ImageBanner>
            <ImageBanner
              colored="true"
              wrapper="col-span-1"
              title="(Trechos do filme 1618 de Luís Ismael)"
              data="sala3/video2.mp4"
              thumbnail="sala3/video_2_thumb.png"
            >
              <p slot="text"></p>
            </ImageBanner>
          </div>
          <h2
            class="text-3xl tracking-wide font-quickbold pt-10 pb-5 text-center"
          >
            Fontes Primárias
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <ImageBanner
              title="Primeira denúncia: Joanna Fernandes contra Branca Dias"
              data={[
                "sala3/primeira_denuncia_1.jpg",
                "sala3/primeira_denuncia_2.jpg",
                "sala3/primeira_denuncia_3.jpg",
              ]}
            >
              <p slot="text">
                Transcrição da Primeira Denúncia - Joanna Fernandes contra
                Branca Dias: “3 de Novembro de 1593. Joanna Fernandes contra
                Branca Dias dixe ser cristaa velha, natural de Africa filha de
                Antonio Mendes africano, defunto e de sua molher Ines Fernandes
                africana, de ydade de cinquoenta annos pouco mais ou menos,
                casada com Alvaro Gonçalves Velludo, lavrador morador nesta
                villa abaixo da matriz, e denunciando dixe que averá trinta e
                quatro ou trinta e cinquo annos que indo ella aprender a coser e
                lavrar a casa de Branca Dias cristaã nova ora já defunta ; cujas
                filhas Ines Fernandes que despois casou com Balthesar Leitão e
                Guimar Fernandes tambem óra já defuntas que então erão solteiras
                insinavão a lavrar e cozer em casa da ditta sua mãi Branca Dias,
                ella denunciante vio no ditto tempo que na sua casa andou
                aprendendo que seria espaço de hum anno que a ditta Branca Dias
                guardava os sabbados, porque sendo costume da ditta Branca Dias
                em todos os outros dias da semana fiar algodão e andar vestida
                do seu vestido da semana, ella denunciante vio a ditta Branca
                Dias nos sabbados de todo o ditto anno que em huma casa
                aprendeo, não fiar nunca e vio que nos dittos sabbados pella
                menhaã se vestia com camisa lavada e apertava à cabeça com seu
                toucado lavado e vestia nelles ho melhor vestido que tinha que
                era huma saia azul clara que ella tinha de festa a qual não
                costumava vestir nos dias da semana, e por quanto ella
                denunciante sabia ser a ditta Branca Dias cristaa nova e dizerem
                que viera com suas filhas, e marido por caso da Inquisição pera
                este Brasil tinha suá sospeita della e lhe parecia mal ver lhe
                fazer o sobreditto e por isso atentava nella nos sabados, e que
                outrossi em todo o ditto tempo que em sua casa aprendeo a ditta
                Branca Dias mãodava nas sestas feiras á tarde (segundo sua
                lembrança era nas sestas feiras á tarde) layar e esfregar o
                sobrado, por ella denunciante e por outras moças suas
                condiscipulas, e ellas lhe esfregavão o sobrado hum dia em cada
                semana que segundo sua lembrança era nas sestas feiras á tarde e
                nas mesmas sestas feiras á tarde mandava a ditta Branca Dias,
                lavar a louça da casa pellas suas negras, e outrosi vio que nos
                sabbados jantava a ditta Branca Dias mais cedo que nos outros
                dias e nos sabados chamava acima do sobrado as dittas suas
                filhas e as outras filhas mais imoças que então tinha, e , todos
                hiam então acima jantar 'com ella sendo costumadas a nunca irem
                jantar com ella nos outros dias da semana e nos dittos sabbados
                jantavão sempre huă iguaria que nunca comiam, nos outros dias da
                semana, a qual iguaria era amarella, a qual deziam as dittas
                suas filhas mais moças que se fazia com grãos pisados, e a carne
                picada e adubos, e que sómente nos dittos sabbados á tarde vio
                ella denunciante 32 Contra Branca Dias que ha ditta Branca Dias
                fazia em novellos as maçarocas do fiado de algodão que tinha
                fiado de semana e nos sabbados pellas menhãas não trabalhava
                nada e por dizer que mais lhe não lembra foi perguntado que
                filhas mais são as que ella diz que então era mais moças que as
                já nomeadas, dixe que erão duas outras mais que já são mortas, e
                que não se affirma se era alguma dellas Ana Jorge fiiha da ditta
                Branca Dias que inda óra esta viva nesta villa e casada com hum
                homem cujo sobrenome he Sousa e assim outra alcorcovada que
                nunca casou, e perguntada mais pello senhor visitador se lhes
                vio fazer mais outras cousas e cerimonias da ley de Moises das
                quais lhe declarou algumas, respondeo que so no que ditto tem
                atentou então e que nada mais lhe lembra e perguntada mais dixe
                que então era inda vivo ho marido da ditta Branca Dias, Diogo
                Fernandes e que não sabe ora viva nenhua das moças que então
                erão com ella condiscipulas, e foi lhe mandado ter segredo.”
              </p>
            </ImageBanner>

            <ImageBanner
              title="Segunda denúncia: Beatriz Luis contra Branca Dias (2ª p.)"
              data="sala3/segunda_denuncia.jpg"
            >
              <p slot="text">
                Transcrição da Segunda Denúncia - Beatriz Luis contra Branca
                Dias: “3 de Novembro de 1593. Beatriz Luis contra Branca Dias
                disse ser cristaa velha natural desta Capitania filha de Luis
                Gonçalves dos da governança desta terra , e de Maria Ferreira,
                defunctos de ydade de cinquoenta e quatro annos pouco mais ou
                menos veuva molher que foi de Fernão dAfonso, carpinteiro,
                moradora nesta villa na Rua do Salvador. E denunciando dixe que
                averá trinta annos pouco mais ou menos que ella era vezinha de
                Branca Dias 'cristaa nova molher de Diogo Fernandes cristão novo
                defuntos os quaes era fama pubrica ditto geralmente por todos
                nesta terra assi bons e honrados e milhores della como da mais
                calidade de gente e povo que ella Contra Branca Dias 33 viera
                degradada pera este Brasil pella Santa Inquisição de Lisboa e
                que elle viera fugido, e morando elles na ditta sua rua duas
                casas alem donde ella denunciante mora hum seu neto moço de
                ydade que então seria de cinquo ou seis annos, dixe muitas vezes
                perante ella denunciante á sua porta e dentro em sua casa que a
                dita sua avó Branca Dias tinha debaixo do chão huns santinhos
                assim como pacas, aos quaes adorava, o qual moço era filho de
                hua sua filha molher de Bastiam Coelho dalcunha o Boas Noites,
                as quais pacas são huns animais do mato desta terra que pouco
                mais ou menos tem o parecer de lebres, e por quanto o ditto seu
                neto dezia as dittas pallavras em todas as partes onde se achava
                creceo a fama das mesmas pallavras que a ditta sua avó Branca
                Dias tinha huns santinhos como pacas, entanto que geralmente se
                dizia isto por todos asim bons, honrados e melhores, como mais
                gente do povo desta terra mui frequentemente e depois de o
                sobreditto passar assim mãodarão ao ditto moço pera a cidade do
                Porto e nunca mais tornou a esta terra, e que outrosim ha mais
                de vinte annos que pella sobreditta maneira foi fama pubrica
                nesta terra que hum filho da ditta Branca Dias que andava em
                Lixboa sem braços e escrevia com ho pee era fugido pera Gulfo.
                Denunciou mais que ha muitos annos estando morrendo o ditto
                Diogo Fernandes ella denunciante se achou presente á ditta sua
                morte e estando presente Joam Bras que já he defunto, o ditto
                Joam Bras tendo na mão ho crucifixo o punha diante dos olhos do
                ditto Diogo Fernandes dizendo- lhe com elle pallavras devotas e
                que chamasse pello nome de Jesu, o ditto Diogo Fernandes nunca
                nomeou o nome de Jesu nem oulhou dereito pera ho crucifixo mas
                virava o rosto pera hua parte e outra, e assim na mesma ora
                morreo, e por não dizer mais foi The mandado ter segredo e do
                costume dixe nada.”
              </p>
            </ImageBanner>
          </div>

          <h2
            class="text-3xl tracking-wide font-quickbold pt-10 pb-5 text-center"
          >
            Extras
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <ImageBanner
              title="Quadro Práticas Judaizantes Família Dias-Fernandes"
              data={[
                "sala3/quadro_praticas_1.png",
                "sala3/quadro_praticas_2.png",
              ]}
            >
              <p slot="text"></p>
            </ImageBanner>
            <ImageBanner
              title="Quadro Práticas Judaizantes Família Dias-Fernandes"
              data={"sala3/sobrenomes.png"}
            >
              <p slot="text"></p>
            </ImageBanner>
            <div />
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
