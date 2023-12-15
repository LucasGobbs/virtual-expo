<script>
  import Section from "../components/Section.svelte";
  import { onMount, tick } from "svelte";
  import ImageBanner from "../components/ImageBanner.svelte";
  import { slide, fade, blur } from "svelte/transition";
  import * as animateScroll from "svelte-scrollto";
  import { content } from "../utils/content";

  const section = content["sala2"];
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
      <div class="px-5 h-screen-80 flex flex-col items-center">
        <h2
          class="transition delay-50
            text-5xl tracking-wide font-quickbold py-10"
        >
          Acervo
        </h2>

        <!-- <div>Icons made by <a href="https://www.flaticon.com/authors/ilham-fitrotul-hayat" title="Ilham Fitrotul Hayat">Ilham Fitrotul Hayat</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div><div>Icons made by <a href="https://www.flaticon.com/authors/pixel-perfect" title="Pixel perfect">Pixel perfect</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div><div>Icons made by <a href="https://www.flaticon.com/authors/bomsymbols" title="BomSymbols">BomSymbols</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div> -->
        <div class="w-2/3 justify-center">
          <h2 class="text-3xl tracking-wide font-quickbold pt-10 text-center">
            Imagens
          </h2>
          <h2 class="text-sm tracking-wide font-quickbold py-2 text-center">
            Contexto Geral
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <ImageBanner title="Bruxas de Salém" data="sala2/bruxas_salem.jpg">
              <p slot="text">Cena do filme "As bruxas de Salém"</p>
            </ImageBanner>
            <ImageBanner
              title="Julgamento de bruxaria"
              data="sala2/julgamento_bruxaria.jpg"
            >
              <p slot="text">
                Julgamento de bruxaria. Retrato de 1692, por Granger
              </p>
            </ImageBanner>
            <div class="row-span-2">
              <ImageBanner
                title="A Bruxa (Albrecht Durer) "
                data="sala2/a_bruxa_albrecht_durer.png"
              >
                <p slot="text">
                  Na Idade Média, a feiticeira era vista como uma mulher
                  criminosa, perversa, ignorante e supersticiosa. Ligadas a
                  crenças pagãs arraigadas, especialmente nas áreas rurais,
                  essas mulheres, devido à sua condição social frágil e falta de
                  conhecimento, eram mais propensas a se envolver em práticas
                  supersticiosas e ilusões atribuídas ao Diabo. A crença em
                  encontros noturnos liderados por uma divindade pagã persistiu
                  por muito tempo, levando as mulheres que compartilhavam dessas
                  crenças a serem rotuladas como loucas pelas autoridades
                  religiosas da época. <br /><br /> Assim, a feiticeira medieval
                  era associada a curandeiras rurais, mulheres idosas e
                  solitárias imersas em superstições, provocando desconfiança e
                  medo na sociedade em que viviam. Apesar de alguns casos de
                  repressão violenta, elas não atraíam muita atenção das
                  autoridades eclesiásticas. <br /><br /> Na cultura
                  eclesiástica, qualquer forma de magia era considerada
                  inaceitável. Em Roma, a prática da magia era estritamente
                  proibida pelas leis romanas. O crime de magia era punido
                  severamente na tradição jurídica latina. A Lei das XII Tábuas,
                  escrita numa sociedade agrária, condenava aqueles que usavam
                  feitiçaria para roubar colheitas ou causar danos a outros,
                  resultando na pena de morte por açoitamento. Em 81 a.C., Sila
                  instituiu a Lex Cornelia de sicariis et veneficiis, marcando
                  ações legais contra a magia, punindo aqueles que atentavam
                  contra a vida de alguém ou utilizavam veneno para o
                  assassinato, chamado de "veneficium". <br /><br /> Entretanto,
                  a Europa não apenas foi um berço da civilização, mas também um
                  berço de superstições, magia, crenças e mitos. Até os séculos
                  XIII-XIV, a feitiçaria era condenável, mas não era considerada
                  diabólica. A construção da imagem da feiticeira na Europa
                  estava profundamente ligada à visão e atitudes masculinas em
                  relação às mulheres, marcadas por contradições entre veneração
                  e hostilidade, às vezes violentas e repressoras, fruto de uma
                  natureza ambígua. <br /><br /> A bruxaria na Europa representou
                  uma transição entre o final da Idade Média e o início da era moderna,
                  perdurando até o século XVII, quando o Iluminismo começou a transformar
                  fundamentalmente a visão de mundo. Estreitamente ligada a questões
                  sociais e culturais, somente a partir do século XV é que práticas
                  de feitiçaria e heresia se mesclaram no novo delito de bruxaria.
                </p>
              </ImageBanner>
            </div>
            <div />

            <ImageBanner
              title="Jovem acusada em 1869"
              data="sala2/jovem_acusada.jpg"
            >
              <p slot="text">
                Retrato de uma jovem acusada em 1869 / Crédito: Thomas
                Satterwhite Nobel
              </p>
            </ImageBanner>
          </div>
          <h2
            class="text-sm tracking-wide mt-10 font-quickbold py-2 pt-8 text-center"
          >
            Brasil
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <ImageBanner title="Calundu" data="sala2/calundu.png">
              <p slot="text">
                A maioria dos processos envolvendo feitiçaria tratava de
                práticas individuais ligadas a técnicas mágicas e orações.
                Raramente faziam menção explícita a pactos com o demônio,
                reuniões noturnas ou práticas coletivas de ritos e cerimônias
                religiosas.
              </p>
            </ImageBanner>
            <ImageBanner
              title="Ilustração de Kleber Sales/AH"
              data="sala2/ilustracao_kleber_sales_1.png"
            >
              <p slot="text">
                A presença do Tribunal do Santo Ofício no Brasil foi
                representada pelas autoridades eclesiásticas locais, que tinham
                a autonomia para identificar casos de desobediência à fé,
                conduzir investigações preliminares e prender suspeitos,
                encaminhando-os para Lisboa, onde o processo era finalizado.
                Essa estrutura operou entre os séculos XVI e XVIII. Embora a
                sede estivesse distante, a Inquisição demonstrou sua influência
                de forma muito próxima, especialmente quando enviava
                funcionários para visitas a áreas cruciais da Colônia.<br />
                <br /> Essas visitas eram eventos de grande importância. A chegada
                do emissário mobilizava a população e gerava procissões. Acompanhado
                por um séquito numeroso, o visitador era recebido em uma residência
                central, onde o governador-geral, autoridades de alto escalão, juízes,
                bispos, vigários e missionários se apresentavam em sinal de respeito.
              </p>
            </ImageBanner>
            <div class="row-span-2">
              <ImageBanner title="Teste" data="sala2/tela_rugendas.png" />
            </div>
            <div class="col-span-1">
              <ImageBanner title="Teste" data="sala2/calundu_carlos.jpg" />
            </div>
            <ImageBanner
              title="Teste"
              data="sala2/ilustracao_kleber_sales_2.png"
              ><p slot="text">
                Em 1591, a chegada do primeiro dos quatro enviados parou
                Salvador. Heitor Furtado de Mendonça foi recebido sob um pálio
                de tela de ouro e, ao entrar na Sé, recebeu elogios à sua pessoa
                e ao Santo Ofício. Dirigiu-se à capela-mor, após a leitura da
                constituição de Pio V em favor da Inquisição, onde um altar
                ricamente adornado com uma cruz de prata erguida e quatro
                castiçais grandes, também de prata, com velas acesas, além de
                dois missais abertos em almofadas de damasco com duas cruzes de
                prata. Em meio a todo esse esplendor, o visitador se dirigiu ao
                topo do altar, sentou-se em uma cadeira de veludo trazida pelo
                capelão e recebeu o juramento do governador, juízes, vereadores
                e outros funcionários, todos ajoelhados diante do Santo Ofício.
                Mendonça chegou preocupado, após ter lido um texto de padre
                Antônio Vieira que afirmava que no Brasil "não se guardava um só
                mandamento de Deus e muito menos os da Igreja".<br />
                <br /> O início das visitas marcava o "Tempo da Graça", um
                período de até 60 dias em que todos eram "convidados" a se
                manifestar. Cópias do monitório, documento que listava os
                "crimes" sujeitos a investigação, eram afixadas nas ruas,
                incluindo blasfêmias, sacrilégios, transgressões sexuais e
                judaísmo. Quanto mais rápido a pessoa se apresentava, menos
                suspeitas levantava contra si.<br />
                <br /> Contudo, essa festa inicial logo se transformava em
                tensão. As denúncias eram anônimas, o que tornava esse momento
                propício para vinganças. Uma mulher trocada pelo marido, por
                exemplo, poderia denunciá-lo por bigamia (também havia casos de
                denúncias de homens abandonados por suas esposas). Comerciantes
                passados para trás nos negócios poderiam sugerir que seus
                concorrentes praticavam o judaísmo. Escravos denunciavam seus
                senhores por sodomia. À medida que as acusações se acumulavam,
                os suspeitos eram levados diante do visitador, muitas vezes sem
                saber qual suposto crime estavam sendo acusados. No século XVII,
                um homem acusado de homossexualidade confessou judaísmo por
                acreditar que essa era a razão da denúncia. Acabou sendo julgado
                pelos dois crimes.<br />
                <br /> Tradicionalmente, são citadas três visitas ao Brasil. A
                primeira, entre 1591 e 1595, passou pela Bahia, Pernambuco,
                Itamaracá e Paraíba, num momento em que a União Ibérica enviava
                vários inquisidores às suas colônias. A segunda, de 1618 a 1621,
                liderada por dom Marcos Teixeira, retornou à Bahia, desta vez
                com maior foco na busca por cristãos-novos. A terceira, de 1763
                a 1769, visitou a província do Grão-Pará e Maranhão, tendo sede
                em Belém.<br />
                <br /> Os arquivos dessas investigações estão na Torre do Tombo,
                em Portugal, citando 40 mil nomes de pessoas perseguidas, mas
                sem classificação por local de nascimento. Não está claro se
                essas foram as únicas visitas.<br />
                <br /> Entre 1627 e 1628, foi descoberta outra visita, que passou
                pelo Rio de Janeiro (onde o visitador Luís Pires da Veiga foi ameaçado
                de apedrejamento pela população), São Paulo e São Vicente. Certamente,
                existem outras visitas das quais os registros ainda não foram encontrados,
                além dos que se perderam em naufrágios. No entanto, é certo que a
                Inquisição teve um grande impacto na vida da Colônia. Sua ação se
                fez sentir em todo o Brasil desde o início da colonização até o século
                XVIII, mesmo em capitanias que nunca foram visitadas, como Minas
                Gerais e Ceará. A extinção formal ocorreu em 1821.
              </p>
            </ImageBanner>
            <div class="col-span-1">
              <ImageBanner
                title="Ilustração de Kleber Sales/AH"
                data="sala2/tela_debret.png"
              />
            </div>

            <div class="col-span-2">
              <ImageBanner title="Teste" data="sala2/documentos_judaizar.jpg" />
            </div>
            <div class="col-span-1"></div>
            <div class="col-span-1">
              <ImageBanner title="Teste" data="sala2/padroes.jpg" />
            </div>
          </div>

          <h2 class="text-3xl tracking-wide font-quickbold pt-10 text-center">
            Videos
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <div />
            <ImageBanner
              title="Video de Bruxa"
              thumbnail="sala2/video_bruxa_thumb.png"
              data="sala2/video_bruxa.mp4"
            >
              <p slot="text">test</p>
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
