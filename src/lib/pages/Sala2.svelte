<script>
  import Section from "../components/Section.svelte";
  import { onMount, tick } from "svelte";
  import ImageBanner from "../components/ImageBanner.svelte";
  import { slide, fade, blur } from "svelte/transition";
  import * as animateScroll from "svelte-scrollto";
  import { content } from "../utils/content";

  const section = content["sala2"];
  let element;

  import { Sound } from "svelte-sound";

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
        class="px-5 h-screen-80 flex flex-col items-center {section.acervoTint}"
      >
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
          <h2
            class="text-sm tracking-wide mt-4 font-quickbold py-2 pt-2 text-center"
          >
            Contexto Geral
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <ImageBanner title="Bruxas de Salém" data="sala2/bruxas_salem.jpg">
              <p slot="text">Cena do filme "As bruxas de Salém" (1996).</p>
            </ImageBanner>
            <ImageBanner
              title="Julgamento de bruxaria"
              data="sala2/julgamento_bruxaria.jpg"
            >
              <p slot="text">
                Julgamento de bruxaria. Retrato de 1692, por Granger.
              </p>
            </ImageBanner>

            <ImageBanner
              title="Jovem acusada em 1869"
              data="sala2/jovem_acusada.jpg"
            >
              <p slot="text">
                Retrato de uma jovem acusada em 1869 / Crédito: Thomas
                Satterwhite Nobel.
              </p>
            </ImageBanner>
          </div>
          <h2
            class="text-sm tracking-wide mt-4 font-quickbold py-2 pt-8 text-center"
          >
            Brasil
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <div />

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
            <ImageBanner title="Padrões e habitos" data="sala2/padroes.jpg">
              <p slot="text">
                Os padrões e hábitos criminosos utilizados pela Inquisição nos
                Domínios de Espanha e Portugal. Gravura, 1748.
              </p>
            </ImageBanner>
          </div>
          <h2
            class="text-3xl tracking-wide font-quickbold pt-10 pb-5 text-center"
          >
            Visitas pastoriais e do Santo Ofício no Brasil
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
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
            <ImageBanner
              title="Ilustração de Kleber Sales/AH"
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
          </div>

          <h2
            class="text-3xl tracking-wide font-quickbold pt-10 pb-5 text-center"
          >
            Casos
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <div />
            <ImageBanner
              title="Tela de Debret (Apenas Ilustrativo)"
              data="sala2/tela_debret.png"
            >
              <p slot="text">
                O ano era 1754 e o local, a Justiça Eclesiástica, na cidade de
                Jundiaí, interior de São Paulo. As rés, Thereza Leyte e
                Escholástica Pinta da Silva, mãe e filha, estão no tribunal do
                Santo Ofício acusadas de terem feito um pacto com o demônio e
                matado o primeiro marido de Escholástica, Manoel Garcia,
                utilizando feitiçarias. Essas mulheres enfrentaram acusações de
                feitiçaria, e nos registros constam algumas práticas atribuídas
                a elas. Por exemplo, relatos mencionam que 'Escholastica causou
                feridas nas pernas do marido simplesmente ao tocá-las', ou ainda
                'deixou-o cego apenas por tocar nos olhos dele'. Há também
                menções de que 'Manoel Garcia sentiu enjoos e dores no estômago
                após a mulher mexer com as mãos em um prato de comida dele'.<br
                /><br /> O processo contra Thereza e Escholastica foi iniciado oito
                anos após a morte de Garcia, e a Justiça Eclesiástica ouviu testemunhas,
                todas do sexo masculino. Estigmatizar mulheres, e ocasionalmente
                homens, era um passo crucial na construção coletiva do estereótipo
                da feitiçaria. Apesar das tensões com a Igreja, as testemunhas defenderam
                as acusadas. Alegaram que Manoel faleceu de lepra e que Francisco,
                autor das acusações, já tinha sido preso e punido por difamar as
                duas mulheres. Inclusive, elas receberam um pedido público de desculpas
                dele. Após a conclusão do processo em 1755, Thereza e Escholastica
                foram consideradas inocentes, e os familiares de Manoel arcarem com
                as despesas judiciais. Sob uma perspectiva histórica, esse documento
                revela a fragilidade e vulnerabilidade das mulheres após a morte
                de uma figura masculina dominante.
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
              <p slot="text">
                Trechos do filme: “O Martelo das Bruxas” (1970), de Otakar Vávra
                - No século XVII, em um condado na região da República Tcheca,
                uma mendiga tenta roubar uma hóstia para realizar um ritual,
                desencadeando uma série de julgamentos e perseguições pela
                Inquisição. O filme é baseado em registros históricos autênticos
                de diversos processos contra pessoas acusadas de bruxaria - os
                depoimentos dos réus são transcrições desses registros.<br /><br
                />
                A obra é impactante ao retratar de maneira crua como os julgamentos
                eram conduzidos pelos inquisidores, detentores de poder supremo.
                Por meio de torturas brutais, os acusados acabavam confessando qualquer
                coisa indicada pelos inquisidores, inclusive denunciando pessoas
                sugeridas por eles. Na trama, um estalajadeiro sem educação formal
                e moral duvidosa, que outrora foi inquisidor, é designado para liderar
                o julgamento da mendiga. Ele a coage a delatar vizinhos e conhecidos,
                desencadeando uma cadeia de acusações que leva à condenação à morte
                de metade do condado. Isso inclui indivíduos influentes e desafetos
                - todos aqueles que, por bom senso ou compaixão, se opunham aos interesses
                do inquisidor.
                <br /><br />O trecho destacado traz duas cenas distintas:
                primeiro o interrogatório de Susana, antes da tortura, para que
                ela confesse a bruxaria e as relações pecaminosas com um padre
                (que era inocente, mas er aum desafeto do inquisidor). Depois,
                Susana é mostrada já profundamente afetada pelas torturas e
                confessando tudo aquilo que lhe foi apresentado e questionado.
              </p>
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
